---
title: "Event Monitoring"
document_type: lesson
learning_path: "Solace Certified Event Broker Administrator Associate Path"
course: "Solace Essentials"
lesson_order: 7
source: Solace Academy
---

# Event Monitoring

- **Course:** Solace Essentials
- **Syllabus order:** 07
## LMS update on opening Event Monitoring


### Event Monitoring SCORM launch screen

The lesson opens with its title and a Start link. The instructions say to navigate between steps with the up and down arrow keys or the step controls on subsequent screens.

### Event Monitoring screen 1 of 10 - Lesson Objectives

The objectives are to introduce monitoring capabilities; explore the basic statistics and metrics available for monitoring; learn how to get support; and explore logs through a hands-on activity.

### Event Monitoring screen 2 of 10 - monitoring challenge prompt

An interactive scenario opens with the title “There is a lot to keep track of!” The guide says complex systems are difficult to monitor and asks what monitoring solutions are available for Solace. CONTINUE is the only visible action.

### Event Monitoring screen 2 of 10 - monitoring needs and response choices

The guide says they need to collect and store metrics, display data visually, and receive notifications when things change, then asks whether PubSub+ offers easy ways to do this. The two responses are: (1) “I'm not sure...” and (2) “Yes, there are a couple of methods you can use to monitor and view your data!”

### Event Monitoring screen 2 of 10 - positive response

Option 2 was selected, affirming that PubSub+ has methods to monitor and view data. The guide responds, “That's great to hear!” and presents CONTINUE.

### Event Monitoring screen 2 of 10 - Scenario Complete


### Event Monitoring screen 3 of 10 - monitoring requirements and Visualization graphic

The lesson identifies three requirements for monitoring PubSub+ brokers: (1) collect metrics and store them in a database; (2) handle events by receiving, correlating, tracking their status, and triggering alerts; and (3) visualize metrics, events, or alerts over time through dashboards. It clarifies that “events” here means system/monitoring events, not application-shared events; a client disconnect caused by a network outage is an example. A large Visualization graphic contains three collapsed, not-yet-viewed markers. Beneath it is a “Key Functions of Monitoring” card with a START button.

### Event Monitoring screen 3 of 10 - metrics collection and storage marker

The “Metrics Collection & Storage” marker opens a popover listing automated collection, configurable polling, and flexible database storage. Its popover includes Previous and Next controls; two other markers remain in the graphic.

### Event Monitoring screen 3 of 10 - Event Handling marker

Using the marker popover’s Next control opened “Event Handling,” with four functions listed: status updates, security events, audit trails, and event status correlation. The Metrics Collection & Storage marker remains available to the left, and another marker is still to inspect.

### Event Monitoring screen 3 of 10 - Visualization marker

The “Visualization” marker lists real-time and historical views, predefined and customizable thresholds and dashboards, historical trending analysis, and alert management. The three graphic markers have now all been viewed; the Key Functions of Monitoring card remains below with its START control.

### Event Monitoring screen 3 of 10 - Key Functions, step 1: Metrics Collection and Storage

The three-step interaction opens on Metrics Collection and Storage. It says monitoring solutions can collect and store broker metrics-status, state, KPIs, and SLAs-and events such as HA failover and failures in a database. The illustration shows varied signals flowing through a collection funnel into a dashboard/database. Step 1 is selected; steps 2 and 3 and a completion control are available.

### Event Monitoring screen 3 of 10 - Key Functions, step 2: Visualization

The interaction says stored metrics and events can be used for visualization, capacity analysis, and performance-trend analysis. A colorful multi-chart dashboard illustration accompanies the text. Step 2 is selected; step 3 and the completion control remain.

### Event Monitoring screen 3 of 10 - Key Functions, step 3: Event Handling

The interaction says metrics should be interrogated and alerts generated or sent based on autonomous broker events. Those alerts appear in the user interface and can also be sent to devices to notify people when something is wrong or unexpected. A monitoring-console illustration accompanies the text. Step 3 is selected; the final completion control remains.

### Event Monitoring screen 3 of 10 - completed Key Functions interaction

After completing all three substeps, the interaction displays: “It is important that any monitoring solution you deploy has these key components.” The completion checkmark is highlighted; START AGAIN is available but unused. The step control advances to step 4.

### Event Monitoring screen 4 of 10 - Ways to Monitor PubSub+ Event Brokers

The screen has three tabs: PUBSUB+ MONITOR, PUBSUB+ INSIGHTS, and SYSLOG EVENTS AND SEMP. The default PubSub+ Monitor tab describes a Solace product that can be deployed on-premises or in the cloud to monitor PubSub+ Event Brokers deployed in Cloud, Software, or Appliance environments.

