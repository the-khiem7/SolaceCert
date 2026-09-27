---
title: "Event Portal Essential"
document_type: lesson
learning_path: "Solace Certified Event Broker Administrator Associate Path"
course: "Solace Essentials"
lesson_order: 4
source: Solace Academy
---

# Event Portal Essential

- **Course:** Solace Essentials
- **Syllabus order:** 04
**Academy status:** Completed on 2026-09-24
## Event Portal Essential workshop

## Welcome screen

The workshop is by Phil FitzGerald and prepares learners to explain what Event Portal does, who it serves, and how to use it. It covers Event Portal’s purpose, terminology, a sample design, a typical workflow, and a hands-on configuration lab that publishes configuration to a broker. Quizzes and downloadable reminders are included.

Prerequisites include basic familiarity with EDA, brokers, and CI/CD, plus access to a broker. The course points to cloud and container broker options and says Lab 2 assumes a container broker. It introduces Ask Solly, a training AI assistant, to help learners explore sample environments. The workshop is designed for developers who learn by investigation.

## Lesson 1 of 7 - What Is Event Portal For?

The video and transcript describe Event Portal as a platform for visualizing and managing an organization’s event-driven architecture and the lifecycle of its events and application interfaces. For developers, the value is faster discovery, design, security, sharing, and deployment with less duplicated effort.

Key points from the transcript:

- Ad hoc documentation and spreadsheets can become stale, difficult to maintain, hard to share, and unreliable as a source of truth for applications, events, schemas, and versions. This can waste time through searching, asking, and duplicated work.
- A graphical designer models applications, events, schemas, and their relationships.
- A centralized, searchable library helps teams find and reuse architecture assets.
- Runtime discovery and management represent event mesh and broker topologies and support pushing configurations from design toward deployment.
- Governance tools include access control, approval workflows, version control, and asset lifecycle management.
- Productivity features include templates for standardizing broker configurations and KPI analytics for tracking the value of EDA work.
- The lesson transitions to explaining the core objects and terminology used in Event Portal.

The transcript includes a product-management perspective that Event Portal helps developers and architects build and integrate event-driven applications faster, and a developer perspective that it helps them get work done. The video transcript was summarized rather than copied verbatim.

## Lesson 2 of 7 - Gener-AI-ate your EDA design

The lesson says a quick way to learn Event Portal is to examine a working example. It points to the `SolaceLabs/event-portal-samples` GitHub repository and an in-course `event-portal-samples-main.zip` download link. The sample-guided steps are to download or unzip the selection; open Designer and use the `...` beside Create Application Domain; import the Application Domain(s); then explore Component and Graphic views.

A six-image carousel illustrates Event Portal sample materials.

**Carousel slide 1 of 6 - GitHub repository.** The screenshot shows the public SolaceLabs/event-portal-samples repository, generated from solacecommunity/template-repo. Visible sample folders include acme-bank/solace/sample-domain, airline/solace/sample-domain, banking/kafka/sample-domain/kafka, master-data-management, natural-resources, retail, supply-chain-retail/solace/sample-domain, and telco/kafka/sample-domain. The repository description says its samples demonstrate implementing best practices with Solace Event Portal; the page shows an Apache-2.0 license.

**Carousel slide 2 of 6 - Designer: Application Domains.** The screenshot shows an empty state, “No application domains have been created.” It defines an application domain as a namespace for applications, events, and other event-driven architecture objects for different teams, groups, or lines of business in an organization. Visible actions are Create Application Domain and Import Application Domain, with a link to documentation. The left navigation lists Designer, Catalog, Runtime Manager, KPI, Micro-Integrations, Agentic AI, Cluster Manager, Mesh Manager, and Insights.

**Carousel slide 3 of 6 - Application Domains menu.** The screenshot shows the ellipsis menu beside Create Application Domain expanded. Its options are Event Access Requests, Kafka Settings, and Import Application Domains.

**Carousel slide 4 of 6 - choosing an import file.** The screenshot shows a macOS Downloads file chooser with the `event-portal-samples-main` folder expanded. Under `retail/solace/masterclass-domain`, `Acme_Retail_Solace_Masterclass_version.json` is selected. Nearby visible entries include `sample-domain`, `sample-event-stream`, `hybrid`, `kafka`, and `README.md`; the chooser offers Cancel and Open.

**Carousel slide 5 of 6 - Acme Retail graph view.** The screenshot shows a graph of related event objects and services in Designer. Visible labels include Stock reservation (1.0.0), Inventory and FraudChe... (1.0.3), Order Created (2.0.3), Order confirmed (0.1.0), Orders Service (1.0.2), Payment Created (1.1.1), Payment service (0.1.0), Payment Updated (0.1.0), Shipping Service (0.1.2), Shipment Created (1.0.2), and Shipment Updated (0.1.0). The interface shows Add Objects, “Showing latest versions,” a Use updated interface toggle, and 100% zoom.

