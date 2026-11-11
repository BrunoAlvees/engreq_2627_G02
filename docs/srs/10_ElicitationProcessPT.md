# 10 Processo e metodologia de elicitação

**Responsável:** Leonor Marinho · **Atualizado em:** 04/11/2026 · **Estado:** rascunho para revisão
**Fontes:** enunciado ([engreq_tp1_2026_27_v2_EN.pdf](../engreq_tp1_2026_27_v2_EN.pdf)), [interviews/](../interviews/), [tecnicas/](../tecnicas/README.md), [requisitos/README.md](../requisitos/README.md), [divisão do trabalho do SRS](../SRSWorkSplitEN.md), histórico do git

## Abordagem

O enunciado pede a metodologia de elicitação apresentada na unidade curricular, sendo todas as técnicas válidas e combináveis. O grupo trabalhou em **cinco passos**, repetidos à medida que chegava nova informação (abordagem iterativa):

| Passo | O que o grupo fez | Resultado |
|---|---|---|
| 1. Compreender o contexto | Ler o enunciado e a primeira sessão com o cliente; identificar o domínio (AMAP/CSA) e o que a FAIR pretende | [Informação conhecida sobre o projeto](../interviews/23-09-2026/LevantamentoInfo23_09_v2PT.md) |
| 2. Preparar | Estudar as fontes existentes antes de reunir com os stakeholders: documentos, concorrentes, mercado, diferenciação. Escrever primeiro perguntas abertas e depois específicas (conselho do docente) | [Técnicas 1 a 4](../tecnicas/README.md), listas de perguntas |
| 3. Elicitar | Sessões com stakeholders (cliente, produtor, coprodutor) e notas das aulas; brainstorms de grupo | [Notas das sessões e complementos](../interviews/) |
| 4. Analisar e especificar | Consolidar o que foi ouvido em requisitos candidatos com uma **fonte** para cada um; atribuir prioridade (MoSCoW); marcar o que não está validado; reduzir e agrupar requisitos | [Requisitos por funcionalidade](../requisitos/README.md) |
| 5. Validar | Levar os requisitos marcados "A validar" e as perguntas em aberto (DV, PA) às sessões seguintes; atualizar os documentos com as respostas | [Perguntas da semana de 02/11](../interviews/10-11-2026/PerguntasEntrevista10_11PT.md) |

## Princípios seguidos

- **Primeiro perguntas abertas, depois específicas.** As primeiras sessões perguntaram como funciona a AMAP no dia a dia, as pessoas envolvidas, os documentos e o que corre mal. As perguntas técnicas vieram depois, com o stakeholder certo (conselho de 23/09).
- **Os documentos dizem o que as pessoas não dizem.** O grupo pediu e analisou documentos reais (formulário de encomenda, termos e condições, guia para novos coprodutores, carta de princípios) e comparou-os com as entrevistas para encontrar diferenças e lacunas ([resultados da técnica 2](../tecnicas/ResultadosAnaliseDocumentalPT.md)).
- **Cada requisito tem uma fonte.** As entrevistas são codificadas de E-1 a E-7, os documentos de D-A a D-F, as técnicas CA, DOC e N. Isto permite ao grupo justificar cada requisito e rastreá-lo até à origem.
- **Nada é "validado" sem o stakeholder.** A informação de um stakeholder é tratada como um ponto de vista. Os pontos incertos ficam como "A validar" ou como perguntas em aberto.
- **Cada AMAP tem as suas regras** e **uma AMAP é feita de pessoas** (princípios orientadores do brainstorm de 14/10): o sistema é configurável e não substitui a relação pessoal.
- **Tudo fica registado no repositório** (planeamento, sessões, tarefas, artefactos), como o enunciado exige, em **português e inglês**.

## Cronologia

