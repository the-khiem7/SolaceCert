---
title: "SCDP Exam - v1.1Sept2025"
document_type: lesson
learning_path: "Solace Certified Developer Practitioner Path"
course: "Solace Certified Developer Practitioner Exam"
lesson_order: 2
source: Solace Academy
---
# SCDP Exam - v1.1Sept2025

## Academy state

The Academy presents this lesson as a timed test with 40 questions. At the first capture, the test showed 1 hour 27 minutes remaining and 3 of 3 attempts left. The test was on page 1 of 40.

## Question 1 of 40

**Question:** Consider a company is planning to launch a new product that is in high demand and expecting bursty/overwhelming order volumes. Their current application architecture is not designed to handle the volume of traffic expected and do not want to lose any orders. The development team has decided to move their applications to an Event Driven Architecture (EDA). Which design pattern in EDA can solve handling overwhelming traffic and offer shock absorption?

**Choices:**

- Saga pattern
- Asynchronous Request-Reply pattern
- Queue-Based Load Levelling pattern
- Command & Query Responsibility Segregation pattern

**Selected answer:** Queue-Based Load Levelling pattern. The test has not yet displayed answer feedback.

## Question 2 of 40

**Question:** An application is publishing messages to a topic destination with Direct delivery mode. The topic is mapped/subscribed to a queue to persist the messages. Which behavior should the publishing application expect if the queue became full and the broker is unable to persist further messages? Assume the queue is configured with broker default settings.

**Choices:**

- The messages are stored on a Dead Message Queue by the broker and publishing application does not receive any acknowledgments from the broker
- The messages are discarded and publishing application does not receive any acknowledgments from the broker
- The messages are discarded and publishing application will receive negative acknowledgments from the broker
- The messages are stored on a Dead Message Queue by the broker and publishing application will receive negative acknowledgments from the broker

**Selected answer:** The messages are discarded and publishing application does not receive any acknowledgments from the broker. Direct delivery is best-effort and does not provide Guaranteed-message acknowledgement behavior; result feedback has not been displayed.

## Question 3 of 40

**Question:** Which two options can an application use to detect duplicate events when consuming from queues using Solace APIs? (Choose two)

**Choices:**

- Compare SenderID property on the message
- Compare the Unique ID set by the publisher application
- Check if Redelivered flag is set on the message by the broker
- Compare Body/Payload of the message

**Selected answers:** Compare the Unique ID set by the publisher application; Check if Redelivered flag is set on the message by the broker. The test has not yet displayed answer feedback.

## Question 4 of 40

**Question:** Solace’s SEMP protocol does NOT cover this:

**Choices:**

- Administration
- Provisioning
- Monitoring
- Publish & Subscribe
- Management

**Selected answer:** Publish & Subscribe. SEMP is a management protocol; publish-subscribe messaging uses data-plane APIs and protocols. The test has not yet displayed answer feedback.

## Question 5 of 40

**Question:** Which two protocols can be specified as a prefix to the host IP address or hostname of the Solace Event Broker, when establishing a secure Session? (Choose two)

**Choices:**

- wss://
- tcp://
- ws://
- tcps://

**Selected answers:** wss:// and tcps://. Both schemes establish secure WebSocket or TCP sessions. The test has not yet displayed answer feedback.

## Question 6 of 40

**Question:** In Solace guaranteed messaging, a publish window determines

**Choices:**

- Time delay between publishes
- Maximum number of outstanding messages on the wire before the acknowledgement of first publish is received
- Speed at which the messages can be published to broker
- Number of messages that can be published in a batch

**Selected answer:** Maximum number of outstanding messages on the wire before the acknowledgement of first publish is received. The test has not yet displayed answer feedback.

## Question 7 of 40

**Question:** A developer would like to analyze expired message on a queue called "ONLINE_ORDERS" instead of being discarded by the broker when the message expires. What steps should the developer take to capture the expired messages from this queue only?

**Choices:**

- Configure the ONLINE_ORDERS queue with a new Dead Message Queue and ensure messages are flagged as TTL-eligible by publishing clients
- It is not possible to configure a specific Dead Message Queue for the ONLINE_ORDER queue, and all expired message will be sent to the default queue called "#DEAD_MESSAGE_QUEUE"
- Configure the ONLINE_ORDERS queue with a new Dead Message Queue and ensure messages are flagged as DMQ-eligible by publishing clients
- Configure the ONLINE_ORDER queue with the default queue called "#DEAD_MESSAGE_QUEUE" and ensure messages are flagged as DMQ-eligible by publishing clients

