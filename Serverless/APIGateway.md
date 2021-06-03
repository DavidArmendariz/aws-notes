# API Gateway

* AWS Lambda + API Gateway
* Support for the WebSocket Protocol
* Handle API versioning
* Handle different environments
* Handle security (authentication and authorization)
* Create API keys, handle request throttling
* Swagger/Open API import to quickly define APIs

## Integrations

* Lambda Function
  * Invoke Lambda Function
  * Easy way to expose REST API backed by AWS Lambda
* HTTP
  * Expose HTTP endpoints in the backend
  * Why? Add rate limiting, caching, user authentications, API keys
* AWS Service
  * Expose any AWS API through the API Gateway
  * Start an AWS Step Function workflow, post a message to SQS
  * Why? Add authentication, deploy publicly, rate control

## Endpoint Types

* Edge-Optimized (Default): for global clients
  * Requests are routed through the CloudFront Edge locations (improves latency)
  * The API Gateway still lives in only one region
* Regional:
  * For clients within the same region
  * Could manually combine with CloudFront
* Private:
  * Can only be accessed from your VPC using an interface VPC endpoint (ENI)
  * Use a resource policy to define access

## Security

* IAM Permissions
  * Create an IAM policy authorization and attach to user/role
  * API Gateway verifies IAM permissions passed by the calling application
  * Good to provide access within your own infrastructure
  * Leverages "Sig v4" capability where IAM credential are in headers
* Lambda Authorizer
  * Uses AWS Lambda to validate the token in header being passed
  * Option to cache result of authentication
  * Helps to use OAuth/SAML/3rd party type of authentication
  * Lambda must **return an IAM policy for the user**
* Cognito User Pools
  * Cognito fully manages user lifecycle
  * API gateway verifies identity automatically from AWS Cognito
  * No custom implementation required
  * Cognito only helps with authentication, not authorization
  