# CloudWatch Logs

* Apps can send logs to CloudWatch using the SDK
* CloudWatch can collect log from:
  * Elastic Beanstalk: collection of logs from application
  * ECS: collection from containers
  * AWS Lambda: collection from function logs
  * VPC Flow Logs: VPC specific logs
  * API Gateway
  * CloudTrail based on filter
  * CloudWatch log agents: for example on EC2 Machines
  * Route53: Log DNS queries
* CloudWatch Logs can go to:
  * Batch exporter to S3 for archival
  * Stream to ElasticSearch cluster for further analytics
* Logs storage architecture:
  * Log groups: arbitrary name, usually representing an application
  * Log stream: instances within application/log files/containers
* Can define log expiration policies (never expire, 30 days, etc...)
* Using the AWS CLI we can tail CloudWatch logs
* To send logs to CloudWatch, make sure IAM permissions are correct

## Metric Filter and Insights

* CloudWatch Logs can use filter expressions
  * Find a specific IP inside of a log
  * Metric filters can be used to trigger alarms
* CloudWatch Logs Insights can be used to query logs and add queries to CloudWatch Dashboards
