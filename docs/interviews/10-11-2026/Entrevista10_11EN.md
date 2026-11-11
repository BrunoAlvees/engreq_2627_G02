# FAIR-AMAP - Stakeholder interview of 10/11

**Updated on:** 10/11/2026 · Source in the requirements: **E-8**

This document summarises the interview held in the PL class of 10/11/2026 (30 minutes). The lecturer played the stakeholders: **FAIR representative** (client) and **AMAP management**. The interview guide is in [PerguntasEntrevista10_11PT](PerguntasEntrevista10_11PT.md).

The information was noted down during the interview. Unclear points are marked "to confirm".

## 1. FAIR representative

### 1.1. Business model
- FAIR plans a **pilot in Portugal**, where the software is offered **almost free of charge** to collect feedback. The number of AMAPs in Portugal is not enough to justify the business.
- In the future, FAIR plans to charge a **minimum fee per AMAP** plus a **percentage of the transaction value**.
- Transactions are **payments to producers**.

### 1.2. Payments
- The group proposed collecting payments through a provider (such as Stripe) and distributing them to the producers. The client **accepted** the proposal.
- **Payment method fees** (e.g. MB Way) are a **producer cost**: the prices they set must already account for that cost structure.
- Alternatively, the fee may be **deducted from the amount transferred** to the producer, as long as this is **transparent**.

### 1.3. An AMAP joining the platform
- The software must work for **several AMAPs**, each with its own rules.
- The AMAP **registers**, and someone at FAIR who manages the system **requests documentation**: AMAP name, location, representative, tax number (NIF), etc. Once submitted, the registration is done.

## 2. AMAP management

### 2.1. A producer joining
- A producer can **apply** or be **invited**. An invited producer is invited to apply, with the selection practically made.
- The application is a page where the producer states:
  - name and location;
  - the products that characterise them and the most important ones;
  - the farming method (organic or not).
- They can upload documents, such as an organic certificate, Demeter, GRASP or GlobalG.A.P. *(names to confirm)*.
- These are used by the **AMAP management to assess** the application. Typically there is a **visit** to the farm, and then the producer is selected or not.
- A selected producer becomes an **active producer**.
- The process may vary between AMAPs, but there is always a **producer registration**.
- **AMAP started by a producer:** they register the AMAP. Once the AMAP is authorised, they hold both the **manager and producer** roles: they apply as a producer and accept the application as manager.
- A producer can be in **several AMAPs**.

### 2.2. Places and capacity
- The limit on places applies **mainly to co-producers**.
- Producers can be registered as active or not. An accepted application, from a producer or a co-producer, can become **active** or go to the **waiting list** if there are no places.
- Capacity exists **at two levels**:
  - The **AMAP** may have a maximum capacity (e.g. 100), which depends on the premises, transport capacity and space.
  - **Each producer** states how many co-producers they accept. Example: one fruit producer delivers 25 baskets and another 30 more, so 55 co-producers can subscribe to fruit.

### 2.3. A producer leaving
- It is **very uncommon**.
- **At the end of a subscription period:** the producer is no longer active.
- **In the middle of a period:** they stop delivering, the planned deliveries are **cancelled** and **accounts must be settled** (refund).

### 2.4. A co-producer leaving
- The rule is to leave **at the end of the subscription period**, but in some circumstances they may leave earlier.
- The withdrawal **must be accepted**. If accepted, the producers with whom the co-producer had subscriptions (e.g. a vegetable basket for 6 months) are **informed** so they stop the deliveries, and the **payments are refunded**.
- What happens if it is not accepted **depends on how formal the AMAP is** *(unclear answer; to confirm)*.
- In practice, refusing is very strange in an AMAP, which follows principles of fairness and consistency. People usually leave because they move abroad. Many co-producers are **expatriates**, students abroad or **digital nomads** who already used AMAPs in their home country. Nobody takes them to court: they let people know, the producers are informed and it is fine.

### 2.5. Documents signed on joining
- **It depends on the AMAP.** Some (e.g. Sara's) use documents that are **almost contracts**, signed on paper. Whoever withdraws after paying does not get the money back. It is not meant for court, but it is a commitment.
- In more informal AMAPs, such as those in Porto, this does not happen.

### 2.6. Producers' tools
- **It depends a lot on the producer.** Larger ones may have software to support production; others will have very little.

### 2.7. Collection confirmation and labels
- In Porto there is always a **label with the name**. Sometimes it is **printed**, sometimes **handwritten** (like the one on Luisa's basket).
- **Essential:** the application must let the co-producer **report that the basket was collected**.
- **Optional:** whoever has a printer prints the label with the name and a **QR code**, which is scanned to confirm collection. Whoever has no printer just **taps a button** in the application.

## 3. Impact on the requirements
| Topic | Requirements | Change |
|---|---|---|
| Pricing model | FR-34, NFR-21 | Minimum fee **per AMAP** (was per producer) + % of transactions; pilot almost free. Validated. |
| Centralized collection and fees | FR-32, NFR-19 | Accepted by FAIR; fees are a producer cost or deducted transparently. Validated. |
| AMAP registration | FR-01, FR-06 | Registration with documentation, authorised by the FAIR administrator. |
| Producer joining | FR-04, FR-08, PA-01, PA-03 | Application or invitation, certification documents, typical visit, assessment by management. PA-01 and PA-03 answered. |
| AMAP started by a producer | FR-06 | The producer holds the management and producer roles. |
| Capacity | FR-01, FR-14 | AMAP capacity + capacity per producer. |
| Producer leaving | FR-09, PA-04 | End of period: inactive. Mid-period: cancel deliveries and settle accounts. PA-04 partly answered. |
| Co-producer leaving | FR-07 | Only at the end of the period; mid-period if the withdrawal is accepted (with refund and producers notified); rules configurable per AMAP. |
| Collection | FR-28, FR-29 | In-app button mandatory; label with QR optional. Validated. |

## 4. Questions not asked
- To the **producer** (not interviewed): notice needed for planning, product shortages, compensation when a producer leaves, notice period for leaving (PA-04), when each product is charged (DV-18 to DV-20), price changes mid-cycle and cancelled deliveries (DV-17).
- To **management**: renewal (intention or mandatory confirmation), checking payments and late payments, who builds the order form and the calendar (DV-07, DV-08), paid trial deliveries and joining mid-cycle (DV-01, DV-03, DV-05), app or link and mobile coverage at the delivery point (DV-28), volunteers and uncollected baskets (DV-14, DV-15), recording allergies in the app (FR-19), joining only for other producers' products (DV-04), order confirmation to the co-producer (DV-10).
- To **FAIR**: data retention after leaving (PA-04), PA-02 (cycle and commitment), whether centralized payment fits the Charter of Principles (C6), contract or trial period and support given to AMAPs, performance targets (NFR-02, NFR-10).
