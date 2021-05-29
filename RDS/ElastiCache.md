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

## Cache security

* All caches in ElastiCache
  * Do not support IAM authentication
  * IAM Policies on ElastiCache are only used for AWS API-level security
* Redis AUTH
  * You can set a "password/token" when you create a Redis cluster
  * This is an extra level of security for your cache on top of security groups
  * Support SSL in flight encryption
* Memcached
  * Supports SASL-based authentication

## Patterns

* Lazy loading: all the read data is cached. Data can become stale in cache
* Write Through: adds or update data in the cache when written to a DB (no stale data)
* Session Store: store temporary session data in a cache (using TTl features)
