---
title: 01. Prerequisite
description: 
published: true
date: 2026-03-03T12:17:55.729Z
tags: 
editor: ckeditor
dateCreated: 2024-08-06T17:14:31.726Z
---

Check the status of hosts / host ports which we will use:

**Decided hosts are**

|  |  |  |  |  |  |
| --- | --- | --- | --- | --- | --- |
| **Hostname** | **Pvt IP** | **Public IP** | **url** | **services** | **Port** |
| ~~test\_dr\_crx\_elk\_3~~ | ~~10.50.14.82~~ | ~~10.34.75.208~~ | ~~elk01.elkdomainname.com~~ | EL Fleet | 9200 8220 |
| ~~test\_dr\_hyd\_elk\_3~~ | ~~10.50.14.110~~ | ~~100.113.16.222~~ | ~~elk02.elkdomainname.com~~ | EL Kibana | 9200 443 |
| ~~mh-us-es-3~~ | ~~10.50.14.239~~ | ~~10.19.91.18~~ | ~~elk03.elkdomainname.com~~ | EL | 9200 |
| my-monitoring-node-alias | 10.50.14.67 | 90.142.214253 | elk.elkdomainname.com | Kibana | 5601 |

Do on all machines. (we are going to use domain names instead of IP because if in future any machine IP change then we do not need to regenerate certificates, we will just change the IP in /etc/hosts)

`echo "#Elasticsearch Domains`  
`10.50.14.82 elk01.elkdomainname.com`  
`10.50.14.110 elk02.elkdomainname.com`  
`10.50.14.239 elk03.elkdomainname.com`  
`90.142.214253 elk.elkdomainname.com" >> /etc/hosts`

make sure ports are listening on the servers.

**All work we are going to use root user, so we do not face any permission issue.**
