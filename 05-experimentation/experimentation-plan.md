# A/B Experiment Brief, Riverty BU Collection, A Fair Way Forward

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | B2: Plain explainer for why income is asked and how it is used. Control: today's income screen without help text. Variant: same screen with a "Why do we ask?" panel open by default (max. 60 words), the label "Typical monthly net income (€)", the helper line "If your pay changes, enter a normal month", and a data-use line (purpose and retention period, to be confirmed by compliance). Plans, amounts and plan order stay the same in both arms. |
| Persona | Mara, 38, shift worker with variable income and two open claims. She opens the portal on her phone during a short break, after a digital reminder, and wants one affordable plan without calling an agent. |
| Expected outcome | More multi-claim consumers answer the income question with confidence and finish the journey with a plan they can keep, instead of closing the portal. |
| Primary success metric | Agreement rate for journey starters with two or more open claims. |
| Baseline rate | 34.8% |
| Guardrail metric | Missed payment within 60 days: at or below 19.0% overall and at or below 22.5% for variable-income consumers. agent contact within 7 days at or below 31.0% |
| Guardrail boundary | Investigate if variant is more than 1 point above control; stop if more than 3 points above. |
| Second guardrail | · |
| Minimum Detectable Effect | +4 percentage points (34.8% to 38.8%) |
| Sample size per arm | 2.281 |
| Traffic split | 50/50 |
| Test duration | 16 weeks |
| Significance threshold | p < 0.05 |

## Control vs. Variant
- **Control (A):** Today's journey as it exists. After the affordability questions starts, Mara sees the income question with no help text. Nothing explains why income is asked, what to enter if her pay changes, or how the data is used (T-206). In M2 this is her moment of misery: "I did not know if they meant this month or a normal month. I closed it and meant to come back" (N-01). In the funnel, 7,364 starters reach the affordability questions, but only 5,943 reach the next step. That is a loss of 1,421 people (19.3%). "Why income is asked" is also 16.2% of agent contacts.
- **Variant (B):** One change: an explainer at the income question (PRD screen 2). Everything below is copied from the M4 PRD.
- The "Why do we ask?" panel is open by default and fits within the first screen on a 360 x 640 px viewport.
- The explainer has a maximum of 60 words, with sentences of at most 15 words.
- The input label reads "Typical monthly net income (€)", and the helper line says: "If your pay changes, enter a normal month."
- A data-use line states the purpose ("only to find a plan that fits you") and the retention period [to be confirmed by compliance].
- If Mara collapses the panel, a link "Why do we ask?" stays visible to reopen it.
- Empty input: error "Please enter an amount. A typical month is fine." Input 0: accepted, with the note "Enter 0 only if you have no income." Negative or not a number: error "Use numbers only, for example 1450." Amount above 20,000 €: soft check "Is this your monthly net income?"
- **Held constant (isolation check):** Identical in both arms:
- Portal and app version, release date, and the German pilot segment (same eligibility rules).
- Entry points and channels (email, SMS, letter QR code) and the reminder messages, including timing.
- The affordability questions themselves (same questions, same order, same validation), and the next steps after the income question.
- The income document step (no fix for the mobile upload bug T-201 during the test).
- The plan screen: same plan options, same amounts, same order (no change to which plan is shown first).
- Chat assistant, agent screens and agent scripts (no handoff summary, B4).
- Randomisation by consumer ID, so one person always sees the same arm. Consumers with several visits stay in the same arm.
Not part of the test: PRD screens 1 and 3 (entry point and confirmation) are only for the prototype. In the live test, only the income screen changes, so there is exactly one change.

## Hypothesis
> I believe that B2: Plain explainer for why income is asked and how it is used. Control: today's income screen without help text. Variant: same screen with a "Why do we ask?" panel open by default (max. 60 words), the label "Typical monthly net income (€)", the helper line "If your pay changes, enter a normal month", and a data-use line (purpose and retention period, to be confirmed by compliance). Plans, amounts and plan order stay the same in both arms. for Mara, 38, shift worker with variable income and two open claims. She opens the portal on her phone during a short break, after a digital reminder, and wants one affordable plan without calling an agent. will result in More multi-claim consumers answer the income question with confidence and finish the journey with a plan they can keep, instead of closing the portal., as measured by a +4 percentage points (34.8% to 38.8%) change in Agreement rate for journey starters with two or more open claims. within 16 weeks. We will protect Missed payment within 60 days: at or below 19.0% overall and at or below 22.5% for variable-income consumers. agent contact within 7 days at or below 31.0% throughout the test.

## Shipping criteria
> We will **ship** if Agreement rate for journey starters with two or more open claims. improves by ≥ +4 percentage points (34.8% to 38.8%) at p < 0.05 and Missed payment within 60 days: at or below 19.0% overall and at or below 22.5% for variable-income consumers. agent contact within 7 days at or below 31.0% does not reach Investigate if variant is more than 1 point above control; stop if more than 3 points above. after 16 weeks.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 16 weeks, no results reviewed before this date.
