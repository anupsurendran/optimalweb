---
layout: post
title: How to Change Google Cloud Account |  CPO200
tags:
- Google Cloud
- CPO200
- FAQ
---


#### The syntax to switch the active account takes the following format.

{% highlight bash %}
gcloud config set account <accountemailaddress>
{% endhighlight %}

#### To switch to using a Compute Engine service account you should type:

{% highlight bash %}

gcloud config set account <SOMEID>-compute@developer.gserviceaccount.com

{% endhighlight %}

#### To switch to using a Gmail based account you should type:

{% highlight bash %}
gcloud config set account <name>@gmail.com 
{% endhighlight %}
