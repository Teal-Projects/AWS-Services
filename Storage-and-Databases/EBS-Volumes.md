h1. Description 


Elastic Bloc Store, provide persisten block storage volumes for use with Amazon EC2 instances in the AWS Cloud. Each Amazon EBS volume is automatically replicated within its Availability Zone to protect you from component failure, offering high availability and durability 


h1. Main Features 

h5. General :
* It's a network drive
* Can be attached to only one instance at a time. (Not like EFS).
* It's lock to an AZ.
* Have a provisioned capacity (in GB and IOPS).
* Only GP2 and IOI can be used as a boot volumes.

h5. Snapshot : 
* Sapshot are incremental - only backup changed blocks.
* Snapshot exist on S3. Stop the instances befor to take the snapshot. 
* To move an EC2 volume from one AZ to an other, take a snapshot of it, create an AMI from the snapshot and then use the AMI to launch the EC2 instance in a new AZ. 
* To move ans EC2 volume from one region to another, take a snapshot of it, create an AMI from the snapshot and then copy the AMI from one region to the other. Then use the copied AMI to lauch the new EC2 instance in the ne region. 

 
h5. Encrypt Root Device Volumes & Snapshots 
* Snapshot of encrypted volumes are encrypted automatically. Like Volume restored from encrypted snapshot. 
* You can share with other AWS account or made public a snapshots, but only if they are unencrypted. 
* You can encrypt root device volumes upon creation of the EC2 instance. 
* The process to encrypt an Root Device volume if not encrypt from the beginning : 
* Create a Snapshot of the unencrypted root device volume. 
* Create a copy of the snapshot and select the encrypt option. 
* Create an AMI from the encrypted snapshot. 
* Use that AMI to launch new encrypted instances. 
 

h5. EBS - GP2 SSD : 
* General Purpose, that balance price and performance for a wide variety of workloads.
* 1 BiB - 16 TiB
* Small gp2 volumes can burst IOPS to 3000
* Max IOPS is 16'000.
* Recommanded  for :
** For most workload.
** System boot volumes
** Virtual desktop.
** Low-latency interactive apps.
** Development and test environments.

h5. EBS - IOI (SSD)
* Provisioned IOPS , for mission-critical low-latency or hihh-throughput workload.
* 4 GiB - 16 TiB.
* IOPS is provisioned (PIOPS)
* The maximum ratio of provisioned IOPS to requested volume (in GiB) size is 50:1
* Recommanded  for :
** Critical business applications that require sustained IOPS performance or more than 16'000 IOPS per volume.
** Large database workload.

h5. EBS - STI (HDD)
* Throughput Optimised for frequently accessed, throuput intensive workload.
* 500 GiB - 16 TiB
* Max IOPS is 500
* Max throughput of 500 MiB/s - can burst
* Recommanded  for :
** Streaming workload.
** Big data, Data warehouses, Log processing.
** Apache Kafka
** Cannot be a boot volume.

h5. EBS - SCI (HDD) 
* Cold Hard Disk Drive, for less frequently accessed workloads.
* 500 GiB - 16 TiB
* Max IOPS is 250
* Max throughput of 250 MiB/s - can burst
* Recommanded  for :
** Throughput orianted storage for large volumes of data that is infrequently accessed.
** Scenarios where the lowest storage cost is important.
** Cannot be a boot volume.

h1. Cost Strategies 

https://aws.amazon.com/ebs/pricing/

h1. Service Constrains 

h5. General :
* Where ever the instances is the EBS Storage will be in the same region.
* When an instances is terminated, the root volume is not lonnger available, but the created EBS are still available.
* Termination Protection is turned off by default.
* Maximum storage size of 16TB
* Use of SSD backed and Provisioned IOPS is recommended for dedicated IO operations as needed
* Only be access by an EC2 instances
* 99.99% available
