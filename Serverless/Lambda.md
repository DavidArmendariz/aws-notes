# AWS Lambda

* Virtual functions, no servers to manage
* Limited by time, short executions
* Run on-demand
* Scaling is automated

## Benefits

* Pay per request and compute time (very cheap)
* Integrated with many AWS services
* Many programming languages
* Easy monitoring through AWS CloudWatch
* Easy to get more resources per functions
* Increasing RAM will also improve CPU and network

## Language support

* Node.js, Python, Java, C#, GoLang, Ruby, Custom Runtime API
* Lambda Container Image
  * The container image must implement the Lambda Runtime API

## Lambda integrations

* API Gateway
* Kinesis
* DynamoDB
* S3
* CloudFront
* CloudWatch Events
* EventBridge
* CloudWatch Logs
* SNS
* SQS
* Cognito

## Limits

* Execution:
  * Memory: 128MB-10GB (64MB increments)
  * Max. execution time: 900 seconds (15 minutes)
  * Environment variabkes (4KB)
  * Disk capacity in the "function container" (in `/tmp`): 512MB
  * Concurrency executions: 1000 (can be increased)
* Deployment
  * Lambda function deployment size (compressed .zip): 50MB
  * Size of uncompressed deployment (code + dependencies): 250MB
  * Can use the `/tmp` directory to load other files at startup
  * Size of environment variables: 4KB
  