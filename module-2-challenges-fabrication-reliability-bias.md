# Module 2 — Challenges of Generative AI (Fabrication, Reliability, Bias)

> **Golden rule:** generative AI is powerful but not perfect: it can fabricate facts, give inconsistent answers, and reflect bias from its training data. Each risk has one primary mitigation — Fabrication → Grounding, Reliability → Content filtering, Bias → Human review.

## What is it?

Three core risks in generative AI — fabrication, reliability, and bias — and three mitigation strategies that address them. These aren't flaws to "fix" once; they're ongoing characteristics of how generative AI works that every solution must account for.

## Explain like I'm 10

Imagine a very confident friend who answers every question — even when they don't know the answer, they'll just make something up that sounds right. That's fabrication. Ask them the same question twice and they might answer slightly differently — that's reliability. And if they only grew up hearing one side of a story, their opinions will lean that way without realising it — that's bias.

## Real-world example

**Situation:** a bank's AI assistant is asked about a very obscure, rarely-discussed lending regulation.

**Problem:** the model wasn't trained on much data about this regulation, so it confidently generates an answer that sounds authoritative but is actually made up (fabrication). Ask the same question twice and you might get two different wrong answers (reliability). If the training data skewed toward one region's lending practices, the answer might unfairly reflect that region's norms (bias).

**How this gets solved:** ground the assistant in the bank's actual verified policy documents, filter out anything unsafe or biased before it reaches the user, and have a human review anything critical before it's acted on.

## The 3 challenges

**1. Fabrication (hallucination)** — the model generates plausible-sounding but factually incorrect content. It cannot tell the difference between what it actually "knows" and what it's inventing. More likely with obscure topics or highly specific questions.

**2. Reliability concerns** — non-deterministic: the same prompt can produce different outputs each time. Inconsistent quality across different topics and complexity levels. No guarantee of factual accuracy without validation.

**3. Bias in AI outputs** — training data reflects societal biases, so the model inherits them. Can produce outputs that favour or disadvantage certain groups. Geographic, cultural, gender, and racial biases are common.

## The 3 mitigations, matched to root cause

**1. Grounding** — connect the model to verified, authoritative data (RAG is the most common way). Fixes fabrication because the model no longer has to "guess" — it references real facts. Acts before generation.

**2. Content filtering** — blocks harmful, biased, or inappropriate outputs before they reach the user. Fixes reliability because it acts as a consistent safety net, catching bad outputs regardless of which version the non-deterministic model happened to generate. Acts after generation, screening the output.

**3. Human review** — a person validates critical outputs before they're published or acted on. Fixes bias because the model can't see its own blind spot — it takes a human with outside judgement to catch unfair patterns. Acts before publication/action, as a final check.

## When is it used?

Any scenario where the AI's output could mislead, harm trust, or unfairly treat a group — especially high-stakes business decisions, customer-facing content, or anything published without review. A mature solution layers all three mitigations together, since each defends against a different risk.

## Key differences

> **Key difference:** each risk has one primary mitigation the exam pairs it with — and each mitigation targets a different root cause.

| Risk | Looks like | Primary mitigation | Root cause targeted |
|---|---|---|---|
| Fabrication (hallucination) | Cites a source/fact that doesn't exist | Grounding | Model doesn't actually know the fact |
| Reliability | Same prompt, different quality each time | Content filtering | Output could be inconsistent/inappropriate |
| Bias | Outputs favour/disadvantage a group | Human review | Model can't see its own bias |

## Exam alert

**Must know:** the 3 risks — fabrication, reliability, bias. The 3 mitigations — grounding, content filtering, human review. The pairing: fabrication → grounding, reliability → content filtering, bias → human review. Generative AI is probabilistic, not deterministic — that's why reliability is a real concern.

**Should know:** fabrication is more likely with obscure or highly specific questions. Bias comes from the training data, not a flaw in the model's "reasoning." The three mitigations are complementary, not exclusive — a mature solution layers all three. Grounding connects directly to RAG.

**Nice to know:** geographic, cultural, gender, and racial bias are the most commonly cited bias categories on the exam.

> **Exam trick:** if a question describes a chatbot that's already grounded (connected to real data) but still gives wrong answers, don't jump to "add more grounding" or "bias." This is a retrieval quality issue — the model is behaving normally; the wrong data was retrieved.

## Exam keywords

"Cites a source that doesn't exist / plausible but wrong" → fabrication → grounding. "Same prompt, different output" → reliability → content filtering. "Outputs favour/disadvantage a group" → bias → human review. "Grounded system still gives wrong answers, model behaves normally" → retrieval quality issue, not a new risk.

## Common confusion

People often confuse fabrication with bias — both produce "wrong" outputs, but for different reasons. Fabrication is the model inventing facts it doesn't know. Bias is the model reflecting unfair patterns from data it does know. People also assume grounding alone guarantees correct answers — but if the wrong document is retrieved, a grounded system can still be wrong. That's a retrieval quality problem, not proof grounding failed as a concept.

## Memory trick

> FABRICATE → GROUND IT. UNRELIABLE → FILTER IT. BIASED → HUMAN-CHECK IT.

## Practice questions

**Question 1.** A model gives a confident, detailed answer about a very niche historical event — but the details turn out to be completely made up. What is this called, and what's the primary mitigation?
**Answer: C — fabrication (hallucination); mitigated by grounding.** The model invented plausible-sounding but false details about an obscure topic — textbook fabrication. Bias is about unfair patterns favouring/disadvantaging groups, not invented facts; reliability is about inconsistency between requests, not invented content itself.

**Question 2.** True or false: reliability concerns mean the model is broken and needs to be replaced.
**Answer: False.** Reliability concerns come from generative AI being non-deterministic by nature — an inherent characteristic to manage (via content filtering and validation), not a defect requiring replacement.

## Related concepts

Retrieval Augmented Generation (RAG) · Grounding · Cost Drivers in Generative AI Usage · Selecting a Generative AI Solution for a Business Need
