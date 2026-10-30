# RF02 – Catalogue and offers

**Updated on:** 28/10/2026 · [Conventions and sources](README.md)

## Description
Lets each producer maintain their catalogue (baskets, extra products and one-off items) and set, for each product, the variants, price type, frequency and capacity. Today the catalogue lives in Google Forms: many options end up as free text and some products exist but are not listed (e.g. dried mushrooms).

## Stimulus/response sequences
- The producer creates a product and sets its price type and frequency → the product becomes available for the next cycle.
- The producer reuses the previous cycle's catalogue → the system copies the products and the producer only adjusts prices and dates.
- A product's capacity runs out → the system stops accepting subscriptions and offers the waiting list.
- The producer has a surplus or a new product → they publish a one-off offer, limited to X co-producers or to a quantity per person.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| FR-11 | The system shall allow the producer to manage their catalogue of baskets, extra products and one-off items, without a closed list of products. | Producer | M | E-1 (class 1), E-2 §4–5, E-3 §11, D-A, N13 | Proposed |
| FR-12 | The system shall allow the producer to offer several basket types and variants of each product. | Producer | M | E-2 §4, E-3 §3, §11, D-A, DOC-06, DOC-07, DOC-15 | Proposed |
| FR-13 | The system shall allow setting each product's price type and frequency. | Producer | M | D-A, E-1 §3.3, E-2 §7, DOC-04, DOC-05, C9 | Proposed |
| FR-14 | The system shall allow setting a maximum capacity per product and per AMAP and manage a waiting list when it is reached. | Producer | M | D-A, E-1 §3.5, DOC-08, N16 | Proposed |
| FR-15 | The system shall show the co-producer each product's details sheet. | Co-producer | S | D-A, DOC-16 | Proposed |
| FR-16 | The system shall allow the producer to publish one-off offers (e.g. surpluses or new products), which co-producers can order outside their subscription. | Producer, Co-producer | S | E-3 §11, N10, Brainstorm 14/10 | Proposed |

## Acceptance criteria

**FR-11 – Manage the catalogue**
- The producer creates, edits and deactivates products; there is no closed list (it is one thing today and may be another tomorrow).
- Each product is one of three types: basket, extra or one-off.
- When preparing a new cycle, the producer can reuse the previous cycle's catalogue and only adjust prices and dates.

**FR-12 – Basket types and variants**
- A producer can offer several basket types (e.g. farm basket, fruit basket), each with a name, description, approximate weight, number of varieties and price.
- A product can have variants (e.g. price level, size, variety, gluten-free), each with its own price.
- *(Could)* The producer can state alternatives to a product (e.g. dried mushrooms when there are no fresh ones).
- *(Could)* The system avoids duplication between basket and one-off items (e.g. reducing one-off blueberries when the basket already includes them).

**FR-13 – Price and frequency**
- Price types: fixed monthly fee, price per unit and price per kg with the actual weight recorded at delivery.
- Frequency: fortnightly, monthly, quarterly, one-off delivery, only in certain months, or on dates chosen by the co-producer.
- *(Could, to validate C9 and DV-24)* The producer can set a discount on extra products for those who already subscribe to a basket.

**FR-14 – Capacity and waiting list**
- Maximum capacity is set per product and per AMAP.
- When capacity is reached, the system stops accepting subscriptions and offers the waiting list.

**FR-15 – Product details sheet**
- The sheet shows the description, certification, storage and shelf life, origin (own production or another producer's) and price with VAT included.
- The producer's details are on the producer's public profile (FR-04).

**FR-16 – One-off offers**
- The producer can limit the offer to a maximum number of co-producers (first come, first served) and/or a maximum quantity per person.
- The producer states the available quantity; the system deducts it as orders arrive and closes the offer when it runs out; the producer can adjust the quantity at any time.

## Mapping to the previous version
In the 28/10 review, the 15 previous requirements were grouped into 6 to reduce detail (lecturer's advice). The detail moved to the acceptance criteria.

| New | Combines previous |
|---|---|
| FR-11 | 01, 02, 11 |
| FR-12 | 03, 04, 12, 13 |
| FR-13 | 05, 06, 15 |
| FR-14 | 07 |
| FR-15 | 08 |
| FR-16 | 10, 14 |
| *(FR-04)* | 09 (producer details, already covered by the producer's public profile) |
