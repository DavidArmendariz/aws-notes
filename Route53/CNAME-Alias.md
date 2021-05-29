# CNAME vs Alias

* AWS resources (Load Balancer, CloudFront) expose an AWS hostname
* CNAME:
  * Points a hostname to any other hostname (app.mydomain.com => app.example.com)
  * **ONLY FOR NON ROOT DOMAIN**
* Alias:
  * Points a hostname to an AWS Resource (app.mydomain.com => something.amazonaws.com)
  * **Works for ROOT DOMAIN and NON ROOT DOMAIN**
  * Free
  * Native health check
  