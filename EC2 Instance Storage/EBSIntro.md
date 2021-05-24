# EBS Intro

* An EBS (Elastic Block Store) Volume is a network drive you can attach to your instances while they run
* It allows your instances to persist data, even after their termination
* They can only be mounted to one instance at a time
* They are bound to a specific AZ
* Think of them as "network USB stick"

## EBS Volume

* It's a network drive
  * It uses the network to communicate the instance, which means there might be a bit of latency
  * It can be detached from an EC2 instance and attached to another one quickly
* It's locked to an AZ
  * To move a volume across, you first need to snapshot it
* Have a provisioned capacity (size in GBs and IOPS)

## Delete on termination attribute

* We can delete EBS volumes when EC2 instance is terminated
* By default, the root EBS volume is deleted
* By default, any other attached EBS volume is not deleted
