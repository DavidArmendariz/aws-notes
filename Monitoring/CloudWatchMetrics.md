# CloudWatch Metrics

* CloudWatch provides metrics for every service in AWS
* Metric is a variable to monitor (CPU Utilization, NetworkIn, ...)
* Metric belongs to namespaces
* Dimension in an attribute of a metric (instance id, environment, etc...)
* Up to 10 dimensions per metric
* Metrics have timestamps
* Can create CloudWatch dashboards of metrics

## EC2 Detailed monitoring

* EC2 instance metrics have metrics "every 5 minutes"
* With detailed monitoring (for a cost), you get data "every 1 minute"
* Use detailed monitoring if you want to more prompt scale ASG

> Note: EC2 Memory usage is by default not pushed (must be pushed from inside the instance as a custom metric)

## Custom Metrics

* Possibility to define and send your own custom metrics to CloudWatch
* Ability to use dimensions (attributes) to segment metrics
  * instance.id
  * environment.name
* Metric resolution:
  * Standard: 1 minute
  * High Resolution: up to 1 second (**StorageResolution** API parameter) - higher cost
* Use API call **PutMetricData**
* Use exponential back off in case of throttle errors
