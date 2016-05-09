---
layout: post
title:  "How to manage your audit logs"
<<<<<<< Updated upstream
date:   2016-03-29 23:00:00
last_modified_at:  2016-04-06 12:06:92
=======
date:   2016-03-29 10:00:00
last_modified_at:  2016-03-29 10:00:00
>>>>>>> Stashed changes
excerpt: "Manage audit logs with Enter Cloud Suite."
categories: logs
tags:
image:
  feature: logs.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---

1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Projects** on the left menu. Note that only master user can manage users and projects and logs. 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-logs-auditlogs-01.png">

3. Choose the project for which you want to enable logs

4. Select log level you want choosing from **Basic and Advanced**
    * Basic level is to trace only object storage operations (Upload and Delete)
    * Advanced level is to trace all object storage and security group operations
Press OK to confirm.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-logs-auditlogs-02.png">

5. Logs are collected and archived inside two new containers (Audit_Logs and Firewall_Logs) for the project choosen in the step above.

6. To access to these logs just click on **Object Storage > Containers** on the left menu
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-logs-auditlogs-03.png">