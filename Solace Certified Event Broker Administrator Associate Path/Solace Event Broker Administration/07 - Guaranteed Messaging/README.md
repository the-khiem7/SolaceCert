---
title: "Guaranteed Messaging"
document_type: lesson
learning_path: "Solace Certified Event Broker Administrator Associate Path"
course: "Solace Event Broker Administration"
lesson_order: 7
source: Solace Academy
---

# Guaranteed Messaging

- **Course:** Solace Event Broker Administration
- **Syllabus section:** Guaranteed Messaging
- **Academy content type:** SCORM

## Screen 1: What's the Scenario?

The active scenario introduces Haroldo as a middleware manager for ACME Retail. He says: “Hi! I'm Haroldo, a middleware manager for ACME Retail. It's really important that we don't lose customer data or have a disruption to order processing. How can we ensure we don't lose our data?” The screen provides a **CONTINUE** control to reveal the scenario response.


## Screen 2: Haroldo's order-retention question

After **CONTINUE**, the scenario asks: “We need to ensure that we retain our order information even if our app goes down. Can guaranteed messaging help with that?” The two response choices are:

1. “Your app hasn't gone down yet, you're probably worrying over nothing.”
2. “Let's learn how guaranteed messaging could help protect that data!”

Choice 2 directly addresses the need to retain order information during application downtime. Select it and record the course's resulting feedback before advancing.

## Screen 3: Scenario response

I selected response 2, **“Let's learn how guaranteed messaging could help protect that data!”** Haroldo responds: **“Thank you! I definitely need to know more.”** The screen offers another **CONTINUE** control.

## Screen 4: Scenario conclusion


## Screen 5: Introduction to Guaranteed Messaging

The course contrasts **Direct Messaging** and **Guaranteed Messaging**. Direct Messaging is appropriate when loss is tolerable, such as for regular update messages or where an application has a built-in retry mechanism after a request timeout. Guaranteed Messaging is appropriate when loss is unacceptable, such as when every message contains critical data or when consumers may be slow or offline.

### Slow subscribers

The lesson first notes that message build-up in a Direct Messaging situation can cause message loss. Adding a **Persistent Queue** gives a slow consumer “shock absorption.” Persistent queues have much greater storage capacity than transport buffers and can handle large bursts of incoming data. Once the condition clears, the consumer drains its backlog, enabling lossless application recovery. The embedded Slow Subscribers video played through to its end (about 0:36) at 2× with audio muted. The player exposed no captions or transcript control; the surrounding written explanation is preserved here.

### Offline subscribers

The lesson asks: “How could guaranteed messaging help in the case of an offline consumer?” During an application failure or network outage, the persistent queue prevents undelivered messages from being discarded and collects messages while the consumer is offline. When the consumer returns, in-flight messages are redelivered; the consumer drains its backlog to complete lossless application recovery. The embedded Offline Subscribers video played through to its end at 2× with audio muted. The player exposed no captions or transcript control; the surrounding written explanation is preserved here.

### Solace Guaranteed Messaging

With Guaranteed Messaging, message movement is often called **guaranteed delivery**. Guaranteed delivery provides **at-least-once** delivery. The lesson introduces two perspectives for explaining this guarantee: the producer and the consumer.

### Producer acknowledgement

Producers using persistent messaging receive a per-message notification of whether the message was delivered successfully. These notifications are acknowledgements (**ACKs**). The Solace message router acknowledges a message only after safely storing it in the **ADB**. Multiple messages may be in flight at the same time. With fault-tolerant pairs, messages are also copied to the mate ADB before the producer receives the acknowledgement.

### Message rejection

If a message cannot be delivered, the Solace message router rejects it by sending a negative acknowledgement (**NACK**) to tell the producer delivery failed. One example is an ACL Profile rule that does not permit the producer to send messages to a given queue.

### Consumer acknowledgements

For consumers using Guaranteed Messaging, the router retains messages in persistent storage until they are acknowledged. Multiple messages may be in flight at once. For fault-tolerant pairs, consumer acknowledgements remove messages from both routers.

### Message order

Many exchanges involve multiple producers and consumers. Solace Guaranteed Messaging assures applications that messages are received in the same order in which the Solace message router accepted them.

### Visual and media recovery

The accessibility view exposes four image controls after **Producer Acknowledgement**, **Message Rejection**, **Consumer Acknowledgements**, and **Message Order**, but no alt text or direct asset link. The embedded SCORM view cannot currently produce a Chrome screenshot, so these four course diagrams and the two video posters are not saved; retain this as an explicit retrieval gap rather than creating replacement imagery. The Slow Subscribers video (about 0:36) and Offline Subscribers video played through at 2× with audio muted. Neither player exposed captions or a transcript control, so their narration is unavailable; the written explanations are preserved above.

## Visuals

No lesson-specific visuals have been saved locally yet. The opening scenario image and other SCORM diagrams are unavailable through the accessibility view; do not invent substitutes. Attempted Chrome screenshot capture timed out, and the Academy page asset inventory showed only LMS/course branding and tracking images rather than lesson diagrams.

