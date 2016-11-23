---
layout: post
title: Google Cloud Storage Options |  CPO200
tags:
- Google Cloud
- CPO200
- Storage 
- Exam Preparation
- FAQ
---


#### What are the different types of Storage available on google cloud ? 

- Persistent disks	
- Local SSDs	
- Cloud Storage buckets	
- RAM disks

#### Which of the following Cloud Storage classes are supported for Container Registry?

○ Standard

○ Durable Reduced Availability

○ Nearline

Answer :

All of the listed classes are supported.

#### List the basic steps for first creating a Cloud Storage bucket and then configuring it for use with Container Registry and pushing a container image to it.

Steps :

1 Type the following command to create your bucket using the Cloud SDK.

{% highlight bash %}
gsutil mb -c <bucketclass> -l <bucketlocation> gs://<bucketname>
{% endhighlight %}

2 Type the following command to tag your container image with the bucket name.

{% highlight bash %}

docker tag user/<imagename> b.gcr.io/<bucketname>

{% endhighlight %}

Note: You must specify b.gcr.io as the hostname in this case.

3 Type the following Cloud SDK command to push the image to your bucket.

{% highlight bash %}

gcloud docker push b.gcr.io/<bucketname>/<imagename>

{% endhighlight %}
