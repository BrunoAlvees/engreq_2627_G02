# RF02 – Catalogue and offers

**Updated on:** 21/10/2026 · [Conventions and sources](README.md)

## Description
Allows each producer to keep their catalogue (boxes, extra products and loose products) and to set, for each product, its variants, price type, frequency and capacity. Today the catalogue lives in Google Forms: many options end up in free text and some products exist but are not listed (e.g. dried mushrooms).

## Stimulus/response sequences
- The producer creates a product and sets its price type and frequency → the product becomes available for the next cycle.
- The producer reuses the previous cycle's catalogue → the system copies the products and the producer only adjusts prices and dates.
- A product reaches its capacity → the system stops accepting subscriptions and offers the waiting list.
- The producer has a surplus → they publish a one-off offer with a limited quantity.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-CAT-01 | The system shall allow the producer to create, edit and deactivate products in their catalogue, without a closed list of products. | Producer | M | E-2 §5, E-3 §11, N13 | Proposed |
| RF-CAT-02 | The system shall distinguish the product types box, extra and loose. | Producer | M | D-A, E-2 §4–5 | Proposed |
| RF-CAT-03 | The system shall allow a producer to offer several box types, each with a name, description, approximate weight, number of varieties and price. | Producer | M | E-2 §4, D-A, DOC-07 | Proposed |
| RF-CAT-04 | The system shall allow product variants (e.g. price tier, size, variety, gluten-free), each with its own price. | Producer | M | D-A, E-3, DOC-06 | Proposed |
| RF-CAT-05 | The system shall support three price types: fixed monthly fee, price per unit, and price per kg using the actual weight recorded at delivery. | Producer | M | D-A, E-2 §7, DOC-05 | Proposed |
| RF-CAT-06 | The system shall allow setting each product's frequency: weekly, fortnightly, monthly, quarterly, one-off, only in certain months, or on dates chosen by the co-producer. | Producer | M | D-A, E-1 §3.3, DOC-04 | Proposed |
| RF-CAT-07 | The system shall allow setting a maximum capacity per product and per AMAP, and manage a waiting list when it is reached. | Producer | M | D-A, E-1 §3.5, DOC-08, N16 | Proposed |
| RF-CAT-08 | The system shall show each product's details: description, certification, storage and shelf life, origin (own production or from another producer) and VAT included. | Co-producer | S | D-A, DOC-16 | Proposed |
| RF-CAT-09 | The system shall show each producer's profile: description, location, production method, certifications and contacts. | Co-producer | S | D-A, E-1 §3.6, DOC-16, N19 | Proposed |
| RF-CAT-10 | The system shall allow the producer to publish one-off offers (e.g. surpluses) with a limited quantity, which co-producers can order outside their subscription. | Producer, Co-producer | S | E-3 §11, N10 | Proposed |
| RF-CAT-11 | The system shall allow the producer to reuse a previous cycle's catalogue when preparing a new cycle. | Producer | S | E-1 (class 1) | Proposed |
| RF-CAT-12 | The system shall allow the producer to state alternatives to a product (e.g. dried mushrooms when there are no fresh ones). | Producer | C | E-3 §3, §11 | Proposed |
| RF-CAT-13 | The system shall avoid duplication between a box and a loose product (e.g. reduce loose blueberries when the box already includes them). | System | C | D-A, DOC-15 | Proposed |
| RF-CAT-14 | The system shall allow the producer to manage the available quantities (stock) of extra products. | Producer | C | E-3 §11 | Proposed |
