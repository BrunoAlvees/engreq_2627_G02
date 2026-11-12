# 10 Elicitation process and methodology

**Owner:** Leonor Marinho · **Updated on:** 04/11/2026 · **Status:** draft for review
**Sources:** assignment ([engreq_tp1_2026_27_v2_EN.pdf](../engreq_tp1_2026_27_v2_EN.pdf)), [interviews/](../interviews/), [tecnicas/](../tecnicas/README.md), [requisitos/README.md](../requisitos/README.md), [SRS work split](../SRSWorkSplitEN.md), git history

## Approach

The assignment asks for the elicitation methodology presented in the course, with all techniques valid and combinable. The group worked in **five steps**, repeated as new information arrived (iterative approach):

| Step | What the group did | Output |
|---|---|---|
| 1. Understand the context | Read the assignment and the first session with the client; identify the domain (AMAP/CSA) and what FAIR wants | [Known information on the project](../interviews/23-09-2026/LevantamentoInfo23_09_v2EN.md) |
| 2. Prepare | Study existing sources before meeting stakeholders: documents, competitors, market, differentiation. Write open questions first and specific ones afterwards (lecturer's advice) | [Techniques 1 to 4](../tecnicas/README.md), question lists |
| 3. Elicit | Sessions with stakeholders (client, producer, co-producer) and notes from classes; group brainstorms | [Session notes and supplements](../interviews/) |
| 4. Analyse and specify | Consolidate what was heard into candidate requirements with a **source** for each one; give priority (MoSCoW); mark what is not validated; reduce and group requirements | [Requirements by feature](../requisitos/README.md) |
| 5. Validate | Take the requirements marked "To validate" and the open questions (DV, PA) to the next sessions; update the documents with the answers | [Questions for the week of 02/11](../interviews/10-11-2026/PerguntasEntrevista10_11PT.md) |

## Principles followed

- **Open questions first, specific ones later.** The first sessions asked about how the AMAP works day to day, the people involved, the documents and what goes wrong. Technical questions came after, with the right stakeholder (advice of 23/09).
- **Documents say what people do not say.** The group asked for and analysed real documents (order form, terms and conditions, guide for new co-producers, charter of principles), and compared them with the interviews to find differences and gaps ([results of technique 2](../tecnicas/ResultadosAnaliseDocumentalEN.md)).
- **Each requirement has a source.** Interviews are coded E-1 to E-7, documents D-A to D-F, techniques CA, DOC and N. This lets the group justify each requirement and trace it back.
- **Nothing is "validated" without the stakeholder.** Information from one stakeholder is treated as one point of view. Uncertain points stay as "To validate" or as open questions.
- **Each AMAP has its own rules** and **an AMAP is made of people** (guiding principles of the 14/10 brainstorm): the system is configurable and does not replace the personal relationship.
- **Everything is recorded in the repository** (planning, sessions, tasks, artefacts), as the assignment requires, in **Portuguese and English**.

## Timeline

| Date | Activity | Type | Evidence |
|---|---|---|---|
| 23/09 | First session: FAIR presented by the lecturer as client | Interview (E-1) | [Notes](../interviews/23-09-2026/LevantamentoInfo23_09_v2EN.md) |
| 29/09 | Session with Sofia Araújo (BioGoods, producer) | Interview (E-2) | [Notes](../interviews/29-09-2026/LevantamentoInfo29_09EN.md), [supplement](../interviews/29-09-2026/Complemento29_09EN.md) |
| 06/10 | Session with Luisa Marques (co-producer, AMAP UPTEC Baixa) and analysis of the order form | Interview (E-3), document analysis | [Notes](../interviews/06-10-2026/LevantamentoInfo06_10EN.md), [supplement](../interviews/06-10-2026/Complemento06_10EN.md) |
| 06/10–14/10 | Techniques 1 to 4 (competitors, document analysis, market, differentiation) | Pre-elicitation | [tecnicas/](../tecnicas/README.md) |
| 07/10 | Class: how new co-producers join (E-4) | Observation | [Requirements README](../requisitos/README.md) |
| 14/10 | Group brainstorm: guiding principles | Brainstorm | [Requirements README](../requisitos/README.md) |
| week of 12/10 | Class: lecturer on the business model (E-5, overheard, not recorded) | Observation | [Requirements README](../requisitos/README.md) |
| 21/10 | Consolidated first list of requirements; decision on centralised collection | Analysis, brainstorm | [requisitos/](../requisitos/README.md) |
| week of 19/10 | Class: invoicing is out of scope (E-6) | Interview (client) | [Requirements README](../requisitos/README.md) |
| 28/10 | Class: how a producer joins an AMAP (E-7); requirements reduced (lecturer's advice) | Interview (client), analysis | [requisitos/](../requisitos/README.md) |
| 30/10 | Identifiers changed to `FR-nn` / `NFR-nn` | Analysis | [Requirements README](../requisitos/README.md) |
| week of 02/11 | Validation sessions with client, producer and AMAP management (30 min) | Interview | [Questions](../interviews/10-11-2026/PerguntasEntrevista10_11PT.md) *(session not yet held when this was written)* |

## Roles in the process

Each business analyst owns one or more techniques or sections (see [10.2](10.2_AppliedTechniquesEN.md) and the [SRS work split](../SRSWorkSplitEN.md)). During sessions the group used three roles: **who asks**, **who takes notes** and **who keeps time** (see the question guide for the week of 02/11). Decisions on scope and priorities are taken **together** in group meetings and recorded in the repository.

## How requirements were treated

1. **Collect** statements, documents and observations, with date and source.
2. **Separate** what was said by the stakeholder from what the group concluded. Doubts become a list of questions (DV, PA).
3. **Write** each requirement as "The system shall…", one verifiable statement per row, with actor, priority, source and status.
4. **Prioritise** with MoSCoW. The priorities are a proposal until the client confirms.
5. **Review and reduce:** requirements that measured the same thing were grouped (103 to 42 functional and 32 to 22 non-functional on 28/10, following the lecturer's advice to reduce detail; new requirements added afterwards bring the current total to 45 FR and 24 NFR).
6. **Validate** in the next session and mark the status "Validated" only with a source.

## Open points

- The session of the week of 02/11 had not yet taken place when this section was written: **update the timeline** with its date and results.
- E-4 (07/10) and E-5 (week of 12/10) were not recorded and were not said directly to the group as the client: confirm with the lecturer.
- Dates of E-5 and E-6 are given by week because the repository does not record the exact day.
