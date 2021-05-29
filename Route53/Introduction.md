# Route53

* Managed DNS
* DNS is a collection of rules and records which helps clients understand how to reach a server through its domain name
* In AWS, the most common records are:
  * A: hostname to IPv4
  * AAAA: hostname to IPv6
  * CNAME: hostname to hostname
  * Alias: hostname to AWS resource
* Route53 can use:
  * Public domain names you own
  * Private domain names that can be resolved by your instances in your VPCs
* Features:
  * Load balancing (through DNS)
  * Health checks
  * Routing policy
    * simple
    * failover
    * geolocation
    * latency
    * weighted
    * multi value
