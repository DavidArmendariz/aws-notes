# Instance Store

* EBS volumes are network drives with good but limited performance
* If you need a high-performance hardware disk, use EC2 instance store
* Better I/O performance
* EC2 instance store lose their storage if they are stopped (ephemeral)
* Good for buffer, cache, scratch data, temporary content
* Risk of data loss if hardware fails
* Backups and replication are your responsibility
