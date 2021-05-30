# Versioning

* You can version your files in Amazon S3
* It is enabled at the bucket level
* Same key overwrite will increment the "version": 1, 2, 3
  * Protect against unintended deletes
  * Easy rollback to previous version

## Notes

* Any file that is not versioned prior to enabling versioning will have version "null"
* Suspending versioning does not delete the previous versions
