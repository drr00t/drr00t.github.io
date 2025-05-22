---
layout: post
title: Putting Posgresql Data in Motion with Kafka-connect and Debezium
date: 2025-04-01 12:01:02 -0300
description: A full environment of a running example of kafka-connect cdc with debezium and postgresql
img: 01-cdc-triad.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [kafka-connect, debezium, cdc, change-data-capture, kafka, postgres, tech-stack]
---


In the world of streaming technologies, PostgreSQL stands out thanks to its low-overhead replication protocol. This enables the use of the change data capture (CDC) pattern to replicate data incrementally.


## Challenge
The challenge is to capture changes in a PostgreSQL database table and make them available to other services with minimal impact on the main service.

## Architecture
The architecture consists of a PostgreSQL database, a Kafka cluster, and a Kafka-connect cluster with the Debezium connector. The Debezium connector captures changes in the PostgreSQL database and sends them to a Kafka topic. Other services can then consume the changes from the Kafka topic.

### Architecture diagram

![Postgresql change data capture architecture]({{site.baseurl}}/assets/img/01-cdc-postgres.png)

### Architecture components

- **PostgreSQL**: relative scalability.
- **Market Open standard**.
  - **Kafka**: high-throughput distributed messaging system.
  - **Kafka Connect**: It is a integration tool, scalable, reliably for streaming data between Apache Kafka and other systems.
    - **Debezium Connector**: open-source CDC tool for capturing changes in database systems.

## Solution

Running experiment available at [kafka-connect-debezium-postgres](https://github.com/drr00t/kafka-connect-debezium-postgres)

### Usage scenarios

- Capturing changes in a PostgreSQL database table and making them available to other services.
- Replicating data from PostgreSQL to other data stores (e.g., Elasticsearch, MongoDB) in real-time.
- Enabling event-driven architectures by publishing database changes as events to a Kafka topic.

## References

- [The Transactional Outbox Pattern](https://developer.confluent.io/courses/microservices/the-transactional-outbox-pattern/)
- [Eliminating the Dual-Write Problem in Apache Kafka Using the Outbox](https://www.confluent.io/events/kafka-summit-london-2023/eliminating-the-double-write-problem-in-apache-kafka-using-the-outbox/)
- [Pattern: Transactional outbox](https://microservices.io/patterns/data/transactional-outbox.html)
