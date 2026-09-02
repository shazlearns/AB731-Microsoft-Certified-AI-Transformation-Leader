# Module 5 — Microsoft Copilot Studio (Topic-Based Design)

> **Golden rule:** Copilot Studio is the low-code "Extend" layer between out-of-the-box Copilot and full custom Azure AI development — use it when responses must follow business rules and stay within guided, controlled boundaries, without building a whole custom AI app.

## What is it?

Copilot Studio lets organisations define custom topics, conversation flows, and connections to internal data/systems — building standalone copilots or extending existing Microsoft 365 Copilot experiences, all without writing a full custom AI application from scratch.

## Explain like I'm 10

Copilot is a smart new employee who knows things generally but doesn't know YOUR company's specific rules yet. Copilot Studio is the training manual you hand them — it tells them exactly what topics to stick to, what business rules to follow, and which internal systems they're allowed to check.

## Real-world analogy

A call centre: out-of-the-box Copilot is a new hire with general knowledge but no script. Copilot Studio is you writing their call scripts (topics/flows) and giving them access to your CRM (internal data/systems) — controlled, on-brand, on-topic. Full custom Azure AI development would be building an entirely new call-centre software system from scratch.

## Example

An insurance company needs a chatbot that only answers claims-policy questions, follows strict regulatory wording, and pulls live claim status from an internal system. Generic Copilot can't guarantee on-policy answers; building a custom Azure AI app is overkill. Copilot Studio fits: topic-based design keeps it on-scope, and it connects to the internal claims system.

## How it works

| Area | What it covers |
|---|---|
| What Copilot Studio Is | Define custom topics, conversation flows, connect to internal data/systems. Create standalone copilots OR extend existing M365 Copilot experiences |
| When It's the Right Tool | Responses must follow business rules/policies/domain-specific logic. Organisations need predictable, guided conversations with controlled outputs |
| Governance & Control | Topic-based conversation design prevents off-scope responses. Integrates with enterprise identity, security, and compliance models |
| vs. Build or Buy | Use when extending Copilot without building a full custom AI app. Sits between out-of-the-box Copilot and custom Azure AI development |

## Deep dive: the mechanism of topic-based conversation design

Topic-based conversation design is Copilot Studio's core architecture: instead of letting the AI freely generate any response to any input, the builder defines a finite set of **topics** — each with its own trigger phrases, conversation flow, and boundaries. The AI only activates a topic when the user's input matches that topic's scope. If nothing matches, it falls back to a default/fallback response rather than improvising.

Analogy: a restaurant menu instead of a chef who'll cook anything you ask for. The menu (topics) defines exactly what's on offer. If you ask for something not on the menu, the waiter doesn't wing it — they say "that's not something we serve" and redirect you, rather than making up a dish that might be wrong, off-brand, or unsafe.

**How the mechanism works, step by step:**

| Step | What happens |
|---|---|
| 1. Topic definition | Builder defines specific topics (e.g. "Check claim status," "Explain return policy") |
| 2. Trigger phrases | Each topic has example phrases/utterances that activate it |
| 3. Conversation flow | Once triggered, the AI follows a designed flow — specific questions, specific data lookups, specific response structure |
| 4. Scope boundary | If user input doesn't match any defined topic, the system falls back to a default response rather than generating an open-ended answer |
| 5. Data connection (optional) | Within a topic's flow, it can pull from connected internal systems — but only in the way the flow defines |

**Example:** an insurance claims chatbot. Topic: "Check Claim Status." Trigger phrases: "where's my claim," "claim status," "check my claim." Flow: ask for claim number → look up status in internal system → return status in pre-approved wording. If a user instead asks "what do you think about my accident, was it my fault?" — that's outside any defined topic, so the system falls back to "I can only help with claim status and policy questions" rather than improvising a liability opinion.

**Why this is THE governance mechanism, not just a feature:** generic Copilot reasons openly across whatever it's asked. Topic-based design structurally removes the possibility of off-scope, off-brand, or non-compliant responses — it's not relying on the AI "choosing" to stay on-topic, it's architecturally constrained to only operate within defined topics.

## When used

When a scenario needs responses to follow business rules/policies/domain logic, needs predictable guided conversations with controlled outputs, or wants to extend Copilot with internal data/systems without building a full custom AI app.

## Key differences

| Concept | Distinction |
|---|---|
| Copilot Studio vs. generic Copilot | Generic Copilot reasons openly; Copilot Studio structurally constrains to defined topics only |
| Copilot Studio vs. custom Azure AI/Foundry | Copilot Studio is low-code, topic/flow-level customisation. Foundry is for custom models, RAG pipelines, full lifecycle governance |
| "Why/when to use" vs. "mechanism" | Business rules + controlled outputs = the GOAL. Topic-based design = the MECHANISM that achieves it |
| Structural vs. behavioural constraint | Topic-based design is architectural (no path exists to an undefined topic) — not a prompt-level instruction the AI could ignore |

## Exam focus

**Must know:** Copilot Studio = the "Extend" option in the Build/Buy/Extend framework. Topic-based design is the specific mechanism (not just "governance" in the abstract) that prevents off-scope responses.

> **Exam trick:** a scenario describing a chatbot that must NEVER give advice outside its defined scope, no matter how it's asked, is testing topic-based design specifically — the answer isn't "add more guardrails" or "fine-tune the model," it's "structure it with defined topics and a fallback for anything outside them."

> **Exam trick:** "topic-based conversation design prevents off-scope responses" is the governance mechanism itself, not a side benefit.

## Exam keywords

Custom topics, conversation flows, internal data/systems connection, standalone copilot, extend M365 Copilot, business rules/policies, domain-specific logic, guided conversations, controlled outputs, topic-based design, trigger phrases/utterances, fallback response, scope boundary, structural constraint, enterprise identity/security/compliance integration, Build/Buy/Extend.

## Common confusion

People conflate Copilot Studio with full custom Azure AI/Foundry development — they're not the same tier; Copilot Studio sits above custom development on the effort/control spectrum. People also assume "controlled outputs" means the AI is being told to "behave" via a prompt/instruction — it's not prompt-level, it's architectural. The AI literally can't wander into an undefined topic.

## Memory trick

> "Middle child" — Copilot Studio is the middle child between out-of-box Copilot (too general) and custom Azure AI development (too much effort). "Menu, not chef."

## Practice questions

**Question 1.** A retail company wants a chatbot that only discusses store return policy, in exact regulatory wording, connected to their inventory system. Should they use generic Copilot, Copilot Studio, or full custom Azure AI development?
**Answer:** Copilot Studio. The scenario needs business-rule-constrained, on-scope responses plus a connection to an internal system — exactly what topic-based design provides, without building a full custom AI app.

**Question 2.** What's the specific mechanism Copilot Studio uses to stop a conversation from wandering off-topic?
**Answer:** Topic-based conversation design — defined topics with trigger phrases, a designed flow, and a fallback response for anything outside those topics. This is a structural constraint, not a behavioural instruction.

**Question 3.** A user asks a HR Copilot Studio bot (built only with topics for "leave balance" and "payslip download") a completely unrelated question about company stock price. What happens?
**Answer:** The bot falls back to a default/fallback response instead of attempting to answer — no topic is defined for stock price, so there's no path for the AI to reason about it.

## Related concepts

Mapping Business Processes & Use Cases to Copilot
