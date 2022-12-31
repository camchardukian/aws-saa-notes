# Elastic Container Service (ECS)

**Amazon ECS** is a fully managed container orchestration service that makes it easy for us to deploy, manage, and scale containerized applications.

It is deeply integrated with the rest of the AWS platform to provide a secure and easy-to-use solution for running container workloads in the cloud (as well as on our own infrastructure now with the release of Amazon ECS Anywhere).

**Container definitions** are used inside of task definitions to describe the different containers that are launched as part of a task.

Container definitions define the image and ports that will be used for a container.

It basically points to an image inside of a container registry and it defines what ports are exposed from that container.

A **task definition** is required to run Docker containers in Amazon ECS. A few of the more important parameters we may specify inside of a task definition are:

- The Docker image to use with each container in our task
- How much CPU and memory to use with each task or each container within a task
- The IAM role that our tasks use (**Task Role**)
- The launch type to use, which determines the infrastructure that our tasks are hosted on

Inside of a task definition we can define multiple containers.

Our application may be on a single task definition, but in most cases an application will span multiple task definitions.

A **task** is the instantiation of a task definition within a cluster.

A **service definition** can be used to help with scaling and high availability because it allows us to choose how many copies of a task we would like to run.