| Data | Atividade | Tipo | Evidência |
|---|---|---|---|
| 23/09 | Primeira sessão: FAIR apresentada pelo docente como cliente | Entrevista (E-1) | [Notas](../interviews/23-09-2026/LevantamentoInfo23_09_v2PT.md) |
| 29/09 | Sessão com Sofia Araújo (BioGoods, produtora) | Entrevista (E-2) | [Notas](../interviews/29-09-2026/LevantamentoInfo29_09PT.md), [complemento](../interviews/29-09-2026/Complemento29_09PT.md) |
| 06/10 | Sessão com Luisa Marques (coprodutora, AMAP UPTEC Baixa) e análise do formulário de encomenda | Entrevista (E-3), análise documental | [Notas](../interviews/06-10-2026/LevantamentoInfo06_10PT.md), [complemento](../interviews/06-10-2026/Complemento06_10PT.md) |
| 06/10–14/10 | Técnicas 1 a 4 (concorrentes, análise documental, mercado, diferenciação) | Pré-elicitação | [tecnicas/](../tecnicas/README.md) |
| 07/10 | Aula: como entram novos coprodutores (E-4) | Observação | [README dos requisitos](../requisitos/README.md) |
| 14/10 | Brainstorm de grupo: princípios orientadores | Brainstorm | [README dos requisitos](../requisitos/README.md) |
| semana de 12/10 | Aula: docente sobre o modelo de negócio (E-5, ouvido de passagem, não gravado) | Observação | [README dos requisitos](../requisitos/README.md) |
| 21/10 | Primeira lista consolidada de requisitos; decisão sobre a cobrança centralizada | Análise, brainstorm | [requisitos/](../requisitos/README.md) |
| semana de 19/10 | Aula: a faturação está fora do âmbito (E-6) | Entrevista (cliente) | [README dos requisitos](../requisitos/README.md) |
| 28/10 | Aula: como um produtor entra numa AMAP (E-7); requisitos reduzidos (conselho do docente) | Entrevista (cliente), análise | [requisitos/](../requisitos/README.md) |
| 30/10 | Identificadores alterados para `FR-nn` / `NFR-nn` | Análise | [README dos requisitos](../requisitos/README.md) |
| semana de 02/11 | Sessões de validação com o cliente, o produtor e a gestão da AMAP (30 min) | Entrevista | [Perguntas](../interviews/10-11-2026/PerguntasEntrevista10_11PT.md) *(sessão ainda não realizada à data de escrita)* |

## Papéis no processo

Cada analista de negócio é responsável por uma ou mais técnicas ou secções (ver [10.2](10.2_AppliedTechniquesPT.md) e a [divisão do trabalho do SRS](../SRSWorkSplitEN.md)). Durante as sessões o grupo usou três papéis: **quem pergunta**, **quem toma notas** e **quem controla o tempo** (ver o guião de perguntas da semana de 02/11). As decisões sobre âmbito e prioridades são tomadas **em conjunto** nas reuniões de grupo e registadas no repositório.

## Como os requisitos foram tratados

1. **Recolher** declarações, documentos e observações, com data e fonte.
2. **Separar** o que foi dito pelo stakeholder do que o grupo concluiu. As dúvidas passam a uma lista de perguntas (DV, PA).
3. **Escrever** cada requisito como "O sistema deve…", uma afirmação verificável por linha, com ator, prioridade, fonte e estado.
4. **Priorizar** com MoSCoW. As prioridades são uma proposta até o cliente confirmar.
5. **Rever e reduzir:** os requisitos que mediam o mesmo foram agrupados (de 103 para 42 funcionais e de 32 para 22 não funcionais a 28/10, seguindo o conselho do docente para reduzir o detalhe; os novos requisitos acrescentados depois elevam o total atual para 45 FR e 24 NFR).
6. **Validar** na sessão seguinte e marcar o estado "Validado" só com uma fonte.

## Pontos em aberto

- A sessão da semana de 02/11 ainda não tinha acontecido quando esta secção foi escrita: **atualizar a cronologia** com a sua data e resultados.
- E-4 (07/10) e E-5 (semana de 12/10) não foram gravados e não foram ditos diretamente ao grupo como cliente: confirmar com o docente.
- As datas de E-5 e E-6 são dadas por semana porque o repositório não regista o dia exato.
