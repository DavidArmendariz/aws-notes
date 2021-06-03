# DynamoDB

* Fully managed, HA, with replication across 3 AZ
* NoSQL
* Scales to massive workloads, distributed database
* Millions of requests per seconds, trillions of row, 100s of TB of storage
* Fast and consistent in performance
* Integrated with IAM for security, authorization and aministration
* Enables event driven programming with DynamoDB Streams
* Low cost and auto scaling capabilities

## Basics

* DynamoDB Is made of tables
* Each table has a primary key
* Each table can have an infinite number of items
* Each item has attributes
* Maximum size of an item is 400KB
* Data types supported are:
  * Scalar Types
  * Document Types
  * Set Types

## Provisioned Throughput

* Table must have provisioned read and write capacity units
* Read Capacity Units (RCU): throughput for reads
  * 1 RCU = 1 strongly consistent read of 4KB per second
  * 1 RCU = 2 eventually consistent read of 4KB per second
* Write Capacity Units (WCU): throughput for writes
  * 1 WCU = 1 write of 1KB per seconds
* Option to setup auto-scaling of throughput to meet demand
* Throughput can be exceeded temporarily using "burst credit"
* If burst credit are empty, you will get a `ProvisionedThroughputException`

## DAX

* Seamless cache for DynamoDB, no application re-write
* Writes go through DAX to DynamoDB
* Micro second latency for cached reads and queries
* Solves the Hot Key problem (too many reads)
* 5 minutes TTL for cache by default
* Up to 10 nodes in the cluster
* Multi AZ
* Secure

## DynamoDB Streams

* Changes in DynamoDB (Create, Update, Delete) can end up in a DynamoDB Stream
* This stream can be read by AWS Lambda, and we can then do:
  * React to changes in real time
  * Analytics
  * Create derivative tables/views
  * Insert into ElasticSearch
* Could implement cross region replication using Streams
* Stream has 24 hours of data retention

## New Features

* Transactions
* On Demand
  * No capacity planning needed - scales automatically

## Security and Other Features

* Security:
  * VPC endpoints available to access DynamoDB without internet
  * Access fully controlled by IAM
  * Encryption at rest using KMS
  * Encryption in transit using SSL/TLS
* Backup and Restore feature available
  * Point in time restore like RDS
  * No performance impact
* Global Tables
  * Multi region, fully replicated, high performance
* Amazon DMS can be used to migrate to DynamoDB (from Mongo, Oracle, MySQL, S3, etc)
* You can launch a local DynamoDB on your computer for development purposes
