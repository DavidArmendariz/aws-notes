# Volume types

There are 6 volume types

* gp2 / gp3 (SSD): General purpose SSD volume that balances price and performance for a wide variety of workloads. IO increases if the disk size increases. There is also a max of 16000 IOPS or equivalently 5334 GB.
* io1 / io2 (SSD): Highest performance SSD volume for mission critical low latency or high throughput workloads. Can increase IO independently. It has a max of 64000 IOPS.
* st 1 (HDD): low cost HDD volume designed for frequently accessed, throughtput-intensive workloads
* sc 1 (HDD): lowest cost HDD volume designed for less frequently accessed workloads
* EBS volumes are characterized in size, throughput, iops
* Only gp2 / gp3 and io1 / io2 can be used as boot volumes