## Screen 6: Understanding Guaranteed Messaging Patterns

The lesson defines a **queue** as a destination to which clients can publish and an endpoint to which consumers can bind to receive messages. Many consumers may bind to a queue, but each individual spooled message can be consumed by only one consumer. The original accessibility description of the diagram is: “a database icon on the left labeled ‘producer’ shows an arrow to an icon labeled ‘Solace’, which shows an arrow to the right to another database icon labeled ‘consumer’.” The original diagram is not yet saved locally because this embedded view exposes no image URL and its screenshot capture is unavailable.

### Message exchange patterns - Point-to-Point tab

The screen has **POINT-TO-POINT**, **PUBLISH-SUBSCRIBE**, and **REQUEST-REPLY** tabs. Point-to-Point is selected initially. It says that explicitly directed exchanges suit some applications and asks how applications use persistent Point-to-Point messaging. Producers send to a named queue agreed upon by applications, and consumers receive those messages directly from that queue.

The **PUBLISH-SUBSCRIBE** tab says that a producer can send a message to multiple queues using topic-to-queue mapping: topic subscriptions are added to each queue so they can receive matching messages. One topic can map to multiple queues, making the pattern scalable. Messages are processed multiple times by different consumers, and each consumer gets its own copy.

The Last-Value Queue section also exposes a **1:22 audio player** with only Play and seek controls and no transcript. Its associated LVQ explanation is preserved above. The diagrams in the pattern sections have no direct links or accessible descriptions, and the embedded SCORM view cannot produce a usable screenshot.

The **REQUEST-REPLY** tab says that applications achieve two-way communication using separate Point-to-Point channels: one carries requests, the other carries replies. Its diagram has no accessible description or direct asset link, and the embedded SCORM view cannot produce a usable screenshot, so the original diagram is not saved locally.

### Queue durability

The course says the main difference between **Durable** and **Non-Durable** endpoints is their lifecycle, with differences also in consumers and names.

| Property | Durable | Non-Durable |
|---|---|---|
| Lifecycle | Explicitly created and deleted by administrators or client applications; supports lossless HA failovers and lossless DR failovers. | Explicitly created and deleted by client applications only; automatically deleted if the client is disconnected for more than **60 seconds**; supports lossless HA failovers. |
| Consumers | One or many consumers. | A single consumer. |
| Name | Administrator-defined or application-defined. | Application-defined or automatically generated. |

### Dynamic provisioning

Some application teams want to manage their own durable endpoints without administrator access. Solace APIs let applications create durable endpoints; creation is separate from connecting to the endpoint, so becoming a consumer is optional. A client application may create its own queue and delete queues it created. Deleting an endpoint also deletes all contained messages. These operations do not require an administrator account, but the application must be granted permission to perform them.

### Template queue

A template queue can control properties of client application-created queues. The queue is referenced in the client profile.

### Last-Value Queue

The image's accessibility description says that some producers read input from a file, database, or another queue and can use that external state to resume after restart. Other publishers have no state repository; a **Last-Value Queue (LVQ)** can provide one. Creating a Solace Queue with `max-spool-usage` set to zero makes it an LVQ. It holds one message of any size up to the maximum accepted message size. Administratively or programmatically, a topic that specifically targets one publisher through a well-defined topic namespace should be associated with the LVQ. The queue retains the last message successfully published by that publisher. After a crash or reconnect, the producer can bind to the LVQ and read that message to learn where it left off in its publication stream. Consumers interested in several publishers should use a wildcard at the topic level that identifies the publisher. The original LVQ illustration is not saved locally because no asset URL or usable screenshot is exposed.

### Queue access type and consumer redundancy

Consumer-application outages may be too disruptive to risk a single consumer. For an **Active/Standby Cluster**, Exclusive Queues let a standby consumer take over when the active consumer disconnects. Because only one consumer is active at a time, this preserves message processing order. With **Non-Exclusive Queues**, multiple consumers may be active simultaneously. If one disconnects, its unacknowledged messages are redistributed to the other active consumers. This permits parallel processing but does not guarantee message processing order. The lesson also presents **Load Balancing Cluster** and **Consumer Scalability** sections whose detailed content has not yet been inspected.

### Queue browsing

Queue browsing lets a client application read messages from a queue without consuming them. Browsing is not guaranteed to expose every message, and it can be used to delete problematic messages when necessary.

### Message replay

A client application can request messages hours or days after their original delivery. Replay can start at a specific time or at the beginning of the replay log, and can be initiated by client applications or administrators. Messages may be replayed to a fully qualified topic, a wildcard topic, or a wildcard subscription. For example, a queue subscribed to `orders/>` can request replay, and the event broker delivers replay-log messages matching `orders/>`. Replay can be enabled or disabled per Message VPN, and replay-log size is configurable per Message VPN. The section's embedded video (about **1:47**) played through to the end at 2× with audio muted; no captions or transcript control was exposed.

### Handling features and Dead Message Queues

The lesson introduces cases where queued messages may not be delivered and two possible paths for discarded messages: delete them or route them to a **Dead Message Queue (DMQ)**. Any endpoint, whether a queue or DTE, can have an associated DMQ.

