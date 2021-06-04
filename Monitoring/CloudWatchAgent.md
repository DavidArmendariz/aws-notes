# CloudWatch Agent

* By default, no logs from your EC2 machine will go to CloudWatch
* You need to run a CloudWatch agent on EC2 to push the log files you want
* Make sure IAM permissions are correct
* The CloudWatch log agent can be setup on premises too
* For virtual servers (EC2 instances, on-premises servers)
* CloudWatch Logs Agent
  * Old version of the agent
  * Can only send to CloudWatch Logs
* CloudWatch Unified Agent
  * Collect additional system-level metrics such as RAM, processes, etc...
  * Collect logs to send to CloudWatch Logs
  * Centralized configuration using SSM Parameter Store

## Metrics

* Collected directly on your Linux server/EC2 instance
* CPU
* Disk metrics
* RAM
* Netstate
* Processes
* Swap Space