**Selected answer:** Configure the ONLINE_ORDERS queue with a new Dead Message Queue and ensure messages are flagged as DMQ-eligible by publishing clients. The test has not yet displayed answer feedback.

## Question 8 of 40

**Question:** Consider an ice cream delivery company using an event driven microservices architecture has implemented the following topic hierarchy: `orders/{productGroup}/{action}/v1/{area}/car/{customerID}/{productID}/{orderID}`. `{productGroup}` is the type of ice creams like cone, stick, gelato, popsicle, etc.; `{action}` is the order action like initialized, updated, canceled; `{area}` is the general region for which an inventory manager is responsible; `{customerID}` is the customer identifier; `{productID}` is the item being ordered; `{orderID}` is the unique order identifier. An inventory manager responsible for popsicle distribution in the New York City (NYC) area would subscribe to which topic for all order actions?

**Choices:**

- `orders/popsicle/>/v1/nyc/*`
- `orders/*/*/v1/nyc`
- `orders/popsicle/*/v1/nyc/*`
- `orders/popsicle/*/v1/nyc/>`
- `orders/popsicle/*/v1/*/>`

**Selected answer:** `orders/popsicle/*/v1/nyc/>`. `*` matches one topic level (the action), while terminal `>` matches the remaining levels after the NYC area. The test has not yet displayed answer feedback.

## Question 9 of 40

**Question:** In a computing context, which statements describe Event(s)? (Choose three)

**Choices:**

- Stream of updates around application state changes
- Commands to other applications
- Time sensitive and each event is unique
- Something that has happened in your application worth telling other applications
- Query state from other applications

**Selected answers:** Stream of updates around application state changes; Time sensitive and each event is unique; Something that has happened in your application worth telling other applications. The test has not yet displayed answer feedback.

## Question 10 of 40

**Question:** Which statement best describes the characteristics of a Solace Queue Browser?

**Choices:**

- Consumer applications can look at Guaranteed messages spooled for a Queue in the order of oldest to newest without consuming them
- Consumer applications can look at Guaranteed messages spooled for a Queue by specifying the start index
- Consumer applications can look at Guaranteed messages spooled for a Queue in any order without consuming them
- Consumer applications can look at Guaranteed messages spooled for a Queue by specifying the ID of the message

**Selected answer:** Consumer applications can look at Guaranteed messages spooled for a Queue in the order of oldest to newest without consuming them. The test has not yet displayed answer feedback.

## Question 11 of 40

**Question:** A developer is designing an online shopping application using an event driven architecture (EDA) that needs to ensure every single order placed and confirmed is delivered to a payment processing system, an inventory system, and a shipping system. Which EDA design pattern should the developer implement to ensure a single order is received by all three systems in the most efficient way possible?

**Choices:**

- Competing Consumers
- Request-Reply pattern
- Publish-Subscribe pattern
- Point-to-Point pattern

**Selected answer:** Publish-Subscribe pattern, so each interested system receives a copy of the order event. The test has not yet displayed answer feedback.

## Question 12 of 40

**Question:** Which two statements describe the characteristics of Non-Durable Queues? (Choose two)

**Choices:**

- Cannot be created by an administrator and only applications can programmatically create it using APIs
- Remains on the broker, i.e. not deleted automatically, upon a broker restart
- Allows multiple consumers to bind to it
- Can be created by an administrator or by an application programmatically
- Is automatically deleted when the client disconnects or times-out

**Selected answers:** Cannot be created by an administrator and only applications can programmatically create it using APIs; Is automatically deleted when the client disconnects or times-out. The test has not yet displayed answer feedback.

## Question 13 of 40

**Question:** Which three statements describe the characteristics of Guaranteed messages? (Choose three)

**Choices:**

- Publisher does require acknowledgment of receipt by the broker
- Publisher does not require acknowledgment of receipt by the broker
- Broker does require acknowledgment of receipt by subscribing clients
- Messages are not retained for a client when it’s not connected to an event broker
- Messages are retained for a client when it’s not connected to an event broker
- Broker does not require acknowledgment of receipt by subscribing clients

