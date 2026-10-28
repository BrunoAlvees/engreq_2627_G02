# RF08 – Reports and indicators

**Updated on:** 28/10/2026 · [Conventions and sources](README.md)

## Description
Produces working reports for producers and indicators on the AMAP's benefits for network organisations, funders and researchers. The client (23/09) found indicators interesting but "nice to have, not a must". The Charter of Principles asks AMAPs to assess their benefits continuously and transparently.

## Stimulus/response sequences
- The producer asks for the cycle's order report → the system generates it and allows exporting it (replacing the Excel file).
- Management asks for the year's indicators → the system calculates the number of co-producers, people fed, producers supported and retention.
- A researcher asks for data → only anonymised data, or data from members who gave consent, is exported.

## Functional requirements
| ID | Requirement | Actor | Prio. | Source | Status |
|---|---|---|---|---|---|
| RF-REL-01 | The system shall allow the producer to export orders and deliveries to a spreadsheet. | Producer | S | E-2 §2 (Excel calculations and planning) | Proposed |
| RF-REL-02 | The system shall calculate indicators on the AMAP's social and environmental benefits. | Management | C | E-1 §3.4 ("nice to have, not a must"), D-D, D-E, DOC-37, N15 | Proposed |
| RF-REL-03 | The system shall allow exporting data to network organisations and researchers, only anonymised or from members who gave consent. | Management | C | E-1 §3.4, D-A (consent), RF-MEM-05, GDPR | Proposed |

## Acceptance criteria

**RF-REL-01 – Export orders and deliveries**
- The export can be filtered by cycle, date, AMAP and product, as CSV or XLSX (RNF-INT-02).
- Amounts due, received and late are in RF-PAG-04.

**RF-REL-02 – Indicators**
- Social indicators: number of co-producers, people fed, producers supported and retention between cycles.
- Environmental indicators (e.g. kilometres travelled, CO2, waste avoided).
- They serve the reports required by funded projects of the organisations that run AMAPs (E-1) and the benefit assessment asked for by the Charter of Principles (D-E).

**RF-REL-03 – Data for the network and researchers**
- Only anonymised data, or data from members who gave consent, is exported (RF-MEM-05).

## Mapping to the previous version
In the 28/10 review, the 5 previous requirements were reduced to 3 to reduce detail (lecturer's advice). The detail moved to the acceptance criteria.

| New | Combines previous |
|---|---|
| RF-REL-01 | 01 |
| RF-REL-02 | 03, 04 |
| RF-REL-03 | 05 |
| *(RF-PAG-04)* | 02 (amounts due, received and late, already covered by payment tracking) |
