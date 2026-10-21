# RF05 – Payments and invoicing

**Updated on:** 21/10/2026 · [Conventions and sources](README.md)

## Description
Calculates how much each co-producer has to pay, collects it in a single payment and distributes it among producers. Today, at AMAP Porto, each producer is paid directly, with their own methods and timing (monthly fee for boxes, meat after weighing, mushrooms at each delivery). BioGoods does the maths in Excel and sends the amount by message, and the co-producer has no simple way to know how much they owe.

**Group proposal (21/10):** **centralised collection**. The co-producer makes **one payment** per period, which is **split among producers** through a **licensed payment provider**. Each producer receives a **summary** of who paid, how much and what it covers. The proposal builds on the lecturer's remark about this kind of app (E-5), the request to combine payments (E-1) and the "possible" model described by BioGoods (E-2 §13).

**Limits:** the system **does not hold the money** (the licensed provider moves it, PSD2) and **does not issue invoices** (each producer invoices in their own software; RNF-RES-01, open).

## Stimulus/response sequences
- The start of the period arrives → the system calculates each co-producer's amount, broken down by producer, and sends them the payment request.
- The co-producer pays (e.g. MB Way, Multibanco reference) → the provider confirms the payment, splits the amount among producers and the system records it automatically.
- The producer records the actual weight of the meat delivered → the amount goes into the next payment.
- The period ends → each producer receives the summary of who paid, how much and what it covers.
- A payment is still due after the deadline → the system notifies the co-producer and AMAP management.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-PAG-01 | The system shall allow AMAP management to choose the payment methods available through the provider (e.g. MB Way, Multibanco reference, card) and each producer to link the account where they receive their share. | Management, Producer | M | D-A, D-C §4.3, CA, DOC-10, group proposal (based on E-5) | Proposed |
| RF-PAG-02 | The system shall allow setting, per producer and per product, when each amount is charged: in advance for the cycle, at the start of each month, or after delivery or weighing. | Producer | M | D-A, E-1 §3.9, E-3 §4, N7 | To validate (C3) |
| RF-PAG-03 | The system shall calculate the amount each co-producer pays in each period, broken down by producer: fixed fees + extras + weighed products − compensated missing items. | System | M | E-2 §2, D-A, E-3 §4, DOC-09 | To validate (C3) |
| RF-PAG-04 | The system shall send the co-producer the payment request and show them, in a single view, the total amount, the breakdown by producer and their payment history. | System, Co-producer | M | E-3 §4, N6, N8, DOC-17 | Proposed |
| RF-PAG-05 | The system shall automatically record payments confirmed by the provider and allow management to manually record payments made outside the platform (e.g. cash). | System, Management | M | D-C §4.3, E-3 §4, DOC-11 | Proposed |
| RF-PAG-06 | The system shall show management and each producer the payment status per co-producer and flag late payments. | System, Management, Producer | S | DV-19, DV-20 | To validate (DV-20) |
| RF-PAG-07 | The system shall allow the producer to record the invoice they issued in their own software (number, date, document), without issuing it in the system. | Producer | S | D-F, DOC-36, C4 | To validate (C6) |
| RF-PAG-08 | The system shall store each product's VAT rate and each producer's VAT scheme, and show prices with VAT included. | Producer | C | D-A, DOC-41 | Proposed |
| RF-PAG-09 | The system shall allow AMAP management to record each member's annual fee and the common fund, and produce the annual financial report. | Management | C | D-C §4.3, §4.5, DOC-24 | To validate (DV-22) |
| RF-PAG-10 | The system shall combine a co-producer's payments to several producers into a single operation, with the amount split among producers through a licensed payment provider (the system does not hold the money). | Co-producer, System | M | Group proposal (based on E-5), E-1 §3.9, E-2 §13 | Proposed |
| RF-PAG-11 | The system shall allow integrated online payments through a licensed payment provider. | Co-producer | M | Group proposal (based on E-5), E-1 §3.9, PSD2 | Proposed |
| RF-PAG-12 | The system shall issue invoices on behalf of the producer or the AMAP. | Producer, Management | W | E-1 §3.9, E-2 §13 | To validate (C6) |
| RF-PAG-13 | The system shall generate, for each producer and period, a **summary of payments received**: who paid, how much, when, and which subscription, products or deliveries it covers. | System, Producer | M | Group proposal (based on E-5), E-2 §2 (Excel calculations), DOC-09 | Proposed |
| RF-PAG-14 | The system shall calculate the amount FAIR charges each producer or AMAP, according to the defined pricing model (e.g. minimum fee plus a volume-based component). | FAIR administrator | C | E-1 §4, E-5 | To validate (DV-25) |
