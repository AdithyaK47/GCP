Main objectives: 

Create Kubernetes Engine cluster 

Deploy an app to the cluster 

Delete the cluster 
 

Google Kubernetes Engine (GKE) provides a managed environment for deploying, managing, and scaling your containerized applications using Google infrastructure. The Kubernetes Engine environment consists of multiple machines (specifically Compute Engine instances) grouped together to form a container cluster.  

Kubernetes Engine clusters are powered by the Kubernetes open source cluster management system. Kubernetes provides the mechanisms to interact with the container cluster. Kubernetes is used to provide commands and resources to deploy and manage applications, perform administration tasks and set policies, and monitor the health of deployed workloads. 

Some of the benefits: automatic management, monitoring and liveness probes for application containers, automatic scaling, rolling updates, etc. 

 

A cluster consists of at least one cluster master machine and multiple worker machines called nodes. Nodes are  VM instances that run the Kubernetes processes necessary to make them part of the cluster. 

 

Kubernetes Engine uses Kubernetes objects to create and manage cluster's resources. Kubernetes provides the deployment object for deploying stateless applications like web servers. Service objects define rules and load balancing for accessing application from the Internet. 

 

Commands to note: 

gcloud container clusters create [CLUSTER-NAME] 

gcloud container clusters get-credentials [CLUSTER-NAME]  

(Get authentication credentials for the cluster) 

kubectl create deployment [name]  --[container-image]  

kubectl expose deployment [name] --type=LoadBalancer --port 8080 (Creates a Kubernetes Service that exposes application to external traffic) 

(--port specifies the port that the container exposes. 

type="LoadBalancer" creates a Compute Engine load balancer for your container.) 

gcloud container clusters delete [CLUSTER-NAME] 
