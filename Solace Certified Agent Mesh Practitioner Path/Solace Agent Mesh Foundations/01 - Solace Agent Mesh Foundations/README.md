---
title: Solace Agent Mesh Foundations
document_type: lesson
source: Solace Academy
learning_path: Solace Certified Agent Mesh Practitioner Path
course: Solace Agent Mesh Foundations
lesson_order: 1
---

# Solace Agent Mesh Foundations

## Course page overview before entering the SCORM lesson

The course is a foundations-level introduction to Solace Agent Mesh, described as an agent development and runtime platform for connecting AI agents and coordinating workflows across an enterprise. It assumes no prior hands-on experience with Solace Agent Mesh. It asks learners to understand how multiple agents coordinate in an enterprise, why event-driven design can outperform polling and batch processing for agents that need to react in real time, and how an Orchestrator that decides at runtime differs from a Workflow that runs consistently.

The course page says learners will study through short readings, interactive knowledge checks, scenarios, and one hands-on activity in the final section. That activity is described as installing the free Desktop App and building a working agent with Quick Build.

### Listed course objectives

- Understand the core concepts and architecture of Solace Agent Mesh, including Agents, Tools, Entrypoints, and the Event Broker.
- Explain the six Agent Development Lifecycle (ADLC) stages: Hiring, Onboarding, Coaching, Supervision, Teamwork, and Improvement.
- Apply a cost, governance, security, and repeatability checklist when reasoning about a new agent.
- Distinguish Orchestrator-based from Workflow-based coordination and identify which fits a situation.
- Identify the five coordination patterns workflows are built from and the node types underneath them.
- Explain how event-driven design lets agents react to real-time data instead of polling, waiting for batch files, or relying on custom point-to-point integrations.
- Understand how open protocols such as A2A and MCP prevent vendor and model lock-in.
- Build a first working agent with the free Desktop App and Quick Build.

### Audience and prerequisites

The intended audience includes people evaluating Solace Agent Mesh for organizational AI plans; engineers, architects, and technical leads seeking conceptual grounding; product and program managers assessing what agentic AI systems can and cannot do; and learners preparing for the hands-on Solace Agent Mesh Developer path. There are no required prerequisites. The page notes an optional primer video for learners new to large language models or retrieval-augmented generation.

### Outcome stated by the course

The course promises a mental model of how agentic AI systems are built, governed, and coordinated, plus firsthand experience standing up a first working agent. It says the hands-on Developer path builds on this foundation.

No instructional visual appeared on this course overview screen. The Academy showed the syllabus lesson as **Not started** and the course as **0 of 2 lessons completed**; this is the live starting state, before entering the SCORM lesson.

## SCORM lesson content

Screens and internal activities are recorded below in the order presented by the SCORM module.

## Academy player screen before starting the SCORM module

The lesson player shows this course as **in progress**, with **0 of 2 lessons completed**. Its syllabus lists this SCORM lesson followed by the separate **Feedback Survey - 2025** lesson. The learning-plan progress card shows **0 of 2 courses completed** and identifies the Practitioner exam as the next mandatory course, still **Not started**. The player offers a **Start learning now** button. No instructional content or key course visual is shown on this player screen.

### Screen 1 — Welcome to Solace Agent Mesh Foundations

**Section label:** Lesson 01 — Welcome. The screen asks learners to follow fictional Acme Retail through a stockout and identify problems caused by adding AI agents in isolation. The screen estimates about 7 minutes and lists one video and one activity. The SCORM progress indicator reads 10%; the course contents panel estimates about 55 minutes remaining.

The Welcome text describes Solace Agent Mesh as an agent development and runtime platform that provides one consistent way to build, connect, and run agents at scale. The course uses Acme Retail as a running example and ends with a hands-on section in which learners build and run an agent.

The screen previews six topics: why bolting agents onto existing systems in isolation backfires; the six Agent Development Lifecycle stages; the components running under an Agent Mesh; how A2A and MCP avoid lock-in to one model, cloud, or framework; when to use an Orchestrator versus a Workflow; and building and running a first working agent. Its closing statement says Solace Agent Mesh helps users build, test, deploy, observe, and improve agents.

**Internal section map shown in the SCORM sidebar:** Welcome; Why a Lifecycle, Not Just a Framework; The Agent Development Lifecycle; Componentization: What's Actually Running; Coordinating Multiple Agents: Orchestrator vs. Workflows; Agents Reacting, Not Polling; Getting Started; Glossary. This is the module's internal content navigation; it remains within the single Academy SCORM syllabus lesson.

**Media status:** The screen advertises one video and one activity for this section, but neither has been opened on this screen. No transcript or captions were shown here.

**Visual status:** The enlarged platform diagram is described below. The course image was inspected, but its local-file limitation is recorded below.

#### Welcome visual — Solace Agent Mesh platform overview

The enlarged course diagram places People interfaces (Web Chat UI, Slack UI, Teams UI) and Apps & Agents (enterprise apps, Solace Event Mesh real-time events, and webhook events) above an **Entrypoints** layer labeled “Secure, Session Management.” Inside a green platform area it groups **Agent Builder**, **Solace Native Agents**, **Observability & Evals**, **A2A Proxy** for external agents, **Connectors** for data access and real-time context, and **AI Services** for any LLM or SLM. The diagram places cloud and orchestration logos (AWS, Azure, Google Cloud, Kubernetes, Helm) beside the platform. Below it, A2A connects to third-party agents; Connectors connect to enterprise data sources such as SQL and APIs and to text and image models; AI Services connect to “100+ LLMs/SLMs.” Arrows show the interfaces/events feeding Entrypoints and the platform connecting out to agents, enterprise data, and models.

**Visual file limitation:** I inspected the original enlarged diagram and captured it in the browser view. The course exposes no download control for the image, and Chrome's image context action did not expose a save option. The available Chrome screenshot interface returned a display-only capture without a workspace file path; its local-data export alternative was blocked by browser URL policy. I therefore cannot place a faithful screenshot or original asset in `img/` and am preserving the visual's visible labels and relationships here instead of fabricating an image.

### Screen 2 — Our Use Case: Acme Retail's stockout

Acme Retail sells outdoor gear through **1 website, 2 call centers, and 41 physical stores**. In late September, a Denver customer buys the last pair of a discontinued hiking boot online. As soon as the order clears, the warehouse system immediately sets the remaining stock to zero, but the Denver store, call centre, and two AI assistants built the previous quarter do not know the item sold.

#### Existing agents (both tabs inspected)

- **Customer Assistance Agent:** Runs on Acme's website and answers shopper questions such as “Is this in stock?”, “Does it come in my size?”, and “When will it ship?” It cannot tell customers anything the inventory database has not reported. That database updates only from an overnight batch file, so the agent is not wrong about what it knows; it is always answering from last night.
- **Staff Assistance Agent:** Runs on handheld scanners carried by store staff so they can check what is (or should be) on the shelf without visiting the back room. It reads the same inventory system as the website but refreshes about every twenty minutes instead of overnight. If a stockout occurs at minute six after a refresh, it can remain invisible to staff for up to fourteen more minutes.

The screen says both agents use the inventory database's most recent state. The store therefore continues selling a boot that no longer exists until a register catches it or a caller complains that the website said it was in stock. The warehouse had the correct zero count immediately; the problem is that almost nothing else in the business heard about it in time. The course labels the market context **“Retail volatility: demand now moves faster than the systems meant to track it.”** It emphasizes: **“Adding AI agents didn't fix these issues. It exposed it.”**

