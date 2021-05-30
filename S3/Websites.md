# Websites

* S3 can host static websites and have them accessible on the www
* The website URL will be either of these ones:
  * `<bucket-name>.s3-website-<AWS-region>.amazonaws.com`
  * `<bucket-name>.s3-website.<AWS-region>.amazonaws.com`
* If you get 403 (Forbidden) error, make sure the bucket policy allows public reads
