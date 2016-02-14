--- 
layout: post
title: Exhaustive list of Easy Ways to Speed up Wordpress
tags: 
- wordpress speed
- fast loading
- performance
- plugins
---

### 1. Remove unnecessary Plugins

At the time of writing this article there are 42,837 plugins on the [Wordpress Plugin site](https://wordpress.org/plugins/). This gives an average of approximately 3300 plugins written every year for this popular blogging and content management system.

> 3300 Wordpress Plugins written on average every year !

This cannot happen unless there is a huge team of Wordpress Plugin creators who work on this on a consistent basis. What we know is that the quality of these plugins vary based on the quality of the plugin authors. The functional quality might be ok but the performance of these plugins might not be great. 

As part of any speed optimization excercise it is important to start with a cleanup excercise of looking at your Plugin folder and finding out which Plugins are not used. The good news is that most WordPress Plugins have an option to completely uninstall themselves, though not all. 

![alt Wordpress plugin deactivation and speed optimization]({{ site.baseurl }}/assets/img/wordpress-plugin-speed.png "Clean up Wordpress Plugins for Speed")



If you wish to completely get rid of the  WordPress Plugin then you have to do the following :

* Check the WordPress Plugin instructions in the detail *ReadMe* file  on how to properly uninstall the Plugin.
* Sometimes the WordPress Plugin requires some  addition of code to your WordPress Theme. You will have to  manually edit the Theme files to remove it.
* You will have to Deactivate the Plugin and remove it manually through your FTP program. This means you will have to Login to the blog or website which runs Wordpress via your FTP Program. Go to the Plugin directory and find where the Plugin is installed.
Delete the WordPress Plugin folder and  files from your hosting server provider.

To summarize, the sequence of the Wordpress Plugin cleanup excercise is to
Deactivate, Delete and Permanently delete Plugins  using FTP

### 2. Find a good Host for your Wordpress Site or Blog

> [Wordpress Host Performance test](http://optimal.io/benchmarks/paas/wordpress-hosting-web-performance-report-Q1-2016.html "Wordpress Hosting speed benchmarks") results from Q1 2016

There are some [recent wordpress performance tests](http://www.wpsitecare.com/performance-of-7-top-wordpress-hosting-companies-compared/ "Wordpress hosting performance testing comparison") which we did not have to duplicate. The performance winners for under 10 dollars therefore are :

* [SiteGround](http://www.Siteground.com) @ $3.95/month 
* [Inmotion Hosting](http://www.inmotionhosting.com) @ $4.89/month
* [Site5](http://www.site5.com) @ $8.95/month

For enterprise type features along with performance, Like Staging – Great for testing out new themes and plugins without affecting your existing site, Transferable Installs, LargeFS and their own CDN (they have partnered with NetDNA), [WPEngine](/wordpress-speedup "faster wordpress host") comes out in front.
 
> [WPEngine is Enterprise grade with High Performance](/wordpress-speedup "CDN enabled Wordpress")

### 3. Use the best Wordpress Cache Plugin to speed up your site 

#### What is a Cache ?

A cache is a place to store data to help with quick retreival. Most frequently used active data is often cached in order to reduce load times. All modern browsers use caching to speed up content retreival. When you return to a frequently accessed website, there is a very high probability  your browser will have a good portion of the site’s files stored within its cache. This means that the browser needs to receive less ‘fresh’ information from the site, resulting in a faster load time. The way Wordpress caching plugins work is by saving the dynamically generated HTML files and serving them from the Wordpress cache instead of regnerating the HTML files which avoids running PHP scripts or getting the data from the Wordpress Database.

#### What is the key functionality you should look in a Wordpress Cache Plugin ?

The key metric which a Wordpress Cache should be measured against is Speed of your site's page rendering. Some Wordpress Plugins come with extra performance features such as integration with content delivery networks, GZIP compression (file compression feature), and minification (removing all unnecessary characters from the front end code so that only absolutely necessary data is send to the browser). These all enable your site or blog to run even faster.

#### The top 3 Wordpress Cache plugins are :

####[WP Super Cache](https://wordpress.org/plugins/wp-super-cache/ "Top Wordpress Cache Plugin for helping with Increasing Wordpress Speed")
[WP Super Cache](https://wordpress.org/plugins/wp-super-cache/ "Wodpress Cache to increase speed of Wordpress Site") can deliver static pages with mod_rewrite (which is faster than the usual PHP generated HTML caching) or PHP, depending on your preference, meaning that each visitor doesn’t need to load all of the WordPress PHP files – they simply receive a static HTML page. However, there is the ‘legacy caching mode’, meaning that if you’re logged in, you won’t experience the supercached HTML files. WP Super Cache also enables you to change the order in which plugins load, so if you need certain plugins to load with lighting speed, you’re in luck. 

####[W3 Total Cache](https://wordpress.org/plugins/w3-total-cache/ "Secondmost popular Wordpress Cache for website performance")
[W3 Total Cache](https://wordpress.org/plugins/w3-total-cache/ "improve speed of wordpress site using w3 total cache") claims that it can help sites powered by Wordpress to go 10x faster. It helps with optimized progressive render so that pages start rendering quickly.

To improve loading time, W3 Total Cache utilizes file minification and GZIP compression. Like WP Super Cache, W3 Total Cache also supports Content Delivery Networks and allows you to export your settings for future use.

####[WP Rocket](http://wp-rocket.me/ "Paid plugin for improving wordpress peformance") 
[WP Rocket](http://wp-rocket.me/ "Wordpress performance cache paid plugin") is a great Cache Plugin if you are ready to pay for it. It has [in built google font optimization](http://blog.optimal.io/Tips-to-help-with-google-font-loading-speed/ "Increase speed of google fonts"), DNS Prefetching, supports better deferring of Javascript loading and is more eCommerce friendly. 


 
### 4. Optimize your database

Most of Wordpress's data is stored in 11 MySQL tables. 
* wp_commentmeta – Stores meta information about comments
* wp_comments – Stores your comments
* wp_links – Stores blogroll links (blogroll feature is deprecated, but can be added using Link Manager)
* wp_options – Stores the options defined in the admin settings area
* wp_postmeta – Stores post meta information
* wp_posts – Stores data for posts, pages, and other custom post types
* wp_terms – Stores post tags and categories for posts and links
* wp_term_relationships – Stores the association between posts and categories and tags and the association between links and link categories
* wp_term_taxonomy – Stores a description about the taxonomy (category, link, or tag) used in the wp_terms table
* wp_usermeta – Stores meta information about users
* wp_users – Stores your users

The Wordpress site [Wordpress Database Description]("http://codex.wordpress.org/Database_Description") available for the diagramatic representation of these tables. 

phpMyAdmin is the most common way to manage a WordPress database. If you do not have access to phpMyAdmin, do not be too concerned about this as most database management tools have a similar interface and work in the same way.

As shown in the screenshot below, with phpMyAdmin, it allows you to optimize tables from the main drop down menu. All you need to do to optimize your database is click on the “Check All” box, select “Optimize table” from the dropdown menu, and then click on the “Go” button.

![alt Wordpress MySQL phpMyAdmin speed optimization]({{ site.baseurl }}/assets/img/increase-speed-wordpress-mysql.png "Wordpress MySQL Optimization for Speed")

You can optimize tables that are affected by overhead by using the SQL command OPTIMIZE TABLE. For example, you could optimize the wp_posts table by executing this SQL query in the MySQL command line or the phpMyAdmin sql command window :

{% highlight sql %}
OPTIMIZE TABLE 'wp_posts'
{% endhighlight %}

Based on point #1 in this article about cleaning up Plugins, even if you have decided to stop using a plugin, there is a chance that the Plugin data still remains in the database. A small number of WordPress plugins include an option on their settings page to remove all data, though the majority of plugins do not have this option. Over time, this can add bloat to the Wordpress Database.
WordPress themes also store settings in the database and will remain in your database when you switch themes.

A useful plugin to help you with this is [WPDBSpringClean](https://wordpress.org/plugins/wpdbspringclean/ "Cleaning Wordpress Plugin Data for Speed"). This plugin will identify unoptimized tables and will allow you to optimize them by deleting the allocated unused space within a particular table. The plugin also optionally allows you to specify search criteria such as the minimum amount of overhead per table and minimum unused space for a table.


### 5. Limit the number of Revisions

WordPress places no limitation on the number of revisions that are saved. This was a feature which was introduced because of popular demand in Wordpress veresion 2.6. However, If you are working on a long article, you typicall make intermediate saves and this could result in hundreds of revisions being saved. Every revision save could potentially correspond to  a couple or a dozen rows in your database.

There is no point having unlimited number of revisions for each blog post. Think about it - How often have you gone to the first version of your blog post and retreived it. The good new is that WordPress allows you to reduce the number of revisions that are stored which means that you can define n - X, where n is the last revision and X the revisions before.



>The general rule of thumb is to not go more than 5 revisions for any blog post. 
 You can make this change in the wp-config.php file

{% highlight php %}
define( 'WP_POST_REVISIONS', 5 );
{% endhighlight %}

### 6. Just show enough information on your Wordpress Home Page

Reducing content is an art. Try to show just the right sized excerpt to maximize the marketing pull instead of full posts. Reduce the number of posts on the page by either limiting the count of posts or by showing the main category your blog is popular for.
If there are widgets which are not providing any value then remove them.  Navigating through your site should be absolutely effortless for the end user. They should be presented with just enough navigational elements that makes it easy to find what they are looking for. The best pattern to navigate to olders posts is by by showing the **Most Popular** post section.

> Be extremely careful and choosy about advertisements you put on your home page. 
The most efficient way of promoting a product or services is to link directly to the page using an image that has been optimized for the web. You can take this one step further and link using text links instead.

### 7. Don't let others suck away your good Assets (ie. prevent hotlinking)

Hotlinking is a way by which other sites (including other non-wordpress sites) link to your great assets (ie. images, hosted videos etc) and render them on their sites. 


> This is bad primarily because it increases your bandwidth consumption and also because the leech site probably gets credits for your great content.

The smartest way to prevent image hotlinking is by editing the .htaccess file. The modification of .htacccess file allows you to:

- Block individual websites or allow other wordpress sites which you own
- Allow or deny blank referrers
- Display custom images detecting image hotlinking
- Protect files and directories

##### EDITING The .htaccess file

Don’t attempt to edit the file this time. Just paste the following code if you don't have any RewriteEngine rules :

{% highlight unix %}
RewriteEngine on
RewriteCond %{HTTP_REFERER} !^$
RewriteCond %{HTTP_REFERER} !^http(s)?://(www\.)?your-site.com [NC]
RewriteCond %{HTTP_REFERER} !^http(s)?://(www\.)?your-other-wordpress-domain.com [NC]
RewriteRule \.(jpg|jpeg|png|gif)$ http://i.imgur.com/g7ptdBB.png [NC,R,L]
{% endhighlight %}

Explanation:

Line 1 turns on the rewrite engine used for enabling the redirection process.

Line 2 allows blank referrers to view the image. Some folks who use firewall usually surf without any referrers. Now, you don’t want to block your images from them. Hence, you allow blank referrers.

Line 3 allows ‘your-site.com’ to view the images. Replace ‘your-site.com’ with your actual domain name – don’t use the www.Similarly if you want to allow other sites to use your images, you can replace ‘your-other-wordpress-domain.com’ with the proper domain name.

Line 5 replaces all unauthorized images to be replaced by the this image. You can also create a custom image and upload it to any directory other than the root directory. If you place it in the root directory, your server might fall in an infinite loop. Thus, its best to place the image in a folder say “images” and use that link. In which case the URL would be: “http://my-site.com/images/preventhotlink.png”

### 8. Image and other asset optimization on Wordpress
>The biggest problem we see with many blogs is that they upload massive non-optimized emails for their blogs. 

If you do a proper job, you could potentially increase your single post rendering time by a huge margin. We have seen long time Wordpress bloggers focused on optimizing their most popular blog posts speed by just doing image optimization. High resolution images that are unnecessarily large in file size can drastically slow down page speed. Why upload image files which are HUGE (e.g. > 1MB) and slow down your page when it’s possible to reduce image size without losing it’s quality.

The good news is there are a couple of good plugins which you can use to help with image optimizationa and thereby speed of the wordpress site.

- The free version of [WP Smush.it](https://wordpress.org/plugins/wp-smushit/ "Wordpress Image Optimization for speed"), lets you compress images up to 1MB in size, while the pro version smushes images up to 5MB in size. The plugins work by stripping meta data from JPEG files, optimizing JPEG compression, converting certain GIFs to indexed PNGs and stripping the un-used colours from indexed images. In summary, the plugin strips hidden, bulky information from your images, reducing the file size without losing quality.
- [EWWW Image Optimizer](https://wordpress.org/plugins/ewww-image-optimizer/ "Wordpress Image compression to load pages faster") uses lossless optimization techniques, so your image quality will be exactly the same before and after the optimization. The only thing that will change is your file size. The one small exception to this is GIF animations. While the optimization is technically lossless, you will not be able to properly edit the animation again without performing an --unoptimize operation with gifsicle. The gif2png and jpg2png conversions are also lossless but the png2jpg process is not lossless. 
- [CW Image Optimizer](https://wordpress.org/plugins/cw-image-optimizer/ "Linux littleutils for wordpress image compression") is another plugin that automatically and losslessly optimizes your images as you upload them to your site, and can optimize images previously uploaded. This plugin is based on WP Smush.it, though unlike the WPMU DEV plugin which uses the Yahoo! Inc. Smush.it service, CW Image Optimizer uses the Linux littleutils image optimization tools. This means your images never leave your server.

Another think to consider is Lazy loading. This [Lazy loading plugin](https://wordpress.org/plugins/bj-lazy-load/ "Loading images faster for wordpress") replaces all your post images, post thumbnails and content iframes with a placeholder and loads the content as it gets close to enter the browser window when the visitor scrolls the page. Also works with text widgets.

### 9. Make sure your Gravatar image is not Bloated and Cached


> Every gravatar image is a new HTTP request.

Even if the same image is loaded, a page with 100 comments would have 100 additional HTTP requests. Unfortunately, Gravatar images do not contain expire headers. [FV Gravatar cache](https://wordpress.org/plugins/fv-gravatar-cache/ "gravatar image speeding up") helps with caching gravatars with WordPress cron job, caching gravatars on comment submission and maintaining a single copy of the default gravatar instead of downloading it again and again for all the email addresses with no gravatar associated.

### 10. Reduce Repeated PHP Script execution

If you examine your theme’s Header.php file in your Presentation > Theme Editor tab in the control panel you will find some lines that look somewhat like the following:

{% highlight php %}
<title><?php bloginfo('name'); ?> <?php bloginfo('description');?></title>
<link rel="shortcut icon" type="image/x-ico" href="&lt?php bloginfo('template_url'); ?>/favicon.jpg" />
<link rel="stylesheet" type="text/css" media="screen" href="<?php bloginfo('stylesheet_url'); ?>"/>

{% endhighlight %}

 We can eliminate those 5 PHP executions and replace them with plain HTML which is atleast 10 times faster.


Now, all we need to do is replace that original PHP code with the already processed code and save the Header.php file. When a blog gets some heavy traffic that adds up pretty quickly. Do this also with other commonly used scripts like the Footer.php .

{% highlight php %}
<title>Optimal.io - your web optimization site</title>
<link rel="shorcut icon" type="image/x-ico" href="http://optimal.io/wp-content/themes/speed-site/favicon.jpg" />
<link rel="stylesheet" type="text/css" media="screen" href="http://optimal.io/wp-content/themes/speed-site/style.css"/>
...
{% endhighlight %}

### 11. Disable pingbacks and trackbacks

> Pingbacks are inefficient

There is often a very small chance of Pingbacks being legitimate and being used in the way they were intended. With that in mind, in nearly all cases, it’s preferable to disable the notifications, and therefore avoid publishing them altogether.

Thankfully, turning off the trackback and pingback notifications in WordPress is very straightforward. However it is worth pointing out that turning off this feature only applies to new posts, rather than it working retroactively. This means it’s best to take this action early on, rather than ignoring the issue while you continue to add content to your site.

To disable notifications for trackbacks and pingbacks on your WordPress site, simply login to the admin dashboard. Then go to Settings > Discussion and uncheck the ‘Allow link notifications from other blogs (pingbacks and trackbacks)’ option.


### 12. Get smarter and faster themes

When we refer to smart - what we refer to is things like social icons using image sprites instead of doing multiple requests. Simplified minified single css and javascript files. All this while maintaining SEO and mobile optimized layouts. There is a [good review](https://85ideas.com/wordpress/fastest-wordpress-themes/) here of some fast performing themes.






