---
title: "SCEDAP Exam v2.0-Feb2025"
document_type: lesson
learning_path: "Solace Certified EDA Practitioner Path"
course: "Solace Certified Event-Driven Architecture Practitioner Exam"
lesson_order: 2
source: Solace Academy
---

# SCEDAP Exam v2.0-Feb2025

## Academy state

On 2026-09-29 the live Academy page presented a timed, required 28-question test on one page. The initial screen showed 1 hour 28 minutes 51 seconds remaining and 3 of 3 attempts available. The exam is part of the second mandatory course in the Solace Certified EDA Practitioner Path. Questions and choices below are transcribed from the live page, and the selected answers from the submitted attempt are recorded. Academy displayed the final result and completion details below.

## Question 1 of 28

**Question:** Which of these is not a benefit of Event Driven Architecture?

**Choices:**

- Centralized data consistency
- Real-time data processing and analytics
- Improved scalability and resilience
- Loose coupling between system components

**Selected answer:** Centralized data consistency. EDA commonly provides real-time processing, scalability, resilience, and loose coupling; it does not guarantee centralized data consistency.

## Question 2 of 28

**Question:** Which statement is correct about events?

**Choices:**

- Events represent commands that must be executed in a specific order
- Events are immutable records of something that has happened in the past
- Events are always requests for action that require a response
- Events are asynchronous by nature and can be modified

**Selected answer:** Events are immutable records of something that has happened in the past.

## Question 3 of 28

**Question:** What are some of the activities that can help bring culture change, awareness, or create intent for an event driven architecture within an organization? (Choose two)

**Choices:**

- Organize workshops with Middleware and API team, and LoB team
- Educate stakeholders on benefits of EDA
- Get buy in from stakeholders on an eventing platform and tools
- Implement a quick proof-of-concept to demonstrate the value of EDA

**Selected answers:** Organize workshops with Middleware and API team, and LoB team; Educate stakeholders on benefits of EDA.

## Question 4 of 28

**Question:** Consider you are tasked to select the next candidate project to transform into real-time event driven solution. What are the top three things you would look for when making the selection? (Choose three)

**Choices:**

- Projects that cause a medium to high positive business impact
- Projects that don’t involve integration with an iPaaS
- Projects that remove brittleness, or performance issues
- Projects that can serve as a quick win that will deliver business value
- Projects that cause a low positive business impact

**Selected answers:** Projects that cause a medium to high positive business impact; Projects that remove brittleness, or performance issues; Projects that can serve as a quick win that will deliver business value.

## Question 5 of 28

**Question:** What are some of the ways an Event Mesh can support an event driven application architecture? (Choose two)

**Choices:**

- Provides you with a single pane glass to view all your distributed applications
- Connects and choreographs microservice applications
- Enables you to design and track event flows
- Can dynamically push events from on-prem to cloud services and applications

**Selected answers:** Connects and choreographs microservice applications; Can dynamically push events from on-prem to cloud services and applications.

## Question 6 of 28

**Question:** Solace’s Event Driven Methodology has six steps, one of them being the "Pilot Selection". What is the purpose of this step in the methodology?

**Choices:**

- To select the tools and eventing platform you will be using the pilot
- To select an Event Broker technology to use for the pilot
- To determine the events and event flows to get started with first and cataloging them for your pilot
- To select cloud native services to use for the pilot

**Selected answer:** To determine the events and event flows to get started with first and cataloging them for your pilot.

## Question 7 of 28

**Question:** Solace’s Event Driven Methodology has six main steps. Associate these steps with their correct purpose and intent.

**Selection instruction:** Select one association for every element. The same six purposes were offered for each step: "Engaging stakeholders, defining the vision, strategy and roadmap"; "Identifying projects, applications, and services that would benefit from an event-driven approach"; "Identify the eventing platform and tools for your architecture"; "Determining which event flow to get started with first"; "Decomposing the business flow into event-driven microservices, and identify events in the process"; "Cataloging and advertising events, and demonstrating agility and responsiveness of applications."

**Selected associations:**

- Event Streaming Foundations — Identify the eventing platform and tools for your architecture.
- Implement Quick Win — Cataloging and advertising events, and demonstrating agility and responsiveness of applications.
- Event Driven Design — Decomposing the business flow into event-driven microservices, and identify events in the process.
- Real-time Candidate — Identifying projects, applications, and services that would benefit from an event-driven approach.
- Pilot Selection — Determining which event flow to get started with first.
- Culture, Awareness, Intent — Engaging stakeholders, defining the vision, strategy and roadmap.

## Question 8 of 28

**Question:** You have an application with the following services: Inventory, Payment and Shipping. You intend to use an event broker to communicate with them. Which kind of interaction should you use for each service?

**Choices:**

- Synchronous for Inventory and Payment, asynchronous for Shipping
- Asynchronous for all services
- Asynchronous for Inventory and Payment, synchronous for Shipping
- Synchronous for all services

**Selected answer:** Synchronous for Inventory and Payment, asynchronous for Shipping.

## Question 9 of 28

