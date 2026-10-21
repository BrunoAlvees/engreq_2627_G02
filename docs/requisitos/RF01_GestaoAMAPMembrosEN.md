# RF01 – AMAP and member management

**Updated on:** 21/10/2026 · [Conventions and sources](README.md)

## Description
Allows creating and configuring independent AMAPs (with one or several producers) and managing each person's path: joining request, trial deliveries, waiting list, registration, personal data and consents. Today, people join by contacting the main producer directly, data arrives through Google Forms and there is no record of each member's status.

## Stimulus/response sequences
- A prospective member opens the AMAP's public page (or searches the portal) → they see the introduction, the producers and whether there are places available.
- The prospective member asks to join → the system records the request and notifies whoever handles it. If there is no place, it puts them on the waiting list.
- Management accepts the request → the person becomes "on trial" and, after the trial deliveries, is invited to subscribe to the cycle.
- A co-producer asks for their data to be erased → the system records the request and tracks the response deadline.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-MEM-01 | The system shall allow creating an AMAP with a name, pick-up point, distribution day and time, contact and operating rules. | AMAP management, FAIR admin | M | D-A, E-2 §6, DOC-33 | Proposed |
| RF-MEM-02 | The system shall support several independent AMAPs, each with its own rules, and allow a producer to take part in several AMAPs. | FAIR admin | M | E-2 §1, §11, CA | Proposed |
| RF-MEM-03 | The system shall support AMAPs with a single producer and AMAPs with several producers, who may offer the same or different products. | AMAP management | M | E-2 §3, N14 | Proposed |
| RF-MEM-04 | The system shall provide a public page for each AMAP (introduction, principles, producers and products, place and time, available places) with a "I want to join" option that starts the joining request. | Prospective member | S | E-1 §3.1, D-C, D-D, Brainstorm 14/10 | Proposed |
| RF-MEM-05 | The system shall allow a prospective member to request to join an AMAP and record who handles the request (main producer or management). | Prospective member, Management | M | E-1 §3.1, E-4, DOC-38 | Proposed |
| RF-MEM-06 | The system shall put the prospective member on an ordered waiting list when the AMAP has no places, and notify them when a place becomes available. | System | M | E-1 §3.1, D-A, DV-02, DV-03, N16 | To validate (DV-03) |
| RF-MEM-07 | The system shall allow trial deliveries before subscribing, with a number configurable per AMAP. | Management, Producer | S | E-4 (2 deliveries), D-C (1 delivery), DOC-23 | To validate (DV-01) |
| RF-MEM-08 | The system shall store each member's status: prospective, on waiting list, on trial, active or left. | System | M | DOC-38, E-4 | Proposed |
| RF-MEM-09 | The system shall allow AMAP management to approve or refuse a registration request. | Management | S | D-B §3.2, DOC-22 | Proposed |
| RF-MEM-10 | The system shall register the co-producer with name, email and mobile number, and ask for the tax number (NIF) only if they want an invoice with it. | Co-producer | M | D-A, D-B, DOC-18, DOC-39, VAT Code art. 40 | Proposed |
| RF-MEM-11 | The system shall register the producer with a description, location, contacts and evidence of how they produce (certificates, or photos and a description of the farm). | Producer | M | E-1 §3.6, D-A, DOC-16 | To validate (PA-01) |
| RF-MEM-12 | The system shall require acceptance of the AMAP's Terms and Conditions and Guide, with a declaration of legal age, and store the accepted version and date. | Co-producer | M | D-A, D-B, DOC-19 | Proposed |
| RF-MEM-13 | The system shall allow giving and withdrawing optional consents (e.g. use of data in studies), keeping proof (date and version). | Co-producer | M | D-A, D-B, DOC-20, DOC-40, GDPR art. 7 | Proposed |
| RF-MEM-14 | The system shall allow data subjects to view, export, correct and request the erasure of their data, and track the response deadline (1 month). | Co-producer, Management | M | D-B §3.1, DOC-40, GDPR art. 12 | Proposed |
| RF-MEM-15 | The system shall state, per AMAP, the data controllers (the producers) and the contact point. | Management | S | D-B §3.1, DOC-21, GDPR art. 26 | Proposed |
| RF-MEM-16 | The system shall allow assigning roles (co-producer, producer, AMAP management, administrator) with different permissions; one person may hold several roles. | FAIR admin, Management | M | E-1 §3.2, D-C §4.5, CA (AMAPJ) | Proposed |
| RF-MEM-17 | The system shall allow recording that a co-producer leaves mid-subscription, with the reason, and choosing what happens to the remaining deliveries: transfer the subscription to a replacement or donate the remaining deliveries to an institution. Payment settlements are handled case by case. | Co-producer, Management | S | D-F, DOC-32, C5, E-2 §7, E-2 §9 (donation), Brainstorm 14/10 | Proposed |
| RF-MEM-18 | *(Merged into RF-MEM-17 in the 14/10 brainstorm.)* | — | — | — | Rejected |
| RF-MEM-19 | The system shall provide a public portal listing all AMAPs on the platform, with search by location and a link to each AMAP's page. | Prospective member | C | E-1 §3.1, CA, Brainstorm 14/10 | Proposed |
| RF-MEM-20 | The system shall allow a co-producer to be a member of several AMAPs (e.g. to get deliveries every week) and see the deliveries of all of them in a single calendar. | Co-producer | S | E-2 §6, Brainstorm 14/10 | Proposed |
| RF-MEM-21 | The system shall have an AMAP rules panel where management configures what varies between AMAPs: cycle length, subscription deadlines, number of trial deliveries, renewal mode (RF-SUB-11), possible box destinations for absences (RF-ENT-11) and documents (Terms, Guide). | Management | M | Principle 1, E-2 §1, §11, Brainstorm 14/10 | Proposed |
