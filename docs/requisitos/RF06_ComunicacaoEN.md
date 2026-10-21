# RF06 – Communication and notifications

**Updated on:** 21/10/2026 · [Conventions and sources](README.md)

## Description
Replaces WhatsApp messages and scattered emails with automatic notifications and communication channels inside the platform: delivery reminders, AMAP announcements and messages between producer and co-producer. Today co-producers forget deliveries, and the producer sends a WhatsApp message every week with the box contents.

## Stimulus/response sequences
- One day before a delivery → the system sends each co-producer a reminder with what they will collect.
- Management posts an announcement → all AMAP members receive it.
- The producer posts farm news → their co-producers receive it.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-COM-01 | The system shall send a reminder before each delivery, with the configured lead time, stating what the co-producer will collect. | System | M | E-1 §3.8, E-2 §14, E-3 §9, N5 | Proposed |
| RF-COM-02 | The system shall automatically notify: cycle opening, new offers, box contents, date changes, product availability, uncollected box and new payment note. | System | M | E-1 §4, E-2 §4, D-A, D-C | Proposed |
| RF-COM-03 | The system shall allow AMAP management to send announcements to all members or to a group (e.g. co-producers only). | Management | M | D-C §4.6, E-3 §12 | Proposed |
| RF-COM-04 | The system shall allow messages between producer and co-producer, and from the producer to all their co-producers. | Producer, Co-producer | S | D-A, D-C §4.6, E-2 §2, N19 | Proposed |
| RF-COM-05 | The system shall allow the producer to post news about production (e.g. state of the crops, weather damage). | Producer | S | E-1 §3.8, N19 | Proposed |
| RF-COM-06 | The system shall allow each user to choose how they receive notifications (e.g. email or in-app notification). | Co-producer, Producer | S | Hyp. (E-3 §12: WhatsApp and email) | To validate |
