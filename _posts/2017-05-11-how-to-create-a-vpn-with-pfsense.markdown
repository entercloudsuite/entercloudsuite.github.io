---
layout: post
title:  "How to create a VPN with pfSense"
date:   2017-05-11 09:00:00
last_modified_at:  2017-05-11 09:00:00
excerpt: "Manage your networks with Enter Cloud Suite."
categories: networks
tags:
image:
  feature: networks.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---

This guide will work only using [Horizon](https://horizon.entercloudsuite.com/).

1. Create two networks: one for the WAN, one for the internal LAN
2. Launch an instance with the pfSense image (image name: `pfSense 2.3.2` - ID: `010ae2b2-a948-46b8-a702-c9c4a1346afc`s) with the two networks attached. We recommend at least an x2 flavor.

![Aggiungere immagine "pfsense_creazioneimmagine"](pfsense_creazioneimmagine.PNG)

<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}pfsense_creazioneimmagine.PNG">

> Please note the order of the added nics.
> In this guide we'll use `pfSense_WAN` network in NIC1 and `pfSense_LAN` network in NIC2.

Aggiungere imm "pfSenseNetwork_Wan_Lan"

3. Reach the virtual terminal of the instance, using the "Console" section of the instance, and follow the setup wizard on the terminal in order to setup pfSense. Remember the nic order to define which is WAN and which is LAN.
4. Once the multiselection menu appears, select the option “2”
5. When this message appear "Should VLANs be set up now [y|n]? you must type "N".
6. When the system will prompt "Enter the WAN interface name or 'a' for auto-detection" you need to remember the order of added nics (2nd point), in our case WAN is the first selected so we will type "vtnet0".

agg imm "pfsense_vtnet0_wan"

After that we will insert vtnet1 for the LAN interface.

agg imm "pfsense_vtnet1_lan"

Then leave an empty space when it ask "Enter the Optional 1 interface name or 'a' for auto-detection"

agg imm "pfsense_emptyspace"

Type "Y" when it ask if "you want to preceed"

agg imm "pfsense_proceed"

7. Now you need to setup the interface(s) IP address, type "2".

agg imm "pfsense_enterenoption"

8. You need to setup only the LAN address, you will see the available interfaces and you need to insert the number of the LAN interface (in our test, 2)

agg imm "pfsense_onlylan"

9. Setup the same address and subnet which is assigned by Neutron to the machine. You can see it from the overview of the machine in the “Instance” section of Horizon.
agg imm "pfsense_horizon"

(in our test the IP assigned bu Neutron is 192.168.193.4, as you can see from the image below)

agg imm "pfsense_lanip"

then you need to insert the subnet, in our case is /24 so we'll insert "24"

agg imm "pfsense_lansubnet"

Just leave the empty field in the other requests.

10. You shouldn't enable the DHCP server on LAN because when you need to create any server on the `pfSense_LAN` you will select the Network LAN `pfSense_LAN` and the server will have an IP of the same LAN subnet.

agg imm "pfsense_noenableDHCP"

You don't need to revert the HTTP as well, type "N"

agg imm "pfsense_norevert"

At this point just press Enter to finish the configuration.

agg imm "pfsense_finishlan"

11. In order to finish the setup, it's necessary to enable everything in the pfSense firewall in order to access the pfSense web UI; in order to do so:

In the multisection menu, select "12"
Type:
```bash
playback enableallowallwan
playback disablereferercheck
```
You can now associate a floating IP to the instance, and by navigating to `https://<pfsense-ip-address>` you should see the pfSense login interface. Default credentials are admin/pfsense.

After the login, the first setup wizard should appear. When you terminate the procedure, go to the firewall setting to setup your rules (Firewall->Rules)

> WARNING: open the 500 and the 4500 port, UDP protocol for IPSec to work.

12. Once you are done with the IPSec configuration, insert the allow rules in the IPSec firewall rules (Firewall->Rules->IPSec)

>  You have to disable antispoofing in order to avoid your data being blocked by Neutron ports; you need to setup the "neutron" command and the environment for using it and issue:
> ```bash
> neutron port-list | grep "<YOUR-PRIVATE-IP-ON-THE-LAN-NETWORK>"
> neutron port-update <NEUTRON-ID-FROM-PREVIOUS-STEP> --allowed-address-pairs type=dict list=true ip_address=0.0.0.0/1 ip_address=128.0.0.0/1
> ```