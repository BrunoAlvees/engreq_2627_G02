# Technique 4: Differentiation analysis

**Timing:** before elicitation (to prepare interviews), after competitor analysis
**Owner:** Liane Duarte
**Status:** in progress

## Why this technique
- Competitor analysis (technique 1) and market dynamics (technique 3) show **what already exists**. The interviews show **what stakeholders need**. Combining both shows **where FAIR-AMAP could offer more value** than existing solutions.
- It answers the business question: *why would an AMAP like the ones BioGoods works with use FAIR-AMAP instead of an existing platform, or instead of keeping Excel, Google Forms and WhatsApp?*
- It avoids two traps: specifying only what every competitor already does (no reason to choose FAIR-AMAP), or proposing "different" features nobody asked for.
- It turns the differences found into **candidate requirements** and **validation questions** for the next sessions.

## Objectives
1. **List the needs** gathered in the interviews, with the source session.
2. **Check, for each need, whether existing solutions cover it** (based on the competitor analysis).
3. **Identify gaps**: needs that no solution covers, or covers poorly for the context of Portuguese AMAPs.
4. **Propose differentiations** and turn them into **candidate requirements**.
5. **Prepare validation questions** to confirm with stakeholders whether the differentiation has real value.

## Inputs
- Summaries and addenda of the 23/09, 29/09 and 06/10 sessions (`docs/interviews`).
- Analysed documents (`docs/doc_AMAP`): [AMAP Porto Baixa order form](../doc_AMAP/FormularioEncomendas_AMAPPortoBaixa_PT.md) and [Público report on AMAP Porto](../doc_AMAP/ReportagemPublico_AMAPPorto_PT.md) (both in Portuguese).
- Feature matrix from competitor analysis (technique 1, Jakub Piwko) and market dynamics (technique 3, João Mata).
- List of example software (`docs/ExampleSoftwares.md`): GrownBy, Farmigo, CSAware, Local Food Marketplace.
- Current system described by stakeholders: Excel, Google Forms, email and WhatsApp (technique 2, Bruno Alves).

## Method
1. Extract a list of needs from the interviews, each with its source session and stakeholder (producer, co-producer, client).
2. For each need, check the competitor analysis matrix and classify it as:
   - **Covered**: existing solutions already solve it. It becomes a baseline requirement, not a differentiator.
   - **Partial**: it exists, but does not fit the AMAP model (e.g. designed for one-off sales rather than basket subscriptions).
   - **Gap**: none of the analysed solutions solves it.
3. For **partial** needs and **gaps**, fill in the differentiation grid (see below).
4. Review the group's initial hypotheses against what the interviews showed.
5. Take the validation questions to the next session and update the status of each proposal.

### Differentiation grid
For each proposal: **need** → **existing solution or gap** → **proposed differentiation** → **candidate requirement** → **validation question**.

## Needs identified so far

