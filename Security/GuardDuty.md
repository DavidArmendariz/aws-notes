# Guard Duty

* Intelligent Threat discovery to protect AWS Account
* Uses ML algorithms, anomaly detection, 3rd party data
* One click to enable, no need to install software
* Input data includes
  * CloudTrail Logs: unusual API calls, unauthorize deployments
  * VPC Flow Logs: unusual internal traffic, unusual IP address
  * DNS Logs: compromised EC2 instances sending encoded data within DNS queries
* Can setup CloudWatch Event Rules to be notified in case of findings
* CloudWatch Event rules can target AWS Lambda or SNS
* Can protect against CryptoCurrency attacks (has a dedicated "finding" for it)
