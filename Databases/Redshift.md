# Redshift

* Based on PostgreSQL, but not used for OLTP
* It is for OLAP
* 10x better performance than other data warehouses
* Columnar storage of data
* Massively Parallel Query Execution (MPP)
* Pay as you go on the instances provisioned
* Has a SQL interface for performing the queries
* BI tools such as AWS Quicksight or Tableau integrate with it
* Data is loaded from S3, DynamoDB, DMS, other DBs
* From 1 node to 128 nodes, up to 160GB of space per node
* Leader node: for query planning, results aggregation
* Compute node: for performing the queries, send results to leader
* Redshift Spectrum: perform queries directly against S3 (no need to load)
* Backup and restore, Security VPC/IAM/KMS, Monitoring
* Redshift Enhanced VPC Routing: COPY/UNLOAD goes through VPC

## Snapshots and DR

* Redshift has no Multi-AZ mode
* Snapshots are point-in-time backups of a cluster, stored internally in S3
* Snapshots are incremental (only what has changed is saved)
* You can restore a snapshot into a new cluster
* Automated: every 8 hours, every 5GB, or on a schedule. Set retention
* Manual: snapshot is retained until you delete it

## Loading data into Redshift

* Amazon Kinesis Data Firehose
* S3 using COPY command
* EC2 instance (JDBC driver)

## Redshift Spectrum

* Query data that is already in S3 without loading it
* Must have a Redshift cluster available to start the query
* The query is then submitted to thousands of Redshift Spectrum nodes
