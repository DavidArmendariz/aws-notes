# EC2

* EC2 = Elastic Compute Cloud
* You can:
  * Rent virtual machines (EC2)
  * Store data on virtual drives (EBS)
  * Distribute load across machines (ELB)
  * Scale the services using auto scaling groups (ASG)

## EC2 sizing and configuration options

* OS: Linux, Windows, MacOS
* CPU
* RAM
* Storage
  * Network-attached (EBS or EFS)
  * Hardware (EC2 Instance Store)
* Network card: speed of the card, public IP address
* Firewall rules (security groups)
* Bootstrap scripts (EC2 user data)

## EC2 User Data

* It is possible to bootstrap our instances using an EC2 User data script
* bootstrapping means launching commands when a machine starts
* The bootstrap script is only run once at the instance **first start**
* Some common use cases:
  * Installing updates
  * Installing software
  * Downloading common files from the internet
* The EC2 User Data Script runs with the root user (sudo)
