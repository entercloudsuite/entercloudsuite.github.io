---
layout: post
title:  "How to get usage reports"
date:   2016-03-29 11:00:00
last_modified_at:  2016-03-29 11:00:00
excerpt: "Get usage reports with Enter Cloud Suite."
categories: report
tags:
image:
  feature: reports.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---
1. Log into the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.

2. Click on **Reports** on the left menu
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-reports-01.png">

### SCHEDULE A NEW REPORT

1. Click on **Schedule** on top right

2. Insert the name for your new report

3. Select the type of report:
    * Hourly - include usage data from the preceding hour
    * Daily - include usage data from the preceding day
    * Weekly - include usage data from the preceding week
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-reports-02.png">

4. Select the region you want to consider

5. Define the date and the time you want to execute the report. By default, the report is delivery once, but you can choose to repeat the execution every:
    * n Hours
    * Days
    * n Weeks 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-reports-03.png">

6. Reports are delivered as comma-separated values (CSV) format files to a given FTP server. To define your FTP server data, insert:
    * Url
    * Username
    * Password

7. Define the filename format, using predefined vars like:
    * %day - the date of execution in YYYYMMDD format
    * %project - the OpenStack project ID
    * %region - the selected region
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-reports-04.png">

8. Click on **Save**

### BROWSE AND MANAGE YOUR REPORTS

1. Click on **Reports** on the left menu
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-reports-05.png">

2. Click on the blue **Stop** button, on the right, to disable the execution of an active report. A stopped report could be activated, clicking on the “play” button
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-reports-06.png">

3. Click on the blue **Info** button, on the right, to show the FTP settings of each report
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-reports-07.png">

### DELETE A REPORT

1. Click on **Reports** on the left menu

2. Click on the red **bin** button on the right

3. Click on **Ok** to confirm the deletion of the selected report
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-reports-08.png">