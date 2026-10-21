# Report plan (SRS): section split and diagrams

**Status:** proposal for the group to approve
**Updated on:** 21/10/2026
**Template:** `LABDSOFT - Requirements template for TP1 v1.1`

The grade depends on the defence: **every member must know the whole document**, not only their own sections. That is why each section is reviewed by another member.

## 1. Section split

| Member | SRS sections | Section 3 – System features | Reviews sections of |
|---|---|---|---|
| **Bruno Alves** | 4 Data requirements · 5 Domain model · 12.2 Analysis models | **3.3** RF03 Cycles and subscriptions · **3.4** RF04 Calendar and deliveries · consistency of section 3 | Liane |
| **Liane Duarte** | 1 Introduction (in progress) · 2 Overall description | **3.6** RF06 Communication · **3.7** RF07 Community | João |
| **João Mata** | 6 External interfaces · 7 Quality attributes · 8 Internationalisation and localisation · 9 Other requirements | **3.5** RF05 Payments and invoicing | Jakub |
| **Jakub** | 11 Product backlog (priorities and estimates in hours) | **3.2** RF02 Catalogue and offers · **3.8** RF08 Reports and indicators | Leonor |
| **Leonor** | 10 Elicitation process · 12.1 Glossary · 12.3 Elicitation data | **3.1** RF01 AMAP and member management | Bruno |

### Section 3 – System features
- Each **3.x** maps to a `docs/requisitos/RF0x_*` file and follows the template: **Description**, **Stimulus/Response Sequences** and **Functional Requirements** (with ID, actor, priority, source and status).
- Each member adapts their own RF files to this format.
- Bruno checks the **consistency of section 3**: same format, no requirement duplicated across features, and correct cross-references (e.g. RF03 subscriptions ↔ RF05 payments).

## 2. Diagrams

| Diagram | SRS section | Owner | Status |
|---|---|---|---|
| Context diagram | 2.1 Product perspective | Liane | ✅ Exists (`docs/requisitos/diagramas/`) |
| **Overall use case diagram** (all actors and main use cases) | 2.2 User classes and characteristics | Liane | To do |
| **Use case diagram per feature** | In each 3.x, before the stimulus/response sequences | Owner of each RF | To do |
| Logical data model (entities, attributes, types and keys) | 4.1 Logical data model | Bruno | First version in the domain model |
| Context map (bounded contexts and their relations) | 5.1 Domain model overview | Bruno | To do |
| One diagram per bounded context (Members and AMAP · Offers and subscriptions · Deliveries · Payments) | 5.2–5.4 | Bruno | To do |
| Current process (as-is): Google Forms → Excel → WhatsApp → delivery → monthly amount | 12.2 Analysis models | Bruno | To do |
| Proposed process (to-be): the full cycle with the platform | 12.2 Analysis models | Bruno | To do |
| *(Optional)* Sequence diagrams for the most complex flows | Matching 3.x | Owner of each RF | Optional |
| *(Optional)* Delivery state diagram (to collect → collected / handed over / not collected) | 3.4 or 12.2 | Bruno | Optional |

### Use cases: where they go
The template has no dedicated section for use cases. Proposal:
- **One overall diagram in 2.2**, for the big picture (next to the context diagram in 2.1).
- **One diagram per feature in each 3.x**: each stimulus/response sequence matches a use case.
- The **context diagram** shows the system and the **external systems**; the **use case diagram** shows **what each actor does** inside the system. They complement each other.
- **To be confirmed with the lecturer** whether use cases are expected and where.

### How to draw the diagrams
- **Mermaid** inside the `.md` files, exported to PNG in `docs/requisitos/diagramas/imagens/`, like the existing ones.
- The as-is and to-be processes can use **BPMN** (draw.io or bpmn.io), exported to PNG.
- Each diagram has a **PT and EN** version.

## 3. Common rules
- Each member describes **their own technique** in section 10.2 and sends Leonor **their hours** for section 10.3.
- Every requirement states its **source** (interview, document or technique) and its **priority**.
- Use the IDs and terminology already in `docs/requisitos/` (RF01–RF08, NFR) and in the glossary.
- Every section has a **PT and EN** version.
- Before the defence, hold a session where each member explains their sections to the others.

## 4. To decide
- [ ] Approval of this split by all members.
- [ ] Where the text is written: Markdown in the repository (e.g. `docs/srs/`) with final assembly in the `.docx`, or directly in a shared `.docx`.
- [ ] Who assembles the final `.docx` and ensures consistency.
- [ ] Internal deadline for sections to be ready for review.
- [ ] Confirm use cases with the lecturer.

## Approval
| Member | I approve (✔) / Comments |
|---|---|
| Bruno Alves | |
| Liane Duarte | |
| João Mata | |
| Jakub | |
| Leonor | |
