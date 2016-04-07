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

In **Site**, you have to configure the URL you will use to distribute your static files trough the CDN.

4. In **Origin**, you must set the existing source for your files, the one the CDN will fetch objects from:
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-02.png">

Let's suppose that you want you have the domain **www.example.com** and you want to reach the CDN with the URL **cdn.example.com**; in this field, add **cdn.example.com** (without quotes).
ATTENTION: in the DNS panel of your provider you have to set the record as a CNAME of **cdn.entercloudsuite.com.** (without quotes and mind the last dot).

With this configuration:
    * Site: cdn.example.org
    * Origin: http://www.example.org

When you request a file (for example, http://cdn.example.org/files/1.png), the CDN system will get the original file from the origin previously specified (in this case http://www.example.org/files/1.png) and it will cache the file. On the next request of the same file, the origin will not be queried for the file and the CDN will supply directly the file.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-03.png">

Once the configuration is created, you should see the entry in the CDN section of the dashboard.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-04.png">

If you want to modify the origin of the CDN, you have to click the blue button with a white pencil; the edit screen will appear. The only editable field is the origin URL.
If you want to edit the CDN URL, you must delete and create a new CDN entry.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-05.png">
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-06.png">

If you want to delete the CDN configuration, click on the red button with a white trash inside; a confirmation popup will appear.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-07.png">
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-cdn-08.png">