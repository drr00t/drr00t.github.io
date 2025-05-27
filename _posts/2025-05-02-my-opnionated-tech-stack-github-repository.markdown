---
layout: post
title: I would like to share my opinionated tech stack experimentations for data in motion and analytics
date: 2025-05-01 12:01:02 -0300
description: An opinionated overview and hands-on example of a modern data-in-motion stack for real-time change data capture and analytics.
img: 00-big-picture-oltp-olap-1.png # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [cdc, change-data-capture, event streaming, stream analytics, distributed systems, data architecture, tech-stack, graph, data-in-motion, data-engineering, batch processing, data lake, lakehouse, warehouse]
---


In the world of streaming technologies, PostgreSQL stands out thanks to its low-overhead replication protocol. This enables the use of the change data capture (CDC) pattern to replicate data incrementally.

## My Reference Architecture diagram

The Image-1 bellow, shows the base architecture used for most of companies that I have worked with. It is a simplified architecture that can be used for most of the companies. Operational view and Analytical view are separated. 

![]({{site.baseurl}}/assets/img/00-big-picture-oltp-olap-1.png)
_Image-1: Simplified architecture separating operational and analytical views_

The Image-2 bellow, shows the architecture as I see currently, the analytical view it is a special case of operational view.

![]({{site.baseurl}}/assets/img/00-big-picture-oltp-and-olap-special-case-1.png)
_Image-2: Simplified architecture considering analytical view as a special case of operational_

## Technology stack

All the components are open-source and can be run on any cloud provider or on-premises. The technology. I will not list here because everything will be in the code repository.

[https://github.com/drr00t/my-data-in-motion-tech-stack](https://github.com/drr00t/my-data-in-motion-tech-stack)

### Disclaimer

This is my opinionated tech stack, and it is not a recommendation. It is based on my experience and the experience of the companies I have worked with. It is not a definitive list of technologies, and it is not exhaustive. It is a starting point for your own research and experimentation.
