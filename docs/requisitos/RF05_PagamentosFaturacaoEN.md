# RF05 – Payments and invoicing

**Updated on:** 14/10/2026 · [Conventions and sources](README.md)

## Description
Calculates how much each co-producer owes each producer and tracks payments. At AMAP Porto, each producer is paid directly, with their own methods and timing: monthly fee for boxes, meat after weighing, mushrooms at each delivery. Today BioGoods does the maths in Excel and sends the amount by message, and the co-producer has no simple way to know how much they owe.

**Scope proposal (C6, to validate):** the system **calculates, shows and records** payments, but **neither handles money nor issues invoices**. This respects the Charter of Principles (no intermediaries) and avoids the obligations of certified invoicing software and PSD2.

## Stimulus/response sequences
- The start of the month arrives → the system generates each co-producer's payment note per producer and sends it.
- The co-producer pays by MB Way and marks the note as paid → the producer confirms receipt.
- The producer records the actual weight of the meat delivered → the amount goes into the next note.
- A note is still unpaid after the deadline → the system notifies the co-producer and the producer.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-PAG-01 | The system shall allow each producer to set the payment methods they accept (bank transfer, MB Way, cash) and the payment instructions. | Producer | M | D-A, D-C §4.3, CA, DOC-10 | Proposed |
| RF-PAG-02 | The system shall allow setting, per producer and per product, when payment is due: in advance for the cycle, at the start of each month, at each delivery or after weighing. | Producer | M | D-A, E-1 §3.9, E-3 §4, N7 | To validate (C3) |
| RF-PAG-03 | The system shall calculate each co-producer's payment note per producer and period: fixed fees + extras + weighed products − compensated missing items. | System | M | E-2 §2, D-A, E-3 §4, DOC-09 | To validate (C3) |
| RF-PAG-04 | The system shall send the payment note to the co-producer and show them, in a single view, how much they owe each producer and their payment history. | System, Co-producer | M | E-3 §4, N6, N8, DOC-17 | Proposed |
| RF-PAG-05 | The system shall allow the co-producer to mark a payment as made (with optional proof) and the producer to confirm receipt. | Co-producer, Producer | M | D-C §4.3, E-3 §4, DOC-11 | Proposed |
| RF-PAG-06 | The system shall show the producer the payment status per co-producer and flag late payments. | System, Producer | S | DV-19, DV-20 | To validate (DV-20) |
| RF-PAG-07 | The system shall allow the producer to record the invoice they issued in their own software (number, date, document), without issuing it in the system. | Producer | S | D-F, DOC-36, C4 | To validate (C6) |
| RF-PAG-08 | The system shall store each product's VAT rate and each producer's VAT scheme, and show prices with VAT included. | Producer | C | D-A, DOC-41 | Proposed |
| RF-PAG-09 | The system shall allow AMAP management to record each member's annual fee and the common fund, and produce the annual financial report. | Management | C | D-C §4.3, §4.5, DOC-24 | To validate (DV-22) |
| RF-PAG-10 | The system shall allow combining a co-producer's payments to several producers into a single operation, with the AMAP receiving the money and paying the producers. | Management | W | E-1 §3.9, E-2 §13 | To validate (C6) |
| RF-PAG-11 | The system shall allow integrated online payments through a licensed payment provider. | Co-producer | W | E-1 §3.9, PSD2 | To validate (C6) |
| RF-PAG-12 | The system shall issue invoices on behalf of the producer or the AMAP. | Producer, Management | W | E-1 §3.9, E-2 §13 | To validate (C6) |
