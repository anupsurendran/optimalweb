--- 
layout: post
title: Tips to help with google font load times
tags: 
- google fonts
- performance
---

[Web font combinations](http://techdissected.com/web-and-computing/design/top-5-google-font-combinations/ "Web font optimizations") help making websites better to read and the trick is to minimize the number of fonts to help with readability and performance.

### 1. Describe the TEXT
As part of the design process, you might know in advance which particular web font you might use. This often occurs when you're using afont as part of a logo or heading in your landing page or key blog post. The good news is that Google Fonts allows you to specify the TEXT by passing that as an argument that in the request URL for that font.

For example :

http://fonts.googleapis.com/css?family=Tangerine&text=WONDERFUL

By specifying the exact text you require, Google Fonts will provide you with a font file that could potentially be 90% smaller thatn the original full font file. 

### 2. Selecting a SUBSET
You typically do not need the entire unicode character set of a font file and most importantly you only need the right language subset.
Just like the previous example, you simply need to use the subset=value in your font request URL.

http://fonts.googleapis.com/css?family=Tangerine&subset=latin&text=WONDERFUL

### 3. Request MULTIPLE FONTS
Instead of making a separate request for each font file, rather consider chaining the request together. To request multiple font families, separate the names with a pipe character (|).

http://fonts.googleapis.com/css?family=Tangerine|Roboto+Condensed

As you will see below, if you request this url you will see two font-families which are returned with the woff2 format.


{% highlight css %}
@font-face {
  font-family: 'Roboto Condensed';
  font-style: normal;
  font-weight: 400;
  src: local('Roboto Condensed'), local('RobotoCondensed-Regular'), url(http://fonts.gstatic.com/l/font?kit=Zd2E9abXLFGSr9G3YK2MsCINO4zn7r0lJQg85Qda7tf3rGVtsTkPsbDajuO5ueQw&skey=9986ecffddb755ab) format('woff2');
}
@font-face {
  font-family: 'Tangerine';
  font-style: normal;
  font-weight: 400;
  src: local('Tangerine'), url(http://fonts.gstatic.com/l/font?kit=v56dPl2Fzoxg16-bomU6ahif_Qw83hClh7SwGJ4318s&skey=7b78e1b6f929768b) format('woff2');
}

{% endhighlight %}


