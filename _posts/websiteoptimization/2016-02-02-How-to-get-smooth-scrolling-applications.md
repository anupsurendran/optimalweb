--- 
layout: post
title: How to create a smooth scrolling experience for your web application
tags: 
- website
- performance
- smooth scrolling
---

### Smooth Scrolling affects User Experience

The browser needs to draw your website on the screen when a user starts scrolling. This affects the user's perception about how fast the website loads. A jerky scroll gives a clunky experience which we need to minimize. 

### What happens when you scroll ?

Everything the browser does starts with the DOM Tree. The DOM tree contains all the elements of the page. The browser looks at the DOM with the styles and it gorups together elements and take a picture of them. These groupings are called layers. Each layer needs to be painted and rasterized. All this is finally composited together to the image that you then finally see jigsaw puzzled together on the screen. The good news is that the layers help the browser focus in on painting specific texture when something in that layer gets changed. 

### Take advantage of the GPU for animation
If you have animations, Canvas benefits from the immediate mode. It allows drawing commands to be sent directly to the GPU. There is a great article from flipboard around mobile web [performance optimization with the Canvas tag]("http://engineering.flipboard.com/2015/02/mobile-web/" mobile web 60fps rendering)


### Avoid Expensive Selectors and Styles
The [descendant selector is very expensive](https://developer.mozilla.org/en-US/docs/Web/CSS/Descendant_selectors), as there needs to be a check for a match with every descendant element. On a page which is decently complex, this can result in triggering a lot of descendant selector searches. The key thing to understand here is that the relationship is not really a parent and child relationship for these CSS elements. 

Universal selectors like *, [disabled], [type=“text”], etc. are very expensive for the browser to match, as every element in the DOM must be checked.

CSS properties which should ideally be used sparingly :

{% highlight css %}
border-radius
box-shadow
transform
filter
:nth-child
position: fixed;

{% endhighlight %}

### Debouncing events related to Scroll

It is important to decouple Scroll events and other events on your site. Whether this is animation, or other business functions. There is a great article on how to [debounce scroll events](http://www.html5rocks.com/en/tutorials/speed/animations/) from Paul Lewis.

Typically, as you see in the article, the solution is that you store the last scroll valiue in a variable whenever you receive a scroll event. You then read this value when you make updates in the requestAnimationFrame method.


The key things to make sure are to keep the Paint times below the 16ms threshold and to limit repaints and reflows. This is specifically important when you do animations.
