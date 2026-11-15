# 5 Domain model

**Owner:** Bruno Alves · **Updated on:** 14/11/2026 · **Status:** ready for the report
**Sources:** section 3 (FR-01 to FR-45), interview of 10/11 (E-8), [state diagrams (12.2)](../requisitos/diagramas/DiagramasEstadoEN.md). Replaces the first [domain model](../requisitos/diagramas/ModeloDominioEN.md) of 14/10. Diagrams: `requisitos/diagramas/imagens/Dominio*EN.drawio` and `.png`.

# 5 Domain model

The domain model describes the main concepts of FAIR-AMAP and how they relate, using the language of the AMAPs and independently of any technology. It is organised in five bounded contexts: parts of the domain with their own vocabulary and rules, aligned with the features of section 3. The logical data model and the data dictionary derived from it are in section 4.

## 5.1 Domain model overview

The core of the domain is the AMAP and its members: every other context refers to an AMAP, a person and the role that person has in it. Subscriptions made in a cycle generate the deliveries and the amounts to pay; deliveries and payments produce the notices sent to members. Two external systems complete the picture: the licensed payment provider, which splits each payment among the producers, and the notification services.

![Bounded contexts of FAIR-AMAP (context map)](DominioContextosEN.png)

| Bounded context | Purpose | Features | Main concepts |
|---|---|---|---|
| Membership | Who belongs to each AMAP, with which role and status, and under which rules | 3.1 | FAIR (platform), AMAP, AMAP rules, Person, Membership, Consent, Withdrawal request, Producer application, Farm visit |
| Catalogue and subscriptions | What each producer offers in each cycle and what each co-producer subscribes to | 3.2, 3.3 | Producer profile, Product, Variant, Cycle, Offer, Subscription, Subscription line, Exclusion |
| Deliveries | What happens on each delivery date, for each co-producer | 3.4 | Delivery date, Delivery, Delivered item, Missing item, Absence, Collection, Bag label |
| Payments | How much each co-producer pays, to whom, and what FAIR charges | 3.5 | Payment rules, Payment request, Producer share, Payment, FAIR charge |
| Communication and community | Notifications, messages, documents and the life of the AMAP as a community | 3.6, 3.7, 3.8 | Notification, Notice, Message, News post, Document, Event, Working group, Rota shift, Assembly, Feedback, Data export |

## 5.2 Membership

FAIR runs the platform: it sets the pricing model, is the data processor (NFR-08) and its administrators authorise each AMAP and assign its first manager (FR-01, FR-06). An AMAP is registered on the platform and, once authorised, its rules (cycle length, trial deliveries, renewal mode, absence destinations, withdrawal rules) are configured by its own management (FR-01, NFR-24). A person can hold several memberships: in several AMAPs, or as producer and management of the same AMAP (FR-06, FR-07). The membership carries the role and the status whose life cycle is shown in the state diagrams of section 12.2. Consents keep the version and date of each document accepted (FR-05). A producer joins through an application, usually after a farm visit (FR-08); a co-producer who wants to leave mid-period makes a withdrawal request (FR-07).

![Class diagram – Membership](DominioMembershipEN.png)

## 5.3 Catalogue and subscriptions

Each producer has a public profile and a catalogue of products (baskets, extras and one-off products), each with one or more variants and their price type (FR-11 to FR-13). An offer places a variant in a cycle, with that cycle's price and capacity, so that the catalogue can be reused from one cycle to the next (FR-11, FR-14). A co-producer makes one subscription per cycle, with one line per offer chosen, possibly from several producers (FR-18). Exclusions (allergies, intolerances, dislikes) belong to the co-producer, not to a single subscription (FR-19, NFR-06).

![Class diagram – Catalogue and subscriptions](DominioCatalogoEN.png)

## 5.4 Deliveries

Each cycle has a calendar of delivery dates per producer (FR-24). On each date, every co-producer with a subscription has one delivery, whose status is planned, absent, collected, not collected or cancelled (state diagram in 12.2). The delivered items record the actual quantity or weight and the substitution made (FR-26); missing items record the compensation (FR-26). A delivery may have an absence, with the destination of the basket and who collects it (FR-27), and is closed by a collection, confirmed with the button or the QR code of the bag label (FR-28, FR-29).

![Class diagram – Deliveries](DominioEntregasEN.png)

## 5.5 Payments

Payment rules state the methods accepted by the AMAP, the account of each producer and when each product is charged (FR-30). A payment request groups, for one co-producer and one period, the shares of all producers (FR-31). The co-producer settles it with one payment, processed by the licensed payment provider, which transfers each producer's share; the system never holds the money (FR-32, NFR-19). Payments made outside the platform are recorded manually (FR-32). The FAIR charge is what FAIR charges each AMAP per period: a fee per AMAP plus a percentage of the transactions (FR-34, NFR-21).

![Class diagram – Payments](DominioPagamentosEN.png)

## 5.6 Communication and community

This context gathers what keeps members informed and organised. Notifications are generated by events of the other contexts and sent through the channels each person chooses (FR-35, FR-38); notices, messages and news posts are written by management or by producers (FR-36, FR-37). Documents keep their versions (FR-39). Events, working groups, rota shifts, assemblies and feedback support the community side of the AMAP (FR-40, FR-41), and data exports only contain anonymised data or data from members who gave consent (FR-44). Indicators (FR-43) are calculated from the other contexts and are not stored.

![Class diagram – Communication and community](DominioComunicacaoEN.png)