| # | Need | Source | Market coverage |
|---|---|---|---|
| N1 | Know the basket contents before delivery, without relying on a weekly WhatsApp message | 29/09 (producer) | *to be filled in* |
| N2 | See **per person** what each co-producer receives, with exclusions (allergies, intolerances, dislikes) and substitutions | 29/09 (producer), 06/10 (co-producer) | *to be filled in* |
| N3 | Confirm basket collection, done by the co-producer; today the space is not supervised and baskets have been left until the next day | 29/09, 06/10 | *to be filled in* |
| N4 | Report an absence and choose what happens to the basket from options defined by the AMAP (friend, donation, sharing with others, draw) | 29/09, 06/10 | *to be filled in* |
| N5 | Delivery date reminders | 29/09, 06/10 | *to be filled in* |
| N6 | Check what was ordered and how much is owed; today the co-producer keeps the form copy and copies the price tables | 06/10 (co-producer), form | *to be filled in* |
| N7 | Different payment rules per producer and even per product (monthly with a payment note, at each delivery, meat only after weighing) within the same AMAP | 06/10, form | *to be filled in* |
| N8 | Reduce the number of payment operations when there are several producers and co-producers | 23/09 (client) | *to be filled in* |
| N9 | Know how heavy the collection will be (co-producers who walk) | 06/10 | *to be filled in* |
| N10 | Receive occasional surplus offers, with quantity management by the producer | 06/10 | *to be filled in* |
| N11 | Easy access to the AMAP's rules | 06/10 | *to be filled in* |
| N12 | Early commitment renewal (about 3 months) so crops can be planned | 29/09 (producer) | *to be filled in* |
| N13 | Configurable subscription length and an open list of extra products | 29/09 | *to be filled in* |
| N14 | Single-producer and multi-producer AMAPs; multi-producer baskets as an ideal scenario | 29/09 | *to be filled in* |
| N15 | Indicators (KPIs) and reports for CSA-related organisations and researchers, aligned with the SDGs; AMAP Porto has already surveyed how many people it feeds | 23/09 (client), report | *to be filled in* |
| N16 | Limited capacity per product (vegetable basket, eggs, meat) and a waiting list for new members | form | *to be filled in* |
| N17 | Order in a structured way what today goes into the free-text comments: other quantities, partial dates (e.g. chicken), loose products instead of a basket, preferences | form | *to be filled in* |
| N18 | Producers state the deliveries they will miss or where the product is not guaranteed (bread, mushrooms), and ask for reconfirmation of rarely delivered orders (olive oil) | form | *to be filled in* |
| N19 | Keep the personal relationship between producers and co-producers; the software should not make the AMAP impersonal | 06/10, report | *to be filled in* |

## Review of initial hypotheses
The techniques README proposed three differentiation hypotheses. Based on the interviews:

| Hypothesis | Status after interviews | Related needs |
|---|---|---|
| Handling collection exceptions | **Strengthened.** Both stakeholders mentioned problems with collection and absences. | N3, N4, N5 |
| Seasonal basket balance | **Weakened.** In the 29/09 session, the producer said this probably has no impact on the software. | — |
| Simplifying payments to multiple producers | **Strengthened.** Each producer has its own rules and the co-producer has no simple way to know how much is owed. | N6, N7, N8 |

## Provisional classification of N10–N19

Before the competitor analysis matrix is available, needs N10–N19 were split into those that look like **baseline requirements** (features common in CSA tools, to be confirmed with technique 1) and those that may lead to **differentiation**.

| Need | Provisional classification | Rationale | Proposal |
|---|---|---|---|
| N10 Surplus offers | Possible differentiation | One-off sales exist in online stores, but are not linked to the basket subscription | D4 |
| N11 Access to the AMAP's rules | Baseline requirement | Simple information page, no differentiating value | — |
| N12 Early renewal | Baseline requirement | CSA tools manage season/contract renewal | — |
| N13 Configurable length and extras | Baseline requirement | Contracts and extra products already exist in tools such as AMAPJ and Juntagrico | — |
| N14 Single- and multi-producer | Baseline requirement, to be confirmed | Depends on how the analysed tools handle several producers in the same AMAP | — |
| N15 KPIs and reports (SDGs) | To be validated | Client request; still unclear who uses the reports and whether it is in the initial scope | — |
| N16 Capacity and waiting list | Possible differentiation | Managed by hand in the form today | D4 |
| N17 Structured ordering | Possible differentiation | Today it goes into free-text comments that someone has to read and copy into Excel | D4 |
| N18 Producer gaps and reconfirmations | Possible differentiation | Today these are notes in the form, not linked to the delivery calendar | D4 |
| N19 Personal relationship | Possible differentiation | Commercial platforms treat the co-producer as a shop customer | D5 |

## Differentiation proposals (draft)
The following proposals still depend on the competitor analysis. They are not demonstrated competitive advantages or agreed requirements.

### D1: Collection and absences
- **Need:** N3, N4, N5.
- **Existing solution or gap:** *to be filled in from the competitor analysis.*
- **Proposed differentiation:** a complete flow around each delivery: reminder, absence notice with a choice of what happens to the basket, collection confirmation by the co-producer, and an alert to the producer when a basket is not collected.
- **Candidate requirements:**
  - The system shall allow the co-producer to confirm basket collection.
  - The system shall allow the co-producer to report an absence and choose what happens to the basket from the options defined by the AMAP.
  - The system shall notify the producer of uncollected baskets on the delivery day.
