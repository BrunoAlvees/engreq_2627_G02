# 11 Product backlog

**Owner:** Jakub Piwko · **Updated on:** 14/11/2026 · **Status:** draft, features 3.1–3.8; story points to be agreed by the group (Planning Poker)
**Sources:** functional requirements in section 3 and [requisitos/](../requisitos/README.md), acceptance criteria in [12.4](12.4_AcceptanceCriteriaEN.md), user classes in [2.2](2.2_UserClassesEN.md)

This section summarises the features as **user stories**: *As a <user class (2.2)>, I want <goal>, so that <benefit>*. Stories are numbered 1, 2, 3… across the whole backlog. One requirement (IR Nr.) may result in several stories, and one story may cover more than one requirement. The detail of each story is in the acceptance criteria of its requirements (appendix 12.4).

**Estimates.** Stories are estimated in **story points (SP)** on the scale 1, 2, 3, 5, 8. A story larger than 8 SP is split into smaller stories. Reference: 1 SP = a small change to an existing screen; 2 SP = one simple screen; 3 SP = a form with validation and a notification; 5 SP = a workflow with several states, or rules used by other features; 8 SP = the largest story allowed. To give the estimate in hours that the template asks for, **1 SP ≈ 4 hours** of one developer, covering design, implementation, tests and review (group reference, to be confirmed).

**Priority** uses the MoSCoW values of section 1.2. A story takes the priority of its requirement unless a reason is given.

**Release (MVP path).** The **MVP** is the smallest release with which one AMAP can run a full subscription cycle on the platform during the pilot in Portugal (E-8): members join, subscribe, receive and collect their baskets, and pay. As a rule, Must stories are in the **MVP**, Should stories in **R2** and Could stories in **R3**; exceptions are explained below each table.

## 11.1 Feature 3.1 – AMAP and member management

| US Nr. | IR Nr. | User story | SP | Hours | Priority | Release |
|---|---|---|---|---|---|---|
| 1 | FR-01 | As a person who runs an AMAP, I want to register my AMAP and submit its documents (name, location, representative, NIF), so that it can be authorised. | 3 | 12 | M | MVP |
| 2 | FR-01, FR-06 | As a FAIR administrator, I want to check a new AMAP's documents, authorise it and assign its first manager, so that only real AMAPs use the platform. | 2 | 8 | M | MVP |
| 3 | FR-01 | As AMAP management, I want to set my AMAP's delivery place, day and time and its maximum number of co-producers, so that members know where and when to collect. | 2 | 8 | M | MVP |
| 4 | FR-01, NFR-24 | As AMAP management, I want to configure my AMAP's operating rules (cycle length, subscription deadlines, absence and withdrawal options), so that the platform follows how my AMAP works. | 5 | 20 | M | MVP |
| 5 | FR-02 | As a prospective co-producer, I want to see an AMAP's public page (producers, place, time, free places), so that I can decide whether to join. | 3 | 12 | S | R2 |
| 6 | FR-02 | As a prospective co-producer, I want to search all the AMAPs on the platform by location, so that I can find one near me. | 3 | 12 | C | R3 |
| 7 | FR-03, FR-04, FR-05 | As a prospective co-producer, I want to ask to join an AMAP by registering (name, email, phone) and accepting its Terms and Guide, so that management can consider my request. | 3 | 12 | M | MVP |
| 8 | FR-03 | As AMAP management, I want to approve or reject joining requests and see each person's status, so that I know who is in the AMAP. | 3 | 12 | M | MVP |
| 9 | FR-03 | As a prospective co-producer, I want to go on the waiting list when the AMAP is full and be notified when a place opens, so that I do not have to keep checking. | 3 | 12 | M | MVP |
| 10 | FR-03 | As AMAP management, I want new members to get a configurable number of trial deliveries before subscribing, so that they can try the AMAP first. | 3 | 12 | S | R2 |
| 11 | FR-04, FR-08 | As a producer, I want a public profile with my location, products and evidence of how I produce (certificates or photos), so that co-producers trust my products. | 3 | 12 | M | MVP |
| 12 | FR-05 | As a member, I want to give or withdraw optional consents and view, export, correct or ask to delete my data, so that I can exercise my rights under the GDPR. | 5 | 20 | M | MVP |
| 13 | FR-06 | As AMAP management, I want to assign and remove roles, with one person allowed several roles, so that each person only sees what their role allows. | 5 | 20 | M | MVP |
| 14 | FR-07 | As a co-producer, I want to belong to several AMAPs and see all my deliveries in one calendar, so that I can get a basket every week. | 3 | 12 | S | R2 |
| 15 | FR-07 | As a co-producer, I want to ask to leave mid-period, so that, if management accepts, my remaining deliveries are refunded and the producers are told to stop. | 5 | 20 | S | R2 |
| 16 | FR-08 | As a producer, I want to apply to an AMAP, or accept its invitation, with my farming method and certificates, so that the AMAP can assess me. | 3 | 12 | M | MVP |
| 17 | FR-08 | As AMAP management, I want to record the farm visit and approve or reject a producer, so that approved producers become active or go on the waiting list. | 3 | 12 | M | MVP |
| 18 | FR-09 | As a producer, I want to announce that I am leaving an AMAP with its notice period, so that management and co-producers are told and can plan. | 3 | 12 | S | R2 |
| 19 | FR-09 | As AMAP management, I want the system to calculate what each co-producer paid and did not receive when a producer leaves, and record the refund or compensation, so that nobody loses money. | 5 | 20 | S | R2 |
| 20 | FR-10 | As AMAP management, I want to set an end date for my AMAP and export its data first, so that we keep our records before personal data is anonymised. | 3 | 12 | C | R3 |
| 21 | FR-45 | As AMAP management or a producer, I want to import members, subscriptions and products from a spreadsheet template, with a preview of rows that could not be read, so that we do not re-enter data by hand. | 5 | 20 | C | R3 |

