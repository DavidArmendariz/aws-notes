# Transferring large amount of data into AWS

* Example: transfer 200TB of data in the cloud. We have a 100 Mbps internet connection
* Over the internet/Site-to-Site VPN:
  * Immediate to setup
  * Will 185 days
* Over direct connect 1Gbps:
  * Long for the one-time setup (over a month)
  * Will take 18.5 days
* Over Snowball:
  * Will take 2 to 3 snowballs in parallel
  * Takes about 1 week for the end-to-end transfer
  * Can be combined with DMS
* For on-going replication/transfers: Site-to-Site VPN or DX with DMS or DataSync
