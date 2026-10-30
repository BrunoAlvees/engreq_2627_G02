# RF05 – Payments and invoicing

**Updated on:** 28/10/2026 · [Conventions and sources](README.md)

## Description
Calculates how much each co-producer has to pay, collects it in a single payment and distributes it among producers. Today, at AMAP Porto, each producer is paid directly, with their own methods and timing (monthly fee for baskets, meat after weighing, mushrooms at each delivery). BioGoods does the maths in Excel and sends the amount by message, and the co-producer has no simple way to know how much they owe.

**Group proposal (21/10):** **centralised collection**. The co-producer makes **one payment** per period, which is **split among producers** through a **licensed payment provider**. Each producer receives a **summary** of who paid, how much and what it covers. The proposal builds on the lecturer's remark about this kind of app (E-5), the request to combine payments (E-1) and the "possible" model described by BioGoods (E-2 §13).

**Limits:** the system **does not hold the money** (the licensed provider moves it, PSD2) and **does not issue invoices**: invoicing is **out of scope** (E-6, NFR-18).

## Stimulus/response sequences
- The start of the period arrives → the system calculates each co-producer's amount, broken down by producer, and sends them the payment request.
- The co-producer pays (e.g. MB Way, Multibanco reference) → the provider confirms the payment, splits the amount among producers and the system records it automatically.
- The producer records the actual weight of the meat delivered → the amount goes into the next payment.
- The period ends → each producer receives the summary of who paid, how much and what it covers.
- A payment is still due after the deadline → the system notifies the co-producer and AMAP management.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| FR-30 | The system shall allow configuring payments for each AMAP and each producer: available methods, the account where each producer is paid and when each product is charged. | Management, Producer | M | D-A, D-C §4.3, E-1 §3.9, E-3 §4, CA, DOC-10, N7, group proposal (based on E-5) | To validate (C3) |
| FR-31 | The system shall calculate the amount each co-producer pays in each period, broken down by producer, and send them the payment request. | System, Co-producer | M | E-2 §2, D-A, E-3 §4, DOC-09, DOC-17, N6, N8 | Proposed |
| FR-32 | The system shall collect in a single payment a co-producer's amount for several producers, with the amount split among producers through a licensed payment provider (the system does not hold the money). | Co-producer, System | M | Group proposal (based on E-5), E-1 §3.9, E-2 §13, PSD2, D-C §4.3, DOC-11 | Proposed |
| FR-33 | The system shall allow tracking payments: status per co-producer, late payments and a summary of payments received by each producer. | System, Management, Producer | M | Group proposal (based on E-5), E-2 §2, DOC-09, DV-19, DV-20 | Proposed |
| FR-34 | The system shall calculate the amount FAIR charges each producer or AMAP, according to the defined pricing model. | FAIR administrator | C | E-1 §4, E-5, NFR-21 | To validate (DV-25) |

## Acceptance criteria

**FR-30 – Configure payments**
- AMAP management chooses the payment methods available through the provider (e.g. MB Way, Multibanco reference, card).
- Each producer links the account where they receive their share.
- Per producer and per product, it is set when each amount is charged: in advance for the cycle, at the start of each month, or after delivery or weighing.

**FR-31 – Calculate and request payment**
- The amount is calculated as: fixed basket fees + extras + weighed products − compensated missing items. Basket fees are fixed; extras vary with what was delivered (D-A).
- The co-producer receives the payment request and sees, in a single view, the total, the breakdown by producer and their payment history.

**FR-32 – Centralised collection**
- The co-producer makes one online payment per period through the licensed provider.
- The provider splits the amount among producers; the system does not hold the money (NFR-19).
- Payments confirmed by the provider are recorded automatically; management can manually record payments made outside the platform (e.g. cash).

**FR-33 – Track payments**
- Management and each producer see the payment status per co-producer and are notified of late payments (to validate DV-20).
- Each producer receives, per period, the summary of payments received: who paid, how much, when, and which subscription, products or deliveries it covers.

**FR-34 – Amount charged by FAIR**
- The pricing model is a minimum fee per producer plus a percentage of payment volume (NFR-21); the amounts are set by FAIR.

## Out of scope for this version
| Previous | Requirement | Reason |
|---|---|---|
| RF-PAG-07 | Record the invoice the producer issued in their own software | Rejected: invoicing is out of scope (E-6) |
| RF-PAG-08 | Store each product's VAT rate and each producer's VAT scheme | Rejected: invoicing is out of scope (E-6); prices with VAT included are in NFR-14 |
| RF-PAG-09 | Manage each member's annual fee, the common fund and the annual financial report | Won't (not in this version): only appears in AMAP Porto's old Guide (D-C), no stakeholder mentioned it; it may no longer exist (DV-22) |
| RF-PAG-12 | Issue invoices on behalf of the producer or the AMAP | Rejected: invoicing is out of scope (E-6) |

## Mapping to the previous version
In the 28/10 review, the 13 active requirements were reduced to 5 to reduce detail (lecturer's advice). The detail moved to the acceptance criteria.

| New | Combines previous |
|---|---|
| FR-30 | 01, 02 |
| FR-31 | 03, 04 |
| FR-32 | 05, 10, 11 |
| FR-33 | 06, 13 |
| FR-34 | 14 |
| — | 07, 08, 09, 12 (see "Out of scope for this version") |