**Feature 3.1 total:** 73 SP ≈ 292 hours · MVP 40 SP (160 h) · R2 22 SP (88 h) · R3 11 SP (44 h).

**Notes:**
- **Story 4** covers the general rules panel of FR-01. The rules of other features are configured in their own stories (trial deliveries in story 10, renewal in feature 3.3), so that no story is larger than 8 SP.
- **Story 10 (S):** FR-03 is Must, but trial deliveries were not confirmed by the client in E-8 (AS-11). The waiting list (story 9) was confirmed and stays in the MVP.
- After approval (story 17), the producer states the dates and products they can deliver through the catalogue (feature 3.2) and the calendar (feature 3.4).

## 11.2 Feature 3.2 – Catalogue and offers

| US Nr. | IR Nr. | User story | SP | Hours | Priority | Release |
|---|---|---|---|---|---|---|
| 22 | FR-11 | As a producer, I want to create, edit and deactivate products of three types (basket, extra, one-off), with no closed list, so that my catalogue matches what I produce. | 3 | 12 | M | MVP |
| 23 | FR-11 | As a producer, I want to copy the previous cycle's catalogue and only adjust prices and dates, so that I do not rebuild it every cycle. | 2 | 8 | M | R2 |
| 24 | FR-12 | As a producer, I want to offer several basket types, each with a name, description, approximate weight, number of varieties and price, so that co-producers can choose the basket that suits them. | 3 | 12 | M | MVP |
| 25 | FR-12 | As a producer, I want to add variants to a product (e.g. size, variety, gluten-free), each with its own price, so that co-producers do not have to ask for them in free text. | 3 | 12 | M | MVP |
| 26 | FR-13 | As a producer, I want to set each product's price type (fixed monthly fee, per unit, or per kg with the actual weight recorded at delivery), so that co-producers are charged correctly. | 5 | 20 | M | MVP |
| 27 | FR-13 | As a producer, I want to set each product's frequency (fortnightly, monthly, quarterly, one-off, certain months or dates chosen by the co-producer), so that deliveries follow my production. | 5 | 20 | M | MVP |
| 28 | FR-14 | As a producer, I want to set how many co-producers I accept per product, so that subscriptions close and the waiting list opens when I reach my limit. | 3 | 12 | M | MVP |
| 29 | FR-15 | As a co-producer, I want to see a product's details sheet (description, certification, storage, origin, price with VAT), so that I know what I am buying. | 2 | 8 | S | R2 |
| 30 | FR-16 | As a producer, I want to publish a one-off offer with an available quantity and a limit per person or number of co-producers, which closes when it runs out, so that I can sell surpluses. | 5 | 20 | S | R2 |

