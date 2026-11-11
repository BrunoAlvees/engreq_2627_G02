# RF01 – AMAP and member management

**Updated on:** 11/11/2026 · [Conventions and sources](README.md)

## Description
Lets users create and configure independent AMAPs (with one or several producers) and manage each person's path: membership request, trial deliveries, waiting list, registration, personal data and consents. Today, joining is done by contacting the main producer directly, data arrives through Google Forms and there is no record of each member's status.

## Stimulus/response sequences
- The prospective member opens the AMAP's public page (or searches the portal) → sees the presentation, the producers and whether there is a place.
- The prospective member asks to join → the system records the request and notifies whoever handles it. If there is no place, it puts them on the waiting list.
- Management accepts the request → the person becomes "on trial" and, after the trial deliveries, is invited to subscribe to the cycle.
- The co-producer asks for their data to be deleted → the system records the request and tracks the response deadline.
- The producer states they will leave the AMAP → the system records the leaving date, notifies management and the co-producers and stops including them in new cycles.
- Management asks for the AMAP to leave the platform → the system allows exporting the data, notifies the members and, on the end date, sets the AMAP to inactive.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| FR-01 | The system shall allow creating and configuring independent AMAPs, with one or several producers and their own operating rules. | AMAP management, FAIR admin | M | D-A, E-2 §1, §3, §6, §11, E-8, CA, N14, DOC-33, principle 1 | Validated (E-8) |
| FR-02 | The system shall provide a public page for each AMAP and a portal with all AMAPs on the platform, from which a prospective member can request to join. | Prospective member | S | E-1 §3.1, D-C, D-D, CA, Brainstorm 14/10 | Proposed |
| FR-03 | The system shall manage a prospective member's joining process, from the request until they become an active member, including the waiting list and trial deliveries. | Prospective member, Management, System | M | E-1 §3.1, E-4, D-A, D-B §3.2, D-C, DOC-22, DOC-23, DOC-38, N16 | Proposed |
| FR-04 | The system shall allow registering co-producers and give each producer a public profile showing how they produce. | Co-producer, Producer | M | E-1 §3.6, D-A, D-B, D-E, DOC-16, DOC-18, DOC-39 | Proposed |
| FR-05 | The system shall collect members' acceptance of the terms and their consents, and allow them to exercise their personal data rights (GDPR). | Co-producer, Management | M | D-A, D-B §3.1, DOC-19, DOC-20, DOC-21, DOC-40, GDPR arts. 7, 12, 26 | Proposed |
| FR-06 | The system shall allow each AMAP's management to assign roles within the AMAP, with different permissions, and one person may have several roles. | Management, FAIR admin | M | E-1 §3.2, D-C §4.5, CA (AMAPJ), principle 1 (each AMAP has its own rules), group decision of 30/10, E-8 | Proposed |
| FR-07 | The system shall allow a co-producer to belong to several AMAPs and record their departure in the middle of a subscription. | Co-producer, Management | S | E-2 §6, §7, §9, E-8, D-F, DOC-32, C5, Brainstorm 14/10 | Validated (E-8) |
| FR-08 | The system shall manage a new producer joining an AMAP, from the application until they state what they can deliver and when. | Producer, Management | M | E-7 (class of 28/10), E-2 §1 (BioGoods joined when the previous producer left), E-2 §3, E-8 | Validated (E-8) |
| FR-09 | The system shall manage a producer leaving an AMAP, ensuring that deliveries already paid for by co-producers are either made or compensated. | Producer, Management | S | E-2 §1 (the previous producer of AMAP Baixa stopped taking part), D-C, D-E (risk sharing), group proposal of 28/10, E-8 | Partly validated (E-8; notice period still open, PA-04) |
| FR-10 | The system shall allow an AMAP to stop using the platform, exporting its data before it is anonymised. | Management, FAIR admin | C | NFR-22, NFR-08, GDPR art. 20, group proposal of 28/10 | Proposed (PA-04) |
| FR-45 | The system shall allow an AMAP to import its existing data (members, subscriptions and products kept in spreadsheets or form answers) when it starts using the platform. | Management, Producer | C | DE-08 ([2.5](../srs/2.5_PressupostosDependenciasEN.md)), SI-8 ([6](../srs/6_ExternalInterfacesEN.md)), E-2 §2 (Excel per AMAP), E-3 §2 (Google Forms), group agreement of 05/11 | Proposed |