**Carousel slide 6 of 6 - Acme Retail applications.** The screenshot shows the Applications tab for the Acme Retail domain. It lists Inventory and FraudCheck Service, Orders Service, Payment service, and Shipping Service. Each row has Broker Type Solace, Application Type Standard, and one version. The adjacent tabs are Components, Events, Schemas, Enumerations, Event APIs, and Event API Products; the page also shows a name filter and Create Application control.

The page asks “What did you find...?” and provides a “TAKEN A LOOK? THEN CONTINUE” control. After recording all six carousel screens, the control was activated and the lesson was marked Completed. The GitHub sample and zip were not opened or downloaded.

## Lesson 3 of 7 - Level up on your definitions

The opening screen is by Phil FitzGerald. It says learners may know EDA and Event Portal terms and have seen ACME screens, and now should understand what those terms mean as concepts and as GUI elements. Instructions: download the worksheet, play the audio chat (under 8 minutes), click the icons for more content, then explore the ACME environment; Ask Solly is available for questions. The page exposes a 1.5 MB image file, `Course_Graphics_Event Portal 1920.png`. The table of contents reports this lesson 25% complete and the course 14% complete; “Gener-AI-ate your EDA design” is marked Completed.

At opening, the labeled graphic had 13 markers, all initially unviewed: Get organised; Making it easier; Meeting reality; Extending API reach; Check in on reality; Applications a la Apps; The fundamental event; Add in segregation; Refine the topics; What can apps expect?; Are we current?; Design to done; and Want to know the flow? The Video Transcript accordion was initially collapsed; its full transcript is recorded below.

### Marker 1 - Get organised

The marker says an application version can be pinned to a specific version when promoting it. Version control and environment support help ensure the right configuration is pushed to the right broker. When an application version is promoted to a new environment, Event Portal pushes the necessary configurations based on approved access requests. Multiple environments support iterative development: newer versions can be built and promoted while stable versions remain in production. Lifecycle states protect developers from breaking one another’s work; for example, a released object cannot be changed, protecting other developers who use released events.

The lesson page includes a 7:15 audio player and says to listen while looking below; a transcript is available below. An embedded documentation excerpt says Event Portal 1.0 was deprecated as of October 31, 2024, and says Event Portal 2.0 has surpassed it in value and capabilities.

The background infographic includes labels for application domain, events and shared events, enumeration, schema, environment, versions, config push, runtime event manager, and APIs/API products, alongside workflow actions Authorize, Promote, Audit, Measure, Configure, and Run.

### Marker 2 - Making it easier

Configuration templates let middleware or integration teams define approved queue configurations, controlling the shared broker resources used by applications. Developers can select a predefined template instead of configuring every queue detail manually. Templates standardize queue configurations and may represent sizes such as small, medium, and large, with performance, capacity, and behavior parameters. Platform owners decide which queue types developers may use and can enforce resource policies. Templates are integrated with config push, so an application promotion can use only approved templates. This simplifies development while helping prevent problematic or excessive resource use.

### Marker 3 - Meeting reality

Runtime Event Manager presents an operational view of an event-driven architecture: application connections to brokers, published and subscribed events, and queues. This differs from a traditional resource-centric broker view. It supports multiple environments such as development, integration, and production, each with its own event mesh and broker configuration, and allows different application versions to be deployed to them. Event Portal pushes the connection configuration to the runtime; Runtime Event Manager shows deployments so teams can verify which versions are active. It distinguishes deployed runtime objects from design-time objects that represent intended configuration.

The marker also covers broker configuration (queues, ACLs, and client profiles), RBAC by environment, governed self-service deployment without direct broker access, and auditing that compares runtime and design configuration to find discrepancies such as manually added queue subscriptions. Configuration push follows permissions and portal definitions, and APIs can support deployment and management automation.

### Marker 4 - Extending API reach

Event Portal can expose asynchronous events as Event APIs for teams, partners, and end users. Event APIs can be integrated alongside REST APIs in third-party API management platforms to give developers a unified way to use synchronous and asynchronous interfaces. An API management/devportal API supports integration with platforms such as Axway or custom-built platforms. Event API products bundle events for publishing, subscribing, or both; they can specify class of service and view size, and can be exposed externally as managed offerings. API products can support monetization through end-customer access. Designers can export an AsyncAPI specification for code-generation tools, and the UI exposes APIs for automating many operations.

### Marker 5 - Check in on reality

Cataloging makes applications, events, schemas, and enumerations discoverable. Runtime auditing checks whether broker state matches the Event Portal design: it scans runtime data, compares it with design intent, and surfaces discrepancies, especially changes made outside Event Portal. Runtime objects can be brought back into Designer to update the design when needed. Audits can show queue spool usage, queue ownership, and security violations such as an unexpected subscription. The marker presents Event Portal as a governed visibility window into the EDA, avoiding the need to inspect each broker directly.

### Marker 6 - Applications a la Apps

Developers define an application interface by selecting the events an application will publish and subscribe to, reusing existing events or creating new ones. At runtime, applications receive only permitted event data through broker connections that Event Portal configures from the interface. Newly produced events are cataloged automatically. AsyncAPI specifications can be exported to code-generation tools such as Spring Cloud Streams; starter plugins for IDE integrations help generate the event interface so developers can focus on business logic.

