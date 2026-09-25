# VPN Bridges

- **Course:** Solace Event Broker Administration
- **Syllabus section:** VPN Bridges
- **Academy content type:** SCORM

## Lesson notes

### Screen 1: Academy lesson page

The Academy course page is open to **VPN Bridges**. It reports **8 of 14 lessons completed**. The syllabus marks **High Availability — 1 of 1 completed**, **Data Replication — 1 of 1 completed**, and **Guaranteed Messaging — 0 of 1 completed, In progress**. **VPN Bridges** is the selected lesson and shows **0 of 1 completed**; the page identifies **Data Replication** as the previous lesson and **Dynamic Message Routing** as the next. The Academy view offers **Expand lesson view**; the SCORM course content has not yet been opened.

**Next:** Expand the lesson view and record its initial SCORM screen before proceeding.

### Screen 2: SCORM course overview

The SCORM course title is **VPN Bridge**. Its overview describes a comprehensive exploration of the Virtual Private Network (VPN) Bridging Model: its core principles and architecture, how it supports secure and efficient communication between disparate VPNs, and deployment scenarios with scalability, security, and performance requirements. The table of contents lists four items, all **Unstarted**: **What's the Scenario?** under **The Context**; **Understanding VPN Bridges** and **VPN Bridge Topologies and Direction** under **The Concept**; and **Quiz** under **The Click**. The overview offers **START COURSE**. No instructional image is exposed on this screen.

**Next:** Start the course and record its first screen before interacting.

### Screen 3: What's the Scenario?

This is **Lesson 1 of 4**. Haroldo says: **“Hi! I'm Haroldo. My middleware team at ACME Retail needs to figure out how to control the flow of messages between our teams.”** A **CONTINUE** button is visible. The SCORM module shows **0% COMPLETE** and all four sections remain **Unstarted** on this initial screen.

**Next:** Continue to reveal the scenario question and response choices; record them before selecting an answer.

Continuing shows Haroldo's specific need: **“I need to help our order management group send a subset of messages to to the finance system to let them know to process transactions. There's a separate Message VPN for each of the app teams.”** The course text contains the duplicated **“to to”** as shown. Two responses are offered: **(1)** “Just allow access to all of the transaction information.” **(2)** “Hmm, maybe VPN bridging can help. Let's take a look.” Response 2 proposes investigating VPN bridging to share a selected subset across separately isolated app-team VPNs.

**Next:** Select response 2 and record the course feedback before continuing.

Selecting response 2 leaves **“Hmm, maybe VPN bridging can help. Let's take a look.”** displayed under Haroldo's scenario. No separate correct/incorrect label or additional feedback is shown. The sidebar marks **What's the Scenario? Completed** and the module remains at **25% COMPLETE**; the **2 of 4 — Understanding VPN Bridges** link is available.

**Next:** Open **2 of 4 — Understanding VPN Bridges** and capture the content before interacting.

## Visuals

### Screen 4: Understanding VPN Bridges

This is **Lesson 2 of 4 — The Concept**. The SCORM header initially reported **25% COMPLETE**; after all three markers were opened and the page was reviewed, it reported **50% COMPLETE** and marked **Understanding VPN Bridges** Completed. In the table of contents, this item was initially marked **15% Completed** and later showed **54% Completed** before it completed. **What's the Scenario?** is also Completed, while **VPN Bridge Topologies and Direction** and **Quiz** are Unstarted.

#### What is a Message VPN Bridge?

Message-VPNs are isolated messaging environments in Solace. Messages published to a message-VPN are contained to that message-VPN. Message-VPN bridges provide a solution allowing messages to be shared between message-VPNs in a selective and controlled manner. Using message-VPN bridges, links can be created between message-VPNs on the same or separate appliances to share data. The messages that are allowed to flow from one message-VPN to another can be specified in the form of topic subscriptions. Message-VPN bridges can be configured to move data between message-VPNs using the direct or guaranteed messaging modes.

![Diagram of a VPN bridge connecting two isolated Message VPNs](img/vpn-bridge-overview.png)

Global Applications with datacenters across the world may need a way to share data between the regions. If these applications want to share messages selectively between regions, they can use message-VPN bridging.

