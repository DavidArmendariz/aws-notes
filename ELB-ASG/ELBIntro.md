# ELB Introduction

* Load balancers are servers that forward internet traffic to multiple servers (EC2 instances) downstream
* Spread load across multiple downstream instances
* Expose a single point of access (DNS) to your application
* Seamlessly handle failures of downstream instances
* Do regular health checks to your instances
* Provide SSL termination (HTTPS) for your websites
* Enforce stickiness with cookies
* High availability across zones
* Separate public traffic from private traffic
* An ELB (EC2 Load Balancer) is a manager load balancer
  * AWS guarantees that it will be working
  * AWS takes care of upgrades, maintenance, high availability
  * AWS provides only a few configuration knobs

## Health checks

* They enable the load balancer to know if instances it forwards traffic to are available to reply to requests
* The health check is done on a port and a route (`/health` is common)
* If the response is not 200 (OK), then the instance is unhealthy

## Types of load balancers

* Classic Load Balancer (v1, old generation, 2019)
  * HTTP, HTTPS, TCP
* Application Load Balancer (v2, new generation, 2016)
  * HTTP, HTTPS, WebSocket
* Network Load Balancer (v2, new generation, 2017)
  * TCP, TLS, UDP

## Good things to know

* LBs can scale but not instantaneously
