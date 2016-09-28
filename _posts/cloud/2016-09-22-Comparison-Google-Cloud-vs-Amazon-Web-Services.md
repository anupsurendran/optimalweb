---
layout: post
title: Mapping of AWS and Google Cloud Terminologies
tags:
- AWS
- Google Cloud
- Cloud
- Terminology
- Comparison
---


This is a full list of services from Google and Amazon side by side.


||Concept||Service||AWS Term ||Google Cloud Term |||  
||:----------------||:-----------------||:-----------------||:----------------------------------||
||Data Center Cluster ||Grouping of Data Centers||Region||Region   ||  
||Abstracted Data Center ||Data Center||Availability Zone||Zone   ||  
||Edge Caching ||Content Caching||CloudFront||Points of Presence (Multiple Services)   ||  
||Computing  || IaaS || Amazon Elastic Compute Cloud|| Google Compute Engine||
||Computing  || PaaS || AWS Elastic Beanstalk || Google App Engine||
||Computing  || Containers|| Amazon Elastic Compute Cloud Container Service || Google Container Engine||
||Network||Load Balancer||Elastic Load Balancer||Google Cloud Load Balancing||
||Network||Peering||Direct Connect||Google Cloud Interconnect||
||Network||DNS||Amazon Route 53||Google Cloud DNS||
||Storage	||Object Storage	||Amazon Simple Storage Service	||Google Cloud Storage||
||Storage||Block Storage	||Amazon Elastic Block Store	||Google Compute Engine Persistent Disks||
||Storage||Cold Storage	||Amazon Glacier	||Google Cloud Storage Nearline||
||Storage||File Storage	||Amazon Elastic File System	||ZFS / Avere||
||Database||RDBMS||	Amazon Relational Database Service||Google Cloud SQL
||Database||NoSQL: Key-value||Amazon DynamoDB	||Google Cloud Bigtable
||Database||NoSQL: Indexed||Amazon SimpleDB||Google Cloud Datastore
||Big Data & Analytics	||Batch Data Processing	||Amazon Elastic Map Reduce	||Google Cloud Dataproc, Google Cloud Dataflow||
||Big Data & Analytics||Stream Data Processing	||Amazon Kinesis||Google Cloud Dataflow||
||Big Data & Analytics||Stream Data Ingest	||Amazon Kinesis||Google Cloud Pub/Sub||
||Big Data & Analytics||Analytics	||Amazon Redshift	||Google BigQuery||
||Application Services	||Messaging	||Amazon Simple Notification Service	||Google Cloud Pub/Sub||
||Management Services||	Monitoring	||Amazon CloudWatch	||Stackdriver Monitoring||
||Management Services||Deployment	||AWS CloudFormation	||Google Cloud Deployment Manager||




