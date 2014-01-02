--- 
layout: post
title: How to add a SVG image in D3
tags: 
- tips
- d3 
- add svg
---

First of all - Happy 2014 to all of you!.

In D3, you have the option of importing XML. SVG is and XML based vector image format.
{% highlight javascript linenos=table %}
d3.xml("/assets/infographics/" 
       + svgSource, 
"image/svg+xml", 
function(xml) {			
 var importedNode = document.importNode(xml.documentElement, true);
	
	$('#svg-image')
        .find('g#' + id).append($(xml.documentElement).clone());
			container.attr("x" , "200px");
			container.attr("y", "200px");
 });
{% endhighlight %}

If you are interested in generating dynamic Infographics automatically - try Secondprism's 
[Infographic generator here](http://app.secondprism.com/assets/product/infographic_for_dashboard.html).
