# Scaling Policies

* **Target Tracking Scaling**
  * Most simple and easy to set-up
  * Metrics:
    * Average CPU utilization
    * Average network in (bytes)
    * Average network out (bytes)
    * Application Load Balancer request count per target
* **Simple / Step Scaling**
  * When a CloudWatch alarm is triggered (e.g. CPU > 70%), then add 2 units
  * When a CloudWatch alarm is triggered (e.g. CPU < 30%), then remove 1 unit
* **Scheduled Actions**
  * Anticipate a scaling based on known usage patterns
  * Example: increase the min. capacity to 10 at 5 pm on Fridays

## Scaling Cooldowns

* The cooldown period helps to ensure that your ASG does not launch or terminate additional instances before the previous scaling activity takes effect
* In addition to default cooldown for ASG, we can create cooldowns that apply to a specific **simple scaling policy**
* A scaling-specific cooldown period overrides the default cooldown period
* One common use for scaling-specific cooldowns is with a scale-in policy; a policy that terminates instances
based on a specific riteria or metric. Because this policy terminates instances, Amazon EC2 Auto Scaling needs less time to determine wether to terminate additional instances
* If the default cooldown period of 300 seconds is too long, you can reduce costs by applying a scaling-specific cooldown period
of 180 seconds to the scale-in policy
* If your application is scaling up and down multiple times each hour, modify the ASG cool-down timers and
the CloudWatch Alarm Period that triggers the scale-in

![ScalingCooldowns](images/ScalingCooldowns.png)
