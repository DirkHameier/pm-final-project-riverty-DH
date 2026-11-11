# Roadmap, PRD & Prototype (Module 4)

## Your strategic anchors
- **Persona (M2), who are you solving for?:** Mara, a shift worker with two open claims, on her phone during a short break. Goal: one affordable plan for both claims without calling anyone. Confirmed friction: she cannot answer the income question and leaves. The data confirms she is real, but she is the most affected group (about 9% of starters), not the average user.
- **Primary success metric (M3), your leading indicator:** Agreement rate for starters with two or more claims. Baseline: about 34.8% (1,034 agreements from 2,968 starters). Proposed target: 41%, about 6 points, which is one third of the gap to single-claim consumers (52.1%). That would mean about 180 more agreements per month.
- **Moment of misery (M2), the specific friction blocking the goal:** The moment Mara reaches the income question and cannot answer it. The portal asks for her income, but she does not know if it means this month or a normal month. Her pay changes with her shifts, and she has only a short break. Nothing on the screen explains what to enter or why the question is asked, so she stops.
- **Guardrail metric (M3), what must not drop or break:** Missed payment within 60 days must not rise above 19.0% overall, and not above 22.5% for variable-income consumers. The 6-month-first screen already raised it from 15.2% to 19.0%, so a higher agreement rate bought with weaker plans would not count as success. Second guardrail: agent contact within 7 days must not rise above 31.0%.

## Scan the backlog & set a human baseline
- **My instinctive “quick wins” before touching the AI (2 to 3 feature IDs + why):** B2, B5, B4. B2 fixes Mara’s income moment with a text change. B5 fixes the upload failure behind 853 lost journeys and the highest-loss step (22.1%). B4 ends repeated questions on agent calls  without changing the consumer flow.

## Audit, override & decide
- **Where did you override the AI? (feature + old vs. new score + why):** _(not filled in)_
- **Did the AI over-value a Sales/Eng request your M2 interviews don’t support?:** _(not filled in)_
- **Did it underweight something your M3 cohort/funnel data strongly supports?:** _(not filled in)_

## Generate your interactive roadmap
- **My “Now” lane (this sprint), the 2 to 3 quick wins I’ll build first:** B2 Plain explainer: why income is asked and how it is used (Value 5, Effort 1).
B5 Mobile photo upload, or skip the document under a set amount (Value 5, Effort 2).

Both attack Mara's core friction and are cheap. "Why income is asked" causes 16.2% of agent calls (N-01, N-06, T-206), and 853 journeys never got a document because of the mobile upload bug (T-201). I will also add a line to B2 about what happens after a missed payment, the top call reason at 18.6%. B1 and B3 are Next, because they are Major Projects that do not fit this sprint.
- **What I cut, and the “no” I’m protecting the scope from:** I cut two features:
B7 Show the shortest plan first: it is cheap, but in Month 4 it raised SSR while missed payments rose from 15.6% to 18.4%. This breaks my 19.0% guardrail, and interview N-02 shows the same pattern.
B8 Chat assistant on every portal page: Effort 5 for unclear value. Chat users miss more payments (21.6% vs 18.3%), and the chat confirms plans without explaining a missed payment (N-05, T-208).

The "no" I am protecting: I will not raise the Self-Service Rate with changes that push consumers into plans they cannot keep. A plan counts as resolved when it is created, so I protect the missed-payment guardrail first.
- **Prototype/roadmap screenshot link (paste into your deliverables):** bu-collection-roadmap.png
