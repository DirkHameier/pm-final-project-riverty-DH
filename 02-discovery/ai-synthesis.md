# AI Synthesis, Product Health & Insights Summary (Module 2)

## Responses
- **Assumption to validate #1:** Lack of understanding of the process
- **Assumption to validate #2:** The process is often interrupted before completion
- **Assumption to validate #3:** Proposed installment amounts are not acceptable for many consumers
- **Moment of misery / red flag #1 (e.g., “user gave up after 3 tries”):** N-03, consumer, two open claims: “I could only see one claim at a time. I did not know if paying one would stop the letters about the other.”
- **Moment of misery / red flag #2:** N-01, consumer, two open claims, shift work: “I opened it on my break. It asked for my income and I did not know if they meant this month or a normal month. I closed it and meant to come back.”
- **Moment of misery / red flag #3:** N-02, consumer, one claim: “I picked the plan with the lowest number of months because it looked like the right answer. The amount was too high and I missed the second payment.”
- **Product Health & Insights Summary (Claude's output):** # Product Health & Insights Summary

**Executive Summary**
The platform is mostly stable, but a few technical faults and data inconsistencies undermine the consumer journey at the moments that matter most: income disclosure, plan selection, and the first payment. Consumers lack clarity about what they are agreeing to and what happens if they miss a payment, so many abandon the journey or choose a plan that does not fit them. Agents cannot see what consumers entered or why a plan was offered, which increases support load and creates complaint risk that clients monitor closely.

---

## 1. Technical Stability

Several defects interrupt the journey at key steps, and they hit mobile and shift-working consumers hardest. The most visible one is the document upload failure, which affects a large number of journeys. Smaller faults, such as lost answers and badly timed reminders, add friction and can lead directly to missed payments.

- **Income document upload times out on mobile (large photos):** 853 journeys in the sample month requested a document that never arrived. **Severity: Critical**
- **Reminder before the first instalment is sent after the due date in some cases:** this increases the risk of missed first payments and broken plans. **Severity: High**
- **Back button on the plan review screen clears affordability answers:** consumers must re-enter sensitive data. **Severity: Medium**

## 2. Onboarding & UX

Consumers interrupt the journey when questions are ambiguous or when the portal does not match their situation. Shift workers and consumers with several claims are particularly affected. Plan selection relies on assumptions (for example, "fewer months must be the right answer") instead of guidance on affordability.

- **No way to set up one plan for two or more claims:** the portal shows claims one at a time, and consumers do not know whether paying one claim stops letters about the other. **Severity: High**
- **Ambiguous income question:** consumers do not know whether "income" means this month or a normal month, and some abandon the journey. **Severity: High**
- **Plan selection without affordability guidance:** a consumer chose the shortest plan, found the amount too high, and missed the second payment. **Severity: High**
- **Preference for phone contact:** some consumers do not trust a digital journey to tell them the real cost. **Severity: Low**

## 3. Trust & Clarity

Trust is the main barrier to digital adoption. Consumers are unsure why their data is collected, how long it is kept, and whether it could be used against them. Amounts that differ between the portal and the letter make this worse, especially for purchased portfolios, where consumers say they will not agree to anything until someone explains the difference.

- **Portal amount differs from the letter:** 531 journeys in the sample month were affected, 343 of them in purchased portfolios. **Severity: Critical**
- **No help text on why income is asked or how long it is kept:** consumers fear that their input may be used against them, especially those in financial difficulty. **Severity: High**
- **Chat assistant confirms plans without explaining the consequences of a missed payment:** consumers get a fast "yes" but remain unsure about the risks. **Severity: High**

## 4. Support Load & Agent Enablement

Agents work without context. They cannot see what the consumer entered online, so they ask for the same details again, and they cannot see why a plan was offered, so they struggle to understand and handle failures. This lengthens calls and reduces consumers' confidence in the process. Compliance also expects every decision to be explainable to both consumers and agents.

- **Agent screen does not show consumer-entered data:** agents repeat questions, which frustrates consumers and lengthens calls. **Severity: High**
- **No visibility of why a plan was offered:** agents see only a number, which limits root-cause analysis when plans fail. **Severity: High**
- **Explainability requirement:** decisions must be traceable for consumers, agents, and compliance. **Severity: Medium**

## 5. Client & Portfolio Risk

Clients value low complaint levels as much as recovery. Spikes in broken plans appear in their reporting, so the issues above have a direct commercial impact. Inconsistent data across acquired portfolios limits reliability, particularly for contact and address history.

- **Broken plans and complaints are visible in client reporting:** this creates relationship and reputation risk. **Severity: High**
- **Inconsistent data quality across acquired portfolios:** some portfolios lack reliable phone or address history. **Severity: Medium**

---

**Minor Technical Debt:** Isolated wording inconsistencies, minor interface preferences, and small data gaps that do not currently block journeys or payments.
- **Did the AI catch the specific moment of misery / pain point you found in Step 1?:** Partly, yes, but not all
- **Did it smooth over a critical frustration into a generic bullet point?:** No
- **Did the AI try to suggest features or a roadmap despite the constraints?:** No, it wasn’t suggested
- **Logic leak / hallucination #1 (e.g., “AI suggested a new search bar feature, roadmap leak”):** _(not filled in)_
- **Logic leak / hallucination #2:** _(not filled in)_
