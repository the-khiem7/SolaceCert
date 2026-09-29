---
title: "Micro-Integrations"
document_type: lesson
learning_path: "Solace Certified Integration Associate Path"
course: "Event-Driven Integration with Solace Platform"
lesson_order: 4
source: Solace Academy
---

# Micro-Integrations

- **Syllabus order:** 04
- **Course section:** The Concepts
- **Knowledge checks:** Both multiple-choice checks answered correctly.

## Notes

### What Are Micro-Integrations?

The screen recalls that Solace is turning integration “inside out” and contrasts two models. The old way, described as typical of the past 20 years, is centralized, monolithic, point-to-point, and tightly coupled; the lesson names IBM, TIBCO, and, to some extent, modern iPaaS as examples. Its diagram shows many systems joined through a dense central integration cluster. The new-way tab says to move integrations and connectors to the edge, enabling real-time data flow and events in the middle; its diagram depicts decentralized, distributed, event-driven connections around an event mesh.

The lesson defines Micro-Integrations as small, specialized software pieces that act like translators. They connect different systems to and from the event mesh and perform the necessary data transformations. The 1:24 explainer video was played through at 2×. It depicts a source and a target connected through the event mesh by Micro-Integration components; no caption or transcript tracks were available.

The “What Micro-Integrations Offer” accordions list six benefits:

- **Flexibility:** Specialized connectors or adapters can connect core systems or microservices to external third-party applications and be updated without affecting the rest of the system.
- **Faster data distribution:** Higher performance than traditional integration solutions.
- **API compatibility:** Handles differences in APIs, data formats, and protocols between a system and third-party applications.
- **Scalability:** Multiple instances can be deployed to support increasing traffic.
- **Reduced vendor lock-in:** Makes it easier to switch between third-party services or use multiple services for the same function.
- **Security:** Adds a layer of security for external-system interactions, helping isolate core systems from potential vulnerabilities.

### Connecting Services

Micro-Integrations offer an alternative to centralized, monolithic, synchronous patterns common in iPaaS solutions while complementing and enhancing traditional integration patterns and technologies rather than replacing them. The lesson lists three uses: connect iPaaS deployments to the event mesh for real-time connectivity; augment iPaaS by offloading messages to the broker to improve performance during traffic bursts and spikes; and build Micro-Integrations with iPaaS or a preferred code framework, or use prebuilt ones deployed and managed in Solace Platform’s Cloud Console.

The “How Solace Platform Micro-Integrations Liberate and Integrate your Data” carousel has an introduction card and five benefit slides:

1. **Accelerate your integration:** Deployment close to source and target applications supports performance, fast data movement, and simpler network configuration.
2. **Unlock agility and adaptability:** Micro-Integrations are easier to configure, update, and scale than centralized platforms that are difficult and time-consuming to change. This makes it easier to change how applications consume event streams and interact, then reuse them in new ways.
3. **Supersize with easy scaling:** The distributed design can meet growing demand by deploying additional instances; horizontal scaling handles more traffic across environments.
4. **Rock-solid reliability:** Decoupled communication makes systems more tolerant of failures, speed mismatches, and target-system changes.
5. **Easy operation and monitoring:** Deployments in Solace Cloud, a private VPC, or a datacenter can be accessed, configured, and managed through Solace Platform’s Cloud Console. This makes it easier to adapt or add applications without disrupting existing workflows.

### Micro-Integration vs Connectors

The follow-on carousel asks how a Micro-Integration differs from a connector:

- An iPaaS connector typically provides connectivity to or from a data source or target, but does not perform transformation, mapping, masking, orchestration, or routing; other parts of the integration flow handle those functions.
- A Micro-Integration includes a source or target connector that establishes data flow between an event distribution layer, such as an event mesh, and a system. It may also include functions that modify content as messages move onto or off the mesh, including payload transformation, data enrichment or validation, field masking, and header modification.
- A Micro-Integration is more than a connector, but a source or target Micro-Integration is only half of an integration flow, not an end-to-end integration on its own.

### Core Concepts

Micro-Integrations break monolithic integration flows into small, manageable, purpose-built components that connect applications and services to the Event Mesh. Their design principle is “Do one thing, do it well.” Each component is designed for a specific task, such as connecting to a database type or handling a particular API integration. Listed benefits are deployment within minutes, easier maintenance and troubleshooting, simpler testing and validation, and greater flexibility for updates and modifications.

The “What Are Micro-Integrations Made Of?” accordions describe these components:

