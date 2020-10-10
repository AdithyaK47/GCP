# Google Cloud Pub/Sub: Qwik Start - Console

Pub/Sub is an asynchronous messaging service that decouples services that produce events from services that process events.

In other words, a messaging service for exchanging event data among applications and services. 
A producer of data publishes messages to a Cloud Pub/Sub topic. A consumer creates a subscription to that topic. 
Subscribers either pull messages from a subscription or are configured as webhooks for push subscriptions. 
Every subscriber must acknowledge each message within a configurable window of time.
Pub/Sub offers durable message storage and real-time message delivery with high availability and consistent performance at scale.

# Core concepts

Topic: A named resource to which messages are sent by publishers.

Subscription: A named resource representing the stream of messages from a single, specific topic, to be delivered to the subscribing application. 

Message: The combination of data and (optional) attributes that a publisher sends to a topic and is eventually delivered to subscribers.

Message attribute: A key-value pair that a publisher can define for a message. 