**Selected answers:** Publisher does require acknowledgment of receipt by the broker; Broker does require acknowledgment of receipt by subscribing clients; Messages are retained for a client when it’s not connected to an event broker. The test has not yet displayed answer feedback.

## Question 14 of 40

**Question:** Consider the following Topic taxonomy and enumerations. The taxonomy levels are Product, Sub Product, Country, Process, and Priority. Their enumerations are Collections, DDI, DDA, SG, HK, Initiation, Clearing, High, Medium, and Low. Subscribing to which topic would give you all high priority payment collection DDI initiation messages for the SG country?

**Choices:**

- `Collections/DDI/*/Initiation/High`
- `Collections/DDI/SG/Initiation/*`
- `Collections/DDI/SG/*/High`
- `Collections/DDI/SG/>`
- `Collections/DDI/SG/Initiation/High`

**Selected answer:** `Collections/DDI/SG/Initiation/High`. This exact topic selects Collections, DDI, SG, Initiation, and High. The on-screen taxonomy diagram was visible and its labels are transcribed above; no local image was saved because the available screenshot export was bound to a blank page instead of the active Chrome tab. The test has not yet displayed answer feedback.

## Question 15 of 40

**Question:** Which three statements describe the characteristics of Solace Message Replay? (Choose three)

**Choices:**

- Cannot be initiated by an administrator and only applications can initiate replay of messages
- Can be configured with infinite depth by adding more storage to the Solace broker
- The ability to initiate message replay from Solace Broker Manager or Solace CLI by specifying a Queue to replay the messages to
- The ability to replay messages not just to a fully qualified topic, but to a wildcard topic, or to a wildcard subscription
- Automatically prune out the oldest messages from the Replay Log to make room for new messages as they arrive if the event Replay Log has reached its maximum depth
- Does not consume any resources or storage resources on the Solace broker

**Selected answers:** The ability to initiate message replay from Solace Broker Manager or Solace CLI by specifying a Queue to replay the messages to; The ability to replay messages to a wildcard topic or wildcard subscription; Automatically prune the oldest messages from the Replay Log at maximum depth. The test has not yet displayed answer feedback.

## Question 16 of 40

**Question:** Consider a consumer application subscribing to messages published on a Topic with Direct delivery mode. In which two scenarios can the consumer application lose messages? (Choose two)

**Choices:**

- Egress message buffer overflow due to a Queue, subscribing to the Topic, being full
- Message build-up due to slow processing from the Topic
- Message build-up due to slow processing from a Queue that is subscribing to the Topic
- Egress message buffer overflow due to a network congestion

**Selected answers:** Egress message buffer overflow due to a Queue subscribing to the Topic being full; Egress message buffer overflow due to network congestion. Direct messages can be discarded when a consumer cannot accept delivery; the test has not yet displayed answer feedback.

## Question 17 of 40

**Question:** An application can initiate replay of messages from a replay log in Solace broker using which three approaches? (Choose three)

**Choices:**

- After a specific application defined message ID
- From the beginning of the message replay log
- From the newest to the oldest message in the replay log
- After a specific replication group message ID generated by the broker
- Starting from a specific date and time
- After a specific match based on a selector expression

**Selected answers:** From the beginning of the message replay log; After a specific replication group message ID generated by the broker; Starting from a specific date and time. The test has not yet displayed answer feedback.

## Question 18 of 40

**Question:** Which feature or administration tool available from Solace can be used by an application to programmatically and automatically configure and monitor a Solace broker?

**Choices:**

- Solace Monitor
- SEMP
- SolAdmin
- Solace CLI
- Solace Broker Manager

**Selected answer:** SEMP. It is the programmatic management protocol. The test has not yet displayed answer feedback.

## Question 19 of 40

**Question:** Which two Solace broker features can a developer set connection limit on to prevent rogue applications from exhausting connections on a single broker? (Choose two)

**Choices:**

- Broker system settings
- Message VPN
- Client username
- Client profile
- ACL profile

**Selected answers:** Message VPN; Client profile. The Message VPN can cap total simultaneous connections for that VPN, and its client profiles can cap connections per client username. The test has not yet displayed answer feedback.

## Question 20 of 40