**Feature 3.2 total:** 31 SP ≈ 124 hours · MVP 22 SP (88 h) · R2 9 SP (36 h).

**Notes:**
- **Story 23 (M, R2):** copying the catalogue is only needed from the second cycle, so it is not part of the MVP, although FR-11 is Must.
- The AMAP's own capacity is set in story 3; story 28 adds the capacity per producer (FR-14, E-8) and reuses the waiting list of story 9.
- The *(Could)* items in the acceptance criteria of FR-12 and FR-13 (alternatives, duplicates, discount on extras) are not in the backlog until they are validated with the client (C9, DV-24).

## 11.3 Feature 3.3 – Cycles and subscriptions

| US Nr. | IR Nr. | User story | SP | Hours | Priority | Release |
|---|---|---|---|---|---|---|
| 31 | FR-17 | As AMAP management, I want to open a cycle with its length, opening date and subscription deadline, so that members are notified and can subscribe until the deadline. | 3 | 12 | M | MVP |
| 32 | FR-18 | As a co-producer, I want to choose products from several producers of my AMAP in one step, with quantity and variant, so that I do not fill in one form per producer. | 5 | 20 | M | MVP |
| 33 | FR-18 | As a co-producer, I want to choose delivery dates and structured options where a product needs them (e.g. meat, loose instead of basket), so that I do not have to write them as free text. | 3 | 12 | M | MVP |
| 34 | FR-18 | As a co-producer, I want to see a summary with the estimated monthly amount per producer and receive a confirmation, so that I know what I ordered and what I will pay. | 3 | 12 | M | MVP |
| 35 | FR-19, NFR-06 | As a co-producer, I want to record my exclusions (allergies, intolerances, dislikes), visible only to my producers, so that my basket is adapted. | 3 | 12 | M | MVP |
| 36 | FR-19 | As a producer, I want to see my co-producers' exclusions and record the substitution I made, so that I can adapt each basket. | 2 | 8 | M | MVP |
| 37 | FR-20 | As AMAP management, I want subscription requests after the deadline to stay pending until I approve or refuse them, so that late members can still join when possible. | 3 | 12 | S | R2 |
| 38 | FR-20 | As a producer, I want to set until when co-producers can change their order before each delivery, so that they can change it during the cycle without contacting me. | 5 | 20 | S | R2 |
| 39 | FR-21 | As a co-producer, I want to see my current subscriptions and history at any time, so that I no longer need the email copy of my form. | 2 | 8 | M | MVP |
| 40 | FR-22 | As a co-producer, I want to be asked in advance whether I will renew, with my previous order pre-filled, so that renewing takes one step and producers can plan. | 3 | 12 | S | R2 |
| 41 | FR-22 | As AMAP management, I want to choose whether renewal is an intention or a mandatory confirmation by a deadline, after which unconfirmed places go to the waiting list, so that the rule fits my AMAP. | 3 | 12 | S | R2 |
| 42 | FR-23 | As a producer, I want to see the totals ordered per product, variant, delivery date and AMAP, so that I can plan production and harvesting. | 3 | 12 | M | MVP |

**Feature 3.3 total:** 38 SP ≈ 152 hours · MVP 24 SP (96 h) · R2 14 SP (56 h).

**Notes:**
- **Stories 32–34:** FR-18 (subscribe in a single step) is the core of the MVP and would be larger than 8 SP as one story, so it is split into choosing products, choosing dates and options, and the summary with confirmation.
- In the MVP, subscriptions simply close at the deadline set in story 31; late requests (story 37) and order changes during the cycle (story 38) come in R2.
- **Stories 40–41 (R2):** renewal is only needed at the end of the first cycle, and the renewal mode is still to be validated (DV-12).

## 11.4 Feature 3.4 – Calendar and deliveries

