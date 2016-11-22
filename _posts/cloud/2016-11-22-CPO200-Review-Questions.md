---
layout: post
title: Google CPO200 Exam Review Questions |  Google CPO200 Exam Preparation
tags:
- Google Cloud
- CPO200
- Review Questions 
- Exam Preparation
---

#### 1. Which of the following are global resources? (choose 2 of the available options)

❏ Snapshots

❏ Persistent disks

❏ Instances

❏ External IP addresses

❏ Firewall rules


Answer : 

✓ Snapshots 

✓ Firewall Rules


#### 2. You check the status of an instance and find it is TERMINATED. Which of the following are likely causes?(select 2 of the available options)

❏ The instance is being migrating due to host maintenance

❏ You did not override the default availability policy for on host maintenance

❏ The instance is preemptible

❏ The instance is performing a periodic system update

❏ A project Owner has issued a shutdown command from within the operating system

Answer : 

✓ The instance is preemptible

✓ A project Owner has issued a shutdown command from within the operating system    

#### 3. True or False. In order to connect to an instance using SSH, a user must be assigned Owner permissions to a project or the IAM role compute.instanceAdmin.

False. In order to connect to an instance using SSH, a user must be assigned Owner permissions to a project or the IAM role compute.instanceAdmin. You can also manually provide a user access to an instance using an SSH key-pair for a linux account without requiring project access. Owner and Editor permissions allow SSH connections.  

#### 4. True or False. Instances in separate networks in the same project must use their external IP addresses to communicate. 

You have created a firewall rule to allow HTTP traffic to particular instances in your default network running
HTTP servers, but the web pages are unreachable. Suggest possible troubleshooting steps.

Answer:

True. Instances attached to separate networks in the same project must use their external IP addresses to communicate.

Possible troubleshooting steps include:

● Verify the instances are tagged correctly and that the firewall rule applies to the correct tag(s)

● Check for operating system-level components that may be blocking traffic on the virtual machine

● Verify the network routes are configured to allow traffic

● Check that the instances have been assigned an external IP address

#### 5. Instance tags can be used to define which of the following networking components? (select 2 of the available options) 

❏ Which network an instance belongs to

❏ Network address translation of external to internal IP addresses

❏ Which firewall rules apply to an instance

❏ Which routes apply to an instance

❏ Mark an instance able to send traffic to the internet

Answer :

✓ Which firewall rules apply to an instance

✓ Which routes apply to an instance

#### 6. Can you prevent the destruction of an attached persistent disk when the instance is deleted?

❏ Yes, use the --keep-disks option with the gcloud compute instances delete command

❏ Yes, deselect the option “Delete boot disk when instance is deleted” when creating an instance

❏ No, attached persistent disks are always associated with the lifetime of the instance

Answer:

✓ Yes, use the --keep-disks option with the gcloud compute instances delete command

✓ Yes, deselect the option “Delete boot disk when instance is deleted” when creating an instance

#### 7. Why would you create an image from an existing disk? (select 2 of the available options)

❏ To preserve the installation of specific software

❏ Because instances with attached disks have readonly storage

❏ Because persistent disks only retain information when they are attached to an instance

❏ To serve as the basis for other instances

Answer :

✓ To preserve the installation of specific software

✓ To serve as the basis for other instances

#### 8. True or False. Once scopes are customized during instance creation, they cannot be modified even if the instance is stopped.

Answer:

True. Currently, the only way to modify instance scopes is to recreate the instance.


#### 9. True or False. User-defined service accounts can only be used with IAM roles.

Answer :

True. Default and user-defined service accounts can be used with IAM roles and project roles. 

#### 10. You need to migrate data from a persistent disk to another region. Reorder the following tasks:

1. Attach disk

2. Create disk

3. Create snapshot

4. Create instance

5. Unmount file system(s)

Answer :

1. Unmount file system(s)

2. Create snapshot

3. Create disk

4. Create instance

5. Attach disk

#### 11. Which of the following are use cases for snapshots? (select 2 of the available options)

❏ Use snapshots to migrate instance configuration including tags

❏ Use snapshots to migrate data to an instance in the same region

❏ Use snapshots to migrate data to a local solid state disk

❏ Use snapshots to migrate data from SSD to a standard persistent disk

Answer :

✓ Use snapshots to migrate data to an instance in the same region

✓ Use snapshots to migrate data from SSD to a standard persistent disk

