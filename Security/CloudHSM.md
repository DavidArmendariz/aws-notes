# CloudHSM

* KMS => AWS manages the software for encryption
* CloudHSM => AWS provisions encryption hardware
* Dedicated hardware (HSM)
* You manage your own encryption keys entirely
* HSM device is tamper resistant
* CloudHSM clusters are spread across Multi AZ
* Supports both symmetric and asymmetric encryption (SSL/TLS Keys)
* Must use the CloudHSM Client Software
* Redshift supports CloudHSM for database encryption and key management
* Good option to use with SSE-C encryption
