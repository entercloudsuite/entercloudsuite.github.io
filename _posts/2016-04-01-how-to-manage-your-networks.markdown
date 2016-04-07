---
layout: post
title:  "How to manage your networks"
date:   2016-03-29 23:00:00
last_modified_at:  2016-04-06 12:06:92
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
1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Networks > Networks** on the menu
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-networks-manage-networks-01.png">

3. Now Dashboard shows your networks in all ECS regions

4. Create a new network just clicking on **Create Network** 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-networks-manage-networks-02.png">

5. Choose name, region (it-mil1 / de-fra1 / nl-ams1) and address with CIDR of your LAN network. 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-networks-manage-networks-03.png">

6. This step auto create a network with the subnet that you defined and attach it to your virtual router.

7. Back to network list and now you can see the new subnet 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-networks-manage-networks-04.png">

8. You can rename network clicking on **pencil** button and delete it with red bucket icon.

9. You can configure entire virtual networks infrastructure on <a href="https://dashboard.entercloudsuite.com" target="_blank">https://horizon.entercloudsuite.com</a> in Network Tab on the left menu. 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-networks-manage-networks-05.png">