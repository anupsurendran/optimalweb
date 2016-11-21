---
layout: post
title: Google Cloud SQL Questions |  CPO200
tags:
- Google Cloud
- CPO200
- Storage 
- Exam Preparation
- FAQ
---


#### True or False. Cloud SQL instances can be accessed by Compute
Engine instances from multiple regions.

True. It is possible but increased latency will be an issue, as the traffic
will have further to travel between Compute Engine and Cloud SQL
instances. A Compute Engine external IP address must be in the list of
authorized networks to access a Cloud SQL instance.

#### True or False. Cloud SQL instances can only export data in mysqldump
file format.

False. Cloud SQL also supports exporting data in CSV format.

#### True or False. Statements and functions related to files and plugins are
not supported

True. Examples for first generation are :

- LOAD DATA INFILE
Note that LOAD DATA LOCALINFILE is supported.
- SELECT ... INTO OUTFILE
- SELECT ... INTO DUMPFILE
- INSTALL PLUGIN ...
- UNINSTALL PLUGIN
- CREATE FUNCTION ... SONAME ...



#### True or False. Choice of MySQL 5.5 and 5.6 is available on Google Cloud

True.



