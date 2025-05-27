---
layout: post
title: Quarkus Outbox Packing Domain Aggregate to Stream Analytics
date: 2025-04-01 12:01:02 -0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
# img: i-rest.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Quarkus, outbox, stream-analytics, cdc, outbox, aggregation, data-in-motion, data-engineering, kafka, debezium, postgresql, data-architecture]
---

# **Just a preview of the content, I will write a full post about this topic in the future.**

> The dual-write problem is a common challenge in microservices architectures, where two or more services need to maintain consistency across their data stores. This can be particularly difficult when one service needs to update another service's data store, as it can lead to issues with data integrity and reliability.



## Architecture


### My Reference Architecture diagram


## Technology stack

- Docker Compose for local development and testing
- PostgreSQL as the source database
- Kafka as the event streaming platform
- Kafka-connect with Debezium connector for change data capture (CDC)
- AKHQ for Kafka topic management and monitoring
- Quarkus for building the outbox service

## Repository with demo project

All the components are open-source and can be run on any cloud provider or on-premises. The technology. I will not list here because everything will be in the code repository.


[https://github.com/drr00t/my-data-in-motion-tech-stack](https://github.com/drr00t/my-data-in-motion-tech-stack)

> Disclaimer: This repository is a work in progress and is not a recommendation and I will do not provide a full documentation about configuration options. My idea with this it's to provide some glance of how to use the technology stack and how to put it together.

## References

[The Transactional Outbox Pattern](https://developer.confluent.io/courses/microservices/the-transactional-outbox-pattern/)
[Eliminating the Dual-Write Problem in Apache Kafka Using the Outbox](https://www.confluent.io/events/kafka-summit-london-2023/eliminating-the-double-write-problem-in-apache-kafka-using-the-outbox/)
[Pattern: Transactional outbox](https://microservices.io/patterns/data/transactional-outbox.html) -->
