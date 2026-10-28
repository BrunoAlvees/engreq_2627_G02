# RF06 – Communication and notifications

**Updated on:** 28/10/2026 · [Conventions and sources](README.md)

## Description
Replaces WhatsApp messages and scattered emails with automatic notices and communication channels inside the platform: delivery reminders, AMAP notices and messages between producer and co-producer. Today co-producers forget deliveries and the producer sends a WhatsApp message every week with the basket contents.

## Stimulus/response sequences
- One day before the delivery → the system sends each co-producer a reminder with what they will collect.
- Management posts a notice → all AMAP members receive it.
- The producer posts production news → their co-producers receive it.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-COM-01 | The system shall send users automatic notifications about events that concern them, including a reminder before each delivery. | System | M | E-1 §3.8, §4, E-2 §4, §14, E-3 §9, D-A, D-C, N5 | Proposed |
| RF-COM-02 | The system shall allow AMAP management to send notices to all members or to a group. | Management | M | D-C §4.6, E-3 §12 | Proposed |
| RF-COM-03 | The system shall allow the producer to communicate with their co-producers, through messages and production news. | Producer, Co-producer | S | D-A, D-C §4.6, E-1 §3.8, E-2 §2, N19, Brainstorm 21/10 | Proposed |
| RF-COM-04 | The system shall allow each user to choose how they receive notifications. | Co-producer, Producer | S | E-3 §12, RNF-INT-01, group decisions of 21/10 and 28/10 | Proposed |

## Acceptance criteria

**RF-COM-01 – Automatic notifications**
- Before each delivery, with the configured lead time, the co-producer receives a reminder with what they will collect.
- The system also notifies: cycle opening, new offers, basket contents, date changes, product availability and missing items, uncollected basket and new payment request.

**RF-COM-02 – Management notices**
- Management sends notices to all AMAP members or to a group (e.g. only co-producers, only producers).

**RF-COM-03 – Producer communication**
- The producer exchanges messages with a co-producer and can write to all their co-producers.
- The producer posts news about production (e.g. state of the crops, a pest, weather damage), which stays on their public profile (RF-MEM-04) and is sent to their co-producers.
- A news post can be linked to a missing product (RF-ENT-03), to explain why the basket does not include that product.

**RF-COM-04 – Notification channels**
- Each user chooses the channels: email (RNF-INT-01), push notifications on the phone (RNF-INT-01) and, optionally, WhatsApp (RNF-INT-01).
- WhatsApp is used through the official WhatsApp Business API, with individual messages, not through a bot in a group (unofficial bots break WhatsApp's rules and can get the number banned).

## Mapping to the previous version
In the 28/10 review, the 6 previous requirements were grouped into 4 to reduce detail (lecturer's advice). The detail moved to the acceptance criteria.

| New | Combines previous |
|---|---|
| RF-COM-01 | 01, 02 |
| RF-COM-02 | 03 |
| RF-COM-03 | 04, 05 |
| RF-COM-04 | 06 |