Event data access follows application-level request and approval workflows. Each application has its own credentials for granular access control. Applications can be promoted through environments, with configuration pushed only after required approvals. Runtime audits compare deployed configuration with design intent and flag discrepancies; the portal visualizes data flows and which applications consume data. Application versioning supports iterative development while older versions remain in production. APIs can integrate with CI/CD pipelines to automate promotion, including through GitHub Actions.

### Marker 7 - The fundamental event

Event Portal catalogs event versions, optional aliases/version names, lifecycle state, descriptions, access details, topic addresses, payload schemas, and references from applications and Event APIs. The lesson distinguishes a topic address, which can include variables, from the concrete topic produced when an application substitutes runtime values. Topic variables can be bounded by enumerations or unbounded.

Events can be grouped into Event APIs and exposed externally through API management. An Event API can specify publish/subscribe direction, class of service, and view size. Architects and developers reuse existing events and automatically catalog newly produced events. Event access can require approval or be auto-approved; applications cannot use an approval-gated event until access is granted. Lifecycle states include draft, released, deprecated, and retired, and released events cannot be changed. The design graph visualizes flows and events; runtime audits check alignment with design. A KPI dashboard includes a reuse index and usage information. Event Portal models event types, while brokers handle individual event instances and their runtime flow.

### Marker 8 - Add in segregation

Application domains organize and separate work: a development team can own or participate in one or more domains, or domains can represent business functions. RBAC and data-access controls govern which teams can use specific event data. Unique topic names support consistency. The interface represents domains as hexagons, showing how domains relate to applications and events. Events can be shared between domains by dragging them into the domain being designed, supporting new services. Domains help model the overall EDA architecture, beyond interface definitions alone; the lesson contrasts this with API management platforms that typically focus on interfaces.

### Marker 9 - Refine the topics

An enumeration is a bounded topic-address variable with a limited, predefined set of values, such as weekdays or months. Topic-address variables can be bounded or unbounded; an application supplies values at runtime to form a concrete topic. Unbounded examples include credit-card numbers and order IDs. This distinction helps describe how event data is structured and routed.

### Marker 10 - What can apps expect?

Schemas are cataloged in Event Portal and describe event data formats, including field types (for example, string, integer, and boolean) and structure. Cataloged schemas help developers avoid rebuilding data structures and maintain consistency. Schemas are associated with events, are versioned, and can be exposed with their events through Event APIs and API management platforms.

### Marker 11 - Are we current?

Versioning manages the lifecycle of applications, events, and schemas while supporting new features and fixes alongside stable production versions. Lifecycle states include draft, released, deprecated, and retired; a released object cannot be changed, protecting consumers from breaking changes. Each environment promotion can select a specific application version. Each application version generates an AsyncAPI specification that documents its interface and stays aligned with that version. Versioning and multiple environments help target configuration to the correct brokers. Teams can revert to an earlier version; a rollback preview shows planned changes, such as updating a client profile or deleting queues. Component views show versions of applications, events, and schemas.

### Marker 12 - Design to done

Configuration push sends application and event configuration from Event Portal to brokers through Event Management Agent, which uses Terraform in the backend. The feature offers governed self-service: it checks required approvals and previews broker changes, including queue and ACL changes, before pushing. Each application uses its own broker credentials for granular access, and access is restricted by the defined configuration and permissions. Config push can be driven through APIs or GitHub Actions. Middleware or integration teams can provide approved queue templates, while developers provision from those choices with less need to involve those teams directly.

### Marker 13 - Want to know the flow?

The final marker says, “Wait for the next section...”

### Audio chat transcript - 7:15

The platform provides a timestamped transcript. It contains apparent speech-to-text errors, so these notes preserve its concepts without treating garbled wording as exact terminology.

