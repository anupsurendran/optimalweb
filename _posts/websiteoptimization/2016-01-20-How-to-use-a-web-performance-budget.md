--- 
layout: post
title: How to use a web performance budget
tags: 
- website
- performance budget
---

Before starting on how to use a performance budget, let's try to understand what it is and the  purpose of a budget.

## What is a performance budget ?

Just like a financial budget, a performance budget is a group of limits to certain areas that affect site performance. The idea is that these limits may not be exceeded in the design and development of any web project which your company embarks on. Typically, when you have a solution practice in place, a solution blueprint will take care of the non functional aspects of a solution. Most IT solutions have a front end architecture. The front end enterprise architecture guidelines typically includes the performance budget.

## Why do you need a performance budget ?

The main reason to create a performance budget is to have a tangible starting point for conversation around a web page or website. It shouldn’t act as gospel, but it’s a guideline which your solutions are built upon.

> Speed Index and Milestone Timing describe the high-level user experience. Rule metrics and Quantity help understand how the low-level browser engine works

## Key Metrics for a Performance Budget

### Speed Index
This is a full experience score. It tracks how the web page progressed from start to finish. The lower the score, the better.

Most of the measurement is based on how much of the above-the-fold content is visually complete over time. This has a direct impact to user experience. This was originally developed for [webpagetest](http://www.webpagetest.com/ "Web Performance Testing").

### Milestone Timings
These are typically easy to explain (unlike the Speed Index). Good examples of these are : Time to First Byte (TTFB), domContentLoaded, Time to render etc.

The Milestone Timings (unlike the Speed Index) will not give a full picture of the user experience. For example, a page might load under 3 seconds,  but might not display anything until the 2.8 second mark. The fact that the page loaded fast doesnot improve the user experience, because it still took 2.8 seconds for the user to see something in the browser.


