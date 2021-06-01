# Amazon SQS

## Standard Queue

* Oldest offering (over 10 years old)
* Fully managed service, used to decouple apps
* Attributes:
  * Unlimited throughput, unlimited number of messages in queue
  * Default retention of messages: 4 days, max of 14 days
  * Low latency (<10 ms on publish and receive)
  * Limitation of 256KB per message sent
* Can have duplicate messages (at least once delivery, occasionally)
* Can have out of order messages

## Producing messages

* Produced to SQS using the SDK (SendMessage API)
* The message is persisted in SQS until a consumer deletes it

## Consuming messages

* Consumers (running on EC2 instances, servers, or AWS Lambda)...
* Poll SQS for messages (receive up to 10 messages at a time)
* Process the messages
* Delete the messages using the `DeleteMessage` API

## Multiple EC2 instances consumers

* Consumers receive and process messages in parallel
* At least once delivery
* Best-effort message ordering
* Consumers delete messages after processing
* We can scale consumers horizontally to improve throughput of processing

## Use cases

* SQS with Auto Scaling Group
* SQS to decouple between application tiers

## Security

* Encryption:
  * In-flight encryption using HTTPS API
  * At-rest encryption using KMS keys
  * Client-side encryption if the client wants to perform encryption/decryption itself
* Access Controls: IAM policies to regulate access to the SQS API
* SQS Access Policies (similar to S3 bucket policies)
  * Useful for cross-account access to SQS queues
  * Useful for allowing other services (SNS, S3, ...) to write to an SQS queue

## Access Policy

* Cross Account Access
* Publish S3 Event Notifications to SQS Queue