- **00:00–00:34 - Environments:** Event Portal supports multiple environments in an account, often matching SDLC stages such as development, integration, and production. Specific application versions can be promoted between environments. Administrators grant access and configure options such as configuration templates and runtime configuration.
- **00:34–01:26 - Application domains and applications:** Domains group EDA objects by business line or development team and support access control, organization, and governance. Retail examples include inventory, point of sale, and customer loyalty. Domains exist in Event Portal rather than on event brokers. Applications produce and/or consume events; examples include inventory systems, POS terminals, and customer databases.
- **01:26–02:39 - Events, topics, and enumerations:** Event Portal catalogs and versions events so they can be discovered, edited, and reused. Applications publish events with topic addresses that support routing and filtering at different levels; retail examples include inventory updates, sales transactions, and customer interactions. Enumerations define named values allowed for a topic variable, contrasting open-ended values such as card digits or order IDs with fixed sets such as weekdays or months.
- **02:39–03:31 - Schemas and shared events:** Schemas describe the structure and meaning of event payload data and help publishers and subscribers interpret JSON consistently. A shared event can be reused across domains; the example is a low-stock alert shared by inventory and purchasing. Business operations can involve interconnected events, so objects use versions and lifecycle states.
- **03:31–04:45 - Lifecycle, APIs, and API products:** Released application or event versions cannot be altered; draft, released, deprecated, and retired states enforce lifecycle rules. Event Portal can generate code for applications to use APIs. API products bundle related events and let developers work with synchronous and asynchronous integration in one platform. They can include publish/subscribe direction, class-of-service and size information, and can be offered to external customers for monetization.
- **04:45–05:31 - Event mesh and Runtime Event Manager:** A modeled event mesh and Runtime Event Manager connect design and deployment concepts. An event mesh is a network of interconnected brokers that route events among applications and services. Runtime Event Manager shows application interactions with brokers and helps compare the design to operational reality.
- **05:31–05:54 - Configuration push:** Event Portal can push configuration changes to brokers through Event Management Agent, with Terraform-like automation. The transcript also says teams can choose to download AsyncAPI as part of a CI/CD workflow.
- **05:54–06:40 - Discovery, audit, and broker resources:** Discovery and audit compare runtime objects with design objects associated with brokers. Queue templates govern how users configure consumers. Client profiles define broker behaviors and capabilities provided to an application after it connects.
- **06:40–07:15 - Wrap-up:** The speakers say learners now have the component vocabulary needed to understand a typical Event Portal process, and suggest exploring the ACME sample before the next section.

## Lesson 4 of 7 - The Event Portal Flow

The lesson is by Phil FitzGerald. Its opening screen asks, “Event Portal flows how?” The screenshot shows an embedded video area with a central Play control below the prompt. A four-slide image carousel and a collapsed Video Transcript control are available, followed by the instruction “Complete the content above before moving on.” The table of contents now marks “Level up on your definitions” Completed, reports this lesson 40% complete, and shows 29% overall course progress.
### Video transcript summary - about 6:29

The transcript describes a typical Event Portal workflow and encourages viewers to reproduce it in their sample environment. The speakers note that developers begin by discovering existing, interconnected objects, then design new objects or update a version. Authorization determines which objects they can change; developers can request access to objects owned by others. Design can be exported through APIs to automation platforms or deployed with config push. Audits compare broker and design state, and KPI tracking measures outcomes as the innovation cycle continues.

In the example flow, a developer browses domains they can access, including read-only domains, and checks applications, lifecycle states, local/shared events, and source domains. Runtime Event Manager shows meshes, environments, and applications deployed to brokers; graph arrows show message direction, while Component view gives a list and details. The developer creates an application, adds a shared event from another domain or searches the catalog for a chosen version, then links events to the app. The application version shows publish/subscribe relationships and whether it is deployed.

The developer adds a consumer as a queue or direct subscription, specifies topic addresses, previews matching events in an environment, configures queue details or uses a queue template, and requests any required approval. In Runtime, the developer selects an environment and application version, enters broker credentials, and adds context to the access request. If rejected, the developer adjusts topic choices and resubmits. After approval, config is ready to deploy; AsyncAPI export to CI/CD is an alternative to config push.

Before deployment, Runtime previews broker changes. Config push uses Event Management Agent to apply them, after which the developer verifies the configuration in the development environment. Further changes can add an application version and event subscription; earlier versions can be selected to roll back. Finally, an audit through EMA compares live broker configuration with design and lets the developer update the design or remove unnecessary objects. The lesson frames the workflow as faster innovation with safety and security.

The first carousel image is a green-and-white Solace rocket with “EVENT PORTAL” branding and a mascot in the cockpit. Its prompt asks: “You are a Developer for an Airline. What kind of application domains would you expect to see?”
Carousel slide 2 presents a Solace-branded phone displaying a network of connected event nodes. Its prompt asks: “You are on a Dev team for a Telecoms company. What's a typical shared event between call record and billing domains?”
Carousel slide 3 shows a Solace-branded payment card with a payment-security theme and sample card details. Its prompt asks: “You are working in a Financial Services team. What topic address would you advise for their payment security check team?”
Carousel slide 4 shows part of a Solace-branded hardhat with a connected-event network. The displayed question reads: “You advise a construction . What events would you expect to require approval requests?” A button below says “TRIED IT IN YOUR SAMPLE ENVIRONMENT?”

The video opens on an INNOVATE workflow graphic: Discover, Design, Authorize, Promote, Audit, Measure, Open API, Configure, Codegen & Implement, and Run. Integration logos are shown below Codegen & Implement.

## Lesson 5 of 7 - Explore with the Lab

The opening screen is by Phil FitzGerald. It jokes, “What do Techies and a certain breed of dog owner have in common?” and answers, “Both insist that Labs are the best thing ever.” A 16-second audio player sits below the image, with the visible caption beginning “Work the labs, and when (not if).” The audio was played to completion; the visible caption remained a partial fragment rather than a complete transcript. The screen then introduces “Connect Event Portal to an Event Broker” and has a “GET CONNECTED” link that opens a new tab. On initial entry the lesson showed 43% progress; after viewing the screen, the table of contents showed 57%. Overall Event Portal Essential progress remained 29%.

