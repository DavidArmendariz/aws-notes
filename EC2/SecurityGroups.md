# Security groups

* They are the fundamental of network security in AWS
* They control how traffic is allowed into or out of EC2 instances
* They only contain **allow** rules
* Security group rules can reference by IP or by security group (security groups can reference each other)
* They act as a "firewall" on EC2 instances
* They regulate:
  * Access to ports
  * Authorised IP ranges - IPv4 and IPv6
  * Control of inbound network
  * Control of outbound network

## Things to take into consideration

* Security groups can be attached to multiple instances
* They are locked down to a region / VPC combination
* Security groups are separate from EC2. If traffic is blocked, the EC2 instance won't even see it
* All inbound traffic is **blocked** by default
* All outbound traffic is **authorised** by default

## Common ports

* 22 = SSH
* 21 = FTP
* 22 = SFTP
* 80 = HTTP
* 443 = HTTPS
* 3389 = RDP (Remote Desktop Protocol, to log into a Windows instance)
