---
title: Exam
document_type: lesson
source: Solace Academy
learning_path: Solace Certified Agent Mesh Practitioner Path
course: Solace Certified Agent Mesh Practitioner Exam
lesson_order: 2
---

# Exam

## Academy result

The Academy exam page presented **30 required questions** on one page, a 90-minute time limit, and **3 of 3 attempts left** before submission. I answered every question and submitted the test. The result modal said **“Well done, you have completed the course!”**, reported a **100%** final grade, confirmed **“You earned the course certificate”** and **“You earned the certification: Solace Certified Agent Mesh Practitioner.”** The same modal showed the learning plan completed with **2 of 2 courses completed**. The learning-plan page then confirmed both mandatory courses complete and recorded completion at **09/28/2026 12:43:12 pm**. The Academy provided only the aggregate grade, so correctness is confirmed by the 100% result rather than separate per-question feedback.

## Exam questions, choices, and submitted answers

The questions and choices below are transcribed from the exam screen. The selected response for each item is listed after the choices.

### Question 1

**Which of the following are node types a Solace Agent Mesh workflow is built from, according to this course? Select all that apply:**

- Map — selected
- Loop — selected
- Agent — selected
- Retry
- Switch — selected

### Question 2

**Which of the following is NOT a core capability provided by Solace Agent Mesh?**

- Automated fine-tuning of large language models — selected
- Hosting the tools agents call and connecting them to real enterprise data
- Event-driven inter-agent communication
- Multi-agent task coordination and orchestration

### Question 3

**A $900 return needs to be held for a human decision. Which patterns are doing the work?**

- Conditional, then human-in-the-loop — selected
- Map, because each item is checked independently
- Sequential, because the steps happen in order
- Event-driven, because the return triggered the process

### Question 4

**What do cost, governance, security, and repeatability have in common in this course?**

- They only apply once an agent has already failed in production
- They are the practical checklist that the ADLC is actually for — selected
- They are four pricing tiers Solace Agent Mesh offers
- They are four separate certifications an agent must earn

### Question 5

**What does Event-Driven Architecture (EDA) mean, as this course uses the term?**

- Components exchange data only through a shared database
- A single central service makes every decision for the whole system
- Components communicate by producing, detecting, and consuming events routed through a broker, instead of calling each other directly — selected
- Every component polls every other component on a fixed schedule

### Question 6

**What is a Workflow, as distinct from the Orchestrator?**

- A faster version of the Orchestrator that uses a smaller model
- A list of agents ranked by how often they're used
- A manual approval queue with no automation at all
- An explicit execution graph where every step, order, and failure path is defined ahead of time — selected

### Question 7

**A team writes a script that directly queries System A's database whenever System B needs updated information, with no shared event stream between the two systems. Which flawed pattern does this describe?**

- Polling
- Custom glue code — selected
- Event-driven integration
- Batch processing

### Question 8

**True or false: choosing a Workflow means the agents inside it are less capable than agents the Orchestrator calls.**

- False, a workflow constrains the control flow around the agents, not the agents' own intelligence — selected
- True

### Question 9

**A snowstorm causes a spike in orders for winter boots at three stores over two hours. Would a polling-based system checking every 20 minutes catch this in time to prevent a stockout?**

- Only if the poll interval were lengthened to an hour
- Yes, twenty minutes is frequent enough
- No, it would likely fall behind, since most of the movement happens in the gaps between checks — selected

### Question 10

**Which four things does a running Agent Mesh come down to, according to this course? Select all that apply:**

- Entrypoints — selected
- The event broker — selected
- A central database
- Gateways
- Tools — selected
- Agents — selected

### Question 11

**An Acme team builds an agent in an afternoon. It works in testing, but three months later nobody remembers why it makes certain decisions, and there's no record of who approved it going live. Which root problem does this demonstrate?**

- No safe way to give an agent real-time data access
- A cost problem
- Lock-in and sprawl
- The gap between a working demo and something that runs in production — selected

### Question 12

**Match each component with its role.**

The choices available in each dropdown were **Has a model, instructions, and tools, built for one specific job**; **How an agent reaches the outside world, such as a database query or an API call**; **Carries every message between every piece, so a new agent can be added later without redesigning existing ones**; and **A door into the mesh, such as a chat window, a Slack channel, or an event off the broker**.

- Tool → How an agent reaches the outside world, such as a database query or an API call
- Agent → Has a model, instructions, and tools, built for one specific job
- Event broker → Carries every message between every piece, so a new agent can be added later without redesigning existing ones
- Entrypoint → A door into the mesh, such as a chat window, a Slack channel, or an event off the broker

### Question 13

**Match each ADLC stage with what it actually covers.**

The choices available in each dropdown were **Running the agent against realistic and edge-case scenarios before it talks to a real customer**; **Deciding what the agent's job is, before anyone touches a model**; **Coordinating with other agents and handing off work without stepping on each other**; **Reviewing what the agent got right and wrong, and feeding that back into the next version**; **Giving the agent access to the right data sources and the right security scope, nothing more**; and **Deciding where the stakes are high enough that a person needs to confirm a decision**.

