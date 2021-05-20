# IPs

Networking has two sorts of IPs: IPv4 and IPv6

* IPv4: 198.168.10.1
* IPv6: 1234:1234:3:2000:f1f1:f2e1:221e

IPv4 is still the most used.

## Public IP

* It means the machine can be identified on the internet (WWW)
* Must be unique across the whole web
* Can be geo-located easily

## Private IP

* Private IP means the machine can only be identified on a private network
* The IP must be unique across the private network
* Two differente private networks can have the same IPs

## Elastic IPs

* When you stop and then start an EC2 instance, it can change its public IP
* If you need to have a fixed public IP for your instance, you need an elastic IP
* An Elastic IP is a public IPv4 IP you own as long as you don't delete it
* Can only be attached to one instance only
* With an Elastic IP, you can mask the failure of an instance or software by rapidly remapping
the address to another instance in your account (uncommon)
* You can only have 5 Elastic IPs in your account
* **TRY TO AVOID USING ELASTIC IPs**