**Question:** Consider the following Topic taxonomy and enumerations. Subscribing to which topic would give you all high priority payment collection DDI initiation messages regardless of the country?

**Taxonomy shown:** Product / Sub Product / Country / Process / Priority, with enumerations Collections / DDI / DDA / SG / HK / Initiation / Clearing / High / Medium / Low, as shown in the Question 14 taxonomy graphic.

**Choices:**

- `Collections/DDI/SG/Initiation/High`
- `Collections/DDI/*/*/High`
- `Collections/DDI/>`
- `Collections/DDI/*`
- `Collections/DDI/*/Initiation/High`

**Selected answer:** `Collections/DDI/*/Initiation/High`. The wildcard matches any country while retaining the requested product, process, and priority levels. The test has not yet displayed answer feedback.

## Question 21 of 40

**Question:** Consider an application is publishing messages to topics. Which three UTF-8 characters should be avoided in the topic string when publishing messages? (Choose three)

**Choices:**

- `/`
- `*`
- `>`
- `!`
- `#`

**Selected answers:** `*`, `>`, and `!`. These characters have special meaning in subscriptions, so using them literally in published topics makes matching confusing; `/` is the topic-level separator. The test has not yet displayed answer feedback.

## Question 22 of 40

**Question:** What are some of the benefits of implementing a rich topic architecture with Solace? (Choose three)

**Choices:**

- It removes the explicit need for orchestration
- Removes the need for in-app filtering
- Allows for fine-grained routing, filtering, and access control
- It removes the explicit need for choreography
- Allows topics to be sharded across multiple partitions

**Selected answers:** It removes the explicit need for orchestration; Removes the need for in-app filtering; Allows for fine-grained routing, filtering, and access control. Rich topics support filtering at the broker, and event-driven collaboration can avoid central orchestration. The test has not yet displayed answer feedback.

## Question 23 of 40

**Question:** A developer is trying to solve a problem where read operations (queries) requiring complex views are impacting on the write (command) operations. Which design pattern should the developer implement to solve this problem?

**Choices:**

- Eventual Consistency pattern
- Command & Query Responsibility Segregation pattern
- Publish Subscribe pattern
- Sharding pattern

**Selected answer:** Command & Query Responsibility Segregation pattern. CQRS separates the read/query model from the write/command model. The test has not yet displayed answer feedback.

## Question 24 of 40

**Question:** A developer wants to load balance guaranteed message on a queue to a group of consumer application. Which Queue Access Type should the developer configure the queue with?

**Choices:**

- Non-Exclusive
- Exclusive
- Durable
- Non-Durable

**Selected answer:** Non-Exclusive. Multiple consumer applications can share a non-exclusive queue, with each message delivered to one consumer. The test has not yet displayed answer feedback.

## Question 25 of 40

**Question:** Consider a developer is designing an order processing application and needs to account for receiving duplicate orders or repeated data. Which design pattern should the developer implement to handle receiving duplicates?

**Choices:**

- Point-to-Point pattern
- Idempotent Processor pattern
- Queue-Based Load Levelling pattern
- Eventual Consistency pattern

**Selected answer:** Idempotent Processor pattern. The pattern detects or suppresses duplicate processing, often by using message sequence numbers or unique IDs. The test has not yet displayed answer feedback.

## Question 26 of 40

**Question:** Consider three consumer applications a, b, and c that are replicas of each other receiving updates from a publisher. All three consumers are deployed in different regions with their own databases and need to process every message. Which approach will ensure all three consumer applications achieve eventual consistency? Assume all messages are published with guaranteed delivery mode.

**Choices:**

- Publisher sends 1 copy of the message to a topic that all three consumers subscribe to
- Publisher sends 3 copies of the message to unique topics that are subscribed by each of the consumers
- Publisher sends 3 copies of the message to each of the consumer’s queue
- Publisher sends 1 copy of the message to a topic that is mapped/subscribed on each of the consumer’s queue

**Selected answer:** Publisher sends 1 copy of the message to a topic that is mapped/subscribed on each consumer’s queue. Each queue retains its own guaranteed copy for its consumer. The test has not yet displayed answer feedback.

## Question 27 of 40

**Question:** A developer is designing an application to produce critical events that need to be broadcast in a guaranteed/persistent manner to a group of consumer applications, using the Publish-Subscribe design pattern. Which approach should the developer choose, following best practices, to ensure each consumer receives a copy of the event?