An embedded Solace documentation card links to “Configuring Event Brokers in Event Portal.” It says client details and queues can be configured in Designer, and that Event Portal configuration can add, update, or delete client credentials and queues on Solace event brokers. It points readers to Cluster Manager documentation for configuring queues there. The visible diagram maps Designer to a Model Event Broker and then to an Operational Event Broker Service. It shows Application A with a Solace Event Queue, topic subscription, configuration, client profile name, and published event/topic configuration; the model adds client username and credentials; the operational service includes a queue, topic subscription, client profile, ACL profile for publish/subscribe topic exceptions, and client username and credentials. Arrows also connect an AsyncAPI document and the application developer to the application flow. A help section titled “Did you get stuck? Take a look at the below.” embeds “How to Connect your Event Brokers to Event Portal,” with a Solace resource link.

The linked help video is titled “Event Portal | Connecting Your Solace Event Brokers to Solace Event Portal” and runs 1:34. Its settings expose quality and playback speed but no captions or transcript. The title screen repeats the video title. A later slide says Discovery & Audit and Self-Service Access to Events in Runtime require an event broker connected to Event Portal; it contrasts the previous manual installation of Event Management Agent with Solace-managed connection for cloud-managed brokers in private and dedicated regions. At about 0:43, the video shows Cluster Manager > Services with Development-Europe and Staging-Europe, both Enterprise 250, owned by Joseph Lanoux, and marked Running, plus a blank Create Service tile. This is instructional footage; no broker was connected and no service was created or changed.

At about 0:53, the video shows Account Details > Private Regions. It describes customer-controlled private regions containing datacenters where PubSub+ Cloud can deploy event broker services. The table has one Ready region, location Europe, a datacenter named Acme private region, Event Portal Connections Disabled, Environment Default, and Configuration Last Updated Not configured.

At 1:10, the video shows Runtime Event Manager > us-west-solace-staging > Event Broker Connections. The empty state says “No Event Brokers Connected” and “Connect your event brokers to import runtime data,” with a Connect Event Broker button and an Event Management Agent Connections link. No connect controls were activated.

At about 1:30, the demo shows Staging-Europe as Connected. The broker type is Solace, and Connection Details says “Automatically managed by Event Portal - Connected.” The Discovery Scans table reports “No runtime data has been collected”; Associated Objects shows Applications (0) and Event API Products (0).

The lower portion of the lesson displays an office and event-network illustration above the heading “Did you get stuck? Take a look at the below.” Under it is the poster for “Solace Event Portal - Connecting Your Solace Event Brokers to Solace Event Portal,” linked as “How to Connect your Event Brokers to Event Portal.” At this screen the lesson is marked Completed and the internal workshop progress reads 43% overall.

The Solace resource page is labeled DEMO and titled “How to Connect your Event Brokers to Event Portal.” It embeds the same 1:34 Vidyard video and adds the description: connect event brokers to Event Portal to manage, monitor, and organize an event-driven architecture. No additional transcript is provided, and no broker action was requested on that page.

## Lesson 6 of 7 - Sure you got all that?

By Phil FitzGerald. On entry, the workshop is 43% complete and this lesson is 17% complete. An interactive scenario overlays a female guide on an Event Portal environment-configuration screen. The guide says, “I've heard you know a fair bit about Event Portal.” A CONTINUE button advances the scenario. The page also says “You've seen it. But can you share it?”

The page provides these reflection questions:

1. How does Event Portal's approach to event access differ from traditional methods involving middleware or integration teams? What are the key advantages of this shift for developers and governance teams?
2. What does self-service for event data access mean in the learner's role, and why is governance critical to this model?
3. What factors might lead a data owner to require approval for an event, and what are the good and bad implications for the event-consumption lifecycle?
4. How would one explain the relationship between application domains and event sharing in literal and GUI terms?
5. How do queues and subscriptions work together for guaranteed messaging, and how does this differ from direct messaging?
6. What are the trade-offs between specific topic addresses and wildcards, and how might an approver react to a broad wildcard subscription?
7. What steps add a new application to a development environment, and how do ACLs and client profiles manage broker access?
8. What does config push do, what does it need, and how does it change the traditional broker-configuration workflow?
9. How does versioning support governance and rollback, and what rules apply to draft, released, deprecated, and retired versions?
10. What discrepancies can auditing identify between design-time and runtime?

The page repeats the queues/subscriptions guaranteed-messaging question in its second prompt group. It also offers an Ask Solly link that opens in a new tab.

### Scenario screen 1 - approval-required event

The guide asks: “I'm working on a new application and need to consume data from an existing event. It says it requires approval, so what should I do?”

1. Carry on, configure the app to subscribe, and let the system automatically create the necessary access rules.
2. Request approval through Event Portal, wait for the reply, and then either continue configuring or narrow the topic selection.

The second choice matches the lesson's approval workflow: an app cannot consume an approval-gated event until its owner grants access. This is an in-course scenario; selecting an answer does not change a real Event Portal account.