- **Source Micro-Integrations:** Entry points for data into the event mesh. They connect to external data producers (publishers), transform incoming data into a standardized format (typically JSON), and publish transformed messages to the mesh. The example converts a legacy inventory system’s proprietary format into JSON messages.
- **Target Micro-Integrations:** Exit points from the event mesh. They connect to external data consumers (subscribers), transform standardized JSON into formats required by target systems, and deliver transformed data to external applications. The example converts JSON messages from the mesh into CSV files for a legacy accounting system.
- **Optional payload transformation functions:** Can modify source header or payload data, transform data to meet target format requirements, and insert transformations into mappings. The lesson also describes a no-code interface for mapping and transforming events.
- **Data enrichment capabilities:** Upload sample JSON payloads to define source and target events; define string or numeric constants for mappings; map vendor-specific and custom headers; map headers and payloads; create dynamic Smart Topics from runtime data; and map between data formats.

Solace Micro-Integrations are **unidirectional**: each handles either a source application or a target application. This separation of responsibilities simplifies configuration and troubleshooting, allows inbound and outbound processing to scale independently, and improves error handling by focusing on one direction of data flow.

The lesson describes six lifecycle states:

- **Not Deployed:** Initial state after creation or after successful undeployment; no data flows between the external system and event broker service.
- **Deploying:** Transitional activation state while connections and resources are prepared; it continues until deployment succeeds or fails.
- **Running:** Normal active state; the Micro-Integration is operational and processes data between the external system and event broker service.
- **Down:** Operational error state from which the Micro-Integration cannot recover automatically. Detailed errors support diagnosis and resolution.
- **Unable to Deploy:** Deployment-time error state caused by configuration or connectivity problems that prevent activation; the system provides error details for troubleshooting.
- **Undeploying:** Transitional deactivation state while connections shut down gracefully and data flow stops; once complete, the Micro-Integration returns to Not Deployed.

The lifecycle diagram shows Not Deployed → Deploying, then either Running or Unable to Deploy. Running can transition to Down or Undeploying; Undeploying returns to Not Deployed, and the diagram shows Down returning to Deploying. The lesson says understanding the states is essential for monitoring integration health and required actions; this state-aware approach supports flexible, maintainable architectures.

### Micro-Integration Classification

The lesson divides Micro-Integrations into six categories:

| Type | Key features | Supported technologies shown in the lesson |
| --- | --- | --- |
| **Cloud-managed** | Spring Boot-based; configured, deployed, upgraded, and monitored through Solace Platform Cloud Console; supports source and target integrations, payload transformation and mapping, header mapping, basic auth/client certificates/OAuth, and a visual mapping interface. | Amazon SNS (target only), Amazon SQS (source and target), Azure Service Bus, Google Cloud Pub/Sub, IBM MQ, MQTT, SFTP, and Snowflake. |
| **Self-managed** | Spring Boot-based, runs in its own runtime, and is available through the Solace Platform Integration Hub. Deployment options include executable packages for bare metal, VMs, and cloud compute, or container images for Docker, Podman, and Kubernetes. Runtime models include standalone, active with one or more hot standbys, and active-active with two or more instances for horizontal scaling; configure with properties files or environment variables. | Amazon services (Kinesis, SNS, SQS), Azure Service Bus, Debezium for change data capture, file systems, Google Pub/Sub, IBM MQ, MS, MQTT, SFTP, Snowflake, and TIBCO EMS; the lesson also mentions message transformation capabilities. The source table’s IBM MQ/MS/TIBCO labels are split across lines. |
| **Broker-integrated** | Direct REST-based broker integration configured through REST Delivery Points (RDPs) and managed in Solace Platform Cloud Console; no additional runtime. Supports API-key/OAuth authentication, message transformation, retries, TLS, HTTP compression, and client-certificate authentication. | AWS API Gateway, SNS, SQS, and Lambda; Azure Event Hubs, Service Bus, Functions, and Data Lake Storage Gen2; Google Cloud Functions, Cloud Run, and Cloud Storage. |
| **External-embedded** | Solace-created connectors embedded in third-party platforms, using native host-platform integration, scaling, and management while exposing Solace features and operating in the host runtime. | Kafka Connect (source and sink), Apache Beam I/O, and Spring Cloud Stream Binder. |
| **iPaaS** | Dedicated connectors with native platform integration, iPaaS monitoring and management, support for Solace messaging features, and distribution by an iPaaS partner through the Integration Hub. | MuleSoft (shown with Dell), Boomi, SAP Integration Suite, Informatica, and SnapLogic. |
| **Partner-provided** | Operated and supported by a third party; runtime and management are determined by that operator and connectors may be specialized for enterprise applications. | The lesson points to the Integration Hub for the current supported-technology list. |

