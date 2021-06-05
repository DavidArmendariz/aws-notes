# IAM Conditions

* `aws:SourceIP`: restrict the client IP from which the API calls are being made
* `aws:RequestedRegion`: restric the region the API calls are made to
* Restrict based on tags
* Force MFA

## IAM Roles vs Resource Based Policies

* Attach a policy to a resource versus attaching of a using a role as a proxy
* When you assume a role, you give up your original permissions and take the permissions assigned to the role
* When using a resource based policy, the principal doesn't have to give up his permissions
* Example: User in Account A needs to scan a DynamoDB table in Account A and dump it in an S3 bucket in Account B
* Supported by: Amazon S3 buckets, SNS topics, SQS queues
