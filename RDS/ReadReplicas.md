# Read Replicas

* Up to 5 Read Replicas
* Within AZ, Cross AZ or Cross Region
* Replication is **ASYNC**, so reads are eventually consistent
* Replicas can be promoted to their own DB

## Network Cost

* In AWS there's a network cost when data goes from one AZ to another
* For RDS Read Replicas within the same region, you don't pay that fee

## RDS Multi AZ (disaster recovery)

* SYNC replication
* One DNS name, automatic app failover to standby
* Increase availability
* Failover in case of loss of AZ, loss of network, instance or storage failure

## From single AZ to multi AZ

* Zero downtime
* The following happens internally
  * A snapshot is taken
  * A new DB is restored from the snapshot in a new AZ
  * Synchronization is established between two databases
