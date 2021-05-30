# Introduction

* Amazon S3 allos people to store objects (files) in "buckets"
* Must have a globally unique name
* Buckets are defined at the region level
* Naming convention
  * No uppercase
  * No underscore
  * 3-63 characters long
  * Not an IP
  * Must start with lowercase letter or number
* Objects (files) have a key
* The key is the **FULL** path
  * s3://my-bucket/file.txt (the key is `file.txt`)
  * s3://my-bucket/my_folder1/another_folder/file.txt (the key is `my_folder1/another_folder/file.txt`)
* The key is composed of **prefix** and **object name**
  * s3://my-bucket/my_folder1/another_folder/file.txt (the prefix is `my_folder1/another_folder/` and the object name is `file.txt`)
* Max Object Size is 5TB
* Cannot upload more than 5GB at the same time. Use **multi-part upload**
* Metadata (list of text key/value pairs)
* Tags (useful for security/lifecycle)
* Version ID (if versioning is enable)
