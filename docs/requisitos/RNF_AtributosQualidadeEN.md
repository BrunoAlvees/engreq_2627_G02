# NFR – Quality attributes, interfaces and constraints

**Updated on:** 28/10/2026 · [Conventions and sources](README.md)

Non-functional requirements must be **specific and verifiable** (SRS template). Numerical values marked "Hyp." are group proposals to be discussed and validated. No stakeholder stated them.

## 1. Usability
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-USA-01 | The system shall be a responsive web application (mobile and desktop) that requires nothing to be installed, and can be installed on the phone's home screen as a PWA, without going through app stores. The system shall explain simply how to install the app (Android and iPhone) and turn on notifications. | M | E-3 (WhatsApp, email and phone notes are used today); group decision of 21/10 (avoids App Store and Play Store costs and publishing) | Proposed |
| RNF-USA-02 | The most frequent tasks shall be quick: a co-producer who has used the system before subscribes to a full cycle in **10 minutes** or less, without help; each recurring producer task (publishing the basket contents, recording a missing item, confirming a payment) takes **2 minutes** or less; the co-producer sees what they will collect and how much they owe within **2 clicks** of the home page. | S | E-2 §3 ("just produce"), E-3 §1, §10, CA ("minimal effort for farmers"), Hyp. (values) | To validate |
| RNF-USA-03 | The system shall comply with WCAG 2.1, level AA. | S | Hyp. | To validate |

## 2. Security and data protection
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-SEG-01 | Access shall require authentication. Each role only accesses the data it needs: a producer only sees the co-producers who buy from them. | M | D-B §3.1, GDPR | Proposed |
| RNF-SEG-02 | All communications shall be encrypted (HTTPS/TLS). | M | GDPR art. 32 | Proposed |
| RNF-SEG-03 | Allergies and intolerances are health data: they shall only be stored with explicit consent, only be visible to the producers who deliver to that co-producer, and never appear on printed labels or sheets (which show only the name and the substitutions made). | M | E-2 §4, GDPR art. 9, Brainstorm 14/10 | To validate |
| RNF-SEG-04 | The system shall record who changed orders, deliveries and payments, and when (audit log). | S | Hyp. (C3: disputed amounts) | Proposed |
| RNF-SEG-05 | The system shall make GDPR compliance possible: producers as joint controllers, FAIR as processor, records of processing activities, breach notification within 72 h, and erasure or anonymisation of personal data when the retention period for each purpose ends, unless a legal obligation applies (e.g. tax). | M | D-B, D-B §3.1, GDPR arts. 5, 26, 28, 30, 33 | Proposed |

## 3. Performance and capacity
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-DES-01 | The system shall support AMAPs with up to **200 co-producers** and several AMAPs in the same installation. | M | E-2 §3, §6 (up to ~50 per AMAP; one CSA with ~200), D-D (34 in 2023) | Proposed |
| RNF-DES-02 | Main pages shall load in **2 seconds** or less for 95% of requests, even on the last subscription day. | S | Hyp. | To validate |

## 4. Availability and reliability
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-DIS-01 | The system shall be available during each AMAP's distribution times and the last 3 days of each subscription period; planned maintenance takes place outside those periods. A daily backup shall be made, with a maximum loss of 24 hours of data. | S | D-A (distribution on Tuesdays 17:30–19:30, subscription deadlines), E-3 §9 (collection confirmation), group decision of 28/10 (requirement tied to actual use instead of a generic percentage) | Proposed |
| RNF-DIS-02 | Collection confirmation shall work with a weak network at the pick-up point: it is stored on the phone and sent when there is a connection. | C | Brainstorm 14/10, Hyp. | Idea (assess during implementation) |

## 5. Internationalisation and localisation
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-I18N-01 | The interface shall be in **European Portuguese** and ready for other languages (e.g. English, French). | M | CA (none of the solutions analysed has a Portuguese interface) | Proposed |
| RNF-I18N-02 | Amounts in euros with VAT included, dates in dd/mm/yyyy format and the Portuguese time zone. | M | D-A | Proposed |

## 6. External interfaces
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-INT-01 | The system shall send notifications by **email** and, when the user turns them on, as **push** notifications on the phone (through the PWA). *(Could)* It may also send them by **WhatsApp** (or SMS) through the official WhatsApp Business API, with individual messages and not through a bot in a group. | M | D-A, D-C §4.6, E-2 §2, E-3 §9, §12, group decisions of 21/10 and 28/10 (unofficial bots break WhatsApp's rules) | Proposed |
| RNF-INT-02 | The system shall export data to spreadsheets (CSV/XLSX). | S | E-2 §2 (current Excel) | Proposed |
| RNF-INT-03 | The system shall be able to integrate with a licensed payment provider (e.g. MB Way) able to split one payment among several producers. | S | Group proposal (based on E-5), CA, PSD2, E-1 | Proposed |

## 7. Design and business constraints
| ID | Constraint | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-RES-01 | The system shall not issue invoices: invoicing is out of scope. Each producer invoices in their own software. | M | E-6; Technique 2 results §5, C4 | Validated |
| RNF-RES-02 | The system shall not hold co-producers' money directly (PSD2). Collection is centralised: the co-producer makes a single payment, split among producers through a licensed payment provider (group option on 21/10). | M | Group proposal (based on E-5), PSD2, E-1, E-2 §13 | Proposed |
| RNF-RES-03 | The solution shall respect the AMAP Charter of Principles: it must not act as a commercial intermediary between producer and co-producer. | M | D-E (Charter of Principles), D-C §4.1, E-2, E-3 §5, CA; group interpretation (technique 2, results §5) | To validate (C6) |
| RNF-RES-04 | FAIR charges a minimum fee per producer plus a percentage of the payment volume that goes through the platform; the amounts are set by FAIR. | S | Group proposal (based on E-1 §4, E-5); CA and D-E favoured no commission | Proposed |
| RNF-RES-05 | The solution shall be a platform shared by several AMAPs (multi-AMAP), with each AMAP's data kept separate. | M | CA ("one shared instance for Portuguese AMAPs"), E-2 §1 | Proposed |
| RNF-RES-06 | The solution shall be maintained by FAIR over time (fixes, security updates and evolution). | S | E-1 (software built by amateurs stops being maintained) | Proposed |
| RNF-RES-07 | Differences between AMAPs and between producers in the same AMAP (cycle length, delivery dates and mode, change deadlines, payment timing, absence rules) shall be handled through configuration, without specific development for each AMAP or producer. | M | Principle 1 of the 14/10 brainstorm, E-2 §1, §11, E-3 §2–§4, §8 | Proposed |

## Mapping to the previous version
In the 28/10 review, the 32 previous requirements were reduced to 22 by combining those that measure the same thing (lecturer's advice to reduce detail).

| New | Combines previous |
|---|---|
| RNF-USA-01 | USA-01, USA-06 |
| RNF-USA-02 | USA-02, USA-03, USA-05 |
| RNF-USA-03 | USA-04 |
| RNF-SEG-03 | SEG-03, SEG-07 |
| RNF-SEG-05 | SEG-05, SEG-06 |
| RNF-DIS-01 | DIS-01 (99.5% replaced by actual-use periods), DIS-02 |
| RNF-DIS-02 | DIS-03 |
| RNF-INT-01 | INT-01, INT-03, INT-05 |
| RNF-INT-03 | INT-04 |
| *(others)* | unchanged |
