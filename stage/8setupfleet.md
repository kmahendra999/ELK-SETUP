---
title: 08. Kibana start recommendations 
description: 
published: true
date: 2026-03-03T12:17:34.014Z
tags: 
editor: ckeditor
dateCreated: 2024-08-05T16:28:01.428Z
---

**ON ELK3:**

`setcap ‘capnetbind_service=+ep’ /usr/share/kibana/node/bin/node`

![](images/8setupfleet-01.png)

Enter Command:

`crontab -e`

Enter the below given content in the file and save

`@reboot setcap 'cap_net_bind_service=+ep' /usr/share/kibana/node/bin/node`

> `This above steps are recommended also we need to do if kibana is not running.`

`systemctl status kibana`

`systemctl restart kibana`

`systemctl status kibana`

![A black screen with white text

Description automatically generated](images/8setupfleet-02.png)

When we see status the red mark line should come. else see logs what we done mistake and where.
