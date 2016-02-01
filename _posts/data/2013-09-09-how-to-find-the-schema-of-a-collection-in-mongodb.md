--- 
layout: post
title: How to find the schema of a collection in MongoDB
tags: 
- tips
- mongodb
- mongodb command line
- data
---

The last two commands are equivalent to the SQL command below
{% highlight sql %}
Describe Table
{% endhighlight %}

Open a mongo shell and run the following commands :

{% highlight bash %}
MongoDB shell version: 2.4.5
> show dbs
local 0.078125GB
todo 0.453125GB
> use todo
switched to db todo
> show collections
system.indexes
tasks
> var schematodo = db.tasks.findOne();
> for (var key in schematodo) { print (key) ; }
_id
label
content
{% endhighlight %}

Also, on a side note, It is interesting to also note that we at [optimal.io](http://www.optimal.io/ "web performance benchmark") did a [web performance test for NOSQL vendors](http://optimal.io/benchmarks/saas/nosql-web-peformance-report-Q1-2016.html "web performance for NOSQL vendors") and MongoDB's site came #7. 
