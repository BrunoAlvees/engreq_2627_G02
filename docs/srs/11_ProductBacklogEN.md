# 11 Product backlog

**Owner:** Jakub Piwko · **Updated on:** 13/11/2026 · **Status:** draft, feature 3.1 only; hours to be agreed by the group (Planning Poker)
**Sources:** functional requirements in section 3 and [requisitos/](../requisitos/README.md), acceptance criteria in [12.4](12.4_AcceptanceCriteriaEN.md), user classes in [2.2](2.2_UserClassesEN.md)

This section summarises all the features as **user stories**. One functional requirement (IR Nr.) may result in several user stories. Each story is written from the point of view of a user class from section 2.2: *As a <user class>, I want <goal>, so that <benefit>*.

**Priority** uses the MoSCoW values of section 1.2 (M, S, C). A story normally takes the priority of its requirement; where it differs, the reason is given below the table.

**Estimated hours** cover all stages of development for one story: analysis and design, implementation (interface and server), tests, review and deployment. The estimates use a reference scale (proposal, to be agreed by the group) based on the number and complexity of the acceptance criteria:

| Size | Hours | Typical story |
|---|---|---|
| S | 8 | One screen or one rule, few acceptance criteria |
| M | 16 | A form with validation and notifications, or a simple workflow |
| L | 24 | A workflow with several states, or a rule that depends on other features |
| XL | 32 | Configuration or calculations that affect several features |

## 11.1 Feature 3.1 – AMAP and member management

| US Nr. | IR Nr. | User story | Estimated hours | Priority |
|---|---|---|---|---|
| US-01 | FR-01 | As a person who runs an AMAP, I want to register my AMAP with its name, location, representative and tax number (NIF) and submit the requested documents, so that it can be authorised to use the platform. | 16 | M |
| US-02 | FR-01, FR-06 | As a FAIR administrator, I want to check the documents of a new AMAP, authorise or reject it and assign its first manager, so that only real AMAPs use the platform. | 8 | M |
| US-03 | FR-01 | As AMAP management, I want to configure my AMAP's rules (capacity, cycle length, subscription deadlines, number of trial deliveries, renewal mode, absence options, withdrawal rules, documents) in one rules panel, so that the platform follows how my AMAP works. | 32 | M |
| US-04 | FR-02 | As a prospective co-producer, I want to see an AMAP's public page with its presentation, principles, producers, place and time of delivery and whether there are places, so that I can decide whether to join. | 16 | S |
| US-05 | FR-02 | As a prospective co-producer, I want to search a portal of all the AMAPs on the platform by location, so that I can find one near me. | 16 | C |
| US-06 | FR-03 | As a prospective co-producer, I want to ask to join an AMAP and accept its Terms, so that AMAP management can consider my request. | 16 | M |
| US-07 | FR-03 | As AMAP management, I want to approve or reject joining requests and see each person's status (prospective, waiting list, on trial, active, left), so that I know who is in the AMAP. | 16 | M |
| US-08 | FR-03 | As a prospective co-producer, I want to be put on the waiting list when there are no places and be notified when one opens, so that I do not have to keep checking. | 16 | M |
| US-09 | FR-03 | As AMAP management, I want new members to receive a configurable number of trial deliveries before they subscribe, so that they can try the AMAP first. | 16 | S |
| US-10 | FR-04 | As a co-producer, I want to register with my name, email and phone, with the tax number (NIF) only if I want an invoice with NIF, so that I can use the platform. | 16 | M |
| US-11 | FR-04 | As a producer, I want a public profile with a description, location, contacts and evidence of how I produce (certificates or photos of the farm), so that co-producers know and trust how I produce. | 16 | M |
| US-12 | FR-05 | As a co-producer, I want to accept the AMAP's Terms and Guide when I register and give or withdraw optional consents, so that my choices are recorded with their date and version. | 16 | M |
| US-13 | FR-05 | As a co-producer, I want to view, export, correct and ask for the deletion of my personal data, so that I can exercise my rights under the GDPR. | 24 | M |
| US-14 | FR-06 | As AMAP management, I want to assign and remove roles in my AMAP, with one person allowed several roles, so that each person only sees and does what their role allows. | 24 | M |
| US-15 | FR-07 | As a co-producer, I want to be a member of several AMAPs and see all my deliveries in one calendar, so that I can get deliveries every week. | 16 | S |
| US-16 | FR-07 | As a co-producer, I want to ask to leave in the middle of a subscription period, so that, if AMAP management accepts it, the remaining deliveries are refunded and the producers are told to stop delivering. | 24 | S |
| US-17 | FR-08 | As a producer, I want to apply to an AMAP, or accept an invitation from its management, with my details, farming method and certificates, so that the AMAP can assess my application. | 16 | M |
| US-18 | FR-08 | As AMAP management, I want to record the farm visit and approve or reject a producer's application, so that approved producers become active or go on the waiting list if the AMAP is full. | 16 | M |
| US-19 | FR-08 | As a newly active producer, I want to state the dates and the products I can deliver, so that the AMAP can include me in the next cycle. | 8 | M |
| US-20 | FR-09 | As a producer, I want to announce that I am leaving an AMAP, with the notice period set in its Terms, so that management and co-producers can plan. | 16 | S |
| US-21 | FR-09 | As AMAP management, I want the system to calculate, for each co-producer, what was paid and not delivered when a producer leaves, and record the compensation or refund, so that nobody loses money. | 24 | S |
| US-22 | FR-10 | As AMAP management, I want to set an end date for my AMAP on the platform and export all its data before that date, so that we keep our records. | 16 | C |
| US-23 | FR-10 | As a FAIR administrator, I want the personal data of an AMAP that has left to be deleted or anonymised after a grace period, so that the platform complies with the GDPR. | 8 | C |
| US-24 | FR-45 | As AMAP management or a producer, I want to import members, subscriptions and products from a spreadsheet template, with a preview of the rows that could not be read, so that we do not have to enter our data again by hand. | 24 | C |

**Total for feature 3.1:** 416 hours (Must: 240 h · Should: 112 h · Could: 64 h).

**Priorities that differ from their requirement:**
- **US-04 (S), US-05 (C):** FR-02 is Should; the acceptance criteria mark the portal of all AMAPs as Could, while the AMAP's own page is needed to start a joining request.
- **US-09 (S):** FR-03 is Must, but the trial deliveries were not confirmed by the client in E-8 (AS-11, DV-26). The waiting list (US-08) was confirmed and stays Must.
