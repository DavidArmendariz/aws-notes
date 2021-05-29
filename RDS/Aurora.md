# Aurora

* Compatible with Postgres and MySQL
* Aurora is AWS cloud optimized and claims 5x performance improvement over MySQL on RDS, over 3x the performance of Postgres on RDS
* Aurora storage automatically grows in increments of 10GB up to 64TB
* Can have 15 replicas while MySQL has 5 and th replication process is faster (sub 10 ms replica lag)
* Failover in Aurora is instantaneous

## High availability and read scaling

* 6 copies of your data across 3 AZ
  * 4 copies out of 6 needed for writes
  * 3 copies out of 6 need for reads
  * Self healing with peer-to-peer replication
  * Storage is striped across 100s of volumes
* One Aurora instance takes writes (master)
* Automated failover for master in less than 30 seconds
* Master + up to 15 Aurora Read Replicas serve reads
* Support for Cross Region Replication

## Aurora DB Cluster

* Writer endpoint (pointing to the master)
* Reader endpoint (connection load balancing)

## Security

* Similar to RDS because uses the same engine
