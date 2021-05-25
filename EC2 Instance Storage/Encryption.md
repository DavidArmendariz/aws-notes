# EBS Encryption

* When you create an encrypted EBS volume:
  * Data at rest is encrypted inside the volume
  * All the data in flight moving between the instance and the volume is encrypted
  * All snapshots are encrypted
  * All volumes created from the snapshot are encrypted
* Encryption and decryption are handled transparently
* Encryption has a minimal impact on latency
* EBS encryption leverages keys from KMS (AES-256)
* Copying an unencrypted snapshot allows encryption
* Snapshots of encrypted volumes are encrypted

## Encrypt and unencrypt EBS Volume

* Create an EBS snapshot of the volume
* Encrypt the EBS snapshot (using copy)
* Create a new EBS volume from the snapshot
* Now you can attach the encrypted volume to the original instance
