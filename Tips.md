* AWS S3 Access Control Lists:
  * Within Amazon S3, you can use ACLs to give read or write access on buckets or objects to group of users. With
  ACLs you can only grant other AWS accounts (not specific users) access to your Amazon S3 resources.
* Amazon EFS Access Points:
  * Amazon EFS access points are application-specific entry points into an EFS file system that make it easier to manage application access to shared datasets. Access points can enforce a user identity, including the user's POSIX groups, for all file system requests that are made through the access point. Access points can also enforce a different root directory for the file system so that clients can only access data in the specified directory or its subdirectories.
  You can use AWS Identity and Access Management (IAM) policies to enforce that specific applications use a specific access point. By combining IAM policies with access points, you can easily provide secure access to specific datasets for your applications.
* VPC Sharing (part of **Resource Access Manager**):
  * VPC sharing allows multiple AWS accounts to create their application resources, such as Amazon EC2 instances, Amazon Relational Database Service (RDS) databases, Amazon Redshift clusters, and AWS Lambda functions, into shared, centrally-managed virtual private clouds (VPCs). In this model, the account that owns the VPC (owner) shares one or more subnets with other accounts (participants) that belong to the same organization from AWS Organizations. After a subnet is shared, the participants can view, create, modify, and delete their application resources in the subnets shared with them. Participants cannot view, modify, or delete resources that belong to other participants or the VPC owner.
* EBS Encryption allows:
  * Data at rest inside the volume
  * All data moving between the volume and the instance
  * All snapshots created from the volume
  * All volumes created from those snapshots
* VPC-enabled Lambda functions:
  * Lambda functions always operate from an AWS-owned VPC. By default, your function has the full ability to make network requests to any public internet address — this includes access to any of the public AWS APIs. For example, your function can interact with AWS DynamoDB APIs to PutItem or Query for records. You should only enable your functions for VPC access when you need to interact with a private resource located in a private subnet. An RDS instance is a good example.
  Once your function is VPC-enabled, all network traffic from your function is subject to the routing rules of your VPC/Subnet. If your function needs to interact with a public resource, you will need a route through a NAT gateway in a public subnet.
* Launch configurations:
  * A launch configuration is an instance configuration template that an Auto Scaling group uses to launch EC2 instances. When you create a launch configuration, you specify information for the instances. Include the ID of the Amazon Machine Image (AMI), the instance type, a key pair, one or more security groups, and a block device mapping.
  It is not possible to modify a launch configuration once it is created.
* FIFO queues:
  * You can't convert an existing standard queue into a FIFO queue.
* Snowball Edge:
  * Snowball Edge Storage Optimized is the optimal choice if you need to securely and quickly transfer dozens of terabytes to petabytes of data to AWS. It provides up to 80 TB of usable HDD storage, 40 vCPUs, 1 TB of SATA SSD storage, and up to 40 Gb network connectivity to address large scale data transfer and pre-processing use cases. The data stored on the Snowball Edge device can be copied into the S3 bucket and later transitioned into AWS Glacier via a lifecycle policy. You can't directly copy data from Snowball Edge devices into AWS Glacier.
* Aurora:
  * An Amazon Aurora DB cluster consists of one or more DB instances and a cluster volume that manages the data for those DB instances. An Aurora cluster volume is a virtual database storage volume that spans multiple Availability Zones, with each Availability Zone having a copy of the DB cluster data. Two types of DB instances make up an Aurora DB cluster:
  Primary DB instance – Supports read and write operations, and performs all of the data modifications to the cluster volume. Each Aurora DB cluster has one primary DB instance.
  Aurora Replica – Connects to the same storage volume as the primary DB instance and supports only read operations. Each Aurora DB cluster can have up to 15 Aurora Replicas in addition to the primary DB instance. Aurora automatically fails over to an Aurora Replica in case the primary DB instance becomes unavailable. You can specify the failover priority for Aurora Replicas. Aurora Replicas can also offload read workloads from the primary DB instance.
* AWS Global Accelerator:
  * AWS Global Accelerator is a networking service that helps you improve the availability and performance of the applications that you offer to your global users. AWS Global Accelerator is easy to set up, configure, and manage. It provides static IP addresses that provide a fixed entry point to your applications and eliminate the complexity of managing specific IP addresses for different AWS Regions and Availability Zones. AWS Global Accelerator always routes user traffic to the optimal endpoint based on performance, reacting instantly to changes in application health, your user’s location, and policies that you configure. Global Accelerator is a good fit for non-HTTP use cases, such as gaming (UDP), IoT (MQTT), or Voice over IP. Therefore, this option is correct.
