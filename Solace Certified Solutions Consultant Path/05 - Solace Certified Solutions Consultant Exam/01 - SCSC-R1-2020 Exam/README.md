---
title: SCSC-R1-2020 Exam
document_type: lesson
source: Solace Academy
learning_path: Solace Certified Solutions Consultant Path
course: Solace Certified Solutions Consultant Exam
lesson_order: 1
---

# SCSC-R1-2020 Exam

Academy status: completed on 2026-09-30. Academy visibly confirmed a final grade of **84.1**, a course certificate, and the **Solace Certified Solutions Consultant Certification**. The answer record below preserves submitted selections; individual-item feedback was not displayed.

## Questions 1–12

1. **Which component of the Event Portal would be used when trying to analyze events running over your event brokers in real-time in an existing solution?** Options: Event Designer; Event Mesh; Event Catalog; Event Discovery. Selected: **Event Discovery**.
2. **Which Solace product can developer/administrators use to deploy Event Brokers in public cloud or private cloud without manually installing, managing, or upgrading the broker?** Options: PubSub+ Manager; PubSub+ Monitor; PubSub+ CLI; PubSub+ Cloud Console. Selected: **PubSub+ Cloud Console**.
3. **When deploying PubSub+ Event Broker: Software in high availability, what is the function of the third Monitor node?** Options: replication/disaster-recovery capability; voting node to avoid split brain between Primary and Backup; replicate messages and their state; operational monitoring. Selected: **act as the voting node and avoid a split-brain situation between Primary and Backup**.
4. **Which format of the Solace PubSub+ broker is best for highest performance and lowest latency?** Options: PubSub+ Software; PubSub+ Event Portal; PubSub+ As a Service; PubSub+ Appliance. Selected: **PubSub+ Appliance**.
5. **Which component of the Event Portal would architects use when defining and visualizing a new application that will be developed?** Options: Event Mesh; Event Discovery; Event Designer; Event Catalog. Selected: **Event Designer**.
6. **What are the key benefits of using an event-driven solution? (Choose two)** Options: sent in batches; real-time; polling; asynchronous. Selected: **real-time; asynchronous**.
7. **What are some key features of the Cloud Console? (Choose three)** Options: Create and view Existing Service; Build an Event Mesh; Administer User accounts; Configure a new message VPN. Selected: **Create and view Existing Service; Build an Event Mesh; Administer User accounts**.
8. **Which type of the Event Channel allows one-to-one communication?** Options: Topics; Events; Point-to-Point; Queues. Selected: **Point-to-Point**.
9. **Which Solace product collects and reports critical broker metrics and events so you can detect issues before they impact end-users?** Options: PubSub+ Cloud Console; PubSub+ Manager; PubSub+ Monitor; PubSub+ Event Portal. Selected: **PubSub+ Monitor**.
10. **What are the 3 steps to become Event-Driven? (Choose three)** Options: Alert & Inform; Liberate Your Data; Pilot Selection; Modernize Your Platform. Selected: **Liberate Your Data; Pilot Selection; Modernize Your Platform**.
11. **Which quality of service is used when the receiving application cannot tolerate any message loss?** Options: Instant Delivery; Direct Delivery; Indirect Delivery; Guaranteed Delivery. Selected: **Guaranteed Delivery**.
12. **What are the four main foundational elements of the Event Portal? (Choose four)** Options: Application Domain; Event Broker; Schema; Event; Application; AsyncAPI. Selected: **Application Domain; Schema; Event; Application**.
13. **If an enterprise exceeded its client connection capacity on a single event broker and wants to increase the limit, what is required?** Options: limit connections; horizontally scale with more event brokers in a DMR cluster; contact support; vertically scale by adding resources. Selected: **vertical scaling by adding more resources to the event broker**.
14. **Which statement about Queue and Topic destinations is true?** Options: both must be administratively created; queues must be created administratively or programmatically by clients before publish/subscribe; topics must be administratively created; neither needs creation. Selected: **Queues need to be created administratively or programmatically by clients before publishing/subscribing**.
15. **Which type of Event Channel allows one-to-many communication?** Options: Topics; Point-to-Point; Queues; Events. Selected: **Topics**.
16. **A client application with topic subscription `news/*/nort*` would receive messages published to which topic?** Options: `news/hockey`; `news/hockey/europe`; `news/hockey/northamerica`; `news/hockey/northamerica/nhl`. Selected: **`news/hockey/northamerica`**.
17. **What are the three runtime deployment formats of the Event Broker? (Choose three)** Options: PubSub+ As a Service; PubSub+ Software; PubSub+ Appliance; PubSub+ Event Portal. Selected: **PubSub+ As a Service; PubSub+ Software; PubSub+ Appliance**.
18. **Which component of Event Portal gives access to all applications, events, and schemas created in Event Portal?** Options: Event Catalog; Event Designer; Event Mesh; Event Discovery. Selected: **Event Catalog**.
19. **Which statement best describes a characteristic of a queue?** Options: persistence but messages lost on broker/consumer crash; acknowledgement before persistence; persistence and messages not lost on broker/consumer crash; events removed when sent. Selected: **provides persistence for events and they are not lost if the broker or consumer crashes**.
20. **What APIs or protocols are available for developers to connect applications for messaging on PubSub+ Event Brokers? (Choose three)** Options: SEMP; REST; AMQP; MQTT; SSH. Selected: **REST; AMQP; MQTT**.

