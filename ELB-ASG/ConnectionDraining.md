# Connection Draining

* CLB: Connection Draining
* Target Group: Deregistration Delay (for ALB and NLB)
* It is time to complete in-flight requests while the instance is de-registering or unhealthy
* Stops sending new requests to the instance which is de-registering
* Between 1 to 3600 seconds. Default is 300 seconds.
* It can be disabled if you set it to 0
* Set to a low value if your requests are short
