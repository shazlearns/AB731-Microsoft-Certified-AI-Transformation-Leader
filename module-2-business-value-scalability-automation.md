# Module 2 — When Generative AI Provides Business Value (Scalability & Automation)

> **Golden rule:** generative AI creates the most value in high-volume, language-heavy work where it can scale without fatigue — and it should generally augment humans, not fully replace them, especially in business-critical scenarios.

## What is it?

Scenario recognition — spotting the signals that tell you "this is a strong generative AI use case" versus "this is actually a better fit for something else." Two big levers: scalability advantages and automation vs. augmentation.

## Explain like I'm 10

Imagine a bakery that can normally only serve 10 customers an hour because there's one baker. Generative AI is like suddenly having unlimited bakers who never get tired, never take breaks, and can serve thousands of customers at once, all with the same quality. That's scalability. But you still want a human checking that the cakes are actually good before they go out the door — that's automation *assisting* humans, not fully replacing them.

## Real-world analogy — a call centre

- **High-value use cases** = handling customer support, summarising tickets, drafting responses — routine, high-volume language tasks
- **Scalability** = instead of hiring 500 more staff for a busy season, the AI handles the surge instantly, 24/7, without getting tired or inconsistent
- **Automation vs. augmentation** = the AI drafts a reply, but a human still reviews and sends it for anything sensitive — the AI assists the agent, it doesn't replace them
- **When NOT to use it** = if a customer needs a guaranteed, regulator-approved answer (e.g. a legal ruling), you don't want an AI improvising that

## How does it work?

**1. High-value use cases** — content creation at scale (marketing, product descriptions, reports), customer support (intelligent chatbots, ticket summarisation), document processing (summarisation, extraction, translation). Common thread: large volumes of unstructured, language-heavy work.

**2. Scalability advantages** — process thousands of requests simultaneously (API-based); consistent quality at any volume, no human fatigue; 24/7 availability without staffing constraints.

**3. Automation vs. augmentation** — augment human workers (draft → review → publish workflows); automate repetitive writing (emails, summaries, status updates); accelerate decision-making (synthesise data into recommendations). Scenarios generally favour AI assisting humans, not fully replacing them — especially in business-critical situations.

**4. When NOT to use generative AI** — tasks requiring guaranteed accuracy (medical diagnosis, legal rulings); simple classification (traditional ML is cheaper and faster); fixed-rule processes (automation scripts outperform AI).

## When is it used?

Whenever a scenario describes high-volume, language-based, or content-generation work — especially where consistency at scale matters. Also tested in reverse: recognising when a scenario is really describing ML or rule-based automation instead, even though "AI" is mentioned.

## Key differences

| Signal in the scenario | Points to |
|---|---|
| High-volume content creation, chatbots, document processing | Generative AI |
| Needs guaranteed accuracy (medical/legal) | NOT generative AI — needs deterministic accuracy |
| Simple classification task | Traditional ML (cheaper, faster) |
| Fixed, repeatable process | Rule-based / automation scripts |
| AI drafts, human reviews before publishing | Augmentation (preferred over full automation) |

## Exam alert

**Must know:** 3 high-value use case categories — content creation at scale, customer support, document processing. Scalability = handle high volume, run continuously, consistent output, without increasing human effort. Augmentation is generally preferred over full automation, especially for business-critical scenarios. Know the "avoid generative AI" triggers: guaranteed accuracy needed, simple classification, fixed-rule processes.

**Should know:** scalability's core advantage is no human fatigue — quality doesn't degrade as volume increases. "Draft → review → publish" is the classic augmentation workflow pattern.

**Nice to know:** ties back to the 3 Types of AI lesson — unstructured, language-heavy work → generative AI; structured/numeric prediction → traditional ML; fixed logic → rule-based.

> **Exam trick:** if a scenario mentions "AI" but describes a task needing guaranteed, regulator-defensible accuracy (medical, legal), the correct answer is often to reject generative AI even though it's technically capable — deterministic, auditable systems are the safer fit.

## Exam keywords

"High-volume content, chatbots, summarisation" → generative AI. "Guaranteed accuracy, medical/legal ruling" → NOT generative AI. "Draft → review → publish" → augmentation. "Fully replace staff to save time" → usually the wrong answer — exam favours augmentation.

## Common confusion

Many people assume "AI can scale, therefore AI should fully automate everything." The exam pushes back — scalability is about capacity, not about removing human oversight. Especially in business-critical scenarios, the correct answer usually keeps a human in the loop (augmentation), even when the AI could technically handle the full volume alone.

## Memory trick

> SCALE IT, DON'T REPLACE PEOPLE. High volume + language-heavy → generative AI. Guaranteed accuracy or fixed rules → something else. AI assists, humans decide.

## Practice questions

**Question 1.** A hospital wants an AI to summarise patient intake notes for doctors to quickly review, with doctors still making the final diagnosis. Is this a good generative AI use case, and is it augmentation or automation?
**Answer: B — good use case; augmentation (AI summarises, doctor decides).** Summarising notes is exactly the language-heavy, high-volume task generative AI excels at. The doctor still makes the final diagnosis — AI assisting, not replacing, the human decision-maker.

**Question 2.** True or false: because generative AI can scale to thousands of requests at once, it should always fully replace human review in high-volume scenarios to save time.
**Answer: False.** Scalability is about capacity, not about removing oversight. The exam favours augmentation over full automation, especially in business-critical scenarios, regardless of how much volume the AI can technically handle.

## Related concepts

Challenges of Generative AI (Fabrication, Reliability, Bias) · Selecting a Generative AI Solution for a Business Need · 3 Types of AI · Cost Drivers in Generative AI Usage