**Choices:**

- Publish a copy of the event to separate topics that are unique for each consumer
- Publish the event to a topic and have each of the consumers subscribe to the topic
- Publish a copy of the event to each of the consumer’s queue
- Publish the event to a topic and have that topic mapped to each of the consumer’s queue on the broker

**Selected answer:** Publish the event to a topic and have that topic mapped to each consumer’s queue on the broker. Each queue retains a guaranteed copy for its consumer. The test has not yet displayed answer feedback.

## Question 28 of 40

**Question:** A Last-Value Queue with multiple topic subscriptions:

**Choices:**

- Stores last received message on each topic
- Stores last received message of lowest priority
- Stores last received message of highest priority
- Stores last received message of any topic
- Does not support multiple subscriptions

**Selected answer:** Stores the last received message on each topic. The test has not yet displayed answer feedback.

## Question 29 of 40

**Question:** Which minimum level Queue permission allows applications to read messages from the queue as well as delete them from the queue by acknowledging the message?

**Choices:**

- Delete
- Modify Topic
- Consume
- Read-Only

**Selected answer:** Consume. It allows clients to consume and delete messages; Read-Only does not allow deletion. The test has not yet displayed answer feedback.

## Question 30 of 40

**Question:** An application is publishing messages to a topic destination with Persistent delivery mode. The topic is mapped/subscribed to a queue to persist the messages. Which behavior should the publishing application expect if the queue became full and the broker is unable to persist further messages? Assume the queue is configured with broker default settings.

**Choices:**

- The messages are discarded and publishing application will receive negative acknowledgments from the broker
- The messages are stored on a Dead Message Queue by the broker and publishing application does not receive any acknowledgments from the broker
- The messages are discarded and publishing application does not receive any acknowledgments from the broker
- The messages are stored on a Dead Message Queue by the broker and publishing application will receive negative acknowledgments from the broker

**Selected answer:** The messages are discarded and the publishing application will receive negative acknowledgments from the broker. Persistent delivery uses Guaranteed messaging acknowledgements; the test has not yet displayed answer feedback.

## Question 31 of 40

**Question:** Which three statements describe the characteristics of direct messages? (Choose three)

**Choices:**

- Broker does require acknowledgment of receipt by subscribing clients.
- Messages are not retained for a client when it's not connected to an event broker.
- Message are delivered to subscribing clients in the order in which publishers publish them.
- Broker does not require acknowledgment of receipt by subscribing clients.
- Message are retained for a client when it's not connected to an event broker.
- Message delivered to subscribing clients can be out-of-order or not in order in which publishers publish them.

**Selected answer:** Messages are not retained while the client is disconnected; the broker does not require client acknowledgment; subscribing clients receive messages in publisher order.

## Question 32 of 40

**Question:** Consider an organization has mandated all events and messages exchanged by an applications (both data in motion and data at rest) must be encrypted. What steps should a developer take to comply with the above?

**Choices:**

- Configure applications to connect to Solace broker's TLS/SSL listening port so any data exchanged end-to-end is encrypted.
- There are no steps a developer can take and it is the responsibility of the organization's infrastructure or IT team to ensure the network is secure and Solace broker is deployed in a secure environment.
- Configure applications to connect to Solace broker's TLS/SSL listening port and ensure broker is setup with trusted server certificate as well as configured to use encrypted disks so both data at rest and in motion is encrypted.
- Ensure the Solace broker is configured to use encrypted disk so data at rest is encrypted and setup with a trusted server certificate so all data in motion is encrypted.

**Result:** Awaiting exam submission; the test has not yet displayed answer feedback.

## Question 33 of 40

**Question:** Which statement is True of Events?

**Choices:**

- Event data is mutable.
- Event is same as a command.
- Event data is immutable.
- Event is same as a query.

**Selected answer:** Event data is immutable.

## Question 34 of 40

**Question:** A developer is designing a solution that uses Event Driven Architecture. Which Solace product should the developer use to document, visualize, and collaborate on the development of this solution?

**Choices:**

- Solace Event Portal.
- Solace Event Mesh.
- Solace Event Broker.
- Solace Event Streaming Services.
- Solace Broker Manager.

**Selected answer:** Solace Event Portal.

