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


#### True or False? . Cloud SQL instances can be accessed by Compute Engine instances from multiple regions.

True. It is possible but increased latency will be an issue, as the traffic
will have further to travel between Compute Engine and Cloud SQL
instances. A Compute Engine external IP address must be in the list of
authorized networks to access a Cloud SQL instance.

#### True or False? . Cloud SQL instances can only export data in mysqldump file format.

False. Cloud SQL also supports exporting data in CSV format.

#### True or False? . Statements and functions related to files and plugins are not supported

True. Examples for first generation are :

- LOAD DATA INFILE
( Please note that LOAD DATA LOCALINFILE is supported. )
- SELECT ... INTO OUTFILE
- SELECT ... INTO DUMPFILE
- INSTALL PLUGIN ...
- UNINSTALL PLUGIN
- CREATE FUNCTION ... SONAME ...



#### True or False? . Choice of MySQL 5.5 and 5.6 is available on Google Cloud

True.

#### can you identify a sequence of steps to export the data from your Cloud SQL instance using Google Cloud Storage?

- Create a Durable Reduced Availability bucket:

{% highlight bash %}
gsutil mb -cDRA -l <nearbyregion> gs://<exportbucket>
{% endhighlight %}


-  Export your Cloud SQL data to your new bucket:

{% highlight bash %}
gcloud sql instances export yoursqlinstance gs://<exportbucket>
{% endhighlight %}

Optionally, copy the exported data to your local filesystem:

{% highlight bash %}
gsutil -m cp -r gs://<exportbucket>/* .
{% endhighlight %}


