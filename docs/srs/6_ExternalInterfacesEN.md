# 6 External interface requirements

**Owner:** Leonor Marinho · **Updated on:** 12/11/2026 · **Status:** updated with E-8, for review
**Sources:** [NFR](../requisitos/RNF_AtributosQualidadeEN.md) §1 and §6, [context diagram](../requisitos/diagramas/DiagramaContextoEN.md), feature files [RF01–RF08](../requisitos/README.md); source codes in [requisitos/README.md](../requisitos/README.md)

This section describes how FAIR-AMAP connects to its **users** (6.1), to other **software** (6.2), to **hardware** (6.3) and to **communication channels** (6.4). The requirements themselves are in the NFR file; here they are only referenced (`NFR-nn`) and explained. Interface choices that no stakeholder confirmed are marked *Proposed* or *To validate*.

## 6.1 User interfaces

### 6.1.1 General characteristics

| # | Characteristic | Related requirements | Source | Status |
|---|---|---|---|---|
| UI-1 | **Responsive web application** for mobile and desktop, with nothing to install. It can be added to the phone's home screen as a **PWA**, and the app itself explains how (Android and iPhone) and how to turn on notifications. | NFR-01 | E-3, group decision of 21/10 | Proposed |
| UI-2 | **Mobile first.** Co-producers use the phone at the pick-up point and on foot (E-3 §10); producers and AMAP management use both phone and computer. | NFR-01 | E-3, E-2 | Proposed |
| UI-3 | **Language:** European Portuguese, ready for other languages. Amounts in euros with VAT, dates as dd/mm/yyyy, Portuguese time zone. | NFR-13, NFR-14 | CA, D-A | Proposed |
| UI-4 | **Accessibility:** WCAG 2.1 level AA. | NFR-03 | Hyp. | To validate |
| UI-5 | **Speed of the main tasks:** a co-producer who has used the system subscribes to a cycle in 10 minutes or less, and sees what they will collect and what they owe within 2 clicks of the home page. | NFR-02 | Hyp. (values) | To validate |
| UI-6 | **Roles see different screens.** Each user only sees what their role allows; the same person may have several roles (e.g. co-producer and member of a working group). | NFR-04, FR-06 | D-B §3.1, E-1 §3.2 | Proposed |
| UI-7 | **Contact details always visible** between producers and co-producers, so that the app does not replace the personal relationship. | principle 2 (brainstorm 14/10), N19 | E-3, D-D | Proposed |
| UI-8 | **Error and confirmation messages** are in plain language, say what to do next, and every subscription or order ends with a confirmation the user can look up later (today it is the form copy sent by email). | FR-18, FR-21 | E-3 §2 | Proposed |
| UI-9 | **Sensitive data** (allergies and intolerances) is never shown on printed sheets or labels, which only show the name and the substitutions made. | NFR-06, FR-29 | E-2 §4, GDPR art. 9 | To validate |

### 6.1.2 Main screens per user class

| User class | Screen | What it shows or lets the user do | Requirements |
|---|---|---|---|
| Prospective member | **Public AMAP page / portal of AMAPs** | Producers and how they produce, delivery place and day, rules, free places; button to request to join (or join the waiting list) | FR-02, FR-03, FR-04 |
| Co-producer | **Home** | Next delivery (date, place, what they will collect, approximate weight), amount due, pending reminders | FR-21, FR-25, FR-31, FR-35 |
| Co-producer | **Subscribe to a cycle** | Products of all producers of the AMAP in one form, with options, deadline and a confirmation at the end | FR-17, FR-18, FR-19 |
| Co-producer | **Absence** | Report an absence, choose what happens to the basket from the options the AMAP defined, say who collects it | FR-27 |
| Co-producer | **Collect** | Confirm collection of the basket with a **button** (mandatory, also with a weak network); optionally scan the QR code on the bag label | FR-28, FR-29, NFR-12 |
| Co-producer | **Payments** | Amount per producer and per period, one payment, history | FR-31, FR-32, FR-21 |
| Producer | **Basket and catalogue** | Manage catalogue, publish the contents of the next basket, publish one-off offers | FR-11 to FR-16, FR-25 |
| Producer | **Planning and deliveries** | Totals ordered and aggregated preferences; record missing items, compensations and quantities actually delivered | FR-23, FR-26 |
| AMAP management | **Calendar and distribution** | Delivery calendar per producer, printable distribution sheet and bag labels, uncollected baskets | FR-24, FR-28, FR-29 |
| AMAP management | **Members and payments** | Joining requests and waiting list, roles, notices to members, payment status and late payments | FR-03, FR-06, FR-33, FR-36 |
| FAIR administrator | **Platform administration** | Create and configure AMAPs, support, FAIR charges | FR-01, FR-34 |

### 6.1.3 Interface sketches

Low-fidelity sketches (text) of three key screens. They show content and order only, not the final design. They should be replaced by images when the group has a design tool.

**Co-producer home (mobile)**

```
┌──────────────────────────────┐
│ FAIR-AMAP      AMAP Baixa  ≡ │
├──────────────────────────────┤
│ Next delivery                │
│ Tuesday 18/11 · 17:30-19:30  │
│ UPTEC, Porto                 │
│                              │
│ You will collect:            │
│  • Farm basket (~4 kg)       │
│     – no peppers → carrots   │
│  • Eggs ×1 dozen             │
│  Total ≈ 5 kg                │
│                              │
│ [ I can't collect ]          │
├──────────────────────────────┤
│ Amount due this month        │
│ 32,00 €        [ Pay ]       │
├──────────────────────────────┤
│ Home · Orders · Pay · Contacts│
└──────────────────────────────┘
```

