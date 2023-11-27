### Need of Kubernetes

1. In docker there is no dynamic scaling. When traffic is increasing, containers should be increased.
2. Docker containers run on a single host, Docker hosts are vulnerable, and we cannot shift containers to other hosts immediately.
3. Host networking in docker is vulnerable and complex to switch and maintain.
4. Storage in docker is dependent on Host storage, if host crashes, then we lose all data in the host.
5. Log management, docker maintains limited types of logs.

Therefore, to mitigate all these issues in docker, we need Kubernetes as we have most solutions in kubernetes.

### Kubernetes Topics:

Creating Kubernetes Cluster
Namespaces
Pods
Services
Sets
    Daemon sets
    Deployment sets
    Stateful sets
ConfigMaps
Secrets
Taint and Tolerations
Persistent Volumes and Claims
Ingress
Limit Resources
Health Checks
Side cars

### Practice project on Roboshop
### Kubernetes Architecture
    - etcd --> Storage
    - API Server
    - Controller
    - Client
### Monitoring Kubernetes Cluster
### Upgrading cluster
### Helm Charts