# Module 2 — Cost Drivers in Generative AI Usage (Tokens, TCO, ROI)

> **Golden rule:** AI cost isn't one number — it stacks in layers: tokens (what you use) → infrastructure (what runs it) → TCO (the full bill) → ROI (was it worth it?). Never judge cost alone — always weigh it against value.

## What is it?

Every time you use a generative AI model, cost comes from several layers stacking together, not one flat fee. Four buckets: token economics, infrastructure costs, Total Cost of Ownership (TCO), and ROI. Understanding how these connect — and how they link to the Customisation Ladder — is essential for any "is this AI solution worth it?" question.

## Real-world analogy — your phone data plan

- **Tokens** = the actual data you use (more scrolling/streaming = more cost)
- **Infrastructure** = the phone towers, cables, and network gear making that data possible
- **TCO** = your total phone bill — data plan + device cost + add-ons
- **ROI** = "is having this phone plan actually worth what I'm paying?"

## Real-world example

**Situation:** a bank rolls out an AI assistant that summarises customer emails, and leadership wants to know if it's worth the money.
- **Tokens** — every email in + every summary out costs tokens; longer emails = higher cost per request
- **Infrastructure** — compute (GPU/TPU), storage, and networking running the model
- **TCO** — adding RAG (policy documents) or fine-tuning (house style) adds search-index costs, training compute, and retraining cycles on top of API costs
- **ROI** — compare hours saved per staff member × hourly cost, against the total TCO spend

## How does it work?

**1. Token economics** — tokens = the unit of AI consumption (input + output). 1 token ≈ ¾ of a word in English (~4 characters). Longer prompts and longer responses both mean higher cost per request.

**2. Infrastructure costs** — compute (GPU/TPU resources for inference and training), storage (training data, model weights, vector indexes), and networking (API calls, data transfer, latency optimisation).

**3. Total Cost of Ownership (TCO)** — per-token API costs (pay-per-use or reserved capacity), fine-tuning costs (data curation + training compute + retraining cycles), RAG infrastructure (search index, embedding generation, storage).

**4. ROI considerations** — time savings (hours saved per task × employee cost), productivity gains (more output per person, faster turnaround), quality improvement (consistency, accuracy, reduced rework).

## When is it used?

Whenever a scenario asks you to justify, budget for, or compare AI solutions. You're expected to weigh cost (tokens + infrastructure + TCO) against value (ROI) — never look at cost alone.

## Key differences

> **Key difference:** this directly links to the Customisation Ladder — the higher you climb, the more TCO layers stack up.

| Ladder rung | Extra cost it adds to TCO |
|---|---|
| Prompt engineering | None extra — just token cost |
| RAG / Grounding | Search index, embedding generation, storage |
| Fine-tuning | Data curation, training compute, retraining cycles |
| Train your own model | Massive compute, ongoing full retraining |

> **Key difference:** TCO is what you spend. ROI is whether what you spent was worth it.

| | TCO | ROI |
|---|---|---|
| Question it answers | "What does this cost?" | "Was it worth what it cost?" |
| Made up of | Tokens + infrastructure + fine-tuning + RAG | Time savings + productivity + quality |
| Easy memory | "The bill" | "The verdict" |

## Exam alert

**Must know:** tokens = input + output; longer prompts/responses = higher cost. TCO = API costs + fine-tuning costs + RAG infrastructure — not just the API bill. Never evaluate cost alone — always weigh it against ROI (time savings, productivity, quality). ROI = hours saved × employee cost + productivity gains + quality improvement, weighed against TCO.

**Should know:** 1 token ≈ ¾ of a word / ~4 characters. Infrastructure = compute + storage + networking. The customisation ladder directly drives TCO — higher rungs stack more cost layers.

**Nice to know:** reserved capacity vs. pay-per-use mirrors the Azure AI subscription models (pay-as-you-go vs. prepaid/commitment tier). Quality improvement is a valid ROI factor even without a precise dollar figure.

## Exam keywords

"Longer prompts/responses cost more" → token economics. "Compute, storage, networking" → infrastructure costs. "API + fine-tuning + RAG costs combined" → TCO. "Hours saved, productivity, quality vs. cost" → ROI. "Is the cheapest option always best?" → no — weigh cost against whether it meets the business need.

## Common confusion

Many people confuse token cost with TCO, treating the API price as the whole story. In reality, token cost is just one line item — TCO also includes fine-tuning and RAG infrastructure costs if those rungs of the customisation ladder are used. People also confuse cost with value: a cheap solution that doesn't meet the business need has bad ROI even though its TCO is low.

## Memory trick

> TOKENS (what you use) → INFRASTRUCTURE (what runs it) → TCO (total bill) → ROI (was it worth it?)
> Don't just ask "how much?" — ask "was it worth it?"

## Practice questions

**Question 1.** A company fine-tunes its model AND adds RAG. Which categories does this add to their TCO?
**Answer: B — data curation + training compute + retraining cycles (fine-tuning) and search index + embedding generation + storage (RAG).** Both stack on top of base token/API costs.

**Question 2.** True or false: a cheaper AI solution is always the better exam answer, regardless of whether it meets the business requirement.
**Answer: False.** The exam's governing rule is "choose the simplest solution that meets the business need" — not "choose the cheapest solution regardless of fit." Picking the cheapest option that fails the actual need produces poor ROI.

## Related concepts

The Customisation Ladder · Pretrained vs Fine-Tuned Models · Retrieval Augmented Generation (RAG) · Selecting a Generative AI Solution for a Business Need
