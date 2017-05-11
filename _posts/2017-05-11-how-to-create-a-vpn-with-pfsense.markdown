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

1. Create two networks: one for the WAN, one for the internal LAN
2. Launch an instance with the pfSense image (image name: `pfSense 2.3.2` - ID: `010ae2b2-a948-46b8-a702-c9c4a1346afc`) with the two networks attached. 
> Please note the order of the added nics.

3. Reach the virtual terminal of the instance and follow the setup wizard on the terminal in order to setup pfSense. Remember the nic order to define which is WAN and which is LAN.
4. Once the multiselection menu appears, select the option "2"
5. Select the internal NIC
6. Setup the same address and subnet which is assigned by Neutron to the machine. You can see it from the overview of the machine in the "Instance" section of Horizon

7. In order to finish the setup, it's necessary to enable everything in the pfSense firewall in order to access the pfSense web UI; in order to do so: 
In the multisection menu, select "12"
Type:
```bash
playback enableallowallwan
playback disablereferercheck
```
You can now associate a floating IP to the instance, and by navigating to `https://<pfsense-ip-address>` you should see the pfSense login interface. Default credentials are admin/pfsense.

After the login, the first setup wizard should appear. When you terminate the procedure, go to the firewall setting to setup your rules (Firewall->Rules)

> WARNING: open the 500 and the 4500 port, UDP protocol for IPSec to work.

8. Once you are done with the IPSec configuration, insert the allow rules in the IPSec firewall rules (Firewall->Rules->IPSec)

>  You have to disable antispoofing in order to avoid your data being blocked by Neutron ports; you need to setup the "neutron" command and the environment for using it and issue:
> ```bash
> neutron port-list | grep "<YOUR-PRIVATE-IP-ON-THE-LAN-NETWORK>"
> neutron port-update <NEUTRON-ID-FROM-PREVIOUS-STEP> --allowed-address-pairs type=dict list=true ip_address=0.0.0.0/1 ip_address=128.0.0.0/1
> ```