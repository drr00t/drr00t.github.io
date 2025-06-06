---
layout: post
title: Quarkus Outbox Packing Domain Aggregate to Stream Analytics
date: 2025-06-05 12:01:02 -0300
description: Exploring the use of Quarkus and the Outbox pattern for efficient data streaming and aggregation.
img: 02-outbox-post.png # Add image post (optional)
# fig-caption:  # Add figcaption (optional)
tags: [Quarkus, outbox, stream-analytics, cdc, aggregation, data-in-motion, data-engineering, kafka, debezium, postgresql, data-architecture]
---

# **Just a preview of the content, I will write a full post about this topic in the future.**

> The dual-write problem is a common challenge in microservices architectures, where two or more services need to maintain consistency across their data stores. This can be particularly difficult when one service needs to update another service's data store, as it can lead to issues with data integrity and reliability.



## Architecture


### My Reference Architecture diagram
The diagram below illustrates a reference architecture for handling transactional changes and addressing the dual-write problem using the Outbox pattern. By leveraging the relational database's Write-Ahead Log (WAL) and Debezium for change data capture (CDC), only relevant business events are published. This approach avoids the need to monitor all database tables, ensuring that only intentional, consistent changes are streamed to downstream systems.

![]({{site.baseurl}}/assets/img/02-outbox-pattern.png)
_Image-1: Simplified architecture for Outbox with Quarkus_


## Technology stack

- Docker Compose for local development and testing
- PostgreSQL as the source database
- Quarkus for building the outbox service

## Repository with demo project

All the components are open-source and can be run on any cloud provider or on-premises. The technology. I will not list here because everything will be in the code repository.

[https://github.com/drr00t/ppajm-apcn-quarkus/tree/main/sakila-sa-cdc](https://github.com/drr00t/ppajm-apcn-quarkus/tree/main/sakila-sa-cdc)

> Disclaimer: This repository is a work in progress and is not a recommendation and I will do not provide a full documentation about configuration options. My idea with this it's to provide some glance of how to use the technology stack and how to put it together.

## References

[The Transactional Outbox Pattern](https://developer.confluent.io/courses/microservices/the-transactional-outbox-pattern/)
[Eliminating the Dual-Write Problem in Apache Kafka Using the Outbox](https://www.confluent.io/events/kafka-summit-london-2023/eliminating-the-double-write-problem-in-apache-kafka-using-the-outbox/)
[Pattern: Transactional outbox](https://microservices.io/patterns/data/transactional-outbox.html)
