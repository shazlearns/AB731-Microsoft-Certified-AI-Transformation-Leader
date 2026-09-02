# Module 6 — Foundry Tools & the Copilot/Foundry Decision Framework

> **Golden rule:** Copilot is for USING AI. Foundry is for BUILDING and RUNNING AI. Only reach for Foundry when the need genuinely goes beyond what Copilot or Copilot Studio can structurally provide — and the exam always rewards the simplest adequate platform.

## What is it?

Foundry Tools is Microsoft's platform for full custom AI development — model orchestration, RAG pipelines, and lifecycle governance — for scenarios that go beyond productivity tools and require actual AI engineering, not just configuration.

## Explain like I'm 10

Copilot Studio lets you customise an assistant's rulebook. Foundry Tools lets you build your own AI robot from raw parts — you choose its brain, wire up its parts, and you're responsible for testing, deploying, and watching over it.

## Real-world analogy

A car dealership (Buy = Copilot), a customisation shop that adds features to an existing model (Extend = Copilot Studio), and a full engineering workshop that builds a vehicle from raw parts (Build = Foundry Tools). You only go to the workshop when nothing off-the-shelf or modifiable will do.

## Example

A company wants to build a custom AI system that retrieves proprietary technical manuals (not in SharePoint/Graph), reasons over them using a RAG pattern, and feeds results into a multi-step diagnostic pipeline for engineers. No amount of Copilot Studio "topics" can do this — it needs actual model orchestration. That's a Foundry Tools job.

## How it works — 4 building blocks

| Block | What it covers |
|---|---|
| Understanding the Business Problem | Signals: the need goes beyond productivity tools — building models, managing AI workflows, applying lifecycle governance |
| AI Development and Orchestration | Foundry supports the full AI lifecycle — development → deployment → monitoring. Triggers: custom models, RAG patterns, multi-step AI pipelines |
| Governance, Monitoring & Control | Built-in tools for responsible AI evaluation, content safety, model monitoring |
| Operational & Scalable Use Cases | Map to Foundry when a solution must scale, integrate, or evolve over time — match the need to the simplest adequate platform |

## Deep dive: Foundry services

| Service | What it does | Use when |
|---|---|---|
| Azure AI services | Prebuilt APIs — vision, speech, language, decision — no training required | Well-defined tasks: translation, sentiment analysis, document processing |
| Azure Vision | Image/video analysis, OCR (text extraction), visual inspection at scale | Business process involves documents, product images, visual inspection |
| Azure AI Search | Intelligent discovery over structured AND unstructured content — powers RAG patterns | Grounding AI responses in organisational knowledge bases |
| Microsoft Foundry | The enterprise platform layer — build/deploy/manage AI under unified governance | Integrating AI services, custom models, and data connections together |

> **Exam trick:** Azure AI Services (prebuilt APIs), Azure AI Search (retrieval/grounding), and Microsoft Foundry (the umbrella platform) are three different layers, not synonyms.

## Deep dive: matching an AI model to a business need

Once you've decided a scenario needs Foundry-level custom development, there's a second decision layered on top: which *type* of model actually fits the task.

**Step 1 — identify the task type:**

| Task type | Examples | Points to |
|---|---|---|
| Generative | Content creation, summarisation, Q&A, conversational interaction | Generative AI / LLMs |
| Analytical | Classification, prediction, anomaly detection, trend analysis | Traditional ML |

**Step 2 — apply constraints and context:** weigh data type, latency, cost, accuracy requirements, and compliance needs before locking in a model choice.

> The Golden Rule, again: the exam rewards choosing the simplest model type that meets the business requirement — the same principle applied to platform choice (Buy/Extend/Build) and to model choice.

**Bank examples:**

| Scenario | Model type |
|---|---|
| Flag potentially fraudulent transactions from historical spending patterns | Traditional ML — anomaly detection |
| Draft personalised responses to customer complaint emails | Generative — content creation |

## Deep dive: SLMs & embedding models

