# Health Checks

* Have X health checks failed means unhealthy (here, X defaults to 3)
* Default Health Check Interval: 30s (can be set to 10s at a higher cost)
* Abouth 15 health checkers will check the endpoint health
* Can have HTTP, TCP and HTTPS health checks (no SSL verification)
* Possibility of integrating the health check with CloudWatch
* Health checks can be linked to Route53 DNS queries
