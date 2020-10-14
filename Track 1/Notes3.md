# Reliable task scheduling on Compute Engine with Cloud Scheduler

Cron is the standard tool for scheduling recurring tasks on Unix systems.
As the systems you build increase in complexity and become distributed, a single computer running cron can become a critical point of failure. 

Cloud Scheduler provides a fully managed, enterprise-grade service that lets you schedule events.
After you have scheduled a job, Cloud Scheduler will call the configured event handlers, which can be App Engine services, HTTP endpoints, or Pub/Sub subscriptions.

To run tasks on your Compute Engine instance in response to Cloud Scheduler events, you need to relay the events to those instances. 
One way to do this is by calling an HTTP endpoint that runs on your Compute Engine instances.
Another option is to pass messages from Cloud Scheduler to your Compute Engine instances using Pub/Sub

# Serving websites

https://cloud.google.com/solutions/web-serving-overview

What is serverless?

Serverless computing is a paradigm shift in application development that enables developers to focus on writing code without worrying about infrastructure. 
It offers a variety of benefits over traditional computing, including zero server management, no up-front provisioning, auto-scaling, and paying only for the resources used. 
These advantages make serverless ideal for use cases like stateless HTTP applications, web, mobile, IoT backends, batch and stream data processing, chatbots, and more.

Cloud Functions (SERVERLESS FUNCTIONS & EVENTS)
App Engine standard environment (SERVERLESS HTTP APPLICATIONS)
Cloud Run (SERVERLESS CONTAINERS)

