# SRS work split

**Updated on:** 11/11/2026 · **Status:** proposal, to be agreed by the group · **Submission: 15/11/2026**

Based on the LABDSOFT SRS template (v1.1). The goal is a roughly equal **total** contribution per person, counting both work already done and work still left.

## Milestones

Milestones are points where something must be ready **for the whole group** to move on. Task deadlines below are set so that each milestone can be met.

| Date | Milestone | Why it matters |
|---|---|---|
| **07/11** | **Chapter 3 frozen:** FR/NFR IDs and text stable | The backlog (11), use cases and data requirements (4) all refer to these IDs. Changes after this only if the client session requires them. |
| ✅ 10/11 | **Client session** (E-8, 30 minutes; summary in [interviews/10-11-2026](interviews/10-11-2026/Entrevista10_11EN.md)) | Confirmed or rejected the open assumptions (2.5) and doubts (DV, PA). It was the last session before submission: what is still open is a group decision (2.5, 10.4). |
| **09/11** | **Backlog hours agreed** together (Planning Poker) | Estimates are the basis for prioritisation (T4 slides, pp. 26-27). |
| **11/11** | **All sections in the repository** (PT and EN `.md`) | Each section must be final before it goes into Word. |
| 12–13/11 | Word integration: **each member pastes their own sections** into the shared Word document (agreed with Bruno on 11/11) | Use the Word styles; after pasting, update fields (Ctrl+A, F9) so table numbers and the table of contents stay right. |
| 14/11 | Final group review: consistency, IDs, table of contents, revision history | Last chance to fix errors. |
| **15/11** | **Submission** | |

## Work done so far (from the commits)