### Scenario response 1 - approval request

Option 2 was selected. The guide repeats the correct response: request approval through Event Portal, wait for the reply, then continue configuring or narrow the topic selection. The guide responds, “Great, and it has me thinking where the 'request approval' setting is. But I'll ask that another time.” A CONTINUE button appears. The scenario now shows 50% lesson completion.

### Scenario screen 2 - promote an application

The guide asks: “I've designed an application and tested it in the development environment and [it] is ready to be deployed to the production environment. What is the best approach to promoting it?”

1. Promote it through Event Portal.
2. Manually copy it from dev to prod as before.
3. Download the AsyncAPI document for the production version and share it with the developers.

### Scenario response 2 - production promotion

Option 1, “promote it through Event Portal,” was selected. The guide responds, “Ahaaa.” A CONTINUE button appears.

### Scenario screen 3 - promoting to production

The guide asks, “Ok, so how would I do that?” The options are:

1. Ask Solly.
2. Change the version state to Released and add it to a modeled event broker in the production environment's modeled event mesh.

The second option follows the described governed release-and-promotion flow.

### Scenario response 3 - release and promote

The release-and-promotion choice was selected: change the version state to Released and add it to a modeled event broker in the production environment. The guide responds, “Logical.” A CONTINUE button appears.

### Scenario screen 4 - production issue

The guide says, “Me again. That application is experiencing issues in production.” No answer choices appear on this screen; it offers only CONTINUE.

### Scenario screen 5 - runtime/design mismatch

The guide asks: “I suspect the runtime config isn't what shows up in the Event Portal design. Any ideas on how to tidy that up?”

1. Delete and redeploy the app to refresh it; there is no way to inspect brokers.
2. Go to the audit screen, trigger a “run discovery scan” on the runtime environment, and compare the results.

The second option matches the course's audit workflow for comparing runtime state with design intent.

### Scenario response 5 - audit and discovery scan

Option 2 was selected: run a discovery scan in the runtime environment and compare it with the Event Portal design. The guide responds, “Reminds me, I need to ensure my EMA is running.” A CONTINUE button appears.

### Scenario completion screen

The guide displays “Scenario Complete!” with a START OVER control. The background is an Event Portal audit view with an audit-results table and a Selected Topics (0) side panel, visually matching the runtime/design audit scenario. The control was not used. The workshop progress remains 43% overall, while the lesson navigation reports 50% complete.

### Lesson 6 completion screen

The reflection-question section is displayed over the Event Portal workflow infographic, including Authorize, Promote, Audit, Measure, Codegen & Implement, and Run labels. The first group has five questions and a “Wondering about something? ASK SOLLY” button; the next group continues below. After the scenario is completed and the page is scrolled, the table of contents marks “Sure you got all that?” Completed and the workshop progress is 57% overall.

## Lesson 7 of 7 - Advanced & Onwards

By Phil FitzGerald. On entry, the workshop is 57% complete and this final lesson is 43% complete. A 40-second audio player displays the caption: “Well done. You're learning has just begun, here are the next-level links for you to enjoy. Congratulations.”

The lesson offers three resource links: Solace Community for questions or suggestions; feeds.solace.dev to generate custom feeds for testing Event Portal live; and Solace's Event Portal how-to videos (“Go on, keep watching”). Two embedded resource cards are also listed: “How to Use Configuration Templates for Self-Service Access to Events” and “How to Have Self-Service Access to Events in the Runtime.” The page ends with “Congratulations. You've earned it.”

The 40-second audio was played to completion; the player returned to 0:00. Its visible caption is the only transcript available in the lesson.

### Lower lesson screen - first advanced video card

The scroll view shows a poster titled “Solace Event Portal - Using Configuration Templates for Self-Service Access to Events,” with the resource heading “How to Use Configuration Templates for Self-Service Access to Events” and a READ MORE SOLACE link. The next video card begins below it.

### Lesson 7 completion screen

The second resource poster is titled “How to Have Self-Service Access to Events in the Runtime” and has a READ MORE SOLACE link. Below it, a stylized Solace office/mascot image displays “Congratulations. You've earned it.” The table of contents marks “Advanced & Onwards” Completed and the Event Portal Essential progress is 71% overall.

### Follow-up - Lesson 1 completion refreshed

Reopening “What is Event Portal for?” changed its navigation state from 83% to Completed and raised overall Event Portal Essential progress from 71% to 86%. The lesson has a 24-second audio clip whose caption says, “Welcome to the Class. We are here to guide you, do use the downloads and do the hands-on.” The audio was played to completion. Its expanded, timestamped transcript was reviewed; the previously recorded summary covers it.

### Event Portal status after reopening - self-attestation gate

Reopening Event Portal Essential confirms the internal workshop is 86% complete. The table of contents shows six of seven lessons completed; “The Event Portal Flow” is 80% complete. Its visible prompt is “Event Portal flows how?” with an embedded video, four-slide image carousel, and the button “TRIED IT IN YOUR SAMPLE ENVIRONMENT?” The course's completion gate is a claim that the learner tried the sample environment. No sample-environment work was done in this session, so the button has not been selected.

