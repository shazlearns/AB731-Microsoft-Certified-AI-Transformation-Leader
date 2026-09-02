# Module 1 — Pretrained vs Fine-Tuned Models

> **Golden rule:** a pretrained model already knows a lot about everything — a fine-tuned model knows a little extra about *your* specific thing. Fine-tuning = pretrained model + extra specialised training.

## What is it?

Every large language model starts life as a **pretrained model** — trained on a huge, general dataset (books, websites, code, articles) so it develops broad language and reasoning ability.

**Fine-tuning** takes that already-smart pretrained model and trains it further on a smaller, specific dataset, so it becomes better at a narrower task, tone, or format — without starting from zero.

This is only possible because of **transfer learning**: the idea that knowledge learned on one broad task "transfers" and gives the model a head start on a new, narrower task — so fine-tuning is fast and cheap compared to training a model from scratch.

## Explain like I'm 10

Imagine a university graduate who studied everything — history, maths, writing, science. That's the pretrained model: broadly smart, ready to help with almost anything, straight away. Now imagine that same graduate does a 3-month specialist course to become a hospital receptionist — learning hospital terms, forms, and tone. That's fine-tuning. They didn't relearn how to read and write from scratch — they built on what they already knew.

## Real-world analogy — the new hospital hire

- **Pretrained model** = a smart new hire on day one — general knowledge, no hospital-specific training yet.
- **Fine-tuning** = onsite training on this hospital's exact forms, terminology, and tone.
- **Fine-tuned model** = that same hire, now trained specifically for this hospital's way of doing things.

They didn't hire a new person (train from scratch) — they trained the person they already had (transfer learning).

## Real-world example

**Situation:** a bank wants an AI assistant that always writes risk reports in the bank's exact internal format, tone, and terminology.

**Problem:** a general-purpose pretrained model writes well, but not consistently in the bank's specific house style.

**How this concept solves it:** the bank fine-tunes the pretrained model on examples of its own past risk reports. The model keeps all its general language ability, but now reliably matches the bank's required style and structure.

## How does it work?

1. Start with a pretrained model (already trained on massive general data).
2. Collect a smaller, task-specific training dataset (e.g. the bank's own past reports).
3. Continue training the model on this specific dataset — adjusting it, not rebuilding it.
4. The model keeps its general knowledge, but now performs the specific task more accurately and consistently.

Pretrained model → + specific training data → fine-tuned model.

## When is it used?

Use a pretrained (general-purpose) model as-is when the task is broad and the model already performs well enough, or you need something working quickly with minimal setup.

Use fine-tuning when you need specialised behaviour, tone, style, terminology, or output format; the same specialised task will be repeated often, so consistency matters; or general-purpose output isn't precise or consistent enough for the use case.

## Key differences

> **Key difference:** fine-tuning changes HOW the model behaves — it does not give the model new live facts.

| Concept | What it is | Speed / cost | Easy memory |
|---|---|---|---|
| Pretrained model | General-purpose model, used as-is | Fast, cheap, ready now | "Off the shelf" |
| Fine-tuned model | Pretrained model + extra specific training | Slower, costlier, more setup | "Tailored to me" |

## Exam alert

**Must know:** fine-tuning = pretrained model + additional specific training (not built from scratch). Fine-tuning changes behaviour, style, tone, terminology, format — not live facts. Fine-tuning is not the way to give a model current company data — that's RAG/grounding.

**Should know:** transfer learning is the underlying principle that makes fine-tuning fast and efficient. Fine-tuning needs a smaller, task-specific dataset compared to full pretraining.

**Nice to know:** fine-tuning adds ongoing maintenance overhead (retraining as needs evolve).

## Exam keywords

"Consistently follow a specific tone, style, or format" → fine-tuning. "Ready to use immediately, broad task, minimal setup" → pretrained/general-purpose model. "Give the model our current internal facts/documents" → RAG, not fine-tuning. "Builds on existing model knowledge rather than starting over" → transfer learning.

## Common confusion

Many people confuse fine-tuning with RAG because both "customise" a model. The difference: fine-tuning changes HOW the model behaves (baked into the model through extra training); RAG changes WHAT the model knows at answer-time (retrieves live documents rather than retraining anything). A fine-tuned model does not automatically know new facts — it just responds differently.

## Memory trick

> Pretrained = general graduate. Fine-tuned = graduate + specialist course. Fine-tuning = HOW it behaves, not WHAT it knows.

## Practice questions

**Question 1.** A bank wants its AI assistant to always respond in a very specific, formal internal reporting style used only at this bank. Which approach best fits?
A) Use a general-purpose pretrained model as-is B) Fine-tune a pretrained model on examples of the bank's own reports C) Apply RAG to retrieve the bank's report archive D) Train a brand-new model from scratch
**Answer: B.** This is a behaviour/style/format need, which is exactly what fine-tuning solves — and it builds on an existing pretrained model rather than starting over. A) won't reliably match house style; C) RAG supplies facts/documents, not a writing style; D) training from scratch is unnecessary and expensive when transfer learning lets you build on an existing model.

**Question 2.** True or false: fine-tuning a model is the best way to make sure it always has today's most current internal policy information.
**Answer: False.** Fine-tuning bakes behaviour into the model at training time — it doesn't update in real time. Current/live facts should come from RAG or grounding, retrieved at the moment of the question. A fine-tuned model's "knowledge" is frozen at the point it was fine-tuned.

## Related concepts

Transfer Learning · Retrieval Augmented Generation (RAG) · Grounding · Selecting a Generative AI Solution for a Business Need · Generative AI
