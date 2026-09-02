# Module 1 — 3 Types of AI

## The big idea

> **Ask one question:** what does the system do with the information it receives?
> **Follow rules** → **predict an outcome** → **create new content**

| Type | What it does | Banking example | Exam clue |
|---|---|---|---|
| **Rule-based AI** | Follows human-written instructions | Flag a transaction when defined conditions are met | **IF / THEN**, fixed policy, identical outcome |
| **Traditional ML** | Learns from past data to classify, score, or predict | Estimate the likelihood that a transaction is fraud | Probability, prediction, detection, pattern |
| **Generative AI** | Creates new content from learned patterns and context | Draft a summary of a fraud investigation | Write, summarise, explain, generate |

---

## 1. Rule-based AI

**In simple English:** humans write the rules → the computer follows them. The system does **not learn** the rules itself. It applies the logic it has been given.

**How it works**
1. A human defines a rule.
2. The system checks whether the condition is true.
3. It carries out the matching action.

> IF transaction amount is more than $10,000 AND the customer is overseas → send the transaction for review

**Banking example:** a bank may automatically reject a payment when account balance is below $0.

**Why it's useful:** predictable (same input follows the same rule), auditable (a person can see exactly why the decision happened), and well suited to clear, stable, explicit policies.

**Key term — deterministic:** same input + same rules → same output every time.

**Limitation:** if a new situation isn't covered, the system can't adapt by itself — a human must add or change the rule.

> **Common trap:** rule-based AI can automate a decision, but it is not learning from data.

## 2. Traditional AI / Machine Learning

**In simple English:** give the model examples → it learns patterns → it predicts. Traditional ML looks at existing data and learns relationships within it, then applies those patterns to a new case.

**How it works**
1. Give the model historical data.
2. Include known outcomes where available.
3. The model finds useful patterns.
4. Give it a new case.
5. It returns a classification, score, number, or probability.

**Banking example — fraud detection:** a bank gives the model historical transactions labelled fraud or legitimate. The model learns the patterns and evaluates a new transaction, e.g. "fraud probability: 87%." This is usually about classification (fraud or legitimate?), prediction (what's likely to happen?), scoring (how risky is this customer?), or pattern detection (what looks unusual?).

> **AB-731 signal:** when a scenario asks for a probability, risk score, prediction, or detection of patterns, think traditional ML.

## 3. Generative AI

**In simple English:** give it context → it creates something new. Generative AI uses learned patterns to produce new content rather than simply returning a label or prediction.

**What it can create:** a document → summary; a question → explanation; requirements → a project plan or code; data → a narrative report; a prompt → image, audio, or video.

**Banking example:** an investigator provides a case file and asks, "Create an executive summary of this fraud investigation, including the main risk indicators and recommended next steps." The output is new written content.

> **Common trap:** generative AI can discuss, explain, or summarise a fraud case, but it isn't automatically the best choice to calculate the fraud probability — that's typically a traditional ML use case.

## Compare and contrast

| Question to ask | Rule-based AI | Traditional ML | Generative AI |
|---|---|---|---|
| Where does the behaviour come from? | Human-written rules | Patterns learned from data | Patterns learned from data and context |
| Typical output | Action or decision | Label, score, number, or probability | New text, image, code, audio, or video |
| Best scenario clue | "Follow this policy" | "Predict or detect" | "Write, summarise, or create" |

**One banking team, three roles:** the rule follower ("here is the policy, follow it exactly"), the data analyst ("based on millions of transactions, this one has a 90% chance of being fraud"), and the content creator ("here is the investigation report — write an executive summary").

## Technical nuance

> Generative AI is a form of machine learning. These are not three completely separate technologies — for AB-731, focus on what the system is designed to produce and how it's used.

**Discriminative vs. generative:** discriminative models distinguish categories or predict outcomes (e.g. fraud vs. legitimate); generative models create new content (e.g. a written explanation or summary).

## Memory shortcut

> **RULE → PREDICT → CREATE**
> Rule-based = process automation. Traditional ML = prediction/detection. Generative AI = knowledge/content generation.

## AB-731 exam takeaway

1. Choose **rule-based AI** when the decision must follow explicit, stable rules and be consistently auditable.
2. Choose **traditional ML** when the goal is to classify, score, detect patterns, or predict an outcome from data.
3. Choose **generative AI** when the goal is to produce or transform content such as summaries, explanations, plans, or drafts.

> **One-sentence exam answer:** Rule-based systems follow explicit human-written logic; traditional ML learns patterns from data to classify or predict; generative AI uses learned patterns to create new content.

## Quick knowledge check

1. **A bank needs identical claims decisions based on a clear policy. Which approach fits best?**
   → Rule-based AI. Rule-based AI applies human-written IF/THEN logic, so identical inputs always produce identical, auditable outcomes.
2. **A bank wants to estimate whether a transaction is fraudulent. Which approach fits best?**
   → Traditional ML. Estimating a probability or risk score from historical patterns is a prediction/classification task.
3. **A manager wants a concise executive summary of a 100-page risk report. Which approach fits best?**
   → Generative AI. Summarising existing content into new written text is a content-creation task.
4. **True or false: Generative AI and machine learning are completely unrelated.**
   → False — generative AI is a form of machine learning; the three types differ in what they're designed to produce, not in being unrelated technologies.
