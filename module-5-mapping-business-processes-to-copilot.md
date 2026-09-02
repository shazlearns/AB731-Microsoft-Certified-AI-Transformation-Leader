# Module 5 — Mapping Business Processes & Use Cases to Copilot

> **Golden rule:** before using Copilot on any task, ask two questions: (1) Is this the kind of thing Copilot is actually good at? (2) Which Microsoft 365 app does this task naturally belong in? Get both right and you save real time — get either wrong and you either misuse the tool or place it in the wrong app.

## What is it?

This is the practical decision layer for using Copilot in real business processes: recognising the right use cases, understanding that Copilot behaves differently per app, and knowing where it delivers genuine productivity value — all without requiring new workflows or retraining staff.

## Explain like I'm 10

Copilot is like a skilled assistant who works differently depending on which room of the office you put them in. Before you hand them a task, check: is this something they're actually good at, and which room should they be working in?

## Real-world analogy

A personal assistant embedded in different rooms of an office — in the writing room (Word) they draft, in the numbers room (Excel) they crunch data, in the mailroom (Outlook) they triage email, in the meeting room (Teams) they recap discussions. You wouldn't ask the mailroom assistant to build your financial model — same assistant skillset, different context.

## Example

A finance team spends hours weekly manually summarising customer feedback spreadsheets into a report. Pain point identified (repetitive, manual) → use case recognised (summarisation + insight generation — Copilot's strength) → mapped to the right app: Excel for the data review, Word for drafting the final report.

## How it works — 4 building blocks

| Block | What it covers |
|---|---|
| Understanding Business Processes | Focus on information-work: content creation, data review, communication, analysis. Spot pain points — repetitive tasks, delays, manual data handling |
| Use Case Recognition | Copilot excels at drafting, summarisation, insight generation, ideation. NOT appropriate for authoritative decisions, unsupported systems, or deterministic automation |
| App-Context Awareness | AI behaves differently per app: Word = drafting, Excel = data analysis, Outlook = email, Teams = meetings |
| Productivity & Business Value | Reduces time on routine cognitive tasks, improves output consistency — critically, does this WITHOUT requiring new workflows or training |

## Deep dive: Enterprise vs. Consumer Copilot split

Analogy: two employees with the same skillset but different security clearances. Enterprise Copilot has a company badge that opens your organisation's internal filing system — it can pull up YOUR contracts, YOUR emails, YOUR spreadsheets, because Microsoft Graph hands it exactly what your own permissions already allow. Consumer Copilot has no badge — it only knows what's publicly known, or whatever you personally hand it in the conversation.

**The 4 dimensions that separate them:**

| Dimension | Enterprise (Microsoft 365 Copilot) | Consumer (General Copilot) |
|---|---|---|
| Data reach | Organisational data, via Microsoft Graph | Public information + user-provided content only |
| Capability | Contextual reasoning + in-app experiences (Word/Excel/Outlook/Teams) | Public knowledge Q&A + user-prompted generation only |
| Security | Operates within existing security controls + role-based access | No tenant governance at all |
| Permission boundary | Cannot access or expose anything the user isn't already permitted to see | N/A — no org permissions exist to enforce |

**Example:** a manager asks Enterprise Copilot to summarise a Q3 budget review doc in the Finance SharePoint. Copilot pulls it via Graph — but only because the manager already has access to that site. A junior staff member without that access would get nothing back; Copilot never grants MORE access than the person already has. The same question to Consumer Copilot simply can't be answered — that document doesn't exist in Consumer Copilot's world unless manually pasted in.

**The mechanism:** Microsoft Graph is the bridge that gives Enterprise Copilot org-data reach, and it's permission-trimmed by design — it enforces the existing security model rather than creating a new one. This is why M365 Copilot inherits security "automatically, not bolted on."

> **Exam trick:** an employee "seeing information via Copilot that they shouldn't have" is almost always testing whether you know this is a permissions/access misconfiguration issue upstream (in SharePoint/Graph permissions), NOT a Copilot flaw — Copilot enforces, it doesn't override, existing access.

> **Exam trick:** "only public information is needed, no governance required" → General/Consumer Copilot is the correct, simpler choice. Don't over-engineer with Enterprise Copilot when the task doesn't touch org data.

**Common confusion:** "Enterprise Copilot" is not just "the paid version" — it's about data reach and security model, not price tier. Licensing tier (Chat vs. paid add-on) is a separate axis from Enterprise vs. Consumer.

**Memory trick:** "Badge vs. no badge" — Enterprise Copilot has the company badge (Graph access, role-based permissions, org security). Consumer Copilot has no badge.

## Deep dive: Microsoft Graph — the connective layer

Analogy: every app you use at work (email, calendar, documents, chat) is a separate room with its own filing cabinet. Microsoft Graph is a single index card system that knows what's in every room and how they connect — so when you ask a question, it pulls the right pieces from multiple rooms at once.

| Block | What it covers |
|---|---|
| What Microsoft Graph Is | Connects M365 data — users, files, emails, meetings, activities. Lets Copilot retrieve relevant org data in real time |
| Permission-Trimmed Access | Graph only returns data the user is already authorised to access. Existing permissions, sharing settings, and access controls are enforced automatically |
| Contextual Understanding | Enables cross-data reasoning — linking emails to meetings, documents to chats. Provides context-aware responses instead of generic answers |
| When It Matters Most | Exam scenarios involving organisational content, security, or data access. Explains WHY Copilot responses are relevant, personalised, and secure |

**Example:** a user asks Copilot, "What did the team decide about the Q3 budget?" Without Graph, Copilot could only search a single source. With Graph, it links the budget email thread → the meeting where it was discussed → the shared spreadsheet → the follow-up Teams chat, stitching together a coherent answer — surfacing only what the user already has permission to see.

> **Exam trick:** "why does Copilot give more relevant, specific answers in M365 Copilot than generic Copilot?" → the answer is Microsoft Graph's cross-data reasoning, NOT "a better model" or "more training." Same underlying model, different data connectivity.

**Common confusion:** Graph is not a separate "database" Copilot queries — it's a connective/relationship layer. It doesn't store new data, it links and surfaces existing data across apps while respecting existing permissions.

**Memory trick:** "The connector, not the cabinet."

## Deep dive: the 3 Copilot licensing tiers

A separate axis from Enterprise vs. Consumer (which is about data reach) — licensing is about how much you pay and what features you get, once you've already decided M365 Copilot (Enterprise) is right.

| Tier | Cost | Grounding | In-app Copilot | Researcher & Analyst |
|---|---|---|---|---|
| M365 Copilot Chat | Included with M365 | Web only + uploaded files | No | No |
| M365 Copilot (paid add-on) | Paid, per-user/month | Web + work data via Graph | Yes (Word/Excel/PPT/Outlook/Teams) | Yes |
| Pay-as-you-go (Azure AI) | Usage-based | N/A — separate from Copilot licensing entirely | N/A | N/A |

> **Exam trick:** don't confuse "Copilot licensing" (Chat vs. paid add-on) with "Azure AI/Foundry subscription models" (pay-as-you-go vs. prepaid/commitment) — two completely separate licensing systems for two different products.

**When used:** Chat (included, free) → early exploration, low barrier, occasional use. Paid add-on → daily use, core productivity roles, needs in-app experiences + Graph grounding.

## Deep dive: Researcher vs. Analyst

Two distinct AI agents within M365 Copilot (paid add-on tier only), each optimised for a different type of thinking task.

| | Researcher | Analyst |
|---|---|---|
| Use for | Investigating, synthesising, comparing | Analysing metrics, interpreting numbers |
| Signal words | research, summarise, explore, compare, explain | analyse, evaluate, trends, metrics, performance |
| Output style | Narrative report / synthesis | Data interpretation / quantitative insight |

**Example:** "Research how our competitors have positioned their Q3 pricing" → Researcher. "Evaluate the trend in our churn rate over the last 4 quarters" → Analyst.

> **Exam trick:** a scenario can look like data work but actually be a Researcher task if it's synthesising qualitative sources (e.g. "compare what 5 vendors say about their support SLAs") rather than crunching numbers.

## Deep dive: Build vs. Buy vs. Extend

A decision framework for how much custom AI development an organisation should undertake — directly reflecting the golden rule of choosing the simplest solution that meets the need.

| Option | What it means | Example tool |
|---|---|---|
| Buy | Use out-of-the-box Copilot as-is, no customisation | M365 Copilot, standard |
| Extend | Add custom topics/flows/business logic without building from scratch | Copilot Studio |
| Build | Full custom AI application development | Azure AI / Foundry Tools |

**Decision principle:** start with Buy → move to Extend only when needed → Build only as a last resort.

**Example:** a company needs a chatbot answering general HR questions with no special logic → Buy. They need it to follow specific leave-policy rules and connect to their HR system → Extend (Copilot Studio). They need a fully custom AI system with proprietary models and complex multi-step orchestration → Build (Foundry Tools).

> **Exam trick:** a scenario describing something Copilot Studio could clearly handle but the answer choice offered is full custom Azure AI development — that's a distractor. Don't over-engineer; cost savings are a downstream consequence, not the primary driver — the reasoning is always the golden rule.

## Deep dive: the integrated Microsoft AI solution

Not a separate product — the concept that Copilot, Graph, Identity, Compliance, and Responsible AI aren't five separate bolt-on features, but one unified system working together.

Analogy: a hospital where the patient records system, the security badges, the compliance auditing, and the doctors' workflow tools are all ONE connected system — a doctor's badge automatically determines what records they can see, every access is logged for compliance, with no separate "security bolt-on" configured after the fact.

**The 5 components combined:**

| Component | What it contributes |
|---|---|
| Copilot | The AI assistant/interface layer |
| Graph | Connects org data, enforces permission-trimmed access |
| Identity | Identity-based access control — who you are determines what you can do |
| Compliance | Auditing, DLP, regulatory controls — built in, not configured separately |
| Responsible AI | Fairness, transparency, accountability — the ethical framework baked into behaviour |

**Why this matters:** this is WHY Microsoft 365 Copilot is preferred over standalone third-party AI tools whenever security, governance, or organisational data are involved. It inherits identity-based access, permission-trimming, DLP, auditing, and content safety automatically — "built in, not bolted on."

> **Exam trick:** a scenario comparing M365 Copilot against a standalone third-party AI tool for an internal, security-sensitive use case is testing this concept directly — the answer is always M365 Copilot, and the reasoning is the automatic INHERITANCE of security/governance, not just "it's from Microsoft."

**Memory trick:** "One system, not five tools."

## Deep dive: the full decision framework — explicit routing

| Scenario type | Route to | Then |
|---|---|---|
| Internal productivity, no customisation needed | M365 Copilot (Buy) | Done — out-of-the-box is enough |
| Internal productivity, needs custom topics/business rules | Copilot Studio (Extend) | Stays internal, structural customisation only |
| External-facing OR advanced/complex needs | Azure AI services (Build) | Full custom development via Foundry Tools |

**Refined signal words (Researcher vs. Analyst):** "explain" also points to Researcher (synthesis, not number-crunching), and "performance" also points to Analyst (implies metrics/quantitative evaluation).

**A new, independent Build trigger:** beyond "external-facing" or "highly specialised," the exam also treats "the AI experience goes beyond assistant-style interaction" as a standalone Build signal — this applies even to an internal-only tool.

> **Exam trick:** don't assume "internal-only" automatically means Buy or Extend. If the described AI behaviour goes beyond assistant-style Q&A — e.g. autonomous multi-step orchestration embedded in a custom app — that's a Build signal even for a purely internal tool.

**Memory trick:** "Internal stays simple, external goes Azure, beyond-assistant goes Build" — three independent checks, not one.

## When used

When mapping a real business process or task to the right AI tool/app combination — especially in scenarios asking "should Copilot be used here?" or "which app should this task use?"

## Exam focus

**Must know:** the "NOT appropriate for" list — authoritative decisions, unsupported systems, deterministic automation. This is the exam's favourite trap: a scenario describing a compliance sign-off, a legacy system with no Copilot integration, or a fixed rules-based process is testing whether you know Copilot is the WRONG answer.

**Should know:** the task→app mapping (Word/Excel/Outlook/Teams).

> **Exam trick:** "enhances productivity without requiring new workflows or training" is a testable phrase — if a scenario says a solution requires retraining staff or redesigning processes, that's a signal it's NOT well-mapped Copilot usage.

> **Exam trick:** fixed/deterministic criteria (e.g. "approve loans based on fixed credit criteria") points to a rule-based system, not Copilot — even though it sounds like a decision AI could help with. Copilot assists with drafting/summarising around the decision, not making the authoritative call itself.

## Exam keywords

Information-work scenarios, pain point identification, use case recognition, app-context awareness, authoritative decisions, deterministic automation, unsupported systems, productivity, business value, no new workflows/training required, rule-based system, Enterprise Copilot, Consumer Copilot, Microsoft Graph, permission-trimmed, role-based access, tenant governance, cross-data reasoning, contextual understanding, connective layer, licensing tiers, Copilot Chat, paid add-on, Researcher, Analyst, signal words, Build/Buy/Extend, decision principle, simplest solution, integrated Microsoft AI solution, built in not bolted on, identity-based access, DLP, standalone third-party AI tools, decision framework, Azure AI services, external/advanced scenarios, beyond assistant-style interaction.

## Common confusion

People assume Copilot = automation for everything. It's not — it excels at drafting, summarising, generating insight, and ideating, but deliberately stays out of deterministic/rule-following automation and out of final authoritative decisions (a human must own those — ties back to Responsible AI's Accountability principle).

