---
title: MULE Exam - v1.1July2024
document_type: lesson
source: Solace Academy
learning_path: Solace Certified Event-Driven Integration - MuleSoft
course: Solace Certified Event-Driven Integration - MuleSoft Exam
lesson_order: 1
---

# MULE Exam - v1.1July2024

## Academy state

Timed exam, 18 questions. At start, the page showed 43 minutes 31 seconds remaining and 3 of 3 attempts left. The questions are paginated, with one question per page. No instructional images are presented on the question screen; the question content and choices are captured below.

## Questions

### Question 1 of 18 — Choose 3

**Question:** A bank needs to be able to get a complete view of your customer data (Customer 360). However, most of the systems containing the various parts of the Customer profile are dispersed across different data centers and geographies. The bank only uses REST APIs to expose data from internal systems, so the Customer 360 API needs to orchestrate calls to all remote systems, aggregate the data, and present it to user. Which three problems will this implementation pose?

**Choices:**

- Scaling the Customer 360 API and the dependent APIs will be challenging.
- The Core Process API (Customer 360) can time out if there are too many remote calls to be orchestrated, and the “Segment” data APIs are geographically distant.
- If the API calls are deep, this makes the architecture brittle and will lead to the risk of timeout.
- You cannot place load balancers at all levels.
- Changes to one of the API calls in the core orchestration API can be risky as it can impact all the other API calls in the orchestration (due to coupling).

**Selected answers:**

- Scaling the Customer 360 API and the dependent APIs will be challenging.
- The Core Process API (Customer 360) can time out if there are too many remote calls to be orchestrated, and the “Segment” data APIs are geographically distant.
- Changes to one of the API calls in the core orchestration API can be risky as it can impact all the other API calls in the orchestration (due to coupling).

**Rationale:** These selections reflect the scaling, latency/timeout, and coupling risks of synchronous REST orchestration across distant systems. The course lesson on data aggregation describes timeouts as systems and geography increase, and the design principles emphasize coupling on the data path. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 2 of 18 — Single choice

**Question:** Orchestrations can maintain the state of a transaction because they are centrally managed, and every state change (step) in the orchestration can be tracked. In a choreography, due to its “decentralized” nature, state management is challenging. The Event Mesh is the core platform over which choreography is executed in this case. What you need to do?

**Choices:**

- Every service in the choreography needs to be “state aware” and update the state into a database.
- Every service in the choreography needs to be “state aware” and update the by sending an Event to an Event API to update the state in a remote system.
- Every service in the choreography needs to be “state aware” and update the state by calling an API, which can front end any type of storage mechanism.
- The Event Mesh can use variables in the definition of a topic hierarchy. One of the segments in the hierarchy can contains a state signal.

**Selected answer:** The Event Mesh can use variables in the definition of a topic hierarchy. One of the segments in the hierarchy can contains a state signal.

**Rationale:** This matches the course explanation of stateful choreography: participants use topic-structure variables as cues to signal process state, and a monitoring subscriber can observe state changes without a central orchestrator. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 3 of 18 — Single choice

**Question:** You are designing an Order Fulfillment architecture. You are considering how to use synchronous and asynchronous patterns of integration in your design. The Event Mesh is one of the considerations. Which is the best option?

**Choices:**

- Use REST APIs to capture the initial order, but use an Event Mesh with state monitoring capabilities to choreograph the other fulfillment steps.
- Orchestrate the entire process using REST APIs.
- Use REST APIs to capture the initial order, but use an event platform to choreograph the other fulfillment steps. Manage state external through a REST API based service.
- Use REST APIs to capture the initial order, but use an event platform to choreograph the other fulfillment steps. Manage state external through an Event API based service.

**Selected answer:** Use REST APIs to capture the initial order, but use an Event Mesh with state monitoring capabilities to choreograph the other fulfillment steps.

**Rationale:** The course's order-fulfillment example uses an OMS to start the process and event choreography for subsequent steps, with topic structure providing state visibility. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 4 of 18 — Single choice

**Question:** MuleSoft created the API Lifecycle Management framework. The framework has the following sequential steps: 1. design 2. implement 3. deploy 4. manage 5. secure 6. consume. Which of these steps are supported by Solace as it pertains to Event API Lifecycle Management?

**Choices:**