The lesson’s “Which Micro-Integration is Best for You?” screen says Micro-Integrations are not enabled by default and require contacting Solace to enable them. For current options and setup information it links to [Discovering Micro-Integrations](https://docs.solace.com/Micro-Integrations/Managed/discover-micro-integrations-available.htm), [Designing Micro-Integrations](https://docs.solace.com/Micro-Integrations/Managed/create-micro-integration.htm), [Managing Micro-Integrations](https://docs.solace.com/Micro-Integrations/Managed/manage-micro-integrations.htm), [Configuring Event Broker Service Connections](https://docs.solace.com/Micro-Integrations/Managed/configure-event-broker-service.htm), [Solace Platform Integration Hub](https://solace.com/integration-hub/), and [Micro-Integrations, Connectors and Integration Guides](https://docs.solace.com/API/Connectors/Connectors.htm).

### Prerequisites and Design Process

The “What Do You Need?” checklist names these prerequisites:

- **Account and service:** Micro-Integrations must be enabled for the account (not enabled by default); each account has a predefined allocation; the event broker service must be version 10.2.1 or higher.
- **Configuration:** Required queues and subscriptions must be configured on the event broker service, and external-system connection details and credentials must be available.
- **Environment:** Micro-Integrations must be in the same environment as the event broker service. For Customer-Controlled Regions, the Kubernetes cluster must be at least 1k-prod size.

The five design-process tabs lay out the workflow:

1. **Discovery and planning:** Analyze data-exchange needs, performance, and regulatory compliance; choose source-based (external system → broker) or target-based (broker → external system) direction; verify broker version, account enablement, and allocated instances; prepare queues, subscriptions, and credentials.
2. **Basic configuration:** Select a Micro-Integration type from the catalog, choose the same environment as the broker, give it a descriptive name and description, and configure source/target connection settings.
3. **Map and transform:** Map standard and custom headers, configure payload fields with the visual mapper, define static values and data-type conversions, and set up Smart Topics for dynamic topic generation.
4. **Authentication and security:** Select Basic, OAuth, client certificate, or API-key authentication; follow security best practices; configure credentials and access controls.
5. **Testing and deployment:** Validate connectivity and data mapping, configure monitoring and alerts, document the configuration, then deploy and verify operation.

The quiz asks which classification matches REST-based integrations configured through REST Delivery Points and managed through broker administration. The selected answer, **Broker-Integrated Connectors**, was confirmed correct.

### Header and Payload Transformations

The section says Solace Platform Cloud Console provides a graphical source-to-target message and payload mapper so integrations can be configured without coding experience.

#### Header mapping

Headers are metadata that travel with messages, such as routing information, timestamps, message IDs, and control information. Source headers can be used as inputs to mappings and transformations to modify or route messages. Provider-specific source headers are listed automatically based on the selected system; custom source headers can also be defined.

Target header values can come from the message payload, from copied or transformed source headers, or from fixed constants. Writable target provider-specific headers are listed automatically; custom target headers can be defined for special nonstandard headers. Incoming headers do not propagate to target messages by default: an expression must explicitly set the target header. The lesson contrasts this with payloads, which can pass through unchanged when no payload mapping is applied.

The example receives MQTT messages with headers such as topic and QoS and sends them to AWS SQS. To populate the SQS message-group-id from part of the MQTT topic, extract the topic header value, transform it (for example with a string-split function), and map the result to message-group-id.

#### Payload mapping

Payload mapping transforms message payloads between systems. Uploading representative source and target JSON (up to 20 MB) shows the before-and-after structures; fields can then be connected visually by dragging. In the CRM-to-shipping example, firstName and lastName are combined into fullName. When at least one field is mapped, fields left unmapped (such as an internal CRM ID) are dropped and not sent to the target.

The lesson lists text, numbers, booleans, arrays, and structured objects/nested data as supported data types. Simple values such as strings and numbers can be mapped directly; complex objects must be mapped field by field; arrays can map only to arrays. If no fields are mapped at all, the whole payload passes through unchanged, which is useful for header-only changes.

#### Constants

Constants are fixed values defined while designing a mapping, rather than values taken from source data or headers. Define a value once and reuse it across multiple places or mappings. The lesson lists strings, booleans, and integers as constant types. Examples include a company name, department codes, region identifiers, default values such as “Unknown,” 0, or null when source data is missing, and source identifiers such as CRM_SYSTEM and INVENTORY_APP. Defining values in one place makes mappings cleaner and easier to maintain.

#### Transformation functions

Transformation functions are prebuilt, no-code tools that modify source data before it reaches the target. Multiple functions can be chained so that one function’s output becomes the next function’s input.

- **String operations:** Upper case, lower case, concatenate, split, substring, and trim.
- **Number operations:** Absolute value, ceiling, floor, and round.
- **Type conversion:** Convert between numbers, booleans, and text.
- **Security:** Mask sensitive values, for example 1234-5678-9012-3456 to XXXX-XXXX-XXXX-3456.

The 5:49 transformation demo was visually sampled at 2×. Visible console screens showed the Micro-Integrations list and a Create SFTP Source Micro-Integration wizard with Details, Source Connection, optional Mappings, Target Connection, and Summary steps. The mapping view showed source and target fields, mapping lines, function nodes, constants and headers, plus a Smart Topic Destination. A transformation-details modal showed a Join function with a delimiter parameter. The embedded player returned to the beginning after playback; full-playback completion is not recorded.

#### Smart Topics

Topics are addresses or channels for messages. Smart Topics construct addresses dynamically at runtime from message content using a formula with placeholders. In the sales example, fixed topics such as sales/newyork/electronics, sales/london/clothing, and sales/tokyo/groceries are replaced by the pattern sales/{store_location}/{department}. A message containing store_location chicago, department furniture, and amount 1299.99 is routed to sales/chicago/furniture. Smart Topics extract the location and department from payload data at runtime, enabling flexible routing without predefining every combination and supporting content-based delivery.

The lesson links to [Mapping Headers and Payloads (Beta)](https://docs.solace.com/Micro-Integrations/Managed/create-message-headers.htm) and the [Transformation Function Reference](https://docs.solace.com/Micro-Integrations/Managed/mi-ref/transformation-function-ref.htm).


## Visuals

#### What Are Micro-Integrations and Connecting Services

- [What Are Micro-Integrations title card](img/what-are-micro-integrations-title.webp) - dark teal circular motif with the lesson title.
- [Old integration model](img/old-integration-model.webp) - systems connect through a dense centralized point-to-point cluster.
- [New event-mesh model](img/new-event-mesh-model.webp) - decentralized, distributed, event-driven connections around an event mesh.
- [Micro-Integrations video poster](img/micro-integrations-video-poster.webp) - source device connected through an adapter to a monitor.
- [Connecting Services title card](img/connecting-services-title.webp).
- [Micro-Integrations around an event mesh](img/micro-integrations-around-event-mesh.webp) - sources and targets connect through specialized components around the mesh.
- [Carousel introduction diagram](img/micro-integrations-carousel-intro.svg).
- [Accelerate integration illustration](img/benefit-accelerate-integration.webp), [agility illustration](img/benefit-agility-adaptability.webp), [scaling illustration](img/benefit-horizontal-scaling.webp), [reliability illustration](img/benefit-reliability.webp), and [platform connector dashboard](img/micro-integration-console-list.webp).

#### Core Concepts

- [Core Concepts title card](img/core-concepts-title.webp).
- [Source, broker, and target flow](img/source-broker-target-flow.webp) - external system to source Micro-Integration to event broker to target Micro-Integration to external system; an identical copy is also available as [the unidirectional flow diagram](img/microintegration-unidirectional-diagram.webp).
- [Lifecycle state diagram](img/micro-integration-lifecycle-states.webp); an identical copy is also available as [the lifecycle diagram](img/microintegration-lifecycle.webp).
- [Micro-Integration classification title card](img/microintegration-classification-title.webp).
- [Micro-Integration classification overview](img/microintegration-classification-table.webp) - introductory category descriptions and an example Integration Hub connector record.
- [Comparison of Broker-Integrated, Self-Managed, and Cloud-Managed options](img/microintegration-classification-followup.webp).
- [Connector dashboard example](img/micro-integration-console-list.webp).

#### Header, Payload, and Transformations

- [Solace header reference fields](img/solace-header-reference.webp).
- [Mapping constants and source headers in the console](img/mapping-constants-console.webp).
- [Payload concatenation mapping](img/payload-concatenation-mapping.webp) - source name fields connect through a Concatenate function to full_name.
- [Smart Topic concatenation mapping](img/smart-topic-concatenation-mapping.webp) - a constant and a source value feed the topic destination.
- [Smart Topic destination in the console](img/smart-topic-destination-console.webp).
- [Transformation demo poster](img/transformation-demo-poster.webp).