| US Nr. | IR Nr. | User story | SP | Hours | Priority | Release |
|---|---|---|---|---|---|---|
| 43 | FR-24 | As AMAP management, I want the cycle's distribution dates to be created from the AMAP's day and time, and to change single dates (e.g. public holidays), so that everyone knows when distribution takes place. | 3 | 12 | M | MVP |
| 44 | FR-24 | As a producer, I want to set my delivery dates for the cycle within the AMAP's distribution time, with my own frequency, product-specific dates and delivery mode, so that co-producers know when I deliver. | 5 | 20 | M | MVP |
| 45 | FR-24 | As a co-producer, I want to see in one calendar the delivery dates of all producers I buy from, so that I know what arrives on each date. | 3 | 12 | M | MVP |
| 46 | FR-25 | As a producer, I want to publish the basket contents before each delivery, so that I no longer send them by WhatsApp. | 3 | 12 | M | MVP |
| 47 | FR-25 | As a co-producer, I want to see what I will collect on each date from all producers, adjusted for my exclusions and with the approximate weight, so that I can plan how to carry it home. | 3 | 12 | M | MVP |
| 48 | FR-26 | As a producer, I want to confirm a product's availability before delivery, so that the affected co-producers are notified in time. | 3 | 12 | M | MVP |
| 49 | FR-26 | As a producer, I want to record missing items and the compensation given (discount or substitution), so that co-producers do not pay for what they did not receive. | 3 | 12 | M | MVP |
| 50 | FR-26 | As a producer, I want to record the actual quantity or weight delivered to each co-producer (e.g. meat), so that products priced per kg are charged correctly. | 2 | 8 | M | MVP |
| 51 | FR-27 | As a co-producer, I want to report an absence, choose what happens to my basket from my AMAP's options and say who collects it, so that the basket is not wasted and the producer is notified. | 3 | 12 | M | MVP |
| 52 | FR-28 | As a co-producer, or someone collecting for them, I want to confirm the collection with one button in the app, so that the producer knows the basket was collected. | 2 | 8 | M | MVP |
| 53 | NFR-12 | As a co-producer at a pick-up point with weak coverage, I want my confirmation to be stored on the phone and sent later, so that I do not have to wait for a signal. | 3 | 12 | C | R3 |
| 54 | FR-28 | As a producer, I want the system to remind those who have not confirmed and to flag uncollected baskets at the end of the distribution slot, so that I know the same day. | 3 | 12 | M | MVP |
| 55 | FR-28 | As a volunteer, AMAP management or a producer, I want to confirm a collection on behalf of a co-producer without a phone, so that every collection is recorded. | 2 | 8 | M | MVP |
| 56 | FR-29 | As AMAP management, I want to print the distribution sheet for each date as an A4 PDF, showing what each co-producer takes from each producer, so that distribution works without phones. | 3 | 12 | S | R2 |
| 57 | FR-29, FR-28 | As a producer with a printer, I want A4 sheets of bag labels with a QR code each, so that co-producers confirm by scanning and are warned if the bag is not theirs. | 5 | 20 | S | R2 |

**Feature 3.4 total:** 46 SP ≈ 184 hours · MVP 35 SP (140 h) · R2 8 SP (32 h) · R3 3 SP (12 h).

**Notes:**
- Story 43 builds on the AMAP's day, time and place set in story 3; story 45 shows one AMAP, and story 14 (R2) extends it to several AMAPs.
- **Stories 52–55:** FR-28 is the only requirement of this feature validated by the client (E-8): the in-app button is essential, so it is in the MVP; the QR labels (story 57) are optional (E-8).
- **Story 53** comes from NFR-12, which is Could and still an idea to assess during implementation.

## 11.5 Feature 3.5 – Payments