For a message that expires out of an endpoint, it must be flagged as DMQ-eligible by the publisher; this per-message flag is **false by default**. A DMQ must also exist and be associated with the endpoint that held the message. DMQs do not respect Time to Live (**TTL**) and may have no limit on delivery attempts. The lesson recommends an active consumer that drains the DMQ to prevent buildup. The consumer can log useful information because moved messages retain their original headers, including their original destination.

The **Message Rejection Handling** section's embedded video (about **0:40**) played through at 2× with audio muted. The player exposed no captions or transcript control, and its detailed visual actions could not be transcribed from this view.

The **Priority Based Congestion Handling** section contains an embedded video (about **1:13**) that played through at 2× with audio muted. The player exposed no captions or transcript control, and its detailed visual actions could not be transcribed from this view.

### Solace endpoints and queues versus topic endpoints

A Solace endpoint is a virtual object that spools or stores messages. There are two types: a **queue** and a **topic endpoint**. A Solace topic is not the same thing as a Solace topic endpoint.

| Property | Queue | Topic Endpoint |
|---|---|---|
| Inbound | Addressable by name; optionally has many topic subscriptions. | Not addressable by name; has a single topic subscription; optional inbound message filtering. |
| Storage | Stored messages are unaffected by subscription changes. | Stored messages are deleted when subscriptions change. |
| Outbound | One or many consumers; optional outbound message filtering; queue browsing. | One or many non-exclusive consumers; JMS durable subscriber. |

### Publish-Subscribe with topic endpoints

Distributing messages to all interested consumers can provide efficiency, scalability, and flexibility. Producers publish to an agreed topic structure. Consumers may receive through queues or topic endpoints. Queues can have multiple topic subscriptions and attract matching messages, so one queue per consumer may be enough. Topic endpoints use a topic subscription but allow only one topic; a consumer needing multiple subscriptions needs multiple topic endpoints.

### Message filtering with topic endpoints

Applications can receive a subset of messages by using a well-designed topic structure and wildcards. Topic-subscription filtering takes advantage of Topic Routing Blade performance and is the recommended option. Consumers may also use inbound or outbound selectors to filter on message-header properties.

### Message rejection handling with topic endpoints

Producers using Guaranteed Delivery are notified when messages have been persisted. For fan-out to many endpoints, the usual behavior is all-or-nothing: if any one endpoint rejects a message, it is not queued to any endpoint and the producer receives a rejection notification. This is generally desired because it keeps consumers consistent, and is the default for queues. Individual endpoints may instead be configured so inbound discards do not reject the message. This lowers the delivery guarantee and may create inconsistency between consumers; it is the default for Topic Endpoints.

### Visual recovery and remaining interactions

The queue-flow and LVQ images expose useful alt descriptions above but no downloadable source link; they are not saved locally. The **REQUEST-REPLY** diagram and images around queue durability, dynamic provisioning, template queues, active/standby, load balancing, consumer scalability, DMQ handling, and topic endpoints have no descriptive alt text or source links and are not saved locally. The four diagrams in the preceding introduction for producer acknowledgements, message rejection, consumer acknowledgements, and ordering, plus its two video posters, also remain unavailable to local capture. The Load Balancing Cluster and Consumer Scalability images were opened in their zoom views; neither exposed additional text or an asset link. All three pattern tabs are recorded; no further explanatory text was exposed by these image controls.

## Screen 7: Managing Guaranteed Messaging - Guaranteed Messaging Environments


### Managing resources and spool quotas

The system-level resource limits depend on the platform, SolOS version, and attached SAN storage capacity. A system administrator configures Guaranteed Messaging limits for each Message VPN. Limits can also be set inside a VPN for endpoints and client usernames. Four interactive markers are visible for **System Limits**, **Message VPN Limits**, **Endpoint Limits**, and **Client Username Limits**; their expanded descriptions are still to be inspected.

Persistent messages are stored in the message spool. At the system level, maximum spool disk usage should match the attached SAN or allocated disk capacity. Each Message VPN has a separate quota for its spool usage, and each queue or topic endpoint within a VPN also has a quota. Capacity planning must consider expected message rates and sizes together with the maximum acceptable consumer downtime.

### Message spool accounting and endpoint counts

A persistent message sent to a Message VPN counts toward that VPN's quota once, even if delivered to several endpoints. When delivered to multiple endpoints, it counts toward each endpoint's quota. The next section explains that endpoints contain persistent messages, and maximum endpoint count depends on platform and SolOS version. Administrators can set a per-VPN endpoint limit and use a client profile setting to limit how many endpoints a client username may own, controlling application-created endpoints. Two diagrams are exposed only as zoom controls and need inspection.

### Flow limits, status, statistics, and events

The embedded **Flow Limits** video played through and looped at 2× with audio muted; its player exposed no captions or transcript. Solace routers expose status and statistics for configured entities through the CLI or SolAdmin (SEMP), including Message VPNs and individual queues. Guaranteed Messaging events provide an additional monitoring mechanism. Configured thresholds raise real-time events before hard limits are exceeded. Events are logged as a historical record and can be pushed through remote syslog, consumable application messages, or both, enabling existing monitoring integrations and custom event handlers.