## Visual availability

No instructional visual was available in this assessment. Question 11 and question 12 content was visually inspected because the accessibility tree omitted their labels; the visual was not retained as an instructional asset.

## Questions 21–40

21. **Event Portal benefits (select all).** Options: prevents sharing/reuse; single place to design/create/discover/share/secure/manage events; eliminates spreadsheet cataloging; visualizes event flows and application linkages. Selected: **the last three options**.
22. **Valid subscription for `news/sports/hockey/chicagoblackhawks`.** Options: exact topic with different capitalization; `news/sports/*hockey/>`; `news/sports/>/*`; `news/sports/>`. Selected: **`news/sports/>`**.
23. **Difference between a message and an event.** Options included no difference and technical-format claims. Selected: **events can be visible to a business, whereas messages are visible at the transport level between applications and messaging systems**.
24. **Topics that subscribe consumers to multiple topics (choose two).** Options: `acme/driver/status`; `acme/>`; `acme/rides/accepted`; `acme/rides/*`. Selected: **`acme/>`; `acme/rides/*`**.
25. **Requirement for publish-subscribe with guaranteed messaging.** Options: create a queue; apply subscription to client; create durable topic; create a queue with a topic subscription. Selected: **a queue with a topic subscription added to it**.
26. **Benefit of Dynamic Message Routing.** Options: replay from a time; HA; payload-based routing; publisher decoupling from interested consumers and their mesh location. Selected: **publisher decoupling from interested consumers and their event-mesh location**.
27. **Roles benefiting most from Event Portal (choose three).** Options: Data Scientists; Developers; Architects; Middleware teams. Selected: **Developers; Architects; Middleware teams**.
28. **Term for an application that sends and receives an event.** Options: Topics; Queue; Message VPN; Client. Selected: **Client**.
29. **Types of Event Channels (choose two).** Options: Events; Messages; Queues; Topics. Selected: **Queues; Topics**.
30. **Browser-based Solace product for horizontal scaling, Replay, and message-VPN management.** Options: PubSub+ Manager; PubSub+ Cloud Console; PubSub+ Monitor; PubSub+ Event Portal. Selected: **PubSub+ Manager**.
31. **Product to prime applications with historical broker data.** Options: Message Replay; PubSub+ Cache; PubSub+ Manager; Event Portal. Selected: **Message Replay**.
32. **Quality of service for extremely high rate when a consumer can tolerate some loss.** Options: Instant; Guaranteed; Indirect; Direct Delivery. Selected: **Direct Delivery**.
33. **Feature that replicates messages between active and standby brokers and fails over in 30 seconds or less.** Options: Disaster Recovery; High Availability; Dynamic Message Routing; Message Replay. Selected: **High Availability**.
34. **Deployment option flexible for any cloud or on-premises.** Options: Appliance; Software; As a Service; Event Portal. Selected: **PubSub+ Software**.
35. **Subscription matching `NYC1/P01/order/buy`.** Options: `*/p01/*/buy`; `NYC1/P01/*`; `NYC1/*01/order/>`; `*/*/*/buy`. Selected: **`*/*/*/buy`**.
36. **Where events are added when Message Replay is enabled.** Options: queue and replay log; Replay Log; queue; Cache. Selected: **Replay Log**.
37. **What PubSub+ Event Portal can do (select all).** Options: create an event mesh across clouds; collaborate on an event-driven architecture; discover events dynamically from event mesh; design and visualize events, applications, and schemas. Selected: **collaborate; discover events dynamically; design and visualize**.
38. **Event Portal benefits for a Chief Data Officer/Data Governance team (choose two).** Options: ensures privacy-law compliance; use relationships to create security policies and validate schema compliance; understand data lineage. Selected: **relationships/security-policy and schema validation; data lineage**.
39. **Topic-structure best practice.** Options: `ACC/NA/Canada/Ontario/CrossOver`; `acc/na/canada/on/cross_over`; `na/Canada/on/co`; `acmeconnectedcars/northamerica/canada/ontario/crossover`. Selected: **`acmeconnectedcars/northamerica/canada/ontario/crossover`**.
40. **Qualities of Service in PubSub+ Event Brokers (choose two).** Options: Guaranteed Delivery; Instant Delivery; Indirect Delivery; Direct Delivery. Selected: **Guaranteed Delivery; Direct Delivery**.

## Result status

The Academy confirmed completion after submission: final grade **84.1**, course certificate earned, and the Solace Certified Solutions Consultant Certification earned. Individual correct/incorrect feedback was not displayed.
