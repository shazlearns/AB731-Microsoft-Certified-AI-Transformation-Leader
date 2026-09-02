# Module 4 — Impact of Data on AI Solutions

> **Golden rule:** AI is only as good as the data behind it — 4 pillars decide that: data types/formats, data quality, representativeness, and governance.

## What is it?

The impact of data on AI solutions covers how the shape, condition, coverage, and control of an organisation's data directly determines how well an AI system performs. Bad data doesn't just mean "wrong answers" — it maps directly to the fabrication, reliability, and bias risks covered in Module 2.

## Explain like I'm 10

If you feed an AI messy, incomplete, or unfair data, it'll give you messy, incomplete, or unfair answers — "garbage in, garbage out," but for AI.

## Real-world analogy

Think of the AI as a chef. Data Types = what ingredients look like (chopped veg vs. whole ingredients vs. a recipe scrawled on a napkin). Data Quality = whether ingredients are fresh or rotten. Representativeness = whether the pantry has ingredients for ALL the dishes you're expected to cook, not just some. Governance = who's allowed into the pantry and what they can take out.

## Example

An HR chatbot trained mostly on data from head-office employees (not warehouse staff) will struggle to answer warehouse-specific questions accurately — that's a representativeness failure, even if the data itself was "high quality."

## When is it used?

Any exam scenario describing an AI giving inconsistent, outdated, hallucinated, or biased answers — the root cause traces back to one of these 4 pillars. Also relevant during the planning phase of any AI project, before choosing an approach.

## Key differences

- **Data Quality** = is the data itself correct/current/complete? (a data problem)
- **Representativeness** = does the data cover everyone/everything it needs to? (a coverage/bias problem — can exist even with "clean" data)
- **Governance** = who controls and can access the data? (a compliance/access problem)

Don't confuse "poor data quality" with "non-representative data" — you can have perfectly accurate data that's still not representative.

## Exam alert

**Must know:** the 3 data types (structured/semi-structured/unstructured) — expect direct classification questions (e.g. "emails with metadata" = semi-structured). Also the 5 data quality dimensions — accuracy, completeness, consistency, timeliness, relevance.

**Should know:** non-representative data → bias is a direct, frequently tested causal link.

**Nice to know:** data lineage as a specific governance term (tracking origin + changes).

> **Exam trick:** "AI performs poorly for a specific group/scenario" → think representativeness, NOT data quality, unless the question specifically says the data has errors.

## Exam keywords

Structured / semi-structured / unstructured data, data quality, accuracy, completeness, consistency, timeliness, relevance, representative dataset, bias, data lineage, data stewardship, data governance.

## Common confusion

People conflate "data quality" and "representativeness" — quality = correctness of what's there; representativeness = whether what's there covers the right population. Governance ≠ security — governance is broader (lineage, stewardship, ownership, compliance), while security is specifically about protecting data from unauthorised access.

## Memory trick

> "TQRG" — Types → Quality → Representative → Governance. Or: "Right Shape, Right Condition, Right Coverage, Right Hands."

## Practice questions

**Question 1.** An AI model was trained almost entirely on customer data from one country, and now performs poorly for customers in other regions. Which pillar does this failure fall under?
**Answer: Representativeness.** The data may be perfectly accurate, but it doesn't cover the full population the AI needs to serve — a coverage/bias problem, not a data quality problem.

**Question 2.** A dataset has JSON log files with some nested structure but no fixed schema. Which data type is this — structured, semi-structured, or unstructured?
**Answer: Semi-structured.** It has some structure (nested JSON fields) but no fixed schema, the defining trait of semi-structured data — unlike structured data (fixed schema, e.g. tables) or unstructured data (no inherent structure, e.g. free text).

## Related concepts

Challenges of Generative AI (Fabrication, Reliability, Bias) · Grounding: Business Requirements
