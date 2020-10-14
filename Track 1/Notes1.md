# Notes

In cloud computing, the capital investment in building and maintaining data centers is replaced by consuming IT resources as an elastic,
utility-like service from a cloud “provider” (including storage, computing, networking, data processing and analytics, 
application development, machine learning, and even fully managed services).

It gives organizations the opportunity to not only improve flexibility, reduce costs, and focus on core competencies, 
but also to fully transform how they operate — for example, 
by re-designing internal workflows or customer interactions as digital experiences that extend from the data center all the way through to mobile devices.

Some good initial use cases for migrating to the cloud: Disaster recovery (DR), Data archiving, Managed services, etc.


Few services of GCP

1. Computing and hosting
   Options like serverless computing, application platform
   
   Cloud Functions                                                                                                                        
   Google Cloud's functions as a service (FaaS) offering, provides a serverless execution environment for building and connecting cloud services.                
   With Cloud Functions one can write simple, single-purpose functions that are attached to events emitted from your cloud infrastructure and services.             
   The function is triggered when an event being watched is fired. The code executes in a fully managed environment.                                      
   There is no need to provision any infrastructure or worry about managing any servers.                                                                       
   Cloud Functions can be written using JavaScript, Python 3, Go, or Java.                                                                                       
   Take the function and run it in any standard Node.js (Node.js 10), Python 3 (Python 3.7), Go (Go 1.11 or 1.13) or Java (Java 11) environment, 
   which makes both portability and local testing a breeze.                                                                                                         
   
   App Engine                                                                                                                                                       
   It is Google Cloud's platform as a service (PaaS). With App Engine, Google handles most of the management of the resources for you.                     
   For example, if your application requires more computing resources because traffic to your website increases,                                              
   Google automatically scales the system to provide those resources. If the system software needs a security update, that's handled for you, too           
   
   Container computing
   With container-based computing, one can focus on application code, instead of on deployments and integration into hosting environments.                              
   Google Kubernetes Engine (GKE), Google Cloud's containers as a service (CaaS) offering, is built on the open source Kubernetes system,                           
   which gives the flexibility of on-premises or hybrid clouds, in addition to Google Cloud's public cloud infrastructure.                                       
   
   Compute Engine                                                                                                                                                  
   Google Cloud's unmanaged compute service is Compute Engine. One can think of Compute Engine as providing an infrastructure as a service (IaaS),                  
   because the system provides a robust computing infrastructure, but you must choose and configure the platform components that one want to use.                 
   
   Combining computing and hosting options is done in an efficient way to meet the needs.                                                                                   
   
2. Storage                                                                                                                                                     
   Consistent, scalable, large-capacity data storage in Cloud Storage. Cloud Storage comes in several flavors.                                                             
   Persistent disks on Compute Engine, for use as primary storage for the instances.                                                                     
   Fully managed NFS file servers in Filestore.                                                                                                              

3. Databases                                                                                                                                                               
   Google Cloud provides a variety of SQL and NoSQL database services.                                                                                      
   A SQL database in Cloud SQL, which provides either MySQL or PostgreSQL databases.                                                                                
   Two options for NoSQL data storage: Firestore, for document-like data, and Cloud Bigtable, for tabular data.                                                        
   One can also choose to set up your preferred database technology on Compute Engine by using persistent disks.                                                      
   For example, you can set up MongoDB for NoSQL document storage.                                                                                         

4. Networking                                                                                                                                      
   Networks, firewalls, and routes                                                                                                                     
   
   Virtual Private Cloud (VPC) provides a set of networking services that your VM instances use. An instance can have more than one interface,                       
   but each interface must be connected to a different network. Every VPC project has a default network.                                                     
   You can create additional networks in your project, but networks cannot be shared between projects.                                                  
  
   Firewall rules govern traffic coming into instances on a network.                                                                                        
   The default network has a default set of firewall rules, and you can create custom rules, too.                                                                  

   A route lets you implement more advanced networking functions in your instances, such as creating VPNs.                                                     
   A route specifies how packets leaving an instance should be directed. For example,                                                                    
   a route might specify that packets destined for a particular network range should be handled by a gateway virtual machine instance that you configure and operate.  

   Load balancing                                                                                                                                           
   If your website or application is running on Compute Engine, the time might come when you're ready to distribute the workload across multiple instances.         
   Server-side load balancing features provide you with the following options: HTTP(S) load balancing and Network load balancing                         
  
  
5. Big data                                                                                                                                         
   Big data services enable you to process and query big data in the cloud to get fast answers to complicated questions regarding data analysis.                    
   Batch and streaming data processing.                                                                                                                 
   Dataflow provides a managed service and set of SDKs that you can use to perform batch and streaming data processing tasks.                                   
   
   Pub/Sub is an asynchronous messaging service. Your application can send messages as JSON data structures to a publishing unit called a topic.                         
   Because Pub/Sub topics are a global resource,                                                                                                      
   other applications in projects that you own can subscribe to the topic to receive the messages in HTTP request or response bodies.                                
   Pub/Sub's usefulness isn't confined to big data. You can use Pub/Sub in many circumstances where you need an asynchronous messaging service.                 
   
6. Machine learning                                                                                                                                                
   Google Cloud offers a variety of APIs that enable you to take advantage of Google's ML without creating and training your own models.                           
