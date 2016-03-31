---
layout: post
title:  "How to snapshot your instance"
date:   2016-03-29 22:00:00
last_modified_at:  2016-03-29 22:00:00
excerpt: "Snapshot your instance with Enter Cloud Suite."
categories: computing
tags:
image:
  feature: snapshot.jpg
  topPosition: -50px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---
Instance snapshots are a simple way to perform a **full backup of your virtual servers** for DR recovery purposes. Since snapshots rely upon the Openstack Object Storage system (Swift), instance copies are moved from compute nodes to an object storage cluster, in a storage container.
Once a user triggers an instance snapshot, the instance is stored locally and in two more remote datacenters, being **immediately available for restore in any region**. Thanks to Enter Cloud Suite architecture, the object storage cluster spans three different regions in three different EU countries (Italy, Germany, Netherlands), and allows to seamlessly replicate data remotely, without any need for manual operations. 
Should you have any compliance or regulation driven country boundary limitation, you can still avoid this replication by adopting volume-backed instances ("Diskless flavors" or "boot from volume"), a specific type of instances that store the image file and snapshots in a block storage volume, therefore locally to the current region.

## SINGLE SNAPSHOT - QUICKSTART

1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Computing > Instances** on the left menu.

3. Find the instance you want to take a snapshot of and **click on the grey icon on the right**.

4. From the dropdown menu, choose **Create snapshot**.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-01.png">

5. Enter the name for your snapshot in the pop-up text box.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-02.png">

6. **Click on OK** and your snapshot will be queued.

7. To check your snapshots, click on the **Computing > Snapshots** menu on the left.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-03.png">

## ALTERNATIVE PATHS

#### Instance detail menu

1. You can access the snapshotting function also from your instance details: select **Computing > Instances > [click on your instance name] > Snapshots ** and click on the green **Take** button.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-04.png">

2. Insert your snapshot name and define the snapshot retention, in days. Note: In the duration field **0** means the retention for this snapshot will be infinite, **1** means that the snapshot will be deleted exactly 24 hours and 0 minutes after it has been completed.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-05.png">

#### Snapshot summary menu

1. You can access the snapshotting function also from your **Snapshots** page: select **Computing > Snapshots** and click on the green **Take Snapshot** button on top right.

2. Insert your snapshot name, select the instance you want to snapshot and define the snapshot retention. Note: In the duration field **0** means the retention for this snapshot will be infinite, **1** means that the snapshot will be deleted exactly 24 hours after it has been completed.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-06.png">.