# EBS Raid options

* EBS is already redundant storage (replicated within an AZ)
* But what if you want to increase IOPS?
* What if you want to mirror your EBS volumes?
* You would mount volumes in parallel in RAID settings
* RAID is possible as long as your OS supports it
* RAID options:
  * RAID 0
  * RAID 1
  * RAID 5 (not recommended)
  * RAID 6 (not recommended)

## RAID 0

* Increases performance

## RAID 1

* Increase fault tolerance
