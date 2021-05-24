# Spot instances

* We can get a discount of up to 90% compared to on-demand
* We can define a **max spot price** and get the instance while `current spot price < max`
  * The hourly spot price varies based on offer and capacity
  * If current spot price > your max price you can choose to stop or terminate your instance with a 2 minute grace period

## Spot block

* "Block" spot instance during a specified time frame (1 to 6 hours) without interruptions
* In rare situations, the instance may be reclaimed

## Terminating spot instances

* You can only cancel spot instance requests that are **open**, **active** or **disabled**
* Cancelling a spot request does not terminate instances
* You must first cancel a spot request and then terminate the associated spot instances

## Spot Fleets

* Spot Fleets = set of spot instances + (optional) on-demand instances
* The spot fleet will try to meet the target capacity with price constraints
  * Define possible launch pools: instance type, OS, AZ
  * Can have multiple launch pools, so that the fleet can choose
  * Spot Fleet stops launching instances when reaching capacity or max cost
* Strategies to allocate Spot Instances:
  * **lowestPrice**: from the pool with the lowest price (cost optimization, short workload)
  * **diversified**: distributed across all pools (great for availability, long workloads)
  * **capacityOptimized**: pool with the optimal capacity for the number of instances
