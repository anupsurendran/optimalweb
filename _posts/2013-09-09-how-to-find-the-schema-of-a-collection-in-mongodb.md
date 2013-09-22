--- 
layout: post
title: How to find the schema of a collection in MongoDB
tags: 
- tips
- mongodb
- mongodb command line
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