## Memory trick

> "P-U-A-P" → Process (spot the pain point) → Use case (does it fit Copilot's strengths?) → App (which app owns this task?) → Productivity (value delivered without retraining).

## Practice questions

**Question 1.** A team wants Copilot to automatically approve or reject loan applications based on fixed credit criteria. Should Copilot be used here?
**Answer:** No. Fixed/deterministic criteria points to a rule-based system, not Copilot.

**Question 2.** A manager needs to turn scattered meeting notes into a polished summary document. Which app-context should this task map to?
**Answer:** Word — drafting a document is a Word task, even if the notes originated in Teams.

**Question 3.** A scenario says a new AI solution "requires all staff to learn a new workflow before it delivers value." What does this suggest?
**Answer:** It suggests this is NOT well-mapped Copilot usage — a solution needing retraining/redesigned processes signals a mismatch.

**Question 4.** A junior analyst without access to the HR system asks Enterprise Copilot to summarise HR salary data. What happens?
**Answer:** Copilot returns nothing — it never grants more access than the user already has.

**Question 5.** An employee occasionally wants to ask Copilot general work questions but doesn't need it embedded inside Word/Excel. Which licensing tier fits?
**Answer:** M365 Copilot Chat — included with M365, web-only grounding plus uploaded files, no in-app experiences needed.

**Question 6.** A team needs Copilot to follow specific approval workflows unique to their industry, connected to an internal system — nothing more complex than that. Buy, Extend, or Build?
**Answer:** Extend (Copilot Studio) — custom topics/business logic without building from scratch.

**Question 7.** An internal tool needs an AI that autonomously orchestrates a multi-step approval workflow embedded in a custom app UI, going well beyond assistant-style Q&A. Buy, Extend, or Build?
**Answer:** Build — "the AI experience goes beyond assistant-style interaction" is an independent Build trigger regardless of internal/external status.

## Related concepts

3 Types of AI
