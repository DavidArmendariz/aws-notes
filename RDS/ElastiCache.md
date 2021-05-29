# ElastiCache

* To manage Redis or Memcached
* Caches are in-memory databases with really high performance, low latency
* Helps reduce load off databases for read intensive workloads
* Helps make your application stateless
* AWS takes care of OS maintenance / patching, optimizations, setup, configuration, monitoring, failure recovery and backups
* Using ELastiCache **involves heavy application code changes**

## Redis

* Multi AZ with Auto-Failover
* Read Replicas to scale reads and have high availability
* Data durability using AOF
* Backup and restore features

## Memcached

* Multi-node for partitioning of data (sharding)
* No high availability (replication)
* Non persistent
* No backup and restore
* Multi-threaded architecture
