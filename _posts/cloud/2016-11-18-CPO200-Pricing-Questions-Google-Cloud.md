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

#### 7. How do you calculate uptime of a Compute Engine Instance ?

Instance uptime is measured as the number of minutes between when you start an instance and when you stop an instance, the latter being when the instance state is TERMINATED. In some cases, your instance can suffer from a failure and be marked as TERMINATED by the system; in these cases, you will not be charged for usage after the instance reaches the TERMINATED state. If an instance is idle, but still has a state of RUNNING, it will be charged for instance uptime. The easiest way to determine the status of an instance is to use gcloud compute with the gcloud compute instances list command.


#### 8. What are Google Network Pricing considerations ?

A Network Ingress is No charge

Egress to the same zone is No charge

Egress to a different Google Cloud Platform service within the same region is No charge

Egress to Google products (such as YouTube, Maps, Drive) is No charge

Egress* between zones in the same region (per GB) is $0.01

Egress between regions within the US (per GB) is $0.01

Inter-continental Egress is charged At Internet egress rates

#### 9. Are there Load Balancing or Protocol Forwarding rules ?

Up to 5 forwarding rules you create are charged at $0.025/hour. For example, if you create one forwarding rule, you will be charged $0.025/hour. If you have 3 forwarding rules, you will still be charged $0.025/hour. However, if you have 10 rules, you will be charged:

5 forwarding rules = $0.025/hour
Each additional forwarding rule = $0.01/hour

#### 10. Does google cloud offer VPN , if so how much does it cost ?

Yes Google Cloud offers a VPN tunnel. It costs a tunnel (per hour) $0.050

#### 11. Are Static IP address assigned but unused charged by Google Cloud ?

Yes, assigned Static but unused [IP addresses](../Google-Cloud-IP-Addresses/) are charged at $0.010 and Static IP address (assigned and in use) have no charge. Also ephemeral IP address (attached to instance or forwarding rule) has No charge