| Model type | What it is | Best for |
|---|---|---|
| SLM (Small Language Model) | A smaller, cheaper, faster version of an LLM — often runs on-device | Latency-sensitive or cost-sensitive tasks that don't need a full LLM's capability |
| Embedding model | Converts text (or other data) into numerical vectors representing meaning | Powers semantic search and RAG retrieval — finds "similar meaning" content, not exact keyword matches |

Analogy: an LLM is a senior consultant who can reason deeply about anything. An SLM is a junior analyst — faster and cheaper, good enough for narrower tasks. An embedding model isn't a "thinker" at all — it's a librarian's indexing system, converting documents into a form where "similar meaning" items sit near each other.

**SLM example:** a mobile banking app runs an on-device SLM to instantly answer "what's my account balance" — no internet round-trip, works on a weak connection, costs almost nothing at scale. A full LLM here would be overkill.

**Embedding model example:** "How do I waive a late fee?" and "Can a penalty charge be removed?" share no common words, but an embedding model places them close together because they mean the same thing. This is how a RAG system finds the right SOP even when a staff member's wording doesn't match the document's wording — something a plain keyword search would miss.

> **Exam trick:** SLM is about size/speed/cost. Embedding model is about search (finds the right content by meaning). A scenario about on-device cost savings points to SLM; a scenario about correctly retrieving the right document despite different wording points to the embedding model.

## Deep dive: Foundry benefits at enterprise scale

**1. Enterprise-Scale AI Enablement.** Building a house where you'd otherwise separately hire an architect, source materials from five suppliers, hire an inspector, and coordinate them all yourself — Foundry is the project manager + one unified toolkit. Bank example: instead of separately setting up a data pipeline tool, a model training environment, a compliance dashboard, and a deployment system from different vendors, Foundry gives the team all of it in one connected platform.

**2. Scalability — elastic infrastructure without manual capacity planning.** Underlying compute/storage automatically expands or shrinks based on actual demand. Analogy: a rubber band (stretches automatically) vs. a fixed pipe (overflows or needs manual resizing). Bank example: a Black Friday-style promotion spikes fraud-check volume 10x for a few hours; elastic infrastructure auto-allocates more compute then scales back down.

**3. Security and Governance — network isolation + audit logging.**

| Capability | What it means |
|---|---|
| Network isolation | The AI workload runs inside its own isolated network boundary — like a bank vault inside the bank |
| Audit logging | Every access, query, and action on the AI system is automatically recorded |

Bank example: proving to a regulator that only authorised staff queried customer transaction data through the AI system last quarter — audit logging gives that exact timestamped, attributable record already.

**4. Operational Confidence — model versioning + deployment management.**

| Capability | What it means |
|---|---|
| Model versioning | Every model version is saved and tracked — like "track changes" in a Word document — so you can compare or roll back instantly |
| Deployment management | Tools to control HOW a new model version goes live (e.g. gradually, to a small % of traffic first) |

Bank example: retraining the fraud model with new transaction patterns — deployment management lets the bank test the new version on 5% of transactions first; if it flags too many false positives, model versioning lets them roll back in minutes.

> **Memory trick:** "One platform, stretches to fit, locked and logged, safe to iterate" — Enablement → Scalability → Security → Operational Confidence.

## Deep dive: the full Copilot & Foundry decision tree

Walk top to bottom:

| Gate | Question | Answer → Route |
|---|---|---|
| 1 | Does it need organisational data (Microsoft Graph)? | No → Consumer Copilot · Yes → Gate 2 |
| 2 | Does it need customisation / an internal system connection? | No → Gate 3 · Yes → Gate 4 |
| 3 | Daily use + in-app embedding (Word/Excel/Outlook/Teams)? | No → M365 Copilot Chat · Yes → M365 Copilot (paid add-on) |
| 4 | Is that ALL it needs — no RAG, custom model, or multi-step pipeline? | Yes → Copilot Studio (Extend) · No → Azure AI Foundry (Build) |

