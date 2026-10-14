# NFR – Quality attributes, interfaces and constraints

**Updated on:** 14/10/2026 · [Conventions and sources](README.md)

Non-functional requirements must be **specific and verifiable** (SRS template). Numerical values marked "Hyp." are group proposals to be discussed and validated. No stakeholder stated them.

## 1. Usability
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-USA-01 | The system shall be usable on mobile phones and computers (responsive interface), with nothing to install for co-producer functions. | M | Hyp. (E-3: WhatsApp, email and phone notes are used today) | To validate |
| RNF-USA-02 | A co-producer who has used the system before shall be able to subscribe to a full cycle in **10 minutes** or less, without help. | S | Hyp. | To validate |
| RNF-USA-03 | The producer's recurring tasks (publishing the box contents, recording a missing item, confirming a payment) shall take **2 minutes** or less each. | S | E-2 §3 ("just produce"), CA ("minimal effort for farmers"), Hyp. (value) | To validate |
| RNF-USA-04 | The system shall comply with WCAG 2.1, level AA. | S | Hyp. | To validate |
| RNF-USA-05 | The co-producer shall be able to see what they will collect at the next delivery and how much they owe within **2 clicks** of the home page. | S | E-3 §1, §10, Hyp. (value) | To validate |

## 2. Security and data protection
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-SEG-01 | Access shall require authentication. Each role only accesses the data it needs: a producer only sees the co-producers who buy from them. | M | D-B §3.1, GDPR | Proposed |
| RNF-SEG-02 | All communications shall be encrypted (HTTPS/TLS). | M | GDPR art. 32 | Proposed |
| RNF-SEG-03 | Allergies and intolerances are health data: they shall only be stored with explicit consent and only be visible to the producers who deliver to that co-producer. | M | E-2 §4, GDPR art. 9 | To validate |
| RNF-SEG-04 | The system shall record who changed orders, deliveries and payments, and when (audit log). | S | Hyp. (C3: disputed amounts) | Proposed |
| RNF-SEG-05 | The system shall make GDPR compliance possible: producers as joint controllers, FAIR as processor, records of processing activities and breach notification within 72 h. | M | D-B, GDPR arts. 26, 28, 30, 33 | Proposed |
| RNF-SEG-06 | Personal data shall be erased or anonymised when the retention period for each purpose ends, unless a legal obligation applies (e.g. tax). | S | D-B §3.1, GDPR art. 5 | Proposed |

## 3. Performance and capacity
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-DES-01 | The system shall support AMAPs with up to **200 co-producers** and several AMAPs in the same installation. | M | E-2 §3, §6 (up to ~50 per AMAP; one CSA with ~200), D-D (34 in 2023) | Proposed |
| RNF-DES-02 | Main pages shall load in **2 seconds** or less for 95% of requests, even on the last subscription day. | S | Hyp. | To validate |

## 4. Availability and reliability
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-DIS-01 | The system shall be available **99.5%** of the time, with no planned maintenance during distributions or the last days of subscription. | S | Hyp. (D-A: distribution on Tuesdays 17:30–19:30) | To validate |
| RNF-DIS-02 | A daily backup shall be made, and it shall be possible to restore data with a maximum loss of 24 hours. | S | Hyp. | To validate |

## 5. Internationalisation and localisation
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-I18N-01 | The interface shall be in **European Portuguese** and ready for other languages (e.g. English, French). | M | CA (none of the solutions analysed has a Portuguese interface) | Proposed |
| RNF-I18N-02 | Amounts in euros with VAT included, dates in dd/mm/yyyy format and the Portuguese time zone. | M | D-A | Proposed |

## 6. External interfaces
| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-INT-01 | The system shall send notifications by email. | M | D-A, D-C §4.6 | Proposed |
| RNF-INT-02 | The system shall export data to spreadsheets (CSV/XLSX). | S | E-2 §2 (current Excel) | Proposed |
| RNF-INT-03 | The system shall be able to send notifications by SMS or WhatsApp. | C | E-3 §12, Hyp. | To validate |
| RNF-INT-04 | The system shall be able to integrate with a licensed payment provider (e.g. MB Way). | W | CA, PSD2 | To validate (C6) |

## 7. Design and business constraints
| ID | Constraint | Prio. | Source | Status |
|---|---|---|---|---|
| RNF-RES-01 | The system shall not issue invoices, because that would require software certified by the Tax Authority (AT). Each producer invoices in their own software. | M | Technique 2 results §5, C4 | To validate (C6) |
| RNF-RES-02 | The system shall not receive or move co-producers' money: payments are made directly to each producer (PSD2). | M | D-C §4.3, PSD2 | To validate (C6) |
| RNF-RES-03 | The solution shall respect the AMAP Charter of Principles: it must not act as a commercial intermediary between producer and co-producer. | M | D-C §4.1, D-E, CA | To validate (C6) |
| RNF-RES-04 | FAIR's pricing model shall not depend on a commission per box or per transaction. | S | CA, D-E; E-1 §4 (minimum fee + volume) | To validate (DV-25) |
| RNF-RES-05 | The solution shall be a platform shared by several AMAPs (multi-AMAP), with each AMAP's data kept separate. | M | CA ("one shared instance for Portuguese AMAPs"), E-2 §1 | Proposed |
