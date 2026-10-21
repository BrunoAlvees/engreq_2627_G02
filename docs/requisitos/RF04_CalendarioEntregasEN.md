# RF04 – Calendar and deliveries

**Updated on:** 21/10/2026 · [Conventions and sources](README.md)

## Description
Manages the distribution calendar and everything that happens at each delivery: box contents, availability, missing items, absences, collection and forgotten boxes. This is the area with the most problems in the current system: there is no collection confirmation, boxes are left outside after 19:30, and absences and missing items are arranged by message.

## Stimulus/response sequences
- The producer publishes the box contents → each co-producer sees what they will collect, already adjusted for their exclusions, with the approximate weight.
- The co-producer reports an absence → they choose what happens to the box from the AMAP's options and the producer is notified.
- The co-producer collects the box → they confirm the collection in the app (or, if idea RF-ENT-19 goes ahead, scans the bag's QR code).
- The distribution slot ends with unconfirmed boxes → the system notifies the co-producer and the producer.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-ENT-01 | The system shall allow AMAP management to set the distribution place and time (weekday and hours) and change them occasionally (e.g. public holidays). | Management | M | D-A, D-B §3.3, DOC-33, Brainstorm 14/10 | Proposed |
| RF-ENT-02 | The system shall allow different delivery days per AMAP and a producer serving different AMAPs on alternate weeks. | Management, Producer | M | E-2 §6 | Proposed |
| RF-ENT-03 | The system shall allow each producer to set their delivery dates for the cycle, within the AMAP's distribution time, with their own frequency and product-specific dates (e.g. Biogoods fortnightly; Quinta da Serrinha in September and December; bread on all dates except two). The co-producer sees in a single calendar the dates of all producers they buy from. | Producer | M | E-3 §2 (producers set the dates), D-A, DOC-03, C1, Brainstorm 14/10, N18 | Proposed |
| RF-ENT-04 | The system shall allow several pick-up points in one AMAP. | Management | C | E-2 §6 | Proposed |
| RF-ENT-05 | The system shall allow the producer to publish the box contents before each delivery. | Producer | M | E-2 §4, N1 | Proposed |
| RF-ENT-06 | The system shall show each co-producer what they will collect on each date, from all producers, taking exclusions and substitutions into account, with the approximate weight. | Co-producer | M | E-2 §4, E-3 §10, N2, N9 | Proposed |
| RF-ENT-07 | The system shall allow the producer to confirm a product's availability before delivery (e.g. mushrooms, seasonal breads) and notify the affected co-producers. | Producer | S | D-A, E-3 §3, DOC-12, N18 | Proposed |
| RF-ENT-08 | The system shall allow recording missing items in a delivery and the compensation given (discount or substitution in another delivery). | Producer | S | E-3 §7, DOC-34 | Proposed |
| RF-ENT-09 | The system shall allow spreading a shortage across AMAPs in rotation, instead of partial deliveries within the same AMAP. | Producer | C | E-3 §7 | Proposed |
| RF-ENT-10 | The system shall allow recording the actual quantity or weight delivered to each co-producer (e.g. meat). | Producer | M | D-A | Proposed |
| RF-ENT-11 | The system shall allow the co-producer to report an absence and choose what happens to the box from a list defined by the AMAP (friend or relative, donation, sharing among the others, raffle…). | Co-producer | M | E-2 §9, E-3 §6, N4, DOC-25 | Proposed |
| RF-ENT-12 | The system shall allow the co-producer to state who will collect the box on their behalf. | Co-producer | S | E-2 §10, E-3 §9 | Proposed |
| RF-ENT-13 | The system shall allow confirming the collection of each box, by the co-producer or by whoever collects it on their behalf. | Co-producer | M | E-2 §10, E-3 §9, N3 | To validate (mandatory?) |
| RF-ENT-14 | At the end of the slot, the system shall flag unconfirmed boxes and notify the co-producer and the producer. | System | S | D-B §3.3, E-2 §10, DOC-26 | Proposed |
| RF-ENT-15 | The system shall generate a printable distribution sheet for each date (what each co-producer takes, from each producer) as an A4 PDF. Bag labels are covered by RF-ENT-18. | Management, Producer | M | D-C §4.5, E-3 §8, DOC-27, DOC-35 | To validate (DV-13) |
| RF-ENT-16 | After the distribution slot, the system shall ask the co-producer to confirm the collection if they have not done so yet. | System | S | Brainstorm 14/10 (people forget to confirm), E-3 §9 | Proposed |
| RF-ENT-17 | The system shall allow a volunteer, management or the producer to confirm the collection on behalf of a co-producer without a phone. | Management, Producer | S | Brainstorm 14/10 | Proposed |
| RF-ENT-18 | The system shall generate A4 PDF bag labels with the name, "Bag x of y", producer and date, without health data. | System, Producer | S | E-3 §8 ("Name 1 of 2"), CA (CSAware: labels), Brainstorm 14/10 | Proposed |
| RF-ENT-19 | **Idea:** each label may carry an individual QR code. When scanning it, the co-producer confirms the collection of that bag, and the system warns if the bag is not theirs. | Co-producer | C | Brainstorm 14/10; E-3 §9 (bread taken by the wrong person); none of the solutions analysed has this feature | Idea (assess during implementation) |

## Note: 14/10 brainstorm on collection
- **Abroad**, the usual approach is a **printed sheet** where each person ticks their name (the "liste d'émargement" of French AMAPs, generated by Cagette; the sign-in sheet at Lancaster Farm Fresh, USA). We found no solution with QR-code confirmation.
- **Group decision:** the baseline is **confirmation in the app** (RF-ENT-13), with a reminder for those who forget (RF-ENT-16). A single shared sheet adds nothing over the app.
- An **individual QR code per bag** (RF-ENT-19) would prevent bags being mixed up, but forces the producer to print and stick labels every week. It stays as an **idea**, to be assessed during implementation and validated with stakeholders (DV-27, DV-28).
