# Part 2 of the project: recommendations

**Author:** Bruno Alves · **Date:** 28/10/2026 · **Status:** proposal for the group to discuss

## Context
In part 2, the lecturer will give us a **form with very abstract requirements**, from which we will have to **implement** the solution. Since we will use **AI agents to write code**, we should prepare how we work now.

## Recommendation: install the BMAD Method in the part 2 repository
The [BMAD Method](https://github.com/bmad-code-org/BMAD-METHOD) is an agile development method with AI agents (analyst, PM, architect, developer, QA). It helps go from abstract requirements to code in an organised way:
- the **analyst** and **PM** agents detail the abstract requirements from the form (brief, PRD);
- the **architect** defines the architecture;
- requirements are split into **epics and user stories**;
- the **developer** implements one story at a time, and **QA** reviews it.

This way the agents work with shared context and rules, instead of each of us asking our own assistant for "loose" code.

## Precautions
- **Confirm with the lecturer** that AI agents are allowed in part 2 and how their use must be declared.
- **Decide as a group** before installing: everyone needs to know the method to defend it.
- Use **a separate repository for the code** of part 2 (or a separate folder), so it does not mix with the part 1 documentation.
- Pin the BMAD **version** and add personal configuration files to `.gitignore` (`_bmad/custom/config.user.toml`).
- Write the **project rules** for the agents in the repository (`AGENTS.md`): structure, conventions, what they must not change.
- Always review generated code: responsibility stays with the group.

## Reusing part 1
The requirements from this part (`docs/requisitos/`, with acceptance criteria) and the backlog (SRS section 11) can be the starting point for BMAD: the acceptance criteria become the tests for the user stories.
