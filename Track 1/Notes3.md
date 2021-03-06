# Reliable task scheduling on Compute Engine with Cloud Scheduler

Cron is the standard tool for scheduling recurring tasks on Unix systems.
As the systems you build increase in complexity and become distributed, a single computer running cron can become a critical point of failure. 

Cloud Scheduler provides a fully managed, enterprise-grade service that lets user to schedule events.
After one have scheduled a job, Cloud Scheduler will call the configured event handlers, which can be App Engine services, HTTP endpoints, or Pub/Sub subscriptions.

To run tasks on the Compute Engine instance in response to Cloud Scheduler events, one need to relay the events to those instances. 
One way to do this is by calling an HTTP endpoint that runs on your Compute Engine instances.
Another option is to pass messages from Cloud Scheduler to the Compute Engine instances using Pub/Sub

# Serverless

What is serverless?

Serverless computing is a paradigm shift in application development that enables developers to focus on writing code without worrying about infrastructure. 
It offers a variety of benefits over traditional computing, including zero server management, no up-front provisioning, auto-scaling, and paying only for the resources used. 
These advantages make serverless ideal for use cases like stateless HTTP applications, web, mobile, IoT backends, batch and stream data processing, chatbots, and more.

Cloud Functions (SERVERLESS FUNCTIONS & EVENTS)                                                                                                             
App Engine standard environment (SERVERLESS HTTP APPLICATIONS)                                                                                                  
Cloud Run (SERVERLESS CONTAINERS)                                                                                                                               

Cloud Functions provides a connective layer of logic that lets you write code to connect and extend cloud services.                                    
Listen and respond to a file upload to Cloud Storage, a log change, or an incoming message on a Pub/Sub topic.                                            
Cloud Functions augments existing cloud services and allows to address an increasing number of use cases with arbitrary programming logic.                    

Cloud events are things that happen in cloud environment. These might be things like changes to data in a database,                                         
files added to a storage system, or a new virtual machine instance being created.                                           

Events occur whether or not one choose to respond to them. A trigger create a response to an event.
A trigger is a declaration that one is interested in a certain event or set of events. Binding a function to a trigger allows to capture and act on events.

# VPC

Virtual Private Cloud (VPC) provides networking functionality to Compute Engine virtual machine (VM) instances, 
Google Kubernetes Engine (GKE) clusters, and the App Engine flexible environment. 
VPC provides networking for the cloud-based resources and services that is global, scalable, and flexible.

VPC network can be imagined in the same way of a physical network, except that it is virtualized within Google Cloud. 
A VPC network is a global resource that consists of a list of regional virtual subnetworks (subnets) in data centers,                          
all connected by a global wide area network. VPC networks are logically isolated from each other in Google Cloud.                                    

Each VPC network implements a distributed virtual firewall that can be configured.                                                                      
Firewall rules allow to control which packets are allowed to travel to which destinations.                                                                            

Routes tell VM instances and the VPC network how to send traffic from an instance to a destination, either inside the network or outside of Google Cloud.          
While routes govern traffic leaving an instance, forwarding rules direct traffic to a Google Cloud resource in a VPC network based on IP address, protocol, and port.

Interfaces and IP addresses                                                                                                                               
Resources such as VM instances and load balancers have IP addresses in Google Cloud.                                                                    
These IP addresses enable Google Cloud resources to communicate with other resources in Google Cloud, in on-premises networks, or on the public internet.          

External IP addresses are publicly advertised. Resources with external IP addresses can communicate with the public internet.                                    
Internal IP addresses are not publicly advertised. They are used only within a network.                                                                             

One can add multiple network interfaces to a VM instance, where each interface resides in a unique VPC network.                                                            

VPC firewall rules let one to allow or deny connections to or from the virtual machine (VM) instances based on a configuration that one specify.                 
Enabled VPC firewall rules are always enforced, protecting the instances regardless of their configuration and operating system, even if they have not started up.    

https://cloud.google.com/vpc/docs/firewalls                                                                                                       
https://cloud.google.com/solutions/web-serving-overview

VPC sharing and peering                                                                                                                                   
 
Shared VPC                                                                                                                                                        
One can share a VPC network from one project (called a host project) to other projects in the Google Cloud organization.                                        
Also, one can grant access to entire Shared VPC networks or select subnets therein by using specific IAM permissions.                                   

VPC Network Peering                                                                                                                                          
VPC Network Peering allows to build (software as a service (SaaS)) ecosystems in Google Cloud,                                                                       
making services available privately across different VPC networks, whether the networks are in the same project,                                                       
different projects, or projects in different organizations.                                                                              
