# Module 3 — Grounding: Business Requirements

> **Golden rule:** grounding only works in business if the data feeding it is trustworthy, well-architected, and properly governed — good grounding = good library + good search engine + good lock on the door.

## Identify business requirements for grounding solutions

**What it means:** this isn't "what is grounding" (you already know that) — it's what a business needs in place to actually implement grounding successfully. Think of it as the checklist you'd hand to a project team before switching on a grounded AI system.

**Explain like I'm 10:** grounding is like giving your AI a reference library instead of making it guess from memory. But before you build that library, you need to ask: is the library organised? Is it accurate? Who's allowed to read which shelf?

**Real-world analogy:** imagine hiring a new employee (the AI) and giving them access to your company's internal wiki so they answer customer questions correctly. Business requirements = making sure that wiki is (1) accurate & well organised, (2) built with proper search/retrieval, (3) access-controlled per company policy.

**Example:** a bank wants a grounded chatbot to answer "what's my current mortgage rate?" Requirements: rate sheets must be current & structured (data source), a retrieval system must fetch the right rate table (architecture), and only authorised data can be surfaced to comply with financial regulations (governance).

## How it works — 3 requirement categories

| Category | What's needed |
|---|---|
| Data Source Requirements | Accurate, current, well-structured source data (knowledge bases, docs, policy manuals, FAQs) |
| Architecture Considerations | Search/vector index → retrieval step → generation step (this is the RAG pipeline) |
| Compliance & Governance | Controls over what organisational data can be accessed/exposed — critical when grounding on internal data |

## When is it used?

Any time an organisation plans to ground a GenAI solution on their own data (not public web data). Exam context: this usually appears as a "what should you check BEFORE deploying a grounded solution" scenario question.

## Key differences

**Grounding (concept)** = the technique itself (connect AI to trusted external data). **Business requirements for grounding** = the planning/readiness checklist an organisation must satisfy to do it properly.

Note: the "Architecture Considerations" (search index → retrieval → generation) is literally the RAG pattern — confirming RAG is the implementation mechanism for grounding.

## Exam focus

**High priority:** if a scenario mentions "internal/organisational data" + grounding → compliance & governance is almost always the answer being tested.

**Medium priority:** recognising the 3-part architecture (index → retrieval → generation) as it maps back to RAG.

**Lower risk:** just knowing "grounding needs good data" — expect deeper scenario questions, not definitions.

## Exam keywords

Data source requirements, architecture considerations, compliance & governance, trusted external data, retrieval, vector index, organisational data.

## Common confusion

Don't confuse this with fine-tuning readiness — fine-tuning needs labelled training data; grounding needs searchable, accurate reference data. Governance ≠ just "data quality" — it specifically means controlling who/what can access sensitive organisational data through the AI.

## Memory trick

> "SAC" — Source data → Architecture → Compliance. Or: "Good grounding needs a Good Library, a Good Search Engine, and a Good Lock on the door."

## Quick quiz

**Question 1.** A company wants to ground its AI on internal HR policies. Which requirement category ensures employees can't see other employees' confidential salary data through the chatbot?
**Answer: C — Compliance & Governance.** This category specifically controls who/what can access sensitive organisational data through the AI. Data Source Requirements is about accuracy/structure, not access control; Architecture Considerations covers the retrieval pipeline, not permissions; fine-tuning readiness isn't part of grounding at all.

**Question 2.** True or false: the "retrieval step" mentioned in Architecture Considerations is the same core mechanism as RAG's retrieval component.
**Answer: True.** The 3-part architecture (search index → retrieval step → generation step) is literally the RAG pattern — confirming RAG is the implementation mechanism behind grounding's Architecture Considerations.

## Related concepts

Retrieval Augmented Generation (RAG) · Selecting a Generative AI Solution for a Business Need
