# Glacier Vault Lock

* Adopt a WORM (Write Once Read Many) model
* Lock the policy for future edits (can no longer be changed)
* Helpful for compliance and data retention

## S3 Object Lock (versioning must be enabled)

* Adopt a WORM model
* Block an object version deletion for a specified amount of time
* Object retention:
  * Retention period: specifies a fixed period
  * Legal hold: same protection, no expiry date
* Modes:
  * Governance mode: users can't overwrite or delete an object version or alter its lock settings unless they have special permissions
  * Compliance mode: a protected object version can't be overwritten or deleted by any user, including the root user in your AWS account. When an object is locked in compliance mode, its retention mode can't be changed, and its retention period can't be shortened
  