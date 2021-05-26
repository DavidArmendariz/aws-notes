# Cross Zone Balancing

With Cross Zone Load Balancing, each load balancer instance distributes evenly
across all registered instances in all AZ

## ALB

* Always on (can't be disabled)
* No charges for inter AZ data

## NLB

* Disabled by default
* You pay charges for inter AZ data if enabled

## Classic Load Balancer

* Through Console: enabled by default
* Through CLI / API: disabled by default
* No charges for inter AZ data if enabled
