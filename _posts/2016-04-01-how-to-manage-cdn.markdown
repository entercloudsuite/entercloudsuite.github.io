---
layout: post
title:  "How to use the CDN"
date:   2016-03-29 23:00:00
last_modified_at:  2016-04-06 12:06:92
excerpt: "Use the Enter Cloud Suite CDN."
categories: cdn
tags:
image:
  feature: cdn.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---
1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. In the Dashboard, click on **CDN** in the left menu.

3. Once the page loads, click on the **Add Site** button on the top right.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-01.png">

4. You now have to fill the form in order to create a new CDN "site": in **Site**, you have to configure the URL you will use to distribute your static files trough the CDN. In **Origin**, you must set the existing source for your files, the one the CDN will fetch objects from:
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-02.png">

5. Let's suppose that you want to serve via the CDN static objects hosted on **www.entercloudsuite.com**: by setting "www.entercloudsuite.com" as "Site" and "static.entercloudsuite.com" as "Origin", when you will request a file (ie: http://cdn.entercloudsuite.com/logo.png) the CDN will take care of fetching it from the origin, will store the object on its nodes and serve it to you via the nearest node. On subsequent requests, until cache expiry, the origin won't be queried anymore before serving that given file.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-03.png">

6. Once the site is created, you should see the entry in the CDN section of the Dashboard.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-04.png">

7. If you want to modify the origin of the CDN Site, you can click the blue button with a white pencil.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-05.png">
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-06.png">

8. If you want to delete the CDN configuration, click on the red button: a confirmation popup will appear once done.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-07.png">
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-08.png">