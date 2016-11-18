---
layout: post
title: Pricing Questions related to Google Cloud CPO200
tags:
- Google Cloud
- CPO200
- Pricing 
- Exam Preparation
- FAQ
---

### Key Google Cloud Pricing questions


#### 1. Does Google charge in local currency or USD ?

Local Currency.

When charging in local currency, Google will convert the prices listed into applicable local currency pursuantto the conversion rates published by leading financial institutions.

#### 2. What are the two categories of Compute Engine Google cloud offers ?

Google cloud offers  two categories of machine types: predefined machine types and custom machine types.  

#### 3. What is the minimum usage time for charging for a machine type ?

All machine types are charged a minimum of 10 minutes. For example, if you run your virtual machine for 2 minutes, you will be billed for 10 minutes of usage.


#### 4. Is there an incremental second based or minute based billing for machine types ?

Yes, only MINUTE based billing, but it doesnot apply for the first 10 minutes. After 10 minutes, instances are charged in 1 minute increments, rounded up to the nearest minute. An instance that lives for 11.25 minutes will be charged for 12 minutes of usage.

#### 5. Does Google offer any discounts ? If so what is the criteria to get a discount ?

Yes, only if you use your Compute Engine in a sustained manner. You get a sustained discount.

If you run an instance for a significant portion of the billing month, you can qualify for a sustained use discount. When you use an instance for more than 25% of a month, Compute Engine automatically gives you a discount for every incremental minute you use for that instance. The discount increases with usage and you can get up to a 30% net discount for instances that run the entire month. Sustained use discounts are calculated and applied to your bill as your project earns them.  


#### 6. What is an inferred instance, how does it help with discounts ?

An inferred instance combines multiple, non-overlapping instances in the same zone into a single instance for billing. With inferred usage, you are more likely to qualify for sustained use discounts. 

If you look at the picture below - Google has combined the instances to get an inferred instance which will get three inferred instances which will give the longest sustained usage for better discounts.

![Google Cloud Inferred Instance for discounts]({{ site.baseurl }}/assets/img/google_cloud_inferred-instance.png "Google Cloud Inferred Instance for discounts")


