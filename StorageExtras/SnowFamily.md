# AWS Snow Family

* Highly secure, portable devices to collect and process data at the edge, and migrate data into and out of AWS
* AWS Snow Family: offline devices to perform data migrations
* If it takes more than a week to transfer over the network, use Snowball devices!

## Snowball Edge (for data transfers)

* Physical data transpor: move TBs or PBs of data in or out of AWS
* Alternative to moving data over the network
* Pay per data transfer job
* Provide block storage and Amazon S3-compatible object storage
* Snowball Edge Storage Optimized
  * 80TB of HDD capacity for block volume and S3 compatible object storage
* Snowball Edge Compute Optimized
  * 42TB of HDD capacity for block volume and S3 compatible object storage
* Use cases: large data cloud migrations, DC decommision, disaster recovery

## AWS Snowcone

* Small portable computing anywhere, rugged and secure, ,withstands harsh environments
* Light (4.5 pounds, 2.1 kg)
* Device used for edge computing, storage, and data transfer
* 8TBs of usable storage
* Use Snowcone where Snowball does not fit
* Must provide your own battery/cables
* Can be sent back AWS offline, or connect it to internet and use AWS DataSync to send data

## AWS Snowmobile

* Transfer exabytes of data
* Each Snowmobile has 100PB of capacity (use multiple in parallel)
* High security: temperature controlled, GPS, 24/7 video surveillance

## What is Edge Computing?

* Process data while it is being created on an edge location
  * A truck on the road, a ship on the sea, a mining station underground
* These locations may have
  * Limited/no internet access
  * Limited/no easy access to computing power
* We setup a Snowball Edge/Snowcone device to do edge computing
* Eventually we can ship back the device to AWS

## AWS OpsHub

* Historically, to use Snow Family devices you needed a CLI
* Today, you can use AWS OpsHub to manage your Snow Family Device
