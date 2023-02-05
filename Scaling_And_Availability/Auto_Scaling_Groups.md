# Auto Scaling Groups (ASGs)

ASGs can be used to perform automatic scaling and self-healing for EC2. They use launch templates or launch configurations.

ASGs have a minimum, desired, and maximum size.

The ASG works to keep running instances at the desired capacity by provisioning or terminating instances.

ASGs can optionally be assigned Scaling Policies. Scaling Policies ae used to adjust the desired size.

Auto Scaling Groups can be configured in a number of ways such as whether or not to:

- Suspend/resume the ASG’s launch/terminate processes.
- Add the ASG to a Load Balancer on launch.
- Accept notifications from Cloud Watch.
- Balance instances evenly across all Availability Zones.
- Perform instance health checks.
- Terminate and replace unhealthy instances.
- Schedule when the ASG should be running.
