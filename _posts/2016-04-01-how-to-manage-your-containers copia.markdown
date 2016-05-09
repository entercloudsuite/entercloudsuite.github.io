---
layout: post
title:  "How to manage your containers"
date:   2016-03-29 23:00:00
last_modified_at:  2016-04-06 12:06:92
excerpt: "Manage your containers with Enter Cloud Suite."
categories: object-storage
tags:
image:
  feature: share-containers.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---
1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Object storage > Containers** on the left menu.

### CREATE A CONTAINER

1. Click on **Create a Container** on top right.

2. Choose the name for your new container
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-object-storage-create-containers-01.png">

3. Select the storage policy you want to apply to the new container:
    * Standard Replica EU - 3 copies of data, one per region
    * High Replica EU - 5 copies of data, one per region plus two additional copies randomly dispersed
    * Standard Replica ITA - 3 copies of data, all in Italy, each on different storage nodes and drives

4. Click on **Create Container**

### BROWSE AND MANAGE CONTAINERS

1. Click on **Object Storage > Containers** on the left menu

2. Click on the name of your container to get a list of its content

3. To upload a file, click on **Upload File**, on top left

4. To download a file, click on the grey icon next to the file name and select **Download**
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-object-storage-create-containers-02.png">

5. To copy or cut and paste a file, click on the grey icon next to the file name and select **Copy/Move**. Change the name or select a different sub-folder in order to copy or move the file.

6. To create a folder, click on **Create Folder**

### DELETE A CONTAINER

1. Click on **Object Storage > Containers** on the left menu

2. Click on the name of your container to get a list of its content

3. Click on the red bin icon on the right

