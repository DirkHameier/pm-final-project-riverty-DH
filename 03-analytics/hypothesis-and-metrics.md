# Hypothesis & Success Metrics (Module 3)

## Pre-work · Hypothesis check
- **Role , who you are solving for (from M2):** Mara, a consumer and shift worker with two open claims. She opens the portal on her phone during a short break.
- **Goal , what this user is ultimately trying to achieve:** Set up one affordable instalment plan for both claims without having to call anyone.
- **Friction / moment of misery , the specific pain blocking their goal:** ara reaches the income question and cannot answer it. She does not know if “income” means this month or a normal month (N-01). Nothing on the screen explains why it is asked (T-206), so she closes the portal. Variable-income consumers miss payments more often (22.5% vs 17.4%), and consumers with two claims reach an agreement less often (37.7% vs 52.1%).
- **Current workaround , the external tool or manual process they rely on (M2):** The research pack names no external tool, such as Google or a spreadsheet. Her workaround is manual:

She closes the portal and means to come back later (a “mental bookmark”).
She calls an agent, who cannot see what she typed online, so she repeats everything (N-08, T-205).
If she continues without calling, she may guess the income answer (this part is an assumption).
- **Problem Hook , your one-sentence framing of the business crisis (M1):** Consumers like Mara abandon or fail Riverty’s digital instalment journey, so only 3.8% of outreach ends in an agreement and 19% of those plans break within 60 days. This raises agent workload and client complaints, and the SSR north star can still look better than reality.
- **Value Proposition , the outcome your initiative promised to deliver (M1):** A digital instalment journey that helps consumers like Mara agree to a plan they can afford and keep, with a clear handoff to an agent when needed. It promises:

fewer drop-offs and plans that last
less avoidable agent work
fair, explainable outcomes
honest measurement (SSR paired with plan-kept and complaint measures)

## Read the evidence in your case
- **Where does your case say people stall or leave? Does that match the friction you wrote in Module 2?:** Each step in the funnel loses 12% to 22% of the people who reach it.

Entering the journey is the first big leak: 100,000 consumers get outreach, 38,000 enter the portal (38.0%) and 8,360 start the journey (22.0% of visitors).
After the start, the journey loses people at every step:
Step	People lost	Share of that step
Start → affordability questions	996	11.9%
Affordability questions → income document step	1,421	19.3%
Income document step → plan review	1,313	22.1%
Plan review → agreement	784	16.9%
The biggest loss in absolute numbers (1,421 people) happens right after the affordability questions, where the income question sits. This confirms Mara’s moment of misery.
The step with the highest loss rate is the income document step (22.1%). In the journey data, 3,966 people were asked for a document and only 3,113 uploaded one (853 did not). Mara’s story does not cover this friction, so it adds nuance.
Mobile is not the main issue for uploads. The upload rate is 77.8% on mobile and 81.0% on desktop, so my “mobile upload” hunch was too strong.
The funnel cannot show whether people leave because of the income question itself or because of the other affordability questions. I would ask for drop-off per question and per screen, plus return rate after abandonment. That would test the “mental bookmark” workaround.
My hook used the wrong base. The 3.8% is “agreements per 100,000 outreach”, and most of those people never wanted a plan. The better base is 8,360 starters, 46.0% of whom reach an agreement. Also, 19.0% of agreements break within 60 days (3,115 of 3,846 stay on track).
- **What got better or worse in the case, and does that support the workaround your persona uses?:** Over six months, the headline metrics improved while plan quality got worse.

Metric	Month 1	Month 6
Agreement rate	43.1%	46.0%
Missed payment within 60 days	15.2%	19.0%
Agent contact within 7 days	33.4%	31.0%
SSR	31.1%	34.7%
In Month 4, the plan screen changed to show the 6-month plan first instead of the 12-month plan. Missed payments jumped from 15.6% to 18.4% that month and kept rising.
3.8 points on 3,846 agreements is about 146 extra broken plans per month.
This supports N-02, where a consumer chose the plan that looked right and missed the second payment.
The signals point in different directions:
Agreement rate and SSR look better, but missed payments rise. SSR is therefore a misleading north star on its own.
Agreement rate was already rising before Month 4 (43.1% → 44.2%), so the plan screen change does not explain all of it.
There is no control group and only six months, so this is a correlation.
Agent contact fell only 2.4 points. About 31% of starters still contact an agent, so the “call an agent” workaround is very much alive.
The top three contact reasons are 52% of the 2,592 contacts:
“What if I miss a payment” (18.6%)
“Can claims be combined” (17.3%)
“Why is income asked” (16.2%)
The trend file has no split by segment, no euro values and no data on returning users. I would ask for missed payments over time for variable-income consumers and recovered euros per month.
- **Which user in the case is carrying the pain, and is that the person your Module 2 persona describes?:** Mara is real, but she carries three separate pains, not one.

