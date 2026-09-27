---
title: "iPaaS Integration"
document_type: lesson
learning_path: "Solace Certified Integration Associate Path"
course: "Event-Driven Integration with Solace Platform"
lesson_order: 5
source: Solace Academy
---

# iPaaS Integration

- **Syllabus order:** 05
- **Course section:** The Concepts

## Notes

### iPaaS Integration

Integration Platform as a Service (iPaaS) platforms are cloud-based systems for developing, executing, and governing integration flows between applications and services. The lesson says they typically provide pre-built connectors to common applications and services, support cloud and on-premises integration, tools for designing integration workflows, and monitoring and management capabilities.

### iPaaS and Micro-Integrations Compared

| Dimension | Micro-Integrations | iPaaS |
| --- | --- | --- |
| Architecture | Distributed, lightweight components. | Comprehensive, centralized integration hubs that handle many integration patterns. |
| Integration style | Event-driven. | Traditional request-reply with event capabilities added. |
| Deployment | Independent; can be deployed near event sources and targets. | Centralized deployment, often cloud-based. |
| Scope | Purpose-built for specific integration tasks. | General-purpose with pre-built connectors. |
| Complexity | Each integration is isolated, reducing overall complexity. | Implementations can develop “integration spaghetti” as they grow. |
| Scaling | Horizontally scalable; each integration scales independently. | Platform-level scaling may create bottlenecks. |
| Pattern fit | Optimized for event-driven patterns. | Supports multiple patterns but is often optimized for request-reply. |
| Change impact | Update or replace individual integrations without affecting others. | Updates may affect multiple integration flows. |
| Event mesh | Native integration with event mesh technology. | Often needs adapters or connectors for event mesh integration. |
| Implementation speed | Quick for specific use cases. | More setup time, but faster for standard integrations. |

### Additional Learning Resources

The closing carousel recommends three related courses:

- **Event Driven Integration Course – Boomi:** asks how Solace and Boomi work together; [View the Course](https://training.solace.com/learn/courses/597/event-driven-integration-course-boomi).
- **Event Driven Integration Course – SAP:** asks how Solace and SAP work together; [View the Course](https://training.solace.com/learn/courses/593/event-driven-integration-course-sap).
- **Event Driven Integration Architecture – MuleSoft:** asks how Solace and MuleSoft work together; [View the Course](https://training.solace.com/learn/courses/550/event-driven-integration-architecture-mulesoft).


## Visuals

- [iPaaS Integration title card](img/ipaas-title.png).
- [Boomi course card](img/recommended-boomi-course.jpg).
- [SAP course card](img/recommended-sap-course.jpg).
- [MuleSoft course card](img/recommended-mulesoft-course.jpg).
