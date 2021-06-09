# Instance Types

All: https://aws.amazon.com/ec2/instance-types/

Instance types follow this convention:

> m5.2xlarge

Here:

* **m**: instance class
* **5**: generation (AWS improves them over time)
* **2xlarge**: size within the instance class

## General purpose

* Great for a diversity of workloads such as web servers or code repositories.
* Balance between:
  * Compute
  * Memory
  * Networking
* Example of them are the **t** an **m** instance types. For example: **T2**, **M5**, etc.

## Compute Optimized

* Great for compute intensive tasks that require high performance processors.
* Use cases:
  * Scientific modeling and machine learning
  * High performance computing (HPC)
  * Media transcoding
  * Batch processing workloads
  * High performance web servers
  * Dedicated gaming servers
* They are of the **C** type. For example: **C5**, **C4**, etc.

## Memory Optimized

* Fast performance for workloads that process large data sets in memory. They are great for things like:
* Use cases:
  * High performance, relational/non-relational databases
  * Distributed web scale cache stores
  * In-memory databases optimized for business intelligence
  * Applications performing real-time processing of big unstructured data
* Example of them are the **R** instance types. For example: **R4**, **R5**, etc.

## Storage Optimized

* Great for storage intensive tasks that require high, sequential read and write access to large data sets on local storage.
* Use cases:
  * High frequency online transaction processing (OLTP) systems
  * Relational and NoSQL databases
  * Cache for in-memory databases like Redis
  * Data warehousing applications
  * Distributed file systems

* Example of them are the **I** and **D** instance types. For example: **I3**, **D3**, etc.