**Question:** You are implementing a service that can potentially receive duplicates. What can you use to detect duplicates in the requests that you receive? (Choose two)

**Choices:**

- Message payload
- Retransmit flag
- Message ID
- Request sequence number
- Message timestamp

**Selected answers:** Retransmit flag; Message ID. The course material describes duplicate detection using a sequence number or unique ID, together with retransmit-flag inspection.

## Question 10 of 28

**Question:** You have a product catalog database that accepts updates and reads. Due to a successful advertising campaign, there is a huge increase in customers browsing your products. The database reads have increased to a point where the database is unable to cope with the load. The rate of updates has not increased. Which option would you recommend to increase read performance?

**Choices:**

- Increase the number of CPUs and memory for the web server
- Increase the number of CPUs and memory for the database
- Introduce a new instance of the database that is optimized for reads, synchronized by eventual consistency, to serve browsing customers
- Run a cache on AWS. Copy the contents of the database to the AWS cache. Serve the browsing customers off the cache

**Selected answer:** Introduce a new instance of the database that is optimized for reads, synchronized by eventual consistency, to serve browsing customers.

## Question 11 of 28

**Question:** Consider you have online store generating orders and an order processing service receiving those orders. Each order is a discrete event. Your organization launched a new product and you want to be able to deploy additional order processors on-demand to share the load of incoming order. Which pattern should be implemented in this scenario?

**Choices:**

- Competing consumer pattern
- Queue-based load leveling pattern
- Publish-subscribe pattern
- Asynchronous request-reply pattern

**Selected answer:** Competing consumer pattern. Multiple processor instances can share the work by processing separate orders.

## Question 12 of 28

**Question:** There are multiple services performing read operations (queries) on a single database requiring complex views, which is impacting on the write (command) operations. You have decided to implement the CQRS pattern to segregate read database vs write database. Which features must be used with CQRS to ensure eventual consistency of the two databases?

**Choices:**

- Guaranteed delivery
- Retry logic
- Request-reply
- Publish-subscribe

**Selected answer:** Guaranteed delivery. The course material describes guaranteed delivery of command updates to keep the query database synchronized.

## Question 13 of 28

**Question:** Consider you have online store generating orders and an order processing service receiving those orders and sending back confirmations to clients. Which step would best ensure clients are not blocked on the order processor service for confirmations as well as order processor doesn’t lose any orders in the event of high volume?

**Choices:**

- Defer the execution of requests using asynchronous request-reply communication
- Increase the number of CPUs and memory for host machine running the order processor
- Defer the execution of requests using asynchronous request-reply communication implemented over a queue-based load level pattern
- Split the order processors using the sharding pattern to handle bursty/overwhelming traffic

**Selected answer:** Defer the execution of requests using asynchronous request-reply communication implemented over a queue-based load level pattern.

## Question 14 of 28

**Question:** Which communication style typically has the highest coupling between components?

**Choices:**

- Message-based middleware
- Network socket-based communication
- File-based communication
- Database-centric communication

**Selected answer:** Database-centric communication.

## Question 15 of 28

**Question:** What is a key characteristic of durable messaging?

**Choices:**

- Messages are processed exactly once
- Messages are always processed in order
- Messages are delivered instantly
- Messages persist even if the broker crashes

**Selected answer:** Messages persist even if the broker crashes.

## Question 16 of 28

**Question:** In the context of the Eventual Consistency Pattern, which statement is false?

**Choices:**

- All reads will always return the most recent write
- Updates are propagated asynchronously
- All replicas will eventually have the same data

**Selected answer:** All reads will always return the most recent write.

## Question 17 of 28

**Question:** What is the primary challenge that the Retry Pattern addresses?

**Choices:**

- Message ordering
- Transient unavailability or failures
- Data consistency

**Selected answer:** Transient unavailability or failures.

## Question 18 of 28

**Question:** Consider there are two microservices A and B communicating to each other directly via RESTful APIs. A->REST->B. If Microservice A starts sending 100x the normal rate of events, what is the impact on Microservice B?

**Choices:**

- B becomes overloaded with data
- REST by nature will act as a shock absorber for B

**Selected answer:** B becomes overloaded with data.

## Question 19 of 28

**Question:** Given a scenario where you need to design a microservice "A" that updates state and there exists another microservice "B" that performs other, un-related, tasks based on that state change. Do you:

**Choices:**

- Have A produce an event after the state is updated that B can consume
- Have A call B directly once the state has been updated
- Have B poll A, checking to see if the state has been updated

**Selected answer:** Have A produce an event after the state is updated that B can consume.

## Question 20 of 28

**Question:** What is the main difference between a queue and a topic?

**Choices:**

- Topics allow multiple subscribers, queues deliver to only one consumer
- Queues are more reliable than topics
- Queues allow multiple subscribers, topics deliver to only one consumer
- Queues are faster than topics

**Selected answer:** Topics allow multiple subscribers, queues deliver to only one consumer.

## Question 21 of 28

**Question:** What interaction styles are available using an event-driven architecture? (Choose two)

**Choices:**

- Asynchronous publish-subscribe
- Synchronous publish-subscribe
- Synchronous request-reply
- Asynchronous request-reply

