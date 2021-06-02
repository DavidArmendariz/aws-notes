# Docker

* Docker is a software development platform to deploy apps
* Apps are packaged in containers that can be run on any OS
* Apps run the same, regardless of where they are run
  * Any machine
  * No compatibility issues
  * Predictable behavior
  * Less work
  * Easier to maintain and deploy
  * Works with any language, any OS, any technology
* Docker images are stored in docker repositores
* Private: Amazon ECR
* Public: Amazon ECR Public

## Docker vs VMs

* Resources are shared with the host => many containers on one server

## Docker Containers Management

* To manage containers, we need a container management platform
* Three choices:
  * ECS: Amazon's own container platform
  * Fargate: Amazon's own Serverless container platform
  * EKS: Amazon's managed Kubernetes
  