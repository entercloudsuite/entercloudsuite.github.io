---
layout: post
title:  "How to snapshot your instance"
date:   2016-03-29 23:00:00
last_modified_at:  2016-04-06 12:06:92
excerpt: "Snapshot your instance with Enter Cloud Suite."
categories: computing
tags:
image:
  feature: snapshot.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---
Instance snapshots are a simple way to create a **full copy of your instance** for disaster recovery purposes. Since snapshots rely upon the Openstack Object Storage (Swift), instance copies are moved to the ECS object storage cluster.

Once an user triggers an instance snapshot, the instance is stored both locally and in two more remote datacenters, being **immediately available for restore in any region**. Thanks to Enter Cloud Suite architecture, the object storage cluster spans ober three autonomous regions in three different EU countries (Italy, Germany, Netherlands), and allows to seamlessly replicate data geographically. 

Should you have any compliance or regulation driven country boundary limitation, you can still avoid this replication by adopting volume-backed instances ("Diskless flavors" or "boot from volume"), a specific type of instances that store the image file and snapshots in a block storage volume, therefore locally to the current region.

### SINGLE SNAPSHOT - QUICKSTART

1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Computing > Instances** on the left menu.

3. Find the instance you want to take a snapshot of and **click on the grey icon on the right**.

4. From the dropdown menu, choose **Create Snapshot**.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-01.png">

5. Enter the name you want give to your snapshot in the pop-up text box.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-02.png">

6. **Click on OK** and the snapshot creation job will be queued.

7. To check your existing snapshots, click on the **Computing > Snapshots** menu on the left.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-03.png">

### ALTERNATIVE PATHS

#### Instance Detail Menu

1. You can access the snapshot function also from your instance details: select **Computing > Instances > [click on your instance name] > Snapshots ** and click on the green **Take** button.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-04.png">

2. Define your snapshot name and choose the snapshot retention time, in days. Note: In the duration field **0** means the retention for this snapshot will be infinite, **1** means that the snapshot will be deleted exactly 24 hours and 0 minutes after it has been completed.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-05.png">

#### Snapshot Summary Menu

1. You can access the snapshotting function also from your **Snapshots** page: select **Computing > Snapshots** and click on the green **Take Snapshot** button on top right.

2. Insert your snapshot name, select the instance you want to snapshot and define the snapshot retention.