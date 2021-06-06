# IPv6 in VPC

* IPv4 cannot be disabled for your VPC and subnets
* You can enable IPv6 (they are public IP addresses)
* Your EC2 Instances would get at least a private internal IPv4 and a public IPv6

## IPv6 Troubleshooting

* IPv4 cannot be disabled for your VPC and subnets
* So if you cannot launch an instance in your subnet
  * It's not because it cannot acquire an IPv6
  * It's because there are no available IPv4 in your subnet
* Solution: create a new IPv4 CIDR in your subnet
