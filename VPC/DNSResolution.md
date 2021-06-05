# DNS Resolution in VPC

* `enableDnsSupport` (= DNS Resolution Setting)
  * Default true
  * Helps decide if DNS resolution is supported for the VPC
  * If true, queries the AWS DNS server at 169.254.169.253
* `enableDnsHostname` (= DNS Hostname Setting)
  * False by default for newly created VPC, true by default for default VPC
  * Won't do anything unless `enableDnsSupport` is true
  * If true, assign public hostname to EC2 instance if it has a public IP
* If you use custom DNS domain names in a private zone in Route 53, you must set both these attributes to true
