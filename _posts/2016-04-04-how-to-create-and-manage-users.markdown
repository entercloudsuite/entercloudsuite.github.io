---
layout: post
title:  "How to create and manage users"
date:   2016-03-29 23:00:00
last_modified_at:  2016-04-06 12:06:92
excerpt: "Create and manage users with Enter Cloud Suite."
categories: admin-portal
tags:
image:
  feature: users.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---

1. Log into the <a href="https://admin.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a>.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-01.png">

### SEARCH AND BROWSE USERS

1. Insert the name or email of a customer user in the field **USERS**, in the left box
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-02.png">

2. Click on **View** button to search the user
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-03.png">

3. Click on the name of a user listed to go to his details page
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-04.png">

### VIEW AND MANAGE USERS

1. Search an user and open his detail page as seen in the previous steps
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-05.png">

2. If you want to login in user Enter Cloud Suite Dashboard:
    * Click on **Login** button
    * Click on the button to open the user Dashboard in a new window

3. If you want to force the change of the user password
    * Click on **Change password** button
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-06.png">
    * In **Password** and **Confirm Password**, type the new password
    * Click **Change** button to apply the new password

4. If you want to set the user as a Master (the master can access all the Dashboard features such as Reports and Projects/Users management):
    * Click on **Set as master** button
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-07.png">
    * Click on **Yes** button just to confirm the operation.

5. If you want to delete a project click on **Login** button next to master user. Note that only master user can delete projects inside dashboard
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-15.png">
Click on the **Delete** button on the right of the project. 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-20.png">
Note that the project that contains the master user cannot be deleted. If you need to delete that project you have to give before the **master property** to another user in a different project (either in the admin console as described in the steps before or in the dashboard clicking on the “Change master user” button).
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-21.png">
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-22.png">

6. If you want to delete a User click on **Login** button next to master user. Note that only master user can delete users inside dashboard
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-15.png">
Click on the **Delete** button on the right of the user. 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-18.png">
Note that the master user cannot be deleted. If you need to delete the master user you have to give before the “master property” to another user (either in the admin console as described in the steps before or in the dashboard clicking on the “Change master user” button).
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-19.png">

### CREATE USERS AND PROJECTS

1. Search a customer and open his detail page inserting the name of a customer in the field **Customers**, in the left box
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-08.png">

2. If you want to create a new project 
    * Click on the **Add Project** button, in the top right 
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-09.png">
    * After the creation of the project a new user would be associated to it.
    * Insert the email of the user and the name for both, the user and the project
    * In **Password** and **Confirm Password**, type the password for the new user
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-10.png">
    * Click on **Add** button to confirm the creation of the project
    * Then the new user just created has to go to the <a href="https://dashboard.entercloudsuite.com" target="_blank">Enter Cloud Suite Dashboard</a> and click on **Forget password**
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-11.JPJ">
    * Insert user’s email in edit box and then click **Reset password**
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-12.JPG">
    * The user will receive an email with a link to follow where he could set his password. The link will expire after 5 days and after that time the user need to restart the flow again and click **Forget password** again. Note that the **Forget password** doesn’t invalidate current user password which will be changed only after the completion of all steps.
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-13.JPG">
    * After he set his new password the user can log in inside the dashboard
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-14.JPG">

3. If you want to add another user in a **new project** just follow same steps above

4. If you want to add a new user inside an **existing** project 
    * Click on **Login** button next to master user. Note that only master user can add users and projects inside dashboard
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-15.png">
    * Click on the button to open the user Dashboard in a new window
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-05.png">
    * Click on **Projects** on the left menu
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-projects-and-users-01.png">
    * Choose a project in which you want to add a new user and fill the required boxes such as **Email** and **Name and Surname** and then click on **Add** button
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-admin-portal-users-17.png">
    * An email is sent to the new user email address asking him to reset his password as seen in the previous steps  


