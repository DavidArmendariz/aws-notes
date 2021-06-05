# CIDR

* CIDR are used for Security Groups rules, or AWS networking in general
* They help to define an IP address range
  * We have seen ww.xx.yy.zz/32 == 1 IP
  * We have seen 0.0.0.0/0 == all IPs
  * But we can define for example: 192.168.0.0/26: 192.168.0.0 - 192.168.0.63 (64IP)

## Understanding CIDR

* A CIDR has two components
  * The base IP (XX.XX.XX.XX)
  * The subnet mask (/26)
* The base IP represents an IP contained in the range
* The subnet masks defines how many bits can change in the IP
* The subnet mask can take two forms. Examples:
  * 255.255.255.0 (less common)
  * /24 (more common)

## Understanding CIDRs Subnet Masks

* The subnet masks basically allows part of the underlying IP to get additional next values from the base IP
* /32 allows for 1 IP = 2^0
* /31 allows for 2 IP = 2^1
* /30 allows for 4 IP = 2^2
* /29 allows for 8 IP = 2^3
* and so on...

## Quick memo

* /32 = no IP number can change
* /24 = last IP number can change
* /16 = last IP two numbers can change
* /8 = last IP three numbers can change
* /0 = all IP numbers can change

## Example

* 192.168.0.0/24 = 192.168.0.0 - 192.168.0.255 (256 IP)
* 192.168.0.0/16 = 192.168.0.0 - 192.168.255.255 (65536 IP)
* 134.56.78.123/32 = only 134.56.78.123/32
* 0.0.0.0/0 = all IPs

## Private vs Public IP allowed ranges

* The Internet Assigned Numbers Authority (IANA) established certain blocks of IPv4 addresses for the use of private (LAN) and public (Internet) addresses
* Private IP can only allow certain values
  * 10.0.0.0 - 10.255.255.255 (10.0.0.0/8) (in big networks)
  * 172.16.0.0 - 172.31.255.255 (172.16.0.0/12) (default AWS one)
  * 192.168.0.0 - 192.168.255.255 (192.168.0.0/16) (home networks)
* All the rest of the IP on the internet are public IP
