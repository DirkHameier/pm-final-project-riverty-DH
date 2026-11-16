# Individual Insights: Development Process

> Module 6 · Launch Impactful GTM Plans, ★ Deliverable 6 (reflection)
>
> _The personal reflection that closes your final project._

## Friction points

Hard: The data did not give one simple answer. The 6-month-first plan screen raised the Self-Service Rate (31.1% → 34.7%), but missed payments rose too (15.2% → 19.0%). A metric can go up while the product gets worse. Chat users also looked better (SSR 41.5% vs. 33.2%), but they may be a self-selected group, so I could not treat it as cause and effect.

Surprised me: The best first feature was not a big build. The biggest friction was a missing text at the income question, and it needs only a small change. This one screen explains a 19.3% drop (1,421 people) and 16.2% of agent contacts.

_____

## Key learnings

Guardrails are part of the metric, not an extra. Without the 19.0% missed-payment limit, the 6-month screen would have looked like a success.
Good evidence needs clean instrumentation: events like “explainer opened” and “income step completed” must exist before launch, or we cannot learn anything.
Small, isolated changes are easier to test, ship and roll back than big ones.

_____

## Aha! moment

I stopped asking “what can we build?” and started asking “what can we measure and isolate?”. Once I wrote the A/B test with one change, the same plans, the same order and randomisation by consumer ID, the feature, the metric and the guardrails became one clear chain.
_____