### Managing access

Guaranteed Messaging consumes more system resources than non-persistent messaging, so access control is central to managing the environment. The embedded video under **Sending and Receiving Guaranteed Messages** remains to be inspected. Queue topic subscriptions can be changed by administrators or client applications, unlike topic-endpoint subscriptions. Administrators with read-write or admin access can modify a queue's topic subscriptions through the CLI or SolAdmin without ACL Profile topic restrictions. Client applications can modify a queue's topic subscriptions through Solace APIs when granted at least **Modify Topic** permission for that queue.

### Creating and deleting endpoints

The **Creating Endpoints** accordion says administrators with read-write access can create durable endpoints through the CLI or SolAdmin (SEMP). An administrator-created endpoint initially has no owner, and non-owners have permission level **None**; the administrator must assign an owner or grant non-owners more permission before consumers can use it. Applications can be granted endpoint-creation access through their assigned client profile; when enabled, applications can create durable and non-durable endpoints. A related diagram is exposed only as a zoom control and has no accessible description.

The **Deleting Endpoints** accordion says endpoints can be deleted by administrators or client applications, but applications have fewer deletion rights. Deleting any endpoint also deletes all messages it contains. Administrators with read-write access can delete a durable endpoint after shutting it down. An application may delete only an endpoint it created and must have **Delete** permission for that endpoint. The creation and deletion diagrams are available only through zoom controls without accessible descriptions.

### Visuals and media

Four markers, seven zoomable diagrams, and two videos are present on this page. The markers and both endpoint accordions are recorded. The Flow Limits video played through and looped at 2× with audio muted; the **Sending and Receiving Guaranteed Messages** video reached the end at 2× muted, where the player offered Play/Play Video again. Neither player exposed captions or a transcript. Opening zoom controls revealed only an Unzoom image control, without image descriptions. Chrome screenshot capture timed out; the Academy page asset inventory contained no instructional SCORM images. These seven diagrams remain documented retrieval gaps rather than recreated visuals.

## Screen 8: Guaranteed Messaging Quiz

The fifth and final SCORM section is **Quiz**. Its first item says: **“Match the scenario to the best messaging type for each. Click and drag the scenario to either Direct Messaging or Guaranteed Messaging.”** It contains six cards. Based on the course's loss-tolerance and critical-data distinction, the best matches are:

- **Financial trading updates** - Direct Messaging, where timely current updates take priority over delivery assurance.
- **Hospital patient information** - Guaranteed Messaging, because critical patient information must not be lost.
- **Live sports updates** - Direct Messaging, where the latest score matters more than receiving every update.
- **Order processing** - Guaranteed Messaging, to preserve critical order data across application downtime.
- **Rideshare location updates** - Direct Messaging, where fresh location updates are more useful than retransmitting every old update.
- **Bank transfers** - Guaranteed Messaging, because transaction records must not be lost.

When first inspected, the sorting activity showed **0/6 Cards Correct**.

The first multiple-choice question asks: **“Which feature of Solace's guaranteed messaging ensures that messages are not lost even if the subscriber is temporarily disconnected?”** The choices are **low latency transmission**, **high throughput**, and **persistent storage**. The best answer is **persistent storage**, which retains messages while a subscriber is offline.

The second question asks: **“Which of the following scenarios is best suited for the use of guaranteed messaging in Solace?”** Its choices are **transmitting real-time stock market data to traders where speed is more critical than delivery assurance**; **sending a firmware update notification to IoT devices where it's crucial that every device receives the message**; **distributing live sports scores to a mobile app where the latest update is more important than ensuring all messages are received**; and **streaming video content to users where continuous flow without interruption is prioritized over delivery of every data packet**. The best answer is the **firmware update notification**, because delivery to every device is required.

At the initial quiz inspection, both multiple-choice items showed **Incorrect** and **TAKE AGAIN**. No selected answer was exposed in the accessibility tree, so the choices from those earlier failed attempts cannot be recovered. Both questions were later retried successfully; the results and exact feedback are recorded in the retry log below.

### Sorting activity - recorded attempts

1. **Financial trading updates → Direct Messaging** - correct; the activity changed from **0/6** to **1/6 Cards Correct** and advanced to the next card.
2. **Hospital patient information → Guaranteed Messaging** - correct; the activity changed to **2/6 Cards Correct** and advanced to **Live sports updates**.
3. **Live sports updates → Direct Messaging** - correct; the activity changed to **3/6 Cards Correct** and advanced to **Order processing**.
4. **Order processing → Guaranteed Messaging** - correct; the activity changed to **4/6 Cards Correct** and advanced to **Rideshare location updates**.
5. **Rideshare location updates → Direct Messaging** - correct; the activity changed to **5/6 Cards Correct** and advanced to **Bank transfers**.
6. **Bank transfers → Guaranteed Messaging** - correct; the activity shows **6/6 Cards Correct**.

### Multiple-choice retry log