### Event Portal lab page checked for an in-course practice environment

The completed “Explore with the Lab” screen asks whether the learner wants to connect Event Portal to an event broker and provides a GET CONNECTED link to instructional media, plus a help resource. The screen does not show a built-in broker sandbox or a self-contained lab to run in this SCORM lesson. The Event Portal Flow attestation remains unselected.
### Event Portal Essential reopened after survey completion - player loading state

The Academy syllabus confirms the course is still In progress at 10/11 and Event Portal Essential is In progress. Reopening it displays a full-screen lesson shell with Previous lesson, Next lesson, and a close control, while the SCORM content area is blank white and exposes no lesson text or interactive items. This loading screen is not treated as lesson completion.
### Event Portal Essential - Academy recovery prompt

After closing the blank expanded lesson shell, the Academy page exposes a “Resume where you left off” button for Event Portal Essential. The syllabus still shows the lesson In progress and overall course progress at 10/11. This is the recovery control for returning to the saved SCORM screen.
### Event Portal Essential, “The Event Portal Flow” - full video transcript captured

The page is lesson 4 of 7 in the SCORM module, which shows 86% complete. Its heading asks “Event Portal flows how?” The expanded transcript for Phil FitzGerald’s video runs from 00:00 to 06:29. The proposed developer workflow starts by discovering existing event objects and permissions, then designing new objects or updating versions. Developers can export designs through APIs to automation platforms or use Event Portal Config Push to update brokers. They compare design with broker state, track KPIs, and repeat the lifecycle of introducing, improving, or retiring assets (00:00–01:16).

The walkthrough then explores what is already available: some application domains are browsable but not editable; applications can be published, in edit mode, or retired; events may be local to a domain or shared from another domain. Runtime Event Manager shows event meshes, environments, applications deployed to runtime, and broker connections. Message-flow arrows show direction. The designer's component view can simplify a busy graph and expose component details (01:16–02:31).

For a design change, the developer adds an application and a shared event, associates them, or finds an event through the catalog and selects its version. The application version shows publish/subscribe relationships and whether it belongs to an environment. A consumer can be a queue or direct subscription; the developer specifies a topic address and previews which events would match. The workflow calls out that an owner may need to approve the change (02:31–03:49).

Queue configuration can be detailed directly or use queue templates to standardize available choices. Change requests show their approval status. The developer adds an updated application to an environment, supplies broker credentials, and gives the owner context in a request comment. After changing a subscription's topic-level choices, the developer resubmits and receives approval. The approved configuration can then be exported through an asynchronous API for CI/CD or sent with Config Push; the transcript asks viewers to find the asynchronous API download area (03:49–04:55).

In Runtime, the developer reviews the target broker, previews an application version promotion, and applies it. The Event Management Agent (EMA) performs Config Push, after which the broker is checked for the expected configuration. Later changes repeat the preview and deployment cycle. A rollback can select an earlier version and run Config Push again. Finally, the EMA audits live broker configuration and returns differences that can be used to update the design or remove obsolete objects. The closing point is to improve speed without reducing safety or security (04:55–06:29).

This is a narrated demonstration and an instruction to mimic the flow in a sample environment; it does not show that the sample exercise was performed during this session. The four-slide image carousel and the sample-environment attestation remain to be inspected.
### Event Portal Flow - carousel slide 1 of 4

The first image uses an airline developer scenario. It asks, “You are a Developer for an Airline. What kind of application domains would you expect to see?” The phrase “application domains” is highlighted. The image shows a Solace-branded passenger airplane and left/right carousel arrows; slide 1 is selected. The sample-environment attestation button is visible below the carousel and remains unselected.
### Event Portal Flow - carousel slide 2 of 4

The second image switches to a telecom developer scenario. It asks, “You are on a Dev team for a Telecoms company. What's a typical shared event between call record and billing domains?” The phrase “shared event” is highlighted. A Solace-branded mobile device graphic shows connected event nodes and directional arrows. Slide 2 of 4 is selected; the sample-environment attestation remains visible and unselected.
### Event Portal Flow - carousel slide 3 of 4

The third image presents a Financial Services team scenario. It asks, “You are working in a Financial Services team. What topic address would you advise for their payment security check team?” The phrase “topic address” is highlighted. The illustration shows a Solace-branded payment card with event-routing lines and a “PAYMENT SYSTEM” label. Slide 3 of 4 is selected; the sample-environment attestation remains visible and unselected.
### Event Portal Flow - carousel slide 4 of 4

The final image frames a construction scenario. Its visible prompt reads, “You advise a construction . What events would you expect to require approval requests?” The word “events” is highlighted; the displayed sentence does not expose a word after “construction” in the accessible text. The illustration shows a Solace-branded hard hat with connected, directional event nodes. Slide 4 of 4 is selected. The “TRIED IT IN YOUR SAMPLE ENVIRONMENT?” control is visible and remains unselected because the sample exercise has not been performed.
### Event Portal Essential, “Explore with the Lab” - resource details on return

