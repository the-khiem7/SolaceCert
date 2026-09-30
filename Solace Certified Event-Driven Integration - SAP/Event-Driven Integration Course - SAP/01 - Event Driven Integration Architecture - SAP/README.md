---
title: Event Driven Integration Architecture - SAP
document_type: lesson
source: Solace Academy
learning_path: Solace Certified Event-Driven Integration - SAP
course: Event-Driven Integration Course - SAP
lesson_order: 1
---

# Event Driven Integration Architecture - SAP

## Course cover and orientation

The SCORM module is titled **Being Event Driven Integration - with SAP** and is authored by Phil FitzGerald. Its cover asks whether the learner understands how SAP and Solace work together to deliver event-driven architecture and workflow enhancements amid changing integration needs, and whether they can name the big ideas and key components and sketch the workflow. It says the class will develop those abilities.

The module recommends prior knowledge of EDA essentials, Solace Event Portal, and SAP Integration Suite. It states that there is no hands-on component, while the instructions and demonstrations are universally applicable.

The module table of contents, recorded before starting the first internal section, is:

1. **The Context:** The Architectural challenge.
2. **The Concepts:** Evolving Integration architecture; SAP and Solace explained; Essential Concepts; Design Principles.
3. **The Click:** The Solace - SAP workflow; Conclusion.

### Visual record

The cover is a SAP/Solace branded graphic with repeated SAP and Solace motifs behind the title. The embedded SCORM page did not expose its cover image as a separately recoverable asset to the Academy asset inventory, so no local copy has yet been saved. This limitation is retained rather than substituting an image.

## 1. The Architectural challenge

The module frames the architect's role as providing the foundation on which everyone else relies. It assigns the architect four responsibilities:

1. Develop a vision for event-driven architecture.
2. Document, implement, and maintain EDA cost-effectively.
3. Create developer procedures for event-driven integrations that conform to the larger vision.
4. Maximize developer efficiency.

It describes the desired day-to-day outcome for an architect as:

1. Maintaining and updating the business vision with relative ease.
2. Providing discoverability and a consistent mechanism to define and document EDA across teams.
3. Rapidly deploying consistently generated SAP iFlows in support of that vision.
4. Using built-in mechanisms in Event Portal to manage object deployment to the Advanced Event Mesh.

The screen uses the SAP/Solace title treatment faintly behind the content; no separate instructional image asset was exposed by the embedded SCORM frame.

## 2. Evolving Integration architecture

The module says the enterprise view of IT systems is shifting from systems as **data custodians** to systems as the enterprise's **nervous system**. This gives priority to data in motion rather than data at rest, enabling more dynamic decisions.

The target architecture should remain effective during busy periods or temporary component unavailability, grow as components are added, deliver important information even to late consumers, and allow change without upsetting the whole solution. The lesson's framing question is whether integration can keep the centre simple while moving complexity to the edges.

### Advantages of the streamlined model

- An Event Mesh clears the data path for routing and decouples integration paths from performance-impacting systems.
- Native Event Mesh capabilities remove complex routing rules.
- Processing and deployment can be decentralized to the edges for regional resource optimization.
- New consumers can be added in other regions without downtime or modifications to the existing setup.
- Each node can scale independently.
- Higher data volumes can be handled without degrading performance.
- Faults or delays in one system do not disrupt other integration flows.

### Visual: Integration Reimagined

The displayed diagram contrasts **integration of the last 20 years**—one-to-one service relationships labelled “centralized, monolithic, point-to-point, tightly-coupled”—with **integration for the next 20 years**, where the same applications connect through a central mesh labelled “decentralized, distributed, event-driven.” The accompanying conclusion is that iPaaS supplies process power while Solace remains focused on rapid data movement; SAP performs complex functions at the edge. The SCORM frame exposed the diagram's accessible description but not a separately recoverable image asset, so no image file was saved.

### Video check

The section contains a video player. On inspection it reported a remaining duration of `0:00`, showed no captions, transcript, or caption control, and presented no additional visible media content. The lesson's accompanying text and diagram above are therefore the only recorded concepts for this media item.

## 3. SAP and Solace explained

The module compares SAP to an architect of bridges (APIs) and highways (integration platforms), connecting systems smoothly. It positions Solace as moving messages and events rapidly where milliseconds matter. Solace is presented as the backbone for real-time EDAs that process high volumes of data and support reactive applications such as stock-trade monitoring and live sports scores. SAP is presented as strong at connecting systems and messaging languages, predominantly through RESTful integration. Combining SAP's integration capabilities with Solace's event handling is the proposed response to growing real-time, event-driven demand.

An application modelled in Event Portal is stated to be equivalent to an SAP iFlow.

### Solace contribution

