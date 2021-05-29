# Introduction

* Managed DB service for DB use SQL as a query language
* It allows you to create databases in the cloud that are managed by AWS
* Postgres, MySQL, MariaDB, Oracle, Microsoft SQL Server, Aurora

## Advantages

* RDS is a managed service
  * Automated provisioning, OS patching
  * Continuous backups and restore to specific timestamp
  * Monitoring dashboards
  * Read replicas for improved read performance
  * Multi AZ setup for disaster recovery
  * Maintenance windows for upgrades
  * Scaling capability
  * Storage backed by EBS
* We cannot SSH into instances

## RDS backups

* Automatically enabled
  * Daily full bakcup of the database
  * Transaction logs are backed up by RDS every 5 minutes
  * Ability to restore to any point in time
  * 7 days retention (can be increased to 35 days)
* Snapshots:
  * Manually triggered by the user
  * Retention of backup for as long as you want

## Storage Auto Scaling

* Helps you increase storage on your RDS DB instance dynamically
* When RDS detects you are running out of free databas storage, it scales automatically
* You have to set a **maximum storage threshold**
* Automatically modify storage if
  * Free storage is less than 10% of allocated storage
  * Low-storage lasts at least 5 minutes
  * 6 hours have passed since last modification
