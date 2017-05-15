---
layout: post
title:  "How to migrate Virtual Machines from VMware to Enter Cloud Suite"
date:   2017-05-15 17:00:00
last_modified_at:  2017-05-15 17:00:00
excerpt: "Migration from VMware to ECS"
categories: migrations
tags:
image:
  feature: networks.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---

## Intro
This is the procedure to migrate virtual machines from a VMware based-infrastructure to EnterCloudSuite. 
You need to execute these steps on a Linux machine as it requires qemu emulator for conversion and Virt manager to test the image if the Operative System doesn't automatically load KVM drivers. 

## Requirements
- Linux OS (in this guide i'll be using Ubuntu 16.10 Desktop to convert the VM disks)
- qemu-utils
- virt-manager


## Steps
1. Before exporting the image, make sure the network settings of your VM are set to automatically get a dynamic address from DHCP and then install the cloudinit agent on the guest OS.<br>
  - on Ubuntu 16 install it with `apt install cloud-init`
  - on Windows install the stable version of VirtIO drivers _`virtio-win iso`_(https://fedorapeople.org/groups/virt/virtio-win/direct-downloads/stable-virtio/virtio-win.iso), install `cloudbase-init`(https://cloudbase.it/cloudbase-init/) and remove the `sysprep` flag during the installation, in order to avoid re-initializing your VM on the first boot<br>
Now you can export your VM from VMware into `.ova` format.<br>
<br>
2. Extract the contents of the `.ova` file, using the Linux command line: 
  - `tar -xvf VMware-machine.ova` 
  - `VMware-machine.ovf` 
  - `VMware-machine-disk1.vmdk`   
  - `VMware-machine.mf` 
<br>
<br>
3. Convert your VMware machine to a KVM supported format with `qemu` (`qemu-img` is available from the  `qemu-utils` binary package): 
```shell
qemu-img convert -O qcow2 VMware-machine-disk1.vmdk VMware-machine-disk1.qcow2
```
<br>   
4. 
<br>  
> This step is Mandatory for Windows based systems as they require VirtIO drivers to work on KVM hypervisor whereas on Linux systems you can avoid this testing/driver installation step. 
> On Linux systems you can avoid step 4 because drivers are already compatible for KVM.

If your guest OS is Windows, on your local machine test that your image is supported by KVM using `virt-manager`:  
   - Create a new virtual machine --> import existing disk image --> Browse and select your `.qcow2` image  
   - Set up the VM settings (RAM, CPU, network using default nat)  
   - After the VM completes the OS boot check if there are any issues with current drivers and, if so, proceed to VM settings --> Add Hardware -> Storage -> Create a disk image for the virtual machine (create a small disk, for example 1GB). This step is required in order to have the `VirtIO` drivers enabled at boot
   - Select `Disk device` and make sure that `Bus type` is set on `VirtIO`
   - After you have attached the disk, check if the guest OS has detected it by using this command with admin privileges: 
    ```shell
    diskpart
    list disk
    ```
    If you can see both disks listed the driver is working properly and your main drive and the VirtIO one. 
    Shutoff the VM, switch to VM settings --> `IDE Disk 1` --> Advanced Options and set `Disk bus` to `VirtIo`. 
    Remove also the test `VirtIO` mini-disk you've created above.
    Try again and boot the machine: if it boots up the image is ready.
    You can now upload the image file (`VMware-machine-disk1.qcow2`) to Swift.
![screenshot-virt-manger.jpg](/assets/images/posts/virt-manager.png?resize=600){:class="img-responsive"} 
5. Authenticate to Openstack API and upload your image into your tenant's private image repository:
```shell
export OS_IMAGE_API_VERSION=1 && glance image-create --file VMware-machine-disk1.qcow2 --disk-format qcow2  --container-format bare --name "Import from VMware" --progress
```
<br>   
6. Now you can deploy your VM into our Openstack infrastructure by selecting your freshly uploaded template.
Upon the first boot you need to check that network configuration has been set properly. <br>  
