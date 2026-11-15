# 7 Quality attributes · 8 Internationalisation · 9 Other requirements

**Owner:** Bruno Alves · **Updated on:** 14/11/2026 · **Status:** ready for the report
**Sources:** [RNF_AtributosQualidadeEN.md](../requisitos/RNF_AtributosQualidadeEN.md) §1–§5 and source codes in [requisitos/README.md](../requisitos/README.md)

# 7 Quality attributes

This section specifies the non-functional requirements on how well FAIR-AMAP must work. Each one is written so that it can be verified. Numerical values marked **Hyp.** in the source column are group proposals: no stakeholder stated them, and they must be confirmed with FAIR before development. Interface requirements (NFR-15 to NFR-17) are in section 6, and requirements that act as constraints (NFR-18 to NFR-24) are in section 2.4.

## 7.1 Usability

Most co-producers use the system on the phone, often at the pick-up point, and producers want to spend as little time as possible on administration ("just produce", E-2). Usability is therefore measured by the time and the number of steps the most frequent tasks take.

| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| NFR-01 | The system shall be a **responsive web application** (mobile and desktop) that requires nothing to be installed, and can be installed on the phone's home screen as a **PWA**, without going through app stores. The system shall explain simply how to install the app (Android and iPhone) and turn on notifications. | M | E-3; group decision of 21/10 | Proposed |
| NFR-02 | The most frequent tasks shall be quick: a co-producer who has used the system before subscribes to a full cycle in **10 minutes** or less, without help; each recurring producer task (publishing the basket contents, recording a missing item, confirming a payment) takes **2 minutes** or less; the co-producer sees what they will collect and how much they owe within **2 clicks** of the home page. | S | E-2 §3, E-3 §1, §10, CA; Hyp. (values) | Proposed |
| NFR-03 | The system shall comply with **WCAG 2.1, level AA**. | S | Hyp. | Proposed |

**Verification:** NFR-02 is checked with usability tests with at least five co-producers and two producers from a pilot AMAP, timing each task; NFR-03 with an automatic accessibility checker plus a manual review of the main screens.

## 7.2 Performance

The load is concentrated on a few moments: the last day of each subscription period and the distribution time, when many co-producers open the app at once.

| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| NFR-09 | The system shall support AMAPs with up to **200 co-producers** and several AMAPs in the same installation. | M | E-2 §3, §6, D-D | Proposed |
| NFR-10 | Main pages shall load in **2 seconds** or less for 95% of requests, even on the last subscription day. | S | Hyp. | Proposed |

**Rationale:** today AMAPs have up to about 50 co-producers, but one Portuguese CSA already has about 200 (E-2); designing for 200 per AMAP leaves room to grow. NFR-10 is checked with a load test that simulates every co-producer of a 200-member AMAP subscribing in the same hour.

## 7.3 Security

FAIR-AMAP stores personal data (contacts, tax number, payments) and, for some co-producers, health data (allergies and intolerances). Security and privacy follow the GDPR; the controller and processor roles are in NFR-08.

| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| NFR-04 | Access shall require **authentication**. Each role only accesses the data it needs: a producer only sees the co-producers who buy from them. | M | D-B §3.1, GDPR | Proposed |
| NFR-05 | All communications shall be **encrypted** (HTTPS/TLS). | M | GDPR art. 32 | Proposed |
| NFR-06 | Allergies and intolerances are **health data**: they shall only be stored with explicit consent, only be visible to the producers who deliver to that co-producer, and never appear on printed labels or sheets (which show only the name and the substitutions made). | M | E-2 §4, GDPR art. 9, brainstorm 14/10 | Proposed |
| NFR-07 | The system shall record **who changed** orders, deliveries and payments, and **when** (audit log). | S | Hyp. (C3: disputed amounts) | Proposed |
| NFR-08 | The system shall make **GDPR compliance** possible: producers as joint controllers, FAIR as processor, records of processing activities, breach notification within 72 h, and erasure or anonymisation of personal data when the retention period for each purpose ends, unless a legal obligation applies (e.g. tax). | M | D-B, D-B §3.1, GDPR arts. 5, 26, 28, 30, 33 | Proposed |

## 7.4 Safety

FAIR-AMAP does not control physical equipment, so the harm it can cause is indirect. The group identified four risks; each one is covered by requirements already in this SRS, so no new requirement was added. No safety certification applies.

| Risk | Possible harm | Safeguard | Requirements |
|---|---|---|---|
| A co-producer receives a product they are allergic to | Health harm | Exclusions recorded by the co-producer are shown to the producer when preparing the basket, and the substitution is recorded; health data stays private (never on labels) | FR-19, NFR-06 |
| Orders, deliveries or payments are lost | The producer does not know what to deliver; co-producers pay twice or not at all | Daily backup with at most 24 h of data loss; audit log of every change | NFR-11, NFR-07 |
| A co-producer takes another member's bag | Health harm if the bag contains a product they are allergic to; the other member is left without a basket | Each label shows the name and "Bag x of y"; when the producer prints QR labels, scanning warns if the bag is not theirs (E-8) | FR-28, FR-29 |
| Money is lost or held by the platform | Financial loss for co-producers or producers | The system never holds the money; payments go through a licensed provider | NFR-19, NFR-17 |

## 7.5 Availability and reliability

AMAPs do not need the system 24 hours a day: what matters are the distribution times and the end of each subscription period. The requirement is tied to those periods instead of a generic percentage (group decision of 28/10).

| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| NFR-11 | The system shall be available during each AMAP's **distribution times** and the **last 3 days of each subscription period**; planned maintenance takes place outside those periods. A **daily backup** shall be made, with a maximum loss of **24 hours** of data. | S | D-A, E-3 §9; group decision of 28/10 | Proposed |
| NFR-12 | Collection confirmation shall work with a **weak network** at the pick-up point: it is stored on the phone and sent when there is a connection. | C | Brainstorm 14/10; Hyp. | Idea |

# 8 Internationalisation and localisation requirements

The first release is for Portuguese AMAPs: none of the solutions analysed has a Portuguese interface (CA). English is also needed from the start, because some co-producers are foreigners living in Portugal (E-8). FAIR's business model only works at scale (NFR-21, NFR-22), so the system must be ready for other countries without being rewritten.

| ID | Requirement | Prio. | Source | Status |
|---|---|---|---|---|
| NFR-13 | The interface shall be in **European Portuguese** and **English**, and ready for other languages (e.g. French). | M | CA, E-8 (foreign co-producers) | Proposed |
| NFR-14 | The system shall show amounts in **euros with VAT included**, dates in **dd/mm/yyyy** format and times in the **Portuguese time zone**. | M | D-A | Proposed |

**Verification:** NFR-13 is met when every interface text comes from translation files, so a new language only needs a new file with no code changes.

# 9 Other requirements

There are no requirements that do not fit the previous sections. The other non-functional requirements are:

- **constraints** from regulation, the AMAP principles, FAIR's business model and the architecture (NFR-18 to NFR-24): section 2.4;
- **external interfaces** (notifications, spreadsheet export, payment provider; NFR-15 to NFR-17): section 6.

Legal requirements (GDPR and PSD2) are covered by NFR-04 to NFR-08 (section 7.3) and NFR-19 (section 2.4).
