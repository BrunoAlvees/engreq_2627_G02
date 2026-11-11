# Technique 4: Differentiation analysis

**Timing:** started before elicitation (to prepare interviews), after the competitor analysis; completed after the last session with the client (10/11)
**Owner:** Liane Duarte
**Status:** completed

## Why this technique

- The competitor analysis (technique 1) and market dynamics (technique 3) show **what already exists**. The interviews show **what stakeholders need**. The two must be crossed to understand **where FAIR-AMAP can offer more value** than existing solutions.
- It answers the business question: *why would an AMAP like those of BioGoods use FAIR-AMAP instead of an existing platform, or instead of carrying on with Excel, Google Forms and WhatsApp?*
- It avoids two traps: specifying only what every competitor already does (no reason to choose FAIR-AMAP), or proposing "different" features nobody asked for.
- It turns the differences found into **candidate requirements** and **validation questions**.

## Objectives

1. **List the needs** gathered in the interviews, with the session they came from.
2. **Check, for each need, whether existing solutions cover it** (based on the competitor analysis).
3. **Identify gaps**: needs that no solution covers, or covers poorly for the context of Portuguese AMAPs.
4. **Propose differentiators** and turn them into **candidate requirements**.
5. **Prepare validation questions** to confirm with stakeholders whether the differentiation has real value.

## Inputs

- Summaries and complements of the sessions of 23/09, 29/09 and 06/10 and the interview of 10/11 (E-8) (`docs/interviews`).
- Analysed documents (`docs/doc_AMAP`): [AMAP Porto Baixa order form](../doc_AMAP/FormularioEncomendas_AMAPPortoBaixa_PT.md) and [Público report on AMAP Porto](../doc_AMAP/ReportagemPublico_AMAPPorto_PT.md) (both in Portuguese).
- Feature matrix from the competitor analysis ([technique 1](CompetitorAnalysis.md), Jakub Piwko): AMAPJ, Juntagrico, Katuma (Open Food Network) and Local Line, and the market gaps identified. Market dynamics ([technique 3](MarketDynamic.md), João Mata) has no results yet, so it was not used.
- Example solutions ("Other solutions considered" section of [technique 1](CompetitorAnalysis.md)): GrownBy, Farmigo, CSAware and Local Food Marketplace. Their websites were consulted on 11/11/2026 (see "Example solutions" below).
- Current system described by stakeholders: Excel, Google Forms, email and WhatsApp (technique 2, Bruno Alves).
- Final list of requirements ([requirements](../requisitos/README.md)): FR-01 to FR-45 and NFR-01 to NFR-24.

## Method

1. Extract a list of needs from the interviews, each with its source session and stakeholder (producer, co-producer, client).
2. For each need, check the competitor analysis matrix and the websites of the example solutions, and classify the coverage:
   - **Covered**: at least one of the solutions analysed has the feature. It becomes a baseline requirement, not a differentiator.
   - **Partial**: it exists but does not fit the AMAP model (e.g. designed for one-off sales rather than basket subscriptions, or for a single producer).
   - **Not mentioned**: the feature does not appear in technique 1 or on the websites consulted. It is treated as a likely gap, but not a proven one (see "Limitations").
3. For **partial** and **not mentioned** needs, fill in the differentiation grid (see below).
4. Review the group's initial hypotheses against what the interviews showed.
5. Take the validation questions to the following sessions and record the answers. Those still unanswered after the last session (10/11) become a group decision, consistent with sections 2.5 and 10.4 of the SRS.
6. Link each proposal to the final requirements.

### Differentiation grid

For each proposal: **need** → **existing solution or gap** → **proposed differentiation** → **requirements** → **validation**.

## Example solutions

The websites of the four example solutions were consulted on 11/11/2026, to complement the technique 1 matrix. The information comes only from what each website publishes.

