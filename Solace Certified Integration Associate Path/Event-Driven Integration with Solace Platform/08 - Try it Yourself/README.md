---
title: "Try it Yourself"
document_type: lesson
learning_path: "Solace Certified Integration Associate Path"
course: "Event-Driven Integration with Solace Platform"
lesson_order: 8
source: Solace Academy
---

# Try it Yourself

- **Syllabus order:** 08
- **Course section:** The Click

## Notes

### Try It Out

The opening screen is titled “Try It Out.” It asks the learner to watch the Micro-Integrations demo. A “Watch now” link opens the full video on LinkedIn. The next section, “Choose What’s Right for You,” points to the Solace Platform Integration Hub and its available micro-integration types through a “View” link. These external pages are presented as resources; they have not been opened.

The embedded 45:27 “Solace Office Hours - Sept 2025 - Micro-Integrations Update!” recording was played through at 2×. No separate transcript or captions control was exposed, although some Q&A caption text appeared over the video. Visible content covered a Micro-Integration catalog with SQL Server CDC, MQTT, Oracle AQ, PostgreSQL CDC, Qdrant (Beta), Salesforce, SFTP, and Snowflake; a Demo PG CDC mapping screen; an AI mapping dialog that warns it overrides existing mappings and recommends manual mapping to preserve them; a Number-to-String transformation; and dynamic values for seconds since epoch and current UTC date-time. The demo showed the Demo PG CDC flow from the PostgreSQL database postgres, table public.employees, to a Solace Target service plm-demo and destination employees/cdc/alldepartments, with state Not Deployed and 17 total messages.

The presenters also showed a connector workflow configured in application.yml with JSON source and target payloads, ordered transformations from cdc_after_payload, and retry/failover settings including max-attempts 3, a 1000 ms initial back-off, and a 10000 ms maximum. A Simple Queuing example described a Micro-Integration bridging a Solace PubSub+ Event Broker and a Simple Queuing Service bidirectionally, providing protocol translation, message transformation, and delivery assurance; the visible prerequisites were Java 17 and Docker or Podman. A Q&A caption said Micro-Integrations can be deployed as smaller Docker or on-premises Kubernetes workloads similar to self-managed connectors. The multi-flow preview showed multiple source-queue → transformation → target-topic flows sharing an SQS service location and Solace broker; node-size limits shown were Small up to 5 flows (1× SKU), Regular up to 10 (2× SKU), and Large up to 20 (4× SKU). The final visible creation wizard had three steps: Micro-Integration Flow Details, Mappings, and Micro-Integration Summary; the source connection used a queue endpoint and message selector.


## Visuals

The visible title banner reads “Try It Out” and “Try It Yourself,” followed by the Micro-Integrations Demo heading and embedded video area. The recording displayed catalog, mapping, transformation, deployment, configuration, architecture, and flow-creation screens. The final screen is a congratulations panel with a graduation icon and a pale hexagon pattern. Browser screenshots were reviewed, but no local image files could be saved with the available capture workflow; the img folder is empty.
