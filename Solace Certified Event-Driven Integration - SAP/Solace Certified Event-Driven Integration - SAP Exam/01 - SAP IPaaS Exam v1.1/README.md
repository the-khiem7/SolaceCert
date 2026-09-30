---
title: SAP IPaaS Exam v1.1
document_type: lesson
source: Solace Academy
learning_path: Solace Certified Event-Driven Integration - SAP
course: Solace Certified Event-Driven Integration - SAP Exam
lesson_order: 1
---

# SAP IPaaS Exam v1.1

## Live attempt record

The Academy presents a one-page, 25-question assessment. The question and every displayed choice below were captured before any answer was selected. The course lesson remains incomplete until the platform confirms a submitted result. No instructional image or other downloadable visual was exposed on this assessment screen, so `img/` intentionally contains no asset.

## Questions and candidate selections

Candidate selections are study notes derived from the completed prerequisite course; they are not Academy-confirmed answers until the submitted assessment feedback is recorded.

1. **Enterprise Event-Driven Infrastructure:** across cloud, modern on-premises Linux, and legacy mainframe/OS390/VMS/VSAM environments, which two characteristics balance traffic without data loss? *(Choose 2.)* Choices: Shock Absorption: dealing with producer/consumer speed mismatch; Store and Forward: dealing with consumers being offline; Horizontal Scalability: scale to any geography; Dynamic Routing: move events across multiple hops/brokers to its destinations; Hierarchical Topics: ability to dynamically construct destinations from variables and leverage wildcards for subscription. Candidate: **Shock Absorption** and **Store and Forward**.
2. **Benefits of decoupling micro-integrations:** better scalability; better agility; better error management; better observability; better transaction management. *(Choose 3.)* Candidate: **better scalability**, **better agility**, and **better error management**.
3. **Unique Event Mesh properties:** dynamic routing and filtering; protocol bridging; authentication and authorization; support for pub-sub as an event exchange pattern. *(Choose 2.)* Candidate: **dynamic routing and filtering** and **protocol bridging**.
4. **Postgres-to-MySQL-or-Salesforce integration deployment:** deploy the entire packaged asset in the same cloud instance as the source (Postgres DB); deploy the entire packaged asset in the same cloud as the destination MysqlDB; decompose into Postgres DB, SalesForce, MySQL, each with its own transformer plus router, and deploy four separate assets using Event Mesh as conduit; decompose into Postgres DB, SalesForce, MySQL, three transformers plus router, and deploy seven separate assets using Event Mesh as conduit. *(Choose 2.)* Candidate: **deploy beside the source** and **decompose into seven assets**.
5. **MQTT engine events to an IBM MQ-fronted ERP:** write a microservice that subscribes to MQTT and publishes to IBM MQ; route through two microservices via TIBCO EMS; use Event Mesh to bridge all protocols into one unified messaging fabric; bridge protocols and replace Hive MQ with a Solace Broker. *(Choose 2.)* Candidate: **direct MQTT-to-IBM-MQ microservice** and **Event Mesh protocol bridging**.
6. **Other Solace scaling forms:** partitioned queues for vertical consumer scaling; load balancer clustering; broker clustering for horizontal scaling; partition scaling. *(Choose 2.)* Candidate: **partitioned queues for vertical consumer scaling** and **broker clustering for horizontal scaling**.
7. **REST-only Customer 360 API problems:** core-process timeout from many distant calls; risky coupling when one API call changes; difficult scaling of Customer 360 and dependent APIs; deep calls create brittle timeout-prone architecture; inability to place load balancers at all levels. *(Choose 3.)* Candidate: **timeout from distant orchestration**, **coupling risk**, and **scaling challenge**.
8. **Distributed-architecture error handling challenges:** no common infrastructure to propagate errors globally; errors handled locally without broader context/impact assessment; monitoring/logging not centralized and hard to correlate; no impact analysis for upstream/downstream services. *(Choose 2.)* Candidate: **no global error-propagation infrastructure** and **no upstream/downstream impact analysis**.
9. **Multiplexing persistent aggregate streams:** map topics to a queue; use variables in topic names; use wildcards; bridge incoming topics to a single topic. Candidate: **Map topics to a queue**.
10. **Illinois orders for stores beginning `kmt`:** `order/process/IL*/*/*/*`; `order/process/IL/*/kmt*/>`; `order/process/IL/*/kmt>/*/*`; `Order/process/*/Chicago/*/*/*`. Candidate: **`order/process/IL/*/kmt*/>`**.
11. **Less risky Customer 360 approach:** RESTful Customer 360 API orchestrating all segment APIs; Event Mesh map-reduce requests to profile-segment holders and aggregate before presentation; the same Event Mesh approach with every profile holder exposed by REST APIs. Candidate: **Event Mesh map-reduce with aggregation**.
12. **Stateful choreography:** every service is state-aware and updates a database; every service calls an API fronting storage; every service sends an event to an Event API to update state remotely; topic hierarchy contains a state-signal segment. Candidate: **send an event to an Event API to update state remotely**.
13. **Order fulfillment sync/async design:** orchestrate everything with REST; capture initial order with REST, then event-platform choreography and external REST API state service; capture initial order with REST then Event Mesh with state monitoring; capture initial order with REST, event-platform choreography, and external Event API state service. Candidate: **REST intake, event choreography, and external Event API state management**.
14. **Event Portal purpose in SAP Integration Suite:** monitor performance; define and store application objects, events, and schemas; manage user access control. Candidate: **define and store application objects, events, and schemas**.
15. **Event Portal application analogy:** server instance; iFlow or integration object; database schema. Candidate: **an iFlow or integration object**.
16. **Generated Event Portal code upload target:** GitHub repository; local file system; SAP Integration Suite. Candidate: **SAP Integration Suite**.
17. **Generated-iFlow validation maps:** encrypt sensitive data; catch errors associated with input; route messages to different systems. Candidate: **catch input errors**.
18. **Compose-topic property:** define user access levels; define the event topic including dynamic elements; specify transformation rules. Candidate: **define the topic including dynamic elements**.
19. **Set dynamic topic properties in generated iFlow:** only hardcoded values; from JSON-payload elements or explicitly as a constant; only external configuration files. Candidate: **JSON-payload elements or a constant**.
20. **Solace Cloud Console Try Me tab:** monitor CPU; configure and test broker connectivity; manage user accounts. Candidate: **configure and test broker connectivity**.
21. **First code-generation step for SAP IRS integrator:** configure broker; obtain Event Portal token; define schemas. Candidate: **obtain an Event Portal token**.
22. **Generated-iFlow preconfigured consumption adapter:** HTTP; Event Mesh; OData. Candidate: **Event Mesh adapter**.
23. **Stub maps in Generate Shipment Event translations:** add complex translations; delete stub map and translate in one place; translate multiple times. Candidate: **delete stub map and translate in one place**.
24. **Publish events in generated iFlow:** directly to a queue; to a topic; to a database. Candidate: **publish to a topic**.
25. **Compose-topic script purpose:** define transformation rules; create complete topic string including dynamic elements; validate message content. Candidate: **create complete topic string including dynamic elements**.

## Completion evidence

Pending Academy submission and visible result. The prerequisite SAP integration course is already Academy-confirmed complete and is the basis of the candidate selections recorded here.
