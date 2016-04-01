---
layout: post
title:  "How to manage your health checks and smart records"
date:   2016-03-29 12:00:00
last_modified_at:  2016-03-29 12:00:00
excerpt: "Manage your health checks and smart records with Enter Cloud Suite."
categories: dns
tags:
image:
  feature: healthchecks.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---
1. Click on **DNS & Domains** on the left menu

2. Then click on **Add Health Check** button:
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-dns-healthchecks-02.png">

3. Choose a name, a destination IP and a protocol. We’ll use ping, but you can also do TCP checks that will verify if something is listening on a given port, or HTTP, that will check if the destination server is answering with 2xx codes.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-dns-healthchecks-03.png">

4. You will now be redirected to the summary page. As you can see, the health check has been created and it’s working.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-dns-healthchecks-04.png">

5. Let’s create our first High Availability Record. Open you domain’s details page and click on Add Record. Choose type, hostname and TTL for your record and then select **High Availability** as Role.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-dns-healthchecks-05.png">

6. A new box will appear. In an HA record, you can define a primary and a secondary record, an associate an health check to the primary one.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-dns-healthchecks-06.png">

7. It’s very simple: if the check confirms the host is alive, the DNS will answer with the primary record. When it fails, the secondary record is returned to clients.

8. You can define GEO records as well: those records will be returned based on client’s geographical proximity, and on the related health checks.

9. Finally, you can create Load Balancing records: this kind of record is similar to a weighted round-robin: clients will be returned random records from the set you define, based on the weight you specify and on the associated health checks.