This is lesson 5 of 7, “Explore with the Lab.” The page's heading asks what techies and a certain breed of dog owner have in common and answers that both insist Labs are the best thing ever. Under “Work the labs, and when (not if),” it offers “Connect Event Portal to an Event Broker” with a GET CONNECTED link that opens a video in a new tab. The help section links “How to Connect your Event Brokers to Event Portal.” The embedded Solace documentation says Designer configuration can add, update, and delete client credentials and queues on Solace event brokers. These are instructions and documentation links; the page does not expose an in-course sandbox or provisioned broker to practice on.
### GET CONNECTED resource - instructional video landing screen

The GET CONNECTED link opens a Solace video page titled “Event Portal | Connecting Your Solace Event Brokers to Solace Event Portal.” The page shows a video cover and Play Video control. It is instructional media, not a provisioned practice environment or broker console. Next action: inspect the guide to learn how a broker is connected, then return to the course.
### GET CONNECTED guide - key points from 1:34 video

The video “Connecting Your Solace Event Brokers to Solace Event Portal” explains that Runtime Discovery & Audit and self-service access to events require an event broker connected to Event Portal. It contrasts earlier manual installation of the Event Management Agent with Solace-managed connection for cloud-managed event brokers in private and dedicated regions. A demonstration screen shows Runtime Event Manager's modelled event-mesh list with example development, production, staging, Solace, and Kafka entries. The media ends at 1:34 on its replay screen. The video is instructional and demonstrates populated sample data; it does not expose or provision a learner-specific sandbox.
### Event Portal Flow revisited after inspecting the lab resources

Returning from the external connection guide to the SCORM table of contents restored “The Event Portal Flow” to carousel slide 1 of 4. The module still reports 86% complete, and the sample-environment attestation remains visible on the flow lesson. The recorded video transcript and four slide prompts remain in this file.
### Event Portal Flow restored after Activity Guide check

After returning from the Activity Guide screen, the saved SCORM module resumes at “The Event Portal Flow,” lesson 4 of 7. The module reports 86% completion; the side navigation marks this lesson in progress while the other six lesson entries are complete. The course remains at 10/11 LMS lessons completed.

### Official lab provisioning requirements checked

Official Solace guidance confirms that the Event Portal lab flow uses a learner-provisioned environment. The [Design, Code, Deploy with Solace Event Portal codelab](https://codelabs.solace.dev/codelabs/design-code-deploy-with-event-portal/?index=..%2F..index) instructs learners to register for a Solace Cloud trial, provision a PubSub+ Cloud broker, configure the modeled environment, and later push configuration to that broker. Its trial signup requires accepting Solace terms. The [Event Portal overview](https://docs.solace.com/Cloud/Event-Portal/event-portal-overview.htm) describes deploying runtime configuration to brokers and notes that the target environment must be enabled for runtime configuration. The [Event Portal Getting Started guide](https://solace.com/products/event-portal/event-portal-getting-started/) likewise describes setting up application domains, environments, modeled brokers, and operational broker connections.

The Academy's “Explore with the Lab” materials provide connection instructions and a demonstration, but this course session does not expose a learner-specific sandbox, broker, or account. The remaining “TRIED IT IN YOUR SAMPLE ENVIRONMENT?” button is a self-attestation, so it is not selected without an actual sample-environment exercise. No Config Push or broker change was performed.
## Resume checkpoint (historical; superseded by course completion)
This checkpoint records the course state before completion was later confirmed by the Academy on 2026-09-24. It is retained as historical context, not as the current resume point.
## Resume checkpoint

Last verified course position: Solace Essentials is 10/11 lessons complete. Event Portal Essential is 86% complete; “The Event Portal Flow” is lesson 4 of 7 and remains the only incomplete course lesson. The survey and all other lessons are complete.

Current blocker: the final flow lesson asks the learner to attest that they tried the workflow in a sample environment. The course provides instructions but no learner-specific sandbox. Official Solace guidance describes creating a trial account and provisioning a broker, followed by runtime configuration deployment. The user has asked to continue autonomously but has not identified an existing Event Portal tenant, broker, or environment or specified the changes allowed there. Do not select the attestation until the exercise has actually been performed. To resume, use a user-designated sample environment and its permitted scope; if a new Solace trial is required, the learner must accept the signup terms and establish the account and broker. The course is not yet complete.
## Key visual asset recovery

The archived notes describe the six-image sample carousel, a 13-marker course infographic named Course_Graphics_Event Portal 1920.png, the Event Portal workflow graphic, the four-slide Event Portal Flow carousel, and resource posters. These original visuals are no longer exposed by the completed course page; its lesson player offers a retake action. No substitutes were created.

No local course image was available to link from this lesson. The course page currently confirms completion, and reopening completed SCORM content exposes a retake action rather than its lesson screens. The lesson image folder is ready for source assets; no substitute images were fabricated.