- Teamwork → Coordinating with other agents and handing off work without stepping on each other
- Improvement → Reviewing what the agent got right and wrong, and feeding that back into the next version
- Onboarding → Giving the agent access to the right data sources and the right security scope, nothing more
- Supervision → Deciding where the stakes are high enough that a person needs to confirm a decision
- Hiring → Deciding what the agent's job is, before anyone touches a model
- Coaching → Running the agent against realistic and edge-case scenarios before it talks to a real customer

### Question 14

**What does a Switch node do inside a workflow?**

- Repeats a step until a person manually stops it
- Deletes a step that fails validation
- Calls every agent in the mesh simultaneously
- Checks conditions in order and routes to the first one that matches — selected

### Question 15

**Match each orchestration pattern with the mechanism behind it.**

The choices available in each dropdown were **An ordinary workflow step whose job is putting the decision in front of a person instead of an agent**; **One step declares it depends on the step before it**; **Steps with no dependency on each other run together automatically**; **The workflow registers itself on the event broker and is triggered by a published event**; and **A Switch checks conditions in order and routes to the first match**.

- Event-driven → The workflow registers itself on the event broker and is triggered by a published event
- Conditional → A Switch checks conditions in order and routes to the first match
- Parallel → Steps with no dependency on each other run together automatically
- Human-in-the-loop → An ordinary workflow step whose job is putting the decision in front of a person instead of an agent
- Sequential → One step declares it depends on the step before it

### Question 16

**What is an Entrypoint?**

- A backup copy of an agent's configuration
- A way into the mesh, such as chat, Slack, or an event arriving straight off the broker — selected
- A stored credential used to authenticate an agent
- A rule that decides which model an agent uses

### Question 17

**Why does it matter that an agent isn't hardcoded to a single model provider?**

- It removes the need for a tool or a data connection
- Switching providers becomes a configuration change instead of a rewrite of the agent — selected
- It automatically makes the agent faster
- It means the agent no longer needs any instructions

### Question 18

**What does the A2A protocol let agents do?**

- Query a vector database directly without going through a tool
- Bypass the event broker for faster communication
- Automatically retrain themselves on new data
- Talk to any other agent on the mesh, regardless of who built it or what platform it runs on — selected

### Question 19

**Which of the following are among the root problems that stall agentic AI projects, according to this course? Select all that apply:**

- No standard way agents get built across teams — selected
- Lock-in and sprawl — selected
- Too many available LLM providers to choose from
- No safe way to give an agent real-time data access — selected
- A real cost problem, driven partly by agents guessing without fast access to the right context — selected

### Question 20

**What is the difference between reacting fast and reacting well?**

- Reacting fast means noticing the instant something happens; reacting well also requires enough real-time context to make a good decision, not just a fast one — selected
- There is no difference, a fast reaction is always a good one
- Reacting well means waiting as long as possible before acting
- Reacting fast only matters for Workflows, not for individual agents

### Question 21

**Which of the following are among the six stages of the ADLC? Select all that apply:**

- Teamwork — selected
- Hiring — selected
- Supervision — selected
- Deployment
- Improvement — selected
- Training
- Coaching — selected
- Onboarding — selected

### Question 22

**Every incoming order must be validated, checked against stock, priced, and then either confirmed or sent for review, identically, every single time. Is this best handled by the Orchestrator, or a Workflow?**

- Orchestrator
- Workflow — selected

### Question 23

**Why does an event-driven Inventory agent react to a stock threshold faster than a polling-based one?**

- It subscribes directly to the event the warehouse system already publishes, instead of checking in on a timer and missing everything that happens between checks — selected
- It stores a local copy of the entire inventory database
- It uses a more powerful language model
- It ignores stock levels below a certain threshold

### Question 24

**What is Solace Agent Mesh?**

- A database management system
- A user interface design tool
- A network routing protocol
- An agent development and runtime platform — selected

### Question 25

**Why does subscribing directly to a published event let an agent react faster than checking a database on a timer?**

- It only works for read-only data, which is inherently faster
- It stores a complete local copy of the source database
- It's notified the instant something changes, instead of waiting for its next scheduled check — selected
- It uses a larger, more powerful model

### Question 26

**What is MCP used for?**

- Deciding which agent should handle a given request
- Training a new large language model from scratch
- Encrypting messages sent over the event broker
- Letting an agent reach a tool or a data source without that connection being specific to one vendor's way of doing things — selected

### Question 27

**What is the tradeoff of using the Orchestrator for a given request?**

- It can only be used with a single model provider
- It requires the request to be fully specified in advance
- It cannot call more than one agent per request
- It isn't guaranteed to take the same path twice, since it samples from a distribution rather than running a fixed function — selected

### Question 28

**What does a Map node do inside a workflow?**

- Runs one step once for every item in a list, in parallel, and collects the results — selected
- Converts a workflow into an Orchestrator call
- Produces a visual diagram of the workflow for documentation
- Maps a request to a single specific agent, chosen at random

### Question 29

**Match each protocol with what it standardizes.**

The choices available for each protocol were **How an agent reaches a tool or a data source** and **Agent-to-agent communication, regardless of platform**.

- MCP → How an agent reaches a tool or a data source
- A2A → Agent-to-agent communication, regardless of platform

### Question 30

**What is a Skill, in the context of this course?**

- A visual score shown on the mesh dashboard
- Packaged instructions and reference material an agent loads only for something outside its everyday routine — selected
- A permanent upgrade to an agent's underlying model
- A required certification every agent must pass before deployment
