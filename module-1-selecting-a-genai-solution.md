# Module 1 — Selecting a Generative AI Solution for a Business Need

> **Golden rule:** start with the business need, not the AI technology. Choose the simplest solution that meets the requirement, then balance cost, quality, speed, data sensitivity, and maintenance.

## 1. Evaluate the business requirement

Ask three questions:
1. **What is the problem?** What task needs to be automated or augmented?
2. **How complex is the task?** Structured/rule-based (clear, predictable logic) vs. open-ended/creative (language, content, summarisation, drafting)?
3. **Is the data sensitive?** Does the solution handle confidential, internal, financial, or regulated information? For a bank, this affects security, privacy, governance, and where data is processed.

## 2. Match the business need to the AI approach

| Business need | Think | Example |
|---|---|---|
| Create content | Generative AI | Write a customer email or summarise a report |
| Predict / classify / detect | Traditional ML | Estimate fraud probability |
| Converse using company information | GenAI + RAG / grounding | Answer questions using current internal policies |
| Follow fixed rules | Rule-based AI | Apply a clearly defined claims policy |

> **Memory shortcut:** CREATE → GenAI. PREDICT → ML. CONVERSE + COMPANY DATA → GenAI + RAG.

## 3. Choose the level of customisation — the Customisation Ladder

Climb only as far as you need. Start at rung 1; only move up if the current rung genuinely can't solve the problem.

1. 🟢 **Prompt engineering** — just write better instructions to the same model
2. 🔵 **RAG / Grounding** — give it current/organisational facts to reference
3. 🟡 **Fine-tuning** — teach it a specific behaviour, tone, or format
4. 🔴 **Train your own model** — build a brand-new model from scratch (rare, last resort)

**Analogy — ordering food:** prompt engineering = asking the waiter for "no onions, extra spicy" (better instructions, same kitchen). RAG = handing the chef today's fresh ingredient list. Fine-tuning = sending the chef to a course to permanently cook in your specific style. Training your own model = building your own restaurant from the ground up.

**General-purpose model = USE.** Use the model as-is when the task is broad and it already performs well enough. Example: "Summarise this document in five bullet points." Best clue: broad task + quick setup + minimal customisation.

**Fine-tuned model = BEHAVE.** Fine-tuning helps with specialised behaviour, style, terminology, or output format. Example: consistently producing internal risk reports in a specific structure and terminology. Important: fine-tuning is not primarily the way to give a model a database of current company facts. Remember: fine-tuning = teach it HOW.

**RAG-enhanced solution = KNOW.** Give the model trusted information to reference when answering. RAG = Retrieval-Augmented Generation. How it works: question → search the organisation's trusted documents → retrieve relevant information → generate an answer using that information. Example: an employee asks, "What does our current lending policy say?" Remember: RAG = give it WHAT to know.

| | Fine-tuning | RAG |
|---|---|---|
| Main purpose | Change behaviour / style / format | Provide relevant knowledge |
| Uses | Training examples | External or organisational documents/data |
| Best for | Specialised behaviour and terminology | Current or company-specific information |
| Memory trick | HOW | WHAT |

## 4. Understand the trade-offs

**Cost vs. accuracy:** a more capable model generally costs more. You do not automatically choose the biggest model — choose the simplest model that meets the business requirement.

**Speed vs. quality:** a smaller model is faster and often cheaper but may sacrifice depth; a larger model may be better quality but slower and more expensive. Ask: does this process need maximum quality, or is speed more important?

**Customisation vs. maintenance:** more customisation means more setup, which means more ongoing effort/cost. Fine-tuning adds upfront work and requires ongoing updates as requirements change.

## 5. One banking scenario

**Business need:** employees spend too much time searching internal policies.
- Step 1 — define the problem: we need a conversational assistant for policy questions.
- Step 2 — assess complexity: open-ended language task → GenAI is appropriate.
- Step 3 — check the data: internal and potentially sensitive information → security + governance matter.
- Step 4 — choose the solution: the assistant needs current internal policies → GenAI + RAG.
- Step 5 — consider trade-offs: don't automatically choose the largest model — use one that provides sufficient quality at an acceptable cost and speed.

## AB-731 exam alert

If you see: "generate / write / summarise / create" → generative AI. "Predict / classify / detect / probability / score" → traditional ML. "Use our current / internal / company-specific information" → RAG / grounding. "Change behaviour / style / terminology / output format" → fine-tuning. "Fast / cheap / broad / minimal setup" → general-purpose model.

> **Common exam trap:** don't select the most advanced or expensive AI option just because it's more capable. The exam favours the simplest solution that meets the business need.

> **Ladder exam trick:** if a simple problem is described but "train a custom model from scratch" is offered as an option, it's almost always a distractor. The exam rewards restraint — pick the lowest rung on the customisation ladder that solves the stated problem, and remember rungs are additive (e.g. RAG + fine-tuning can be used together, not either/or).

## Final memory map

> General-purpose = USE. RAG = KNOW. Fine-tuning = BEHAVE. Traditional ML = PREDICT.
> Business need → choose AI type → choose customisation → balance trade-offs.

## Quick knowledge check

1. **A bank wants an AI to draft customer emails. What is the likely approach?** → Generative AI (content-creation task).
2. **A bank wants to estimate whether a transaction is fraudulent. What is the likely approach?** → Traditional ML (predict/classify/detect task).
3. **An employee asks an AI about the bank's current internal policy. What capability is especially useful?** → RAG/grounding — answering with current, internal information requires retrieving trusted documents at answer-time.
4. **The AI needs to consistently follow a specialised reporting style and format. What approach may help?** → Fine-tuning — a behaviour need (teach it HOW).
5. **The business need can be met by a smaller, cheaper model. Should you automatically choose the largest model?** → No. Choose the simplest solution that meets the requirement.
