# Module 8 — Driving AI Adoption: The Adoption Team & Scaling

> **Golden rule:** a great pilot is not the same as adoption. The exam rewards recognising that adoption is an ongoing, cross-functional job — not a one-time training event, and not something a single team can own alone.

## What is it?

The Adoption Team is the cross-functional group that translates AI strategy into practical, day-to-day usage — making sure AI tools are actually used effectively, not just deployed. It's distinct from the AI Council (Module 7), which sets the strategy and policy the Adoption Team then executes.

## Explain like I'm 10

Imagine you plant one seed in your garden and it grows into a beautiful flower. Amazing! But that's not a garden yet — a garden needs lots more seeds planted, watered regularly, weeded, and checked on for months. The Adoption Team's job is turning one successful flower (a pilot) into a whole garden (enterprise-wide usage), and then keeping that garden alive — forever, not just on planting day.

## Real-world analogy

A bank's fraud team loves a new AI tool and uses it brilliantly. That's one flower. Scaling adoption means also rolling it out to the loans team, customer service, and every branch — AND keeping the training, support, and check-ins going for all of them, month after month, not just running one big training day and calling it done.

## Example

A bank runs a hugely successful 3-month AI pilot in customer service, then moves straight on to the next project with no further expansion. This is NOT adoption success — it's a Scaling Adoption gap. One team doing well is not the same as the organisation having adopted AI.

## How it works — 4 pillars

| Pillar | What it covers |
|---|---|
| Purpose of an Adoption Team | Translates AI strategy into practical, day-to-day adoption activities. Ensures AI tools are actually used effectively — not just deployed |
| Roles and Responsibilities | Includes business units, IT, security, and compliance stakeholders. No single function owns adoption — it structurally requires cross-functional collaboration |
| Adoption Activities | Communicating AI value and use cases to employees. Supporting learning, gathering user feedback, enabling hands-on experiences |
| Scaling Adoption | Moves beyond pilot programs to consistent, enterprise-wide AI usage. Focuses on ongoing engagement and enablement — explicitly NOT one-time training events |

> **Exam trick:** a scenario describing a hugely successful AI pilot in one department, with no mention of what happens next, is testing whether you know adoption isn't "done" at pilot success. Scaling Adoption is a distinct, ongoing phase.

> **Exam trick #2:** IT managing the technical rollout of an AI tool is NOT the same as IT owning the adoption program. Adoption requires business (value communication), IT (technical enablement), security, and compliance all sharing ownership.

## Deep dive: Adoption Team vs. AI Council (Module 7)

| | AI council (Module 7) | Adoption team |
|---|---|---|
| Role | Sets strategy and governance — the "what" and "why" | Drives day-to-day usage — translates strategy into real behaviour change |
| Composition | Business, IT, legal, security, compliance | Business units, IT, security, compliance — cross-functional, ongoing, never a one-time rollout |
| Timeframe | Sets policy periodically, with review cycles | Continuous — communication, training, feedback, hands-on support never stop |

> **Exam trick:** low usage or confusion in a scenario signals a missing/weak Adoption Team, not a governance problem. The Council can have perfect policy written down and adoption can still fail if no one is doing the day-to-day change management.

## Deep dive: the 6-phase rollout

| Phase | What happens |
|---|---|
| 1. Define strategy & metrics | Set goals and how success will be measured before rollout starts |
| 2. Secure data first | Audit permissions & sensitivity labels BEFORE wide rollout — deliberate ordering, tested directly |
| 3. Pilot small group | Test with a limited, controlled group first |
| 4. Measure & feedback | Collect real usage data and user feedback from the pilot |
| 5. Refine & scale in waves | Adjust based on feedback, then roll out in stages — not all at once. Where Scaling Adoption actually happens |
| 6. Monitor usage & outcomes | Ongoing tracking after rollout — adoption is never "done" |

ELI10: Phase 3 (Pilot Small Group) is planting the first seed, Phase 5 (Refine & Scale in Waves) is planting the rest of the garden in stages, and Phase 6 (Monitor Usage & Outcomes) is the watering that never stops.

> **Exam trick:** "Secure data first" is Phase 2, deliberately BEFORE the pilot in Phase 3 — a scenario that pilots first and audits permissions later has the order backwards.

## Deep dive: barriers to adoption & AI champions

| Barrier category | Examples |
|---|---|
| People-related | Fear of job replacement, low confidence, lack of training |
| Process & integration | AI disrupts workflows, unclear guidance |
| Trust & risk | Privacy, accuracy, reliability, bias concerns |
| Leadership & alignment | No clear ownership, no executive sponsorship |

