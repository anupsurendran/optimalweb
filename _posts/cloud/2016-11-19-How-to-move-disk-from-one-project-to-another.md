---
layout: post
title: How to move Persistent Disk from one project to another on Google compute engine |  CPO200
tags:
- Google Cloud
- CPO200
- IP Address 
- Exam Preparation
- FAQ
---


#### Two steps to move your Persistent Disk across instances 

1) Create your image from your Persistent Disk ( Here is a link to the [google cloud documentation](https://cloud.google.com/compute/docs/images#creating_an_image_from_a_root_persistent_disk) )

{% highlight bash %}
$ gcloud compute images create [example-image] --source-disk [example-disk] --source-disk-zone ZONE --project="old-project-name"
{% endhighlight %}

2) Instantiate the image in the new project. This requires you to have access to both projects.

{% highlight bash %}
$ gcloud compute instances create [example-instance-1] --project=[new-project-name] --image="https://www.googleapis.com/compute/v1/projects/[old-project-name]/global/images/[image-name]" --boot-disk-size [XXXGB] --machine-type=[machine-type] --network="default" --zone=[datacenter-zone] 
{% endhighlight bash %}

You can see the URL of your image in the Images tab under "Equivalent REST" in the console.
In Google Developer Console, select the old project and go to Compute -> Compute Engine -> Images. Click on the new image (i.e. <image-name>), select Equivalent REST and copy the link (something like https://www.googleapis.com/compute/v1/projects/<project-name>/global/images/<image-name>)




