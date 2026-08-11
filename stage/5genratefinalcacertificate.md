---
title: 05. Generate Final ca bundle certificate
description: 
published: true
date: 2026-03-03T12:17:27.042Z
tags: 
editor: ckeditor
dateCreated: 2024-08-05T15:28:43.662Z
---

**IN ELK1:**

`Cd /etc/elasticsearch/certs/elasticsearch/`

**If there is any issue/doubt here, please copy the generated certificate again, which we generated.**

`cp ca.crt elasticsearch/`

`mv elasticsearch/ /etc/elasticsearch/certs/`

`cd /etc/elasticsearch/certs/elasticsearch`

![](images/5genratefinalcacertificate-01.png)

`mv elasticsearch.crt elasticsearch_org.crt ; cat elasticsearch_org.crt ca.crt >> elasticsearch.crt ; chgrp -R elasticsearch /etc/elasticsearch/certs/`

![A black screen with white text

Description automatically generated](images/5genratefinalcacertificate-02.png)

***Verify command from image twice before run.***

***IN ELK2:***

`mv elasticsearch2.crt elasticsearch2_org.crt ; cat elasticsearch2_org.crt ca.crt >> elasticsearch2.crt ; chgrp -R elasticsearch /etc/elasticsearch/certs/`

![](images/5genratefinalcacertificate-03.png)

**IN ELK3:**

`mv elasticsearch3.crt elasticsearch3_org.crt ; cat elasticsearch3_org.crt ca.crt >> elasticsearch3.crt ; chgrp -R elasticsearch /etc/elasticsearch/certs/`

![A screen shot of a computer

Description automatically generated](images/5genratefinalcacertificate-04.png)
