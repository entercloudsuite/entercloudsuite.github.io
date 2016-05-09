---
layout: post
title:  "How to change customer resource quotas"
date:   2016-03-29 23:00:00
last_modified_at:  2016-04-06 12:06:92
excerpt: "Change customer resource quotas with Enter Cloud Suite."
categories: admin-portal
tags:
image:
  feature: quotas.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---

1. Log into the <a href="https://admin.entercloudsuite.com" target="_blank">Enter Cloud Suite Admin Portal</a>.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-quotas-01.png">

2. Insert the name of a customer in the field **Customers**, in the left box
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-quotas-02.png">

3. Click on **View** button to search the customer
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-quotas-03.png">

4. Click on the name of the customer to open the detail page
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-quotas-04.png">

5. Click on the **Edit** button, in **Customer Profile** section 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-quotas-05.png">

6. Change customer resource quotas choosing the desired ranking level. There are 6 ranking level corresponding to 6 different presets of quotas:
    1 --> 1 vpcu; 1 GB; 1 instance
    2 --> 2 vpcu; 2 GB; 2 instances
    3 --> 8 vpcu; 16 GB; 8 instances
    4 --> 16 vpcu; 32 GB ; 16 instances
    5 --> 64 vcpu ; 128 GB; 64 instances
    6 --> 128 vcpu, 256 GB; 128 instances
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-quotas-06.png">

7. Click on **Save** to confirm updates

8. The quota is set concurrently for all regions and for all tenants of that customer, except for those that already exceed the new quota value. 

9. Please note that if you are trying to **downgrade** quota and there are resources in one or more region that exceed the new quota you are trying to set, this will fail in those regions. It’s up to the administrator to remove resources that exceed the quota he wants to set.