## Acceptance criteria

**FR-01 – Create and configure AMAPs**
- An AMAP has a name, delivery point, distribution day and time, contact and operating rules.
- There can be several independent AMAPs on the platform, and a producer can take part in several.
- An AMAP can have a single producer or several, with the same or different products.
- A rules panel lets management configure what varies between AMAPs: cycle length, subscription deadlines, number of trial deliveries, renewal mode (FR-22), possible destinations for the basket during absences (FR-27), mid-period withdrawal rules (FR-07) and documents (Terms, Guide).
- **Registering a new AMAP (E-8):** the AMAP registers with its name, location, representative and tax number (NIF) and submits the requested documentation; the FAIR administrator checks it and authorises the AMAP.
- The AMAP has a **maximum capacity** of co-producers, limited by premises, transport and space (e.g. 100) (E-8, FR-14).

**FR-02 – Public page and portal**
- The AMAP page shows the presentation, principles, producers and products, place and time, and whether there are places.
- The page has an "I want to join" option, which starts the joining request (FR-03).
- *(Could)* The portal lists all AMAPs on the platform, with search by location and a link to each one's page.

**FR-03 – Joining process**
- The prospective member requests to join and the system records who handles the request (main producer or management).
- If there are no places, the person goes on a waiting list ordered by arrival; management may change the order, recording the reason; the person is notified when a place opens (group decision of 21/10).
- Before subscribing, they can have trial deliveries; the number is configurable per AMAP (e.g. 1 or 2), which resolves the difference between E-4 and D-C (DV-01).
- Management can approve or reject the request.
- The system stores each person's status: prospective, on waiting list, on trial, active or left.

**FR-04 – Co-producer registration and producer profile**
- The co-producer registers with name, email and phone; the tax number (NIF) is only requested if they want an invoice with NIF (CIVA art. 40).
- The producer has a public profile with a description, location, contacts and evidence of how they produce (certificates or photos and a description of the farm).
- The evidence is visible to co-producers (trust logic of the Charter of Principles). AMAP management assesses it in the producer's application, typically with a visit to the farm (FR-08, E-7, E-8).

**FR-05 – Terms, consents and GDPR**
- Registration requires accepting the AMAP's Terms and Conditions and Guide, with a declaration of legal age; the system stores the accepted version and date.
- Members can give and withdraw optional consents (e.g. use of data in studies), with proof of date and version.
- Data subjects can view, export, correct and request deletion of their data; the system tracks the response deadline (1 month).
- Each AMAP states the data controllers (the producers) and the contact point.

**FR-06 – Roles and permissions**
- Roles: co-producer, producer, AMAP management and FAIR administrator, each with different permissions.
- Within each AMAP, **AMAP management** assigns and removes roles (who is management, producer or co-producer); FAIR does not decide on the AMAPs' internal organisation (principle 1, NFR-24).
- The **FAIR administrator** only acts at platform level: authorises the registration of a new AMAP (FR-01), assigns its first manager and provides support.
- One person can have several roles (e.g. co-producer and management member).
- If a producer starts the AMAP, once it is authorised they hold both the **management and producer** roles: they apply as a producer (FR-08) and accept the application as management (E-8).

**FR-07 – Several AMAPs and mid-subscription departure**
- A co-producer can be a member of several AMAPs (e.g. to get deliveries every week) and see all their deliveries in a single calendar.
- As a rule, a co-producer leaves **at the end of the subscription period** (E-8).
- Leaving mid-period is a **withdrawal request**, which must be accepted. If accepted, the amount for the remaining deliveries is refunded. Who accepts it and what happens if it is not accepted depend on how formal the AMAP is (some have a signed commitment), so they are configurable per AMAP (E-8, NFR-24). In practice, leaving is amicable and almost always accepted (e.g. foreign co-producers returning to their country).
- When the withdrawal is accepted, the producers with whom the co-producer had subscriptions are **notified** to stop the deliveries, and the reason is recorded. Alternatively, the next deliveries can be transferred to a substitute or donated to an organisation.
- Payment adjustments are handled case by case.

