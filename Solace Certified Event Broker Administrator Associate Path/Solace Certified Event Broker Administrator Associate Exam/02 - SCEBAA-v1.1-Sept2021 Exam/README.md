---
title: "SCEBAA-v1.1-Sept2021 Exam"
document_type: lesson
learning_path: "Solace Certified Event Broker Administrator Associate Path"
course: "Solace Certified Event Broker Administrator Associate Exam"
lesson_order: 2
source: Solace Academy
---

# SCEBAA-v1.1-Sept2021 Exam

Course: Solace Certified Event Broker Administrator Associate Exam
Lesson: SCEBAA-v1.1-Sept2021 Exam
Course state at start: Exam in progress; 1 of 2 lessons completed; 3 attempts available.
Exam format shown by the platform: 70 required questions, timed.

## Resume checkpoint

Recorded through question 2. Question 1 is selected and question 2 is ready to be answered. Exam feedback and final result are pending.

## Questions and recorded responses

### Question 1
How can consumer applications avoid message loss if they connect from the PubSub+ broker or if they are slow consumer?

- Use PubSub+ broker configured with high availability
- Subscribe to topics directly on the PubSub+ broker
- Bind to a queue with the appropriate topic subscriptions mapped to it

Selected response: Bind to a queue with the appropriate topic subscriptions mapped to it.
Rationale: Durable queues retain messages for consumers that disconnect or cannot keep up; direct topic subscriptions alone do not provide that persistence.
### Question 2
An application is publishing messages to the topic: AUS1/P01/order/sell. Which topic subscription will match these messages?

