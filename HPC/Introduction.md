# Compute and networking

* EC2 Enhanced Networking (SR-IOV)
  * Higher bandwidth, higher PPS (packet per second), lower latency
  * Option 1: Elastic Network Adapter (ENA) up to 100Gbps
  * Option 2: Intel  82599 VF up to 10Gbps (LEGACY)
* Elastic Fabric Adapter (EFA)
  * Improved ENA for HPC, only works for Linux
  * Great for inter-node communications, tightly coupled workloads
  * Leverages Message Passing Interface (MPI) standard
  * Bypasses the underlying Linux OS to provide low-latency, reliable transport

## Storage

* Instance-attached storage:
  * EBS: scale up to 64000 IOPS with io1 Provisioned IOPS
  * Instance Store: scale to millions of IOPS, linked to EC2 instance, low latency
* Network storage:
  * Amazon S3: large blob, not a file system
  * Amazon EFS: scale IOPS based on total size, or use provisioned IOPS
  * Amazon FSx for Lustre:
    * HPC optimized distributed file system, millions of IOPS
    * Backed by S3

## Automation and Orchestration

* AWS Batch
  * AWS Batch supports multi-node parallel jobs, which enables you to run single jobs that span multiple EC2 instances
  * Easily schedule jobs and launch EC2 instances accordingly
* AWS ParallelCluster
  * Open source cluster management tool to deploy HPC on AWS
  * Configure with text files
  * Automate creation of VPC, subnet, cluster type and instance types
  