> Resistance is the most common barrier. Low usage = adoption failure, not capability failure. If uptake is poor, the fix is change management — never "buy a better model."

**The 4 barrier categories, expanded:**

- **People-Related** — core driver: resistance, fixed only with proactive change management, never a better model. Bank example: a loan officer avoids the new AI drafting tool because she worries it signals she's "being replaced" — the tool works fine, she just never opens it.
- **Process and Integration Gaps** — core driver: the AI doesn't fit how work actually gets done. Bank example: a risk-flagging tool requires staff to log into a separate system and manually copy data across, adding steps to what used to be one click — so staff quietly go back to the old way.
- **Trust and Risk Concerns** — core driver: low trust stops people using a tool even when they technically have it — access isn't the same as adoption. Echoes Module 7's Inclusiveness standard, except the blocker here is psychological. Bank example: every compliance officer has a licence for the AI research assistant, but usage stays near zero because they don't trust it not to fabricate a regulatory citation.
- **Leadership and Alignment Issues** — core driver: without a visible, unified leadership stance, adoption fragments. Bank example: the CTO announces AI tools are "strongly encouraged," while a regional manager separately tells her branch "hold off until we're sure it's compliant" — staff get conflicting messages and default to doing nothing.

> **Memory trick:** People (won't), Process (can't easily), Trust (don't believe they should), Leadership (no one's telling them to).

**AI champions** are respected practitioners and early adopters — explicitly NOT senior leaders or IT staff. They extend, but never replace, the Adoption Team or governance.

Analogy: champions are the neighbours down the street who already have a beautiful garden and happily show others how they did it — not the city council (that's the AI Council) and not the garden centre staff (that's IT).

**Purpose of an AI Champions Program** — a formal program, not just informal peer encouragement, existing specifically to normalise AI usage and reduce hesitation.

**Champion activities:** sharing real use cases (practical proof, not theory), helping coworkers get started (hands-on, first-prompt-together support), collecting field feedback (noticing recurring friction and passing it upward). All three are experience-driven and practical — explicitly NOT governance or policy.

**The bridge mechanism:** champions bridge users and leadership, making adoption issues visible and actionable — a feedback conduit upward (user friction → Champion → Adoption Team/Council → fix), not just encouragement outward.

> **Exam trap:** a scenario where a Champion drafts or approves a usage policy is testing whether you know that's outside their lane — policy authorship stays with the AI Council, always. A Champion surfacing feedback that *leads to* a policy change is correct; a Champion *writing* the policy is not.

## Deep dive: licensing decision tree (Copilot vs. Azure AI)

**Two separate systems, same underlying maturity logic:**

| System | Who it's for |
|---|---|
| Copilot licensing | End users doing everyday productivity work (drafting, summarising) |
| Azure AI subscriptions | Developers/workloads — AI applications running in production, not people clicking a Copilot button |

> **Exam trap:** don't mix the two systems — a scenario about a developer building a RAG pipeline needs Azure AI language, not Copilot licensing tiers.

**Copilot licensing — the three tiers:** Included with M365 (baseline, no extra cost, best for org-wide exposure); Pay-As-You-Go (flexible, consumption-based, best for pilots/variable usage); Monthly Licensing (predictable per-user cost, best once a role relies on Copilot daily). Progression logic: early exploration → Included/PAYG; targeted, consistent roles → Monthly.

**Azure AI subscriptions — the two tiers:** Pay-As-You-Go (usage-based, best for experimentation/unpredictable demand); Prepaid/Commitment tier (committed capacity, predictable cost, best for steady production workloads). Same maturity logic: experimentation → PAYG; steady production → Prepaid.

**Cost Governance — the thread that ties both systems together:** subscription models ARE the governance tool, not something bolted on top. The exam tests awareness of cost management, not specific pricing details — you'll be asked to reason about which tier fits which situation.

> **The trap:** a scenario where AI usage gets *restricted* to save money is a governance FAILURE. Correct governance manages the *shape* of spend as usage scales, never the *existence* of usage.

## Deep dive: adoption impacts & licensing

**Impacts of AI adoption — second-order effects to plan for as adoption grows:**

