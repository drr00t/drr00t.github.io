---
layout: post
title: Putting Posgresql Data in Motion with Kafka-connect and Debezium
date: 2025-05-10 12:01:02 -0300
description: A full environment of a running example of kafka-connect cdc with debezium and postgresql
img: 01-cdc-triad.png 
# fig-caption: 
tags: [outbox, stream-analytics, cdc, debezium, kafka, kafka-connect, postgresql, data-in-motion, data-engineering]
---

> Change Data Capture (CDC) is a design pattern that allows you to capture changes in a database and propagate them to other systems. It is often used in event-driven architectures to keep data in sync across different services.


## Architecture
The architecture consists of a PostgreSQL database, a Kafka cluster, and a Kafka-connect cluster with the Debezium connector. The Debezium connector captures changes in the PostgreSQL database and sends them to a Kafka topic. Other services can then consume the changes from the Kafka topic.


### My Reference Architecture diagram

The Image-1 bellow, shows the base architecture used for most of companies that I have worked with. It is a simplified architecture that can be used for most of the companies. Operational view and Analytical view are separated. 

![]({{site.baseurl}}/assets/img/01-cdc-postgres.png)
_Image-1: Simplified architecture for CDC with PostgreSQL, Kafka, and Debezium_

## Technology stack

This is a fully open-source and open-standard toolset for running CDC:

- Docker Compose for local development and testing
- PostgreSQL as the source database
- Kafka as the event streaming platform
- Kafka-connect with Debezium connector for change data capture (CDC)
- AKHQ for Kafka topic management and monitoring

## Repository with demo project

All the components are open-source and can be run on any cloud provider or on-premises. The technology. I will not list here because everything will be in the code repository.

[https://github.com/drr00t/my-data-in-motion-tech-stack](https://github.com/drr00t/my-data-in-motion-tech-stack)


> Disclaimer: This repository is a work in progress and is not a recommendation and I will do not provide a full documentation about configuration options. My idea with this it's to provide some glance of how to use the technology stack and how to put it together.

## References
- [Event Sourcing vs. Change Data Capture](https://debezium.io/blog/2020/02/10/event-sourcing-vs-cdc/)
- [Succeeding with Change Data Capture](https://www.confluent.io/blog/how-change-data-capture-works-patterns-solutions-implementation/) 