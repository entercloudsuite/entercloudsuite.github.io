---
layout: post
title:  "How to manage your resources tags"
date:   2016-03-29 23:00:00
last_modified_at:  2016-04-06 12:06:92
excerpt: "Manage resources tags with Enter Cloud Suite."
categories: Tags
tags:
image:
  feature: tags.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---
You can buy additional services such as:
* Control Panel “cPanel”
* Certificate SSL
* New Domain
* Transfer Domain

### BUY ADDITIONAL SERVICES

1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Tags** on the left menu.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-tags-01.png">

### MANAGE TAGS

1. To create a tag click on **Create** on top right 
    * Insert the tag name and choose a color
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-tags-02.png">
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-tags-03.png">
    * Tags created by master user are global  and can be used by all users. For example master user can create tags named **Frontend**,**Database** and **Backend** and then users can tag their instances using these global tags. In this way two different users, **User A** and **User B** ,for example, assigned to different projects **Staging** and **Production** can tags theirs instances with same tags.
    * Tags created by non master users are private and visibile only to the users who created them

2. To delete a tag click on delete button on the right of the tag
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-tags-04.png">
    * Please note that global tags can deleted only by master user
    * Tag deletion removes also its association with all resources but it’s not retroactive and past resource usage consumption preserve their tags.

3. Tags can be assigned to instances and volumes
    * To assign a tag to a resource click on the quick action button right to the resource and then click on **Tags**
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-tags-05.png">
    * Each resource can have up to three different tags
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-tags-06.png">
    * Assigned tags are visible directly in the resource list or inside the resource detail
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-tags-07.png">
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-tags-08.png">

4. To discover wich resources are connected to a specific tag click on **Tags** on the left menu and then click on the count number
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-tags-09.png">
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-tags-10.png">

5. Tags are reported inside the resource usage consumption export. In this way managers can use tags to filter data, create view and pivot to aggregate and summarize data.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-tags-11.png">


