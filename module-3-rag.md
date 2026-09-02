# Module 3 — Retrieval Augmented Generation (RAG)

> **Golden rule:** RAG doesn't teach the model new things — it hands the model the right document at question-time so it can answer using facts it was never trained on.

## What is it?

RAG (Retrieval-Augmented Generation) is a technique that lets a generative AI model answer questions using current, external, or organisation-specific information — without retraining the model. Instead of relying only on what the model learned during training, RAG retrieves relevant documents at the moment of the question, adds them to the prompt, and then the model generates an answer grounded in that retrieved content.

RAG is built from three core components: an **embedding model** (turns text into searchable vectors), a **vector/search index** (stores and searches those vectors), and a **language model** (writes the final answer using what was retrieved).

## Explain like I'm 10

Imagine a very smart friend who has read a huge number of books — but hasn't read today's newspaper. If you ask them about today's news, they won't know. RAG is like handing that friend today's newspaper right before they answer your question. They're still using their own intelligence to explain it well — they just now have the right, current information in front of them.

## Real-world analogy — the open-book exam

A model answering without RAG = a student sitting a closed-book exam, relying only on what they memorised. A model answering with RAG = a student sitting an open-book exam: they can look up the exact right page before answering. The student (model) is still the one writing the answer — RAG just lets them check the right source first.

## Real-world example

**Situation:** an employee asks the bank's AI assistant, "What does our current lending policy say about overseas transfers?"

**Problem:** the model was trained months ago and has no idea what today's lending policy says — policies change and the model can't know that from training alone.

**How this concept solves it:** RAG searches the bank's internal policy documents, retrieves the current lending policy section, adds it to the prompt, and the model generates an accurate answer based on that retrieved, up-to-date text — often with a citation back to the source document.

## How does it work?

**Step 1 — Question:** the user asks a question.
**Step 2 — Retrieve:** the system searches a trusted knowledge base/document store for the most relevant content.
**Step 3 — Augment:** the retrieved content is added into the prompt sent to the model.
**Step 4 — Generate:** the model writes an answer using both its own language ability and the retrieved facts.

Question → retrieve → augment prompt → generate answer.

**3 common RAG patterns — escalating levels of retrieval intelligence:**

| Pattern | Meaning | Giveaway phrase |
|---|---|---|
| Basic RAG | One retrieval step, then generate — like a vending machine: press one button, get one item | "One question, one lookup, one answer" |
| Multi-step / iterative RAG | Retrieves multiple times, usually the same type of source, to gather or refine enough info before answering (e.g. comparing 2024 vs. 2025 policy — both retrievals hit the same document store) | "Needs multiple lookups to compare/refine" (source type stays the same) |
| Agentic RAG | The model actively decides, on its own judgment, which tool/source to query — potentially different tool types (e.g. checking an internal report store AND an external database) | "Dynamically decides", "automatically switches source/tool" |

> **Exam trick:** a scenario can *look* like Multi-step RAG because "multiple lookups" happened — but if the AI automatically switches to a different tool/source type based on what it finds (not just retrieving more of the same kind), that's Agentic RAG, not Multi-step.

**Retrieval strategies** (quality of retrieval drives quality of the whole RAG system): semantic/vector search (finds meaning-based matches, not just exact words); keyword/hybrid search (combines exact keyword matching with semantic search); reranking (happens after retrieval, before generation — retrieves a wide set, e.g. top 20, then re-scores/reorders down to the most relevant few, e.g. top 3, so only the best passages reach the model).

> **Common trap:** reranking is NOT a pre-retrieval step. Order is always: retrieve (wide) → rerank (narrow) → generate.

## When is it used?

Use RAG when the AI needs to answer using current/frequently changing information (policies, prices, live data); organisation-specific or internal documents the model was never trained on; situations where traceability/citations back to a source document matter; or cases where retraining the model for every update would be too slow or expensive.

## Key differences

> **Key difference:** grounding is the broader business goal (accurate, current, trustworthy answers) — RAG is the specific, most common technique used to achieve it.

| | Grounding | RAG |
|---|---|---|
| What it is | The goal/requirement: answers must be accurate, current, trustworthy | A specific technique that retrieves documents to help achieve grounding |
| Scope | Broader concept — can be achieved multiple ways | One method (the most common one) of achieving grounding |
| Easy memory | "The WHY / the requirement" | "The HOW / the tool" |

| | RAG | Fine-tuning |
|---|---|---|
| Main purpose | Provide relevant, current knowledge | Change behaviour / style / format |
| Data used | External/organisational documents, searched live | Training examples, baked in during training |
| Easy memory | "WHAT it knows" | "HOW it behaves" |

## Can RAG + fine-tuning be combined?

> **Key point:** yes — RAG and fine-tuning are not either/or. They solve different problems, so they can be used together on the same model.

RAG does not require a plain pretrained model — it can sit on top of a fine-tuned model too. RAG = gives the model WHAT to know (current facts/documents). Fine-tuning = changes HOW the model behaves (tone, style, format). Because they affect different things, a bank can fine-tune a model to always write in its house style, and still use RAG on that same model to pull in today's actual policy numbers.

> **Exam signal:** if a scenario needs BOTH a consistent specialised style AND current organisational facts, the correct answer is often fine-tuning + RAG together — not a choice between them.

## Exam alert

**Must know:** RAG = Retrieve → Augment → Generate. RAG lets a model use current/organisation-specific info without retraining. RAG is the most common technique used to achieve grounding. "Use our current/internal/company documents" in a question → think RAG.

**Should know:** RAG's 3 core components — embedding model, vector/search index, language model. RAG can provide citations back to source documents — fine-tuning cannot. RAG and fine-tuning are not mutually exclusive. Grounding deployment needs 3 things: good data sources, correct architecture (index → retrieve → generate), and compliance/governance controls.

**Nice to know:** 3 RAG patterns exist (Basic, Multi-step/iterative, Agentic). 3 retrieval strategies exist (semantic/vector search, keyword/hybrid search, reranking).

## Exam keywords

"Current internal policy / company-specific information" → RAG. "Answer must be accurate, trustworthy, and up to date" → grounding (RAG is how you achieve it). "Provide citations / traceable sources" → RAG. "Without retraining the model" → RAG.

## Common confusion

Many people confuse RAG with grounding because they're taught together. The difference: grounding is the requirement ("the answer must be accurate and current"), while RAG is one specific technique used to satisfy that requirement. People also confuse RAG with fine-tuning because both "customise" a model's output — but since they target different things, a single solution can use both at once.

## Memory trick

> RAG = Retrieve → Augment → Generate. Grounding = the WHY. RAG = the HOW. Open-book exam, not closed-book.

## Practice questions

**Question 1.** An employee asks a company chatbot about a policy that was updated yesterday. Which approach best ensures the chatbot's answer reflects the update, without retraining the model?
**Answer: C — use RAG to retrieve the current policy document at question-time.** RAG retrieves the most current document at the moment of the question, so the answer reflects yesterday's update immediately — no retraining needed.

**Question 2.** True or false: grounding and RAG mean exactly the same thing, and the two terms are interchangeable in every case.
**Answer: False.** Grounding is the broader business requirement that answers be accurate, current, and trustworthy. RAG is the specific, most common technique used to achieve grounding — but not the only possible way.

## Related concepts

Grounding · Pretrained vs Fine-Tuned Models · Selecting a Generative AI Solution for a Business Need · Generative AI
