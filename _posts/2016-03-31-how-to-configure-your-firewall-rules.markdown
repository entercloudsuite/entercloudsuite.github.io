---
layout: post
title:  "How to configure your firewall rules"
date:   2016-03-29 21:00:00
last_modified_at:  2016-03-29 21:00:00
excerpt: "Configure your firewall rules with Enter Cloud Suite."
categories: computing
tags:
image:
  feature: firewall.jpg
  topPosition: -50px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---

1. Click on **Computing > Security** on the left menu.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-firewall-01.png">

2. Click on **Create Security Group** on top right of the screen.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-firewall-02.png">

3. Define a **name** and a **description** for your security group, then **choose the region** where you need to use it.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-firewall-03.png">

4. Your security group will now be created and you will be redirected to the main Security screen. In order to modify the security group’s rules, click on its name.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-firewall-04.png">

5. By default, there will be no rules. First of all, create a rule to allow all outgoing traffic from your instances. Fill up the required fields as per screenshot, and click on **Create Rule**.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-firewall-05.png">

6. You can then create specific rules for incoming traffic. In a **basic** use case, you would allow administrative traffic from some service IPs only, and http traffic from any source.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-firewall-06.png">
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-firewall-07.png">

7. As last step, you need to associate the new security group to the instances you want to protect with it. Go back to the instances menu, and click on the instance you need:
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-firewall-08.png">

8. Then, open the **Access & Security** tab. You should now see the “default” security group associated to the instance, and the one you created as available:
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-firewall-09.png">

9. Remove the default one, and add the new security group, then click **Save**. This should be the final setting.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-computing-snapshot-10.png">
