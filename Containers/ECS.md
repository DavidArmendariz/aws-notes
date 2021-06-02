# ECS

* Launch Docker containers on AWS
* You must provision and maintain the infrastructure (EC2 instances)
* AWS takes care of starting/stopping containers
* Has integrations with the ALB

![ECS](images/ECS.png)

## Fargate

* Launch Docker containers on AWS
* You do not provision the infrastructure (no EC2 instances to manage)
* AWS just runs containers for you based on the CPU/RAM you need

![Fargate](images/Fargate.png)

## IAM Roles for ECS Tasks

![Roles](images/Roles.png)

## ECS Data Volumes - EFS File Systems

![DataVolumes](images/DataVolumes.png)

## ECS Services and Tasks

![ServicesAndTasks](images/ServicesAndTasks.png)

## Load Balancing for EC2 Launch Type

![LoadBalancing](images/LoadBalancing.png)

## Load Balancing for Fargate

![LoadBalancingFargate](images/LoadBalancingFargate.png)

## ECS tasks invoked by Event Bridge

![EventBridge](images/EventBridge.png)
