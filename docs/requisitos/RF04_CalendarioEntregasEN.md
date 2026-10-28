# RF04 – Calendar and deliveries

**Updated on:** 28/10/2026 · [Conventions and sources](README.md)

## Description
Manages the distribution calendar and everything that happens at each delivery: basket contents, availability, missing items, absences, collection and forgotten baskets. This is the area with the most problems in the current system: there is no collection confirmation, baskets are left outside after 19:30, and absences and missing items are arranged by message.

## Stimulus/response sequences
- The producer publishes the basket contents → each co-producer sees what they will collect, already adjusted for their exclusions, with the approximate weight.
- The co-producer reports an absence → they choose what happens to the basket from the AMAP's options and the producer is notified.
- The co-producer collects the basket → they confirm the collection in the app (or, if the QR code idea goes ahead, scans the bag's QR code).
- The distribution slot ends with unconfirmed baskets → the system notifies the co-producer and the producer.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-ENT-01 | The system shall manage each AMAP's delivery calendar, with the distribution place and time and each producer's delivery dates and mode. | Management, Producer | M | D-A, D-B §3.3, E-2 §6, E-3 §2, §8, DOC-03, DOC-33, C1, N18, Brainstorm 14/10 and 21/10 | Proposed |
| RF-ENT-02 | The system shall allow the producer to publish the basket contents before each delivery and show each co-producer what they will collect. | Producer, Co-producer | M | E-2 §4, E-3 §10, N1, N2, N9 | Proposed |
| RF-ENT-03 | The system shall allow the producer to confirm product availability and record missing items, compensations and actual quantities delivered. | Producer | M | D-A, E-3 §3, §7, DOC-12, DOC-34, N18 | Proposed |
| RF-ENT-04 | The system shall allow the co-producer to report an absence, choose what happens to the basket and state who collects it on their behalf. | Co-producer | M | E-2 §9, §10, E-3 §6, §9, N4, DOC-25 | Proposed |
| RF-ENT-05 | The system shall allow confirming the collection of each basket and flag baskets not collected. | Co-producer, Management, Producer, System | M | D-B §3.3, E-2 §10, E-3 §9, N3, DOC-26, Brainstorm 14/10 | To validate (mandatory?) |
| RF-ENT-06 | The system shall generate, as printable A4 PDFs, the distribution sheet for each date and the bag labels. | Management, Producer, System | S | D-C §4.5, E-3 §8, CA (CSAware: labels), DOC-27, DOC-35, Brainstorm 14/10 | To validate (DV-13) |

## Acceptance criteria

**RF-ENT-01 – Delivery calendar**
- AMAP management sets the distribution place and time (weekday and hours) and can change them occasionally (e.g. public holidays).
- Each AMAP can have its own delivery day, and a producer can serve different AMAPs on alternate weeks.
- Each producer sets their delivery dates for the cycle, within the AMAP's distribution time, with their own frequency and product-specific dates (e.g. BioGoods fortnightly; Quinta da Serrinha in September and December; bread on all dates except two).
- Each producer states their delivery mode (e.g. labelled bag left at the delivery point, hand delivery, route across several points), which the co-producer can see.
- The co-producer sees in a single calendar the dates of all producers they buy from.
- *(Could)* An AMAP can have several pick-up points.

**RF-ENT-02 – Basket contents**
- The producer publishes the basket contents before each delivery, instead of sending them by WhatsApp.
- Each co-producer sees what they will collect on each date, from all producers, already adjusted for exclusions and substitutions, with the approximate weight.

**RF-ENT-03 – Availability and missing items**
- The producer confirms a product's availability before delivery (e.g. mushrooms, seasonal breads) and the affected co-producers are notified.
- The producer records missing items and the compensation given (discount or substitution in another delivery); they can link a news post explaining the shortage (RF-COM-03).
- The producer records the actual quantity or weight delivered to each co-producer (e.g. meat).
- *(Could)* A shortage can be spread across AMAPs in rotation, instead of partial deliveries within the same AMAP.

**RF-ENT-04 – Absences**
- The co-producer reports the absence and chooses what happens to the basket from a list defined by the AMAP (friend or relative, donation to an organisation, sharing among the others, raffle…). The basket is always collected and paid for.
- The co-producer states who will collect the basket on their behalf.
- The producer is notified of the absence and the chosen destination.

**RF-ENT-05 – Collection confirmation**
- The co-producer, or whoever collects on their behalf, confirms the collection in the app.
- After the distribution slot, the system asks those who have not confirmed to do so.
- At the end of the slot, the system flags unconfirmed baskets and notifies the co-producer and the producer.
- A volunteer, management or the producer can confirm on behalf of a co-producer without a phone.
- *(Idea, assess during implementation)* Each label may carry an individual QR code: when scanning it, the co-producer confirms the collection of that bag and the system warns if the bag is not theirs.

**RF-ENT-06 – Distribution sheet and labels**
- The distribution sheet for each date shows what each co-producer takes, from each producer.
- Bag labels show the name, "Bag x of y", the producer and the date, without health data (RNF-SEG-03).

## Note: 14/10 brainstorm on collection
- **Abroad**, the usual approach is a **printed sheet** where each person ticks their name (the "liste d'émargement" of French AMAPs, generated by Cagette; the sign-in sheet at Lancaster Farm Fresh, USA). We found no solution with QR-code confirmation.
- **Group decision:** the baseline is **confirmation in the app** (RF-ENT-05), with a reminder for those who forget. A single shared sheet adds nothing over the app.
- An **individual QR code per bag** would prevent bags being mixed up, but forces the producer to print and stick labels every week. It stays as an **idea**, to be assessed during implementation and validated with stakeholders (DV-27, DV-28).

## Mapping to the previous version
In the 28/10 review, the 20 previous requirements were grouped into 6 to reduce detail (lecturer's advice). The detail moved to the acceptance criteria.

| New | Combines previous |
|---|---|
| RF-ENT-01 | 01, 02, 03, 04, 20 |
| RF-ENT-02 | 05, 06 |
| RF-ENT-03 | 07, 08, 09, 10 |
| RF-ENT-04 | 11, 12 |
| RF-ENT-05 | 13, 14, 16, 17, 19 |
| RF-ENT-06 | 15, 18 |
