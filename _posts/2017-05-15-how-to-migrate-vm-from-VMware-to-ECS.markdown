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
- Linux system (in this guide i'll be using Ubuntu 16.10 Desktop to convert the VM disks)
- qemu-utils
- virt-manager


## Steps
1. Make sure your network settings are set to automatically get DHCP and then install the cloudinit agent on your OS. 
(For example on Ubuntu 16 you can install it with `apt install cloud-init` and on Windows Machines you need to install Cloudbase-init, you need to remove the `sysprep` flag during the installation to avoid re-initializing your VM on the first boot - https://cloudbase.it/cloudbase-init/ )
Now you can export your VM from VMware into `.ova` format 
Note: For Windows based VMs you must install the stable version of VirtIO drivers ( Stable `virtio-win iso`: https://fedorapeople.org/groups/virt/virtio-win/direct-downloads/stable-virtio/virtio-win.iso ). Mount the `.iso` on the VM and proceed to install all the drivers you can find in the mounted iso (Drivers are manually installed through Windows). 

2. Extract the contents of .ova file, from Linux commandline: 
  - `tar -xvf VMware-machine.ova` 
  - `VMware-machine.ovf` 
  - `VMware-machine-disk1.vmdk`   
  - `VMware-machine.mf` 

3. Convert your VMware machine to a KVM supported format with qemu (qemi-img is available on qemu-utils, on an Ubuntu system you can just install qemu to run this command): 
```shell
qemu-img convert -O qcow2 VMware-machine-disk1.vmdk VMware-machine-disk1.qcow2
```


4. Test that your image is supported by KVM using Virt Manager:  
   - Create a new virtual machine --> import existing disk image --> Browse and select your `.qcow2` image  
   - Set up the VM settings (RAM,CPU, network using default nat)  
   - After the VM finished to boot the OS check if there are any issues with current drivers and if so proceed on the VM settings --> Add Hardware -> Storage -> Create a disk image for the virtual machine (create a small disk, for example 1GB). 
Select `Disk device` and make sure that `Bus type` is set on `VirtIO`. 
After the disk is attached, check if the guest OS has detected the disk; for this you can use the command line: 
From a cmd prompt with administrator privileges issue the command:
```shell
diskpart
``` 
Once DiskPart has loaded, issue:
```shell
list disk
```
If you can see both disks (your main drive and the VirtIO one) the driver is working. 
Shutoff the VM, proceed on the VM settings --> `IDE Disk 1` --> Advanced Options and set `Disk bus` to `Virtio`. 
Remove also the VirtIO mini disk you've created before. 
Try again to boot the machine and if it boots the image is ready to be uploaded to Swift. 

![screenshot-virt-manger.jpg](/assets/images/posts/virt-manager.png?resize=800)


5. Authenticate to Openstack API and upload your image into your tenant:
```shell
source youremail@domain-openrc.sh
```
This source file can be downloaded from the Openstack Horizon Dashboard
```shell
export OS_IMAGE_API_VERSION=1 && glance image-create --file VMware-machine.qcow2 --disk-format qcow2  --container-format bare --name "Machine from vmware" --progress
```

6. Now you can deploy your VM into our Openstack infrastructure and upon the first boot you need to check that network configuration has been set properly. 
> This step is Mandatory for Windows based systems as they require VirtIO drivers to work on KVM hypervisor whereas on Linux systems you can avoid this testing/driver installation step.        
> On Linux systems you can avoid step 4 because drivers are already compatible for KVM.