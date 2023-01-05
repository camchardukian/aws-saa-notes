# Bootstrapping with User Data

When we launch an EC2 container instance, we have the option of passing user data to the instance.

This data can be used to perform common automated configuration tasks, and/or to run scripts when the instance boots.

When using Amazon ECS, the most common use cases for passing user data are to pass configuration information to the Docker daemon and the Amazon ECS container agent.

The User Data we pass in can be accessed via the meta-data IP (http://169.254.169.254/latest/user-data).

Anything in User Data is executed by the instance OS, however, it’s ONLY executed on the initial launch of the instance.

User Data is not very secure. We should try to avoid using it to pass passwords or other long-term credentials.

User data is limited to 16 KB in size. It can be modified when the instance is stopped, but again, it’s only executed on the initial launch.

We can reduce Boot-Time-To-Service-Time via a combination of AMI Baking, and Bootstrapping.
