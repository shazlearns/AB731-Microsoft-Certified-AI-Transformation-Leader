# Module 4 — Machine Learning Lifecycle

> **Golden rule:** an ML solution isn't "done" at deployment — it's a loop: Data Prep → Train → Evaluate → Deploy → Monitor & Retrain. Skipping or rushing any stage (especially Data Preparation) is the #1 cause of ML project failure.

## What is it?

The Machine Learning Lifecycle is the repeatable 5-stage process a team follows to build, ship, and maintain an ML solution — it doesn't end at deployment because real-world data keeps changing (model drift), so monitoring loops back into retraining.

## Explain like I'm 10

Training an ML model is like training a guide dog: you don't just teach it once and forget about it. You keep checking its work, and if the world changes (new streets, new traffic patterns), you retrain it — otherwise it starts making mistakes.

## Real-world analogy

Think of it like opening a restaurant: you prep ingredients (data prep), test recipes (training), get a food critic's review (evaluation), open the doors (deployment), then keep watching customer feedback and adjust the menu over time (monitor & retrain). You never "finish" running a restaurant.

## Example

A bank builds a fraud-detection model. It spends 4 of 5 months just cleaning and labelling transaction data (normal — Data Prep is the biggest time sink). After deployment, fraud patterns shift as scammers adapt, so accuracy drops from 92% to 70% within 3 months. This is model drift — the team collects fresh transaction data and retrains.

## How it works — the 5 stages

**1. Data Preparation — "getting the ingredients ready."** Analogy: before cooking a meal, you wash, chop, and measure every ingredient — this prep work often takes longer than the actual cooking. What happens: collecting, cleaning, labelling, and structuring the data the model will learn from — removing duplicates, fixing errors, handling missing values, ensuring representativeness. Example: a fraud-detection team spends 3 months cleaning and correctly labelling 2 years of transaction records before any model training begins. Why it matters: this is 60–80% of total project time and the #1 cause of ML project failure.

**2. Model Training — "teaching the model."** Analogy: a student studying from a textbook, working through practice problems, with a tutor adjusting their study method along the way. What happens: selecting an algorithm, splitting data into training/validation/test sets, and tuning hyperparameters (settings that control HOW the model learns, e.g. learning rate, number of iterations). Example: the fraud team splits their cleaned data — 70% to train, 15% to validate/tune, 15% held back for a final unseen test. Why it matters: the train/validation/test split exists specifically so the model is evaluated on data it has never seen — this is what makes overfitting detectable.

**3. Evaluation — "the exam before the real job."** Analogy: a trainee pilot doing a check flight in a simulator before ever flying real passengers. What happens: testing the trained model against the held-out test set, checking for overfitting (great on training, poor on new data) or underfitting (poor everywhere), and measuring performance with accuracy, precision, recall, F1 score. Example: the fraud model scores 95% accuracy on training data but only 65% on the untouched test set — a red flag for overfitting. Why it matters: this is the LAST checkpoint before real-world deployment.

**4. Deployment — "opening for business."** Analogy: after passing their check flight, the pilot is finally cleared to fly real passengers. What happens: the model is released into production, integrated into a real system, and starts making live predictions on real, unseen data. Example: the fraud model goes live, now scoring every incoming transaction in real time and flagging suspicious ones for review. Why it matters: performance in production can differ from performance in testing — deployment is a milestone, not the finish line.

**5. Monitor & Retrain — "keeping the pilot current."** Analogy: pilots must complete recurrent training and checks regularly — certified once isn't enough, because conditions change over time. What happens: continuously tracking the model's real-world performance, watching for model drift — the gradual decline in accuracy as real-world patterns shift away from what the model was trained on — and retraining with fresh data when needed. Example: six months after launch, the fraud model starts missing a new scam pattern criminals invented after the training data was collected — the team retrains it on more recent data. Why it matters: ML is never "finished."

> The lifecycle is a loop, not a line — Monitor & Retrain feeds back into Data Preparation/Training, not a dead end.

**3 key failure modes:**

| Term | Meaning |
|---|---|
| Overfitting | Model performs great on training data, poor on new/unseen data — it "memorised" rather than "learned" |
| Underfitting | Model fails to capture patterns even in training data — too simple for the task |
| Model drift | A previously good model's performance degrades over time as real-world data patterns shift |

## When used

Applies to every ML solution (classification, prediction, recommendation, anomaly detection) once you've selected ML as the right tool. Especially critical in production systems facing changing real-world behaviour — fraud detection, demand forecasting, recommendation engines.

## Key differences

Evaluation is a controlled, one-time check using data the model has never seen but from the same time period as training — it catches overfitting/underfitting. Monitor & retrain is ongoing, using genuinely new real-world data collected after deployment — it catches drift.

Overfitting vs. underfitting: overfitting = too closely fit to training data (fails on new data); underfitting = not fit closely enough even to training data (fails everywhere). Overfitting/underfitting are evaluation-stage problems (caught before deployment); model drift is a post-deployment problem (appears after the model has been live for a while).

> A model that was accurate at launch but has degraded months later is NOT overfitting — it's drift, because the model itself hasn't changed, the real world has.

## Exam focus

**High priority:** know all 5 stages in order and that Data Preparation dominates project time.

**Medium priority:** overfitting vs. underfitting definitions.

**Good to know:** precision/recall/F1 distinctions.

> **Exam trick:** a scenario describing accuracy dropping gradually AFTER deployment (not a training-time problem) is testing model drift, not overfitting. Overfitting is caught DURING evaluation, before deployment — drift happens AFTER.

## Exam keywords

Data preparation, model training, hyperparameter tuning, train/validation/test split, overfitting, underfitting, evaluation metrics (accuracy/precision/recall/F1), deployment, model drift, monitor & retrain.

## Common confusion

Overfitting vs. model drift: overfitting is a training-stage problem detected at evaluation (before deployment); model drift is a post-deployment problem — the model was fine at launch but the world changed. Validation set vs. test set: validation is used repeatedly during training to tune; test set is used once, at the end, and must stay completely unseen until final evaluation.

## Memory trick

> "D-T-E-D-M" → Data prep, Train, Evaluate, Deploy, Monitor & retrain — and it loops back to D.

## Practice questions

**Question 1.** A team spends 4 months of a 5-month ML project cleaning, labelling, and structuring their data before any training begins. Is this normal, and what stage is this?
**Answer:** Yes, this is normal — it's the Data Preparation stage. Data Preparation is 60–80% of total project time and the #1 cause of ML project failure.

**Question 2.** A model passes evaluation with 92% accuracy on the held-out test set, but three months after deployment its accuracy has dropped to 70% as customer behaviour has shifted. What should the team do, and what's this phenomenon called?
**Answer:** This is model drift; the team should collect fresh data and retrain the model — the model was fine at launch and the world changed afterward.

**Question 3.** A model shows 98% accuracy on training data but only 61% accuracy on the test set. What's happening?
**Answer:** Overfitting — the model performs great on training data but poorly on new/unseen data, caught at the Evaluation stage, before deployment.

## Related concepts

Machine Learning Selection (When ML Adds Value)
