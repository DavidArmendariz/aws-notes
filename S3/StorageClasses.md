# Storage Classes

* Amazon S3 Standard - General Purpose
* Amazon S3 Standard-Infrequent Access (IA)
* Amazon S3 One Zone-Infrequent Access
* Amazon S3 Intelligent Tiering
* Amazon Glacier
* Amazon Glacier Deep Archive

## Standard - General Purpose

* High durability of objects across multiple AZ
* 99.99% Availability over a given year
* Sustain 2 concurrent facility failures

## Infrequent Access

* Suitable for data that is less frequently accessed, but requires rapid access when needed
* High durability of objects across multiple AZ
* 99.9% Availability
* Low cost compared to Amazon S3 Standard
* Sustain 2 concurrent facility failures

## One Zone - Infrequent Access

* Same as IA but data is stored in a single AZ
* High durability of objects in a single AZ; data lost when AZ is destroyed
* 99.5% Availability
* Low latency and high throughput performance
* Supports SSL for data at transit and encryption at rest
* Low cost compared to IA (by 20%)

## Intelligent Tiering

* Same low latency and high throughput performance of S3 standard
* Small monthly monitoring and auto-tiering fee
* Automatically moves objects between two access tiers based on changing access patterns
* Designed for durability of objects across multiple Availability Zones
* Resilient against events that impact an entire AZ
* 99.9% Availability

## Glacier

* Low cost object storage meant for archiving/backup
* Data is retained for the longer term
* Alternative to on-premise magnetic tape storage
* Each item in Glacier is called "Archive" (up to 40TB)
* Archives are stored in "Vaults"

## Glacier and Glacier Deep Archive

* Glacier - 3 retrieval options:
  * Expedited (1 to 5 minutes)
  * Standard (3 to 5 hours)
  * Bulk (5 to 12 hours)
  * Minimum storage duration of 90 days
* Glacier Deep Archive:
  * Standard (12 hours)
  * Bulk (48 hours)
  * Minimum storage duration of 180 days
