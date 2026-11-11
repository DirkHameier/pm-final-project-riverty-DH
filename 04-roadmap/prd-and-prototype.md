# B2 Plain explainer: why income is asked and how it is used, Simplified PRD (Riverty BU Collection, A Fair Way Forward)

**Scenario:** Riverty BU Collection, A Fair Way Forward

**Author:** Me · **Status:** Draft · **Target:** High-Fidelity Prototype · **Persona:** Mara, 38, shift worker with variable income and two open claims. She opens the portal on her phone after a reminder, has little time, and cannot pay the total at once.

## 1. The Big Picture
- **Vision:** To eliminate Mara's guesswork and fear at the income question by explaining in plain words why we ask, which income to enter and how her answer is used.
- **Press release:** Today, Riverty launched a plain explainer at the income question in its instalment journey. Consumers who cannot pay a balance in one go now see a short text that says why we ask, which income to enter, and how the answer is used and for how long it is kept. Shift workers like Mara no longer have to guess whether to enter this month or a normal month.

Until now, 16.2% of agent contacts were about why income is asked, and consumers closed the portal because they feared typing a wrong number. With the explainer, they can answer on their phone, in one step, without waiting for a call.
- **Success metric:** Self-Service Rate (SSR) for plans, no agent contact within 7 days: 34.7% to 36.7%
- **Guardrail:** Missed payments within 60 days at or below 19.0%

## 2. The Details
### User stories
- As Mara, I want to see why my income is asked, so that I do not close the portal out of fear.
- As Mara, with shifting work hours, I want to know which income to enter, so that I do not enter a number that makes my plan too high.
- As Mara, I want to know how my data is used and how long it is kept, so that I trust the portal enough to answer.
### Screens to build
- 1. Entry point: balance summary, button "Set up a plan", line "Next: 2 questions about your income"
- 2. Core: income question with label, income input (€ per month), "Why do we ask?" panel (open by default), data-use line, button "Continue"
- 3. Confirmation: confirmation message, summary of the entered amount, link "Change my answer", note "Next: your plan options"
### Functional requirements
- The system must show the explainer panel open by default at the income question, within the first screen on a 360 x 640 px viewport.
- The system must keep the explainer to a maximum of 60 words, with sentences of at most 15 words.
- The system must label the input "Typical monthly net income (€)" and show the helper line "If your pay changes, enter a normal month."
- The system must show a data-use line with the purpose ("only to find a plan that fits you") and the retention period [to be confirmed by compliance].
- The system must store and send no data, with no login and no external API.
### Smart behaviors (Situation → Outcome)
- If Mara opens screen 2 → the explainer is already visible
- If Mara collapses the explainer → a link "Why do we ask?" stays visible to reopen it
- If the input is empty and she presses Continue → error "Please enter an amount. A typical month is fine."
- If the input is 0 → accept it and show the note "Enter 0 only if you have no income."
- If the input is negative or not a number → error "Use numbers only, for example 1450."
- If the amount is above 20,000 € → soft check "Is this your monthly net income?" with Confirm and Change
- If the screen is wider than 768 px → centre the layout at 480 px width, content stays the same
### Technical constraints
- No external API calls, and no fonts or scripts from other servers
- No login or user accounts
- No saving of data (no localStorage, no cookies, no database)
- One HTML file with plain JavaScript, no framework
- No affordability calculation, scoring or plan logic

## 3. The Logistics
### Features out
- Affordability calculation (B3)
- Automated income decision or scoring model
- Multi-claim logic (B1)
- Changes to the upload step (B5) and the chat assistant (B8)
- Other languages or markets
- Personalised text based on claims or income
### Edge cases & safety guard
- Empty input → error "Please enter an amount. A typical month is fine."
- Input is 0 → accept it with the note "Enter 0 only if you have no income."
- Text or negative number → error "Use numbers only, for example 1450."
- Amount above 20,000 € → soft check "Is this your monthly net income?"
- Browser back button → show an empty field, no error
- Vulnerable consumer → visible link "Questions? Talk to an agent", never blocks the journey
- Safety: the explainer text is fixed and reviewed, never generated live. It must NEVER promise outcomes ("lower rate", "approved", "guaranteed") and never invent a retention period or legal claim. An unconfirmed retention period blocks release.
### Decision log
- Open by default, not behind a link: Mara has little time and may not tap a small "?", and the income question is her moment of misery.
- Removed personalised explanation to focus on one fixed text: it needs backend work and compliance review of each variant, and one text fits 3 engineers in one sprint.
### Evals
- Accuracy: at least 80% of 5 to 8 test consumers say correctly why income is asked and which income to enter.
- Time-on-task: Mara completes the income step in 60 seconds or less (assumption).
- Safety: 0 explainer texts with outcome promises, 100% compliance sign-off before release, and missed payments stay at or below 19.0%.

## MoSCoW scope
- **Must:** Short plain-language help text at the income question, readable on mobile without scrolling; Clear rule for which income to enter (a typical month for variable or shift income); Statement on how the income data is used and how long it is kept; Compliance approval of the German text before launch
- **Should:** One line on what happens after a missed payment; "Talk to an agent" link inside the explainer for vulnerable consumers; Tracking events: explainer opened, income step completed; Quick wording test with 3 to 5 consumers
- **Could:** Short example for variable income ("If your pay changes, enter a typical month"); A/B test of different wordings; Reuse of the text in letters, chat and other markets
- **Won't (now):** Affordability calculation (B3); Automated income decision or scoring model; Multi-claim logic (B1); Changes to the upload step (B5) and the chat assistant (B8); Other languages or markets; Personalised text based on claims or income