| | GrownBy | Farmigo | CSAware | Local Food Marketplace |
|---|---|---|---|---|
| **What it is** | Direct-sales app from farms to consumers, owned by a farmers' cooperative | CSA management software for farms, herdshares and food hubs | CSA and food hub management software, by LocalHarvest | Software for food hubs, farms and CSAs |
| **Country and language** | USA, English | USA (likely), English | USA, English | USA, English |
| **Subscriptions** | Seasonal shares, customisable, priced per pickup | Fixed or customisable shares; bi-weekly, seasonal or year-round | Fixed or customisable shares | Perpetual or seasonal subscriptions, customisable shares |
| **Customisation** | Add-ons (eggs, meat, mushrooms) | Holds, swaps, pickup changes, add-ons, gifting | List of items to avoid, add-ons, subscription holds | Swaps, add-ons, bundles |
| **Pickup** | Pickup location per subscription | Several sites, day-of attendance lists, packing lists | Labels and sign-in sheets, packing lists, drop sites with capacity | Pick lists, labels, delivery routes |
| **Communication** | Not stated | Not detailed | Newsletters, blog, SMS reminders | "What's in the Box" emails, renewal reminders, SMS |
| **Capacity** | Not stated | Signup caps and waitlists | Capacity per drop site | Not stated |
| **Payments** | Online, SNAP/EBT | ACH, card, cheque, auto-charge | Card, PayPal, eCheck, SNAP | Card, e-check; automated producer payments (Stripe), in the food hub model |
| **Several producers** | Marketplace with several farms, each with its own shop | Not mentioned | Not mentioned | Food hub selling products from several producers |
| **Price** | Not stated | 2% of sales, minimum $150/month | 2% of sales, minimum $100/month | $129 to $349/month, plus add-on modules |

**What they show:** subscription management features (add-ons, swaps, holds, reminders, basket contents, capacity) are already common in the US market. None of the four is in Portuguese, mentions Europe or the GDPR, accepts MB Way, or brings several producers together in one CSA with a single payment and no intermediary. Those that show a price charge a percentage of sales with a monthly minimum, or a fixed monthly fee.

## Needs and market coverage

Type: **Baseline** (a requirement expected in any solution, with no differentiating value) · **Differentiator** (FAIR-AMAP can do better than the solutions analysed).

| # | Need | Source | Market coverage | Type | Requirements |
|---|---|---|---|---|---|
| N1 | Know the basket contents before delivery, without relying on a weekly WhatsApp message | 29/09 (producer) | Covered: "What's in the Box" emails (Local Food Marketplace) | Baseline | FR-25 |
| N2 | See, **person by person**, what each co-producer receives, with exclusions (allergies, intolerances, dislikes) and substitutions | 29/09 (producer), 06/10 (co-producer) | Partial: list of items to avoid (CSAware) and swaps (Farmigo, Local Food Marketplace); allergies and the person-by-person view for the producer are not mentioned | Differentiator (D3) | FR-19, FR-25, NFR-06 |
| N3 | Collection confirmed by the co-producer; today the space is unattended and baskets have been left until the next day | 29/09, 06/10, 10/11 | Partial: attendance lists (Farmigo), sign-in sheets and labels (CSAware), distributions (AMAPJ, Juntagrico); confirmation by the co-producer in the app is not mentioned | Differentiator (D1) | FR-28, FR-29, NFR-12 |
| N4 | Report an absence and choose what happens to the basket from options set by the AMAP (friend, donation, sharing among the others, raffle) | 29/09, 06/10 | Partial: holds and pickup changes (Farmigo, CSAware); choosing what happens to the basket is not mentioned | Differentiator (D1) | FR-27 |
| N5 | Reminders of delivery dates | 29/09, 06/10 | Covered: SMS reminders (CSAware, Local Food Marketplace) | Baseline | FR-35 |
| N6 | Check what was ordered and how much is owed; today the co-producer keeps a copy of the form and copies the price tables | 06/10 (co-producer), form | Partial: contracts (AMAPJ) and outstanding balances (CSAware), but per farm | Differentiator (D2) | FR-21, FR-31 |
| N7 | Different payment rules per producer and even per product (monthly with a payment note, at each delivery, meat only after weighing) within the same AMAP | 06/10, form | Partial: AMAPJ has a treasurer role and the other solutions online payments, designed for one farm; different rules per producer in the same AMAP are not mentioned | Differentiator (D2) | FR-30, FR-31, NFR-24 |
| N8 | Reduce the number of payment transactions when there are several producers and co-producers | 23/09 (client) | Partial: Local Food Marketplace pays producers automatically, but in the food hub model, where the hub is the seller; a single payment split among several producers with no intermediary is not mentioned. None accepts MB Way | Differentiator (D2) | FR-32, FR-33, NFR-17, NFR-19 |
| N9 | Know how much the collection weighs (co-producers who walk) | 06/10 | Not mentioned | Differentiator (D3) | FR-25 |
| N10 | Receive one-off surplus offers, with quantities managed by the producer | 06/10 | Covered: add-on shops linked to the subscription (Farmigo, CSAware, Local Food Marketplace, GrownBy) | Baseline | FR-16 |
| N11 | Easy access to the AMAP rules | 06/10 | Not mentioned | Baseline | FR-39 |
| N12 | Early renewal of the commitment (about 3 months), to plan crops | 29/09 (producer) | Covered: seasonal contracts (AMAPJ), subscriptions (Juntagrico, Local Line) and renewal reminders (Local Food Marketplace) | Baseline | FR-22 |
| N13 | Configurable subscription length and an open list of extra products | 29/09 | Covered: contracts (AMAPJ), seasonal, bi-weekly or year-round subscriptions (Farmigo), add-ons (all) | Baseline | FR-11, FR-17 |
| N14 | Single-producer and multi-producer AMAPs; multi-producer baskets as the ideal scenario | 29/09 | Covered: AMAPJ has contracts and a referent role per producer, and Katuma and Local Food Marketplace bring several producers together in a hub. Multi-producer baskets were left out of scope | Baseline | FR-01 |
| N15 | Indicators (KPIs) and reports for CSA-related organisations and researchers, aligned with the SDGs; AMAP Porto has already surveyed how many people it feeds | 23/09 (client), report | Not mentioned | Differentiator (client request, low priority) | FR-43, FR-44 |
| N16 | Limited capacity per product and per AMAP, and a waiting list for new members | form, 10/11 | Partial: signup caps and waitlists (Farmigo), capacity per drop site (CSAware); capacity per producer within the same AMAP is not mentioned | Differentiator (D4) | FR-03, FR-14 |
| N17 | Order in a structured way what today goes into free-text comments: other quantities, partial dates (e.g. chicken), single products instead of a basket, preferences | form | Partly covered: customisable shares, swaps and add-ons (Farmigo, CSAware, Local Food Marketplace); choosing the dates of each product is not mentioned | Baseline, with per-producer rules (D4) | FR-18, FR-20 |
| N18 | Producers state the deliveries they will miss or where the product is not guaranteed (bread, mushrooms), and ask for reconfirmation of infrequent orders (olive oil) | form | Not mentioned | Differentiator (D4) | FR-20, FR-24, FR-26 |
| N19 | Keep the personal relationship between producers and co-producers; the software must not make the AMAP impersonal | 06/10, report | Partial: AMAPJ and Juntagrico focus on organisation; Katuma, Local Line, GrownBy and Local Food Marketplace follow a shop or food hub logic, and technique 1 concludes that commissions on baskets clash with AMAP ethics | Differentiator (D5) | FR-04, FR-37, FR-40, NFR-20 |