| US Nr. | IR Nr. | User story | SP | Hours | Priority | Release |
|---|---|---|---|---|---|---|
| 58 | FR-30 | As AMAP management, I want to choose which payment methods of the provider are available (e.g. MB Way, Multibanco reference, card), so that members pay in ways they already use. | 2 | 8 | M | MVP |
| 59 | FR-30, NFR-17 | As a producer, I want to link the account where I receive my share, so that I am paid directly by the payment provider. | 3 | 12 | M | MVP |
| 60 | FR-30 | As a producer, I want to set when each product is charged (in advance for the cycle, monthly, or after delivery or weighing), so that payments follow how I sell. | 3 | 12 | M | MVP |
| 61 | FR-31 | As a co-producer, I want the system to calculate my amount for each period (basket fees + extras + weighed products − compensated missing items), broken down by producer, so that I know exactly what I owe. | 5 | 20 | M | MVP |
| 62 | FR-31 | As a co-producer, I want to receive the payment request and see the total, the breakdown by producer and my payment history in one view, so that I no longer copy prices into a note. | 3 | 12 | M | MVP |
| 63 | FR-32, NFR-19 | As a co-producer, I want to make one online payment per period that is recorded automatically when the provider confirms it, so that I do not pay each producer separately. | 5 | 20 | M | MVP |
| 64 | FR-32, NFR-19 | As a producer, I want the provider to split each payment among producers and show any method fees deducted, so that I receive my share without the platform holding the money. | 3 | 12 | M | MVP |
| 65 | FR-32 | As AMAP management, I want to record payments made outside the platform (e.g. cash), so that every member's status is correct. | 2 | 8 | M | MVP |
| 66 | FR-33 | As AMAP management or a producer, I want to see the payment status of each co-producer and be notified of late payments, so that I can follow them up. | 3 | 12 | M | MVP |
| 67 | FR-33 | As a producer, I want a summary for each period of who paid, how much, when and what it covers, so that I no longer do the maths in Excel. | 3 | 12 | M | MVP |
| 68 | FR-34 | As a FAIR administrator, I want to set the pricing model (minimum fee per AMAP plus a percentage, which can be zero during the pilot) and see the amount for each AMAP, so that FAIR can charge for the platform. | 3 | 12 | C | R3 |

**Feature 3.5 total:** 35 SP ≈ 140 hours · MVP 32 SP (128 h) · R3 3 SP (12 h).

**Notes:**
- **Stories 63–64:** FR-32 (centralised collection, validated in E-8) is split into the co-producer's payment and the split among producers. The split is done by the licensed provider (NFR-19); the stories cover the integration only.
- Invoicing is out of scope (E-6, NFR-18), so there are no invoicing stories.
- **Story 68 (C, R3):** the platform is almost free during the pilot (E-8), so FAIR charges are not needed in the MVP.

## 11.6 Feature 3.6 – Communication and notifications

| US Nr. | IR Nr. | User story | SP | Hours | Priority | Release |
|---|---|---|---|---|---|---|
| 69 | FR-35 | As a co-producer, I want a reminder before each delivery, with the lead time set by my AMAP, showing what I will collect, so that I do not forget my basket. | 3 | 12 | M | MVP |
| 70 | FR-35, NFR-15 | As a user, I want to be notified automatically of the events that concern me (cycle opening, new offers, basket contents, date changes, missing items, uncollected basket, payment request), so that I do not have to check the app. | 5 | 20 | M | MVP |
| 71 | FR-36 | As AMAP management, I want to send a notice to all members or to a group (e.g. only producers), so that I no longer depend on WhatsApp groups. | 3 | 12 | M | MVP |
| 72 | FR-37 | As a producer, I want to exchange messages with a co-producer and write to all my co-producers, so that I can answer questions in one place. | 5 | 20 | S | R2 |
| 73 | FR-37 | As a producer, I want to post production news on my profile, sent to my co-producers and linkable to a missing product, so that they understand why a product is missing. | 3 | 12 | S | R2 |
| 74 | FR-38, NFR-15 | As a user, I want to choose whether I receive notifications by email, push or both, so that I get them where I read them. | 3 | 12 | S | R2 |
| 75 | FR-38, NFR-15 | As a user, I want to receive individual notifications on WhatsApp through the official WhatsApp Business API, so that I get them in the app I use most. | 5 | 20 | C | R3 |

**Feature 3.6 total:** 27 SP ≈ 108 hours · MVP 11 SP (44 h) · R2 11 SP (44 h) · R3 5 SP (20 h).

**Notes:**
- **Story 70** builds the shared notification mechanism (email in the MVP); other stories (e.g. 9, 31, 48, 54) only define when a notification is sent.
- **Story 75 (C):** FR-38 is Should, but WhatsApp is optional in its acceptance criteria and depends on the WhatsApp Business API (DE-04).

## 11.7 Feature 3.7 – Community and organisation