**Result:** Awaiting exam submission; the test has not yet displayed answer feedback.

## Question 35 of 40

**Question:** Consider the following Topic taxonomy and enumerations: subscribing to which topic would give you all high priority payment collection messages?

**Visual:** The taxonomy is Product / Sub Product / Country / Process / Priority. The enumerations shown are Collections, DDI, DDA, SG, HK, Initiation, Clearing, High, Medium, and Low.

**Choices:**

- `Collections/*/*/*/*`
- `Collections/DDI/SG/Initiation/High`
- `Collections/*/*/*/High`
- `Collections/>`
- `Collections/DDI/*/*/High`

**Selected answer:** `Collections/*/*/*/High`, covering every sub-product, country, and process under Collections while matching High priority.

**Visual note:** The taxonomy image was visible in the exam. Its labels and order are transcribed above because the browser screenshot export did not provide a local image file.

## Question 36 of 40

**Question:** Which two possible reasons can cause a message to be removed and discarded from a Queue? (Choose two)

**Choices:**

- The queue has reached its storage quota and needs to prune out an older message to make room for new messages that arrive.
- A message’s TTL value has been exceeded and the queue is configured to respect message TTL expiry times.
- The number of redelivery attempts for a message exceeds the Max Redelivery value set for that queue.

**Selected answer:** TTL expiry when the queue respects TTL, and exceeding the queue's maximum redelivery count. These are the queue discard/removal cases listed by the current Solace queue documentation. [Solace Queues documentation](https://docs.solace.com/Messaging/Guaranteed-Msg/Queues.htm)

## Question 37 of 40

**Question:** Consider the following deployment strategies A & B. Which four statements are True for these strategies? (Choose four)

**Visual:** Strategy A is a REST chain from a Web Application to Account Opening, Birthday Email, and Card Mailing microservices. Strategy B uses REST from the Web Application to Account Opening, which publishes to an Event Broker; Card Mailing and Birthday Email microservices subscribe to the broker.

**Choices:**

- Strategy A – Despite having microservices-level granularity, components are not agile and requires modification to existing components to accommodate changes.
- Strategy B – Allows for automation of deployments and comprehensive unit testing, including error scenarios.
- Strategy A & B – Both support fan-out of critical services for scaling.
- Strategy B – Brings in loose coupling of components and changes can be made without impact to existing services.
- Strategy A – Promotes tight coupling and makes one-to-many distribution of data difficult.

**Selected answer:** Strategy A is not agile and needs modification when changes are made; Strategy B allows automated deployments and comprehensive unit testing; Strategy B brings loose coupling; Strategy A promotes tight coupling and makes one-to-many distribution difficult. The shared fan-out statement is not selected because the REST chain does not fan out through a broker.

**Visual note:** The deployment diagram was visible in the exam. Its flow and labels are transcribed above because the browser screenshot export did not provide a local image file.

## Question 38 of 40

**Question:** Consider a consumer application is receiving messages by subscribing to topics. Which Solace broker feature can a developer configure to limit the rate at which message are sent to a consumer application?

**Choices:**

- Queue Endpoint.
- ACL Profile.
- Message Replay.
- Message Eliding.

**Selected answer:** Message Eliding.

**Result:** Awaiting exam submission; the test has not yet displayed answer feedback.

## Question 39 of 40

**Question:** What steps can a developer take to ensure authentication credentials are not sent in plain text to a Solace broker when establishing a session connection from a client messaging application? Assume the broker is already setup with a trusted server certificate.

**Choices:**

- Encrypt the authentication credentials in the session configuration of the client application.
- No steps are required by the developer as the Solace broker is setup with a trusted server certificate, ensuring credentials are encrypted during connection.
- Create a secure session in the client application by connecting to the Solace broker's TLS/SSL listening port.
- Configure the Solace broker with LDAP authentication, eliminating the need to manage the passwords on the broker.

**Selected answer:** Create a secure session in the client application by connecting to the broker's TLS/SSL listening port.

## Question 40 of 40

**Question:** Which Solace broker feature can a developer use to ensure application can only publish or subscribe to the topics they are authorized for?

**Choices:**

- ACL profiles.
- Client usernames.
- Queues.
- Message VPN.
- Client profiles.

**Selected answer:** ACL profiles.
