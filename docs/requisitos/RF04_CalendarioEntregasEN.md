# RF04 – Calendar and deliveries

**Updated on:** 14/10/2026 · [Conventions and sources](README.md)

## Description
Manages the distribution calendar and everything that happens at each delivery: box contents, availability, missing items, absences, collection and forgotten boxes. This is the area with the most problems in the current system: there is no collection confirmation, boxes are left outside after 19:30, and absences and missing items are arranged by message.

## Stimulus/response sequences
- The producer publishes the box contents → each co-producer sees what they will collect, already adjusted for their exclusions, with the approximate weight.
- The co-producer reports an absence → they choose what happens to the box from the AMAP's options and the producer is notified.
- The co-producer collects the box → they confirm the collection in the system.
- The distribution slot ends with unconfirmed boxes → the system notifies the co-producer and the producer.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-ENT-01 | The system shall generate the cycle's delivery calendar from the AMAP's day, time, frequency and place, and allow changing dates (e.g. public holidays). | Management, Producer | M | D-A, E-3 §2, DOC-02, DOC-33 | To validate (C1: who approves?) |
| RF-ENT-02 | The system shall allow different delivery days per AMAP and a producer serving different AMAPs on alternate weeks. | Management, Producer | M | E-2 §6 | Proposed |
| RF-ENT-03 | The system shall allow the producer to mark calendar dates they will skip, and set specific dates for certain products (e.g. meat, olive oil). | Producer | M | D-A, DOC-03 | Proposed |
| RF-ENT-04 | The system shall allow several pick-up points in one AMAP. | Management | C | E-2 §6 | Proposed |
| RF-ENT-05 | The system shall allow the producer to publish the box contents before each delivery. | Producer | M | E-2 §4, N1 | Proposed |
| RF-ENT-06 | The system shall show each co-producer what they will collect on each date, from all producers, taking exclusions and substitutions into account, with the approximate weight. | Co-producer | M | E-2 §4, E-3 §10, N2, N9 | Proposed |
| RF-ENT-07 | The system shall allow the producer to confirm a product's availability before delivery (e.g. mushrooms, seasonal breads) and notify the affected co-producers. | Producer | S | D-A, E-3 §3, DOC-12 | Proposed |
| RF-ENT-08 | The system shall allow recording missing items in a delivery and the compensation given (discount or substitution in another delivery). | Producer | S | E-3 §7, DOC-34 | Proposed |
| RF-ENT-09 | The system shall allow spreading a shortage across AMAPs in rotation, instead of partial deliveries within the same AMAP. | Producer | C | E-3 §7 | Proposed |
| RF-ENT-10 | The system shall allow recording the actual quantity or weight delivered to each co-producer (e.g. meat). | Producer | M | D-A | Proposed |
| RF-ENT-11 | The system shall allow the co-producer to report an absence and choose what happens to the box from a list defined by the AMAP (friend or relative, donation, sharing among the others, raffle…). | Co-producer | M | E-2 §9, E-3 §6, N4, DOC-25 | Proposed |
| RF-ENT-12 | The system shall allow the co-producer to state who will collect the box on their behalf. | Co-producer | S | E-2 §10, E-3 §9 | Proposed |
| RF-ENT-13 | The system shall allow confirming the collection of each box, by the co-producer or by whoever collects it on their behalf. | Co-producer | M | E-2 §10, E-3 §9, N3 | To validate (mandatory?) |
| RF-ENT-14 | At the end of the slot, the system shall flag unconfirmed boxes and notify the co-producer and the producer. | System | S | D-B §3.3, E-2 §10, DOC-26 | Proposed |
| RF-ENT-15 | The system shall generate a printable distribution sheet for each date (what each co-producer takes, from each producer) and bag labels (e.g. "Name 1 of 2"). | Management, Producer | M | D-C §4.5, E-3 §8, DOC-27, DOC-35 | To validate (DV-13) |