* AWS X-Ray
  * AWS X-Ray helps developers analyze and debug production, distributed applications, such as those built using a microservices architecture. With X-Ray, you can understand how your application and its underlying services are performing to identify and troubleshoot the root cause of performance issues and errors. X-Ray provides an end-to-end view of requests as they travel through your application, and shows a map of your application’s underlying components.
  You can use X-Ray to collect data across AWS Accounts. The X-Ray agent can assume a role to publish data into an account different from the one in which it is running. This enables you to publish data from various components of your application into a central account.
* ECS Fargate vs ECS EC2
  * The pricing for the EC2-based launch type is fixed to the memory and capacity provisioned for a chosen instance type. You pay for a full instance regardless of how much of it is being used by the workload. In comparison, Fargate gives an alternative where pricing can often more closely match resource requirements. Fargate workloads are charged for the CPU and memory consumed for a single task, and AWS manages the allocation of these tasks on the underlying infrastructure. Up until a certain threshold, pricing specificity provided by Fargate becomes more cost effective over an EC2-based launch. However, there comes a point where managing your own EC2 fleet is more cost effective than using Fargate. Defining these boundaries is the focus of this post, but bear in mind that you are not limited to an either/or choice, you can use both simultaneously, via Amazon ECS Capacity Providers.
* Lifecycle policy to transition the objects from Amazon S3 Standard to Amazon S3 One Zone-Infrequent Access
  * The minimum storage duration is 30 days before you can transition objects from S3 Standard to S3 One Zone-IA or S3 Standard-IA.
* Storage device decommissioning
  * AWS will initiate a decommissioning process when a storage device has reached the end of its useful life. This process ensures that customer data is not exposed to unauthorized individuals. This hardware device will be physically destroyed or degaussed if it fails decommissioning using the standard process followed by AWS.
* Penetration testing
  * May be performed by the customer against their own instances with prior authorization from AWS
* Shared EC2 instances
  * Different instances running on the same physical machine are isolated from each other via the Xen hypervisor
* Moving an instance from to another placement group
  * You can change the placement group for an instance in any of the following ways:
    * Move an existing instance to a placement group
    * Move an instance from one placement group to another
    * Remove an instance from a placement group
  Before you move or remove the instance, the instance must be in the **stopped** state. You can move or remove an instance using the AWS CLI or an AWS SDK.
* VPC sizes:
  * It is not possible to change the size of the VPC once it has been created
  * This also applies for subnets within the VPC: it is not possible to modify the CIDR of a subnet
* VPC CIDR:
  * You cannot have CIDR Overlaps. If your subnets overlap, you will get a CIDR overlaps error.
* Deleting VPCs:
  * You can delete a VPC even if you have a Virtual Private Gateway. The console will delete all the setups and also delete the Virtual Private Gateway.
  * If you have a running NAT instance, you cannot delete your VPC until you terminate it
* IAM Limits:
  * One AWS Account can have a maximum of 5000 IAM users
* Subnets:
  * Default subnets are assigned a /20 subnet mask
* EC2 Reserved instances:
  * If your AMI changes the reserved instance is still valid if it's the same instance type
  * You can shut down the reserved instance any time you want and the hourly charge won't incur for the shutdown hours
  * It saves you significant money over on-demand instances
* RDS RAID:
  * Amazon recommends RAID 5 and RAID 6 for EBS
* EBS Size:
  * Maximum size of EBS is 1TB
* AMI:
  * You can share your AMI with other AWS account owners
  * You can create an instance store-backed AMI
  * You can create an EBS-backed AMI
  * For instance store-backed AMIs, the root volume is stored in S3
* AWS KMS:
  * AWS KMS supports two kinds of keys — master keys and data keys. Master keys can be used to directly encrypt and decrypt up to 4 kilobytes of data and can also be used to protect data keys. The data keys are then used to encrypt the customer data and the master keys are used to decrypt the customer data
* Amazon S3 Success:
  * A HTTP 200 result code and MD5 checksum, taken together, indicate that the operation was successful
  