- Linear scalability, dynamic event routing, and performance.
- Event governance, multi-protocol capability, and all event exchange patterns.
- Full AsyncAPI support.
- A defined methodology for EDA and microservices architecture.

### SAP contribution

- Comprehensive integration, orchestration, and choreography capabilities.
- A broad connectivity set and comprehensive UX.
- REST API management and governance through Integration Suite.
- Citizen integration and RPA support.
- Both RESTful and event-driven patterns.
- Defined integration methodologies: API-led connectivity and application network.

### Combined Solace + SAP use cases

- High performance, for example IoT or capital markets.
- Global reach and scale, for example global manufacturers and retailers.
- Agility and flexibility, including omnichannel consumption and rapid digital service/product additions.
- Heterogeneous, polyglot environments, such as multi-cloud real-time synchronization.
- Predictive behavior: predictive maintenance, fraud detection, and cross-sell/upsell.
- Automation and process scaling.
- AI readiness for RAG and agentic use cases.

## 4. Essential Concepts

### Scaling

The module identifies three Solace scaling modes:

1. **Vertical consumer scaling:** Partitioned Queues allow any number of consumers to be dynamically added to a channel without performance impact.
2. **Broker scaling:** brokers can be clustered and load-balanced across clusters for high availability.
3. **Event mesh scaling:** connected brokers can create a globally scalable mesh with a seamless event-distribution path.

For a New York–Tokyo example, the traditional approach would deploy event platforms in both regions and build relay clients, bringing performance tuning, coding, and operations work. With an Event Mesh, the Tokyo client registers as a consumer and an event published in New York is routed to it automatically, without special setup, forwarding code, or extra management.

### Data distribution

For one-to-many distribution, SAP and Solace combine event-driven routing with SAP logic handling. The example is ACME Retail changing the price of last season's mountain bikes globally, with local currency and tax differences. A REST-only approach would need APIs per area and complex orchestration and could suffer latency or outages. A globally configured Event Mesh distributes a corporate price-change event to regional SAP consumers, which apply local currency and tax adjustments.

### Data aggregation

Distributed data can span systems, environments, and geographies, making unified aggregation difficult. The example combines a banking customer's demographics in Salesforce, account data on a mainframe, and loan data from a loan system; traditional orchestration becomes harder as systems proliferate and may time out when they are globally distributed.

### Stateful choreography

Stateful choreography means multiple services work together while each knows the process state and its own role. It differs from central orchestration because services communicate directly and pass state as needed. The order-fulfilment example follows a RESTful order submission to an Order Management System, fulfillment initiation, inventory checking and possible replenishment, packaging/pickup/shipping, and customer status updates. Events connect the steps and timing can vary.

The module calls out three Solace advantages for this pattern: **state representation**, **scalability**, and **heterogeneity**. It compares orchestration to a conductor coordinating a business transaction and choreography to a flash mob in which participants know their parts without a central guide. Solace retains process-state visibility during choreography for real-time awareness and detailed stakeholder notification. Topic-structure variables let participants exchange cues and progress; a monitoring subscriber observes those state changes, separating notifications and error handling from the main action.

### Error handling

SAP has built-in exception handling focused largely on in-process errors. In distributed deployments, a failure in one geography can affect other services and require complex rollback. The lesson distinguishes:

- **In-process** handling: inside the workflow; it can slow the workflow, miss wider impacts, and potentially halt the process if it fails.
- **Out-of-process** handling: outside the main workflow, avoiding direct impact on service speed and continuity.

The proposed design is to minimize in-process handling, understand a failure's wider impact, and ensure recovery capability under critical conditions. A Resolution Center can process exceptions outside the main service path, but must avoid becoming a cross-region single point of failure. The suggested hybrid design uses localized, domain-specific Resolution Centers communicating with a central Resolution Center. The Event Mesh enables rapid error offloading and coordination between Resolution Centers and administrative services, preserving service integrity while supporting comprehensive recovery.

## 5. Design Principles

### Routing and filtering

The module identifies destination-based and content-based routing. Both occur in SAP integration, but putting more integration components on the data path increases coupling and can reduce performance.

**Destination-based routing** forwards an event according to the destination named in its packet, like a post office selecting the optimal route from the envelope address. Solace Event Mesh performs this implicitly: brokers exchange topic-subscription information to form a mesh view of event paths, analogous to IP routers exchanging routing tables through BGP.

**Content-based routing** forwards an event based on payload content or metadata, like a librarian shelving a book by genre or audience. The Event Mesh cannot inspect payloads, so it routes by destination while SAP applies content-based routing; the separation reduces coupling and improves performance. Destination-based filtering belongs naturally in the Event Mesh, while SAP performs content-based filtering.

### Protocol bridging

