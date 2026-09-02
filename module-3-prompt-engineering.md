# Module 3 — Prompt Engineering

> **Golden rule:** prompt engineering is the cheapest, fastest lever to improve an AI solution — always try it before fine-tuning or switching models. Clear prompts in = outputs closer to right on the first attempt out.

## What is it?

Prompt engineering is the practice of deliberately structuring your inputs to guide AI output — defining role and constraints, writing clear instructions, and optionally adding examples or reasoning guidance. It's rung 1 on the Customisation Ladder because it changes nothing about the model itself — only what you feed it.

## Explain like I'm 10

Imagine asking a friend to draw you a picture. If you just say "draw something," you might get anything. But if you say "draw a red dog sitting on a green hill, cartoon style, using only 3 colours" — you'll get something much closer to what you wanted, on the first try. That's prompt engineering: giving clearer instructions so you don't have to ask again.

## Real-world analogy — ordering coffee

- **Vague prompt** = "Can I get a coffee?" → you might get anything, and probably have to send it back
- **Engineered prompt** = "A flat white, oat milk, one sugar, extra hot, in a takeaway cup" → you get exactly what you wanted, first time, no back-and-forth

Every time you have to "send it back" (rework), that's wasted time and money — just like rework cycles with AI outputs.

## Real-world example

**Situation:** a bank employee asks an AI assistant to "write a customer email."

**Problem:** vague prompt → the AI has to guess the tone, length, and content, so the output is often unusable and needs a full rewrite.

**How prompt engineering solves it:** instead, the employee writes: "You are a customer service specialist at a bank. Write a concise, professional email (under 150 words) informing a customer their loan application has been approved. Include next steps and a friendly closing." Now the output is close to right on the first attempt — reduced rework, reduced token waste from repeated tries.

## How does it work?

What prompt engineering actually involves: defining role and constraints ("You are a [role], respond in [format/length/tone]"); writing clear instructions; optionally adding examples (zero/one/few-shot); optionally adding reasoning guidance (asking the model to think step-by-step before answering).

The business impact — measurable, not just "nice to have": quality & consistency (better structured prompts lead to more reliable outputs); cost optimisation (every token in a prompt costs money; inefficient/vague prompts waste tokens and often require multiple costly retries); reduced rework cycles (outputs land closer to "right" on the first attempt).

## When is it used?

Always try this first. Before reaching for fine-tuning, RAG, or a different (often more expensive) model, prompt engineering is the cheapest, fastest lever to pull — rung 1 of the Customisation Ladder: ASK (prompting) → GIVE (RAG) → TEACH (fine-tuning) → BUILD (custom model). Watch for signals like inconsistent tone, wrong length, missing structure, or rework/retry patterns — these point to a prompting fix, not a bigger model or RAG.

## Key differences

> **Key difference:** prompt engineering changes nothing about the model itself — it only changes what you feed it.

| | Prompt engineering | Fine-tuning |
|---|---|---|
| What changes | Nothing about the model — just the input | The model itself, through extra training |
| Cost | Cheapest, fastest, no setup | Slower, costlier, more setup |
| When to use | Always try first | Only when prompting alone can't meet the need |
| Easy memory | "Ask better" | "Teach it HOW" |

> **Key difference:** missing facts vs. missing structure — don't confuse the fix.

| Symptom | Root cause | Fix |
|---|---|---|
| Inconsistent tone/length, missing structure | Unclear instructions | Prompt engineering |
| Outdated or missing facts | Model doesn't know the info | RAG / Grounding |

## Exam alert

**Must know:** prompt engineering = deliberately structuring inputs (role, constraints, clear instructions, examples, reasoning guidance). It directly impacts quality, consistency, and cost. It's the first step to try before fine-tuning or switching models. Every token in a prompt costs money — inefficient prompts increase cost through both token waste and rework retries.

**Should know:** "reduced rework cycles" is the key business-impact phrase. Structured prompts/templates help standardise outputs across users and scenarios.

**Nice to know:** connects directly to the customisation ladder's rung 1 — the foundation everything else builds on.

> **Exam trick:** if a scenario describes AI outputs being inconsistent or requiring lots of rework, don't jump straight to "fine-tune the model" or "use a different model." Check whether the symptom is missing structure/clarity (→ prompting) versus missing facts (→ RAG) before picking a fix.

## Exam keywords

"Outputs vary in tone/length/format" → prompt engineering. "Rework, retries, inconsistent quality" → prompt engineering first. "Every token costs money" → prompt engineering (efficient prompts reduce cost). "Missing or outdated facts" → RAG/grounding, not prompting.

## Common confusion

People often reach for RAG or fine-tuning the moment an AI output looks "wrong," without checking whether the real problem is just an unclear prompt. If the model has the right information but presents it inconsistently, that's a structure problem — prompt engineering fixes it. If the model doesn't have the right information, no amount of prompting will fix that — that's when RAG comes in.

## Memory trick

> CLEAR IN → CLOSER TO RIGHT OUT. Better prompts = fewer retries = lower cost = the FIRST lever to pull, always.

## Practice questions

**Question 1.** A marketing team's AI-generated product descriptions swing between overly formal and overly casual, and vary wildly in length. What should they try FIRST?
**Answer: C — improve prompt engineering, specifying tone, length, and format constraints.** Swinging tone and inconsistent length is a clarity/structure problem, not a missing-facts problem, and this fix costs nothing extra. Fine-tuning is only considered after prompting fails; RAG solves missing/outdated facts, not tone/length; a bigger model without clear instructions will still guess.

**Question 2.** True or false: prompt engineering changes the underlying model's behaviour permanently, the same way fine-tuning does.
**Answer: False.** Prompt engineering doesn't touch the model — it only changes what you feed into it, so its effects only last for that interaction. Fine-tuning is what permanently changes the model's behaviour through additional training.

## Related concepts

The Customisation Ladder · Pretrained vs Fine-Tuned Models · Retrieval Augmented Generation (RAG) · Selecting a Generative AI Solution for a Business Need
