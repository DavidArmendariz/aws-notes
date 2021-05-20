# Instance Types

Instance types follow this convention:

> m5.2xlarge

Here:

* **m**: instance class
* **5**: generation (AWS improves them over time)
* **2xlarge**: size within the instance class

## General purpose

Great for a diversity of workloads such as web servers. Example of them are the **T2** instance types.
They offer a great balance for compute, memory and networking.

## Compute Optimized

Great for compute intensive tasks that require high performance processors. For example, these would be great for
things like:

* Scientific modeling and machine learning
* High performance computing (HPC)
* Media transcoding
* Batch processing workloads
* High performance web servers
* Dedicated gaming servers

They are of the **C** type. For example: **C5**, **C4**, etc.

## Memory Optimized

Great for fast performance for workloads that process large data sets in memory. They are great for things like:

* High performance, relational/non-relational databases
* Distributed web scale cache stores
* In-memory databases optimized for business intelligence
* Applications performing real-time processing of big unstructured data

They are of the **R** type. For example: **R5**, **R4**, etc.

## Storage Optimized

Great for storage intensive tasks that require high, sequential read and write access to large data sets on local storage.

* High frequency online transaction processing (OLTP) systems
* Relational and NoSQL databases
* Cache for in-memory databases like Redis
* Data warehousing applications
* Distributed file systems

They are of the **I** and **D** type.