Besides these needs, technique 1 identified **market gaps** that did not come from the interviews but reinforce the differentiation (D6): a Portuguese interface (only Katuma has one), MB Way payment, one instance shared by all Portuguese AMAPs and little effort required from producers. The example solutions confirm these gaps: they are all American, in English, with US payment methods.

## Review of the initial hypotheses

The techniques README proposed three differentiation hypotheses. In light of the interviews and the session of 10/11:

| Hypothesis | Final status | Related needs |
|---|---|---|
| Handling pickup exceptions | **Confirmed.** Both stakeholders mentioned problems with collection and absences, and AMAP management said on 10/11 that it is essential for the co-producer to confirm collection in the app. The solutions analysed handle holds, but not what happens to the basket or confirmation by the co-producer. | N3, N4, N5 |
| Seasonal basket balance | **Dropped.** In the 29/09 session, the producer said this probably has no impact on the software. | — |
| Simpler payments to several producers | **Confirmed.** Each producer has its own rules and the co-producer has no simple way to know how much is owed. On 10/11, FAIR accepted centralised collection. | N6, N7, N8 |

## Differentiation proposals

The coverage stated comes from technique 1 and the example solutions. Validation gives the answer obtained or, where there was none, the group's decision.

### D1: Collection and absences

- **Need:** N3, N4 (N5 is baseline).
- **Existing solution or gap:** the solutions have lists for whoever runs the distribution (attendance lists in Farmigo, sign-in sheets and labels in CSAware) and allow subscriptions to be put on hold. None mentions collection confirmed by the co-producer or choosing what happens to the basket during an absence (friend, donation, sharing, raffle).
- **Proposed differentiation:** a complete flow around each delivery, on the co-producer's side: reminder, absence notice with a choice of what happens to the basket, collection confirmation in the app and an alert to the producer when a basket is not collected. It works at unattended sites.
- **Requirements:** FR-27 (absences), FR-28 (collection confirmation), FR-29 (distribution sheet and labels), FR-35 (reminders), NFR-12 (confirmation with a weak network).
- **Validation:**
  - *Should confirmation be mandatory?* **Answered (E-8):** it is essential that the co-producer can report collection in the app, with a button. A label with a QR code is optional, for those with a printer.
  - *Who gets the alert? What happens if nobody confirms?* Unanswered. **Group decision:** the system flags uncollected baskets to the producer and management (FR-28).

