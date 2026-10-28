# SRS work split

**Updated on:** 28/10/2026 · **Status:** proposal, to be agreed by the group

Based on the LABDSOFT SRS template (v1.1). The goal is a roughly equal **total** contribution per person, counting both work already done and work still left.

## Work done so far (from the commits)

| Member | Done so far | Amount |
|---|---|---|
| **Bruno Alves** | all requirements (RF01–RF08 and NFR), document analysis, 26 open questions (DV), context diagram, domain model; 28/10: section 2.4 and reduction of the requirements from 135 to 64 (lecturer's advice) | very large |
| **Liane Duarte** | notes from all 3 client sessions, differentiation analysis, order form and Público article transcriptions | large |
| **João Mata** | market dynamics | small |
| **Jakub Piwko** | competitor analysis (draft) | small |
| **Leonor** | no commits yet | none |

## Remaining work per SRS section

Effort scale: 1 = small (a few paragraphs, or moving existing text), 2 = medium, 3 = large, 4+ = very large.

| SRS section | Already in the repo | Effort | Owner |
|---|---|---|---|
| Title page, revision history, approval | — | 1 | Leonor |
| **1 Introduction** (purpose, conventions, scope, references) | conventions in [requisitos/README.md](requisitos/README.md) | 2 | Liane (already in progress) |
| 2.1 Product perspective | [context diagram](requisitos/diagramas/DiagramaContextoEN.md) | 1 | João |
| 2.2 User classes and characteristics, plus personas | actors table in [requisitos/README.md](requisitos/README.md) | 2 | Jakub |
| 2.3 Operating environment | — | 1 | Jakub |
| 2.4 Design and implementation constraints | ✅ done: [srs/2.4](srs/2.4_RestricoesConcecaoImplementacaoEN.md) | 0 | Bruno |
| 2.5 Assumptions and dependencies | hypotheses, decision C6 | 2 | Liane |
| **3 System features:** move RF01–RF08 into the SRS format | clean-up ✅ done 28/10 (103 → 42 requirements, with acceptance criteria) in [requisitos/](requisitos/README.md) | 1 | Bruno |
| 3.x Use case diagrams: RF01–RF04 (members, catalogue, subscriptions, deliveries) | to do | 2 | Bruno |
| 3.x Use case diagrams: RF05–RF08 (payments, communication, community, reports) | to do | 1 | João |
| 4 Data requirements: data dictionary, reports | [logical data model](requisitos/diagramas/ModeloDominioEN.md) | 3 | João |
| 5 Domain model: bounded contexts | overview exists | 2 | Bruno |
| 6 External interfaces, including UI sketches | RNF-INT | 4 | Leonor |
| 7–9 Quality attributes (Safety still missing), i18n, other requirements | NFR reduced 28/10 (32 → 22) in [NFR](requisitos/RNF_AtributosQualidadeEN.md) | 2 | Bruno |
| 10.1 Elicitation process / methodology | — | 2 | Leonor |
| 10.2 Stakeholders: list and **RACI matrix** | — | 3 | Leonor |
| 10.3 Applied techniques (summary; details go to the appendix) | 4 techniques in [tecnicas/](tecnicas/README.md) | 2 | Leonor |
| 10.4 Effort involved: Task / BA / Hours table | — | 2 | Jakub (collects everyone's hours) |
| 10.5 Constraints and limitations | — | 1 | Liane |
| **11 Product backlog:** user stories linked to requirement IDs, estimated hours, priority | — (42 functional requirements after the 28/10 reduction) | 4 | Jakub |
| Appendix: Glossary | — | 2 | Jakub |
| Appendix: Analysis models – subscription cycle flow and delivery day flow | to do in [diagramas/](requisitos/diagramas/README.md) | 2 | Bruno |
| Appendix: Analysis models – joining flow (co-producers and producers) and member/delivery state diagrams | to do in [diagramas/](requisitos/diagramas/README.md) | 2 | João |
| Appendix: Elicitation data detail | [interviews/](interviews/) | 2 | Liane |
| Prepare and run the next client session (DV questions, 8 marked High) | [open questions](tecnicas/DuvidasProcessosAtuaisEN.md) | 3 | Liane |
| Assemble the final Word document and check consistency | — | 3 | Bruno |
| Competitor analysis: PT version | [EN version](tecnicas/CompetitorAnalysis.md) | 1 | Jakub |

## Remaining effort per person

| Member | Points | Role |
|---|---|---|
| Bruno | 12 | owner of chapters 3, 5 and 7, use cases RF01–RF04, two analysis diagrams, Word integrator |
| Liane | 10 | introduction, elicitation data and client contact |
| João | 7 | product perspective, data requirements, use cases RF05–RF08, two analysis diagrams |
| Jakub | 12 | backlog, effort, users, glossary |
| Leonor | 14 | elicitation process, stakeholders, interfaces |

## Notes

- **28/10 update:** the requirements were reduced (lecturer's advice) and João's diagrams were split with Bruno.
- **Order matters.** The backlog depends on chapter 3. Bruno stabilises the requirements first. Meanwhile Jakub writes user stories for the areas that are already stable.
- **Agree the backlog hours together**, for example in one Planning Poker session. Estimates are the basis for prioritisation (T4 slides, pp. 26-27).
- **Effort table (10.4):** everyone should log their own tasks and hours from now on. The template asks for hours per business analyst.
- **Avoid editing one Word file at the same time.** Each person writes their section as `.md` in the repo, in PT and EN like the existing files. Bruno moves finished sections into the Word document.
- This split works like a small RACI matrix for the SRS itself. We can reuse it as an example in section 10.2.
