# Course 10: Introduction to Containers w/ Docker, Kubernetes & OpenShift

## Module 4: The Kubernetes Ecosystem: OpenShift, Istio, etc.

### Key Concepts
- OpenShift is an enterprise-ready Kubernetes container platform designed for open hybrid cloud environments.
- Custom Resource Definitions (CRDs) and custom controllers extend Kubernetes APIs to create new declarative APIs.
- Operators automate cluster tasks by using CRDs and custom controllers.
- Builds transform inputs into objects; ImageStreams abstract container image references in OpenShift.
- Service mesh provides traffic management, security, and observability between services.
- Istio is a service mesh that supports connection, security, enforcement, and observability, commonly used with microservices.

### Notes
OpenShift enhances Kubernetes by offering an easier-to-use platform with integrated Jenkins and additional services. It leverages CRDs and custom controllers to extend Kubernetes functionality, enabling automation through Operators. Builds in OpenShift convert source inputs into deployable objects, with ImageStreams managing container images. Service meshes like Istio manage service-to-service communication by controlling traffic flow, encrypting data, and providing metrics for monitoring service behavior, which is essential for microservices architectures.

### Code Examples
```yaml
# Example of a Custom Resource Definition (CRD) in Kubernetes
apiVersion: apiextensions.k8s.io/v1
kind: CustomResourceDefinition
metadata:
  name: examples.example.com
spec:
  group: example.com
  versions:
    - name: v1
      served: true
      storage: true
  scope: Namespaced
  names:
    plural: examples
    singular: example
    kind: Example
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| OpenShift | Enterprise Kubernetes platform for hybrid cloud |
| CRD (Custom Resource Definition) | Extends Kubernetes API with new resource types |
| Operator | Automates cluster tasks using CRDs and controllers |
| Build | Process that transforms inputs into deployable objects |
| ImageStream | Abstracts container image references in OpenShift |
| Service Mesh | Manages traffic, security, and observability between services |
| Istio | Service mesh providing connection, security, enforcement, and observability |

### Glossary
- **OpenShift**: A Kubernetes-based container platform designed for enterprise and hybrid cloud use.
- **Custom Resource Definition (CRD)**: A way to extend Kubernetes APIs with custom objects.
- **Operator**: A method to automate complex Kubernetes cluster tasks using CRDs and controllers.
- **Build**: The process of converting source code or other inputs into a container image or deployable object.
- **ImageStream**: An OpenShift abstraction to manage and reference container images.
- **Service Mesh**: Infrastructure layer that manages service-to-service communication, security, and monitoring.
- **Istio**: A popular service mesh implementation that supports microservices communication and observability.

### Summary
This module covers OpenShift as an enhanced Kubernetes platform with extended APIs through CRDs and automation via Operators. It explains the build process and image management in OpenShift and introduces service meshes like Istio, which provide essential traffic management, security, and observability features for microservices applications.