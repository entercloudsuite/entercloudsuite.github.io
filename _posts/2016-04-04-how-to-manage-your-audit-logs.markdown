---
layout: post
title:  "How to manage your audit logs"
date:   2016-03-29 23:00:00
last_modified_at:  2016-04-06 12:06:92
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

In ECS you can enable some log about Object Storage operations ( Upload new file, Delete files, List files ecc. ) and Security Groups operations ( New rule , delete it , ecc. )

1. To enable, you have to Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a> and goes to Project Tab in left menu:
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-logs-auditlogs-01.png">

2. In every sub-project you can choose two level of logging: Basic and Advanced
    * Basic: Only limited Object Storage operations (Upload and Delete)
    * Advanced: All Object Storage operations and Security Groups operations
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-logs-auditlogs-02.png">

3. Logs will archive in two different container in previusly selected account.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-logs-auditlogs-03.png">