Two or more claims (2,968 starters, 35%) is the strongest signal:
Claims	Agreement rate	Agent contact	SSR
1	52.1%	25.6%	40.6%
2	37.7%	40.0%	26.0%
3+	27.6%	43.0%	19.3%
Variable or shift income (2,862 starters, 34%) mostly shows up in broken plans:
Income	Agreement rate	Missed payment	Agent contact
Variable or shift	41.6%	22.5%	32.7%
Fixed salary	48.1%	17.4%	30.2%
Mobile (6,563 starters, 78.5%) shows up in agreement rate: 43.8% vs 54.0% on desktop. Missed payments are the same on both devices (18.9% vs 19.2%).
My own cut of the journey data for Mara’s exact profile (two or more claims, variable income, mobile) gives 780 starters, about 9% of all:
	Mara’s profile	Everyone else
Agreement rate	29.2%	47.7%
Agent contact	43.8%	29.7%
Missed payment	23.2%	18.7%
SSR	19.6%	36.3%
This confirms the persona, but it also shows she is not the average user. She is the most affected 9%, so she is a good design target but not the whole problem.
Two more signals point in different directions:
Chat assistant users look better (agreement 53.3% vs 44.4%, SSR 41.5% vs 33.2%), but their plans break more (21.6% vs 18.3%). This fits T-208. It may also be selection bias, because I cannot tell who chooses to use the chat.
Portfolio type and entry channel show almost no difference (agent contact 30.4% to 31.5%). The problem does not come from where the consumer enters.

## Step 2 · Craft your hypothesis
- **Qualitative evidence (from M2) , quote the specific friction / moment of misery for your persona:** N-01, consumer, two open claims, shift work: “I opened it on my break. It asked for my income and I did not know if they meant this month or a normal month. I closed it and meant to come back.” T-206: no help text explains why income is asked. N-03: “I could only see one claim at a time.”
- **Quantitative evidence (from M3) , name the metric or data point that confirms the pain; cite the number:** Consumers with two or more claims reach an agreement in 37.7% of cases (two claims) and 27.6% (3+), against 52.1% with one claim. Their agent contact is 40.0% and 43.0%, against 25.6%. Variable-income consumers miss payments in 22.5% of cases, against 17.4% for fixed salary. The funnel loses 1,421 people (19.3%) right after the affordability questions. My cut for Mara’s exact profile (two or more claims, variable income, mobile; 780 starters) shows an agreement rate of 29.2% against 47.7% for everyone else.
- **Persona , role, goal, and the friction you confirmed in the reconciliation steps:** Mara, a shift worker with two open claims, on her phone during a short break. Goal: one affordable plan for both claims without calling anyone. Confirmed friction: she cannot answer the income question and leaves. The data confirms she is real, but she is the most affected group (about 9% of starters), not the average user.
- **Problem you are solving , one sentence describing the specific friction this initiative removes:** Consumers with several claims and variable income cannot finish the digital journey, because it shows claims one at a time, asks an unclear income question and offers no plan that fits their pay. They leave or call an agent.
- **Strategic outcome , what behaviour change do you expect, and how does it map to retention / revenue / churn?:** More multi-claim and variable-income consumers reach an agreement, and the plans last. This means more recovery from consumers who stall today, fewer avoidable agent calls and fewer broken plans in client reporting. The pack has no euro figures, so I cannot yet map this to revenue. I would ask for recovered euros per agreement and cost per agent minute.
- **Primary success metric (initiative signal) , the leading indicator that tells you the gap is closing:** Agreement rate for starters with two or more claims. Baseline: about 34.8% (1,034 agreements from 2,968 starters). Proposed target: 41%, about 6 points, which is one third of the gap to single-claim consumers (52.1%). That would mean about 180 more agreements per month.
- **Guardrail metric (product signal) , the metric that must NOT drop; it protects your existing base:** Missed payment within 60 days must not rise above 19.0% overall, and not above 22.5% for variable-income consumers. The 6-month-first screen already raised it from 15.2% to 19.0%, so a higher agreement rate bought with weaker plans would not count as success. Second guardrail: agent contact within 7 days must not rise above 31.0%.
- **Decision window , how much time or data before you scale, pivot, or kill? minimum threshold to proceed?:** Run an A/B test, because the trend data has no control group. Read agreement rate after 4 weeks. Read the missed-payment guardrail only after about 10 to 12 weeks, because plans need 60 days to show a missed payment. Scale if multi-claim agreement rate is at least 4 points above control and missed payments are no more than 1 point above control. Pivot if agreement rate rises but missed payments rise by more than 2 points. Kill if agreement rate is less than 1 point above control after 8 weeks.
- **Draft your full hypothesis sentence , one to three sentences; quote the metric, name the persona, name the outcome:** Based on N-01 (“I did not know if they meant this month or a normal month”) and on only 34.8% of multi-claim starters reaching an agreement (52.1% with one claim), I believe that a clear income question and one affordable plan for both claims for Mara (a shift worker with two claims, on her phone) will result in more plans she can keep, as measured by a 6-point increase in multi-claim agreement rate (34.8% to 41%). I will protect missed payments (at or below 19.0%) and agent contact (at or below 31.0%), and will decide go/no-go after 12 weeks.
