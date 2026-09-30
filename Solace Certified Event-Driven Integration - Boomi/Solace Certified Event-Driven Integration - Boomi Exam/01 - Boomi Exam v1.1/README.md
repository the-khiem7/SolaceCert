---
title: Boomi Exam v1.1
document_type: lesson
source: Solace Academy
learning_path: Solace Certified Event-Driven Integration - Boomi
course: Solace Certified Event-Driven Integration - Boomi Exam
lesson_order: 1
---

# Boomi Exam v1.1

Source: [Solace Academy](https://training.solace.com/learn/learning-plans/94/solace-certified-event-driven-integration-boomi/courses/596/solace-certified-event-driven-integration-boomi-exam/lessons/4353/boomi-exam-v11)

## Exam state

- Academy status: **completed**; 21 questions submitted.
- Started: 2026-09-30.
- Visuals: no instructional visual was exposed on the current exam screen; the screen consisted of question text, choices, timer, and pagination.

## Academy-confirmed result

- Completion message: **Well done, you have completed the course!**
- Final grade: **71**.
- Certificate: **You earned the course certificate**.
- Certification: **You earned the certification: Solace Certified Event Driven Integration - Boomi**.
- Learning plan: **Learning plan completed — 3 of 3 courses completed**.

## Questions and confirmed answers

### Question 1 of 21

**Question:** What is one of the benefits of using the "Automatically Manage Solace Queues" feature in Boomi?

**Choices:**

- It optimises network latency
- It creates queues and sets configurations in Solace

**Selected answer:** It creates queues and sets configurations in Solace.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 2 of 21

**Question:** What event integration is demonstrated using Boomi in the demo?

**Choices:**

- Data warehousing
- Order fulfilment

**Selected answer:** Order fulfilment.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 3 of 21

**Question:** You work with a global CPG corporation. You need to change the price of one of the products and propagate that price instantly to all stores around the world. What is the best way to accomplish this?

**Choices:**

- Each country and store have a set of REST APIs that accept changes to the price of the products in the inventory. The corporate headquarters orchestrates a call to all of the globally exposed APIs to trigger the price change.
- Each designated region has its stores connected by an eventing platform. These eventing platforms are interconnected via fixed network connections. A price change event issued at the corporate headquarters will propagate across these private links into the respective regional eventing platforms and from there to all the interconnected stores.
- Use an Event Mesh that spans all the regions and all the stores in one seamless fabric. A price change event issued at the corporate headquarters will be routed directly to all interested parties around the world in real time.

**Selected answer:** Use an Event Mesh that spans all the regions and all the stores in one seamless fabric. A price change event issued at the corporate headquarters will be routed directly to all interested parties around the world in real time.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 4 of 21

**Question:** You work in a truck manufacturing company and part of your predictive maintenance strategy is to have real time insight into how the engines on the road are performing. That means that the sensors on the engines will emit events that you need to collect and analyze in real time. Sensors communicate via MQTT. In your enterprise environment you have three types of messaging platforms: IBM MQ for integration to legacy systems; TIBCO EMS for general enterprise-wide event driven integrations; Hive MQ (MQTT) for IoT purposes. You have an Event Mesh at your disposal, so you can use this in your design. What are the two best ways to have engine events make their way into the legacy ERP fronted by IBM MQ? (Choose 2)

**Choices:**

- Write a microservice that subscribes to MQTT events and publishes the event to IBM MQ.
- Use the Event Mesh and bridge all protocols into one unified messaging fabric.
- Use the Event Mesh and bridge all protocols into one unified messaging fabric and replace the Hive MQ Broker with a Solace Broker.
- Write a microservice that subscribes to MQTT events and publishes the event to TIBCO EMS. Write a second microservice that subscribes to TIBCO EMS and then re-publishes the event to IBM MQ.

**Selected answers:** Write a microservice that subscribes to MQTT events and publishes the event to IBM MQ; and use the Event Mesh and bridge all protocols into one unified messaging fabric.

**Confirmation:** Both choices were selected on the live Academy exam before advancing.


### Question 5 of 21

**Question:** Event Storming is a methodology for designing event driven applications. In Event Storming there are three types of events: Domain events, Aggregate events, and Command events. How do the Event Storming event categories align with the API Led definitions?

**Choices:**

- System = Aggregate; Process = Command; Experience = Domain
- System = Command; Process = Aggregate; Experience = Domain
- System = Domain; Process = Aggregate; Experience = Command
- System = Domain; Process = Command; Experience = Aggregate

**Selected answer:** System = Aggregate; Process = Command; Experience = Domain.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 6 of 21

**Question:** Multiplexing refers to the scenarios where you need to “unify multiple” sources of data into a single one; this is typically done to support broader real time event analysis. You need to ensure that the aggregate stream is persistent, so that analytics can run off the stream. What is the best way to multiple different data streams?

**Choices:**

- Use variable in the topic names and each stream can replace the variables as desired.
- Use wildcards.
- Map topics to a queue.
- Bridge incoming topics to a single topic.

**Selected answer:** Map topics to a queue.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 7 of 21

**Question:** What is the purpose of the email notification sent by the shipping service at the end of the process?

**Choices:**

- To update the customer's address
- To confirm that the order was shipped

**Selected answer:** To confirm that the order was shipped.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 8 of 21

**Question:** You are adding an Event Mesh to your distributed architecture. What are two of the unique Event Mesh properties? (Choose 2)

**Choices:**

- protocol bridging
- support for pub-sub as an event exchange pattern
- authentication and authorization
- dynamic routing and filtering

**Selected answers:** protocol bridging; dynamic routing and filtering.

**Confirmation:** Both choices were selected on the live Academy exam before advancing.


### Question 9 of 21

**Question:** You are trying to design an integration that allows you to extract data from a Postgres DB and move it to a MySQL DB or SalesForce based on the data in the extracted record. You built your integration using three connectors (one for each data source or destination), a router component, and three transformers. What are two best deployment options for this integration application? (Choose 2)

**Choices:**

- Decompose the integration application into its functional components: (Postgres DB, SalesForce, MySQL), 3 transformers, plus the router component, and deploy 7 separate assets, using the Event Mesh in the middle as a conduit
- Deploy the entire packaged asset in the same cloud as the destination MysqlDB
- Decompose the integration application into its functional components: (Postgres DB, SalesForce, MySQL) each one with its own transformer, plus the router component, and deploy thus 4 separate assets, using the Event Mesh in the middle as a conduit
- Deploy the entire packaged asset in the same cloud instance as the source (Postgres DB)

**Selected answers:** Deploy the entire packaged asset in the same cloud as the destination MysqlDB; and deploy the entire packaged asset in the same cloud instance as the source (Postgres DB).

**Confirmation:** Both choices were selected on the live Academy exam before advancing.


### Question 10 of 21

**Question:** You are planning an Event Driven Infrastructure in your enterprise. The applications and systems across your enterprise are on different networks and installed on hardware platforms with different processing abilities. These systems are spread across an ecosystem that includes cloud-based, on-premises modern (Linux-based installs), and on-premises legacy environments (mainframes OS390s/VMS/VSAM). The business cannot lose data as it will impact the customer experience and can lead to loss of revenue. You have the Event Mesh at your disposal. Given that you need to balance traffic across your diverse physical architecture without losing any data, which two key characteristics should you look for in your selected Event Driven Integration platform? (Choose 2)

**Choices:**

- Shock Absorption: dealing with producer/consumer speed mismatch
- Store and Forward: dealing with consumers being offline
- Dynamic Routing: move events across multiple hops/brokers to its destinations
- Horizontal Scalability: scale to any geography
- Hierarchical Topics: ability to dynamically construct destinations from variables, and leverage wild cards for subscription

**Selected answers:** Shock Absorption: dealing with producer/consumer speed mismatch; and Store and Forward: dealing with consumers being offline.

**Confirmation:** Both choices were selected on the live Academy exam before advancing.


### Question 11 of 21

**Question:** What are two common challenges with handling errors in a distributed architecture? (Choose 2)

**Choices:**

- There is no impact analysis to the up and downstream services.
- There is no common infrastructure to propagate the error “globally”
- Monitoring and logging are not centralized and hard to correlate.
- The error is handled locally (in isolation) without broader context or impact assessment

**Selected answers:** Monitoring and logging are not centralized and hard to correlate; and the error is handled locally (in isolation) without broader context or impact assessment.

**Confirmation:** Both choices were selected on the live Academy exam before advancing.


### Question 12 of 21

**Question:** Orchestrations can maintain the state of a transaction because they are centrally managed, and every state change (step) in the orchestration can be tracked. In a choreography, due to its “decentralized” nature, state management is challenging. The Event Mesh is the core platform over which choreography is executed in this case. What you need to do?

**Choices:**

- Every service in the choreography needs to be “state aware” and update the state into a database.
- Every service in the choreography needs to be “state aware” and update the state by calling an API, which can front end any type of storage mechanism.
- Every service in the choreography needs to be “state aware” and update the by sending an Event to an Event API to update the state in a remote system.
- The Event Mesh can use variables in the definition of a topic hierarchy. One of the segments in the hierarchy can contains a state signal.

**Selected answer:** The Event Mesh can use variables in the definition of a topic hierarchy. One of the segments in the hierarchy can contains a state signal.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 13 of 21

**Question:** You are designing an Order Fulfillment architecture. You are considering how to use synchronous and asynchronous patterns of integration in your design. The Event Mesh is one of the considerations. Which is the best option?

**Choices:**

- Use REST APIs to capture the initial order, but use an event platform to choreograph the other fulfillment steps. Manage state external through an Event API based service.
- Orchestrate the entire process using REST APIs.
- Use REST APIs to capture the initial order, but use an event platform to choreograph the other fulfillment steps. Manage state external through a REST API based service.
- Use REST APIs to capture the initial order, but use an Event Mesh with state monitoring capabilities to choreograph the other fulfillment steps.

**Selected answer:** Use REST APIs to capture the initial order, but use an event platform to choreograph the other fulfillment steps. Manage state external through an Event API based service.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 14 of 21

**Question:** What functionality does Boomi provide for API management and cataloging, as seen in the demo?

**Choices:**

- Machinery for API management and cataloging
- Automated threat detection

**Selected answer:** Machinery for API management and cataloging.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 15 of 21

**Question:** Demultiplexing refers to a scenario where you want to split a given data stream into smaller purpose-specific ones. In an Event Mesh you can achieve that leveraging wild cards. You are designing an Order Processing system for your widget franchise. As orders come in you need to route them to the various state and city processing services to account for tax calculations and respective regional discounts. You leverage the hierarchical topic structure of the Event Mesh platform for that. The structure of the topic is as follows: `order/process/{state/province}/{city}/{store}/{department}/{productid}`. What would the subscription string look like to handle all orders in Illinois, for all stores beginning with kmt?

**Choices:**

- `order/process/IL/*/kmt>/*/*`
- `order/process/IL*/*/*/*`
- `Order/process/*/Chicago/*/*/*`
- `order/process/IL/*/kmt*/>`

**Selected answer:** `order/process/IL/*/kmt*/>`.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 16 of 21

**Question:** What is the role of local variables within the Boomi processes in the demo?

**Choices:**

- To define global constants
- To manipulate topics and perform logic

**Selected answer:** To manipulate topics and perform logic.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 17 of 21

**Question:** In the context of importing topic subscriptions, how are wildcards represented initially when imported from the event portal?

**Choices:**

- Percentage signs
- Squiggly lines indicating regionality

**Selected answer:** Percentage signs.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 18 of 21

**Question:** A bank needs to be able to get a complete view of your customer data (Customer 360), however most of the systems containing the various parts of the Customer profile are dispersed across different data centers and geographies. What is the less risky way to accomplish this?

**Choices:**

- Use an Event Mesh to implement a Map Reduce paradigm whereby you request responses from each “Profile Segment” holder system, and aggregate the response before presentation with every Profile Segment holder system exposed by REST APIs.
- Use an Event Mesh to implement a Map Reduce paradigm whereby you request responses from each “Profile Segment” holder system, and aggregate the response before presentation.
- Create a REST-full Customer 360 API that orchestrates the API calls to all the other “segment” APIS.

**Selected answer:** Use an Event Mesh to implement a Map Reduce paradigm whereby you request responses from each “Profile Segment” holder system, and aggregate the response before presentation.

**Confirmation:** The choice was selected on the live Academy exam before advancing.


### Question 19 of 21

**Question:** The Event Mesh is the highest level of scaling for the Solace platform. Which two other forms of scaling are part of the Solace platform? (Choose 2)

**Choices:**

- load balancer clustering
- partitioned queues for vertical consumer scaling
- partition scaling
- broker clustering for horizontal scaling

**Selected answers:** partitioned queues for vertical consumer scaling; and broker clustering for horizontal scaling.

**Confirmation:** Both choices were selected on the live Academy exam before advancing.


### Question 20 of 21

**Question:** You are planning to build an Event Driven Architecture that leverages an Event Mesh at its core. As a good design pattern, decoupled micro-integrations that communicate with each other via the Event Mesh, is the best option. What are three key benefits of decoupling? (Choose 3)

**Choices:**

- better error management
- better scalability
- better observability
- better transaction management
- better agility

**Selected answers:** better error management; better scalability; and better agility.

**Confirmation:** All three choices were selected on the live Academy exam before advancing.


### Question 21 of 21

**Question:** A bank needs to be able to get a complete view of your customer data (Customer 360). However, most of the systems containing the various parts of the Customer profile are dispersed across different data centers and geographies. The bank only uses REST APIs to expose data from internal systems, so the Customer 360 API needs to orchestrate calls to all remote systems, aggregate the data, and present it to user. Which three problems will this implementation pose? (Choose 3)

**Choices:**

- If the API calls are deep, this makes the architecture brittle and will lead to the risk of timeout.
- You cannot place load balancers at all levels.
- Scaling the Customer 360 API and the dependent APIs will be challenging.
- Changes to one of the API calls in the core orchestration API can be risky as it can impact all the other API calls in the orchestration (due to coupling).
- The Core Process API (Customer 360) can time out if there are too many remote calls to be orchestrated, and the “Segment” data APIs are geographically distant.

**Selected answers:** If the API calls are deep, this makes the architecture brittle and will lead to the risk of timeout; scaling the Customer 360 API and the dependent APIs will be challenging; and changes to one of the API calls in the core orchestration API can be risky as it can impact all the other API calls in the orchestration (due to coupling).

**Confirmation:** All three choices were selected on the live Academy exam before submission.

