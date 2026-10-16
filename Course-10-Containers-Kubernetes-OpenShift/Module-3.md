# Course 10: Introduction to Containers w/ Docker, Kubernetes & OpenShift

## Module 3: Managing Applications with Kubernetes

### Key Concepts
- ReplicaSet enables scaling by creating or deleting pods.
- ReplicaSet maintains actual state to match desired state.
- Autoscaling adjusts resources at cluster, node, or pod level.
- Autoscaler types: Horizontal Pod Autoscaler (HPA), Vertical Pod Autoscaler (VPA), Cluster Autoscaler (CA).
- Rolling updates deploy app changes in a controlled, automated way.
- Rolling update and rollback strategies: all-at-once and one-at-a-time.
- ConfigMaps provide non-sensitive configuration variables.
- Secrets provide sensitive information securely.
- Service Binding manages configuration and credentials for backend services, protecting sensitive data.

### Notes
A ReplicaSet in Kubernetes ensures that a specified number of pod replicas are running at any time, scaling the number of pods up or down as needed to match the desired state. Autoscaling mechanisms help dynamically adjust resources based on demand, improving efficiency and performance. Rolling updates allow applications to be updated without downtime by gradually replacing pods with new versions, with options for rollback if issues arise. ConfigMaps and Secrets are Kubernetes objects used to inject configuration data and sensitive information into pods securely. Service Binding automates the management of credentials and configuration for external services, simplifying application integration while maintaining security.

### Code Examples
```yaml
apiVersion: apps/v1
kind: ReplicaSet
metadata:
  name: example-replicaset
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
        image: example-image
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| ReplicaSet | Maintains a stable set of pod replicas |
| HPA (Horizontal Pod Autoscaler) | Scales pods horizontally based on metrics |
| VPA (Vertical Pod Autoscaler) | Adjusts pod resource requests and limits vertically |
| Cluster Autoscaler (CA) | Scales cluster nodes based on pod demand |
| Rolling Update | Updates pods gradually without downtime |
| ConfigMap | Stores non-sensitive configuration data |
| Secret | Stores sensitive data securely |
| Service Binding | Manages credentials and config for external services |

### Glossary
- **ReplicaSet**: A Kubernetes controller that ensures a specified number of pod replicas are running.
- **Autoscaling**: Automatic adjustment of resources based on workload demand.
- **Rolling Update**: A deployment strategy that updates pods incrementally to avoid downtime.
- **ConfigMap**: Kubernetes object for storing non-sensitive configuration data.
- **Secret**: Kubernetes object for storing sensitive information securely.
- **Service Binding**: Mechanism to provide applications with credentials and configuration for external services.

### Summary
This module covers how Kubernetes manages application scaling and updates through ReplicaSets and autoscaling techniques. It also explains how to securely manage configuration and sensitive data using ConfigMaps, Secrets, and Service Binding, enabling smooth and secure application deployment and maintenance.