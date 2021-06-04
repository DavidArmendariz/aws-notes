# CloudTrail

* Provides governance, compliance and audit for you AWS account
* CloudTrail is enabled by default
* Get a history of events/API calls made within your AWS Account by:
  * Console
  * SDK
  * CLI
  * AWS Services
* Can put logs from CloudTrail into CloudWatch Logs or S3
* A trail can be applied to All regions (default) or a single region
* If a resource is deleted in AWS, investigate CloudTrail first!

## Events

* Management Events:
  * Operations that are performed on resources in your AWS account
  * Examples:
    * Configuring security
    * Configuring rules for routing data
    * Setting up logging
  * By default, trails are configured to log management events
  * Can separate Read Events from Write Events
* Data Events:
  * By default, data events are not logged (because high volume operations)
  * Amazon S3 object-level activity
  * AWS Lambda function execution activity

## CloudTrail Insights

* Enable CloudTrail Insights to detect unusual activity in your account
  * Inaccurate resource provisioning
  * Hitting service limits
  * Burst of AWS IAM actions
  * Gaps in periodic maintenance activity
* CloudTrail Insights analyzes normal management events to create a baseline
* And then continuously analyzes write events to detect unusual patterns
  * Anomalies appear in the CloudTrail console
  * Event is sent to Amazon S3
  * An EventBridge event is generated (for automation needs)

## CloudTrail Events Retention

* Events are stored for 90 days in CloudTrail
* To keep events beyond this period, log them to S3 and use Athena