Event Mesh supports JMS, MQTT, AMQP, and SMF. Developers can use familiar protocols without deploying separate systems for each. The mesh can also bridge Kafka, IBM MQ, and TIBCO EMS, allowing event movement across messaging platforms.

### Multiplexing and demultiplexing

- **Multiplexing (Mux):** gather events from several sources into a single main channel, useful for live combined-data statistics and analysis.
- **Demultiplexing (Demux):** divide an event stream into smaller, manageable substreams based on real-time information, adding flexibility and agility.

Solace implements these patterns with simple configuration: map multiple topics to one queue, and use hierarchical topic structures with wildcards and variables. For example, publishers can use `order/process/{city}/{storeid}`—such as `order/process/Chicago/123` or `order/process/NewYork/456`—while consumers select New York orders via `order/process/NewYork/*` or all US orders via `order/process/>`. This decouples publishers and subscribers, removes needless logic from the integration path, and supports combining Mux and Demux for more streamlined processing.

The content-based-routing illustration was present only as an unlabeled embedded image with a Zoom control; its original asset was not exposed by the SCORM frame, so it is documented but not copied.

## 6. The Solace - SAP workflow

The workflow is presented as four timeline stages:

1. **Starting in Event Portal** — getting applications in line.
2. **Moving into SAP Integration Suite** — bringing event driven to a real experience.
3. **Deployment** — setting parameters and maps.
4. **Testing your flow** — using Try Me to measure success.

Each stage contains a video player. The first player exposed no captions or transcript control; after it loaded, it showed about 2:08 remaining. The remaining players were titled only by the three stage labels above and exposed no displayed transcript, captions, examples, or conclusions. No additional claims are made for their unavailable media content.

## 7. Conclusion and knowledge check entry

The conclusion says that the learner has seen how SAP and Solace work together for event-driven architecture and workflow enhancements, reviewed the changing face of integration, and can name the big ideas and key components and sketch the workflow. The module then offers **Start Quizzing Your Skills** to validate and explain the material. The conclusion has been recorded before entering that assessment.

### Knowledge check 1 of 4 — pending submission

**Selection instruction:** choose one answer (radio buttons).

**Question:** “What does this mean?” A supporting image is displayed but has no accessible description or exposed original asset, so its contents could not be recovered faithfully.

- The growth in application variety, need and density will only grow.
- We've reached peak complexity.

**Submitted answer:** “The growth in application variety, need and density will only grow.”

**System feedback:** Correct. Confirmed correct answer: “The growth in application variety, need and density will only grow.” Explanation: “How could it not eh?” The choice “We've reached peak complexity” was correctly unselected.

### Knowledge check 2 of 4 — pending submission

**Selection instruction:** checkboxes are displayed, so the screen permits one or more selections.

**Question:** “You currently live in this kind of complexity.” A supporting image is displayed without accessible description or a recoverable original asset.

- Yes
- No
- I dare not think about it

**Submitted answer:** “Yes.”

**System feedback:** Correct. Confirmed correct answer: “Yes.” Explanation: “Even if you claim not to, you will do soon or are part of other system spaghetti.” “No” and “I dare not think about it” were confirmed correctly unchecked.

### Knowledge check 3 of 4 — pending submission

**Selection instruction:** enter a free-text answer.

**Question:** “Integration turned inside ___?” A supporting image is displayed without accessible description or a recoverable original asset.

**Submitted answer:** `out`.

**System feedback:** Correct. Confirmed acceptable response: `out`.

### Knowledge check 4 of 4 — pending submission

**Selection instruction:** choose one answer (radio buttons).

**Question:** “Good for business?” A supporting image is displayed without accessible description or a recoverable original asset.

- Competitively smart
- Absolutely (but with effort)

**Submitted answer:** “Absolutely (but with effort).”

**System feedback:** Correct. Confirmed correct answer: “Absolutely (but with effort).” “Competitively smart” was confirmed correctly unselected.

The knowledge check reached 100% completion and every one of the module's seven internal sections was visibly marked Completed before leaving the SCORM assessment.

### Knowledge check result

The SCORM module visibly reported **100% COMPLETE**. Quiz Results showed **Your score: 100%**, **Passed**, with a passing threshold of **80%**.

## Academy completion reconciliation

Immediately after closing the SCORM module, Academy still displayed **Course in progress, 0 of 1 lessons completed**. After a page refresh, it visibly synchronized: the course showed **Course completed**, the lesson content status showed **Completed**, and the page said “Well done! The course is completed.” Academy records the completion as 2026-09-30 at 11:21 am.

## Completion evidence

At initial resume, the Academy showed this as the only course lesson and marked the course in progress with 0 of 1 lessons completed. Internal module sections were all shown as unstarted. Completion will be recorded only after the module and Academy visibly confirm it.
