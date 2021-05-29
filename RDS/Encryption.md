# Encryption

* At rest encryption
  * Possibility to encrypt the master and read replicas with AWS KMS - AES - 256 encryption
  * Encryption has to be defined at launch time
  * If the master is not encrypted, the read replicas cannot be encrypted
  * Transparent Data Encryption (TDE) available for Oracle and SQL Server
* In-flight encryption
  * SSL certificates to encrypt data to RDS in flight
  * Provide SSL options with trust certificate when connecting to database

## Encryption operations

* Encrypting RDS backups
  * Snapshots of un-encrypted RDS databases are un-encrypted
  * Snapshots of encrypted RDS databases are encrypted
  * Can copy a snapshot into an encrypted one
* To encrypt an un-encrypted RDS database
  * Create a snapshot of the un-encrypted database
  * Copy the snapshot and enable encryption for the snapshot
  * Restore the database from the encrypted snapshot

## Network and IAM

* Network Security
  * RDS databases are usually deployed within a private subnet, not a public one
  * RDS security works by leveraging security groups
* Access Management
  * IAM policies help control who can manage AWS RDS
  * Traditional Username and Password can be used to login into the database
  * IAM based authentication can be used to login into RDS MySQL and PostgreSQL

## IAM Authentication

* You don't need a password, just an authentication token obtained through IAM and RDS API calls
* Auth token has a lifetime of 15 minutes
