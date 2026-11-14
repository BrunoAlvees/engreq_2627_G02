# 11 Product backlog

**Owner:** Jakub Piwko · **Updated on:** 14/11/2026 · **Status:** draft, feature 3.1 only; story points to be agreed by the group (Planning Poker)
**Sources:** functional requirements in section 3 and [requisitos/](../requisitos/README.md), acceptance criteria in [12.4](12.4_AcceptanceCriteriaEN.md), user classes in [2.2](2.2_UserClassesEN.md)

This section summarises the features as **user stories**: *As a <user class (2.2)>, I want <goal>, so that <benefit>*. One requirement (IR Nr.) may result in several stories, and one story may cover more than one requirement. The detail of each story is in the acceptance criteria of its requirements (appendix 12.4).

**Estimates.** Stories are estimated in **story points (SP)** on the scale 1, 2, 3, 5, 8. A story larger than 8 SP is split into smaller stories. Reference: 1 SP = a small change to an existing screen; 2 SP = one simple screen; 3 SP = a form with validation and a notification; 5 SP = a workflow with several states, or rules used by other features; 8 SP = the largest story allowed. To give the estimate in hours that the template asks for, **1 SP ≈ 4 hours** of one developer, covering design, implementation, tests and review (group reference, to be confirmed).

**Priority** uses the MoSCoW values of section 1.2. A story takes the priority of its requirement unless a reason is given.

**Release (MVP path).** The **MVP** is the smallest release with which one AMAP can run a full subscription cycle on the platform during the pilot in Portugal (E-8): members join, subscribe, receive and collect their baskets, and pay. As a rule, Must stories are in the **MVP**, Should stories in **R2** and Could stories in **R3**; exceptions are explained below each table.

## 11.1 Feature 3.1 – AMAP and member management

| US | IR Nr. | User story | SP | Hours | Priority | Release |
|---|---|---|---|---|---|---|
| US-01 | FR-01 | As a person who runs an AMAP, I want to register my AMAP and submit its documents (name, location, representative, NIF), so that it can be authorised. | 3 | 12 | M | MVP |
| US-02 | FR-01, FR-06 | As a FAIR administrator, I want to check a new AMAP's documents, authorise it and assign its first manager, so that only real AMAPs use the platform. | 2 | 8 | M | MVP |
| US-03 | FR-01 | As AMAP management, I want to set my AMAP's delivery place, day and time and its maximum number of co-producers, so that members know where and when to collect. | 2 | 8 | M | MVP |
| US-04 | FR-01, NFR-24 | As AMAP management, I want to configure my AMAP's operating rules (cycle length, subscription deadlines, absence and withdrawal options), so that the platform follows how my AMAP works. | 5 | 20 | M | MVP |
| US-05 | FR-02 | As a prospective co-producer, I want to see an AMAP's public page (producers, place, time, free places), so that I can decide whether to join. | 3 | 12 | S | R2 |
| US-06 | FR-02 | As a prospective co-producer, I want to search all the AMAPs on the platform by location, so that I can find one near me. | 3 | 12 | C | R3 |
| US-07 | FR-03, FR-04, FR-05 | As a prospective co-producer, I want to ask to join an AMAP by registering (name, email, phone) and accepting its Terms and Guide, so that management can consider my request. | 3 | 12 | M | MVP |
| US-08 | FR-03 | As AMAP management, I want to approve or reject joining requests and see each person's status, so that I know who is in the AMAP. | 3 | 12 | M | MVP |
| US-09 | FR-03 | As a prospective co-producer, I want to go on the waiting list when the AMAP is full and be notified when a place opens, so that I do not have to keep checking. | 3 | 12 | M | MVP |
| US-10 | FR-03 | As AMAP management, I want new members to get a configurable number of trial deliveries before subscribing, so that they can try the AMAP first. | 3 | 12 | S | R2 |
| US-11 | FR-04, FR-08 | As a producer, I want a public profile with my location, products and evidence of how I produce (certificates or photos), so that co-producers trust my products. | 3 | 12 | M | MVP |
| US-12 | FR-05 | As a member, I want to give or withdraw optional consents and view, export, correct or ask to delete my data, so that I can exercise my rights under the GDPR. | 5 | 20 | M | MVP |
| US-13 | FR-06 | As AMAP management, I want to assign and remove roles, with one person allowed several roles, so that each person only sees what their role allows. | 5 | 20 | M | MVP |
| US-14 | FR-07 | As a co-producer, I want to belong to several AMAPs and see all my deliveries in one calendar, so that I can get a basket every week. | 3 | 12 | S | R2 |
| US-15 | FR-07 | As a co-producer, I want to ask to leave mid-period, so that, if management accepts, my remaining deliveries are refunded and the producers are told to stop. | 5 | 20 | S | R2 |
| US-16 | FR-08 | As a producer, I want to apply to an AMAP, or accept its invitation, with my farming method and certificates, so that the AMAP can assess me. | 3 | 12 | M | MVP |
| US-17 | FR-08 | As AMAP management, I want to record the farm visit and approve or reject a producer, so that approved producers become active or go on the waiting list. | 3 | 12 | M | MVP |
| US-18 | FR-09 | As a producer, I want to announce that I am leaving an AMAP with its notice period, so that management and co-producers are told and can plan. | 3 | 12 | S | R2 |
| US-19 | FR-09 | As AMAP management, I want the system to calculate what each co-producer paid and did not receive when a producer leaves, and record the refund or compensation, so that nobody loses money. | 5 | 20 | S | R2 |
| US-20 | FR-10 | As AMAP management, I want to set an end date for my AMAP and export its data first, so that we keep our records before personal data is anonymised. | 3 | 12 | C | R3 |
| US-21 | FR-45 | As AMAP management or a producer, I want to import members, subscriptions and products from a spreadsheet template, with a preview of rows that could not be read, so that we do not re-enter data by hand. | 5 | 20 | C | R3 |

**Feature 3.1 total:** 73 SP ≈ 292 hours · MVP 40 SP (160 h) · R2 22 SP (88 h) · R3 11 SP (44 h).

**Notes:**
- **US-04** covers the general rules panel of FR-01. The rules of other features are configured in their own stories (trial deliveries in US-10, renewal in feature 3.3), so that no story is larger than 8 SP.
- **US-10 (S):** FR-03 is Must, but trial deliveries were not confirmed by the client in E-8 (AS-11). The waiting list (US-09) was confirmed and stays in the MVP.
- After approval (US-17), the producer states the dates and products they can deliver through the catalogue (feature 3.2) and the calendar (feature 3.4).
