# Directory Services

## Microsoft Active Directory

* Found on any Windows Server with AD Domain Services
* Database of objects: user accounts, computers, printers, file shares, security groups
* Centralized security management, create account, assign permissions
* Objects are organized in **trees**
* A group of trees is a **forest**

## AWS Directory Services

* AWS Managed Microsoft AD
  * Create your own AD in AWS, manage users locally, supports MFA
  * Establish "trust" connections with your on-premise AD
* AD Connector
  * Directory Gateway (proxy) to redirect to on-premise AD
  * Users are managed on the on-premise AD
* Simple AD
  * AD-compatible managed directory on AWS
  * Cannot be joined with on-premise AD
  