**Bank use case examples — one per destination:**

| Destination | Bank scenario |
|---|---|
| Consumer Copilot | A relationship manager asks Copilot to explain what the RBA's latest cash rate decision means in plain English — public knowledge, no internal data involved |
| M365 Copilot Chat | A branch teller occasionally asks Copilot to help word a customer email about a fee waiver — low-frequency, no need to live inside Outlook or pull Graph data |
| M365 Copilot (paid add-on) | A credit risk analyst uses Copilot daily inside Excel to evaluate loan default trends — needs Graph grounding + in-app embedding |
| Copilot Studio (Extend) | The bank builds a bot that walks new-account staff through KYC document checklist rules and connects to the internal onboarding system |
| Azure AI Foundry (Build) | The bank builds a custom fraud-detection system: a RAG pattern over historical transaction patterns feeding a multi-step model pipeline that flags suspicious activity and explains its reasoning to investigators |

**The independent Build trigger:** regardless of internal/external status, "the AI experience goes beyond assistant-style interaction" (autonomous multi-step orchestration, not just conversational Q&A) is its own standalone signal for Build.

> **Exam trick:** Azure AI services is the exam's explicit, named destination for "external or advanced" scenarios.

## When used

When a scenario describes custom model development, RAG patterns, multi-step AI pipelines, or a need for full lifecycle governance (build → deploy → monitor) that Copilot/Copilot Studio structurally cannot provide.

## Key differences

This is the detailed "Build" endpoint of the Build/Buy/Extend spectrum. Three concrete triggers separate Build from Extend: custom models, RAG patterns, multi-step AI pipelines — plus the independent "beyond assistant-style interaction" signal.

## Exam focus

**Must know:** "the exam rewards matching the business need to the simplest adequate platform" — don't pick Foundry if Copilot Studio could handle it.

> **Exam trick:** a scenario mentioning "governance" or "monitoring" alone doesn't automatically mean Foundry — Copilot already has governance via the Integrated Solution (Graph/Identity/Compliance). Foundry's governance layer is specifically for custom-built models and pipelines.

## Exam keywords

Foundry Tools, custom AI development, orchestration, AI lifecycle, RAG patterns, multi-step AI pipelines, responsible AI evaluation, content safety, model monitoring, enterprise compliance, simplest adequate platform, Azure AI services, Azure Vision, Azure AI Search, decision framework, beyond assistant-style interaction, OCR, task type, generative tasks, analytical tasks, SLM, embedding model, semantic search, elastic infrastructure, network isolation, audit logging, model versioning, deployment management.

## Common confusion

People assume "governance" is a Foundry-exclusive feature. It's not — Copilot has governance too (via Graph/Identity/Compliance inheritance), just automatic and built-in rather than something you configure yourself. Foundry's governance tools are for when you're the one building and need to actively evaluate/monitor a custom model.

## Memory trick

> "Build it, Ship it, Watch it" — Foundry covers the whole lifecycle: build (development/orchestration) → ship (deployment) → watch (monitoring/governance).

## Practice questions

**Question 1.** A business needs an AI that retrieves data from a proprietary internal database using a RAG pattern and performs multi-step reasoning across several data sources. Buy, Extend, or Build?
**Answer:** Build (Azure AI Foundry). RAG patterns and multi-step AI pipelines are explicit Foundry triggers — Copilot Studio can't handle RAG or custom multi-step orchestration.

**Question 2.** A bank wants to predict which loan applicants are likely to default based on structured financial data. Generative or Traditional ML?
**Answer:** Traditional ML — an Analytical task (prediction).

**Question 3.** A mobile banking app wants an instant, low-cost, on-device response for basic balance queries. SLM or full LLM?
**Answer:** SLM — smaller, cheaper, faster, often runs on-device, matching this latency- and cost-sensitive, narrow task.

## Related concepts

Mapping Business Processes & Use Cases to Copilot · Microsoft Copilot Studio (Topic-Based Design)