The course says Acme is not an outlier: Gartner predicts more than **40%** of agentic AI projects will be cancelled by the end of 2027, and MIT found **95%** of organizations building them are seeing zero return. It says the gap is not a shortage of AI, but the lack of a shared way to see what is happening, a standard way to build agents, and a path from demo to production. The screen links to the [Gartner prediction](https://www.gartner.com/en/newsroom/press-releases/2025-06-25-gartner-predicts-over-40-percent-of-agentic-ai-projects-will-be-canceled-by-end-of-2027) and an [MIT NANDA report PDF](https://mlq.ai/media/quarterly_decks/v0.1_State_of_AI_in_Business_2025_Report.pdf).

#### Visual descriptions

The customer-agent illustration shows a shopper using a laptop opposite a purple robot, with image and text-card symbols and simple arrows. The staff-agent illustration shows an employee holding a phone beside a purple robot with headphones; small image, color-palette, and code symbols surround them. The third visual is titled **“The Retail Sector is Facing Greater Volatility Than Ever”** and overlays a jagged green line with labels for Supply Chain Disruption, Digital Sales Growth, Focus on Savings, Real Inventory Visibility, Diversified In-shop Experience, Rise in Wages, and Global Trade Rebalancing.

**Visual file limitation:** These course illustrations and chart were inspectable in the SCORM's **Enlarge image** view, but no image download control was exposed. The Chrome screenshot API only displayed captures without a workspace file path, and its local-data export alternative was blocked by browser URL policy. No substitute images were created; the labels and visible composition are recorded above.

**Media status:** This scenario screen contains the two interactive agent tabs and the three illustrations described above. It displays source links but no playable media or transcript/captions.


### Screen 3 — Isolated agents and brittle integrations

The next Acme screen states that the two agents were built separately, each to solve its own problem. Because the teams did not coordinate, neither agent knows the other exists or what it knows. Connecting either assistant to another system required custom code that reached directly into the warehouse database; the course says this would inevitably break when the database schema changes. Every additional system Acme wants to connect adds another one-off integration that must be built and maintained by hand. No key instructional visual, quiz, or media controls appear on this screen.

### Screen 4 — Production readiness and the stockout handled two ways

The screen asks why the earlier problems did not appear before. It says a system that works in a demo is different from one Acme can run through a holiday sales spike, submit to security review, and keep running after its builder moves to another project. Moving from a working demo to something that runs safely in production is described as the “harder half” of the problem. The screen then introduces the same stockout handled in two ways: one system learns about it on a timer, while the other learns about it as soon as it happens.

#### Visual description — “Impact of Event-Driven Operations in Retail”

The enlarged slide splits a shopping-cart scenario into **Non Real-Time** and **Real-Time** paths, with green arrows leading to four outcome cards per path. The non-real-time row pairs stale or delayed updates with lost sales, product no longer available to sell, a frustrated customer who makes no sale, and a disconnected customer experience: shelf replenishment waits until inventory is low; a replenishment order is sent to the warehouse only at night; Jane drives to a store after the web inventory was not updated and finds an empty shelf; and Frank cannot see accumulated loyalty points in his app until the next day or later. The real-time row pairs replenishment before shelf inventory gets low with increased sales; stockroom changes communicated as they happen with always having product to sell; website inventory updated in real time so Jane sees actual stock with improved customer experience and increased sales; and Jane and Frank's loyalty points updated immediately after a sale and visible in their app with an engaging customer experience. The drawings include a shopping cart, sold-out signs, a staff/stockroom scene, a phone being tapped, and a loyalty card with a star.

**Visual file limitation:** I inspected the original enlarged slide and found image references in the SCORM frame, but the supported attempt to retrieve a source image timed out. The browser screenshot-save path is blocked by its export policy, so no faithful screenshot or original file could be placed in this lesson's `img/` folder. The slide title, labels, scenarios, outcomes, and illustrations are described above.

#### Scenario · Dave (personal reflection)

The complete question shown is: **“Have you every encountered any of these while working with AI?”** The on-screen selection instruction is **“Select from the items below.”** It presents four unchecked checkboxes:

- “A system that didn't know about another system.”
- “An integration that broke when something upstream changed.”
- “An AI tool that confidently gave a wrong answer.”
- “A demo that never made it to production.”

This asks for the learner's personal experience. I left all boxes unchecked and did not submit a personal answer. The screen exposes no Submit control, scoring, correct-answer indicator, or additional feedback state for this reflection. The explanation already shown on the screen says that silos, brittle wiring, hallucinations, and demos not ready for production are different symptoms of the same cause: agents added in isolation without a shared way to see what is happening across the business right now. No confirmed correct personal response is provided.

#### Optional video — introductory AI fundamentals

The screen offers an optional primer titled **“Introductory Guide to AI Fundamentals: LLMs, RAG & Agentic AI Explained.”** The Academy screen estimates about 15 minutes; the embedded player showed about 18 minutes 43 seconds, and the exported English auto-generated captions run from **[0:00]** through **[18:40]**. The complete transcript is preserved in [primer-transcript.txt](primer-transcript.txt).

The video introduces large language models as systems that understand and generate human language, then describes them as sequence-prediction systems. It uses a layered neural-network analogy and explains transformer context, tokens, and vector embeddings, including semantic proximity and the risk that embeddings can reflect human biases. It then presents retrieval-augmented generation (RAG) as a way to supply external context to an LLM: a user query is routed through a service that retrieves relevant information from a vector database, passes that context with the query to the model, and post-processes a response. The presenter lists fresher answers, easier data updates than retraining, source transparency, and lower hallucination likelihood as benefits, and describes retrieval, cross-checking sources, precise querying, and post-generation checks as ways RAG can help. Research, financial workflows, customer support, semantic search, and vector databases are examples. The final portion introduces agentic AI as minimally supervised systems of specialized agents; it names instructions, a model, and tools as common agent parts and describes a mesh with gateways feeding an orchestrator that selects agents, illustrated by a Slack question about Jira routed to a Jira agent.

The transcript is a YouTube export of **English auto-generated captions**. It is complete from the recorded opening to the recorded ending, and is linked as a separate text file to avoid duplicating 503 timestamped caption lines in this README. The direct YouTube transcript panel had remained in a loading state; the browser's transcript export nevertheless returned the caption file. No other video captions or downloadable slide deck were exposed in the Academy screen.

### Section 02, screen 1 — Why a Lifecycle, Not Just a Framework

The SCORM sidebar has advanced to **Lesson 02 — Why a Lifecycle, Not Just a Framework**, described as five problems that stall agentic AI projects and the Agent Development Lifecycle (ADLC) as the structure that answers them. The section estimates about 10 minutes and lists two activities. The course progress meter reads 20%, with about 45 minutes remaining.

Acme's developer Dave spends a weekend connecting the website assistant directly to the warehouse database. By Monday it works, and his manager asks when it can go live for every store. Under **Where the demo stalls**, the screen says the build has no way to test what happens when the warehouse database is slow, no record of what it did if a customer complains about an incorrect answer next month, and nobody except Dave who understands how it is wired together. Those gaps did not matter for a demo but matter when real customers depend on it. The course introduces five recurring AI-project challenges and says Acme already faces them.

The five collapsed challenge controls are titled **1. The gap between a demo and production**, **2. No standard way any of this gets built**, **3. A cost problem**, **4. Lock-in and sprawl**, and **5. No safe way to give an agent real-time data access**. Below them the screen says they appear to be five separate problems but are actually one: Acme never agreed on a standard way to build an agent, so each team solves all five from scratch in isolation. The details behind the five controls and five unlabeled hotspot buttons are recorded below after inspection.

An embedded two-step card began at **Step 1 of 2**, headed **“Software engineering hit the same wall decades ago.”** It says software is now built, tested, deployed, and watched once live through a defined Software Development Lifecycle (SDLC). After the first step was recorded and the quiz submitted, I opened step 2; its content is recorded below.

The next explanation says agentic AI is at the same point. The **Agent Development Lifecycle (ADLC)** fills that gap; it is not a way to write an agent's logic, but the structure around it. The screen says to develop, test, deploy, observe, and improve agents the same way each time, so quality and governance do not depend on which team built a particular agent. An **Enlarge image** control appears beside this explanation; its visual has not yet been inspected.

The **What does Dave need to consider?** tab set is initially on **Cost**. It asks what each question costs and whether the number stays predictable as use grows. Without fast access to the right context, agents may compensate with more retries, longer reasoning chains, and extra calls to fill knowledge gaps. The text says this makes production costs unpredictable; a cost review should check both current cost per question and whether that remains stable as usage grows. The other tabs, **Governance**, **Security**, and **Repeatability**, have not yet been opened.

The screen says the checklist is what the ADLC is for: test something before it ships, get the right approval before it goes live, watch it once running, and feed what is learned into the next build. It says if Dave had asked these questions before his weekend build, the conversation with his manager would have gone differently.

#### Knowledge check — one question, unlimited attempts

**Question:** “A different Acme team builds an agent in an afternoon. It works in testing, but three months later nobody remembers why it makes certain decisions, and there's no record of who approved it going live. Which of the five root problems does this demonstrate?”

**Selection instruction:** The screen says **“Answer at least one question to check your answers.”** The **Check answers** button is locked until an option is selected. Four radio choices are shown:

- “The gap between a working demo and something that runs in production”
- “A cost problem”
- “Lock-in and sprawl”
- “No safe way to give an agent real-time data access”

Before submission, no response was selected and the Check answers button was locked. The submitted response and feedback are recorded below.

**Submitted answer:** I selected **“The gap between a working demo and something that runs in production”** and pressed **Check answers**. The Academy marked it **CORRECT** and returned: **“Right. Building it was the easy afternoon; operating it, explaining it, and having a record of who approved it is the job nobody was assigned.”** This confirms the selected answer as correct; there were no incorrect attempts.

The visible recap says the section has covered five root problems in unmanaged agent development (demo-to-production gap, no standard process, unpredictable cost, lock-in and sprawl, and unsafe data access); introduced the ADLC by comparing it with the change software engineering and API management already went through; and walked through the four things to decide before building an agent: cost, governance, security, and repeatability.

#### Expanded challenge explanations

- **1. The gap between a demo and production:** Dave can build something in a weekend, but operating it, fixing it when it breaks, and improving it over months is an entirely different job.
- **2. No standard way any of this gets built:** The website team built its assistant one way. If store operations uses different tools, tests, and error handling, Acme cannot ensure both agents meet the same standard.
- **3. A cost problem:** Each question costs money in model calls. If an agent cannot get fast, current Acme data, it guesses and spends more tokens working around missing context instead of receiving the right answer directly.
- **4. Lock-in and sprawl:** Dave's agent is wired to one model provider, so switching later requires rewiring. Other teams are independently adding agents without tracking how many exist or what they can access.
- **5. No safe way to give an agent real-time data access:** The warehouse database also contains supplier costs and pending purchase orders. A direct connection lets the assistant see everything in that database, whether or not its job requires it.

#### Five expanded challenge callouts

The interactive graphic presents five markers. The accessibility view labels each panel heading as **“4”** and does not expose a distinct heading; the visible panel text is captured here in marker order.

1. **Marker 1 of 5:** “Agents don’t have easy access to the real-time data they need to make good decisions. They often rely on outdated, batch-processed information or need custom code just to get data from one system to another. This creates blind spots, slow reactions, and poor outcomes (especially when decisions depend on fast-changing conditions).”
2. **Marker 2 of 5:** “In modern enterprises, most agents are currently being built in silos. One team might spin up a chatbot, another creates a document summarizer, and a third integrates with an internal system. But these agents don’t coordinate or share knowledge. Without a common way to manage or connect them, you end up with a fragmented mess of isolated tools rather than a smart, collaborative ecosystem.” The panel continues: “Scaling is another issue. Performance becomes unpredictable as more agents get added or more users come online. It's hard to pinpoint bottlenecks, and even harder to make the system resilient without overengineering everything.”
3. **Marker 3 of 5:** “An agent doesn't always answer instantly, and neither does a person waiting at a human-in-the-loop step. That's fine in a chat window, but it becomes a real design problem when response time affects something time-sensitive like a checkout flow, a support queue, or a process a customer is waiting on. Systems built assuming an instant, synchronous answer handle this poorly.”
4. **Marker 4 of 5:** “Model providers ship upgrades every few months, so committing to one today risks looking outdated within a year. That leaves most teams stuck between two bad options:” **“Commit early and risk locking into a choice that ages quickly”** or **“Wait and risk falling behind competitors already experimenting.”** It concludes: **“Neither one is actually a strategy.”**
5. **Marker 5 of 5:** “Finally, there’s production challenges. Running AI agents in a live environment (where you need to add, remove, or update them without downtime) is a massive operational headache. Add in strict requirements for security, governance, and compliance, and the complexity multiplies fast.”

#### Checklist tabs

- **Cost** asks: “What does this cost per question? Does that number stay predictable as more people use it?” Without fast access to the right context, agents use more retries, longer reasoning chains, and extra calls to fill gaps. A review checks today's per-question cost and whether it stays stable or climbs as usage grows.
- **Governance** asks: “Who can see what this agent is doing, and who signs off before it goes live?” Without that, decisions happen with no one watching and there is no record of who approved them or why. Governance should make both questions answerable on demand.
- **Security** asks: “If the tool this agent calls is wrong, or compromised, what else can it reach?” Tools inherit the access granted when configured, and the course says that access is rarely revisited once things work. Security checks whether an agent has access beyond what its job requires; a tool scoped too broadly can make one bad call much worse.
- **Repeatability** asks: “If a different team builds a new agent, does it hold up to the same standards as yours? Or does every agent start from scratch?” Without a shared standard, teams reinvent testing, error handling, and deployment, and quality depends on who built the agent. Repeatability lets the next agent start from something instead of starting over.

#### ADLC visual description

The enlarged diagram is a circular green arrow loop around a Solace “S” mark. It orders five labeled stages clockwise: **Develop → Test → Deploy → Observe → Improve → Develop**. Gear, clipboard, deployment/network, magnifying-glass, and rising-chart icons sit at the corresponding stage points. No words beyond the five stage names appear inside the graphic.

**Visual file limitation:** I inspected the original enlarged diagram. The supported attempt to retrieve a source image timed out, and the browser screenshot-save route is blocked by its export policy. No image file could be placed under `img/`; the cycle and its labels are described above.

**Step 2 of 2 — “Then companies went through the same shift again with APIs”** says that once companies had dozens or hundreds of APIs, they needed a standard way to design, secure, and monitor them; otherwise API sprawl becomes its own problem. The embedded card shows **Back** and **Next step** controls after this text. Pressing **Next step** on step 2 cycles the card back to step 1; it does not advance the SCORM section.

### Section 03, screen 1 — Stages of the Agent Development Lifecycle

The SCORM sidebar has advanced to **Lesson 03 — The Agent Development Lifecycle**, described as six ADLC stages framed as hiring and managing a new employee and applied end to end to Acme's Inventory agent. The section estimates about 7 minutes; the course progress meter reads 30% with about 40 minutes remaining.

The opening asks what must happen before an agent is trustworthy enough to run without supervision. The screen says Solace frames the ADLC as six stages and invites learners to think of it as hiring and managing a new employee. The **Stages of the ADLC** stepper is initially at **Step 1 of 6 — Hiring**: define what the agent's role is before building anything; this means deciding what it will be used for, not choosing a model or prompts. A vague job description creates a vague agent, and if the job cannot be stated concretely in one sentence, including what the agent should and should not do, it is not ready to build. The stepper controls are **Back** and **Next step**.

**Step 2 of 6 — Onboarding:** The screen compares onboarding to a new employee needing a badge, laptop, and access to the systems the job actually uses. For an agent, this means connecting the right data sources so it can retrieve current data when needed instead of relying only on what the model already knows, which the course relates to retrieval-augmented generation. It also means giving the agent the right security scope: read access to what its job requires and nothing else. The screen warns that giving an agent access to everything means it can see too much while still knowing too little about what matters.

**Step 3 of 6 — Coaching:** Before entrusting an agent with important work, run it against realistic scenarios, including edge cases, unusual inputs, and situations that do not happen every day, before it speaks to a real customer. If it handles them badly, it should fail during testing rather than in front of someone relying on the answer. A rare situation that does not belong in an agent's everyday instructions can be packaged as a **skill**: reference material loaded only when that situation comes up.

**Step 4 of 6 — Supervision:** Supervision means knowing where the stakes are high enough to pause for a check, rather than watching every move and decision. Routine decisions can proceed automatically; an action that could cause a serious mistake if wrong should wait for a person to confirm. The course names two mechanisms: **Role-Based Access Control (RBAC)** determines who may approve which actions, and **tracing** records what actually happened.

**Step 5 of 6 — Teamwork:** This stage is about how a new hire fits into everyone else's work, not only the person's own job description. Agents rarely operate alone for long. Coordinating with other agents, handing work off, and staying out of each other's way is its own discipline.

**Step 6 of 6 — Improvement:** Improvement means collecting feedback and making the agent better by seeing what it got right, what it got wrong, and where a person had to intervene and correct it. The records and artifacts an agent leaves after each decision are what make the next version better rather than merely different.

After visiting step 6, **Next step** cycled the interactive card back to **Step 1 of 6 — Hiring**; the loop does not advance to another SCORM screen. All six stages had been opened and recorded before leaving this section.

The screen warns: **“Skipping ahead and just building agents will break something at each stage.”** It provides these stage reminders: Hiring without a clear job produces an agent that does the wrong things well; Onboarding without the right scope lets it see more than it should; Coaching without testing means its first hard case is a real customer; Supervision without checkpoints lets a bad decision ship before anyone notices; Teamwork without coordination means agents step on each other once there is more than one; Improvement without a feedback loop means the agent in a year is no better than the one shipped on day one.

#### Acme Inventory agent example

Dave's Inventory agent watches stock across the warehouse and all **41 stores** and flags reorders before stock reaches zero. The example table gives one concrete action for each stage:

| Stage | What Dave actually did |
|---|---|
| Hiring | Before anything else, he wrote: “Watch stock across the warehouse and all forty-one stores, flag a reorder the moment any product crosses its threshold, and do nothing else.” |
| Onboarding | Connected it to the warehouse database and store counts with read access to inventory and nothing else, not supplier contracts or payroll. |
| Coaching | Tested against a supplier delay, a sudden order spike, and a store that overreports its shelf count before touching production data. |
| Supervision | Set the threshold between a routine **40-unit** reorder and a **4,000-unit** reorder that must be confirmed by a person first. |
| Teamwork | Ensured the agent's reorder flag actually reaches the agent handling supplier orders. |
| Improvement | Made it possible for Dave to look back in three months and see exactly where its recommendations needed correction. |

#### Match each action to an ADLC stage

The on-screen instruction is **“Match the action to the stage.”** Six prompts each have a dropdown initially set to **“— Select —”**. Every dropdown shows the same six choices: **Hiring**, **Onboarding**, **Coaching**, **Supervision**, **Teamwork**, and **Improvement**. The exact prompts are:

- “Deciding the Inventory agent should only watch stock levels, not process refunds”
- “Reviewing three months of the agent's reorder decisions to see where it needed correcting”
- “Making sure the Inventory agent's reorder flag reaches the supplier-order agent”
- “Giving the agent read access to the warehouse database but not supplier contracts”
- “Running the agent against a simulated supplier delay before it goes live”
- “Pausing a 4,000-unit reorder for a person to confirm”

The screen says **“Place at least one item to check your answers.”** The **Check answers** button is locked until a response is selected. Before submission, all six answers were blank; the submitted matches and feedback are recorded below.

**Submitted matches:** Inventory scope only / not process refunds → **Hiring**; reviewing three months of decisions → **Improvement**; routing the reorder flag to the supplier-order agent → **Teamwork**; read access to inventory but not supplier contracts → **Onboarding**; simulated supplier-delay test → **Coaching**; pausing a 4,000-unit reorder for human confirmation → **Supervision**. I submitted all six together. The Academy reported **“6 of 6 correct.”** All six selections were confirmed correct; the system displayed no additional per-match explanation, and there were no incorrect attempts.

The visible recap says the lesson covers Hiring, Onboarding, Coaching, Supervision, Teamwork, and Improvement as the general ADLC model, then applies all six to Acme's Inventory agent. The opening's **Enlarge image** control was inspected and is described below.

#### ADLC stages visual description

The enlarged graphic draws the six stages as a loop of thick green arrows: Hiring → Onboarding → Coaching across the top, then down to Improvement → Teamwork → Supervision across the bottom and back up to Hiring. It captions Hiring **“Define role, responsibilities, expectations,”** Onboarding **“Give access to systems & tools,”** Coaching **“Internal education to improve competence,”** Supervision **“Close oversight to ensure accuracy,”** Teamwork **“Get them working together as a team,”** and Improvement **“Monitor performance and provide feedback.”** Small thumbnails illustrate an agent role/configuration, connected databases and APIs, test or evaluation results, human oversight, a workflow, and performance/feedback instrumentation. The labels and direction of flow are legible; the small thumbnail text is not readable enough to transcribe. No video or audio appears in this section.

**Visual file limitation:** I inspected the original enlarged diagram. The supported attempt to retrieve a source image timed out, and the browser screenshot-save route is blocked by its export policy. No image file could be placed under `img/`; the stages, arrows, labels, and thumbnail subjects are described above.

### Section 04, screen 1 — The Four Components

The SCORM sidebar has advanced to **Lesson 04 — Componentization: What's Actually Running** and the internal page **The Four Components**. It describes Agents, Tools, Entrypoints, and the event broker, then assembles them against Acme's Inventory agent. The page estimates about 4 minutes and lists one activity. The course progress meter reads 40% with about 35 minutes remaining. The screen says a running Agent Mesh comes down to four things.

The component tabs begin on **Agents**. The screen calls agents the workers: each has a model, instructions, and tools it is allowed to call, and is built for one specific job rather than everything. When one agent needs another, it does not call it directly like one function calling another; it sends a message over the **A2A protocol**, which the screen calls the open standard any agent on the mesh uses to talk to any other, regardless of who built it or what it is for. The other component tabs were opened and recorded below.

In the Acme mapping, the Inventory agent watches stock and reorders items when stock runs low; the rendered screen's accessibility text then runs into **“A call to the supplier ordering system”** without a separating space. Tools include a query against the stock database and a call to the supplier ordering system. Entrypoints include chat from a store manager, employee, or customer; events arriving directly from the broker; and a webhook or REST call from another system. The event broker carries every message to a tool or another agent over the same broker Acme already runs.

The **Event Broker** tab says it ties everything together: every message between every piece—an agent calling a tool, an entrypoint handing off a request, or one agent notifying another—travels over the broker. This makes the whole flow traceable end to end and lets a new agent be added later without redesigning how existing agents communicate. The enlarged Event Broker visual is an abstract dark-blue/teal network mesh: many application and service icons appear as nodes around a central Solace event-mesh hub, connected by multiple paths; the small node labels are not legible.

The **Vocabulary Check** instruction is **“Tap a card to turn it over.”** I turned over all four cards. **Entrypoint** reveals “A store manager asks a question in a chat window”; **Event Broker** reveals “Carries the message from the Inventory agent to the supplier-order agent”; **Agent** reveals “Has a model, instructions, and a job: watch stock, flag reorders”; and **Tools** reveals “Checks the stock database and calls the supplier ordering system.” These are definition cards rather than a scored quiz: the page showed no selection prompt, submit control, score, or correctness feedback. All four cards remained face-up when I finished. The overall four-component model and component visuals were inspected and described below before advancing.

#### Tools tab and visual

**Tools** are described as how an agent reaches the outside world: a database query, API call, or whatever its job requires. Connections are typically configured as connectors to specific systems, built once and reused by any agent that needs them rather than custom-wired into one agent. Some use **MCP**, an open standard for reaching a tool or data source without tying the connection to one vendor's approach. Tools run sandboxed so a buggy or compromised tool cannot reach beyond its allowed scope. Related tools can be grouped into a reusable **toolset** and managed as one unit.

The enlarged Tools diagram shows four **User** nodes on the left feeding an **OrchestratorAgent**. On the right, the orchestrator connects to two **LLM** nodes and a **Tool: extract_content_from_artifact** node. A vertical connection leads from the orchestrator to a **MarkitdownAgent**, which then connects to another **MarkitdownAgent** node below. The slide is a dark node-and-connector canvas; no other explanatory labels are visible.

**Visual file limitation:** I inspected the original enlarged diagram. The supported source-image retrieval attempt timed out and the browser screenshot-save route is blocked by its export policy. No original or screenshot file could be saved under `img/`; the nodes and connections are described above.

#### Entrypoints tab and visual

**Entrypoints** are the different ways to communicate with the mesh. The screen gives a person typing a question in chat as one example; understanding what they typed without requiring rigid command syntax is natural language processing. A message arriving in a team's Slack channel is another entrypoint. A broker event arriving without anyone typing is a third. The screen summarizes these as the same agent underneath, with different ways in.

The enlarged slide is titled **“Solace's Event-Driven Approach to Integration and AI.”** Its left column says: **“Liberate your data from source systems and devices”; “Stream & Filter it to target systems, anywhere they exist”; “React & Integrate it with target systems, anywhere they exist”;** and **“Democratize it by providing self-service discovery, access and governance.”** The central network mesh spans AWS, Azure, Alibaba Cloud, Google Cloud, and Kubernetes. Salesforce feeds the network at the “Liberate” side; “Stream & Filter” is centered; the “React” side points to SAP, ServiceNow, and Workday; and an Agentic AI node branches to AI/service, data, and agent icons. At the bottom, “Democratize” is bracketed over Architects, Developers, and Stakeholders.

**Visual file limitation:** I inspected the original enlarged slide. The supported source-image retrieval attempt timed out and the browser screenshot-save route is blocked by its export policy. No original or screenshot file could be saved under `img/`; the text and network relationships are described above.

#### Event Broker visual

The enlarged Event Broker image is an abstract event-mesh illustration on a dark blue and teal field. A central Solace mesh or hub connects a range of application, service, and system icons around it through multiple intersecting paths. The image illustrates the broker's role carrying messages across the mesh; individual small icon labels are not legible.

**Visual file limitation:** I inspected the original enlarged image, but its nodes have no readable labels. The supported source-image retrieval attempt timed out and the browser screenshot-save route is blocked by its export policy, so no original or screenshot file could be saved under `img/`.

The visible recap says the page covered the four-part component model, assembled the components against Acme's Inventory agent, and named A2A as the protocol agents use to talk to one another alongside the available ways to enter the mesh.

#### Overall Agent Mesh visual description

The enlarged **Solace Agent Mesh** architecture diagram shows application interfaces and enterprise data sources entering a green platform. Its **Gateway** is labeled “Secure, Session Management,” and **Connectors** provide “Data Access, Real-Time Context.” Inside the platform, an **Orchestrator** is “Dynamic, Flexible”; **Visualizer** is “Observable, Explainable”; **Data Management** lists “Speed, Accuracy, LLM Token Costs”; **Toolsets** list data analysis/visualization and artifact management; **Agent Builder** is no-code; **Agent Coding** is pro-code; **Deployer** supports Kubernetes in cloud or self-managed form; and **Event Mesh** is “Scalable, Resilient.” The lower platform area contains **Agent Proxies**, **Native Agents**, and **AI Service**. Outside the platform, **Agent2Agent** connects to third-party agents with examples Amazon AgentCore, LangChain, Microsoft AutoGen, Salesforce Agentforce, and Google ADK. Model integrations are labeled **“Over 100 LLMs including”** Anthropic, Bedrock, Gemini, Groq, Mistral AI, OpenAI, OCI, and Vertex AI. On the left are Native Web UI, Slack, Microsoft Teams, REST/API, and SQL symbols; on the right are user roles Admins, Business Users, Developers, and DevOps.

**Visual file limitation:** I inspected the original enlarged diagram. The supported source-image retrieval attempt timed out and the browser screenshot-save route is blocked by its export policy. No original or screenshot file could be saved under `img/`; the architecture and all legible labels are described above.

#### Agents visual description

The Agents tab's enlarged slide is titled **“What is an AI Agent?”** It defines an agent as **“a software system that perceives, reasons, and acts autonomously”** and calls it the digital equivalent of a skilled human worker at machine speed and enterprise scale. It compares a human **Co-Worker** (specialized knowledge, tools, judgment) with an **AI Agent** (autonomous software worker with LLM reasoning and digital tools) as the **same role in a new medium**. Four paired cards relate **Brain = LLM** (core reasoning engine; examples GPT-4o, Claude 3, Gemini 1.5), **Specialized Skills = Agent Skills** (configured or fine-tuned domain capabilities such as customer support or code review), **Tools = Agent Tools** (APIs and functions for actions such as web search, email, SQL), and **Data = Agent Connectors** (live enterprise sources such as Salesforce, SAP, Kafka).

**Visual file limitation:** I inspected the original enlarged slide. The supported source-image retrieval attempt timed out and the browser screenshot-save route is blocked by its export policy. No original or screenshot file could be saved under `img/`; the definition and the four paired cards are described above.

### Section 04, screen 2 — Why Openness Matters

The SCORM sidebar has advanced to **Lesson 05 — Componentization: What's Actually Running**, internal page **Why Openness Matters**. Its summary says the page explains why an agent is not tied to one model or cloud, and how A2A and MCP address lock-in. It estimates about 4 minutes and lists one activity; the course meter reads 50% with about 30 minutes remaining.

The opening asks, **“What happens the day your model provider changes its pricing, or a cheaper, better option ships?”** It says systems not designed for this face a rewrite: an agent hardcoded to one model must be rebuilt to use another, and the associated code, prompts, and integrations usually have to be rebuilt too.

Under **“Openness is the fix,”** the page gives two design choices. First, an agent is not hardcoded to one model; it calls the model configured for that job through the mesh's AI service layer, rather than through code inside the agent. Second, changing providers is a configuration change, not a rewrite. The same applies to where the system runs: because nothing assumes a particular cloud, it can move between self-hosted infrastructure and cloud providers without redesigning the agents.

The **Compare and contrast** table has three columns: scenario, **Hardcoded to one provider**, and **Open by design**. Its rows are: **Switching models** — “Rewrite the agent” vs. “Change a configuration value”; **Moving clouds** — “Redesign around the new platform” vs. “Nothing in the agent assumes a cloud”; **Reaching a new tool** — “Custom integration per system” vs. “MCP, the same way every time”; and **An agent built elsewhere** — “Throw it out and rebuild” vs. “If it speaks A2A, it can join. (E.g. LangGraph, custom frameworks, anything).” No answer selection or graded quiz is present on this screen; its one listed activity is this comparison content. The visible advancing control is **Continue**.

#### Openness visual description

The enlarged slide is titled **“How Agent Mesh is Different.”** It presents three green circles with headings and bullets:

- **Easy to Experiment & Build:** Pro-code and No-code Agent Builder; pre-built and extensible Gateways, Connectors, Toolsets; dynamic agent discovery and orchestration.
- **Ready for Production:** Resilient, scalable, unmatched real-time responsiveness due to event-driven architecture; enterprise-grade security, observability, and trust; intelligent data management—faster, cheaper, more accurate.
- **Open & Vendor Neutral:** Available open-source Community edition; support for A2A and MCP protocols for broad support of agents, data sources, and tools; deployment into any cloud via Kubernetes, any LLM.

The slide footer reads **“© Solace | Proprietary & Confidential”** and shows page number 24. **Visual file limitation:** I inspected the enlarged slide, but could not save an original or screenshot under `img/`: the supported source-image retrieval attempt timed out and browser screenshot saving is blocked by its export policy. The visible title, headings, and bullets are transcribed above.

### Section 04, screen 3 — A2A and MCP working together

The next SCORM screen explains that **A2A** is an open standard that lets agents on the same mesh communicate. An agent built elsewhere by another team on another platform can join the same conversation if it speaks that protocol; agents built on a completely different framework, such as **LangGraph**, can join the mesh seamlessly. **MCP** is described as the standard way for an agent to reach a tool or data source without making that connection specific to one vendor's approach.

The screen's central statement is: **“None of this is about avoiding commitment; it's about not paying twice: once to build something, and again to rebuild it the moment a model, a cloud, or a tool needs to change.”** The **old way** says Dave's original weekend build was wired directly to one model provider, so switching later would have meant rewriting it from scratch. The **new way** says a different Acme team can build an agent on a completely different platform and join the same mesh as Dave's Inventory agent instead of throwing it out and rebuilding it. The page concludes, **“This is exactly what closes Acme's lock-in problem.”**

The **Quiz Time!** panel is labeled **“KNOWLEDGE CHECK · 1 QUESTION UNLIMITED ATTEMPTS.”** The full question is: **“Acme's supplier-relations team built an agent on a completely different platform last year. Which of the following is true if that agent speaks the A2A protocol?”** The four choices are:

1. “It can join the same mesh as Dave's Inventory agent without being rebuilt.”
2. “It has to be rebuilt on Agent Mesh before other agents can reach it.”
3. “It can be reached, but only through a custom one-off integration.”
4. “It can't participate, because it uses a different model provider.”

The selection instruction is **“Answer at least one question to check your answers.”** Before answering, all four radio buttons were unselected and **Check answers** was disabled/locked. The submitted selection and Academy feedback are recorded below.

The visible recap says the screen covered why an agent need not be tied to one model or cloud and what that prevents; connected A2A and MCP to the earlier lock-in and sprawl problem; and showed that an agent built outside Acme's mesh can join if it speaks the same open protocols. The enlarged visual is a dark brown/black abstract background with dim geometric shapes and a centered MCP logo and label, **“MCP (Model Context Protocol).”** No further legible copy is in the image.

**Visual file limitation:** I inspected the original enlarged MCP image. The supported source-image retrieval attempt timed out and browser screenshot saving is blocked by its export policy, so an original or screenshot could not be saved under `img/`; the visible logo and text are described above.

**Submitted answer and feedback:** I selected **“It can join the same mesh as Dave's Inventory agent without being rebuilt.”** The Academy marked it **CORRECT** and returned: **“Exactly. A2A being an open standard is the whole point: speaking the protocol is the only requirement for joining the conversation.”** The other three choices were confirmed unselected/disabled after submission. The page exposed **Try again**, but no retry was needed.



### Section 05, screen 1 — Orchestrator vs. Workflow

The SCORM sidebar has advanced to **Lesson 06 — Coordinating Multiple Agents: Orchestrator vs. Workflows**, internal page **Orchestrator vs. Workflow**. The description says it explains what the Orchestrator does and the alternative for a process that must run the same way every time. The page estimates about 5 minutes and lists one activity; course progress is 60% with about 25 minutes remaining.

The opening says Dave encounters orchestration and workflows while building out Agent Mesh and asks what they do and how to choose between them. The stepper is at **Step 1 of 2 — The Orchestrator**. It defines the Orchestrator as an LLM-backed coordinator model doing the reasoning underneath, the same kind of model each agent uses for its own job. Given a task, it decides at runtime which agents to call, in what order, and how to combine their results. It fits open-ended requests such as **“summarize this”** or **“draft a reply to this customer”** and adapts to ambiguity. The tradeoff is that it is not guaranteed to take the same path twice because an LLM samples from a distribution rather than running a fixed function. The page calls that acceptable for a low-stakes question but not ideal when a process must run identically every time. The stepper controls are **Back** and **Next step**; I recorded step 1 before opening step 2.

The orchestration illustration's caption reads: **“A coordinator deciding at runtime which workers to call, in what order, and how to combine what comes back.”** Its enlarged balance-scale visual compares two columns. **Orchestrator:** LLM-Decided Control Flow; Non-Deterministic Repeatability; Emergent Visibility; Difficult Auditability; LLM-Managed Error Handling. **Workflow:** YAML-Defined Control Flow; Deterministic Repeatability; Explicit Visibility; Full Auditability; Configurable Error Handling. The scale visually balances the two approaches.

#### Linked demo video

The page links **“Orchestration vs Workflows Demo”** to a Vidyard video titled **“Workflows Demo; What and Why - Solace Agent Mesh”**, with a displayed duration of **2:43**. The player settings exposed Quality and Speed only; there was no captions control or transcript link, and no transcript was available from the course page or video page. I observed a presenter on camera, but the player did not expose readable captions or transcript text. I therefore have not inferred additional spoken claims from the video; the orchestration concepts and examples above come from the visible lesson text, table, and illustration.

The **So which one should Dave use?** comparison table contrasts **Orchestrator** with **Workflow**:

| Dimension | Orchestrator | Workflow |
|---|---|---|
| Decides the path | At runtime, by an LLM | Ahead of time, by you |
| Same input, same path? | Not guaranteed | Every time |
| Best for | Open-ended, ambiguous requests | Processes that must be exact |
| Failure handling | Reasoned about in the moment | Defined as part of the graph |

The screen clarifies that agents inside a workflow are still fully capable AI agents; a workflow constrains the control flow around them, not their intelligence.

The **Test your understanding!** panel is labeled **“KNOWLEDGE CHECK · 3 QUESTIONS UNLIMITED ATTEMPTS.”** Each item has two choices. The exact questions and choices are:

1. **“A store manager types: ‘summarize what happened with the Denver boot situation last week.’ Orchestrator call, or Workflow?”** Choices: **Orchestrator**; **Workflow**.
2. **“Every incoming order must be validated, checked against stock, priced, and then either confirmed or sent for review, identically, every single time. Orchestrator call, or Workflow?”** Choices: **Orchestrator**; **Workflow**.
3. **“Choosing a workflow means the agents inside it are less capable than agents the Orchestrator calls.”** Choices: **True**; **False**.

The instruction is **“Answer at least one question to check your answers.”** Before submitting, all six radio buttons were unselected and **Check answers** was disabled/locked. The submitted answers and Academy feedback are recorded below.

Under **“One more thing worth clarifying,”** the page says the Orchestrator and Workflows are not competing options; they work together. The Orchestrator can hand a task to a Workflow after recognizing that the request matches one, handling the ambiguous front end—understanding what a person is asking—while the workflow handles the part that must be exact. The recap says the page covered the Orchestrator vs. Workflow distinction and when each is the right call.

**Visual file limitation:** I inspected the enlarged comparison illustration, but the supported source-image retrieval attempt timed out and browser screenshot saving is blocked by its export policy. No original or screenshot could be saved under `img/`; the legible labels and visual balance are described above.

**Stepper, Step 2 of 2 — Workflows:** A workflow is an explicit execution graph: the builder defines every step, the order they run, and what happens if something fails. There is no inference or interpretation at runtime; it follows the graph exactly as written. Agents inside a workflow remain fully capable AI agents; the workflow constrains control flow, not their intelligence. After I pressed **Next step** from step 2, the card returned to **Step 1 of 2 — The Orchestrator**; it loops and does not advance the SCORM page.

**Submitted answers and feedback:** I selected **Orchestrator** for question 1, **Workflow** for question 2, and **False** for question 3, then submitted the set together. The Academy marked all three **CORRECT** and returned these explanations: Q1, **“Right. It's open-ended, there's no single correct sequence of steps, and adapting to the ambiguity is the job.”** Q2, **“Correct. ‘Identically, every single time’ is the requirement an LLM-decided path can't promise.”** Q3, **“Right. A workflow constrains the control flow around the agents, not the agents themselves.”** The submitted radio values were confirmed after submission. **Try again** was available but unnecessary.

### Section 05, screen 2 — Patterns and What's Underneath Them

The SCORM sidebar is at **Lesson 07 — Coordinating Multiple Agents: Orchestrator vs. Workflows**, internal page **Patterns and What's Underneath Them**. Its description says it presents five coordination patterns against an Acme order-fulfillment example and the mechanism behind each. The page estimates about 5 minutes, lists one activity, and shows course progress at 70% with about 20 minutes remaining.

Under **“Here's what happens once the Inventory agent flags a reorder,”** the page says the recommendation does not go straight to the supplier; it must pass three checks: **Confirm the reorder is legitimate**; **Check the supplier's current terms and pricing**; **Either approve it automatically or send it to a human for review**. A callout says this sequence covers each of the orchestration patterns Dave needs to recognize.

The **Orchestration Patterns** card starts at **Step 1 of 5 — Sequential**. Some steps cannot start until an earlier one finishes. In Dave's reorder-approval process, confirming the reorder is legitimate must finish first because the downstream supplier-terms and pricing checks depend on knowing the reorder is real. Underneath, one step declares that it depends on the preceding step. The card has **Back** and **Next step** controls. This step was recorded before advancing to step 2.

The section **“In a workflow, what do we call each of these steps?”** explains that a workflow is built from a small set of node types; every pattern is one or more of these wired together. A node is the smallest executable step in the graph. Some nodes call agents, some make routing decisions, and others control how many times or in how many ways a step runs. The enlarged table reads:

| Node | What does it do |
|---|---|
| Agent | Calls a named agent, passes input, captures output |
| Switch | Evaluates conditions top-to-bottom, routes to the first match |
| Map | Runs a node once per item in an array, parallel by default |
| Loop | Repeats a node until a condition is false |
| Workflow | Calls another workflow as a sub-step |

The separate **Map** callout says it runs one step once for every item in a list, in parallel, and collects the results. Its example is checking stock across every Acme warehouse at once, one check per warehouse, instead of writing the loop by hand.

#### Return scenario knowledge check

The panel is headed **“Put your knowledge to the test!”** and **“SCENARIO · DAVE.”** Its scenario reads: **“A customer starts a return. Every return has to be logged, checked against the original order, inspected for eligibility, and then either auto-refunded or, above a threshold, routed to a person. Acme also wants each item in a multi-item return checked independently, all at once.”** The question is **“Which pattern is doing the work when a $900 return gets held for a human decision?”** The four visible checkbox choices are:

- **Conditional, then human-in-the-loop.**
- **Sequential, because the steps happen in order.**
- **Map, because each item is checked independently.**
- **Event-driven, because the return triggered it.**

No selection instruction or separate answer-submit button is visible in the initial screen state; all four boxes are unchecked. Clicking **“Conditional, then human-in-the-loop.”** immediately selected the checkbox and returned feedback, so the choice was submitted on selection.

**Submitted answer and feedback:** I selected **“Conditional, then human-in-the-loop.”** The Academy marked it **CORRECT** and said: **“Right on both halves. A Switch checks the value and routes to a different path, and the escalation itself is an ordinary step whose job is putting the decision in front of a person.”** The feedback offered **Try another answer**; no retry was needed.

The recap says the lesson walks through **sequential, parallel, conditional, event-driven, and human-in-the-loop** patterns; connects each pattern to its mechanism, including the **Switch** node for conditional logic and running one check across a list at once; and explains that an Orchestrator and a workflow can hand off to each other rather than being an either-or choice. No video or audio appears on this screen.

**Visual file limitation:** I inspected the original node-types image. The supported source-image retrieval attempt timed out and browser screenshot saving is blocked by its export policy. No original or screenshot could be saved under `img/`; the table text is transcribed above.

**Orchestration Patterns, Step 2 of 5 — Parallel:** Some steps are independent and do not need to wait in line. After the reorder is confirmed legitimate, checking current supplier terms and confirming pricing both depend on that confirmation but not on each other, so they can run at the same time. The underlying rule is the opposite of sequential: steps without a dependency between them run together automatically.

**Orchestration Patterns, Step 3 of 5 — Conditional:** Not every reorder follows the same path. An unusually large order, such as the **4,000-unit** case, requires a person's sign-off, so the workflow routes it differently from a routine reorder. The screen names the **Switch** node: it checks conditions in order and routes to the first match. This decision is worth writing down and testing instead of leaving it to an LLM's judgment in the moment.

**Orchestration Patterns, Step 4 of 5 — Event-driven:** A workflow need not wait for a person to open it and click a button. The reorder-approval process registers itself on the event broker like an agent. As soon as the Inventory agent publishes its reorder flag to the broker, the whole process starts automatically.

**Orchestration Patterns, Step 5 of 5 — Human-in-the-loop:** Not every decision should complete on its own. When the conditional check flags a reorder outside normal bounds, the workflow does not guess; it hands the decision to a person for approval instead of finishing automatically. After I pressed **Next step** from step 5, the card returned to **Step 1 of 5 — Sequential**; the stepper loops without advancing the SCORM page.

### Section 06, screen 1 — Agents Reacting, Not Polling

The SCORM sidebar has advanced to **Lesson 08 — Agents Reacting, Not Polling**. The description says it explains why polling, batch processing, and glue code add delay and revisits what Acme's stockout problem could have looked like. The page estimates about 6 minutes; the course shows 80% progress and about 15 minutes remaining.

The opening describes Acme Retail as noisy: website orders arrive, warehouse shipments are scanned in and out, and store stock shifts throughout every day. Revisiting the Denver boots that customers were told were in stock after they had sold out, the page says the boots did not disappear without a trace: the warehouse system logged the moment they sold out. The question is whether Dave's Inventory agent can hear about those events in time to matter.

Under **“Most systems reach that kind of data one of three ways,”** I opened all three tabs:

- **Polling:** An agent checks a database every few minutes and hopes nothing important happened in between, missing events that occur in the gaps.
- **Batch processing:** Data does not arrive until an overnight file loads. The screen names this as the specific reason Acme's website assistant kept telling customers the Denver boot was in stock long after it was not.
- **Custom glue code:** Someone directly wires two systems together; it works until one changes something and the integration quietly breaks.

The page concludes: **“All three share the same weakness. They add delay, which turns a real-time problem into a stale one.”** The visible advancing control is **Continue**. This screen has no quiz, video, audio, or enlarged visual.

### Section 06, screen 2 — So how should the Inventory Agent get its data instead?

After **Continue**, the page asks how the Inventory agent should get data instead. The event-driven sequence stepper is at **Step 1 of 5 — Stock crosses the threshold**: a customer buys one of the last pair of boots, causing stock for that boot to fall below Acme's reorder threshold. The card has **Back** and **Next step** controls. I recorded step 1 before opening the following step.

A callout says: **“The agent was already listening, and it acted without being asked. That's agentic AI in practice.”** The next section, **“But listening for events is only half the story,”** says an agent that reacts as soon as something happens but sees only the bare fact of the event may make a bad decision quickly instead of a good decision slowly. If it only knows that stock crossed the threshold, it might recommend reordering 40 units for a store about to close for renovations, or miss that the same product is overstocked two states away and could be shipped from there. **Real-time context** matters as much as the **real-time trigger**. The callout concludes: **“Reacting fast and reacting well are two different problems, and solving only the first one just means Acme finds out it made a bad call faster than it used to.”**

#### Snowstorm and context knowledge checks

The first **SCENARIO · DAVE** says: **“A snowstorm causes a spike in orders for winter boots at three Colorado stores over two hours.”** Under **“Consider this:”** it asks: **“Would a polling-based system, checking every 20 minutes, catch this in time to prevent a stockout?”** The three checkbox choices are **“No, it would likely fall behind.”**, **“Yes, twenty minutes is frequent enough.”**, and **“Only if the poll interval were shortened to five minutes.”**

The second **SCENARIO · DAVE** says: **“Say the agent is now event-driven and fires the instant stock crosses the threshold.”** Under **“How do you react well, not just fast?”** it asks: **“Beyond ‘stock crossed the threshold’, what else does it need to make a good call?”** The three checkbox choices are **“Stock levels at nearby stores, and whether the product is overstocked elsewhere.”**, **“Recent sales velocity, and whether this spike is weather-driven and temporary.”**, and **“Nothing else. The trigger is the decision.”**

No selection instruction or separate submit button is visible in the initial state; all six boxes are unchecked. Selecting a choice submits it immediately and displays **CORRECT** feedback plus **Try another answer**. For the polling question I selected **“No, it would likely fall behind.”** The Academy said: **“Right. A two-hour spike against a twenty-minute timer means most of the movement happens in the gaps, and the agent only ever sees a stale snapshot.”** For the context question, I selected **“Stock levels at nearby stores, and whether the product is overstocked elsewhere.”** The Academy said: **“Exactly the fast-vs-well distinction. A transfer from a store two states over may beat a reorder entirely.”** I then used **Try another answer** to check the other context answer: **“Recent sales velocity, and whether this spike is weather-driven and temporary.”** It was also marked **CORRECT**, with: **“Right. Reordering for a two-day storm the way you'd reorder for sustained demand is the wrong call made quickly.”** Each selection was checked separately; the choice **“Nothing else. The trigger is the decision.”** was not selected. The recap says the lesson covered polling, batch processing, and custom glue code; how an event-broker entrypoint lets the Inventory agent react as soon as something happens; how Acme could have prevented its original problem; and why both fast and well-informed reactions matter. No video, audio, or enlarged visual appears on this screen.

### Section 07, screen 1 — Getting Started

The SCORM sidebar is at **Lesson 09 — Getting Started**. The page description says to install the free Desktop App, configure two models, and build a first working agent in minutes. It estimates about 10 minutes and lists **4 videos**; the course meter reads 90% with about 5 minutes remaining.

Under **“Time to try it yourself!”** the page says the course so far has been theory and this section offers a hands-on activity that takes only a few minutes end to end; learners may expand on it creatively. It invites the learner to follow the videos to build a first agent with Solace Agent Mesh.

The four embedded videos are **Installing on Mac** (0:52), **Installing on Windows** (1:21), **Configure your models** (1:56), and **Build your first agent** (8:25). The Mac and Windows cards link to **Get the Solace Agent Mesh Desktop App for MacOS/Windows** at [solace.com/products/agent-mesh/download](https://solace.com/products/agent-mesh/download/). The written instructions also say the free app is available for Mac, Windows, or Linux, and the process is download, install, launch. No installation or download was performed.

The page's written **Steps** are:

1. **Get the Desktop App:** download the free app for Mac, Windows, or Linux, then install and launch it.
2. **Set up your models:** on first launch, set up a **General** model and a **Planning** model; choose any provider for which you have a key.
3. **Open Quick Build:** describe the desired agent in plain language; the canvas assembles a working agent from the sentence.
4. **Ask it something:** a sensible answer confirms a real agent talking to a real mesh in about five minutes, with no configuration written by hand.

The screen congratulates the learner on creating an agent and suggests playing with it or building a couple of agents useful in day-to-day life. The recap says the learner installed the free Desktop App, built a first working agent with Quick Build, and confirmed it with a live question.

#### Getting Started video captions and visual notes

The embedded videos exposed no captions or transcript controls. In the native player menu I inspected, the options were download, playback speed, and picture-in-picture; no captions option or transcript link was present. The videos were shown at their starting previews; I have not inferred spoken content beyond the visible course text.

The **Installing on Mac** preview shows a macOS desktop with a forest wallpaper and a Solace Agent Mesh installer icon. The **Installing on Windows** preview shows a dark Windows desktop with File Explorer open to the Desktop and the Agent Mesh setup executable listed. **Configure your models** shows a dark Agent Mesh interface with a **Configure Your AI Models** dialog: it says to enter LLM details for built-in General and Planning models in one step, noting they can be customized independently later or configured later in Agent Mesh; a **Model Provider** dropdown and **Cancel** and **Set Up Default Models** buttons are visible. **Build your first agent** shows the dark Quick Build interface with the prompt **“Let's build something. Tell me what you need.”**, suggestion chips, and a text-entry area.

**Visual file limitation:** I inspected the video previews and player menus. The supported screenshot-save route is blocked by its export policy, and no original still image was exposed for saving under `img/`; the visible preview frames are described above. No transcript or captions were available, so no claims from the videos' audio are added beyond the visible lesson text and preview content.

### Section 08, screen 1 — Glossary

The SCORM sidebar advanced to **Lesson 10 — Glossary**, described as a reference appendix of the technical terms used throughout the course. At entry, the SCORM meter visibly read **100%** and **Complete**, with about 5 minutes remaining. I opened each of the 20 glossary entries and recorded its definition:

| Term | Academy definition |
|---|---|
| Event-Driven Architecture (EDA) | Components communicate by producing, detecting, and consuming events routed through a broker, instead of calling each other directly. |
| Artificial Intelligence (AI) | The broad field of building systems that perform tasks normally requiring human judgment: reasoning, learning, solving problems without one fixed procedure. |
| AI Agent | A specialized unit, built around a model, given instructions and tools, that performs a defined job and communicates with other agents over A2A. |
| Agentic AI | Systems capable of reasoning through a task and taking action over time, not just answering a single question. |
| Large Language Models (LLM) | The models agents and the Orchestrator are built around, trained to generate and reason over language. |
| Natural Language Processing (NLP) | The field concerned with computers understanding and working with human language. |
| Generative AI | AI that produces new content, text, images, code, based on patterns learned from data, rather than retrieving something that already exists. |
| Artefact | A file or content object created or referenced during an agent's work. |
| Hallucination | An agent generating a confident answer that's actually wrong, usually from stale or missing context. |
| Retrieval Augmented Generation (RAG) | Giving an agent access to real, current information, often through a vector database, so it answers from current data instead of only what it learned during training. |
| Orchestrator | The built-in, LLM-backed coordinator that decides at runtime which agent should handle a request and in what order. |
| Workflow | An explicit, deterministic execution graph over a set of agents, used when the steps and their order need to be exactly the same every time. |
| Entrypoint | A way into the mesh—chat interface, Slack, an event straight off the broker, webhook/REST call, etc. |
| A2A Protocol | The open standard agents use to communicate with each other, regardless of what platform built them. |
| Connector | A configured link between the mesh and a backend system, set up once and reusable by any agent that needs it. |
| Toolset | A bundle of tools grouped together so an agent can use the whole set as one unit. |
| Skill | Packaged instructions and reference material an agent can load only for something outside its everyday routine. |
| ADLC (Agent Development Lifecycle) | The six-stage structure—Hiring, Onboarding, Coaching, Supervision, Teamwork, Improvement—that governs how an agent gets built, tested, deployed, and improved. |
| RBAC (Role Based Access Control) | Deciding what a person or agent is allowed to approve or access based on their role. |
| Observability / Tracing | A record of what an agent actually did, step by step, so a decision can be reviewed after the fact. |

This glossary screen contains no quiz, video, audio, or visual asset. The **Next lesson** control in the Academy shell leads to the separate **Feedback Survey - 2025** syllabus lesson.

**Event-driven sequence, Step 2 of 5 — The warehouse publishes an event:** The screen says that the instant stock drops below the threshold, the warehouse system publishes an event, now with something downstream listening for it. The card has **Back** and **Next step** controls.

**Event-driven sequence, Step 3 of 5 — The Inventory agent picks it up:** The agent subscribes to the reorder event. When the warehouse system emits it, the Inventory agent reacts immediately and starts its workflow.

**Event-driven sequence, Step 4 of 5 — It gathers real context:** As the workflow begins, the agent checks current stock across every store as well as recent sales velocity for that product.

**Event-driven sequence, Step 5 of 5 — It generates a reorder recommendation:** The agent builds a fresh recommendation from real-time data and either acts autonomously or sends it to a person for review. After I pressed **Next step** from step 5, the card returned to **Step 1 of 5 — Stock crosses the threshold**; the stepper loops without advancing the SCORM page.
