# Parte 2 do trabalho: recomendações

**Autor:** Bruno Alves · **Data:** 28/10/2026 · **Estado:** proposta para o grupo discutir

## Contexto
Na parte 2, o professor vai entregar um **formulário com requisitos muito abstratos**, a partir do qual teremos de **implementar** a solução. Como vamos usar **agentes de IA para escrever código**, convém preparar já a forma de trabalhar.

## Recomendação: instalar o BMAD Method no repositório da parte 2
O [BMAD Method](https://github.com/bmad-code-org/BMAD-METHOD) é um método de desenvolvimento ágil com agentes de IA (analista, PM, arquiteto, developer, QA). Ajuda a passar de requisitos abstratos para código de forma organizada:
- o agente **analista** e o **PM** detalham os requisitos abstratos do formulário (brief, PRD);
- o **arquiteto** define a arquitetura;
- os requisitos são partidos em **épicos e user stories**;
- o **developer** implementa uma story de cada vez, e o **QA** revê.

Assim os agentes trabalham com contexto e regras comuns, em vez de cada um pedir código "solto" ao seu assistente.

## Cuidados
- **Confirmar com o professor** que o uso de agentes de IA é permitido na parte 2 e como deve ser declarado.
- **Decidir em grupo** antes de instalar: todos têm de conhecer o método para o defenderem.
- Usar **um repositório próprio para o código** da parte 2 (ou uma pasta separada), para não misturar com a documentação da parte 1.
- Fixar a **versão** do BMAD e pôr no `.gitignore` os ficheiros de configuração pessoal (`_bmad/custom/config.user.toml`).
- Escrever no repositório as **regras do projeto** para os agentes (`AGENTS.md`): estrutura, convenções, o que não podem alterar.
- Rever sempre o código gerado: a responsabilidade continua a ser do grupo.

## Aproveitar a parte 1
Os requisitos desta parte (`docs/requisitos/`, com critérios de aceitação) e o backlog (secção 11 do SRS) podem servir de base ao BMAD: os critérios de aceitação passam a ser os testes das user stories.
