# Encryption for objects

* Four methods:
  * SSE-S3: encrypts S3 objects using keys handled and managed by AWS
  * SSE-KMS: leverage AWS KMS to manage encryption keys
  * SSE-C: when you want to manage your own encryption keys
  * Client Side Encryption

## SSE-S3

* Uses keys handled and managed by Amazon S3
* Object is encrypted server side
* AES-256 encryption type
* Must set header: `"x-amz-server-side-encryption": "AES256"`

## SSE-KMS

* KMS advantages: user control + audit trail
* Object is encrypted server side
* Must set header: `"x-amz-server-side-encryption": "aws:kms"`

## SSE-C

* server side encryption using data keys fully managed by the customer outside of AWS
* Amazon S3 does not store the encryption key you provide
* HTTPS must be used
* Encrpytion key must be provided in HTTP headers for every request

## Client Side Encryption

* Clients library such as Amazon S3 Encryption Client
* Clients must encrypt data themselves before sending to S3
* Clients must decrypt data themselves when retrieving from S3
* Customer fully manages the keys and encryption cycle

## Encryption in transit (SSL/TLS)

* Amazon S3 exposes:
  * HTTP endpoint (non encrypted)
  * HTTPS endpoint (encryption in flight)
* Most clients would use the HTTPS endpoint by default
* HTTPS is mandatory for SSE-C
