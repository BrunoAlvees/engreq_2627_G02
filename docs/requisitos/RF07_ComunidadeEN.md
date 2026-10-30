# RF07 – Community and organisation

**Updated on:** 28/10/2026 · [Conventions and sources](README.md)

## Description
Supports the community side of the AMAP: accessible rules and documents, volunteer working groups, distribution rotas, assemblies and events (farm visits, workshops). At AMAP Porto, management is done by volunteer producers and co-producers (a Coordinating Team and 6 working groups). The documents exist but are hard to find.

## Stimulus/response sequences
- A new co-producer joins → they get access to the Terms, the Guide and the Charter of Principles.
- Management creates the distribution rota → volunteers sign up and receive reminders.
- Management calls an assembly → members are notified and the minutes are available afterwards.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| FR-39 | The system shall make the AMAP's documents and rules available to members, always in their current version. | Management, Co-producer | M | E-3 §12, D-C, D-E, DOC-29, N11 | Proposed |
| FR-40 | The system shall support the AMAP's volunteer organisation: working groups, distribution rotas and assemblies. | Management, Co-producer | C | D-A, D-B §3.3, D-C §4.5, E-2 §11, E-3, CA (Juntagrico), DOC-28 | To validate (DV-14) |
| FR-41 | The system shall allow organising AMAP events and gathering co-producers' feedback. | Management, Producer | C | E-1 §3.7, E-2 §11, D-C §4.5, DOC-30 | Proposed |

## Acceptance criteria

**FR-39 – Documents and rules**
- Members can easily find the Terms and Conditions, the AMAP Guide and the Charter of Principles.
- The current version is always shown; the versions each member accepted are stored (FR-05).

**FR-40 – Volunteer organisation**
- Management creates working groups, assigns members (producers and co-producers) and defines their tasks *(to validate DV-14: only appears in the old Guide, D-C)*.
- Management creates rotating volunteer rotas for distribution, with sign-up and reminders *(to validate DV-14)*.
- Management calls assemblies and meetings and shares the minutes (assembly confirmed at AMAP Baixa, E-2 and E-3).

**FR-41 – Events and feedback**
- Management or the producer creates events (farm visits, production help days, workshops, social gatherings) and members sign up.
- Management gathers co-producers' feedback on the quality, variety, schedule and format of deliveries.

## Mapping to the previous version
In the 28/10 review, the 6 previous requirements were grouped into 3 to reduce detail (lecturer's advice). The detail moved to the acceptance criteria.

| New | Combines previous |
|---|---|
| FR-39 | 01 |
| FR-40 | 02, 03, 04 |
| FR-41 | 05, 06 |
