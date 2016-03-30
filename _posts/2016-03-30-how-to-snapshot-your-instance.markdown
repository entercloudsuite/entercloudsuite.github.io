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
1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Computing > Instances** on the left menu.

3. Click on **Launch instance** on top right of the dashboard.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-01.png">

4. Choose a name for the instance you are going to spin up.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-02.png">

5. Select a Region you want your instance to be run into (Italy-Milano1, Germany-Frankfurt1 or Netherlands-Amsterdam1).
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-03.png">

6. Pick a flavor to define the virtual hardware specifications (CPU, RAM and HDD) of your instance.  
**Note: if you are exceeding your configured quotas, some flavors may be grayed out accordingly.**
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-04.png">

7. Select an image to boot your instance from: this is the software template you are going to use to run your instance. May be a standard template provided by Enter (e.g. Ubuntu Linux or Windows 2008R2) or a snapshot previously taken from a user's instance.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-05.png">

#### That's it!

You're ready to proceed and click "Launch Instance". It will take around 10 seconds before your instance will be available for logon (a bit more if you chose a snapshot as an image).