### D2: Payments with several producers

- **Need:** N6, N7, N8.
- **Existing solution or gap:** the solutions analysed take online payments for one farm. Local Food Marketplace pays several producers, but in the food hub model, where the hub sells the products; that would make the platform an intermediary, which the AMAP Charter of Principles excludes. None accepts MB Way.
- **Proposed differentiation:** the co-producer makes a single payment per period, calculated with each producer's rules and split among producers through a licensed payment provider, without the platform selling or holding the money. The co-producer sees what is owed to each producer and the order history, and each producer gets a summary of who paid.
- **Requirements:** FR-21 (history), FR-30 (payment rules), FR-31 (calculation per producer), FR-32 (single split payment), FR-33 (tracking), NFR-17 (payment provider), NFR-19 (the system does not hold the money), NFR-20 (no commercial intermediation).
- **Validation:**
  - *Does the AMAP want centralised payments?* **Answered (E-8):** FAIR accepted centralised collection; payment method fees are a producer cost or are deducted transparently.
  - *Who issues the invoice?* **Answered (E-6):** invoicing is out of scope; each producer invoices in their own software (NFR-18).

### D3: Personalised basket and information before delivery

- **Need:** N2, N9 (N1 is baseline).
- **Existing solution or gap:** publishing the basket contents already exists ("What's in the Box" emails in Local Food Marketplace) and CSAware has a list of items to avoid. Allergies, the person-by-person view for the producer and the weight are not mentioned.
- **Proposed differentiation:** basket contents shown to each co-producer with their exclusions and substitutions already applied, and a list for the producer of what each person receives. Allergies are handled as health data.
- **Requirements:** FR-19 (exclusions and substitutions), FR-25 (basket contents), NFR-06 (health data only with consent).
- **Validation:** *is the weight useful to everyone? Does the producer have time to publish the contents?* Unanswered, because no producer was interviewed in the last session. **Group decision:** basket contents are a requirement (FR-25); the approximate weight did not become a requirement of its own. This differentiator is weak: the main part already exists on the market.

### D4: Flexible orders and capacity

- **Need:** N16, N18 (N10 and N17 are baseline).
- **Existing solution or gap:** add-ons, swaps and customisable shares are already common (Farmigo, CSAware, Local Food Marketplace, GrownBy), and Farmigo has signup caps with waitlists. Capacity per producer within the same AMAP, each producer's own rules (change deadlines, partial dates) and producers stating the deliveries they will miss are not mentioned.
- **Proposed differentiation:** the common part (add-ons, swaps, waiting list) is baseline. The difference lies in what is specific to an AMAP with several producers: capacity of the AMAP and of each producer, each producer's change rules, a producer calendar with the deliveries they will miss or where the product is not guaranteed, and reconfirmation requests.
- **Requirements:** FR-03 (joining and waiting list), FR-14 (capacity), FR-16 (one-off offers), FR-18 (structured subscription), FR-20 (deadlines and changes), FR-24 (calendar), FR-26 (availability and shortages).
- **Validation:**
  - *Who manages the waiting list?* **Answered (E-8):** capacity exists at two levels, the AMAP and each producer; an accepted application becomes active or goes to the waiting list; management accepts members.
  - *What requests appear in the comments? How are surpluses allocated? How far ahead does the producer know they will miss a delivery?* Unanswered. **Group decision:** rules are configurable per producer (FR-20, NFR-24) and the producer records shortages when known (FR-26).

### D5: Software that keeps the personal relationship

- **Need:** N19.
- **Existing solution or gap:** AMAPJ and Juntagrico focus on organisation, and Juntagrico coordinates volunteer work. Katuma, Local Line, GrownBy and Local Food Marketplace follow a shop or food hub logic (catalogue, cart, commissions), which technique 1 considers contrary to AMAP ethics. Farmigo and CSAware are management tools for one farm, with no volunteer organisation.
- **Proposed differentiation:** treat the personal relationship as a design principle rather than a feature: the software handles management (orders, payments, absences) to free time for direct contact, shows who the producer is, lets them communicate with their co-producers and supports the AMAP's volunteer organisation, without acting as a commercial intermediary.
- **Requirements:** FR-04 (producer profile), FR-37 (producer communication), FR-40 (volunteer organisation), NFR-20 (no commercial intermediation). Exclusions are recorded by the co-producer's choice and visible only to the producer (FR-19, NFR-06).
- **Validation:** *should exclusions be in the system? What would make the AMAP impersonal? Would they rather keep WhatsApp?* Unanswered. **Group decision:** exclusions recorded with consent and visible only to the producer (FR-19, NFR-06); WhatsApp remains a possible channel (NFR-15, Could). In the 10/11 session, management stressed that AMAPs follow principles of fairness and trust, which is consistent with this proposal.

