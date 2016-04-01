---
layout: post
title:  "How to share your containers"
date:   2016-03-29 18:00:00
last_modified_at:  2016-03-29 18:00:00
excerpt: "Share your containers with Enter Cloud Suite."
categories: Object Storage
tags:
image:
  feature: share-containers.jpg
  topPosition: -50px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---
Containers are HTTP-based folders that contain files only for authenticated access. Nevertheless, users may want to provide public HTTP access to container contents, as if they were web server folders. In this case, there's an option to remove authentication for specific containers: every object can be then presented as an unique public URL, and be integrated into web applications for static content (images, .css or .js) or as an origin for a CDN.

1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Object storage > Containers** on the left menu

3. Find the container you want to make public, and click on the grey icon next to it
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-object-storage-share-containers-01">

4. Confirm and click OK

5. Now the container is listed as **Public** in the **Access** column

6. To retrieve a single object URL, enter the container, find the file you want to publish and click on the grey icon on the right, the select **Share**
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-object-storage-share-containers-02">

7. In the popup form, choose if you want to share a plain link (green icon) 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-object-storage-share-containers-03">

8. If you want to provide someone access to container by sending the link via email, click the blue icon
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-object-storage-share-containers-04">

9. Define the expiration for the public URL

10. If you want to verify your active and previous shares, go to **Object storage > Shares**, where you can also verify if a link has been opened and how many times.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-object-storage-share-containers-05">