- design, implement, deploy, manage
- design, implement, deploy, manage, secure, consume
- design, implement, deploy, manage, secure, consume, monetize
- design, implement, deploy

**Selected answer:** design, implement, deploy, manage, secure, consume.

**Rationale:** Solace Event API lifecycle management spans design through secure consumption; monetization is the added distractor. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 5 of 18 — Choose 2

**Question:** You are adding an Event Mesh to your distributed architecture. What are two of the unique Event Mesh properties?

**Choices:**

- authentication and authorization
- support for pub-sub as an event exchange pattern
- protocol bridging
- dynamic routing and filtering

**Selected answers:** protocol bridging; dynamic routing and filtering.

**Rationale:** The course explicitly describes native protocol bridging and dynamic destination-based routing/filtering as Event Mesh capabilities. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 6 of 18 — Choose 2

**Question:** The Event Mesh is the highest level of scaling for the Solace platform. Which two other forms of scaling are part of the Solace platform?

**Choices:**

- load balancer clustering
- broker clustering for horizontal scaling
- partition scaling
- partitioned queues for vertical consumer scaling

**Selected answers:** broker clustering for horizontal scaling; partitioned queues for vertical consumer scaling.

**Rationale:** The course identifies broker clustering and Partitioned Queues as the other scaling forms, including vertical consumer scaling through Partitioned Queues. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 7 of 18 — Choose 2

**Question:** You work in a truck manufacturing company and part of your predictive maintenance strategy is to have real time insight into how the engines on the road are performing. That means that the sensors on the engines will emit events that you need to collect and analyze in real time. Sensors communicate via MQTT. In your enterprise environment you have three types of messaging platforms: IBM MQ for integration to legacy systems; TIBCO EMS for general enterprise-wide event driven integrations; Hive MQ (MQTT) for IoT purposes. You have an Event Mesh at your disposal, so you can use this in your design. What are the two best ways to have engine events make their way into the legacy ERP fronted by IBM MQ?

**Choices:**

- Write a microservice that subscribes to MQTT events and publishes the event to TIBCO EMS. Write a second microservice that subscribes to TIBCO EMS and then re-publishes the event to IBM MQ.
- Use the Event Mesh and bridge all protocols into one unified messaging fabric.
- Write a microservice that subscribes to MQTT events and publishes the event to IBM MQ.
- Use the Event Mesh and bridge all protocols into one unified messaging fabric and replace the Hive MQ Broker with a Solace Broker.

**Selected answers:** Use the Event Mesh and bridge all protocols into one unified messaging fabric; use the Event Mesh and bridge all protocols into one unified messaging fabric and replace the Hive MQ Broker with a Solace Broker.

**Rationale:** Both selections use the Event Mesh to connect the MQTT sensor path to legacy IBM MQ, with the second also consolidating the IoT broker on Solace. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 8 of 18 — Single choice

**Question:** A bank needs to be able to get a complete view of your customer data (Customer 360), however most of the systems containing the various parts of the Customer profile are dispersed across different data centers and geographies. What is the less risky way to accomplish this?

**Choices:**

- Create a REST-full Customer 360 API that orchestrates the API calls to all the other “segment” APIS.
- Use an Event Mesh to implement a Map Reduce paradigm whereby you request responses from each “Profile Segment” holder system, and aggregate the response before presentation with every Profile Segment holder system exposed by REST APIs.
- Use an Event Mesh to implement a Map Reduce paradigm whereby you request responses from each “Profile Segment” holder system, and aggregate the response before presentation.

**Selected answer:** Use an Event Mesh to implement a Map Reduce paradigm whereby you request responses from each “Profile Segment” holder system, and aggregate the response before presentation.

**Rationale:** This uses distributed request/reply and aggregation over the Event Mesh, avoiding the centralized synchronous REST orchestration path across distant systems. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 9 of 18 — Choose 2

**Question:** You are planning an Event Driven Infrastructure in your enterprise. The applications and systems across your enterprise are on different networks and installed on hardware platforms with different processing abilities. These systems are spread across an ecosystem that includes cloud-based, on-premises modern (Linux-based installs), and on-premises legacy environments (mainframes OS390s/VMS/VSAM). The business cannot lose data as it will impact the customer experience and can lead to loss of revenue. You have the Event Mesh at your disposal. Given that you need to balance traffic across your diverse physical architecture without losing any data, which two key characteristics should you look for in your selected Event Driven Integration platform?

