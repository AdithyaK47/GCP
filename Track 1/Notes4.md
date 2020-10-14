# Deployment

Kubernetes Deployment objects and their use in Google Kubernetes Engine (GKE)

Deployments represent a set of multiple, identical Pods with no unique identities. 
A Deployment runs multiple replicas of your application and automatically replaces any instances that fail or become unresponsive.
In this way, Deployments help ensure that one or more instances of your application are available to serve user requests. 
Deployments are managed by the Kubernetes Deployment controller.

Pods are the smallest, most basic deployable objects in Kubernetes. A Pod represents a single instance of a running process in your cluster.
Pods contain one or more containers.
A Pod is meant to run a single instance of your application on your cluster. 
They are not designed to run forever, and when a Pod is terminated it cannot be brought back. 
In general, Pods do not disappear until they are deleted by a user or by a controller.
When a Pod starts running, it requests an amount of CPU and memory. This helps Kubernetes schedule the Pod onto an appropriate node to run the workload.

Deployments use a Pod template, which contains a specification for its Pods
You can update a Deployment by making changes to the Deployment's Pod template specification

Deployment Manager

You can use Google Cloud Deployment Manager to create a set of Google Cloud resources and manage them as a unit, called a deployment.

Managing resources, Automation, 