The video controls currently show **Play Video** even though earlier session notes recorded playback to the end; despite that earlier viewing, Introduction remains at 88%. Replaying and letting both videos reach their natural end is the next completion check.

**Next:** Play the Slow Subscribers video to the end, record what it shows and any feedback/progress change, then do the same for Offline Subscribers before leaving the section.

### Screen 12: Slow Subscribers video reached its end


**Next:** Play the **Offline Subscribers** video through to the end and check whether the Introduction progress changes.

### Screen 13: Offline Subscribers video reached its end


**Next:** Inspect the four zoomable diagrams and any remaining interactive controls in Introduction, then revisit the section outline to identify what is still unmarked before proceeding to Patterns.

### Screen 14: Producer Acknowledgement diagram

Opening the **Producer Acknowledgement** zoom control displays a three-unit producer/server icon on the left, a right-pointing message arrow, and a large box labeled **Guaranteed Messaging** on the right. This provides a visual for producer-to-router message flow. The modal exposes **Unzoom image**; it supplies no download control or caption. I recorded the visible labels and direction, then closed the zoom view. The course diagram could not be saved as a local file from this screenshot interface.

**Next:** Return to the Introduction page, check whether viewing this image changes section progress, then inspect the remaining zoomable diagrams before advancing.

### Screen 15: Message Rejection diagram

The **Message Rejection** zoom view shows a producer sending to **“Q1”** toward the **Guaranteed Messaging** router. An **ACL Profile** box says **“Disallow all Sends except ‘Q2’”**, and the flow has a **NACK** marker, illustrating rejection when a producer's ACL does not authorize the queue destination. The modal exposes **Unzoom image**; no download or caption is available. The diagram was inspected and described in text because a local image asset cannot be saved from the screenshot interface.

**Next:** Close the zoom view, inspect the Consumer Acknowledgements diagram, then the Message Order diagram.

### Screen 16: Introduction marked complete


**Next:** Open the **Consumer Acknowledgements** zoom image, record the flow and labels, then inspect the Message Order diagram.

### Screen 17: Consumer Acknowledgements diagram


**Next:** Close the zoom view and inspect the Message Order diagram.

### Screen 18: Message Order diagram

The **Message Order** zoom view shows producers on the left, a Solace router in the center, and consumers on the right. Two internal streams are each labeled **“A and B”**; the diagram marks messages **A1, A2, B1, and B2** and uses arrows to depict traffic through the router to consumers. It visually accompanies the rule that the router preserves the order in which it accepts messages. The exact mapping of each numbered marker is not text-labeled, so I recorded only the visible labels and roles. The modal exposes **Unzoom image** and no download control; the screenshot interface does not provide a local asset save path.




**Next:** Open each message-exchange pattern tab, record its text and diagram, and check whether changing the tabs advances the section.

### Screen 20: Publish-Subscribe pattern tab

The **PUBLISH-SUBSCRIBE** tab says a producer sends messages to multiple queues by topic-to-queue mappings, where topic subscriptions are added to each queue. One topic may map to several queues for scale; different consumers then process their own copy of a message. The diagram shows a producer publishing to a topic and branching toward queues; the visible first queue is **Q1** with topic subscription **`training/>`**, feeding a consumer. A lower branch is below the screenshot viewport. The screenshot interface provided no local save path for this course diagram, so the visible portion and its limitation are recorded in text.

**Next:** Open the **REQUEST-REPLY** tab and record its explanation and diagram.

### Screen 21: Request-Reply pattern tab

The **REQUEST-REPLY** tab says two-way application communication uses separate point-to-point channels: one for requests and another for replies. Its diagram shows a producer on the left sending through a **Request Queue** to a consumer on the right; the consumer sends a response back through a separate **Reply Queue**. The screenshot interface did not provide a local save path for the diagram. The Patterns section remains at **40% Completed** after visiting this tab; its other visible content and visuals still need review.

**Next:** Review the queue durability, provisioning, and queue-access sections and their interactive media/diagrams, recording each view before proceeding.

### Screen 22: Queue Durability and Dynamic Provisioning

The Queue Durability comparison shows:

| Property | Durable | Non-Durable |
|---|---|---|
| Lifecycle | Explicit create/delete by administrators or client applications; lossless HA and DR failovers | Explicit create/delete by client applications only; automatically deleted after the client disconnects for more than 60 seconds; lossless HA failovers |
| Consumers | One or many | Single |
| Name | Administrator- or application-defined | Application-defined or automatically generated |

The following **Dynamic Provisioning** section asks how application teams can manage durable endpoints without administrator access. Solace APIs let applications create durable endpoints separately from connecting to them, so becoming a consumer is optional. The associated creation/deletion illustrations continue below the viewport. No local screenshot file path is available for these course visuals.

**Next:** Continue down Dynamic Provisioning and record the endpoint-creation and deletion diagrams and any interaction controls.

### Screen 23: Dynamic Provisioning and Template Queue


**Next:** Continue to Last-Value Queue, listen to its audio, and inspect the accompanying diagram.

### Screen 24: Last-Value Queue illustration and Queue Access Type