![World map showing VPN bridging between Solace clouds in Amazon Services and Google Cloud Platform](img/global-vpn-bridge-regions.png)

Bridges can also be configured to share data between different clouds and on-premise.

![Architecture diagram showing VPN bridges connecting cloud and on-premise Solace deployments](img/vpn-bridge-across-clouds.png)

You can also use VPN bridges to connect Message-VPNs on different routers or the same router. The Message-VPNs can have the same or different names if they are on different routers.

![Diagram showing VPN bridges between Message VPNs on the same or different routers](img/vpn-bridges-between-routers.png)

#### Message VPN Bridge Model

The model can be broken down into three areas:

- The network connection between the message VPNs, which acts as the transport.
- Messages are attracted using topic subscriptions, acting as the attractors.
- The bridge client receives the messages from the source.

![Message VPN bridge model showing source and destination VPNs, transport, and bridge clients](img/vpn-bridge-model.png)

The labeled graphic exposes three markers: **Attractors**, **Transport**, and **Bridge Client**.

**Attractors marker:** “Topic subscriptions are used to control which messages are sent across message VPN bridges. As with consumers, a well-designed topic structure and the ability to use wildcards gives message VPN bridges the ability to only transmit the messages that need to be shared.”

**Transport marker:** “The network connection between the message VPNs acts as the transport.”

**Bridge Client marker:** “In this model, the bridge client is a Solace client. It connects to the ‘Remote’ message VPN using a client username and has a client profile and ACL profile applied. Also, as a client connected to the ‘Remote’ Message VPN, we get all the same detailed information that is available for all Solace clients, including detailed statistics, real-time events, and more.” All three model markers are now marked **Viewed**. The section progress was **54% Completed** immediately after opening Bridge Client, then changed to **Completed** and SCORM progress to **50% COMPLETE** after the page was reviewed.

#### Flexibility

One of the key benefits of the Message VPN Bridging Model is the flexibility that it offers:

- Customized **Topic Subscriptions** control the flow of messages.
- **Delivery Mode** options:
  - Direct messaging with at most once delivery.
  - Guaranteed messaging with at least once delivery.
- **Message Direction** choices:
  - Unidirectional bridging.
  - Bidirectional bridging.
- Alternative **Transport Modes**:
  - Compressed connections.
  - Encrypted connections.

#### VPN Bridge Delivery Mode

Message-VPN bridges for direct and guaranteed messaging both follow the same principles. For a pair of message-VPNs, bridges are always created on the message-VPN that is the destination for messaging traffic. The bridge, when created on the local (destination) message-VPN, connects to the remote (source) message-VPN and attracts messaging traffic towards it.

![Direct-message VPN bridge from a source VPN to a destination VPN through a bridge client](img/direct-message-bridge-delivery.png)

**Direct Messaging:** To use direct messaging, topic subscriptions are added to the bridge configuration in the “local” message VPN. Using its connection to the “remote” message VPN, these topic subscriptions are applied by the bridge client to attract messages across the bridge. The messages are then distributed in the “local” message VPN.

**Guaranteed Messaging:** Bridges using guaranteed messaging use a queue endpoint on the remote message VPN. Topic subscriptions are added to the queue in the “remote” message VPN. The bridge client binds to the queue to attract messages across the bridge. The messages are then distributed in the “local” message VPN.

![Guaranteed-message VPN bridge using a queue in the source VPN](img/guaranteed-message-bridge-delivery.png)

#### Mixed Delivery Modes

Message VPN bridges may be configured to use both delivery modes. The message delivery mode used depends on the matching topic subscription. You can map critical messages to topic subscriptions on the queue and bridge them to the destination messages VPN and map less critical messages like state messages with delivery mode of direct messaging.

If we have a two of the same topic subscription configured on the bridge but one has a guaranteed delivery mode and the other has a direct delivery mode, then the destination message vpn will get the same message twice. In order to avoid this, we would ensure that we have a separate topic name subscription on the bridge. If the topic space doesn’t naturally divide into guaranteed and direct delivery modes, consider including the `<DeliveryMode>` in the topic structure. This can simplify the configuration needed to ensure the desired delivery mode is used end to end when using both delivery modes.

