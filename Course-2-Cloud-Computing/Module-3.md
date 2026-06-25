# Course 2 - Module 3 - Components of Cloud Computing

## Glossary

- **ACL**: Access Control Lists  
- **AZ (Availability Zones)**: Distinct Data Centers with their own power, cooling, and networking resources. These Zones can have names like DAL-09 or us-east-1.  
- **Bare-metal hypervisor**: Installed directly on top of the physical server. They're more secure, have lower latency, and are usually the ones you see in the market the most.  
- **Block storage**: Presented to compute nodes using high-speed fiber connections, which means that read and write speeds are typically much faster and reliable than with file storage.  
- **CDNs (Content Delivery Networks)**: A distributed server network that delivers temporarily stored, or cached, copies of website content to users based on the user’s geographic location.  
- **Cloud Region**: A geographic area or location where a Cloud provider’s infrastructure is clustered, and may have names like NA South or US East.  
- **Containers**: An executable unit of software in which application code is packaged, along with its libraries and dependencies, in common ways so that it can be run anywhere, whether it be on desktop, traditional IT, or the cloud.  
- **Data center**: A huge room or a warehouse containing cloud infrastructure.  
- **Dedicated hosts**: Offer single-tenant isolation.  
- **Direct Attached storage (Local storage)**: Storage which is presented directly to a cloud-based server and is effectively either within the host server chassis or within the same rack.  
- **File storage**: Typically presented to compute nodes as ‘NFS Storage’. NFS stands for Network File System and means that the storage is connected to compute nodes over a standard ethernet network.  
- **Hosted hypervisor**: There's a layer of host OS between the physical server and the hypervisor. These hypervisors are less frequently used and mostly used for “end-user” virtualization.  
- **HPC (High-performance computing)**  
- **Hypervisor**: A piece of software that runs above the physical server or host.  
- **IOPS (Input/Output Operations Per Second)**: Refers to the speed at which the disks can write and read data.  
- **NFS (Network File Storage)**  
- **Object storage**: Storage not attached to a compute node, rather it is accessed via an API.  
- **Reserved virtual server Instances**: Allow you to reserve capacity and guarantee resources for future deployments.  
- **SDN (Software Defined Networking)**  
- **Shared or Public Cloud VMs**: Provider-managed, multi-tenant deployments that can be provisioned on-demand with predefined sizes.  
- **Transient or Spot VMs**: Take advantage of unused capacity in a cloud data center.  
- **Virtualization**: Process of creating a software-based or virtual version of something whether that be compute, storage, networking, servers, or applications.  
- **VLANs (Virtual Local Area Networks)**  
- **VM (Virtual machines)**: Software-based computers, based on virtualization technologies.  
- **VPC (Virtual Private Cloud)**  
- **VPN (Virtual Private Networks)**

## Key Concepts
- Data centers house cloud infrastructure — Availability Zones are isolated data centers
  with independent power, cooling and networking
- Cloud Regions = geographic clusters of data centers (e.g. US East, EU West)
- Virtualization = abstracting physical hardware into software-based resources
- VM (Virtual Machine) = software-based computer running on physical hardware via a hypervisor
- Hypervisor types: bare-metal (direct on hardware) vs hosted (runs on top of an OS)
- Containers = lightweight packages of app code + dependencies — run consistently anywhere
- Block storage = high speed, low latency, connected via fiber — best for databases
- File storage = uses NFS over Ethernet — shared access across multiple compute nodes
- Object storage = accessed via API, not directly attached — best for large unstructured data
- VPC = isolated private network within a public cloud
- VLAN = virtual local area network — segments network traffic
- ACL = Access Control List — manages who can access what
- CDN = caches content geographically closer to users for faster delivery

## Quiz Result
9/10 ✅

## Summary
Cloud infrastructure runs on data centers organized into Availability Zones and Regions.
Virtualization enables VMs and containers to run on shared physical hardware efficiently.
Storage comes in three types — block (fast), file (shared), and object (API-based) — each
suited for different use cases. Networking is secured and isolated using VPCs, VLANs,
and ACLs, while CDNs improve performance by serving content closer to users.