| Member | Done so far | Amount |
| --- | --- | --- |
| **Bruno Alves** | all requirements (RF01–RF08 and NFR), document analysis, 26 open questions (DV), context diagram, domain model; 28/10: section 2.4 and reduction of the requirements from 135 to 64 (lecturer's advice); use cases RF01–RF02 | very large |
| **Liane Duarte** | notes from all 3 client sessions, differentiation analysis, order form and Público article transcriptions; questions for the next session; drafts of 2.5, 10.4 and 12.3. **11/11:** section 1 (1.1–1.4) written; 2.5, 10.4 and 12.3 updated with E-8 and finalised; technique 4 completed (market coverage, review of four example solutions, D1–D6, conclusions); "Other solutions considered" added to technique 1; requirements README and open statuses updated ("To validate" → "Proposed", NFR-14 and NFR-21 rewritten); sections 1, 2.5, 10.4 and 12.3 converted to Word | very large |
| **João Mata** | market dynamics | small |
| **Jakub Piwko** | competitor analysis (draft) | small |
| **Leonor Marinho** | drafts of the front matter, section 6 and sections 10 to 10.2 | medium |

## Remaining work per SRS section

Effort scale: 1 = small (a few paragraphs, or moving existing text), 2 = medium, 3 = large, 4+ = very large.

| SRS section | Already in the repo | Effort | Owner | Deadline |
| --- | --- | --- | --- | --- |
| Title page, revision history, approval | draft: [srs/0](srs/0_TitlePageRevisionApprovalEN.md) | 1 | Leonor | 14/11 (final revision history) |
| **1 Introduction** (purpose, conventions, scope) | ✅ done: [srs/1](srs/1_IntroductionEN.md), Word version ready | 0 | Liane | — |
| 1.4 References | ✅ done: in [srs/1](srs/1_IntroductionEN.md) (28 references) | 0 | Liane | — |
| 2.1 Product perspective | [context diagram](requisitos/diagramas/DiagramaContextoEN.md) | 1 | João | 09/11 |
| 2.2 User classes and characteristics, plus personas | actors table in [requisitos/README.md](requisitos/README.md) | 2 | Jakub | 09/11 |
| 2.3 Operating environment | — | 1 | Jakub | 09/11 |
| 2.4 Design and implementation constraints | ✅ done: [srs/2.4](srs/2.4_RestricoesConcecaoImplementacaoEN.md) | 0 | Bruno | — |
| 2.5 Assumptions and dependencies | ✅ done: [srs/2.5](srs/2.5_PressupostosDependenciasEN.md), updated with E-8, Word version ready | 0 | Liane | — |
| **3 System features:** move RF01–RF08 into the SRS format | clean-up ✅ done 28/10 (103 → 42 requirements, with acceptance criteria) in [requisitos/](requisitos/README.md) | 1 | Bruno | **07/11** |
| 3.x Use case diagrams: RF01–RF04 (members, catalogue, subscriptions, deliveries) | RF01 and RF02 done in [diagramas/](requisitos/diagramas/README.md) | 2 | Bruno | 09/11 |
| 3.x Use case diagrams: RF05–RF08 (payments, communication, community, reports) | to do | 1 | João | 09/11 |
| 4 Data requirements: data dictionary, reports | [logical data model](requisitos/diagramas/ModeloDominioEN.md) | 3 | João | 11/11 |
| 5 Domain model: bounded contexts | overview exists | 2 | Bruno | 10/11 |
| 6 External interfaces, including UI sketches | draft: [srs/6](srs/6_ExternalInterfacesEN.md) | 4 | Leonor | 11/11 |
| 7–9 Quality attributes (Safety still missing), i18n, other requirements | NFR reduced 28/10 (32 → 22) in [NFR](requisitos/RNF_AtributosQualidadeEN.md) | 2 | Bruno | 09/11 |
| 10 Process adopted for elicitation: methodology (section intro) | draft: [srs/10](srs/10_ElicitationProcessEN.md) | 2 | Leonor | 11/11 |
| 10.1 Stakeholders: list and **RACI matrix** | draft: [srs/10.1](srs/10.1_StakeholdersRACIEN.md) | 3 | Leonor | 11/11 |
| 10.2 Applied techniques (summary; details go to the appendix) | draft: [srs/10.2](srs/10.2_AppliedTechniquesEN.md) | 2 | Leonor | 11/11 |
| 10.3 Effort involved: Task / BA / Hours table | started: [srs/10.3](srs/10.3_EffortInvolvedEN.md) (Liane's hours); each member adds their rows | 2 | Jakub (collects everyone's hours) | everyone sends hours by 10/11; table 11/11 |
| 10.4 Constraints and limitations | ✅ done: [srs/10.4](srs/10.4_RestricoesLimitacoesEN.md), updated with E-8, Word version ready | 0 | Liane | — |
| **11 Product backlog:** user stories linked to requirement IDs, estimated hours, priority | — (44 functional requirements after the 28/10 reduction) | 4 | Jakub | user stories 09/11 (hours agreed together); final 11/11 |
| Appendix: Glossary | — | 2 | Jakub | 11/11 |
| Appendix: Analysis models – subscription cycle flow and delivery day flow | to do in [diagramas/](requisitos/diagramas/README.md) | 2 | Bruno | 10/11 |
| Appendix: Analysis models – joining flow (co-producers and producers) and member/delivery state diagrams | to do in [diagramas/](requisitos/diagramas/README.md) | 2 | João | 10/11 |
| Appendix: Elicitation data detail | ✅ done: [srs/12.3](srs/12.3_DetalheDadosElicitacaoEN.md), with E-8, pasted into Word | 0 | Liane | — |
| Prepare and run the next client session (DV questions, 8 marked High) | ✅ done: [questions](interviews/10-11-2026/PerguntasEntrevista10_11PT.md); session held on 10/11 (E-8) | 0 | Liane | — |
| Assemble the final Word document and check consistency | each member pastes their own sections; final consistency check on 14/11 (group review) | — | everyone | 13/11 |
| Competitor analysis: PT version | [EN version](tecnicas/CompetitorAnalysis.md) | 1 | Jakub | 11/11 |

## Remaining effort per person

| Member | Points | Role |
| --- | --- | --- |
| Bruno | 12 | owner of chapters 3, 5 and 7, use cases RF01–RF04, two analysis diagrams |
| Liane | 0 | introduction, 2.5, 10.4 and elicitation data: all done (11/11); hours for 10.3 in [srs/10.3](srs/10.3_EffortInvolvedEN.md) |
| João | 7 | product perspective, data requirements, use cases RF05–RF08, two analysis diagrams |
| Jakub | 12 | backlog, effort, users, glossary |
| Leonor | 14 | elicitation process, stakeholders, interfaces |

## Notes

- **28/10 update:** the requirements were reduced (lecturer's advice) and João's diagrams were split with Bruno.
- **05/11 update:** deadlines and milestones added for the 15/11 submission; section 10 renumbered to match the lecturer's template (10 intro, 10.1 stakeholders, 10.2 techniques, 10.3 effort, 10.4 constraints).
- **11/11 update:** the client session (E-8) took place on 10/11 and was the last one; each member pastes their own sections into Word. Liane's sections (1, 2.5, 10.4, 12.3) and technique 4 are complete.
- **Order matters.** The backlog depends on chapter 3, so chapter 3 is frozen first (07/11). Meanwhile Jakub writes user stories for the areas that are already stable. Data requirements (4) build on the domain model, and 2.5, 10.4 and 12.3 are closed after the client session.
- **If a deadline cannot be met,** say so in the group as early as possible, so the work can be shared before 11/11.
- **Agree the backlog hours together**, for example in one Planning Poker session. Estimates are the basis for prioritisation (T4 slides, pp. 26-27).
- **Effort table (10.3):** everyone should log their own tasks and hours from now on. The template asks for hours per business analyst.
- **Avoid editing one Word file at the same time.** Each person writes their section as `.md` in the repo, in PT and EN like the existing files, and pastes it into the shared Word document when it is final (agreed on 11/11).
- This split works like a small RACI matrix for the SRS itself. We can reuse it as an example in section 10.1.