| US Nr. | IR Nr. | User story | SP | Hours | Priority | Release |
|---|---|---|---|---|---|---|
| 76 | FR-39, FR-05 | As a member, I want to find the current Terms and Conditions, Guide and Charter of Principles, with the versions I accepted stored, so that I always know the rules in force. | 3 | 12 | M | MVP |
| 77 | FR-40 | As AMAP management, I want to create working groups, assign members and define their tasks, so that volunteer work is organised. | 3 | 12 | C | R3 |
| 78 | FR-40 | As a co-producer, I want to sign up for a distribution rota and get a reminder, so that distribution always has volunteers. | 5 | 20 | C | R3 |
| 79 | FR-40 | As AMAP management, I want to call assemblies and meetings and share the minutes, so that every member can take part and stay informed. | 3 | 12 | C | R3 |
| 80 | FR-41 | As AMAP management or a producer, I want to create events (e.g. farm visits, workshops) with member sign-up, so that the community meets beyond deliveries. | 3 | 12 | C | R3 |
| 81 | FR-41 | As AMAP management, I want to gather co-producers' feedback on quality, variety, schedule and format of deliveries, so that the AMAP can improve. | 3 | 12 | C | R3 |

**Feature 3.7 total:** 20 SP ≈ 80 hours · MVP 3 SP (12 h) · R3 17 SP (68 h).

**Note:** stories 77–78 are still to be validated with the client (DV-14): working groups and rotas appear only in the old AMAP Porto Guide (D-C).

## 11.8 Feature 3.8 – Reports and indicators

| US Nr. | IR Nr. | User story | SP | Hours | Priority | Release |
|---|---|---|---|---|---|---|
| 82 | FR-42, NFR-16 | As a producer, I want to export orders and deliveries to CSV or XLSX, filtered by cycle, date, AMAP and product, so that I can keep working in my own spreadsheets. | 3 | 12 | S | R2 |
| 83 | FR-43 | As AMAP management, I want to see social indicators (co-producers, people fed, producers supported, retention between cycles), so that I can report to funded projects. | 3 | 12 | C | R3 |
| 84 | FR-43 | As AMAP management, I want to see environmental indicators (e.g. kilometres travelled, CO2, waste avoided), so that I can show the AMAP's benefits. | 5 | 20 | C | R3 |
| 85 | FR-44, FR-05 | As AMAP management, I want to export data for network organisations and researchers, only anonymised or from members who gave consent, so that research is possible without breaking the GDPR. | 5 | 20 | C | R3 |

**Feature 3.8 total:** 16 SP ≈ 64 hours · R2 3 SP (12 h) · R3 13 SP (52 h).

**Note:** story 84 needs data the platform does not collect yet (e.g. distances), so its estimate is the least certain.

## 11.9 Summary

| Feature | Stories | SP | Hours | MVP | R2 | R3 |
|---|---|---|---|---|---|---|
| 3.1 AMAP and member management | 1–21 | 73 | 292 | 40 | 22 | 11 |
| 3.2 Catalogue and offers | 22–30 | 31 | 124 | 22 | 9 | 0 |
| 3.3 Cycles and subscriptions | 31–42 | 38 | 152 | 24 | 14 | 0 |
| 3.4 Calendar and deliveries | 43–57 | 46 | 184 | 35 | 8 | 3 |
| 3.5 Payments | 58–68 | 35 | 140 | 32 | 0 | 3 |
| 3.6 Communication and notifications | 69–75 | 27 | 108 | 11 | 11 | 5 |
| 3.7 Community and organisation | 76–81 | 20 | 80 | 3 | 0 | 17 |
| 3.8 Reports and indicators | 82–85 | 16 | 64 | 0 | 3 | 13 |
| **Total** | **85** | **286** | **1144** | **167 SP (668 h)** | **67 SP (268 h)** | **52 SP (208 h)** |

**MVP path.** The MVP (167 SP ≈ 668 h) follows the subscription cycle: the AMAP is authorised and configured (3.1) → producers set up their catalogue (3.2) → management opens a cycle and co-producers subscribe (3.3) → baskets are delivered and collected (3.4) → co-producers pay once and producers receive their share (3.5), with reminders and notices (3.6) and the AMAP's rules available (3.7). R2 makes the cycle easier to repeat (renewal, catalogue copy, order changes, messages); R3 adds community and reporting features.

**Not included:** the technical foundation shared by all stories (project setup, login, PWA installation, hosting and backups, translations; e.g. NFR-01, NFR-05, NFR-11, NFR-13). The group should decide whether to add it as separate stories.