![Diagram illustrating messages flowing across bridge clients with mixed direct and guaranteed delivery modes](img/mixed-bridge-delivery-modes.png)

**Next:** Open **3 of 4 — VPN Bridge Topologies and Direction**; all displayed text, visuals, and marker content from this section are saved above.

### Screen 5: VPN Bridge Topologies and Direction — Pipeline Topology selected

This is **Lesson 3 of 4**. SCORM reports **50% COMPLETE**. Under **Multi-Bridge Topologies**, the lesson says: “Message VPN bridges can be combined to share data beyond two message VPNs.” It introduces three message VPN topologies: **Pipeline**, **Fan-out**, and **Network**. The **PIPELINE TOPOLOGY** tab is initially selected; the other two tabs are available but have not yet been opened.

In the pipeline topology, also known as pipe and filter, messages can be published on the message VPN and bridged across another message VPN where the messages are filtered and published to the other message VPN. This allows the pipeline topology to provide controlled message flow.

**Visual gap:** The selected pipeline tab displays the original `pipe.png` diagram from course media key `rise/courses/T9kp5gYvYOK9lp21kq8yzi36D3XQAOGH/mdtP7BxMVBxITRCd-pipe.png`. The visible lesson page does not expose an accessible image description. The exact media key was recovered from the loaded lesson package, but direct retrieval from its media CDN returned HTTP 403; Chrome screenshot capture timed out. Therefore, no local screenshot or image file is available for this diagram at this checkpoint.

The same page includes the following **VPN Bridge Direction** content:

**Unidirectional Bridging:** “In the simplest case, a message VPN bridge is unidirectional, in that messages only move in one direction.” Unidirectional bridges can be useful in such cases as data centralization data from distributed locations or one-way data replication.

**Bi-directional Bridging:** “Extending the configuration of a unidirectional bridge by adding a bridge in the opposite direction results in a bidirectional bridge where message moves in both directions.” For bidirectional bridges, the topic subscriptions are configured separately, allowing for asymmetric sharing of messages. Also, bidirectional bridges share a connection and have automatic loop prevention, so even with overlapping Topic subscriptions, messages are prevented from being sent back over the link on which they were received. Bidirectional bridges can be useful in scenarios such as connecting regions for global applications or integrating interdependent applications within a region.

**Visual gaps:** The lesson shows original diagrams for unidirectional (`rise/courses/T9kp5gYvYOK9lp21kq8yzi36D3XQAOGH/IgGvpzE8JMwaf_VJ-uni.png`) and bidirectional bridging (`rise/courses/T9kp5gYvYOK9lp21kq8yzi36D3XQAOGH/uowFBXn8rAKg4tDc-vpn-bridge-bi.png`). These media keys were recovered from the loaded lesson package, but direct retrieval from the media CDN returned HTTP 403 and Chrome screenshot capture timed out, so no local copies are available.

**Next:** Open the Fan-out tab and record its displayed content before opening Network.

### Screen 6: Fan-out Topology tab

The **FAN-OUT TOPOLOGY** tab is selected. The lesson says: “The fan-out topology is useful when you have messages that are being published to one VPN and you would like that data to be published to multiple VPNs. The Fan-out topology provides controlled message distribution.”

**Visual gap:** The tab displays its original fan-out diagram (`fanout.png`; media key `rise/courses/T9kp5gYvYOK9lp21kq8yzi36D3XQAOGH/CqRIfLtzcsm8yzMu-fanout.png`). Direct retrieval from the lesson media CDN returned HTTP 403, and Chrome screenshot capture timed out, so the original could not be saved locally.

**Next:** Open the Network tab and record its displayed content.

### Screen 7: Network Topology tab

The **NETWORK TOPOLOGY** tab is selected. The lesson says: “In Network topology, typically you connect VPNs with one other in a loop fashion and this is usually done when you want to share between regions.” It adds: “Care must be taken to avoid Topic routing loops. The recommended avoidance technique is to use topic hierarchy design.”

**Visual gap:** The original Network topology diagram is associated with the course media key `rise/courses/T9kp5gYvYOK9lp21kq8yzi36D3XQAOGH/Lew2lTR1prUMJOZY-network%2520top.png`. It could not be saved locally; the other diagram assets from this same course package returned HTTP 403 when retrieved, and Chrome screenshot capture timed out.