### Event Monitoring screen 4 of 10 - PubSub+ Insights tab

The Insights tab identifies PubSub+ Insights as Solace's other monitoring product: a service-monitoring solution available directly from the PubSub+ Cloud Console.

### Event Monitoring screen 4 of 10 - Syslog Events and SEMP tab

For organizations integrating existing monitoring solutions or collecting metrics programmatically, brokers provide Syslog Events pushed to external Syslog servers for real-time monitoring, and SEMP (Solace Element Management Protocol). SEMP can poll broker metrics at regular intervals; custom integrations can store and analyze the results.

### Event Monitoring screen 5 of 10 - SEMP for Monitoring

SEMP can collect monitoring metrics as well as configure/administer broker objects; examples include queues and client connections. The lesson links a separate monitoring REST API and online Swagger reference at `docs.solace.com/API-Developer-Online-Ref-Documentation/swagger-ui/monitor/index.html` for the supported APIs. Applications poll the broker at a configured interval; polling should avoid impacting application messaging, and the interval determines metric granularity. An API reference and client-library illustration accompanies the text.

### Event Monitoring screen 5 of 10 - zoomed SEMP reference illustration

The enlarged illustration pairs a REST/Swagger-style reference showing object resources, HTTP methods, and query parameters with SEMP tutorial cards. The cards include basic operations using curl and Java, generating SEMP client libraries, and Message VPN with Queue examples in Java, Python, and Ruby.

### Event Monitoring screen 6 of 10 - Syslog Events

PubSub+ Event Brokers generate Syslog messages for broker events, including routine client connects/disconnects, failures such as disk failure, and emergency/critical events such as hardware-level failure on an Appliance. The broker records these messages using Linux Syslog facilities. It can also push them in parallel to an external Syslog server over UDP. A warning-symbol illustration accompanies the text.

### Event Monitoring screen 7 of 10 - PubSub+ Monitor

PubSub+ Monitor is described as a comprehensive best-practice solution that collects metrics, handles events, stores both, manages alerts, and provides pre-built dashboards for broker health. It is a standalone client/server application, with its service deployed on virtual machines on-premises or in the cloud and a browser-based client. It is agentless and connects to broker SEMP interfaces. The architecture diagram shows Cloud, Software, and Appliance brokers connected through SEMP and Syslog to PubSub+ Monitor, with a browser client.

### Event Monitoring screen 7 of 10 - zoomed PubSub+ Monitor diagram

The enlarged architecture places PubSub+ Cloud, Software, and Appliance brokers as sources. SEMP and Syslog feeds converge on a PubSub+ Monitor service, which is accessed through a browser client.

### Event Monitoring screen 8 of 10 - PubSub+ Insights

Unlike standalone PubSub+ Monitor, Insights is a service-monitoring solution built into the Cloud Console. It provides centralized, proactive, at-a-glance monitoring for Cloud and Software brokers, including metric collection, pre-built dashboards, and capacity-planning metrics. It can show ready-made or custom dashboards, configure event notifications, access broker service logs, collect hundreds of metrics, show application insights, be set up easily, and provide real-time and historical data. A capacity-overview dashboard illustration accompanies the list.

### Event Monitoring screen 8 of 10 - zoomed PubSub+ Insights dashboard

The enlarged “Capacity Overview (Early Access)” dashboard image shows a service selector and client-connection metrics, including current connections, utilization, a connection-utilization trend by service, and high-water, minimum, and average connection counts. Additional MQTT and REST panels show connection counts and utilization trends for incoming and outgoing connections. These are example dashboard values in the course illustration.

### Event Monitoring screen 9 of 10 - monitoring solutions sorting activity

The screen asks the learner to drag each card into the category that best fits: PubSub+ Monitor, PubSub+ Insights, or Both. The displayed card is “Has pre-built dashboards.”

### Event Monitoring screen 9 of 10 - completed monitoring solutions sorting activity

The five cards are classified as follows: “Has pre-built dashboards” - Both; “Connects to brokers' SEMP interface” - PubSub+ Monitor; “Standalone application” - PubSub+ Monitor; “Built into the Cloud Console” - PubSub+ Insights; “Works with PubSub+ Cloud” - Both. The activity confirms “5/5 Cards Correct.” REPLAY is available; it was not used.

### Event Monitoring screen 10 of 10 - Activity Guide exercises

The final screen says to try Exercise 7, “Viewing Syslog Logs Files,” and Exercise 8, “Gathering Diagnostics for Docker Containers,” in the Solace Essentials Activity Guide. These are hands-on activities outside this SCORM lesson; no broker or Docker environment was configured or changed.

### Event Monitoring LMS status after leaving the lesson

## Key visual asset recovery
