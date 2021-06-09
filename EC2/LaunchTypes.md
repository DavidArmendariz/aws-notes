# Launch Types

* On-Demand Instances: short workload, predictable pricing
* Reserved (Minimum 1 year):
  * Reserved instances: long workloads
  * Convertible Reserved Instances: long workloads with flexible instances
  * Scheduled Reserved Instances: for example, if we need an instance every monday between 3 and 6 pm
* Spot instances: short workloads, cheap, can lose instances so they are less reliable
* Dedicated hosts: book an entire physicial server where you can control the instance placement

## EC2 On Demand

* Pay for what you use
  * For Linux: billing per second , after the first minute
  * For Windows: billing per hour

## EC2 Reserved instances

* Up to 75% discount compared to On Demand
* Reservation period: 1 or 3 years
* Purchasing options
  * No upfront
  * Partial upfront (more discount)
  * All upfront (even more discount)
* Reserve a specific instance type
* Recommended for steady-state usage applications (like databases)

### Convertible Reserved instance

* Can change the EC2 instance type
* Up to 54% discount

### Scheduled Reserved instances

* Launch within time window you reserve
* You still need to commit 1 or 3 years

## EC2 Spot instances

* Can get a discount of up to 90% compared to On Demand
* Instances that you can "lose" at any point of time if your max price is less than the current spot price
* The MOST cost efficient instances in AWS

Use cases:

* Batch jobs
* Data analysis
* Image processing
* Any distributed workloads

## EC2 Dedicated hosts

An Amazon EC2 Dedicated Host is a physical server with EC2 instance capacity fully dedicated to your user. Dedicated Hosts can help you address
**compliance requirements** and reduce costs by allowing you to use **your existing server-bound software licenses**.

You need to commit for a 3 year period reservation.

Use cases:

* Software that have complicated licensing model
* Companies that have strong regulatory or compliance needs

## EC2 Dedicated instances

It's similar to dedicated hosts. Instances are running on hardware that's dedicated to you, but you have no control over instance placement.
