# AGENTS.md — rules for every AI agent in this repository

Read by Codex and (through `CLAUDE.md` / `GEMINI.md`) by Claude Code and Gemini CLI.
Human guide: [docs/BMADGuideEN.md](docs/BMADGuideEN.md) · [docs/GuiaBMADPT.md](docs/GuiaBMADPT.md).

## Project

FAIR-AMAP, ENGREQ (ISEP 2026/27), Group 02. A web platform that supports the regular
activity of AMAPs/CSAs. Pilot: AMAP Porto. TP2 = build an MVP in two Scrum sprints
(Sprint 1: 23/11 → 13/12, Sprint 2: 14/12 → 10/01). Brief: `docs/engreq_tp2_2026_27.pdf`.

## The plan is the group's, not yours

1. **Never invent requirements.** The sources of truth, in this order:
   1. `docs/engreq_tp2_2026_27.pdf` (the 7 user stories of Sprint 1);
   2. the group's domain model, story map and backlog in `docs/` and `_bmad-output/planning-artifacts/`;
   3. the TP1 SRS in `docs/srs/` (non-functional requirements, glossary);
   4. professor feedback: `docs/RecomendacoesDefesaTP1PT.md`.
   If something is missing or ambiguous, **stop and ask** — the group asks the client, not the AI.
2. **Domain model first.** Code entities follow the domain model and the glossary (same names).
   No `string` where a domain type belongs (Quantity + Unit, Money, DateRange, enums).
3. **One story at a time.** Implement only the story you were given, within its acceptance criteria.

## Definition of done (every story)

- Every acceptance criterion has at least one automated test, and all tests pass.
- REST API design (resources, HTTP verbs, status codes).
- Only free / open-source technologies.
- Story file updated (status, files changed) in `_bmad-output/implementation-artifacts/`.

## AI-use log (required by the TP2 report)

The report must list where AI was used and the prompts. After each BMAD workflow or relevant
prompt, append one line to `docs/ai-usage-log.md`: date, member, tool, workflow/prompt, what
was produced, what the group changed.

## Repository conventions

- Documents for the report: Markdown, **PT and EN** versions (suffix `PT` / `EN`).
  BMAD planning/implementation artifacts can be English only.
- Do not edit or delete other members' files without being asked.
- Never `git push` or commit unless the member explicitly asks.