The diagram shows **Producer: Sender1** publishing to three destinations. A one-message **Queue: Sender1_LVQ** has topic subscription **`*/Sender1/>`**; ordinary queues **Q1** and **Q2** each show **`LOB/*/topic/namespace`** subscriptions and feed separate consumers. This accompanies the Last-Value Queue explanation: with `max-spool-usage` set to zero, the queue stores the publisher's latest message so the producer can recover its publication position after a crash or reconnect. The next heading, **Queue Access Type**, asks how redundant consumers can make message consumption fault tolerant. The screenshot interface offers no local image-save path.

**Next:** Listen to the 1:22 Last-Value Queue audio and capture its transcript or key points; then review the Active/Standby, Load Balancing, and Consumer Scalability diagrams.

### Screen 25: Last-Value Queue audio completed

The embedded Last-Value Queue audio played through its full **1:22**. The player returned to **Play** and reset the seek position; no transcript or caption control was exposed. The page's accessible description explains that producers with an external source can recover their position after a failure, while stateless publishers can use an LVQ. An LVQ has `max-spool-usage` set to zero and stores the last successfully published message (one message, up to the maximum message size). A publisher-specific topic subscription lets a reconnecting producer read that message and determine its prior publication position; consumers following multiple publishers use a wildcard that identifies publishers in the topic. Patterns progress reached **68% Completed** during the audio interaction.

**Next:** Continue to Queue Access Type and inspect the Active/Standby, Load Balancing, and Consumer Scalability diagrams.

### Screen 26: Queue Access Type - Exclusive and Non-Exclusive

The page asks how to make message consumption fault tolerant when consumer outages are disruptive. **Exclusive Queues** support an active/standby pair: if the active consumer disconnects, the standby takes over, and only one consumer is active, preserving message-processing order. The diagram labels queue access type **Exclusive**, with arrows to **Active** and **Standby** consumers. **Non-Exclusive Queues** allow several consumers to be active in parallel; on disconnect, that consumer's unacknowledged messages are redistributed to the other active consumers. This permits parallel processing but does not guarantee message order. The screenshot shows the start of a second diagram with active consumers; its lower part continues below the viewport. The course visual could not be saved locally from the screenshot interface.

**Next:** Continue through the Active/Standby, Load Balancing, and Consumer Scalability illustrations and record each diagram.

### Screen 27: Consumer clusters and Queue Browsing

The **Consumer Scalability** illustration contrasts an **Exclusive queue**, which maintains per-topic order, with a **Non-Exclusive queue**, where message-consumption order depends on fast versus slow consumers and a disconnect triggers consumer redistribution. The page's nearby text explains that Exclusive Queues allow a standby to take over while preserving order; Non-Exclusive Queues redistribute unacknowledged messages and support parallel consumption without order guarantees. **Queue Browsing** says a browser reads messages without consuming them, is not guaranteed to see every message, and can delete problematic messages. The screenshot shows both diagrams above this text; course screenshots cannot be saved to local files through this interface.

**Next:** Play the Message Replay video to completion, then continue through Handling Features and Dead Message Queue. Current visible evidence remains **60% COMPLETE** overall and **70%** for Patterns.

### Screen 28: Message Replay

Message Replay lets a client request delivery hours or days after the original delivery. A replay request can start at a specified time or at the beginning of the replay log, and either a client application or an administrator can initiate it. Replay supports a fully qualified topic, a wildcard topic, or a wildcard subscription; for example, a queue subscribed to `orders/>` can receive replay-log messages matching that wildcard. Replay can be enabled or disabled per Message VPN, and the replay-log size is configurable per Message VPN.

The 1:47 embedded video played through to its end at 2× speed with audio muted. A visible slide titled **“Message Replay Protects Your Event Data”** diagrams a publisher sending an event to Solace PubSub+; the broker writes the event to both a queue and the Replay Log, and replay storage continues after all subscribers have received the event. A visible subtitle fragment says, **“but they will remain in the replay log.”** No separate transcript control appeared, so the text and diagram on the course page plus this captured subtitle fragment are recorded without claiming a full transcript. The rendered screenshot could not be exported to a local file through the available screenshot interface, and no course-linked download for this video slide was exposed; no local image is linked.

**Next:** Continue into Handling Features and Dead Message Queue, recording the next screen before scrolling.

### Screen 29: Handling Features and Dead Message Queue prerequisites


**Next:** Scroll to reveal the rest of the DMQ illustration and handling rules, then record them before advancing.

### Screen 30: Dead Message Queue behavior and Message Rejection Handling


**Next:** Inspect the full DMQ diagram using its zoom control, then capture the Message Rejection Handling and Priority Based Congestion Handling media before scrolling onward.

### Screen 31: Dead Message Queue decision diagram

The zoomed diagram shows a message in a **Queue** going to a **Consumer** during normal delivery. If the message loses delivery eligibility, it reaches a decision labeled **“DMQ?”**: **No** leads to a delete/recycle bin, while **Yes** routes the message into a **Dead Message Queue**, whose messages are then delivered to a separate consumer. The zoom control provides no download option. This diagram is described here because the current Chrome screenshot API displays the captured screen but does not expose a local image path for saving it into the lesson's `img` folder.

