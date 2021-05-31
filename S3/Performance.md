# Performance

* S3 automatically scales to high requests rates, latency 100-200 ms
* Your application can achieve at least 3500 PUT/COPY/POST/DELETE and 5500 GET/HEAD requests per second per prefix in a bucket
* There are no limits to the number of prefixes in a bucket

## KMS Limitation

* If you use SSE-KMS you may be impacted by the KMS limits
* When you upload, it calls the **GenerateDataKey** KMS API
* When you download it, calls the **Decrypt** KMS API
* Count towards the KMS quota per second

## Optimizations

* Multi-Part upload:
  * recommended for files > 100MB, must use for files > 5GB
  * can help parallelize uploads (speed up transfers)
* S3 Transfer Acceleration
  * Increase transfer speed by transferring file to an AWS edge location which will forward the data to the S3 bucket in the target region
  * Compatible with multi-part upload

## Byte-Range Fetches

* Parallelize GETs by requesting specific byte ranges
* Better resilience in case of failures
* Can be used to speed up downloads
* Can be used to retrieve only partial data (For example the head of a file)