- */*/*/sell
- AUS1/*01/order/>
- AU*/P01/or*/sell
- AU*1/P01/*

Selected responses: */*/*/sell; AU*/P01/or*/sell.
Rationale: `*` can match a topic level by itself and can perform a prefix match when it follows a literal prefix. The other patterns contain `*` in unsupported positions or do not match the topic levels. See [Wildcard Characters in Topic Subscriptions](https://docs.solace.com/Messaging/Wildcard-Charaters-Topic-Subs.htm).


### Question 3
When deploying PubSub+ Event Broker: Software in a high-availability mode, three node are required: Primary node, Backup node, and a third Monitor node. What is the function of this third Monitor node?

- To act as the voting node and avoid a split brain situation between Primary and Backup node
- To provide replication/disaster recovery capability
- To allow operations teams to monitor Primary and Backup node for performance and capacity
- To replicate messages and their state

Selected response: To act as the voting node and avoid a split brain situation between Primary and Backup node.
Rationale: The monitor node is the tie-breaker that prevents both messaging nodes from becoming active during a communication failure. See [Event Broker Redundancy for High Availability](https://docs.solace.com/Features/HA-Redundancy/Redundancy-and-Fault-Tolerance-Overview.htm).


### Question 4
What part of the VPN Bridge model is responsible for controlling which messages are sent across message VPN bridges?

- Topic Subscriptions
- Message Direction
- Network Connection
- Bridge Client

Selected response: Topic Subscriptions.
Rationale: Topic subscriptions control which topics the bridge receives and forwards.


### Question 5
Consider the scenario: A market data application want to publish stock price updates to multiple applications hosted in different regions for market data analysis. Which multi-bridge topology should an administrator implement to achieve this use case?

- Guaranteed Topology
- Network Topology
- Pipeline Topology
- Fan-out Topology

Selected response: Fan-out Topology.
Rationale: Fan-out distributes messages from one publishing VPN to multiple receiving VPNs.


### Question 6
Consider the scenario: A system administrator configured an ACL Profile with Publish Topic Default Action set to Disallow, with the following exception: acme/online/*. Which topics can a publisher use to successfully send messages?

- acme/online/purchase
- acme/online/refund
- acme/trading/price
- acme/onlinestore/shipping

Selected responses: acme/online/purchase; acme/online/refund.
Rationale: The exception allows one topic level after `acme/online/`; other prefixes or levels do not match.


### Question 7
A Last-Value Queue in Solace is used to store the latest message that was published to it. Which message spool configuration is required for a last-value queue?

- Message spool quota should be configured to be 0MB
- Message spool quote should be set to the size of the smallest message that can be published
- Message spool quota should be set to the size of the largest message that can be published
- Message spool quota should be configured to be 1MB

Selected response: Message spool quota should be configured to be 0MB.
Rationale: A zero maximum spool quota enables LVQ behavior and retains only the newest message. See [Queues: Last Value Queues](https://docs.solace.com/Messaging/Guaranteed-Msg/Queues.htm).


### Question 8
Which statement best describes one of the benefits of Dynamic Message Routing?

- Allows subscriber to replay messages back from a specific point in time
- Dynamically routes messages based on the message contents/payload
- Publishers don’t need to know which consumers are interested in the message, or where they are connected to in the event mesh
- Provides high-availability to PubSub+ Event Brokers

Selected response: Publishers don’t need to know which consumers are interested in the message, or where they are connected to in the event mesh.
Rationale: Dynamic Message Routing decouples publishers from subscriber locations and interests.


### Question 9
What is the main difference between VPN Bridging and Dynamic Message Routing in terms of VPN connection?

- VPN Bridges allows only different routers connection for vpns, DMR allows same or different router vpn connection
- There is no difference between both features, both only allow different router vpn connections
- There is no difference between both features, both allow same or different router vpn connections
- VPN Bridges allows same or different router vpn connection, DMR allows only different router connections for vpn

Selected response: VPN Bridges allows same or different router VPN connections, while DMR allows only different router connections.
Rationale: VPN Bridges can link different-named VPNs on one or two event brokers; DMR forms inter-broker links. See [Message VPN Bridges](https://docs.solace.com/Features/VPN/Message-VPN-Bridges-Overview.htm) and [Dynamic Message Routing](https://docs.solace.com/Features/DMR/DMR-Overview.htm).


### Question 10
Consider the scenario: A client application is publishing guaranteed messages to a queue. These messages are published with a TTL of seconds and DMQ-eligibility is not set. The queue has been configured to respect TTL, and there is a dead message-queue (DMQ) configured for the queue. What will happen to the message 5 seconds after a published message is spooled to the queue?

- The message would have been demoted to direct transport
- The message will remain on the queue
- The message would have been deleted from the queue
- The message would have been moved to a dead-message queue

Selected response: The message would have been deleted from the queue.
Rationale: Once TTL expires, the broker discards the message if it is not DMQ-eligible. See [Configuring Queues](https://docs.solace.com/Messaging/Guaranteed-Msg/Configuring-Queues.htm).


### Question 11
For consumers using persistent messaging, how does the PubSub+ Event Broker receive acknowledgements for messages before they are removed from the message spool?

- The PubSub+ Event Broker only receives acts when consumers use direct messaging
- After all the messages are consumed, the PubSub+ Event Broker receives an ack for all messages before the messages are removed from the message spool
- On per message basis, the PubSub+ Event Broker receives an ack for each message before the messages are removed from the message spool
- PubSub+ Event Broker does not receive acknowledgements from the consumers

Selected response: On a per-message basis, the broker receives an acknowledgment for each message before it is removed from the spool.
Rationale: Persistent guaranteed messages are deleted from the spool after the broker receives their consumer acknowledgments.


### Question 12
Consider the scenario: an administrator wants to delegate queue management and provisioning to applications. Which managed object/feature would allow applications to dynamically provision queues?

- ACL profile
- Message-vpn
- Client profile
- Client username

Selected response: Client profile.
Rationale: Client profiles include the permission to allow guaranteed endpoint creation, which enables applications to dynamically provision queues. See [Configuring Client Profiles](https://docs.solace.com/Security/Configuring-Client-Profiles.htm).


### Question 13
What happens in the case of an automatic HA failover when auto-revert is disabled?

- When the Active broker comes back up, it cannot take activity as it is not able to go through synchronization process with the backup node
- Both active and backup node share activity with client applications
- When the previously Active broker comes back up, it automatically takes activity once again
- When the previously Active broker comes back up, it synchronizes with the current active broker and goes into Standby state

Selected response: The previously active broker synchronizes with the current active broker and enters Standby state.
Rationale: With auto-revert disabled, the recovered node does not automatically reclaim the active role.


### Question 14
Which Solace feature is responsible for synchronizing configurations and message spool data between software nodes in High Availability?

- Revert-Activity
- Message Propagation
- Config-Sync
- Replication

Selected response: Config-Sync.
Rationale: Config-Sync propagates configuration between HA mates; the HA mate link separately synchronizes Guaranteed messages and message state. See [High Availability for Software Event Brokers](https://docs.solace.com/Features/HA-Redundancy/SW-Broker-Redundancy-and-Fault-Tolerance.htm).


### Question 15
What are some of the ways an administrator can monitor the health of a PubSub+ Event Broker? (Choose two)

- By integrating syslog events on the broker with a syslog server
- Using PubSub+ Event Portal part of the Cloud Console
- By polling various statistics on the broker using SEMP
- Using the Event Catalog part of the Cloud Console

Selected responses: Integrate broker syslog events with a syslog server; poll broker statistics using SEMP.
Rationale: Syslog exports broker events, and SEMP provides access to broker statistics.


### Question 16
Consider the scenario: A development team is looking to develop a new application using Solace messaging called ACME Trading Platform. Which access level permission should be provided to developers that are responsible for just monitoring their production environment?

- Read-Only
- None
- Admin
- Read-write

Selected response: Read-Only.
Rationale: Monitoring-only users need visibility without configuration or write permissions.


### Question 17
Consider the scenario: you have a single application that must receive all messages from a particular publisher. What delivery mode and destination type would you use?

- Guaranteed
- Cache
- Direct
- Topic

Selected responses: Guaranteed; Topic.
Rationale: Guaranteed delivery is used when messages must be retained for reliable receipt, and the topic destination identifies the publisher's message subject for routing.


### Question 18
How many links are required between different clusters in Dynamic Message Routing?

- 1 internal link
- 2 internal links
- 1 external link
- 2 external links

Selected response: 1 external link.
Rationale: Clusters communicate with each other using external links; one external link is configured between a pair of clusters. See [DMR Network Construction Rules](https://docs.solace.com/Features/DMR/DMR-Mgmt-Prerequisites.htm).


### Question 19
During the failback process, what is the administrator required to do to switch activity from backup to primary node?

- Wait until the primary node synchronizes with the backup node, then run `revert-activity` on the primary node
- Wait until the primary node synchronizes with the backup node, then run `revert-activity` on the backup node
- Wait until the primary node synchronizes with the backup node, then run `release-activity` on the primary node
- Run `revert-activity` on the backup node without waiting for the primary to synchronize

Selected response: Wait for synchronization, then run `revert-activity` on the primary node.
Rationale: Revert activity switches service back to the primary after it has synchronized with the active backup.


### Question 20
Consider the scenario: A system administrator wants to raise a monitoring event when SMF client connections reach 80% threshold of the connection limit defined on the message-vpn. Which managed object can be used to set this connection threshold?

- acl-profile
- queue
- client-username
- client-profile

Selected response: client-profile.
Rationale: Client profiles configure connection limits and their warning thresholds for clients.


### Question 21
What are some of the items that are not saved in the system configuration backup? (Choose Multiple)

- VPN configurations
- Product Keys
- CLI Scripts
- Trusted Certificates

Selected responses: Product Keys; CLI Scripts; Trusted Certificates.
Rationale: Configuration backups omit product keys and TLS certificates; CLI scripts and CA certificates must also be backed up separately. See [Backing Up and Restoring Event Broker Configurations](https://docs.solace.com/Admin/Managing-Event-Broker-Configurations.htm).


### Question 22
What happens to message ACK during Synchronous Message Replication?

- ACK is sent to publisher before the message is received by the backup data centre
- Two ACKs are sent to the publisher, one from the primary data centre and the other from the backup data centre
- ACK is not sent to publisher until the message is acknowledged by the backup data centre

Selected response: The ACK is not sent to the publisher until the backup data center acknowledges the message.
Rationale: Synchronous replication considers a message persisted only after it is stored on both active and standby sites. See [Synchronous and Asynchronous Message Replication](https://docs.solace.com/Features/DR-Replication/Sync-Asynch-Replication.htm).


### Question 23
Consider the scenario: A COVID-19 medical research facility is publishing analytics data to the active event broker of an HA triplet located at the Toronto data center. The data is then consumed by different agencies for further assessment. The development team wants to ensure that there is a zero message loss, hence the data should be replicated to an HA triplet at the Hong Kong data center. Which type of replication should be used to ensure zero message loss?

- Synchronous Replication
- Guaranteed Replication
- Asynchronous Replication
- Active Replication

Selected response: Synchronous Replication.
Rationale: Synchronous replication waits until messages are stored on both active and standby sites before acknowledging them.


### Question 24
When designing the topic structure and hierarchy for applications to use, which option follows the best practice and guidelines?

- ACC/NA/Canada/Ontario/CrossOver
- acmeconnectedcars/northamerica/canada/ontario/crossover
- acc/na/ca/on/crossover
- na/Canada/on/co

Selected response: acmeconnectedcars/northamerica/canada/ontario/crossover.
Rationale: This topic uses a consistent, descriptive hierarchy with stable levels and lowercase naming. See [Topic Architecture Best Practices](https://docs.solace.com/Messaging/Topic-Architecture-Best-Practices.htm).


### Question 25
Consider the scenario: you have multiple applications that receive update messages from a publisher and can tolerate message loss. What delivery mode and destination type would you use?

- Queue
- Guaranteed
- Direct
- Topic

Selected responses: Direct; Topic.
Rationale: Direct messages published to a topic can fan out to multiple subscribers when occasional loss is acceptable.


### Question 26
Solace PubSub+ has the message-spool configured and enabled at the system and message-vpn levels. Which of the following managed objects needs to be configured to allow clients connected to a message-vpn to send and receive guaranteed messages?

- client-username
- message-vpn
- acl-profile
- client-profile

Selected response: client-profile.
Rationale: Client profiles control client messaging capabilities, including whether clients can send or receive Guaranteed messages.


### Question 27
Before upgrading the SolOS on an Event Broker, what should an administrator do?

- Empty all queues on the Event Broker
- Perform system configuration backups
- Check client stats for message loss
- Turn off guaranteed messaging

Selected response: Perform system configuration backups.
Rationale: A current configuration backup provides a recovery point before an upgrade.


### Question 28
What access level is required to create other admin users?

- admin
- Read-Only
- Read-Write
- Write-Only

Selected response: admin.
Rationale: Creating other administrative users requires the full administrative access level.


### Question 29
In the Replay feature, when an application publishes an event to the Solace PubSub+ Event Broker, the event gets added to?

- PubSub+ Cache
- PubSub+ queue
- Replay Log
- PubSub+ queue & to Replay Log

Selected response: Replay Log.
Rationale: The Replay feature stores published events in the replay log, from which subscribers can later request replay.


### Question 30
What statement best describes VPN Bridges connecting message VPNs? (Choose multiple)

- VPN Bridges can only connect message VPNs on different brokers
- VPN Bridges can connect message VPNs with the same name, if they are on different brokers, or different names no matter where the message VPNs are
- VPN Bridges can connect message VPNs within the same event broker and on different brokers
- VPN Bridges can only connect message VPNs that have different names

Selected responses: The statement about matching VPN names only across different brokers; the statement that VPN Bridges can connect VPNs on the same or different event brokers.
Rationale: Same-named VPNs can be bridged across brokers, while differently named VPNs can be bridged on the same broker or across brokers. See [Message VPN Bridges](https://docs.solace.com/Features/VPN/Message-VPN-Bridges-Overview.htm).


### Question 31
Once the LDAP Client is authenticated, it can receive its authorization based on the LDAP Authorization group that they belong to. Which objects are defined within the LDAP Authorization Group to assign authorization rules to the client? (Choose two)

- Message VPN
- Client Username
- ACL Profile
- Client Profile
- LDAP Profile

Selected responses: ACL Profile; Client Profile.
Rationale: LDAP authorization groups associate clients with an ACL profile and a client profile. See [Configuring Client LDAP Authorization](https://docs.solace.com/Security/Configuring-LDAP-Groups.htm).


### Question 32
Which type of messages are used to record the occurrence of events happening on broker, such as routine operations or critical damages?

- ADB messages
- System messages
- VPN messages
- Syslog messages

Selected response: Syslog messages.
Rationale: Event brokers generate syslog messages for routine operations, failures, errors, and critical conditions. See [Monitoring Events Using Syslog](https://docs.solace.com/Monitoring/Monitoring-Events-Using-Syslog.htm).


### Question 33
Which Solace feature is responsible for synchronizing configurations and message spool data between software nodes in Data Replication?

- Message Propagation
- Release-Activity
- Revert-Activity
- Config-Sync

Selected response: Config-Sync.
Rationale: Config-Sync propagates configuration between replication mates; message data is propagated by the replication mechanism. See [Config-Sync](https://docs.solace.com/Features/Config-Sync/Config-Sync-Overview.htm).


### Question 34
Where do you configure endpoints & client objects?

- Client Profile level
- SolOS level
- System level
- Message VPN level

Selected response: Message VPN level.
Rationale: Queues, endpoints, client usernames, and related client objects are scoped to a Message VPN.


### Question 35
A client application with a topic subscription of `covid/*/nort*` would receive messages published to which of the below topics?

- covid/stats/NA
- covid/stats/northamerica/canada
- covid/stats/northamerica
- covid/stats/NorthAmerica

Selected response: covid/stats/northamerica.
Rationale: `*` matches one level, `nort*` matches a prefix at the next level, the extra level does not match, and topic matching is case-sensitive. See [Wildcard Characters in Topic Subscriptions](https://docs.solace.com/Messaging/Wildcard-Charaters-Topic-Subs.htm).


### Question 36
Which Solace product provides a real-time and historical dashboard into key metrics and events of the Event Broker?

- PubSub+ Monitor
- PubSub+ Manager
- PubSub+ Event Portal
- PubSub+ Event Catalog

Selected response: PubSub+ Monitor.
Rationale: PubSub+ Monitor provides real-time and historical metrics and event monitoring.


### Question 37
What is required to achieve a request-reply message exchange pattern with guaranteed messaging?

- One queue for request channel and one queue for reply channel
- One queue must be created with a topic subscription added to it
- One queue must be created
- A topic subscription must be applied to the subscribing client

Selected response: One queue must be created with a topic subscription added to it.
Rationale: A queue with a matching topic subscription can receive and spool Guaranteed requests; the requester can receive replies through its reply-to destination. See [Request Reply Messaging](https://docs.solace.com/Messaging/Guaranteed-Msg/Guaranteed-Messages.htm).


### Question 38
Which Solace channel provides only a single topic subscription to attract messages?

- Exclusive Queues
- Non-exclusive queue
- Durable Queues
- Topic Endpoints

Selected response: Topic Endpoints.
Rationale: A topic endpoint is associated with one topic subscription, while queues can have multiple subscriptions.


### Question 39
How can an application receive an acknowledgement from the PubSub+ broker for a message they publish?

- Publish the message to a Queue
- Publish the message to a Topic
- Set the message delivery mode to Direct
- Set the message delivery mode to Persistent

Selected response: Set the message delivery mode to Persistent.
Rationale: Persistent delivery uses Guaranteed Messaging, which provides publisher acknowledgments from the broker.


### Question 40
A client application is publishing messages to the topic `news/sports/hockey/chicagoblackhawks`. Select the valid topic subscription an application can use to subscribe to these messages.

- news/sports/hockey/chicago*
- news/sports/>
- news/sports/*hockey/>
- news/sports/>/*

Selected responses: news/sports/hockey/chicago*; news/sports/>.
Rationale: A trailing `*` performs a prefix match at that topic level, and `>` at the final level matches one or more remaining levels. See [Wildcard Characters in Topic Subscriptions](https://docs.solace.com/Messaging/Wildcard-Charaters-Topic-Subs.htm).


### Question 41
A client-username is always associated with managed objects that control properties and permissions of connected clients. Which managed objects provide such capabilities?

- client-object
- client-profile
- message-vpn
- acl-profile

Selected responses: client-profile; acl-profile.
Rationale: Client profiles define client behavior and capabilities; ACL profiles define client access permissions.


### Question 42
During the LDAP Authentication process, where are the authentication/authorization configurations for each of the LDAP servers stored at?

- Message VPN
- Client Username
- ACL Profile
- LDAP Profile

Selected response: LDAP Profile.
Rationale: An LDAP profile stores the LDAP server connection and authentication configuration used by the broker.


### Question 43
What is required to achieve a publish-subscribe message exchange pattern with guaranteed messaging?

- A topic subscription must be applied to the subscribing client
- A topic subscription must be applies to the publishing client
- One or more queues must be created with topic subscriptions added to each one
- One queue must be created

Selected response: One or more queues must be created with topic subscriptions added to each one.
Rationale: Guaranteed publish-subscribe delivery uses queues with topic subscriptions to receive matching published messages.


### Question 44
Which statement best describes the wildcard characteristic of Replay feature?

- Provides high-availability to PubSub+ Event Brokers
- A queue can be set up to receive messages on topics `orders/>`, request a replay, and the event broker will deliver all the messages in the Replay Log that match the `orders/>` subscription.
- Allows subscriber to replay all previous messages
- Dynamically routes messages based on the message contents/payload

Selected response: A queue can be set up to receive messages on topics `orders/>`, request a replay, and the event broker will deliver all the messages in the Replay Log that match the `orders/>` subscription.
Rationale: Replay delivers stored messages that match the queue's topic subscriptions; topic wildcards constrain which messages are replayed.


### Question 45
Which of these statements about Queue and Topic destinations is TRUE?

- Topics need to be created administratively before clients can publish/subscribe to those destinations
- Queues need to be created administratively or programmatically by clients before they can publish/subscribe to those destinations
- Neither Queue nor Topic destinations need to be created on the PubSub+ Broker
- Both Queue and Topic destinations should be administratively created beforehand on the PubSub+ Broker

Selected response: Queues need to be created administratively or programmatically by clients before they can publish/subscribe to those destinations.
Rationale: Topic destinations are dynamic; queues are managed broker objects that must be provisioned before use.


### Question 46
An order processing application is connecting to `INCOMING_ORDERS` queue and is processing the orders in sequence. Due to unpredictable load and processing time, the queue builds up. The development team wants to have any orders pending on the queue for more than a minute to not be processed. Which Solace feature can be used to implement this capability on the queue?

- Last Value Queue
- Message Timers
- Message Expiration
- Message Eliding

Selected response: Message Expiration.
Rationale: Message expiration lets a message expire after its TTL, preventing stale queued messages from being delivered after the allowed age.


### Question 47
Which type of administrative user can make configuration changes and display monitoring information on the Event Broker?

- CLI User
- Read-only User
- File Transfer User
- Support User

Selected response: CLI User.
Rationale: A CLI administrative user can configure the broker and view monitoring information; read-only and file-transfer roles have narrower permissions.


### Question 48
Consider an application publishing New Order messages in a guaranteed manner and we require only one application to consume and process the orders, but also have a standby application ready to consume in the event the first one disconnects. What is the best practice to implement this requirement in PubSub+ Event Brokers?

- Publish the order messages to a dead message queue
- Publish the order messages to a topic with the topic mapped on to a single Exclusive queue
- Publish the order messages to a topic with the topic mapped on to a single Non-Exclusive queue
- Publish the order messages to a single Non-Exclusive queue

Selected response: Publish the order messages to a topic with the topic mapped on to a single Exclusive queue.
Rationale: An Exclusive queue delivers messages to one consumer at a time and supports standby consumers, while topic mapping routes matching publications onto the queue.


### Question 49
What should an administrator configure on the PubSub+ Event Broker in the case of having the primary data center not being able to reach the backup data center during synchronous replication?

- The administrator should wait until the backup data centre come back online
- Configure Sync-Ineligible on the message-vpn to downgrade to async replication to allow publishers to send messages
- Configure Sync-Ineligible on the client-username to downgrade to async replication to allow publishers to send messages
- Configure Sync-eligible on the client profile to downgrade to async replication to allow publishers to send messages

Selected response: Configure Sync-Ineligible on the message-vpn to downgrade to async replication to allow publishers to send messages.
Rationale: The degraded replication state and automatic downgrade to asynchronous mode are managed at the Message VPN replication level. See [Synchronous and Asynchronous Message Replication](https://docs.solace.com/Features/DR-Replication/Sync-Asynch-Replication.htm).


### Question 50
What are the 3 configurable entities under the message VPN responsible for controlling guaranteed message delivery from producers? (Choose multiple)

- Endpoint Administrative Status
- Dead Message Queue
- Client Profile
- ACL Profile

Selected responses: Endpoint Administrative Status; Client Profile; ACL Profile.
Rationale: Endpoint administrative state determines whether the destination accepts traffic, client profiles control guaranteed send capability, and ACL profiles authorize publishing to topics. See [Using Client Profiles and Client Usernames](https://docs.solace.com/Cloud/client-profiles.htm) and [Messaging Components and Application Interactions](https://docs.solace.com/API/Component-Maps.htm).


### Question 51
Which access level permission below cannot be applied to CLI management users in Solace?

- admin
- Write-Only
- Read-Write
- Read-Only

Selected response: Write-Only.
Rationale: Solace CLI management access levels include admin, read-write, and read-only; there is no write-only access level.


### Question 52
A flight ticketing system is sending new purchase orders on the topic `acme/orders`. We have three consumer applications to provide redundancy and load sharing. Assuming Shared Subscription is enabled and consumers are using SMF, which topic should the consumer applications subscribe to ensure a single order is delivered to only one consumer?

- `#share/service/acme/orders`
- `#share/acme/orders`
- `share/acme/orders`
- `acme/*`

Selected response: `#share/service/acme/orders`.
Rationale: `#share/<share-name>/<topic>` identifies the shared group (`service`) and the topic subscription (`acme/orders`), so matching messages are distributed to one group member.


### Question 53
Durable queues are known to? (Choose two)

- have only a single consumer
- be explicitly created or deleted by administrators or client applications
- be explicitly created or deleted by client applications only
- have a single or multiple consumer

Selected responses: be explicitly created or deleted by administrators or client applications; have a single or multiple consumer.
Rationale: Durable queues persist until deleted and may be provisioned administratively or by a permitted client; depending on queue access type, they support one or multiple consumers.


### Question 54
An application wants to consume messages from a queue with multiple clients connected and load balance messages among them. What queue property should be used to achieve this?

- Set Distribute All property on queue
- Set queue access type to Non Exclusive
- Enable Share All flag on queue
- This is not possible with Solace queues

Selected response: Set queue access type to Non Exclusive.
Rationale: A non-exclusive queue permits multiple consumer flows, and the broker distributes messages among connected consumers.


### Question 55
A message-VPN is created for which of the following?

- High availability configuration
- Clustering configuration
- Message Data Separation
- Equipment sharing

Selected response: Message Data Separation.
Rationale: Message VPNs provide logically separate messaging domains within an event broker, isolating message data and configuration.


### Question 56
There are three Solace PubSub+ instances required for Software High Availability. What are the three nodes?

- Primary Node, Backup Node, Secondary Backup Node
- Primary Node, Backup Node, Monitor Node
- Parent Node, Child Node 1, Child Node 2

Selected response: Primary Node, Backup Node, Monitor Node.
Rationale: Software HA uses a primary and backup broker plus a monitor node that helps arbitrate failover and prevent split brain.


### Question 57
During the LDAP Authentication process, where are the client’s credentials validated for authentication?

- LDAP Profile
- LDAP Authorization Group
- Message VPN
- LDAP Server

Selected response: LDAP Server.
Rationale: The broker uses the LDAP profile to locate and communicate with an LDAP server, which validates the user's credentials.


### Question 58
To achieve a point-to-point message exchange pattern with guaranteed messaging, what is required?

- Producer publishing messages straight to the queue and message gets consumed by one subscribing client
- A topic subscription must be applied to the subscribing client
- A queue must be created with a topic subscription added to it
- A durable topic must be created

Selected response: Producer publishing messages straight to the queue and message gets consumed by one subscribing client.
Rationale: Point-to-point delivery sends a guaranteed message directly to a queue, where one consumer receives each message.


### Question 59
Which Solace feature/product can developers use to prime new applications with historical data published to queues on PubSub+ Event Brokers?

- PubSub+ Manager
- Message Replay
- PubSub+ Cache
- PubSub+ Event Portal

Selected response: Message Replay.
Rationale: Message Replay can replay stored guaranteed messages from queues to a consumer that needs historical data.


### Question 60
Which authentication mechanisms are available for client applications to use when connecting to PubSub+ Event Broker? (Choose multiple)

- LDAP authentication
- Client certificate authentication
- Kerberos authentication
- Multi-factor authentication
- Device authentication

Selected responses: LDAP authentication; Client certificate authentication; Kerberos authentication.
Rationale: Solace client authentication supports LDAP-backed credentials, client certificates, and Kerberos. See [Configuring Client Authentication](https://docs.solace.com/Security/Configuring-Client-Authentication.htm).


### Question 61
Which of the following wildcards allow consumers to subscribe to multiple topics? (Choose two)

- `uber/rides/*`
- `uber/driver/sta*tus`
- `uber/>`
- `*uber/rides/accepted`

Selected responses: `uber/rides/*`; `uber/>`.
Rationale: `*` matches one complete topic level, while `>` matches one or more remaining levels. Embedded or prefixed wildcard characters are not valid wildcard levels.


### Question 62
Consider the scenario: A consumer application wants to receive only the most current direct messages published to the topics that they subscribed to. The application can only handle 10 messages per second per topic. What is the delay time interval that should be set on the client-profile?

- 1000 ms
- 500 ms
- 1 ms
- 100 ms

Selected response: 100 ms.
Rationale: A rate of 10 messages per second corresponds to one delivery every 0.1 seconds (100 ms), matching the eliding delay needed to favor current messages at the client’s processing rate.


### Question 63
In topic endpoints, what happens to stored messages when topic subscriptions change?

- Topic endpoints must be emptied before any topic subscription changes
- Stored messages remain unaffected by subscription changes
- Stored messages will be deleted by subscription changes
- Stored messages remain unaffected but any new messages would be rejected

Selected response: Stored messages remain unaffected by subscription changes.
Rationale: A subscription change affects which future messages are admitted; messages already stored on the topic endpoint remain there.


### Question 64
Which configuration object is used to authenticate clients trying to connect to the PubSub+ Event Broker?

- Client usernames
- ACL profiles
- Client profiles
- Queues

Selected response: Client usernames.
Rationale: Client usernames or external authentication mappings identify and authenticate clients; ACL profiles and client profiles control authorization and capabilities.


### Question 65
Consider the scenario: An e-commerce website team is expecting to have excessive message volumes during their biggest sale of the year. The team want to prioritize orders related to the products on sale as high priority and not-on-sale products as low priority to make sure the website remains responsive. What happens to the orders being published to the queue if the number of messages is above the message priority threshold limit?

- High priority messages will be saved on the queue and low priority messages would be put on hold
- High priority messages will be discarded, and low priority messages will be saved on the queue
- High priority messages will be saved on the queue and low priority messages would be discarded by the queue
- Both high priority and low priority messages would be discarded by the queue

Selected response: High priority messages will be saved on the queue and low priority messages would be discarded by the queue.
Rationale: At the priority threshold, the queue preserves higher-priority messages and discards lower-priority traffic to protect important orders.


### Question 66
What is the main difference between direct messaging mode and guaranteed messaging mode when moving messages from source to destination VPN in VPN Bridges?

- Topic subscriptions are added to bridge in the Source message VPN in direct messaging, but are added to queue in Destination message VPN in guaranteed messaging
- There is no difference in how direct and guaranteed messaging handle transporting messages across VPNs
- Topic subscriptions are added to bridge in the Destination message VPN in direct messaging, but are added to queue in Source message VPN in guaranteed messaging
- Topic subscriptions are added to queue in the Source message VPN in direct messaging, but are added to bridge in Destination message VPN in guaranteed messaging

Selected response: Topic subscriptions are added to bridge in the Destination message VPN in direct messaging, but are added to queue in Source message VPN in guaranteed messaging.
Rationale: Direct bridge subscriptions are configured on the destination-side bridge; guaranteed transfers use a bridge queue on the source VPN. See [Message VPN Bridges](https://docs.solace.com/Features/VPN/Message-VPN-Bridges-Overview.htm).


### Question 67
Which configuration feature can an administrator use to restrict the topics an application can publish and/or subscribe to?

- Message VPNs
- ACL profiles
- Client profiles
- Client usernames

Selected response: ACL profiles.
Rationale: ACL profiles define publish and subscribe topic access rules and are associated with clients through their usernames or authorization groups.


### Question 68
Which type of failure can be resolved by Data Replication but not by High Availability?

- Network infrastructure failure
- Data centre failure
- Event Broker component failure
- Event Broker power failure

Selected response: Data centre failure.
Rationale: Data replication copies message data between separate sites and supports recovery from a data-centre outage; HA handles broker failures within an HA group.


### Question 69
Which messaging feature allows consumer applications to throttle and receive only the most current non-persistent messages published to topics?

- Dead-message queue
- Message Eliding
- Shared Subscription
- Priority Based Congestion Handling

Selected response: Message Eliding.
Rationale: Message eliding suppresses older Direct messages for slow consumers so they receive more current values at a manageable rate.


### Question 70
Which authentication feature requires just a client’s username & password?

- OAuth authentication
- Basic Internal authentication
- Kerberos authentication
- RADIUS authentication

Selected response: Basic Internal authentication.
Rationale: Basic internal authentication validates the supplied username and password against the broker’s internal client-username database.



## Final result

Submitted the 70-question exam and passed with a final score of 91.3%. The course page confirmed the certificate and the Solace Certified Event Broker Administrator Associate certification were earned.
