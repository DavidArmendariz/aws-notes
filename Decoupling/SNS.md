# SNS

* What if you want to send one message to many receivers?
* The "event producer" only sends messages to one SNS topic
* As many "event receivers" (subscriptions) as we want to listen to the SNS topic notifications
* Each subscriber to the topic will get all the messages
* Up to 10 million subscriptions per topic
* 100,000 topics limit
* Subscribers can be:
  * SQS
  * HTTP/HTTPS
  * Lambda
  * Emails
  * SMS messages
  * Mobile notifications
* Many AWS services can send data directly to SNS for notifications
* CloudWatch (for alarms)
* Auto Scaling Groups notifications
* Amazon S3 (on bucket events)
* CloudFormation (upon state changes => failed to build, etc)

## How to publish

* Topic publish (using the SDK)
  * Create a topic
  * Create a subscription (or many)
  * Publish to the topic
* Direct Publish (for mobile apps SDK)
  * Create a platform application
  * Create a platform endpoint
  * Publish to the platform endpoint
  * Works with Google GCM, Apple APNS, Amazon ADM

## Security

* Encryption:
  * In-flight encryption using HTTPS API
  * At-rest encryption using KMS keys
  * Client-side encryption if the client wants to perform encryption/decryption itself
* Access Controls: IAM policies to regulate access to the SNS API
* SNS Access Policies (similar to S3 bucket policies)
  * Useful for cross-account access to SNS topics
  * Useful for allowing other services (S3...) to write to an SNS topic
  