# Hibernate

* When we stop EC2 instances:
  * The data on disk (EBS) is kept intact in the next start
* When we terminate an EC2 instance:
  * Any EBS volume (root) also set up to be destroyed is lost
* With EC2 Hibernate:
  * The in-memory (RAM) is preserved
  * The instance boot is much faster (the OS is not stopped / restarted)
  * Under the hood: the RAM state is written to a file in the root EBS volume
  * The root EBS volume must be encrypted

## Use cases

* long-running processing
* saving the RAM state
* services that take time to initialize

## Things to know

* Not all instance types are supported
* Instance RAM size must be less than 150 GB
* Not all AMIs are supported
* The root volume must be EBS, encrypted, not instance store and large
* Available for on-demand and reserved instances
* An instance cannot be hibernated more than 60 days
