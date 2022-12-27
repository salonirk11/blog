---
layout: post
title:  "System Design: Non-Functional Requirements"
categories: [ System Design ]
image: assets/images/demo1.jpg
---

Non-Functional Requirements are those requirements that are not directly related to the product/feature/functionality 
we want to build. These requirements should be built into the system inherently by the engineering team to make good 
systems.

Here we discuss the main Non-Functional requirements that need to be considered before designing a system.

Critical non-functional requirements are: 
- Availability
- Reliability
- Maintainability
- Scalability
- Fault Tolerance

## Availability
The system you design should be readily available to the users which means, whenever a user wants, they should be able 
to access the system with normal behavior.

### What contributes to downtime?
- Software Crashes
- Hardware failures
- Human errors
- Planned Downtime

### Measuring Availability
Availability can be visualized as the ratio of the time the system was available to the total time the system was 
expected to be available.

Availability = \frac{Total Time - Service down time}{Total Time} * 100  

Eg. If a system was running for 24 hours and the system was down for 8 minutes the availability of this system would be:
99.5% availability is also referred to as 2 Nines availability.

Availability = \frac{24 * 60 - 8}{24*60} * 100 ~ 99.5%

Here is a reference table of service downtime allowed for standard availabilities:
![walking]({{ site.baseurl }}/assets/images/table1.jpg)

Higher the availability, the higher the nines, the better.

Ideally, our system should aim for high availability, but that comes with a trade-off with consistency in the case of network-partitioned distributed systems (CAP Theorem).

### Ensuring Availability
- Making the system fault tolerant
- Removing any single point of failure using Redundancy and Replication

## Reliability