**Selected answers:** Asynchronous publish-subscribe; Synchronous request-reply. Publish-subscribe is the asynchronous event interaction style, while request-reply can use a synchronous exchange.

## Question 22 of 28

**Question:** What is a situation where you would likely want to use a synchronous interaction, rather than an asynchronous interaction?

**Choices:**

- A bank withdraws money from one account and deposits it into another account
- An order moves from Salesforce into an SAP backend
- A user updates contact information which needs to be entered into a variety of backend systems
- An Uber driver logs into the app and makes herself available for rideshare

**Selected answer:** A bank withdraws money from one account and deposits it into another account.

## Question 23 of 28

**Question:** In RealStore’s event driven architecture, the same event triggers 4 microservices: Alpha, Beta, Charlie and Delta. All of the microservices have an associated datastore. Due to an expired credential, microservice Charlie fails to complete successfully on the first attempt. What must happen now?

**Choices:**

- The exact timing and nature of the error will determine the result
- An alert must go out and support personnel will need to manually update the Alpha, Beta and Delta datastores
- Alpha, Beta and Delta datastores roll back automatically and become consistent
- If the event that triggers Charlie remains in the queue, it can be retried, and eventually all datastores will be consistent

**Selected answer:** If the event that triggers Charlie remains in the queue, it can be retried, and eventually all datastores will be consistent.

## Question 24 of 28

**Question:** RealStore’s rewards program sign-up microservice is used nationwide. However, only one of the company’s regions (District 9) has a customer relationship management (CRM) tool that would like to be notified about rewards program sign-up. If RealStore is using an event-driven architecture, what is the best way to accomplish this?

**Choices:**

- Create an intermediate microservice that intelligently filters the rewards program sign-up events
- Include logic in the rewards program sign-up microservice to only emit events for District 9
- Include logic in the District 9 CRM that eliminates events from non-District 9 events
- Ensure that region is included in the rewards program sign-up event’s topic string, and create a subscription for District 9 that attracts appropriate events

**Selected answer:** Ensure that region is included in the rewards program sign-up event’s topic string, and create a subscription for District 9 that attracts appropriate events.

## Question 25 of 28

**Question:** What are the key benefits of using event-driven solution? (Choose two)

**Choices:**

- Real-time
- Polling
- Asynchronous
- Batch processing

**Selected answers:** Real-time; Asynchronous.

## Question 26 of 28

**Question:** Which of the following topics allow consumers to subscribe to multiple topics? (Choose two)

**Choices:**

- nyctaxi/driver/status
- nyctaxi/>
- nyctaxi/rides/accepted
- nyctaxi/rides/*

**Selected answers:** nyctaxi/>; nyctaxi/rides/*. The wildcard subscriptions can match multiple topic strings.

## Question 27 of 28

**Question:** What are the key benefits of the Event Portal? (Select all that apply)

**Choices:**

- Eliminates the need for cataloging events in spreadsheets
- Prevents architects and developers from sharing and reusing events with each other
- Provides you with a single place to design, create, discover, share, secure and manage all events within your ecosystem
- Provides a visual representation of your event flows and event linkages between applications

**Selected answers:** Eliminates the need for cataloging events in spreadsheets; Provides you with a single place to design, create, discover, share, secure and manage all events within your ecosystem; Provides a visual representation of your event flows and event linkages between applications.

## Question 28 of 28

**Question:** Consider the company RealStore has a Supply Chain system that is tracking the movement of goods from manufacturer to distribution centers to retailers across all its transportation vehicles, such as trucks and container ships. Which topic template would provide the best flexibility for consumer applications part of this system, and receive location updates for specific vehicle types and specific regions?

**Choices:**

- realstore/transport/{vehicleType}/{vehicleID}/{latitude}/{longitude}
- realstore/transport/{vehicleType}/{latitude}/{longitude}
- realstore/transport/{vehicleID}/{latitude}/{longitude}
- realstore/transport/{vehicleType}/{latitude}/{longitude}/{vehicleID}

**Selected answer:** realstore/transport/{vehicleType}/{latitude}/{longitude}/{vehicleID}. Placing vehicle type and location levels before the vehicle ID lets consumers filter by those categories.

## Academy result and feedback

On 2026-09-29, I submitted the completed 28-question test. Academy displayed “Final score: 34 of 37” and “Well done, you have passed the test!” The completion dialog said the course was completed, showed the final grade as 34, and confirmed that the course certificate and EDA Practitioner Certification were earned. The course page then marked the Exam Guide and SCEDAP test as Completed and the course as “Course completed.” Academy did not display per-question correctness feedback or an answer review after submission.

## Later resume attempt

An older, still-open exam form was resumed after the course had already been marked complete. All remaining answers were selected, but submitting that stale form returned “Invalid user status” and “Something went wrong. Please try again later!” The attempt remains unsubmitted; the Academy-confirmed 34/37 result above remains the completed course record.

## Visuals

The exam screen displayed all 28 prompts as text, radio controls, checkboxes, and association selectors. No instructional image or diagram was visible in the exam question set, so no local image asset was available or needed.

