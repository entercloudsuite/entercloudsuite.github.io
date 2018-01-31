---
layout: post
title:  "How to use Swift with S3 compatibility"
date:   2018-01-31 15:00:00
last_modified_at:  2018-01-31 15:00:00
excerpt: "Swift Object Storage with S3 API."
categories: object-storage
tags:
image:
  feature: support.jpg
  topPosition: 0px
bgContrast: dark
bgGradientOpacity: lighter
syntaxHighlighter: yes
---

### Intro
In the following guide we will provide some useful information to configure any S3-compatible client with EnterCloudSuite Object Storage Swift.


### How-to

1) Log into the Horizon interface (https://horizon.entercloudsuite.com/) and proceed to "Access & Security" -> API Access
2) Click on User Credentials to show your current S3 API Secrets
3) The main parameters for any S3 like client to work with our Object Storage Swift are:
   - EC2 Access Key  
   - EC2 Secret Key
   - Endpoint ( swift.{region}.entercloudsuite.com, example: swift.it-mil1.entercloudsuite.com )

4) Any compatible S3 client can connect to our S3 APIs and download/upload/manage Swift Object Storage via an S3 interface


Examples:

Windows Client running S3Browser (http://s3browser.com/ - freeware)

- Download the client from the site
- Accounts --> Add a new account --> S3 compatible storage
- Use the following settings*:
<img class="responsive-guide-img" src="{{ site.baseurl_posts_img }}ecs-s3browser.png">

Access KEY ID is EC2 Access Key
Secret KEY is EC2 Secret Key



Linux Client runnign aws cli (https://github.com/aws/aws-cl - opensource)

- Download the client from main repositories or pip install
- configure AWS credentials using Access and Secret Key
~/.aws/credentials
[default]
aws_access_key_id = <EC2 Access Key>
aws_secret_access_key = <EC2 Secret Key>
- verify that credentials are correct and working with the command:
```aws --endpoint-url https://swift.it-mil1.entercloudsuite.com s3api list-buckets```







