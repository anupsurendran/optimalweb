---
layout: post
title: How we are building Alexa for the mobile industry.
tags:
- alexa
- mobile statistics
- alexa for mobile
- find top apps running on mobile
---

*Where is the Univeral Mobile Statistics Site ?*

It's a mobile world - everybody knows that. It's been like this for almost a decade now. The funniest thing is that we still don't have an [Alexa](http://www.Alexa.com) for the mobile industry. There is no publicly available source currently which I can take a look at to see where my / my company's mobile application ranks amongst other apps of the sametype. There are challenges to get statistics from mobile applications - distribute processing, offline/online support, hybrid applications all lead to 

In my opinion there are three ways to do this.  

1. Google could ask their Google Analytics mobile users to publish their mobile statistics publicly. 

I know that this is a completely different model which will conflict with their existing service model where the end customers will not agree to because its their 'private' metrics. 

Even if Google goes down with this model, there is a challenge of proving that the metrics is correct. What I mean by that is that the Analytics code ( UA-*** ) could have been used in one of an existing mobile application which was already popular and therefore prevents an easy verifiable method to prove the identity of the mobile application.

2. Users call an api to publish their user statistics.

Again this proves to be a non-verifiable way of ensuring the statistics is accurate.

3. A 3rd Party runs device level statistics and collects it centrally. 

A mobile phone is a personal device.  Running a process there to collect information requires permissions from users and has an intrinsic resistance built up. But if you think through this problem, and if use inferential statistics, you could identify a sample which represents your population you want to get data from. You could incentivize them to get the data you need (ie. sending only app related data back to your servers).   


