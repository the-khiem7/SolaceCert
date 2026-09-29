---
title: "Integration Patterns"
document_type: lesson
learning_path: "Solace Certified Integration Associate Path"
course: "Event-Driven Integration with Solace Platform"
lesson_order: 3
source: Solace Academy
---

# Integration Patterns

- **Syllabus order:** 03
- **Course section:** The Concepts

## Notes

### Introduction to Integration Patterns

The opening screen introduces key factors for choosing an event-driven integration pattern through a billing-address correction. A customer’s billing record changes from “21 Frank Street” to “12 Frank Street.” The sample customer table contains one billing address and three shipping addresses, each with its own address ID, version, and timestamp. The lesson points out that the billing address is replicated across CRM, billing, shipping/logistics, marketing, and other systems, which may be owned by different teams or companies. It asks how to implement the correction in an event-driven environment and what information to send; this screen poses the design question without answering it.


### Event Notification Pattern

The publisher sends a small notification to the broker that a change happened. The minimal example says customer 2293922’s address entity changed. Its sample event envelope includes `specversion` 0.3, type `com.RealStore.customer.address`, source `/address`, an event ID, timestamp, `customerId`, and `datacontenttype` `application/json`; it omits the changed address values. The lesson then shows a more specific notification that adds metadata identifying address ID 114422 and purpose `billing`. It still omits the updated street address. In both cases, consumers are expected to query the read endpoint for the latest state. The “Quick Reference - Address Table” accordion expands to show the same four-row example table from the introduction.


### Event Change Pattern

In contrast to Event Notification, the Event Change Pattern includes updated data in the event payload. The first sample identifies customer 2293922 and billing address ID 114422, then carries an `oldState` address line (`21 Frank Street`) and `newState` address line (`12 Frank Street`). The lesson also shows an alternative snapshot containing the billing purpose, both address lines, and an address timestamp in each state. Its concluding note says the updated data is specified in both examples. The “Reference - Address Table” accordion reveals the same four-row customer address table used earlier.


### Event Payload Pattern

This screen frames payload selection around what consumers benefit from: data about a specific customer versus records for a specific entity, while ignoring the larger context the entity operates in. Its example places the complete set of four address records inside the customer-level old and new state: billing address 114422 plus three shipping addresses. Only the billing address line changes from “21 Frank Street” to “12 Frank Street”; the three shipping addresses are repeated unchanged in both arrays. The reference accordion links back to the address table, and the concluding note says the updated data is specified in this scenario.


### Determining Which Pattern to Use

The final section recommends weighing four factors. The consuming systems’ ability to manage out-of-order delivery matters because ordering guarantees are expensive and require deeper processing logic than idempotence. If consumers cannot reliably reorder or select messages to process, the notification pattern is simplest: event time and processing time are decoupled, consumers fetch the latest state from the data owner, and idempotent consumers can tolerate delay and batch work. This depends on a highly available read service, since the callback may occur well after the event.

Batching can reduce downstream API calls, including for SaaS products that charge per call, when propagation delay is negotiable. The notification pattern makes this simpler; with change or payload events, messages may need to be compared before they can be combined, and complexity rises if the provider does not select the payload.

Publisher simplicity is another criterion. More verbose events take more work to construct and extract, cost more to send, and increase exposure to out-of-order risk. Including data in messages also raises channel protection needs such as encryption and masking.

A requirement for consumers to audit every state change overrides the earlier criteria. The lesson says entity auditing ideally belongs in the event-sending service as the single source of truth, with consumers accepting eventually consistent replication. If an external system must audit every change, it has to handle out-of-order delivery, making the event payload pattern the only viable option in that case.

The four audio players show durations of 1:19, 0:47, 0:30, and 0:59. All four Transcript panels were expanded and reviewed. The “So What’s the Gist?” carousel has two slides. “Simplicity is Key” says Event Notification is the simplest pattern for publishers and consumers to define and implement, although consumers need an additional error-handling API call if the endpoint that retrieves the current state is unresponsive. Its image shows two people beside a computer with a “TRY AGAIN” error. Slide 2 says handling this extra error call is generally easier than dealing with out-of-order message delivery, which requires inspecting multiple parts of the consumer application and comparing them with the incoming event. When requirements rule out Event Notification, the lesson recommends deciding whether ordering belongs to individual services or a Streaming Pipeline, and ensuring data security rules-particularly for PII-are applied. Its image shows people working around a computer with gears and a wrench. The content cites [Arvind Balachandran’s Medium post](https://medium.com/swlh/event-notification-vs-event-carried-state-transfer-2e4fdf8f6662).





## Visuals

- [Integration Patterns title card](img/integration-patterns-introduction.webp) - title artwork SHA-256 verified as identical across the lesson section title screens.
- [Simplicity recap, slide 1](img/simplicity-is-key-slide-1.webp) - two people beside a laptop showing an error and Try Again.
- [Simplicity recap, slide 2](img/simplicity-is-key-slide-2.webp) - people working on a computer with gears and a wrench.