- **Validation questions:** should confirmation be mandatory? Who receives the alert when a basket is not collected? What happens if nobody confirms?

### D2: Payments with multiple producers
- **Need:** N6, N7, N8.
- **Existing solution or gap:** *to be filled in from the competitor analysis.*
- **Proposed differentiation:** a monthly summary per co-producer showing the amount owed to each producer, calculated according to each producer's rules (fixed monthly fee, at each delivery or after weighing), plus order history. Today each producer sends its own payment note.
- **Candidate requirements:**
  - The system shall allow each producer's payment rule to be configured.
  - The system shall show the co-producer the amount owed to each producer each month.
  - The system shall allow the co-producer to view the orders placed in the period.
- **Validation questions:** does the AMAP want to centralise payments or keep paying each producer directly? Who issues the invoice in each case?

### D3: Personalised basket and information before delivery
- **Need:** N1, N2, N9.
- **Existing solution or gap:** *to be filled in from the competitor analysis.*
- **Proposed differentiation:** basket contents published by the producer and shown to each co-producer with their exclusions and substitutions already applied, and the approximate weight.
- **Candidate requirements:**
  - The system shall allow the producer to publish the basket contents for each delivery.
  - The system shall show each co-producer their basket, taking registered exclusions into account.
- **Validation questions:** is the weight useful for everyone or only some co-producers? Does the producer have time to publish the contents every week?

### D4: Flexible orders and capacity
- **Need:** N10, N16, N17, N18.
- **Existing solution or gap:** *to be filled in from the competitor analysis.*
- **Proposed differentiation:** replace the form's free-text comments with structured options: quantities and dates per product, loose products, maximum capacity per product with a waiting list, a producer calendar showing the deliveries they will miss or where the product is not guaranteed, reconfirmation requests, and surplus offers with limited quantities.
- **Candidate requirements:**
  - The system shall allow the producer to set the maximum capacity of each product and put new co-producers on a waiting list when that capacity is reached.
  - The system shall allow the co-producer to choose the quantity and delivery dates of each product without using free-text comments.
  - The system shall allow the producer to indicate the deliveries they will miss or where the product is not guaranteed.
  - The system shall allow the producer to request reconfirmation of infrequent orders.
  - The system shall allow the producer to publish surplus offers with limited quantities.
- **Validation questions:** who manages the waiting list, the producer or the AMAP coordination? Which requests appear most often in the comments? Are surpluses allocated first-come first-served or some other way? How far in advance does the producer know they will miss a delivery?

### D5: Software that keeps the personal relationship
- **Need:** N19.
- **Existing solution or gap:** *to be filled in from the competitor analysis.*
- **Proposed differentiation:** treat the personal relationship as a design principle rather than a feature: the software handles management (orders, payments, absences) to free up time for direct contact, shows who the producer is and lets them communicate with their co-producers, without the shop logic (catalogue, cart, commissions) of commercial platforms.
- **Candidate requirements:**
  - The system shall allow the producer to introduce themselves to co-producers (farm, production method).
  - The system shall allow the producer to send news and notices to the co-producers of their AMAP.
- **Caution:** D1 and D3 automate moments that are personal contact today (confirming collection, finding out what is in the basket). It must be validated that this does not go against this need.
- **Validation questions:** what would make the AMAP impersonal, in the stakeholders' view? Would they rather keep WhatsApp for informal communication and use the software only for management? Are there moments they do not want automated?

## Expected results (evidence)
- Table of needs with market coverage classification.
- Differentiation grid filled in for partial needs and gaps.
- List of differentiating candidate requirements.
- Validation questions for the next session and their answers.
- Hours logged per team member.

## Work log
| Date | Member | Task | Hours |
|---|---|---|---|
| 07/10 | Liane Duarte | Objectives, method, needs from interviews and initial proposals | 2.0 |
| 14/10 | Liane Duarte | PT/EN sync, provisional classification of N10–N19, proposals D4 and D5 | 1.0 |
