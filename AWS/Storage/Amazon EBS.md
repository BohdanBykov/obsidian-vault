(Core AWS storage services, AWS course)
***
# Overview

Elastic Block Storage service is an easy-to-use and high performance, designed for use with [[Amazone EC2]] compute instances for both throughput and transaction-intensive workloads at any scale. 

AWS recommends Amazon EBS for data that must be quickly accessible and requires long-term persistence. EBS volumes are well suited for the use as primary storage for the file systems, databases or any application that requires fine granular updates and access to raw, unformatted, block-level storage. Amazon EBS is well suited to both database-style applications that rely on random reads and writes and to throughput-intensive applications that perform long, sequential reads and writes.

EBS volume behave like raw, unformatted block devices. You can mount these block devices as EBS volumes on your EC2 instances. EBS volumes that are attached to an EC2 instance are exposed as raw block storage volumes that persist independently from the life of the instance. You can create a file system on top of these volumes or use them in any way you would use a block device (hard drive). You can dynamically change the configuration of a volume attached to an EC2 instance, unlike traditional disk drives that come in fixed sizes.

You can choose from different EBS volume types to balance optimal price and performance.
You can achieve single-digit millisecond latency for high-performance database workloads, such as SAP HANA(?), or gigabyte-per-second throughout of large, sequential workloads such as Apache Hadoop. You can change EBS volumes types, tunes performance, or increase volume size without disrupting your critical applications. Amazon EBS provides you cost-effective block-storage when you need it.

Designed for mission-critical systems, EBS volumes are replicated withing an AWS
Availability Zone and scale to store petabytes of data. Also, you can use EBS snapshots with automated lifecycle policies to back up your volumes in [Amazon S3] (Simple Storage Service). You can do this while ensuring geographical protection of your data and business continuity.

With Amazone EBS, you pay only for the storage and resources that you provision.
***

# Features

- ## Single Availability Zone
	 You create EBS volume in the same Availability Zone as your EC2 instance, it provides low latency and high-performance block storage for your work load. Also, you can create a snapshot and restore it to a new volume anywhere in the same AWS Region.

- ## Persistence 
	 Amazon EBS volumes are durable and persistent by default. It will survive, even if your EC2 instance is terminated. EBS volumes are managed independently of the [[Amazon EC2]] instances to which they are attached. You can detach an existing EBS volume from an EC2 instance and reattach it to a different EC2 instance. This provides you the ability to change EC2 instance types to meet your performance requirements and optimize your [[Amazon EC2]] costs.

- ## Volume types 
	 Amazon EBS provides multiple volume types that you can use to optimize storage performance and cost.
	 - SSD-based
		 - gp3 and gp2 (General Purpose) SSD volumes balanced price and performance for transactional applications, including virtual desktops, test and development environments, and interactive gaming applications.
		 - io2 and io3 (Provisioned) IOPS SSD volumes have the highest performance, for most demanding transactional applications, including SAP HANA, Microsoft SQL Server etc.
	- HDD-based
		- st1 (Throughout Optimized) HDD for frequently accessed and throughput-intensive workloads
		- sc1 (Cold) HDD has the lowest cost, for less frequently accessed data.

- ## Elastic volumes
	 Using it, you can adapt your volumes as the needs of your application change. Use this feature to increase capacity, tune performance, and change the type of any new or existing current generation volume dynamically, with no downtime or performance impact. You can make modifications in the future as your business needs change

- ## Data encryption
	 You can create your EBS volumes as encrypted volumes to meet a wide range of data-at-rest encryption requirements for regulated/audited data and applications. The encryption occurs on the server that host EC2 instances, providing encryption of data in transit from EC2 instances to Amazon EBS storage.

- ## Native snapshot support
	 You can create point-in-time snapshots of EBS volumes, which are persisted to [Amazon S3]. Snapshots protect data for long-term durability. You can use snapshots to restore your data to new volumes, expand the size of a volume, or move volumes across Availability Zones.

- ## AWS Backup 
	 With AWS Backup, you can back up EBS volumes, centralize and automate data protection across multiple Amazon EBS volumes.

- ## Performance monitoring
	 Performance metrics, such as bandwidth, throughput, latency, and average queue length, are available through the AWS Management Console. Amazon CloudWatch provides these metrics so that you can monitor the performance of your volumes. You can make sure that you are providing enough performance for your applications and paying only for resources you need.
***

# Amazon EBS use cases

![[Pasted image 20221217205007.png]]

- ## Enterprise applications
	 Amazon EBS provides high availability and high durability block storage to reliably run mission-critical applications. These applications include Oracle, SAP, Microsoft Exchange, Microsoft SharePoint and VMware applications on VMware Cloud on AWS. 

	 For more information, see [Lift-and-Shift Application Workloads.](https://aws.amazon.com/products/storage/lift-and-shift/)

- ## Relational databases
	 Amazon EBS scales with your performance needs, whether you are supporting millions of gaming customers or billions of ecommerce transactions. Databases such as SAP HANA, Oracle, Microsoft SQL, MySQL and PostgreSQL are widely deployed on Amazon EBS.

- ## NoSQL databases
	 Amazon EBS volumes provide consistent and low-latency performance for running NoSQL databases such as Cassandra, MongoDB, and CouchDB.

- ## Big data analytics engines
	 Amazon EBS offers data persistence, dynamic-performance adjustments, and the ability to detach and re-attach volumes. With these capabilities, you can resize clusters for big data analytics engines such as Hadoop and Spark.

- ## File systems and media workflows
	 With Amazon EBS, you can scale easily with additional volumes to support growing file systems. You can also choose from four different volumes to optimize price and performance.
