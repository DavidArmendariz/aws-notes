# DynamoDB

* AWS proprietary technology, managed NoSQL database
* Serverless, provisioned capacity, auto scaling, on demand capacity
* Can replace ElastiCache as a key/value store (storing session data for example)
* HA, Multi AZ by default, Read and Writes are decoupled, DAX for read cache
* Reads can be eventually consisten or strongly consistent
* Security, authentication and authorization with AWS Labmda
* Backup/Restore feature, Global Table feature
* Monitoring through CloudWatch
* Can only query on primary key, sort key, or indexes
