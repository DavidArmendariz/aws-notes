# STS

* Allows to grant limited and temporary access to AWS resources
* Token is valid for up to one hour (must be refreshed)
* **AssumeRole**
  * Within your own account: for enhanced security
  * Cross Account Access: assume role in target account to perform actions there
* **AssumeRoleWithSAML**
  * return credentials for users logged with SAML
* **AssumeRoleWithWebIdentity**
  * return creds for users logged with an IdP (Facebook Login, Google Login, OIDC compatible)
  * AWS recommends against using this, and using Cognito instead
* **GetSessionToken**
  * for MFA, from a user or AWS account root user

## Using STS to Assume a Role

* Define an IAM Role within your account or cross-account
* Define which principals can access this IAM Role
* Use AWS STS to retrieve credentials and impersonate the IAM Role you have access to
* Temporary credentials can be valid between 15 minutes to 1 hour
