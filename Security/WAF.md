# Web Application Firewall

* Protects your web applications from common web exploits (Layer 7)
* Layer 7 is HTTP (vs Layer 4 is TCP)
* Deploy on Application Load Balancer, API Gateway, CloudFront
* Define Web ACL (Web Access Control List)
  * Rules can include: IP addresses, HTTP Headers, HTTP body, or URI strings
  * Protects from common attack - SQL injection and Cross-Site Scripting (XSS)
  * Size constraints, geo-match (block countries)
  * Rate-based rules (to count occurrences of events) - for DDoS protection

## Firewall Manager

* Manager rules in all accounts of an AWS Organization
* Common set of security rules
* WAF rules
* AWS Shield Advanced
* Security Groups for EC2 and ENI resources in VPC
