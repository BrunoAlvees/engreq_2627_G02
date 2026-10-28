# RF08 – Reports and indicators

**Updated on:** 21/10/2026 · [Conventions and sources](README.md)

## Description
Produces working reports for producers and management (orders, payments) and indicators on the AMAP's benefits for network organisations, funders and researchers. The client (23/09) found indicators interesting but not a priority. The Charter of Principles asks AMAPs to assess their benefits continuously and transparently.

## Stimulus/response sequences
- The producer asks for the cycle's order report → the system generates it and allows exporting it (replacing the Excel file).
- Management asks for the year's indicators → the system calculates the number of co-producers, people fed, producers supported and retention.
- A researcher asks for data → only anonymised data, or data from members who gave consent, is exported.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-REL-01 | The system shall allow the producer to export orders and deliveries (per cycle, date, AMAP and product) in a spreadsheet format. | Producer | S | E-2 §2 | Proposed |
| RF-REL-02 | The system shall show the producer, per month, the amounts due, received and overdue. | Producer | S | E-2 §2, DV-19 | Proposed |
| RF-REL-03 | The system shall calculate indicators of the AMAP's benefits: number of co-producers, people fed, producers supported and retention between cycles. | Management | S | D-D, D-E, E-1 §3.4, DOC-37, N15 | To validate (priority) |
| RF-REL-04 | The system shall calculate environmental indicators (e.g. kilometres travelled, CO2, waste avoided). | Management | C | E-1 (class 1) | To validate (priority) |
| RF-REL-05 | The system shall allow exporting data for network organisations and researchers, only anonymised or from members who gave consent. | Management | C | E-1 §3.4, D-A (consent), RF-MEM-05 | Proposed |
