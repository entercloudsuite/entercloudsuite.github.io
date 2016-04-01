---
layout: post
title:  "How to manage your Floating IPs"
date:   2016-03-29 16:00:00
last_modified_at:  2016-03-29 16:00:00
excerpt: "Manage your Floating IPs with Enter Cloud Suite."
categories: networks
tags:
image:
  feature: floatingips.jpg
  topPosition: -50px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---
1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Networks > Floating IP** on the menu
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-networks-floating-ips-01.png">

3. Now you can see the list of floating ips associate to your project.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-networks-floating-ips-02.png">

4. Add a new floating ip in your project clicking **Create IP** and select the region where the IP address will be used. 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-networks-floating-ips-03.png">

5. Add a floating ip to server that not have it clicking on blue icon **Associate IP** and select the instance
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-networks-floating-ips-04.png">

6. Disassociate IP from an instance clicking on the same blue icon **Dissassociate IP** and click ok 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-networks-floating-ips-05.png">

Note: You can associate only 1 floating ip per VM.