**FR-08 – New producer joining**
- The producer **applies** to an AMAP or is **invited** by management to apply (E-8).
- The application states name, location, main products and farming method (organic or not) and allows uploading documents (e.g. organic certificate or other certifications), which become part of the public profile (FR-04).
- *(Optional)* Typically, AMAP members visit the farm before deciding; if the visit takes place, it is recorded (date, who went, notes).
- Management or the assembly approves or rejects the application. The process may vary between AMAPs, but always ends in a producer registration.
- An approved producer becomes **active** or, if the AMAP has no capacity, goes to the **waiting list** (FR-03, FR-14). A producer can be in several AMAPs.
- Once approved, the producer states the dates they can deliver (FR-24) and what they can deliver (FR-11).

**FR-09 – Producer leaving**
- A producer leaving is uncommon (E-8). The producer announces their departure with the notice period set by the AMAP in the Terms they accepted when joining (FR-08). By default, they keep delivering until the end of the period already paid for and leave at the end of the subscription period, becoming **inactive**.
- **Leaving mid-period:** that producer's planned deliveries are cancelled and accounts are settled or refunds made, depending on the circumstances (E-8).
- From the leaving date, the producer no longer appears in new cycles, in the catalogue or in the AMAP's calendar, and future charges are cancelled with the provider. The affected co-producers are notified.
- **Leaving without notice:** the system calculates, for each co-producer, the amount paid and not delivered. The AMAP's other producers may offer their own products to compensate for that amount (this is voluntary); the system records the compensation given to each co-producer.
- The compensated amount is still owed by the producer who left to whoever compensated, because the money has already been transferred to them (NFR-19). The system records the settlement until it is resolved; management handles it case by case.
- If nobody compensates, management asks the producer who left for a refund (through the provider or directly) and the system records the status: pending or refunded.
- The producer becomes **inactive** in that AMAP: the profile and history (deliveries, payments) are kept for the accounts and reports, and can be reactivated if they return. If they belong to other AMAPs, they stay active there.
- The data is only deleted if the producer asks (FR-05) or at the end of the retention period (NFR-08); the payment history is anonymised, not deleted.
- If the AMAP is left without a producer for a type of product, management can open a new application (FR-08).

**FR-10 – AMAP leaving the platform**
- Management asks to leave and sets the end date, preferably at the end of a cycle. Members are notified in advance.
- Before the end date, management can export all the AMAP's data (members, subscriptions, deliveries, payments) in CSV or XLSX (NFR-16).
- On the end date, the AMAP becomes **inactive**: the public page is no longer visible and both the charges to co-producers and FAIR's charges stop (FR-34). The data is kept for a grace period, so the AMAP can export it or change its mind.
- At the end of the grace period, personal data is deleted or anonymised (NFR-08); only aggregate figures remain for the indicators (FR-43). The length of the grace period is to be defined with FAIR (PA-04).
- Members who belong to other AMAPs keep their account (FR-07).

**FR-45 – Import of existing data**
- Management or the producer uploads a CSV/XLSX file (members, subscriptions, products) and the system shows a preview with the rows it could not read before saving anything.
- Imported people are not active members until they accept the terms and consents (FR-05); personal data is only imported for people the AMAP is entitled to contact (NFR-08).
- The expected file format is a template provided by the system. Answers from Google Forms are imported through their spreadsheet export. Direct connection to other tools is out of scope.
- Priority *Could*: without it, each AMAP re-enters its data by hand (assumption DE-08 in 2.5).

## Mapping to the previous version
In the 28/10 review, the 21 previous requirements were grouped into 7 to reduce detail (lecturer's advice). The detail moved to the acceptance criteria.

| New | Combines previous |
|---|---|
| FR-01 | 01, 02, 03, 21 |
| FR-02 | 04, 19 |
| FR-03 | 05, 06, 07, 08, 09 |
| FR-04 | 10, 11 |
| FR-05 | 12, 13, 14, 15 |
| FR-06 | 16 |
| FR-07 | 17, 18 (already merged into 17), 20 |
| FR-08 | *(new, 28/10: producer joining, E-7)* |
| FR-09 | *(new, 28/10: producer leaving)* |
| FR-10 | *(new, 28/10: AMAP leaving the platform)* |
| FR-45 | *(new, 05/11: import of existing data, SI-8)* |
