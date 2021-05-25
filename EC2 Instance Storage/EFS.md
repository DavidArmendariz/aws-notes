# Elastic File System

* Managed NFS (network file system) that can be mounted on many EC2
* EFS works with EC2 instances in multi AZ
* Highly available, scalable, expensive, pay per use
* Use cases:
  * content management
  * web serving
  * data sharing
  * wordpress
* Uses security group to control access to EFS
* Compatible with Linux based AMI (not Windows)
* Encryption at rest using KMS
* POSIX file system that has a standard file API
* File system scales automatically, pay-per-use, no capacity planning
* Performance mode (set at EFS creation time)
  * General purpose (default): latency sensitive use cases
  * Max I/O: higher latency, throughput, highly parallel
* Throughput mode
  * Bursting
  * Provisioned
* Storage Tiers
  * Standard
  * Infrequent access