**Subscribe to a cycle (mobile)**

```
┌──────────────────────────────┐
│ Jan–Jun 2027 · closes 04/12  │
├──────────────────────────────┤
│ BioGoods                     │
│  (•) Farm basket   32 €/month│
│  ( ) Fruit basket            │
│  [ ] Eggs                    │
│ Quinta da Serrinha           │
│  [ ] Olive oil               │
│ Exclusions: [ peppers      ] │
├──────────────────────────────┤
│ Total per month: 32,00 €     │
│ [ Confirm subscription ]     │
└──────────────────────────────┘
```

**Producer: record a delivery (mobile or desktop)**

```
┌──────────────────────────────┐
│ Delivery 18/11 · AMAP Baixa  │
├──────────────────────────────┤
│ Basket contents  [ edit ]    │
│  carrots, potatoes, kale ... │
│ Eggs available?  (•) Yes     │
│                  ( ) No      │
│ Missing / compensation:      │
│  [ ______________________ ]  │
│ [ Save and notify members ]  │
└──────────────────────────────┘
```

> The product names and amounts in the sketches are examples taken from the interviews (basket about 4 kg, 32 € per month, delivery on Tuesdays); they are not requirements.

## 6.2 Software interfaces

| # | Interface | Direction and data | Purpose | Related requirements | Status |
|---|---|---|---|---|---|
| SI-1 | **Licensed payment provider** (e.g. Stripe; MB Way as a payment method), able to split one payment among several producers | Out: payment request with amounts per producer. In: payment confirmation and status | One payment per co-producer per period, without the system holding the money. Payment method fees are a producer cost or are deducted transparently from the amount transferred (E-8) | NFR-17, NFR-19, FR-32, FR-33 | Validated (E-8) |
| SI-2 | **Email service** | Out: notifications, reminders and notices. In: delivery status (optional) | Reminders, confirmations, notices from management | NFR-15, FR-35, FR-36 | Proposed |
| SI-3 | **Web push** through the PWA | Out: push notifications to phones | Same notifications on the phone, when the user turns them on. **On iPhone, push only works if the PWA is installed on the home screen**; otherwise the user only gets email | NFR-01, NFR-15 | Proposed |
| SI-4 | **WhatsApp Business API** (or SMS) | Out: individual messages (not a bot in a group) | Optional channel, because WhatsApp is the channel in use today | NFR-15 *(Could)* | Idea |
| SI-5 | **Spreadsheet export** (CSV/XLSX) | Out: orders, deliveries and payments | For those who work in Excel today | NFR-16, FR-42 | Proposed |
| SI-6 | **PDF generation** (A4) | Out: distribution sheet and bag labels | Printed at the distribution point. The label with the name may carry an **optional QR code**, scanned to confirm collection (E-8) | FR-28, FR-29 | Proposed |
| SI-7 | **Anonymised data export** to network organisations and researchers | Out: anonymised data, or data from members who gave consent | Reports and indicators | FR-44, FR-05 | Proposed |
| SI-8 | **Import of existing data** from spreadsheets (CSV/XLSX) and form answers | In: members, subscriptions and products already kept in Excel and Google Forms | Avoid each AMAP re-entering everything by hand when it starts using the platform | FR-45, assumption DE-08 in [2.5](2.5_PressupostosDependenciasEN.md) | Idea |

**Not in scope:** invoicing software. The system does not issue invoices; each producer keeps invoicing in their own software (NFR-18, E-6), so there is no interface to it.

## 6.3 Hardware interfaces

FAIR-AMAP is a web application and has **no direct interface with specific hardware**. It runs on the users' own devices:

- **Phones and tablets** (Android and iPhone), with a current browser, for the PWA, push notifications and collection confirmation (NFR-01, NFR-12).
- **Computers** with a current browser, for management and producers.
- **Printers** (A4) for the distribution sheet and bag labels (FR-29). The system only generates the PDF. Not every producer has a printer, so printing is optional (E-8).
- **Phone camera** (optional), to scan the QR code on the bag label and confirm collection. The lecturer called it "a nice feature" (E-8). Whoever has no printer or does not scan just taps the button in the app (FR-28).

## 6.4 Communication interfaces

| # | Requirement | Related requirements | Status |
|---|---|---|---|
| CI-1 | All traffic between browser, app and servers uses **HTTPS/TLS**. | NFR-05 | Proposed |
| CI-2 | Notifications go through **email**, **web push** and, optionally, **WhatsApp/SMS**. The user chooses the channels. | NFR-15, FR-38 | Proposed |
| CI-3 | The integration with the payment provider uses the provider's **secure API** (HTTPS). Card or bank data is **never stored** by FAIR-AMAP. | NFR-17, NFR-19, FR-32 | Proposed |
| CI-4 | Collection confirmation works with a **weak network**: it is stored on the phone and sent when there is a connection. | NFR-12 | Idea |
| CI-5 | Personal data in messages is limited to what is needed; health data is **never** sent by email, push or WhatsApp. | NFR-06, NFR-08 | To validate |
| CI-6 | Page speed targets (2 seconds or less for 95% of requests) apply to the communication between user and server. | NFR-10 | To validate |

## Open points

- **Payment provider and channels:** the client accepted collection through a provider such as Stripe (E-8, so C6 is resolved). Still open: which provider and whether MB Way is offered as a method, and which channels co-producers want (many use WhatsApp today).
- **UI sketches:** are they enough for the SRS, or does the lecturer expect mock-ups? To ask in the next session.
- **New identifiers:** `UI-n`, `SI-n` and `CI-n` are local to this section. If the group prefers, they can become `NFR-nn` (the next free number is NFR-25), updating PT and EN.
