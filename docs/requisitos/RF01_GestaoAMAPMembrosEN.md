# RF01 – AMAP and member management

**Updated on:** 28/10/2026 · [Conventions and sources](README.md)

## Description
Lets users create and configure independent AMAPs (with one or several producers) and manage each person's path: membership request, trial deliveries, waiting list, registration, personal data and consents. Today, joining is done by contacting the main producer directly, data arrives through Google Forms and there is no record of each member's status.

## Stimulus/response sequences
- The prospective member opens the AMAP's public page (or searches the portal) → sees the presentation, the producers and whether there is a place.
- The prospective member asks to join → the system records the request and notifies whoever handles it. If there is no place, it puts them on the waiting list.
- Management accepts the request → the person becomes "on trial" and, after the trial deliveries, is invited to subscribe to the cycle.
- The co-producer asks for their data to be deleted → the system records the request and tracks the response deadline.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-MEM-01 | The system shall allow creating and configuring independent AMAPs, with one or several producers and their own operating rules. | AMAP management, FAIR admin | M | D-A, E-2 §1, §3, §6, §11, CA, N14, DOC-33, principle 1 | Proposed |
| RF-MEM-02 | The system shall provide a public page for each AMAP and a portal with all AMAPs on the platform, from which a prospective member can request to join. | Prospective member | S | E-1 §3.1, D-C, D-D, CA, Brainstorm 14/10 | Proposed |
| RF-MEM-03 | The system shall manage a prospective member's joining process, from the request until they become an active member, including the waiting list and trial deliveries. | Prospective member, Management, System | M | E-1 §3.1, E-4, D-A, D-B §3.2, D-C, DOC-22, DOC-23, DOC-38, N16 | Proposed |
| RF-MEM-04 | The system shall allow registering co-producers and give each producer a public profile showing how they produce. | Co-producer, Producer | M | E-1 §3.6, D-A, D-B, D-E, DOC-16, DOC-18, DOC-39 | Proposed |
| RF-MEM-05 | The system shall collect members' acceptance of the terms and their consents, and allow them to exercise their personal data rights (GDPR). | Co-producer, Management | M | D-A, D-B §3.1, DOC-19, DOC-20, DOC-21, DOC-40, GDPR arts. 7, 12, 26 | Proposed |
| RF-MEM-06 | The system shall allow assigning roles with different permissions, and one person may have several roles. | FAIR admin, Management | M | E-1 §3.2, D-C §4.5, CA (AMAPJ) | Proposed |
| RF-MEM-07 | The system shall allow a co-producer to belong to several AMAPs and record their departure in the middle of a subscription. | Co-producer, Management | S | E-2 §6, §7, §9, D-F, DOC-32, C5, Brainstorm 14/10 | Proposed |

## Acceptance criteria

**RF-MEM-01 – Create and configure AMAPs**
- An AMAP has a name, delivery point, distribution day and time, contact and operating rules.
- There can be several independent AMAPs on the platform, and a producer can take part in several.
- An AMAP can have a single producer or several, with the same or different products.
- A rules panel lets management configure what varies between AMAPs: cycle length, subscription deadlines, number of trial deliveries, renewal mode (RF-SUB-06), possible destinations for the basket during absences (RF-ENT-11) and documents (Terms, Guide).

**RF-MEM-02 – Public page and portal**
- The AMAP page shows the presentation, principles, producers and products, place and time, and whether there are places.
- The page has an "I want to join" option, which starts the joining request (RF-MEM-03).
- *(Could)* The portal lists all AMAPs on the platform, with search by location and a link to each one's page.

**RF-MEM-03 – Joining process**
- The prospective member requests to join and the system records who handles the request (main producer or management).
- If there are no places, the person goes on a waiting list ordered by arrival; management may change the order, recording the reason; the person is notified when a place opens (group decision of 21/10).
- Before subscribing, they can have trial deliveries; the number is configurable per AMAP (e.g. 1 or 2), which resolves the difference between E-4 and D-C (DV-01).
- Management can approve or reject the request.
- The system stores each person's status: prospective, on waiting list, on trial, active or left.

**RF-MEM-04 – Co-producer registration and producer profile**
- The co-producer registers with name, email and phone; the tax number (NIF) is only requested if they want an invoice with NIF (CIVA art. 40).
- The producer has a public profile with a description, location, contacts and evidence of how they produce (certificates or photos and a description of the farm).
- The evidence is not verified by the platform or by AMAP management: it is visible to co-producers, who judge it directly (trust logic of the Charter of Principles; PA-01 resolved by the group on 21/10).

**RF-MEM-05 – Terms, consents and GDPR**
- Registration requires accepting the AMAP's Terms and Conditions and Guide, with a declaration of legal age; the system stores the accepted version and date.
- Members can give and withdraw optional consents (e.g. use of data in studies), with proof of date and version.
- Data subjects can view, export, correct and request deletion of their data; the system tracks the response deadline (1 month).
- Each AMAP states the data controllers (the producers) and the contact point.

**RF-MEM-06 – Roles and permissions**
- Roles: co-producer, producer, AMAP management and FAIR administrator, each with different permissions.
- One person can have several roles (e.g. co-producer and management member).

**RF-MEM-07 – Several AMAPs and mid-subscription departure**
- A co-producer can be a member of several AMAPs (e.g. to get deliveries every week) and see all their deliveries in a single calendar.
- A mid-subscription departure is recorded with the reason; the next deliveries can be transferred to a substitute or donated to an organisation.
- Payment adjustments are handled case by case.

## Mapping to the previous version
In the 28/10 review, the 21 previous requirements were grouped into 7 to reduce detail (lecturer's advice). The detail moved to the acceptance criteria.

| New | Combines previous |
|---|---|
| RF-MEM-01 | 01, 02, 03, 21 |
| RF-MEM-02 | 04, 19 |
| RF-MEM-03 | 05, 06, 07, 08, 09 |
| RF-MEM-04 | 10, 11 |
| RF-MEM-05 | 12, 13, 14, 15 |
| RF-MEM-06 | 16 |
| RF-MEM-07 | 17, 18 (already merged into 17), 20 |
