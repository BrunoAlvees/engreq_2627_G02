# RF03 – Cycles and subscriptions

**Updated on:** 21/10/2026 · [Conventions and sources](README.md)

## Description
Organises the work in cycles (currently six-monthly at AMAP Porto; quarterly or yearly in others) and lets the co-producer subscribe to each cycle's products, with their options and exclusions. It replaces the Google Form and the email copy that co-producers keep to remember what they ordered. It also gives the producer a view of the orders to plan production.

## Stimulus/response sequences
- Management opens a cycle → the system notifies active members and accepts subscriptions until the deadline.
- The co-producer chooses boxes, extras, variants and dates → the system shows a summary with the estimated monthly amount per producer and confirms the subscription.
- A request arrives after the deadline → it stays pending until management approves it.
- The end of the cycle is approaching → the system invites the co-producer to renew, with the previous order pre-filled.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-SUB-01 | The system shall allow creating a cycle with a configurable length (e.g. 3, 6 or 12 months), an opening date and a subscription deadline. | Management | M | E-1 §3.5, E-2 §7, D-A, DOC-01, N13 | Proposed |
| RF-SUB-02 | The system shall allow the co-producer's commitment period to differ from the length of the offer cycle. | Management | S | E-1 §3.5 | To validate |
| RF-SUB-03 | The system shall allow the co-producer to subscribe, in a single step, to products from several producers of the same AMAP. | Co-producer | M | D-A, E-3 §1 | Proposed |
| RF-SUB-04 | The system shall allow choosing, in each subscription, the quantity, the variant and, where applicable, the delivery dates (e.g. meat). | Co-producer | M | D-A, N17 | Proposed |
| RF-SUB-05 | The system shall offer structured options for requests that currently go into free text (e.g. meat options, loose instead of box, varying the bread during the cycle). | Co-producer | S | D-A, DOC-14, N17 | Proposed |
| RF-SUB-06 | The system shall allow the co-producer to record exclusions (allergies, intolerances, dislikes) and the producer to record the substitution made. | Co-producer, Producer | M | E-2 §4, E-3 §14, N2 | Proposed |
| RF-SUB-07 | The system shall only accept requests after the deadline as pending, until management approves or refuses them. | Management | S | D-A | Proposed |
| RF-SUB-08 | The system shall allow setting, per product, a change deadline before each delivery (e.g. bread until Sunday for the Tuesday delivery). | Producer | S | E-3 §3 | Proposed |
| RF-SUB-09 | The system shall send the co-producer a subscription confirmation with the products, dates and amounts per producer. | System | M | D-C §4.2, E-3 §1, DOC-17 | Proposed |
| RF-SUB-10 | The system shall allow the co-producer to view, at any time, their current subscriptions and history. | Co-producer | M | E-3 §1, N6, DOC-17 | Proposed |
| RF-SUB-11 | The system shall allow renewing the subscription with a configurable lead time (e.g. 3 months), starting from the previous order. | Co-producer, Management | S | E-2 §7, N12, DV-11, C8 | To validate (DV-12) |
| RF-SUB-12 | The system shall allow different commitment rules for new members (e.g. 3 months at first, then 6). | Management | C | E-2 §7 | Proposed |
| RF-SUB-13 | The system shall allow the producer to ask for an order to be confirmed or changed before a future delivery (e.g. December olive oil same as September). | Producer | C | D-A, DOC-13, N18 | Proposed |
| RF-SUB-14 | The system shall show the producer the total ordered per product, variant, delivery date and AMAP, to plan production and harvesting. | Producer | M | E-2 §2, §13, E-1 §3.5 | Proposed |
| RF-SUB-15 | The system shall allow the producer to view aggregated preferences and exclusions to plan the next cycle's production. | Producer | C | E-1 (class 1) | Proposed |
