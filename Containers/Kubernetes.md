# Kubernetes

**Kubernetes (K8s)** lets us run containers in a reliable and scalable way, while making efficient use of resources. It also lets us expose our containerized application to the outside world.

A **cluster** in Kubernetes is a highly available cluster of compute resources which are organized to work as one unit.

The **control plane** manages the cluster, scheduling, applications, scaling, and deploying.

**Nodes** are a VM or physical server which function as a worker in the cluster.

A **kubelet** is an agent that can can be used to interact with the cluster control plane.

The **Kubernetes API** is what the kubelet agent uses to communicate with the control plane.

**Pods** are the smallest units of computing in Kubernetes. Pods are nonpermanent, and it’s common to see a ‘one-container-one-pod’ architecture when working with Kubernetes.
