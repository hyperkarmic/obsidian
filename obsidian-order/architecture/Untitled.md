# 6 architecture models

# 1. Layered (N-tier) architecture

The layered architecture pattern, also known as the N-tier architecture pattern, is the standard architecture used for most Java Enterprise applications. A layered architecture style divides components (or applications) into horizontal, logical layers.

Each layer has a distinct role within the system. One layer may be responsible for handling business logic, while another is responsible for handling presentation logic. This demonstrates a concept known as the separation of concerns (SoC). Components of a layer will **only** deal with logic within that layer. Separating layers like this also makes testing and developing software easier as the pattern itself isn’t too complex. The downside is that this isn’t the most efficient pattern to use and can be difficult to scale up.

Most layered architectures will consist of four closed layers:

-   Presentation
-   Business
-   Persistence
-   Database

***
# 2. Client-server architecture

In a client-server architecture, there are multiple nodes or clients connected over a network or internet connection who communicate with a central server.

There are two main types of components:

-   **Service requesters** (aka clients) that send requests
-   **Service providers** that respond to requests

In this architecture, the server hosts, manages and delivers most of the resources and services a client requests. This is also known as a **request-response messaging pattern**.
***
#  3 .Event-driven architecture

Event-driven architecture patterns are distributed asynchronous architecture patterns that are highly adaptable. This pattern is best suited for small to large applications with high scalability. Since event-processor components are isolated from each other in this pattern, changes to components can be made without impacting the performance of other components.

There are two main topologies to this pattern: the **mediator** and the **broker** topologies.

Mediator topologies have four main types of components:

-   Event queues
-   Event mediators
-   Event channels
-   Event processors

**Mediator topologies** are used when an event has multiple steps that require some level of coordination through a central mediator to be processed.

When a user sends the initial event to an **event queue**, the initial event is then directed to the **event mediator**.

Receiving the initial event prompts the event mediator to publish and send processing events to event channels, telling them to start executing each process step. The event processors receiving the processing events from the event channels contain business logic components that execute all of the steps required to process the initial event.

In general, event-processor components should only perform a single business task without relying on other event processors. This is because you want your event processors to be able to run steps concurrently with other event processors.
***
# 4. Microkernel architecture

Microkernel architectures (also known as plug-in architectures) are typically used to implement applications that can be downloaded as a third-party product. This architecture is also commonly found in internal business applications.

One fun thing about this architecture is that you can actually embed it within other patterns, like layered architectures.

There are two types of architectural components in your typical microkernel architecture: a **core system** and **plug-in modules**.
***
The **core system** contains the minimum business logic needed to make the software system operational. You can extend the software system’s functionality by connecting **plug-in components** to add more features.

It’s kind of like adding a cold-air intake to your car to boost its torque and horsepower.
***
# 5 Microservices architecture

Microservices architectures are one of the most popular software trends at the moment, and one reason for this can be attributed to the easy scalability of development. When microservices can no longer be maintained, they can be rewritten or replaced.

There’s no universally accepted definition for the term **“microservice”**. We will define a microservice as an independently deployable module for this article.

A microservices architecture consists of groups of small, independent, self-contained services with small code bases. Unlike with a monolithic application using a layered architecture pattern, keeping small, separate code bases can minimize the number of dependencies.

Each component of a microservices architecture is deployed as a separate unit. **Separately deploying units** streamlines the delivery pipeline and makes deployment much faster. Development teams can easily build up **continuous delivery** pipelines with smaller units. Testing also becomes easier because you only need to test the features of an individual microservice.
***
# 6. Cloud-native architecture

When you think about typical web applications, most of them typically process requests from clients in the same way. A client sends a request from the web browser, which is sent to the web server, then an application server, and finally, the database server. When this kind of data flow deals with a high volume of concurrently running requests, you typically end up with bottleneck issues. This is where cloud-native architecture patterns come in. Cloud-native patterns are designed to minimize scalability- and concurrency-related issues by removing the central database and using **replicated, in-memory data grids** instead.

The cloud-native architecture is primarily used for [distributed computing systems](https://www.educative.io/blog/distributed-systems-considerations-tradeoffs?eid=5082902844932096) where the interactions between components are mediated through one or more shared spaces.

In this shared space, the components exchange tuples and entries. This brings us to the concept of tuple spaces, or the idea of distributed shared memory.

**Tuple spaces** provide a repository of tuples that can be accessed concurrently. Application data is kept in memory and replicated across active processing units.

The two main types of components within this architecture pattern are:

-   Processing units
-   Virtual middleware

Processing units will typically contain:

-   Application modules
-   An in-memory data grid
-   Optional asynchronous persistence store for failover
-   A data replication engine

The **data replication engine** is what the **virtual middleware** uses to replicate data changes made in one processing unit across all other active processing units.
***
[Software architecture diagramming and patterns | by The Educative Team | Jun, 2022 | Dev Learning Daily](https://learningdaily.dev/software-architecture-diagramming-and-patterns-7d38999e7a12)

%%to do ------rip images out of above article!!!!%%
***
#archetecture-patterns #microservices #microkernel #event-driven #cloud-native #layered