# Kubernetes
Kubernetes is an open source container orchestration platform that automates many of the manual processes involved in deploying, 
managing, and scaling containerized applications. 
In other words, one can cluster together groups of hosts running Linux® containers, and Kubernetes helps to easily and efficiently manage those clusters. 


Uses 

1) Orchestrate containers across multiple hosts. 

2) Make better use of hardware to maximize resources needed to run enterprise apps. 

3) Control and automate application deployments and updates. 

4) Mount and add storage to run stateful apps.  

5) Scale containerized applications and their resources on the fly. 

6) Services which guarantees the deployed applications are always running the way one intended them to run. 

7) Health-check and self-heal apps with auto placement, auto restart, auto replication, and autoscaling. 

 
Key terms to note: 

1. Control plane: The collection of processes that control Kubernetes nodes. This is where all task assignments originate. 

2. Nodes: These machines perform the requested tasks assigned by the control plane. 

3. Pod: A group of one or more containers deployed to a single node. All containers in a pod share an IP address, IPC, hostname, and other resources. 
   Pods abstract network and storage from the underlying container. This lets you move containers around the cluster more easily. 

4. Replication controller:  This controls how many identical copies of a pod should be running somewhere on the cluster. 

5. Service: This decouples work definitions from the pods. Kubernetes service proxies automatically get service requests to the right pod—no matter where it moves in the cluster    or even if it’s been replaced. 

6. Kubelet: This service runs on nodes, reads the container manifests, and ensures the defined containers are started and running. 

7. kubectl: The command line configuration tool for Kubernetes. 

GKE, Google Kubernetes Engine is a managed environment for deploying, managing, scaling using google infrastructure. 
GKE contains multiple machines to form cluster. It also includes native integration with cloud monitoring and cloud logging. 


A cluster is the foundation of Google Kubernetes Engine (GKE), the Kubernetes objects that represent the containerized applications all run on top of a cluster. 
In GKE, a cluster consists of at least one control plane and multiple worker machines called nodes. 
These control plane and node machines run the Kubernetes cluster orchestration system. 

Control Plane: The control plane runs the control plane processes, including the Kubernetes API server, scheduler, and core resource controllers. 
The lifecycle of the control plane is managed by GKE when you create or delete a cluster. The control plane is the unified endpoint for a cluster. 
Responsible for what runs on all cluster’s nodes. 
The control plane and nodes also communicate using Kubernetes APIs. 

Gcr.io container registry contains container images for Kubernetes software running on control plane and nodes needed when a cluster is created/updated. 

https://cloud.google.com/kubernetes-engine/docs/concepts/cluster-architecture#nodes 


# Instance Groups

Instance groups is a collection of VM instances that one can manage as a single entity. 
Two kinds of VM instances are Managed Instance Groups (MIG) and Unmanaged Instance Groups. (UIG)
The first one is automated whereas the latter is where one manages the instance. 

# Auto-scaler, Auto-upgrade and Auto-repair

Auto scaling automatically add or remove VM instances from the group based on increase or decrease in the load.  
There are several autoscaling policies available; for example, the one based on CPU utilization, it watches avg. CPU utilization of VM instances. 

Cluster Autoscaler: When demand (Workload) is high, cluster autoscaler adds node to node pool, when it is low, it is scaled back to minimum size,
i.e. automatically resizes number of nodes in a given node pool. User have to specify minimum & maximum size for node pool. 

Node pool is a group of nodes within a cluster that have same configuration. 

Cluster autoscaler increases/decreases the size of the node pool automatically, based on the resource requests 
(rather than actual resource utilization) of Pods running on that node pool's nodes. It periodically checks the status of Pods and nodes, and takes action.  
 
If pods are unschedulable, it is because there are not enough nodes in node pool, and nodes are added up to maximum size of node pool.  
If pods are under-utilized, and all Pods could be scheduled even with fewer nodes in the node pool, Cluster autoscaler removes nodes, 
down to the minimum size of the node pool. 

When scaling down, cluster autoscaler respects scheduling and eviction rules set on Pods. These restrictions can prevent a node from being deleted by the autoscaler. 


Auto-upgrading nodes: Node auto-upgrades helps the nodes in the cluster to be updated with cluster control plane (master) version when it is updated. It provide several benefits such as lower management, ease of use, better security.  

Auto-repairing nodes: Node auto-repair feature helps to keep the nodes in the cluster in a healthy, running state. When enabled, GKE makes periodic checks on the health state of each node in the cluster. If a node fails consecutive health checks over an extended time period, GKE initiates a repair process for that node. 
If GKE detects that a node requires repair, the node is drained and re-created. GKE waits one hour for the drain to complete. If the drain doesn't complete, the node is shut down and a new node is created. If multiple nodes require repair, GKE might repair nodes in parallel. 

# Load Balancing 

GCP, the Google Cloud Platform provides Load Balancing to distribute incoming traffic across multiple VMs. Benefits of Load balancing are scaling the app, 
supporting heavy traffic, health checks, route traffic efficiently. 

To decide which load balancer best suits your implementation of Google Cloud, consider the following aspects of Cloud Load Balancing: 

1) Global versus regional load balancing 

2) External versus internal load balancing 

3) Traffic type 

Proxy based load balancer inherits DDOS protection from GFE. (Google Front-end)      

https://cloud.google.com/load-balancing/docs/choosing-load-balancer 
 
# Instance Templates

Instance templates are a resource to create a VM instance & MIG. It is a global resource, not bound to a region/zone.  
We can use it anytime when we want to create a VM instance quickly on the basis of pre-existing configuration. We cannot update an existing Instance template.   

# Health Checks

Google Cloud provides health checking mechanisms that determine whether backend instances respond properly to traffic. 

Health check v/s Legacy Health check 

https://cloud.google.com/load-balancing/docs/health-checks#health_check_categories_protocols_and_ports 

 