| Impact area | What changes |
|---|---|
| Data | Greater reliance on high-quality, well-governed data; exposes existing gaps. AI surfaces what used to sit unnoticed |
| Security | Expanded risk surface — identity-based access controls and data leakage prevention become critical, ongoing not one-time |
| Privacy | AI may process personal, confidential, or regulated data in new contexts. Privacy policies specifically must be updated |
| Cost | Consumption-based pricing scales with usage, so success (high adoption) directly increases spend. Cost governance means actively managing experimentation vs. production spending — NOT avoiding or restricting AI use |

**Bank example — Data:** a shared drive has outdated permissions from a departed contractor's old account. Nobody noticed for years. Once an AI assistant can surface that drive's contents in a chat response, the old gap becomes an active leak. This is why rollout Phase 2 ("Secure data first") exists BEFORE piloting.

**Security vs. Privacy — same underlying data, two different lenses:** Security asks "is this technically exposed?" Privacy asks "does how AI now uses this data still match what our policy promised?" A scenario can trigger one without the other.

> **Exam trap — cost governance:** if a scenario implies an organisation "limited/restricted AI usage to control costs," that is describing a GOVERNANCE FAILURE, not a success. Correct cost governance = managing how spend scales — never discouraging adoption itself. Memory trick: "Govern the spend, not the use."

**Copilot licensing by adoption stage:**

| Copilot licensing | Best for |
|---|---|
| Included with M365 | Early exploration, low barrier |
| Monthly per-user | Daily use, core productivity roles |
| Pay-as-you-go | Pilots, variable usage |

**Azure AI/Foundry subscription models** (separate from Copilot licensing):

| Model | Best for |
|---|---|
| Pay-as-you-go | Usage-based, flexible — experimentation and variable demand |
| Prepaid / commitment tier | Committed usage, predictable cost — steady production workloads |

> **Exam trick:** organisations typically move from pay-as-you-go to prepaid as usage stabilises — this maturity signal mirrors Scaling Adoption itself. Subscription models are part of cost governance, not just billing.

## When used

Whenever a scenario describes AI tools being deployed but not effectively used, a successful pilot with unclear next steps, low usage/confusion despite good governance, or a question about who is responsible for day-to-day AI behaviour change across an organisation.

## Key differences

This page is the "execution" companion to the Module 7 Responsible AI & Governance page. The AI Council sets the rules; the Adoption Team gets people to follow them; Scaling Adoption is what keeps that effort alive after an initial pilot succeeds.

## Exam focus

**Must know:** adoption is never a one-time rollout. Scaling Adoption specifically means moving beyond pilot success to consistent, enterprise-wide, ongoing usage.

> **Exam trick:** a scenario mentioning "governance" or "monitoring" alone doesn't point to the AI Council if the actual problem is people not following an already-clear policy — that's an Adoption Team gap, specifically a Scaling Adoption gap if the issue is that a successful pilot was never expanded.

## Common confusion

People assume a successful pilot equals successful adoption. It doesn't — a pilot proves the tool CAN work; Scaling Adoption is the separate, ongoing job of making it work everywhere, continuously. People also assume IT can own adoption since it manages the technical rollout — adoption requires shared ownership across business, IT, security, and compliance.

## Memory trick

> "One flower isn't a garden." A successful pilot is one flower. Scaling Adoption is planting, watering, and weeding the whole garden — forever, not just on planting day.

## Practice questions

**Question 1.** A bank runs a wildly successful 3-month AI pilot in its customer service team, then moves on to the next project without expanding it further. Is this Scaling Adoption done well, or a gap?
**Answer:** A Scaling Adoption gap — one team doing well is not the same as the organisation having adopted AI.

**Question 2.** True or false: since IT usually manages the technical rollout of AI tools, it's acceptable for IT to own the adoption program on its own.
**Answer:** False. Adoption structurally requires shared ownership across business, IT, security, and compliance.

**Question 3.** Name the 6 phases of the adoption rollout, in order.
**Answer:** 1) Define strategy & metrics, 2) Secure data first, 3) Pilot small group, 4) Measure & feedback, 5) Refine & scale in waves, 6) Monitor usage & outcomes.

**Question 4.** Who staffs an AI champions program — and who is explicitly excluded?
**Answer:** Respected practitioners and early adopters staff it; senior leaders and IT staff are explicitly excluded — grassroots influence, not a mandate from above.

**Question 5.** True or false: cost governance in the context of AI adoption means limiting or discouraging AI usage to control spending.
**Answer:** False. Restricting AI usage to save money is a governance failure. Correct cost governance manages how spend scales — never the existence of usage.

## Related concepts

Responsible AI: Importance, Governance & the AI Council
