# RF03 – Cycles and subscriptions

**Updated on:** 28/10/2026 · [Conventions and sources](README.md)

## Description
Organises the work in cycles (currently six-monthly at AMAP Porto; quarterly or yearly in others) and lets the co-producer subscribe to each cycle's products, with their options and exclusions. It replaces the Google Form and the email copy that co-producers keep to remember what they ordered. It also gives the producer a view of the orders to plan production.

## Stimulus/response sequences
- Management opens a cycle → the system notifies active members and accepts subscriptions until the deadline.
- The co-producer chooses baskets, extras, variants and dates → the system shows a summary with the estimated monthly amount per producer and confirms the subscription.
- A request arrives after the deadline → it stays pending until management approves it.
- The end of the cycle is approaching → the system invites the co-producer to renew, with the previous order pre-filled.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-SUB-01 | The system shall allow creating subscription cycles with a configurable length, an opening date and a subscription deadline. | Management | M | E-1 §3.5, E-2 §7, D-A, DOC-01, N13 | Proposed |
| RF-SUB-02 | The system shall allow the co-producer to subscribe, in a single step, to products from several producers of the same AMAP, with their options, and receive a confirmation. | Co-producer, System | M | D-A, D-C §4.2, E-3 §1, DOC-14, DOC-17, N17 | Proposed |
| RF-SUB-03 | The system shall allow the co-producer to record exclusions (allergies, intolerances, dislikes) and the producer to record the substitution made. | Co-producer, Producer | M | E-2 §4, E-3 §14, N2 | Proposed |
| RF-SUB-04 | The system shall apply subscription deadlines and each producer's rules for changing orders during the cycle. | Co-producer, Producer, Management | S | D-A, E-3 §3, DOC-13, N18, Brainstorm 14/10 | Proposed |
| RF-SUB-05 | The system shall allow the co-producer to view, at any time, their current subscriptions and history. | Co-producer | M | E-3 §1, N6, DOC-17 | Proposed |
| RF-SUB-06 | The system shall ask co-producers in advance whether they will renew, starting from their previous order. | Co-producer, Management | S | E-2 §7, N12, DV-11, C8, Brainstorm 14/10 | To validate (DV-12) |
| RF-SUB-07 | The system shall give the producer the information needed to plan production: totals ordered and aggregated preferences. | Producer | M | E-1 §3.5, E-1 (class 1), E-2 §2, §13 | Proposed |

## Acceptance criteria

**RF-SUB-01 – Cycles**
- The cycle length is configurable (e.g. 3, 6 or 12 months), with an opening date and a subscription deadline.
- *(Could, to validate PA-02)* The co-producer's commitment period may differ from the length of the offer cycle.

**RF-SUB-02 – Subscribe**
- In a single step, the co-producer subscribes to products from several producers of the same AMAP.
- For each product they choose the quantity, the variant and, where applicable, the delivery dates (e.g. meat).
- Requests that currently go into free text have structured options (e.g. meat options, loose instead of basket, varying the bread during the cycle).
- The system sends a confirmation with the products, dates and amounts per producer.

**RF-SUB-03 – Exclusions and substitutions**
- The co-producer records exclusions (allergies, intolerances, dislikes); allergies are health data (RNF-SEG-03).
- The producer records the substitution made.

**RF-SUB-04 – Deadlines and changes**
- Requests after the deadline stay pending until management approves or refuses them.
- Each producer defines whether the co-producer can change their order and how long before each delivery (e.g. bread until Sunday for the Tuesday delivery).
- The co-producer can change their order during the cycle, within those rules.
- *(Could)* The producer can ask for an order to be confirmed or changed before a future delivery (e.g. December olive oil same as September).

**RF-SUB-05 – View subscriptions**
- The co-producer sees their current subscriptions and history at any time, with no need to keep the form copy received by email.

**RF-SUB-06 – Renewal**
- The lead time is configurable (e.g. 3 months before the new cycle), because crops are planted in advance.
- Each AMAP chooses the mode: **(A) intention**, indicative only, so the producer can plan; or **(B) mandatory confirmation** by a deadline, with those who do not confirm losing their place to the waiting list.

**RF-SUB-07 – Production planning**
- The producer sees the total ordered per product, variant, delivery date and AMAP, to plan production and harvesting.
- *(Could)* The producer sees aggregated preferences and exclusions to plan the next cycle's production.

## Mapping to the previous version
In the 28/10 review, the 15 active requirements were grouped into 7 to reduce detail (lecturer's advice). The detail moved to the acceptance criteria.

| New | Combines previous |
|---|---|
| RF-SUB-01 | 01, 02 |
| RF-SUB-02 | 03, 04, 05, 09 |
| RF-SUB-03 | 06 |
| RF-SUB-04 | 07, 08, 13, 16 |
| RF-SUB-05 | 10 |
| RF-SUB-06 | 11 |
| RF-SUB-07 | 14, 15 |
| — | 12 (rejected in the 14/10 brainstorm: new members already have trial deliveries, RF-MEM-03) |