### D6: A Portuguese, shared and affordable platform

- **Need:** market gaps from technique 1 and the client's request to serve several AMAPs (E-8).
- **Existing solution or gap:** only Katuma has a Portuguese interface, and it is a shop platform. The organisation tools (AMAPJ, Juntagrico) are not in Portuguese, and technique 1 identifies the lack of an instance shared by Portuguese AMAPs as a gap. The commercial solutions are American, in English, with US payment methods, and charge 2% of sales with a minimum of $100 to $150 per month (Farmigo, CSAware), a monthly fee of $129 to $349 (Local Food Marketplace) or from $79 per month (Local Line). For an AMAP of 30 to 50 co-producers, these costs are high.
- **Proposed differentiation:** one platform in Portuguese for several AMAPs, each with its own rules, with MB Way and GDPR compliance, almost free during the pilot and with a fee per AMAP afterwards, which imports existing data and takes little of the producers' time.
- **Requirements:** NFR-13 (European Portuguese), NFR-22 (multi-AMAP), NFR-24 (configurable rules), NFR-17 (payment provider, e.g. MB Way), NFR-08 (GDPR), NFR-21 (pricing model and pilot), FR-45 (data import), NFR-02 (quick tasks).
- **Validation:** **Partly answered (E-8):** FAIR wants to serve several AMAPs with their own rules and plans an almost free pilot in Portugal. The time targets (NFR-02) were not validated and remain a group proposal.

### Ideas seen in the example solutions

Some features of the example solutions are not in the requirements. They were not validated with stakeholders and are recorded for a future iteration:
- swaps made by the co-producer themselves (FR-19 covers substitutions made by the producer);
- changing the pickup point for one date;
- giving a basket to someone else.

## Conclusions

**What is baseline** (already exists in the solutions analysed and FAIR-AMAP must have it, but it does not set it apart): cycles and contracts with configurable length, catalogue and add-ons, swaps and customisable shares, basket contents before delivery, renewal, waiting list, several producers per AMAP, roles, reminders and access to the rules (N1, N5, N10 to N14, N17).

**What sets FAIR-AMAP apart:**
1. **A Portuguese, shared, configurable and affordable platform** (D6). All the solutions analysed except Katuma are in English only, and the commercial ones charge a percentage of sales or a monthly fee that is high for a small AMAP.
2. **A single payment split among several producers, with no intermediary** (D2). None of the solutions analysed does this without acting as the seller, and FAIR accepted it.
3. **Collection and absences on the co-producer's side** (D1): collection confirmation in the app and a choice of what happens to the basket. The solutions analysed only have lists for whoever distributes, and holds.
4. **Rules for several producers within the same AMAP** (D4): capacity per producer, each producer's change rules and shortages.
5. **An organisation tool, not a shop**, that keeps the personal relationship and supports volunteer organisation (D5).

The personalised basket (D3) and the indicators (N15) have value, but the main part of D3 already exists on the market and both depend on validation with producers that could not be done.

These conclusions feed the project scope (SRS section 1.3) and the summary of techniques (section 10.2).

## Limitations

- Coverage comes from the technique 1 matrix and the websites of the example solutions, based on public information. "Not mentioned" means the feature is not mentioned, not that the solution lacks it. No solution was tried from the inside.
- The GrownBy website mainly shows the shop for consumers; features for farms and the price are not on the home page.
- No producer was interviewed in the 10/11 session, so the questions in D3 and part of D4 remained unanswered (see SRS section 10.4).

## Results (evidence)

- Table of needs with market coverage and type (baseline or differentiator).
- Comparison of the example solutions.
- Completed differentiation grid (D1 to D6), with the final requirements.
- Answers to the validation questions and group decisions.
- Conclusions on how FAIR-AMAP differentiates itself.
- Hours logged per group member.

## Work log

| Date | Member | Task | Hours |
|---|---|---|---|
| 30/09 | Liane Duarte | Search for examples of similar software (GrownBy, Farmigo, CSAware, Local Food Marketplace) | 0.5 |
| 07/10 | Liane Duarte | Objectives, method, needs from interviews and initial proposals | 2.0 |
| 14/10 | Liane Duarte | PT/EN sync, provisional classification of N10–N19, proposals D4 and D5 | 1.0 |
| 11/11 | Liane Duarte | Analysis of the example solutions' websites, coverage of N1–N19, E-8 answers, link to the final requirements, proposal D6, conclusions and limitations | 2.5 |
