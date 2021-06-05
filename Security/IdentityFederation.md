# Identity Federation

* Federation lets users outside of AWS to assume temporary role for accessing AWS resources
* These users assume identity provided access role
* Federations can have many flavors:
  * SAML 2.0
  * Custom Identity Broker
  * Web Identity Federation with Amazon Cognito
  * Web Identity Federation without Amazon Cognito
  * Single Sign On
  * Non-SAML with AWS Microsfot AD
* Using federation, you don't need to create IAM users (user management is outside of AWS)

## SAML 2.0 Federation

* To ingreate Active Directory/ADFS with AWS (or any SAML 2.0)
* Provides access to AWS Console or CLI (through temporary creds)
* No need to create an IAM user for each of your employees

## Active Directory FS

* Same process as with any SAML 2.0 compatible IdP

## Summary

* Needs to setup a trust between AWS IAM and SAML (both ways)
* SAML 2.0 enables web-based, cross domain SSO
* Uses the STS API: `AssumeRoleWithSAML`

> Note: federation through SAML is the "old way" of doing things. Amazon SSO (Single Sign On) Federation is the new managed and simpler way

## Custom Identity Broker Application

* Use only if identity provider is not compatible with SAML 2.0
* The identity broker must determine the appropriate IAM policy
* Uses the STS API: `AssumeRole` or `GetFederationToken`

## Web Identity Federation (AssumeRoleWithWebIdentity)

* Not recommended by AWS (use Cognito instead)

## Cognito

* Goal:
  * Provide direct access to AWS Resources from the client side
* Example:
  * Provide (temporary) access to write to S3 bucket using Facebook Login
* Problem:
  * We don't want to create IAM users for our app users
* How:
  * Log in to federated identity provider (or remain anonymous)
  * Get temporary AWS credentials back from the Federated Identity Pool
  * These credentials come with a pre-defined IAM policy stating their permissions
  