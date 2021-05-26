# SSL / TLS

* AN SSL Certificate allows traffic between your clients and your load balancer to be encrypted in transit
* SSL is used to encrypt connections
* TLS is a newer version of SSL
* TLS certificates are mainly use, but people still refer as SSL
* Public SSL certificates are issued by Certificate Authorities (CA)
* Load balancers use an X.509 certificate (SSL/TLS server certificate)
* You can manage certificates using ACM (AWS Certificate Manager)
* HTTPS listener:
  * You must specify a default certificate
  * You can add an optional list of certs to support multiple domains
  * Clients can use **SNI** (Server Name Indication) to specify the hostname they reach

## Server Name Indication (SNI)

* SNI solves the problem of loading multiple SSL certificates onto one web server (to serve multiple websites)
* It is a newer protocol and requires the client to indicate the hostname of the target server in the initial SSL handshake
* The server will then find the correct certificate or return the default one
* Only works for ALB, NLB, CloudFront

## SSL Certificates

* Classic Load Balancer
  * Support only one SSL Certificate
  * Must use multiple CLB for multiple hostname with multiple SSL certificates
* Application Load Balancer
  * Supports multiple listeners with multiple SSL certificates
  * Uses SNI to make it work
* Network Load Balancer
  * Supports multiple listeners with multiple SSL certificates
  * Uses SNI to make it work
