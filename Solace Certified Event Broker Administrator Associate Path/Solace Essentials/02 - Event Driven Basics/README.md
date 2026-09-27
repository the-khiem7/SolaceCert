---
title: "Event Driven Basics"
document_type: lesson
learning_path: "Solace Certified Event Broker Administrator Associate Path"
course: "Solace Essentials"
lesson_order: 2
source: Solace Academy
---

# Event Driven Basics

- **Course:** Solace Essentials
- **Syllabus order:** 02
**Academy status:** Completed on 2026-09-24
## Event Driven Basics - Step 1 of 2

The lesson introduces common terminology used in event-driven architecture.

## Event Driven Basics - Step 2 of 2: core terms

- **Events:** Notifications that something changed. They represent business-relevant state changes and cannot be altered after they occur. Examples include a thermostat reporting high temperature, a stock price changing, and a rideshare driver arriving.
- **Event streams:** Continuous, unbounded sequences of events. A stream may have started before a consumer begins reading and may continue indefinitely; events are ordered by when they occurred. Examples include incoming orders, driver location updates, and security-camera video.
- **Commands:** Instructions asking a particular consumer to do something. The consumer processes the request and confirms it to the issuer. Examples include unlocking a connected car by app, automatically braking a train, and turning on home air conditioning.
- **Events and messages:** A message has a header with transmission details and a body containing the transmitted data. Events describe business-level changes; messages are visible at the transport level. Messages can carry events, commands, or raw data. An event message carries an event through an event broker from producer to consumer.
- **Loose coupling:** Producers can publish without knowing which consumers receive an event, and consumers need not know the producers. They can use different languages and platforms. They still share an implicit data contract, such as a JSON schema. Reducing the number of distinct event types can reduce coupling.
- **Event channels:** Logical addresses on a broker. Producers publish to channels and interested consumers subscribe. A broker can host channels for different purposes.
  - **Topics** support publish-subscribe, one-to-many delivery. They use hierarchical names such as `myhome/livingroom/temperature`; wildcards can match multiple topics.
  - **Queues** support point-to-point delivery, where one consumer processes a given event. Multiple receivers can share a queue for load balancing. Queues persist events through broker or consumer failures. The broker acknowledges persistence to the producer; the consumer acknowledges processing before the event is removed.
- **Clients:** Applications that send or receive events are broker clients. Related role terms include sender/receiver, producer/consumer, publisher/subscriber, and requestor/provider.
- **Quality of service:** Choose reliability based on the consequences of message loss.
  - **Direct delivery** favors throughput and low latency, but messages may be lost if there is no subscriber or a consumer falls behind. The course describes this as fire-and-forget.
  - **Guaranteed delivery** stores events and acknowledges successful storage, or reports a negative acknowledgement if storage fails. The broker forwards stored events when consumers are ready and retains them until consumer acknowledgement. It requires broker disk storage and a queue. Topics can be mapped to queues for persistence. The course describes this as store-and-forward.
## Key visual asset recovery

No discrete key instructional visual is described in the archived notes for this lesson.

No local course image was available to link from this lesson. The course page currently confirms completion, and reopening completed SCORM content exposes a retake action rather than its lesson screens. The lesson image folder is ready for source assets; no substitute images were fabricated.
