---
layout: post
title:  "How to boot your first instance"
date:   2016-03-29 23:00:00
last_modified_at:  2016-03-29 23:00:00
excerpt: "Create and launch your first instance with Enter Cloud Suite."
categories: computing
tags:
image:
  feature: first-instance.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---
1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Computing > Instances** on the left menu.

3. Click on **Launch instance** on top right of the dashboard.

4. Choose a name for the instance you are going to spin up.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-first-instance-03.png">

5. Select a Region you want your instance to be run into (Italy-Milano1, Germany-Frankfurt1 or Netherlands-Amsterdam1).
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-first-instance-04.png">

6. Pick a flavor to define the virtual hardware specifications (CPU, RAM and HDD) of your instance.  
**Note: if you are exceeding your configured quotas, some flavors may be grayed out accordingly.**
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-first-instance-05.png">

7. Select an image to boot your instance from: this is the software template you are going to use to run your instance. May be a standard template provided by Enter (e.g. Ubuntu Linux or Windows 2008R2) or a snapshot previously taken from a user's instance.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-first-instance-06.png">

8. Define if the instance shall be provisioned with a public Internet facing IP or with a private IP for internal use only. **Note: if you didn't provision a a router or a network (LAN or subnet)inside your tenant, the system will configure it for you. If you already set-up your single network with a single LAN, the system will pick the existing one automatically. If you configured more networks, you will be prompted to choose the one you want your instance to connect to.**
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-first-instance-07.png">

9. Define the public SSH key you are going to use to access your instance: import an existing one, create a new keypair or select an already uploaded key from the following menu. Should you choose to create a new keypair, you will be prompted to download the private key once you click on "Launch instance" at the form bottom. **Note: all SSH keypairs are visible only region-wide: if you are launching an instance in IT-MIL1, make sure the key you want to use is available in this region as well.**
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-first-instance-08.png">

10. Schedule automated backups for your instance: this feature allows you to define periodic snapshots in order to free you from the hassle of taking manual copies of your environments.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-first-instance-09.png">

#### That's it!

You're ready to proceed and click "Launch Instance". It will take around 10 seconds before your instance will be available for logon (a bit more if you chose a snapshot as an image).
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-first-instance-10.png">