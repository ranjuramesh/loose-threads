---
title: Let's talk data - Schema Evolution
type: take
tags:
  - data
date:
  "{ date:YYYY-MM-DD }":
substack_url:
published: false
---
Schema Evolution is one of the core data problems and it has been around since the first database got built. It starts as simple as dealing with a table column being dropped to as complex as a reference schemas being changed in a schema registry. But the fundamental problem statement is - "Something changed in the source and now there is a need to make sure the data pipelines are able to deal with it."

Before we dig in, I want to make one important statement -
> ***Data generates value only when it flows.

## Definition of Schema Evolution

"["Schema evolution is about dealing with changing data structures and compositions, while still making sure the downstream data pipelines don't break and cause data integrity issues."]
## Typical Schema Evolution example

![[Pasted image 20240724072313.png]]
^[Copyright - # DAMPF - Dresden Auto-Managed Persistence Framework by Sebastian Gotz]
Nature of data is to change, both in content and structure. Any system which is not able to cater to this is going to be unusable for live production systems. For example, consider the picture above. A student schema which was earlier supplying current semester field replaced it with birthday, which will cause all the downstream data pipelines to fail. 
# Schema evolution - Producer vs Consumer

Who is responsible for making sure schema evolution doesn't lead to data pipeline failures. This question taps into a much larger question of who is responsible for data? Producer or the Consumer. Different data teams have tackled this according to their own preferences, but my experience has been that consumers are the ones who care more about schema evolution rather than producers.
![[Pasted image 20240724083922.png]]
^[Copright - Carnegie Mellon institute]
# Schema evolution with Change Management

It can be argued that the upstream shouldn't change the schema without notifying all the downstream systems. But this means that there is a need for a intensive change management process.  For anyone who is interested to know more about change management in Data, here is a good article about it - https://changemanagementinsight.com/the-process-of-change-management-in-data-governance/

Now, the trade-off here is that you are dependent on process to make sure failures are minimized w.r.t. change management. But with the speed with which the current software teams move, it is too much of a dead weight to use change management for mitigating schema evolution.
# Schema evolution in different data categories

There are many ways to categorize data and one popular approach is the based on the structure of the data. Based on structure, there are 3 categories of data - Structured, Semi-Structured and Unstructured. This is a good article to learn more about this - https://www.forbes.com/sites/bernardmarr/2019/10/18/whats-the-difference-between-structured-semi-structured-and-unstructured-data/. Due to various reasons, the way each category of data deals with schema evolution is different. 

Structured data is the one that has been around for a long time and is the defacto for software team even today. And due to it's long history, schema evolution is the most difficult in structured data. It usually falls on to change management and data governance to deal with the schema changes. But over time, we can use data dictionary, data catalog and multiple table versions to manage schema evolution.

With Semi-structured data, metadata along with data catalog is a must. Schema registry helps a lot while dealing with semi-structured data.

Finally, unstructured data is wild wild west. Frankly, I have not seen a use case where unstructured data was used. Most of the time, unstructured needs some form ML to make it useful.

![[Screenshot 2024-07-24 at 8.24.59 AM.png]]
# Schema evolution with Schema Registry

Schema registry is an idea that has been around for a while now and it's very interesting. You build a central repository where the schema is stored with strong versioning. It's upto the consumer to figure out which version that they want to use. This approach caught on with Kafka and I believe, this should be de-facto for all data schemas.
![[Pasted image 20240724083417.png]]
^[Copyright - Confluent, Inc]
This is a schema registry implementation for Kafka by Confluent. It's very similar to having an additional verification mechanism, wherein the consumers can understand what is the current state of data and then make necessary decisions themselves based on their requirements.
# Schema evolution and data products

Finally, I come to the most important part of this entire blog. Why is schema evolution important? It's because data products can be successful only when there is a good way to automatically manage schema evolution and in real time. This is fundamental to delivering data products which meets key metrics like uptime, consumption etc.