**Next:** Close the zoom view, inspect the Message Rejection Handling media and its full diagram, and record the content before scrolling.

### Screen 32: Message Rejection Handling fan-out example


**Next:** Play the Message Rejection Handling video through to the end and capture its captions or key points before continuing.

### Screen 33: Message Rejection Handling video completed

The embedded Message Rejection Handling video ran to **100%** and reset to its Play control; playback was **0:40** at **2×** with audio muted. Its visible fan-out diagram matches Screen 32: `training/topic` is routed to Q1, Q2, and full Q3, with rejection shown for Q3. One subtitle fragment visible during playback was **“In the fan out case.”** No separate transcript control appeared, so this is not a full transcript. The text later in the lesson states the associated queue behavior: if any endpoint rejects a guaranteed message in fan-out, it is queued to none of the endpoints and the producer is notified; queues use this as the default behavior. The rendered course visual has no exposed download path, and the browser screenshot action does not provide a local file path.

**Next:** Play the Priority Based Congestion Handling video to completion and record any captions or instructional points before scrolling.

### Screen 34: Priority Based Congestion Handling video completed


**Next:** Inspect the Solace Endpoints diagram and the comparison between queues and topic endpoints before continuing.

### Screen 35: Solace endpoints and queue versus topic-endpoint comparison

The screen distinguishes Solace topics from Solace topic endpoints. A Solace endpoint is a virtual object that stores messages; the two types are queues and topic endpoints. The comparison table shows:

| Property | Queue | Topic Endpoint |
|---|---|---|
| Inbound | Addressable by name; optionally has many topic subscriptions. | Not addressable by name; has a single topic subscription; optional inbound message filtering. |
| Storage | Stored messages are unaffected by subscription changes. | Stored messages are deleted with subscription changes. |
| Outbound | One or many consumers; optional outbound message filtering; queue browsing. | One or many non-exclusive consumers; JMS durable subscriber. |


**Next:** Inspect the Publish-Subscribe with Topic Endpoints diagram, then record its details and finish the remaining Patterns content.

### Screen 36: Publish-Subscribe with Topic Endpoints

The zoomed diagram shows two producers publishing `training/topic` and `second/topic`, four topic-subscription endpoints, and two consumers. The first topic routes to two endpoints subscribed to `training/>`; the second routes to two endpoints subscribed to `second/topic`. The upper two endpoints feed one consumer and the lower two feed another. The lesson text explains that queues may hold multiple topic subscriptions, so one queue per consumer can attract several topics; a topic endpoint has one topic subscription, so a consumer needing multiple subscriptions needs multiple topic endpoints. The pattern can provide efficiency, scalability, and flexibility. A Chrome screenshot was captured and inspected, but no local image file could be obtained from the screenshot control and no source download was exposed.

**Next:** Record the filtering and message-rejection sections and inspect the rejection diagram.
### Screen 37: Topic endpoint filtering and message rejection

Topic-subscription filtering lets applications select a subset of messages through a well-designed topic structure and wildcards. The lesson recommends it because it uses the Topic Routing Blade for performance. Consumers may also use inbound or outbound selectors to filter on message-header properties.

The **Message Rejection Handling with Topic Endpoints** section says Guaranteed Delivery producers are notified when messages have been persisted. In fan-out, the default all-or-nothing behavior rejects the publication if any endpoint rejects it: the message is queued to none of the endpoints and the producer is notified, preserving consistency across consumers. This is the default for queues. Individual endpoints can be configured so inbound discards do not cause rejection; this reduces delivery guarantees and can leave consumers inconsistent. That is the default for Topic Endpoints. The zoomed diagram shows a producer publishing `training/topic` to three topic endpoints (TE1, TE2, and TE3), each subscribed to `training/>`, with a consumer attached to each endpoint. TE1 and TE2 show green acceptance checks; TE3 shows a red rejection mark. This visual represents endpoint-level acceptance and rejection during fan-out. A Chrome screenshot was captured for review, but the screenshot tool did not provide a local file path and no course asset download control was exposed.


### Screen 38: Managing Guaranteed Messaging - environment overview


The **System Limits** marker opens a callout stating that limits are based on platform and SolOS version. The screenshot shows this callout over the resource-limit illustration; its attached-SAN context is stated in the surrounding text. The image remains unavailable as a local file.

The **Message VPN Limits** marker opens a callout stating that these limits are **Configured by System Administrator**. Its screenshot was captured; this callout is displayed over the same resource-management illustration and no local image file was exposed.

The **Endpoint Limits** marker opens the callout **Within the Message VPNs**. The screenshot confirms the marker position on the resource-management illustration; no local file was available.

The **Client Username Limits** marker also opens a callout reading **Within the Message VPNs**. Its position is captured in Chrome over the resource-management illustration, but no local image file was exposed.

**Next:** All four resource-limit markers have been viewed. Continue to Message Spool Quotas and Message Spool Accounting.

### Screen 39: Message spool quotas and accounting

