---
layout: post
title: Google Command Cheatsheet |  CPO200
tags:
- Google Cloud
- CPO200
- Command 
- Exam Preparation
- Cheatsheet
---


##### 1. Type the Cloud SDK command to list the available Compute Engine zones and make a note of possible alternatives to your default zone. 

{% highlight bash %}

gcloud compute zones list 

{% endhighlight %}

##### 2. Type the Cloud SDK command to create a bucket, this time using the class Durable Reduced Availability.

{% highlight bash %}
gsutil mb -c DRA -l $BUCKET_LOC gs://<dratestbucket>
{% endhighlight %}

##### 3. Why is the -m option useful in this gsutil context?

The -m option enables the parallel transfer of files to and from Google Cloud Storage. In this case, the bandwidth is high between Compute Engine and Cloud Storage so it's advantageous to enable parallel operations which require a fast network connection.

##### 4. How can you read the contents of one of the newly uploaded objects directly from Cloud Storage. What is the command you would type?

{% highlight bash %}
gsutil cat gs://<dratestbucket>/<objectname.extension>
{% endhighlight %}

##### 5. Type the Cloud SDK command to add a firewall-rule to the default network in the Guestbook project to allow HTTP connections on port 80 from anywhere to instances tagged ‘http’.

{% highlight bash %}
gcloud compute firewall-rules create default-allowhttp --allow tcp:80 --target-tags http
{% endhighlight %}

##### 6. Type the Cloud SDK command to create a Compute Engine instance based on the guestbook-1 image, tagged with ‘http’ and assign it the < externalipaddress > address.

{% highlight bash %}
gcloud compute instances create guestbook --image guestbook-1 --tags http --zone $ZONE --address <externalipaddress>
{% endhighlight %}

##### 7. How can you give a snapshot name to your snapshot ?

{% highlight bash %}
gcloud compute disks snapshot <diskname> --snapshotname <snapshotname> \
--zone $ZONE
{% endhighlight %}

##### 8. How can you authorize and IP address to access the sql instance ?

{% highlight bash %}
gcloud sql instances patch mysqlinstancename --authorizednetworks $IP
{% endhighlight %}

##### 9. What is the command to describe the project-wide configuration data including metadata ?

{% highlight bash %}
gcloud compute projectinfo describe
{% endhighlight %}


