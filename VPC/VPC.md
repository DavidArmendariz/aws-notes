# VPC in AWS - IPv4

* You can have multiple VPCs in a region (max 5 per region - soft limit)
* Max CIDR per VPC is 5. For each CIDR:
  * Min size is /28 = 16 IP addresses
  * Max size is /16 = 65536
* Only the private IP ranges are allowed:
  * 10.0.0.0 - 10.255.255.255 (10.0.0.0/8)
  * 172.16.0.0 - 172.31.255.255 (172.16.0.0/12)
  * 192.168.0.0 - 192.168.255.255 (192.168.0.0/16)
* Your VPC CIDR should not overlap with your other networks
