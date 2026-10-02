# Course 10: Introduction to Containers w/ Docker, Kubernetes & OpenShift

## Module 2: Kubernetes Basics

### Key Concepts
- Container orchestration automates container lifecycle for faster, error-reduced deployments.
- Kubernetes is an open-source, portable, scalable container orchestration system.
- Kubernetes architecture includes control plane (controllers, API server, scheduler, etcd) and worker plane (nodes, kubelet, container runtime, kube-proxy).
- Kubernetes objects: Namespaces, Pods, ReplicaSets, Deployments, Services.
- Services types: ClusterIP, NodePort, External Load Balancer, External Name.
- Advanced Kubernetes objects: Ingress, DaemonSet, StatefulSet, Job.
- Kubernetes capabilities: automated rollouts/rollbacks, storage orchestration, scaling, self-healing, service discovery, load balancing.

### Notes
Container orchestration automates the lifecycle of containers, enabling faster deployments, fewer errors, higher availability, and improved security. Kubernetes is a widely used open-source system that manages containerized applications across clusters of machines. Its architecture is divided into a control plane, which manages the cluster state and scheduling, and worker planes, which run the containerized applications. Key Kubernetes objects include Namespaces for resource isolation, Pods as the smallest deployable units, ReplicaSets for scaling Pods, and Deployments for managing updates. Services provide stable networking and access policies to Pods, with different types supporting internal and external access. Additional objects like Ingress manage external access routing, DaemonSets ensure Pods run on all nodes, StatefulSets handle stateful applications with persistent storage, and Jobs manage batch tasks. Kubernetes offers features such as automated rollouts, scaling, secret management, and self-healing to maintain application reliability and efficiency.

### Code Examples
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: example-deployment
spec:
  replicas: 3
  selector:
    matchLabels:
      app: example
  template:
    metadata:
      labels:
        app: example
    spec:
      containers:
      - name: example-container
        image: example-image:latest
        ports:
        - containerPort: 80
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| Namespace | Isolates groups of resources within a cluster |
| Pod | Smallest deployable unit, represents an app instance |
| ReplicaSet | Manages scaling of Pods |
| Deployment | Manages updates and rollbacks of Pods and ReplicaSets |
| Service (ClusterIP) | Provides internal access to Pods |
| Service (NodePort) | Exposes service on each node's IP at a static port |
| Service (ELB) | External Load Balancer, exposes service externally |
| Ingress | Manages external access routing to multiple services |
| DaemonSet | Ensures a Pod runs on all nodes |
| StatefulSet | Manages stateful applications with persistent storage |
| Job | Runs batch tasks and tracks completion |

### Glossary
- **Container orchestration**: Automation of container lifecycle management.
- **Kubernetes control plane**: Components that manage the cluster state and scheduling.
- **Pod**: The smallest unit in Kubernetes representing a running process.
- **ReplicaSet**: Ensures a specified number of pod replicas are running.
- **Deployment**: Provides declarative updates for Pods and ReplicaSets.
- **Service**: Defines networking policies to access Pods.
- **Ingress**: API object managing external user access to services.
- **DaemonSet**: Ensures a copy of a Pod runs on all or selected nodes.
- **StatefulSet**: Manages deployment and scaling of stateful applications.
- **Job**: Creates Pods to run batch processes until completion.

### Summary
This module covers Kubernetes fundamentals, including its architecture, key objects, and capabilities. Understanding these concepts enables efficient management of containerized applications with automated deployment, scaling, and maintenance features.