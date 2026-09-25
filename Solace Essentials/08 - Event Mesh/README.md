# Event Mesh

- **Course:** Solace Essentials
- **Syllabus order:** 08
**Academy status:** Completed on 2026-09-24
### Event Mesh screen — blank embedded lesson with LMS completion toast

On opening Event Mesh, the LMS displayed a “Lesson completed” toast. The lesson content area remained blank, and its embedded SCORM frame showed `about:blank`; the LMS navigation offered Summary as the next lesson. No Event Mesh lesson text or activity was available to capture in the visible page.

### Event Mesh lesson preview — title screen after SCORM load

After reopening Event Mesh from the syllabus, the embedded package finished loading and displayed its preview: a centered “Event Mesh” title with a downward arrow and an accessible Start link. The syllabus continued to mark the lesson In progress.

### Event Mesh screen 1 of 2 — lesson objectives

The lesson objectives are to understand Event Mesh and demonstrate how to create an Event Mesh.

### Event Mesh screen 2 of 2 — embedded video preview

The final SCORM step embeds a video titled “How to Build an Event Mesh with Solace Platform” by Solace. Its thumbnail reads “Building an Event Mesh with Solace Platform” and shows a play control plus a “View on YouTube” link. The step's Next control is disabled until content is completed; the player frame is exposed as `about:blank` in the accessibility tree.

### Event Mesh embedded video — playback and captions

The Solace video started playing in the course at 0:03 of 9:03. English captions are enabled in the player. The visible opening caption says the presenter will walk through building an Event Mesh using Solace technology. The player offers speed settings; the lesson's Next control remains gated on completion.

### Event Mesh video — key points from the English captions

The Solace video’s caption transcript is 9:02; the embedded player displays 9:03. It defines an Event Mesh as an architectural layer above the network that lets distributed applications, microservices, and IoT devices communicate dynamically and decoupled through publish/subscribe. Applications connect to event brokers; consumers register subscriptions, publishers send events, and brokers route data according to those subscriptions (0:24–0:55).

Clustering brokers shares subscription information across the mesh and supports horizontal scaling. A consumer can subscribe on one broker and receive data published through another. DMR can bridge brokers over a WAN, including across regions, and support hybrid or multi-cloud designs; data flows to subscribers on demand, reducing unnecessary bandwidth use (0:55–2:21). The video focuses on data movement and identifies Dynamic Message Routing (DMR) as the Solace feature used to build the mesh (2:23–2:41).

For Solace Cloud, the demonstration starts with multiple broker instances and uses the Event Mesh View to visualize the topology. It creates DMR bridges through each broker’s Web Manager by opening Bridges > DMR Bridges > Click to Connect, choosing the Solace Cloud account and remote broker/Message VPN, then applying the fetched connection details. The presenter enables compression for WAN links and creates links among three brokers (2:44–5:28). The video notes that Cloud preconfigures cluster details and credentials.

For software or appliance brokers, the extra step is to create a cluster before configuring DMR. Then open DMR Bridges, connect to the remote broker, choose the Message VPN, and consider the connection direction: a broker behind a router/firewall may need to initiate the link outbound. Configure the cluster credentials, create the bridge, and test that it reaches Up status (5:32–8:27). Demo credentials shown in the video are intentionally omitted from these notes.

The presenter closes by noting that DMR setup can be automated through the SEMP REST management API and tools such as Chef, Puppet, or Ansible (8:27–8:52).

### Event Mesh embedded video — playback completed

The player reached its end screen at 9:02 of 9:03 and displays “Play video again,” the outro segment, and YouTube end-screen recommendations. English captions were enabled during playback. The SCORM step remains 2 of 2 and its Next control stays disabled because this is the last step; the LMS navigation offers Summary as the next lesson.
## Key visual asset recovery

The archived notes preserve the embedded-video transcript and describe its broker-topology demonstration. No reusable still image was available in the completed course page.

No local course image was available to link from this lesson. The course page currently confirms completion, and reopening completed SCORM content exposes a retake action rather than its lesson screens. The lesson image folder is ready for source assets; no substitute images were fabricated.
