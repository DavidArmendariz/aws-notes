# AWS KMS

* Easy way to control access to your data, AWS manages keys for us
* Fully integrated with IAM for authorization
* Integrates with:
  * EBS
  * S3
  * Redshift
  * RDS
  * SSM

## Customer Master Key

* Symmetric (AES-256 Keys)
  * First offering of KMS, single encryption key that is used to encrypt and decrypt
  * AWS services that are integrated with KMS use symmetric CMKs
  * Necessary for envelope encryption
  * You never get access to the key unencrypted (must call KMS API to use)
* Asymmetric (RSA and ECC key pairs)
  * Public (encrypt) and private key (decrypt) pair
  * Used for encrypt/decrypt or sign/verify operations
  * The public key is downloadable, but you can't access the private key unencrypted
  * Use case: encryption outside of AWS by users who can't call the KMS API

## KMS

* Able to fully manage the keys and policies:
  * Create
  * Rotation policies
  * Disable
  * Enable
* Able to audit key usage (using CloudTrail)
* Three types of CMK:
  * AWS Managed Service Default CMK: free
  * User Keys created in KMS: $1 per month
  * User Keys imported (must be 245-bit symmetric key): $1/month
* plus pay for API call to KMS
* Never store your secrets in plain text, especially in your code
* Encrypted secrets can be stored in the code/environment variables
* KMS can only help in encrypting up to 4KB of data per call
* If data > 4KB, use envelop encryption
* To give access to KMS to someone:
  * Make sure the key policy allows the user
  * Make sure the IAM policy allows the API calls

## Key Policies

* Control access to KMS keys "similar" to S3 bucket policies
* Difference: you cannot control access without them
* Default KMS Key Policy:
  * Created if you don't provide a specific KMS key policy
  * Complete access to the key to the root user = entire AWS account
  * Gives access to the IAM policies to the KMS key
* Custom KMS Key Policy:
  * Define users, roles that can access the KMS key
  * Define who can administer the key
  * Useful for cross-account access to your KMS key
  