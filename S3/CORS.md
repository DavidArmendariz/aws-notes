# CORS

* An **origin** is a scheme (protocol), host (domain) and port.
* Web Browser based mechanism to allow requests to other origins while visiting the main origin
* The requests won't be fulfilled unless the other origin allows for the requests, using CORS Headers (e.g. `Access-Control-Allow-Origin`)

## S3 CORS

* If a client does a cross-origin request on our S3 bucket, we need to enable the correct CORS headers
