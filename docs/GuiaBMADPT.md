# Método BMAD: guia rápido para o grupo

Vamos usar o **método BMAD** (v6.12) para implementar a TP2 com agentes de IA. Com ele, a IA segue
o **nosso** plano (modelo de domínio → story map → stories com critérios de aceitação → código e
testes), em vez de improvisar. Versão inglesa: [BMADGuideEN.md](BMADGuideEN.md).

## 1. Preparação (uma vez, ~5 min)

1. `git pull`: o BMAD já está no repositório (`_bmad/`, `.claude/skills/`, `.agents/skills/`).
2. Instalar o **uv** (o BMAD corre pequenos scripts em Python): https://docs.astral.sh/uv/
3. Abrir o **vosso** agente de IA **na pasta do repositório**:

   | Usas | Corre | Ficheiro de regras que lê |
   |---|---|---|
   | Claude Code | `claude` | `CLAUDE.md` → `AGENTS.md` |
   | ChatGPT → **Codex CLI** | `codex` | `AGENTS.md` |
   | Gemini → **Gemini CLI** | `gemini` | `GEMINI.md` → `AGENTS.md` |

   ⚠️ O chat web do ChatGPT ou do Gemini **não vê o repositório** e não corre o BMAD. Usem os agentes de linha de comandos.
4. Opcional, para o agente falar em português: criar `_bmad/custom/config.user.toml`
   (não vai para o git) com:
   ```toml
   [core]
   communication_language = "Portuguese (Portugal)"
   ```

## 2. O único comando a decorar

Pedir ao agente: **`bmad-help`**, por exemplo *"bmad-help, o que faço a seguir?"*
O agente vê o que já existe e diz qual é o passo seguinte.

## 3. O fluxo que seguimos

| Passo | Quem | Skill a pedir | Resultado |
|---|---|---|---|
| 0 | **O grupo, sem IA** | — | Modelo de domínio, story map (MVP / MVI1 / MVI2 / Backlog) e prioridades em `docs/` |
| 1 | 1 membro | `bmad-prd` | PRD a partir do enunciado e do nosso story map |
| 2 | 1 membro | `bmad-architecture` | Arquitetura (API REST, tecnologias, componentes) |
| 3 | 1 membro | `bmad-create-epics-and-stories` | Stories com critérios de aceitação |
| 4 | Scrum Master | `bmad-sprint-planning` | `sprint-status.yaml` (quem faz o quê) |
| 5 | **Cada membro, a sua story** | `bmad-build` + id da story | Código e testes dessa story |
| 6 | Outro membro | `bmad-code-review` | Revisão antes de juntar ao `main` |
| — | Quando o plano muda | `bmad-correct-course` | Proposta de alteração |

O planeamento fica em `_bmad-output/planning-artifacts/`, e as stories e o estado do sprint em
`_bmad-output/implementation-artifacts/`. **Ambos vão para o git**, para todos os agentes verem o mesmo plano.

## 4. Regras (lista completa no [AGENTS.md](../AGENTS.md))

- A IA não inventa requisitos. Se algo não estiver claro, perguntamos ao cliente.
- Uma story só está feita quando **cada critério de aceitação tem um teste que passa**.
- Uma story por branch e por membro. Fazer pull antes de começar.
- **Registar cada uso de IA** em [ai-usage-log.md](ai-usage-log.md): o relatório tem de o indicar, com os prompts.
- Cada um tem de saber **explicar sem apontamentos** o que a IA fez por si.
