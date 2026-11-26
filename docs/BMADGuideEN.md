# BMAD Method — quick guide for the group

We use the **BMAD Method** (v6.12) to implement TP2 with AI agents. It makes the AI follow
**our** plan (domain model → story map → stories with acceptance criteria → code + tests)
instead of improvising. Portuguese version: [GuiaBMADPT.md](GuiaBMADPT.md).

## 1. Setup (once, ~5 min)

1. `git pull` — BMAD is already in the repo (`_bmad/`, `.claude/skills/`, `.agents/skills/`).
2. Install **uv** (BMAD runs small Python scripts): https://docs.astral.sh/uv/
3. Open **your** AI agent **in the repository folder**:

   | You use | Run | Rules file it reads |
   |---|---|---|
   | Claude Code | `claude` | `CLAUDE.md` → `AGENTS.md` |
   | ChatGPT → **Codex CLI** | `codex` | `AGENTS.md` |
   | Gemini → **Gemini CLI** | `gemini` | `GEMINI.md` → `AGENTS.md` |

   ⚠️ The ChatGPT / Gemini **web chats do not see the repo** and cannot run BMAD. Use the CLI agents.
4. Optional — talk to the agent in your language: create `_bmad/custom/config.user.toml`
   (not committed) with:
   ```toml
   [core]
   communication_language = "Portuguese (Portugal)"
   ```

## 2. The one command to remember

Ask the agent: **`bmad-help`** — *"bmad-help, what should I do next?"*
It looks at what already exists and tells you the next step.

## 3. The flow we follow

| Step | Who | Skill to ask for | Output |
|---|---|---|---|
| 0 | **Group, without AI** | — | Domain model, story map (MVP / MVI1 / MVI2 / Backlog) and priorities in `docs/` |
| 1 | 1 member | `bmad-prd` | PRD from the TP2 brief + our story map |
| 2 | 1 member | `bmad-architecture` | Architecture (REST API, stack, components) |
| 3 | 1 member | `bmad-create-epics-and-stories` | Stories with acceptance criteria |
| 4 | Scrum Master | `bmad-sprint-planning` | `sprint-status.yaml` (who does what) |
| 5 | **Each member, own story** | `bmad-build` + story id | Code + tests for that story |
| 6 | Another member | `bmad-code-review` | Review before merging |
| — | When the plan changes | `bmad-correct-course` | Change proposal |

Planning outputs go to `_bmad-output/planning-artifacts/`, stories and sprint status to
`_bmad-output/implementation-artifacts/`. **Both are committed**, so every agent sees the same plan.

## 4. Rules (full list in [AGENTS.md](../AGENTS.md))

- The AI does not invent requirements. If something is unclear → we ask the client.
- A story is done only when **every acceptance criterion has a passing test**.
- One story per branch / per member. Pull before starting.
- **Log every AI use** in [ai-usage-log.md](ai-usage-log.md) — the report must list it, with prompts.
- You must be able to **explain without notes** anything the AI produced for you.