All persistent messages use the message spool. At the system level, maximum spool disk usage should match the capacity of the attached SAN or allocated disk. Each Message VPN has a separate quota, and each queue or topic endpoint within the VPN has its own quota. Capacity planning should account for expected message rates and sizes plus the maximum acceptable consumer downtime.

The zoomed **Message Spool Accounting** diagram shows a **1 MB** message delivered into one Message VPN and routed to **Queue 1** and **Queue 2**; **Queue 3** receives no copy. Quota accounting in the diagram is **System +1 MB**, **Message VPN +1 MB**, **Queue 1 +1 MB**, **Queue 2 +1 MB**, and **Queue 3 ---**. This illustrates that the Message VPN counts the persistent message once even when it is delivered to multiple endpoints, while each receiving endpoint counts it toward its own quota. The screenshot was captured for inspection, but no local image file was exposed.

**Next:** Continue to endpoint-count limits and record the following management sections.

### Screen 40: Endpoint counts and flow limits

The **Limiting the Number of Endpoints** section says endpoints store persistent messages; maximum counts depend on platform and SolOS version. Administrators can impose a per-Message VPN endpoint limit and cap how many endpoints a client username may own through its assigned client profile, which controls application-created endpoints.

The visible **Flow Limits** diagram shows maximum ingress limits of **5**, **5**, and **1** for Client Usernames 1–3, and maximum egress limits of **50**, **50**, and **10**. The example Message VPN has maximum ingress and egress flows of **1,000** each; Client Usernames 1 and 2 map to Client Profile 1 (ingress 5, egress 50), while Client Username 3 maps to Client Profile 2 (ingress 1, egress 10). The diagram also notes that a queue's **Max Bind Count** property limits egress flows. The embedded Flow Limits video played to **100%** at **2×** with audio muted. It showed the example limits and client-profile mapping described above, with **Max Bind Count** identified as another egress-flow limit. No transcript or captions were exposed. A screenshot was captured; no local image path was available.

**Next:** Continue to Status and Statistics, then Guaranteed Messaging Events.

### Screen 41: Status, statistics, and guaranteed-messaging events

The router exposes status and statistics for configured entities. Through the CLI or SolAdmin (SEMP), an operator can retrieve operational status for an entity such as a Message VPN or queue; all these entities maintain detailed statistics.

Guaranteed Messaging limits are hard limits: the router prevents actions that would exceed them. For each imposed limit, the router can also raise real-time events at configurable thresholds. The **Message Spool Usage (MB)** graph shows **CLEAR**, **HIGH**, and **EXCEED** threshold lines over time. Events are written to a log as a historical record and can provide early detection so administrators or applications can react. Configure them as push notifications through remote syslog, application-consumable messages, or both. This can integrate with existing syslog monitoring and support custom event handlers; many monitoring solutions use both methods. A Chrome screenshot was captured; no local image file was available.

**Next:** Continue to Managing Guaranteed Messaging Access and the send/receive guidance.

### Screen 42: Managing Guaranteed Messaging Access

Guaranteed Messaging uses more resources than non-persistent messaging, so administrators need controls over application access. The screen introduces **Sending and Receiving Guaranteed Messages** with a flow diagram divided into **Service Access**, **Destination Access**, and **Administrative Status**. Its visible send path starts at a producer using a client profile, is checked against an ACL Profile for the destination, and reaches a queue or topic endpoint with an administrative status. The diagram also depicts an administrator creating, updating, and deleting an endpoint. The zoomed diagram numbers the flow as **1 Sending**, **2 Receiving**, and **3 Administration**. A producer sends to a queue or topic endpoint, which delivers to a consumer. The administrator can create, update, and delete endpoints and add topic subscriptions; the consumer can receive and delete messages. The image distinguishes service access, destination access, and endpoint administrative status. A Chrome screenshot was captured, but no local image file or download control was exposed.


### Screen 43: Sending and receiving access controls


### Screen 44: Queue topic subscriptions and endpoint permissions

Unlike topic endpoints, queue topic subscriptions may be modified by users other than the active consumer. Administrators with read-write or admin access can add or remove queue subscriptions through the management interface, CLI, or SolAdmin (SEMP); ACL Profiles only restrict client applications. Client applications using Solace APIs need at least **Modify Topic** permission for the queue. The **Endpoint Ownership & Permissions** table shown in the tutorial grants **Browse Messages** to Read Only, Consume, Modify Topic, and Delete; **Acknowledge Messages** to Consume, Modify Topic, and Delete; **Add/Remove Topic Subscriptions** to Modify Topic and Delete; and **Delete Endpoint** only to Delete. The Delete Endpoint permission marked with an asterisk applies only to application-created endpoints. The accompanying queue diagram shows the application asking to modify topic subscriptions on a queue; the ACL Profile allows **Modify Topic Subscriptions**, while an administrator performs the change with read-write access. The table and diagram were captured and inspected in Chrome; no local screenshot file was exposed. **Next:** Expand Creating Endpoints and record its contents before opening Deleting Endpoints.

### Screen 45: Creating endpoints


### Screen 46: Deleting endpoints
