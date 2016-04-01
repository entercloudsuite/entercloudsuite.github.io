---
layout: post
title:  "How to manage your containers"
date:   2016-03-29 19:00:00
last_modified_at:  2016-03-29 19:00:00
excerpt: "Manage your containers with Enter Cloud Suite."
categories: object-storage
tags:
image:
  feature: create-containers.jpg
  topPosition: -50px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---
1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Object storage > Containers** on the left menu.

### CREATE A CONTAINER

1. Click on **Create a container** on top right

2. Insert the name for your new container
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-object-storage-create-containers-01">

3. Select the storage policy you want to apply to the new container:
    * Standard Replica EU - 3 copies of data, one per region
    * High Replica EU - 5 copies of data, one per region plus two additional copies randomly dispersed
    * Standard Replica ITA - 3 copies of data, all in Italy, each on different storage nodes and drives

4. Click on **Create Container**

### BROWSE AND MANAGE CONTAINERS

1. Click on **Object storage > Containers** on the left menu

2. Click on the name of your new container to list its contents

3. To upload a file, click on **Upload file**, on top left

4. To download a file, click on the grey icon next to the file name and select **Download**
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-object-storage-create-containers-02">

5. To copy or cut and paste a file, click on the grey icon next to the file name and select **Copy/Move**. Change the name or select a different sub-folder in order to copy or move the file.

6. To create a folder, click on **Create folder**

### DELETE A CONTAINER

1. Click on **Object storage > Containers** on the left menu

2. Click on the name of your new container to list its contents

3. Click on the red bin icon on the right