#### 12. You are tasked with setting up storage for log files generated by a web site. They may be read by only one group of people and the retention policy mandates deletion after one month. Which of the following will you use to achieve these objectives? (select 2 of the available options)

❏ Locate storage in a specific region (EU, US, or Asia)

❏ The web option of gsutil

❏ Customized ACL settings

❏ The cron option of gsutil

❏ The lifecycle option of gsutil

Answer:

✓ Customized ACL settings

✓ The lifecycle option of gsutil

#### 13. Is it possible for two different Google Cloud Platform projects to each create a Cloud Storage bucketwith the identifier gs://local-logs?

❏ Yes, identifiers must be unique within a project

❏ No, identifiers must be globally unique

❏ Yes, as long as the buckets are in different geographical
regions

Answer:

✓ No, identifiers must be globally unique

#### 14.Complete the answers for comparing managed and unmanaged instance groups.

__Unmanaged instance groups__

Zone-based - Yes/No 

Mix of instance types - Yes/No

Resize method - Yes/No

Use existing instances - Yes/No

__Managed instance groups__

Zone-based - Yes/No 

Mix of instance types - Yes/No

Resize method - Describe

Use existing instances - Yes/No

Answer:

__Unmanaged instance groups__

Zone-based - Yes

Mix of instance types - Yes

Resize method - By manually adding instances

Use existing instances - Yes

__Managed instance groups__

Zone-based - Yes

Mix of instance types - No

Resize method - Instruct instance group manager to resize from template

Use existing instances - No

#### 15. Cloud SQL Questions

[CPO200 - Cloud SQL Questions](/Cloud-SQL-Questions-CPO200)

#### 16. Which of the following are valid methods of querying instance metadata from your laptop. (select 2 of the available options)

❏ gcloud compute instances metadata <instance>

❏ gcloud compute instances describe <instance>

❏ Issue a curl command to the metadata service

❏ gcloud compute metadata list

❏ Inspect instance metadata in the Cloud Platform Console

Answers:

✓ gcloud compute instances describe <instance>

✓ Inspect instance metadata in the Cloud Platform Console

#### 17. You login to an instance and find the startup script does not appear to have run. List possible troubleshooting steps to isolate the cause.

Possible troubleshooting steps include:

● Check the startup script log at /var/log/startupscript.log

● Verify that the URL for the script is correctly configured in metadata

● Manually try to read the startup script from Cloud Storage using

gsutil:

● gsutil cat gs://<bucket></path/to/script.sh>

● Check that the instance has the correct authorization scopes to read the script from the source Cloud Storage bucket, as well as the related ACLs

● Check if there are any syntax errors while running the script manually after you login to the instance

#### 18. Shutdown scripts run in which of the following circumstances? (select 3 of the available options)

❏ Running sudo shutdown from the guest operating system

❏ An instance is undergoing live migration

❏ Running the instances().stop method

❏ Running the instances().delete method

❏ Running the instances().reset method

Answer :

✓ Running sudo shutdown from the guest operating system

✓ Running the instances().stop method

✓ Running the instances().delete method

#### 19. True or False. The use of instance templates is optional with an autoscaler.

False. The use of instance templates is optional with an autoscaler. An autoscaler uses an instance group manager to add and remove instances in an instance group. An instance group manager creates instances based on an instance template.

#### 20. What is a potential role of shutdown scripts when using an autoscaler?

A shutdown script can be used to gracefully shut down any applications or upload logs prior to terminating an instance as a result of an autoscailer.

#### 21. Which of the following features are associated with Network Load Balancing? (select 2 of the available options)

❏ Target proxies

❏ Target pools

❏ Forwarding rules

❏ Global forwarding rules

❏ URL maps

Answer :

✓ Target pools

✓ Forwarding rules

#### 21. Network load balancing is a good fit for which of the following scenarios? (select 1 of the available options)

❏ Content-based load balancing

❏ Cross-region load balancing

❏ Load balancing confined to a single region

❏ Load balancing confined to a single zone

❏ None of the above

Answer :

✓ Load balancing confined to a single region

#### 22. Review the following comparison table for Network and HTTP(S) load balancing.

__Network load balancing__

Health checks Optional - Optional

Cross-region - No

Protocols - Multiple protocols 

Packet inspection Supported 

__HTTP(s) load balancing__

Health checks - Required

Cross-region - Yes

Protocols - HTTP(S) only

Packet inspection - Not supported
