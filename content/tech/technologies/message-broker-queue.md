---
title: "Message Broker/Queue"
description: ""
lead: ""
date: 2021-04-10T23:48:41+12:00
lastmod: 2021-04-10T23:48:41+12:00
draft: false
images: []
menu: 
  tech:
    parent: "technologies"
weight: 180
toc: true
---

Common Terms:
- Producer - anything that publishes a message
- Consumer - anything that consumes a message

Common Metrics: 
- Messages In/Out Count/rate
- Failure
- Queued messages/Queue depth

## [Apache ActiveMQ](https://activemq.apache.org/)

- Message broker

Terms:
- Queue - messages awaiting delivery to a single consumer
- Topic - Messages to be delivered to multiple consumers subscribed to that topic
- Store - space on storage occupied by persistent messages

Metrics:
- [JVM metrics](/tech/technologies/language/#java)
- Average enqueue time - Avg time from in to out of messages
- Queue size - Number of messages in the queue/store not acknowledged by a consumer
- Count
- Enqueue count - Number of message sent to queue
- Dequeue count - Number of message removed from queue
- Expired count - Number of messages not delivered because they expired
- Memory/Storage
- Memory usage - % usage of memory limit for NON_PERSISTENT messages
- Store usage - % usage of storage limit for PERSISTENT messages
- Temp usage - % usage of storage limit for temporary messages

[Dynatrace ActiveMQ monitoring](https://www.dynatrace.com/support/help/technology-support/application-software/other-technologies/supported-out-of-the-box/activemq/)

## [Apache Kafka](https://kafka.apache.org/)

- Can be thought of as an advanced Queue
- Apps write records (K:V) to Kafka Topics (Producer API)
- Apps can subscribe to topics (Consumer API)
- Intermediaries can subscribe to data, process it and place it in Output topics (Streams API)
- Apps can listen to changes (Connector API)

Terms: 
- Topics
- Logs (one per topic)
- Distributions (multiple per topic)
- Leader (server that handles read/write to a partition)

Metrics:


[Dynatrace Apache Kafka monitoring](https://www.dynatrace.com/support/help/shortlink/kafka)
 
## [IBM App Connect (Integration Bus)](https://www.ibm.com/docs/en/integration-bus)

- Connect applications together, regardless of message formats or protocols that they support
- Can transform messages from one format to another, route messages based on content, enrich - capabilities that IBM MQ does not have

[Dynatrace IBM Integration Bus monitoring](https://www.dynatrace.com/news/blog/get-out-of-the-box-visibility-into-your-ibm-integration-bus-beta/)

## [IBM MQ](https://www.ibm.com/products/mq)

Metrics:
- Queue depth
- Oldest Message Age
- Active Channels

[Dynatrace IBM MQ monitoring](https://www.dynatrace.com/support/help/shortlink/ibm_mq_activegate_extension)

## [Mule ESB (Enterprise Service Bus)](https://www.mulesoft.com/resources/esb/what-mule-esb)

## [RabbitMQ](https://www.rabbitmq.com/)

- Message broker
- Well suited for loosely coupled microservices

Terms:
- Exchange: Messages are pushed to exchange
- Queue: Exchange routes message to a Queue

Metrics:
- Messages Published - The rate at which messages are incoming to the RabbitMQ cluster
- Queued Messages
- Messages Delivered & Get - Outgoing delivered messages
- Channels - The number of channels (virtual connections). High number of channels may mean memory leak in node
- Failed - The number of unhealthy nodes

[Dynatrace RabbitMQ monitoring](https://www.dynatrace.com/support/help/technology-support/application-software/other-technologies/supported-out-of-the-box/rabbitmq/)