**Next:** Move down through the page to review the direction content before opening the quiz.

### Screen 8: VPN Bridge Direction — lower page reviewed

After moving down through the page, the previously recorded **Unidirectional Bridging** and **Bi-directional Bridging** explanations remained the final lesson content; the accessibility view exposed no additional prose. The three topology tabs have all been selected and recorded. The section now shows **Completed** and SCORM progress is **75% COMPLETE**. The unidirectional and bidirectional course diagrams remain documented as unavailable local assets in Screen 5.

**Next:** Open **4 of 4 — Quiz**, record the complete matching prompt and all available choices, then answer and verify the result.

### Screen 9: VPN Bridges quiz — initial matching question

This is **Lesson 4 of 4 — Quiz**. SCORM reports **75% COMPLETE**. The quiz introduction says: “Now let's see if we can help Haroldo answer his question.” A matching activity asks: **“What kind of flexibility is offered by VPN Bridging?”** A **SUBMIT** button is visible; the activity has not been submitted, and no feedback is shown yet.

The activity presents these matching terms and definitions:

- **Customized topic subscriptions** — controls the flow of messages.
- **Options for delivery mode** — direct messaging and guaranteed messaging.
- **Choice of message direction** — unidirectional or bidirectional.
- **Many alternative transport modes** — compressed and encrypted connections.

The last pair is flagged as an incorrect pair in the loaded course answer data, even though the earlier Flexibility lesson text listed compressed and encrypted connections under transport modes. Treat it as a possible distractor and resolve its correct match through the quiz interaction and feedback. No answer has been submitted yet.

**Next:** Inspect the matching controls, pair the terms using the course lesson, submit once, and record the platform's feedback.

### Screen 10: Matching cards exposed by keyboard focus

Moving keyboard focus through the quiz exposes four draggable source cards, in this order: **Choice of message direction**, **Many alternative transport modes**, **Customized topic subscriptions**, and **Options for delivery mode**. Each is exposed as an image labeled “Draggable item” with help text “Rectangular shape with an arrow on the right side.” The accessibility tree does not expose the drop-zone labels or a keyboard drag instruction. No card has been matched and the quiz is still unsubmitted.

**Next:** Use the exposed course pairings to complete the drag-and-drop activity, submit, and record feedback.

### Screen 11: Quiz completion status before submission

Keyboard navigation now exposes the four drop-zone definitions: **controls the flow of messages**, **direct messaging and guaranteed messaging**, **Unidirectional or bidirectional**, and **compressed and encrypted connections**. The SCORM header now reports **100% COMPLETE** and the sidebar marks **Quiz Completed**, although no answer has been submitted and no quiz feedback or result is displayed. This appears to reflect course-page progress rather than a verified quiz result. A temporary keyboard drag selection was cancelled; the cards remain unpaired and **SUBMIT** remains available.

**Next:** Pair the matching cards from the lesson's definitions, submit the response, and record the actual result/feedback before leaving the SCORM player.

### Screen 12: Submit validation

Clicking **SUBMIT** without a registered card pairing displays: **“Please answer the question to continue.”** The course provides no scored result or correctness feedback. The SCORM header remains **100% COMPLETE** and the sidebar still says **Quiz Completed**, but the matching response is incomplete and unverified. Clicking/focusing the draggable cards and using keyboard focus/arrow keys did not produce a visible or accessible pairing; screenshot capture through Chrome timed out, so target coordinates could not be inspected for mouse dragging.

Immediately after closing the SCORM player, Academy still reported **8 of 14 lessons completed** and **VPN Bridges — In progress, 0 of 1 completed**. After the page refreshed, Academy updated to **9 of 14** and **VPN Bridges — Completed, 1 of 1**; the lesson pane displays **“You have completed this lesson!”** and offers the next Academy lesson. The SCORM's **Submit** validation had shown **“Please answer the question to continue”** and no matching response was registered, so the LMS completion state conflicts with the quiz state.

**Next:** Continue to **Dynamic Message Routing**, as Academy confirms VPN Bridges Completed (1/1). Preserve the quiz discrepancy in the checkpoint; do not describe its answer as correct or verified.