**Choices:**

- Dynamic Routing: move events across multiple hops/brokers to its destinations
- Shock Absorption: dealing with producer/consumer speed mismatch
- Store and Forward: dealing with consumers being offline
- Hierarchical Topics: ability to dynamically construct destinations from variables, and leverage wild cards for subscription
- Horizontal Scalability: scale to any geography

**Selected answers:** Shock Absorption; Store and Forward.

**Rationale:** Shock absorption handles speed differences among systems, while store-and-forward retains data for consumers that are offline. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 10 of 18 — Single choice

**Question:** Demultiplexing refers to a scenario where you want to split a given data stream into smaller purpose-specific ones. In an Event Mesh you can achieve that leveraging wild cards. You are designing an Order Processing system for your widget franchise. As orders come in you need to route them to the various state and city processing services to account for tax calculations and respective regional discounts. You leverage the hierarchical topic structure of the Event Mesh platform for that. The structure of the topic is as follows: `order/process/{state/province}/{city}/{store}/{department}/{productid}`. What would the subscription string look like to handle all orders in Illinois, for all stores beginning with kmt?

**Choices:**

- `order/process/IL*/*/*/*`
- `order/process/IL/*/kmt*/>`
- `order/process/IL/*/kmt>/*/*`
- `Order/process/*/Chicago/*/*/*`

**Selected answer:** `order/process/IL/*/kmt*/>`.

**Rationale:** This selects Illinois, any city, store names with the requested prefix, and all remaining department/product levels. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 11 of 18 — Single choice

**Question:** Multiplexing refers to the scenarios where you need to “unify multiple” sources of data into a single one; this is typically done to support broader real time event analysis. You need to ensure that the aggregate stream is persistent, so that analytics can run off the stream. What is the best way to multiple different data streams?

**Choices:**

- Bridge incoming topics to a single topic.
- Map topics to a queue.
- Use variable in the topic names and each stream can replace the variables as desired.
- Use wildcards.

**Selected answer:** Map topics to a queue.

**Rationale:** The course states Solace supports Mux by mapping multiple topics to a queue; queue persistence supports downstream analytics. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 12 of 18 — Single choice

**Question:** You work with a global CPG corporation. You need to change the price of one of the products and propagate that price instantly to all stores around the world. What is the best way to accomplish this?

**Choices:**

- Use an Event Mesh that spans all the regions and all the stores in one seamless fabric. A price change event issued at the corporate headquarters will be routed directly to all interested parties around the world in real time.
- Each designated region has its stores connected by an eventing platform. These eventing platforms are interconnected via fixed network connections. A price change event issued at the corporate headquarters will propagate across these private links into the respective regional eventing platforms and from there to all the interconnected stores.
- Each country and store have a set of REST APIs that accept changes to the price of the products in the inventory. The corporate headquarters orchestrates a call to all of the globally exposed APIs to trigger the price change.

**Selected answer:** Use an Event Mesh that spans all regions and stores as one seamless fabric.

**Rationale:** This matches the course's global price-distribution example: publish the corporate price-change event once and route it to interested regional consumers. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 13 of 18 — Choose 3

**Question:** You are planning to build an Event Driven Architecture that leverages an Event Mesh at its core. As a good design pattern, decoupled micro-integrations that communicate with each other via the Event Mesh, is the best option. What are three key benefits of decoupling?

**Choices:**

- better agility
- better scalability
- better error management
- better observability
- better transaction management

**Selected answers:** better agility; better scalability; better error management.

**Rationale:** The course connects decoupling to adding consumers without downtime, independently scaling nodes, and isolating faults or delays from other flows. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 14 of 18 — Choose 2

**Question:** You are trying to design an integration that allows you to extract data from a Postgres DB and move it to a MySQL DB or SalesForce based on the data in the extracted record. You built your integration using three connectors (one for each data source or destination), a router component, and three transformers. What are two best deployment options for this integration application?

**Choices:**

