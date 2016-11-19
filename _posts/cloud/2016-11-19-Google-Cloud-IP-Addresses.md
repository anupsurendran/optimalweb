---
layout: post
title: IP Address Questions related to Google Cloud CPO200
tags:
- Google Cloud
- CPO200
- IP Address 
- Exam Preparation
- FAQ
---


#### 1. What type of IP Addresses can be used with HTTP(S) ?

Global IP addresses can only be used with HTTP(s) and SSL load balancing. Global IP addresses cannot be applied to an instance.

#### 2. What type of External IP Addresses does Google Cloud Support ?

Compute Engine supports two types of external IP addresses:

##### Static external IP addresses

Static external IP addresses are assigned to a project long term until they are explicitly released, and remain attached to an instance, even when the instance is stopped, until they are explicitly detached.

##### Ephemeral external IP addresses

Ephemeral external IP addresses are assigned to an instance only until it is restarted or terminated. If an instance is terminated or stopped, any ephemeral external IP addresses assigned to the instance are released back into the general Compute Engine pool and become available for use by other projects. When a stopped instance is started again, a new ephemeral external IP address is assigned to the instance.

#### 3. How do you assign an External IP Address to an instance ?


To assign a static external IP address, use the --address flag during instance creation and provide the static external IP address:

{% highlight bash %}

gcloud compute instances create [INSTANCE_NAME] --address [IP_ADDRESS]

{% endhighlight %}

#### 4. How to change the external IP Address of an instance ?

An instance can have only one external IP address. If the instance already has an external IP address, you can remove that address by deleting the old access configuration. Then you can add a new access configuration with the new external IP address.

{% highlight bash %}

gcloud compute instances describe [INSTANCE_NAME]

{% endhighlight %}

If there is an existing access config, the access config appears in the following format:

{% highlight bash %}

networkInterfaces:
- accessConfigs:
  - kind: compute#accessConfig
    name: external-nat
    natIP: 130.211.181.55
    type: ONE_TO_ONE_NAT

{% endhighlight %}

Before you add a new access config, you must delete the existing access configuration using the instances delete-access-config sub-command:

{% highlight bash %}

gcloud compute instances delete-access-config [INSTANCE_NAME] \
    --access-config-name [ACCESS_CONFIG_NAME]

{% endhighlight %}

After this you can add a new external IP Address

{% highlight bash %}

gcloud compute instances add-access-config [INSTANCE_NAME] \
    --access-config-name [ACCESS_CONFIG_NAME] --address [IP_ADDRESS]

{% endhighlight %}

#### 5. How do you delete an external IP Address ?

{% highlight bash %}
gcloud compute addresses delete [ADDRESS_NAME]
{% endhighlight %}
