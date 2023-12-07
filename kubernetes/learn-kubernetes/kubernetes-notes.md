### Details of the Kubernetes Resources (or) Objects.

* Name Space: A Name space is a logical seperation of resources in a kubernetes cluster.
* Side Car: Another container in same pod for different purpose like log aggregation (ELK) is called a side car. In a single pod, if there are multiple containers, all of them use same IP-Address.
* Kubernetes Service, There are three types.
  1. ClusterIP
  2. Node Port
  3. Load balancer

* ClusterIP is internal to Kubernetes Cluster.
* Node Port is to connect the pod from outside/internet. you can expose the port of the node. container port is attached to node port.
* Through node port, we can access the pod from all nodes in that kubernetes kluster.
* Load Balancer will work with public cloud environments.