- Deploy the entire packaged asset in the same cloud instance as the source (Postgres DB).
- Deploy the entire packaged asset in the same cloud as the destination MysqlDB.
- Decompose the integration application into its functional components: (Postgres DB, SalesForce, MySQL) each one with its own transformer, plus the router component, and deploy thus 4 separate assets, using the Event Mesh in the middle as a conduit.
- Decompose the integration application into its functional components: (Postgres DB, SalesForce, MySQL), 3 transformers, plus the router component, and deploy 7 separate assets, using the Event Mesh in the middle as a conduit.

**Selected answers:** Deploy the entire packaged asset in the same cloud instance as the source (Postgres DB); decompose into four functional assets and use the Event Mesh as conduit.

**Rationale:** Co-locating the packaged integration with its source limits source-side network distance; decomposition into source/destination edge integrations with the Event Mesh in the middle aligns with the course's micro-integration design and avoids unnecessary seven-way fragmentation. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 15 of 18 — Choose 2

**Question:** What are two common challenges with handling errors in a distributed architecture?

**Choices:**

- Monitoring and logging are not centralized and hard to correlate.
- There is no impact analysis to the up and downstream services.
- The error is handled locally (in isolation) without broader context or impact assessment.
- There is no common infrastructure to propagate the error “globally”.

**Selected answers:** Monitoring and logging are not centralized and hard to correlate; the error is handled locally in isolation without broader context or impact assessment.

**Rationale:** Distributed errors span systems and geographies, making correlation and broader impact assessment difficult; the course proposes coordinated Resolution Centers over the Event Mesh. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 16 of 18 — Single choice

**Question:** MuleSoft pioneered the integration approach known as API Led Connectivity. In the API Led architecture there are three layers: system, process, experience. These layers also apply to Event APIs. Which definitions describes these types of Events?

**Choices:**

- System Events: Relate to data access or data extraction from data source systems. Process Events: Relate to aggregate data i.e. Customer 360/Product360 OR events that are part of a business process choreography. Experience Events: Relate to Notifications or Alerts sent to customers directly.
- System Events: Relate to querying Databases. Process Events: Relate to choreographing business processes. Experience Events: Relate to mobile applications.
- System Events: Relate to business system data changes. Process Events: Relate orchestrating business process events. Experience Events: Relate to Web applications.
- System Events: Relate to file system access. Process Events: Relate to business process management events. Experience Events: Relate to customer describing their experience on a Web/Mobile app.

**Selected answer:** System Events cover data access/extraction; Process Events aggregate data or participate in business-process choreography; Experience Events provide customer-facing notifications or alerts.

**Rationale:** This option maps the three layers to source-system data, cross-system business processes, and customer-facing experience events. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 17 of 18 — Single choice

**Question:** Event Storming is a methodology for designing event driven applications. In Event Storming there are three types of events: Domain events, Aggregate events, Command events. How do the Event Storming event categories align with the API Led definitions?

**Choices:**

- System = Domain; Process = Aggregate; Experience = Command
- System = Aggregate; Process = Command; Experience = Domain
- System = Command; Process = Aggregate; Experience = Domain
- System = Domain; Process = Command; Experience = Aggregate

**Selected answer:** System = Domain; Process = Aggregate; Experience = Command.

**Rationale:** Domain events originate from systems, aggregate events reflect process-level aggregation, and commands map to experience-level requests. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

### Question 18 of 18 — Single choice

**Question:** Which technologies are used to implement the Event API Lifecycle steps?

**Choices:**

- Design = MuleSoft Event Portal Plugin, Build = Git Workflow plugin, Deploy = Solace Event Portal
- Design = Solace Event Portal, Build = MuleSoft Event Portal Plugin, Deploy = Git Workflow plugin
- Design = MuleSoft Event Portal Plugin, Build = Solace Event Portal, Deploy = Git Workflow plugin
- Design = MuleSoft API designer, build = MuleSoft Studio, deploy = MuleSoft Anypoint Platform

**Selected answer:** Design = Solace Event Portal, Build = MuleSoft Event Portal Plugin, Deploy = Git Workflow plugin.

**Rationale:** Solace Event Portal is the design/governance environment described in the course; the MuleSoft plugin supports event API implementation, with the Git workflow used for deployment/configuration. No item-level correctness feedback was shown; the final Academy grade and pass are recorded below.

## Submission status

All 18 required questions have an answer selected. The test has not yet been submitted; score and Academy feedback are pending.

