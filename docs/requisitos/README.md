# Requisitos / Requirements

**Atualizado em / Updated on:** 21/10/2026

**PT:** Lista consolidada dos requisitos da FAIR-AMAP, organizada por **funcionalidade do sistema** (as "System features" do template do SRS). Junta os requisitos candidatos das sessões com stakeholders e das quatro técnicas de elicitação. Cada requisito indica a sua **fonte**, para se poder justificar na defesa. Esta é uma **primeira versão para discussão no grupo**: as prioridades são uma proposta inicial e nenhum requisito foi ainda validado pelo cliente.

**EN:** Consolidated list of FAIR-AMAP requirements, organised by **system feature** (the "System features" of the SRS template). It brings together the candidate requirements from the stakeholder sessions and the four elicitation techniques. Each requirement states its **source** so it can be justified in the presentation. This is a **first version for group discussion**: priorities are an initial proposal and no requirement has been validated by the client yet.

## Princípios orientadores / Guiding principles
Definidos no brainstorm de 14/10 / Defined in the 14/10 brainstorm.

1. **PT:** **Cada AMAP tem as suas regras.** O sistema é configurável por AMAP e por produtor e não impõe um modelo único. **EN:** **Each AMAP has its own rules.** The system is configurable per AMAP and per producer and does not impose a single model.
2. **PT:** **Uma AMAP é feita de pessoas.** A prioridade é o contacto direto entre produtores e coprodutores. A aplicação **simplifica e automatiza** o processo, mas não substitui essa relação: os contactos ficam sempre visíveis. **EN:** **An AMAP is made of people.** The priority is direct contact between producers and co-producers. The app **simplifies and automates** the process but does not replace that relationship: contact details are always visible.
3. **PT:** **As entregas de uma AMAP não são semanais.** Quem quer receber todas as semanas subscreve duas AMAP (RF-MEM-07). **EN:** **AMAP deliveries are not weekly.** Those who want deliveries every week subscribe to two AMAPs (RF-MEM-07).

## Ficheiros / Files

| # | Funcionalidade / Feature | Prefixo / Prefix | Ficheiros / Files |
|---|---|---|---|
| RF01 | Gestão da AMAP e dos membros / AMAP and member management | `RF-MEM` | [PT](RF01_GestaoAMAPMembrosPT.md) · [EN](RF01_GestaoAMAPMembrosEN.md) |
| RF02 | Catálogo e ofertas / Catalogue and offers | `RF-CAT` | [PT](RF02_CatalogoOfertasPT.md) · [EN](RF02_CatalogoOfertasEN.md) |
| RF03 | Ciclos e subscrições / Cycles and subscriptions | `RF-SUB` | [PT](RF03_CiclosSubscricoesPT.md) · [EN](RF03_CiclosSubscricoesEN.md) |
| RF04 | Calendário e entregas / Calendar and deliveries | `RF-ENT` | [PT](RF04_CalendarioEntregasPT.md) · [EN](RF04_CalendarioEntregasEN.md) |
| RF05 | Pagamentos e faturação / Payments and invoicing | `RF-PAG` | [PT](RF05_PagamentosFaturacaoPT.md) · [EN](RF05_PagamentosFaturacaoEN.md) |
| RF06 | Comunicação e notificações / Communication and notifications | `RF-COM` | [PT](RF06_ComunicacaoPT.md) · [EN](RF06_ComunicacaoEN.md) |
| RF07 | Comunidade e organização / Community and organisation | `RF-CMD` | [PT](RF07_ComunidadePT.md) · [EN](RF07_ComunidadeEN.md) |
| RF08 | Relatórios e indicadores / Reports and indicators | `RF-REL` | [PT](RF08_RelatoriosIndicadoresPT.md) · [EN](RF08_RelatoriosIndicadoresEN.md) |
| RNF | Atributos de qualidade, interfaces e restrições / Quality attributes, interfaces and constraints | `RNF-*` | [PT](RNF_AtributosQualidadePT.md) · [EN](RNF_AtributosQualidadeEN.md) |
| — | Diagramas / Diagrams | — | [diagramas/](diagramas/README.md) |
| — | Perguntas em aberto / Open questions | `PA-nn` | [PT](PerguntasEmAbertoPT.md) · [EN](PerguntasEmAbertoEN.md) |

## Convenções / Conventions

### Identificadores / Identifiers
- **PT:** `RF-<ÁREA>-<nn>` para requisitos funcionais e `RNF-<TIPO>-<nn>` para não funcionais. **Um ID nunca é reutilizado** depois de publicado: se um requisito for rejeitado, fica na tabela com o estado "Rejeitado". **Exceção:** na revisão de 28/10 os requisitos foram agrupados para reduzir o detalhe e os IDs foram renumerados; cada ficheiro tem uma tabela de correspondência com os IDs anteriores.
- **EN:** `RF-<AREA>-<nn>` for functional requirements and `RNF-<TYPE>-<nn>` for non-functional ones. **An ID is never reused** once published: if a requirement is rejected, it stays in the table with status "Rejected". **Exception:** in the 28/10 review, requirements were grouped to reduce detail and IDs were renumbered; each file has a mapping table to the previous IDs.

### Formato / Format
- **PT:** "O sistema deve…" (um requisito por linha, verificável). Colunas: **ID · Requisito · Ator · Prioridade · Fonte · Estado**.
- **EN:** "The system shall…" (one verifiable requirement per row). Columns: **ID · Requirement · Actor · Priority · Source · Status**.

### Prioridade (MoSCoW) / Priority (MoSCoW)
| | PT | EN |
|---|---|---|
| **M** | Must: obrigatório na 1.ª versão | Must: required in the first version |
| **S** | Should: importante, mas a solução funciona sem ele | Should: important, but the solution works without it |
| **C** | Could: desejável, se houver tempo | Could: desirable if time allows |
| **W** | Won't (desta vez): fora do âmbito desta versão | Won't (this time): out of scope for this version |

### Estado / Status
| PT | EN | Significado / Meaning |
|---|---|---|
| Proposto | Proposed | Tem fonte, ainda não validado com o cliente / Has a source, not yet validated with the client |
| A validar | To validate | Depende de uma dúvida em aberto (ver coluna Fonte) / Depends on an open question (see Source column) |
| Ideia | Idea | Proposta do grupo a avaliar na implementação / Group proposal to assess during implementation |
| Validado | Validated | Confirmado pelo cliente ou stakeholder / Confirmed by the client or stakeholder |
| Rejeitado | Rejected | Fora do âmbito ou descartado / Out of scope or discarded |

### Fontes / Sources
| Código / Code | Fonte / Source |
|---|---|
| E-1 | Sessão de 23/09 (professor como cliente FAIR) — [resumo](../interviews/23-09-2026/LevantamentoInfo23_09_v2PT.md) |
| E-2 | Sessão de 29/09 (BioGoods, produtora) — [resumo](../interviews/29-09-2026/LevantamentoInfo29_09PT.md), [complemento](../interviews/29-09-2026/Complemento29_09PT.md) |
| E-3 | Sessão de 06/10 (coprodutora da AMAP UPTEC Baixa) — [resumo](../interviews/06-10-2026/LevantamentoInfo06_10PT.md), [complemento](../interviews/06-10-2026/Complemento06_10PT.md) |
| E-4 | Aula de 07/10 (professor, processo de adesão; a confirmar se como cliente) |
| E-5 | Aula da semana de 12/10 (professor, em conversa com outro grupo sobre o modelo de negócio; ouvido pelo Bruno, não gravado): o dinheiro das subscrições é recolhido num só ponto e distribuído pelos produtores, com um resumo de quem pagou e quanto / Class in the week of 12/10 (lecturer, talking to another group about the business model; overheard by Bruno, not recorded): subscription money is collected in one place and distributed among producers, with a summary of who paid and how much |
| E-6 | Aula da semana de 19/10 (professor como cliente FAIR, em resposta a uma pergunta do Bruno sobre como os produtores passam as faturas): a faturação está fora do âmbito / Class in the week of 19/10 (lecturer as FAIR client, answering Bruno's question on how producers issue invoices): invoicing is out of scope |
| D-A … D-F | Documentos da AMAP Porto e da rede — [análise](../doc_AMAP/AnaliseDocumentosAMAPPT.md), [resultados](../tecnicas/ResultadosAnaliseDocumentalPT.md) |
| DOC-nn | Requisitos candidatos da análise documental (técnica 2) |
| N-nn | Necessidades da [análise de diferenciação](../tecnicas/AnaliseDiferenciacaoPT.md) (técnica 4) |
| CA | [Análise de concorrência](../tecnicas/CompetitorAnalysis.md) (técnica 1) |
| C-n, DV-nn | Diferenças entre fontes e dúvidas em aberto — [resultados §4.2](../tecnicas/ResultadosAnaliseDocumentalPT.md), [dúvidas](../tecnicas/DuvidasProcessosAtuaisPT.md) |
| Hip. | Hipótese do grupo, sem fonte de stakeholder (validar) / Group hypothesis, no stakeholder source (to validate) |
| Brainstorm dd/mm | Ideia surgida num brainstorm do grupo (ver nota no ficheiro da área) / Idea from a group brainstorm (see note in the area file) |

## Atores / Actors
| PT | EN | Descrição / Description |
|---|---|---|
| Coprodutor | Co-producer | Consumidor que subscreve produtos da AMAP / Consumer who subscribes to AMAP products |
| Produtor | Producer | Agricultor ou transformador que oferece produtos / Farmer or processor who offers products |
| Gestão da AMAP | AMAP management | Pessoa, comissão ou grupos de trabalho que organizam a AMAP / Person, committee or working groups that run the AMAP |
| Interessado | Prospective member | Pessoa que quer aderir a uma AMAP / Person who wants to join an AMAP |
| Administrador FAIR | FAIR administrator | Gere a plataforma e as AMAP clientes / Manages the platform and client AMAPs |
| Sistema | System | Ações automáticas (notificações, cálculos) / Automatic actions (notifications, calculations) |

## Decisões de âmbito em aberto / Open scope decisions
- **C6 – Intermediação / Intermediation:** **PT:** a Carta de Princípios das AMAP exclui intermediários. As regras de faturação (software certificado pela AT) e de pagamentos (PSD2) apontam no mesmo sentido. A proposta é uma ferramenta de organização que **não recebe dinheiro nem emite faturas**. Os requisitos afetados estão marcados "A validar (C6)". **EN:** the AMAP Charter of Principles excludes intermediaries. Invoicing rules (AT-certified software) and payment rules (PSD2) point the same way. The proposal is an organisation tool that **neither handles money nor issues invoices**. Affected requirements are marked "To validate (C6)". **Atualização 21/10 / Update 21/10 (E-5):** **PT:** o professor referiu que, neste tipo de aplicação, o dinheiro das subscrições é recolhido num só ponto e distribuído pelos produtores. Fica em aberto um **modelo B**: cobrança centralizada através de um prestador de pagamentos licenciado, sem o sistema guardar o dinheiro nem emitir faturas (RNF-RES-02, RNF-INT-04, RF-PAG-03, 04). **EN:** the lecturer mentioned that, in this kind of app, subscription money is collected in one place and distributed among producers. A **model B** remains open: centralised collection through a licensed payment provider, without the system holding the money or issuing invoices (RNF-RES-02, RNF-INT-04, RF-PAG-03, 04).
- **Modelo de cobrança da FAIR / FAIR pricing model:** **PT:** fee mínima + volume (E-1) vs. ética das AMAP (CA). **EN:** minimum fee + volume (E-1) vs. AMAP ethics (CA).
- **N19 – Automatização vs. relação pessoal / Automation vs. personal relationship:** **PT:** os stakeholders valorizam a relação pessoal entre produtores e coprodutores (E-3, D-D). A automatização da composição do cabaz (RF-ENT-02) e da confirmação de levantamento (RF-ENT-05, RF-ENT-05) **foi pedida** pelos stakeholders (E-2, E-3) e não está em causa. Falta validar: (1) se as exclusões e preferências, hoje tratadas de forma informal porque a produtora conhece cada coprodutor (E-3), devem passar a ser registadas no sistema (RF-SUB-03) ou continuar a ser combinadas diretamente; (2) como evitar que a AMAP fique mais impessoal, já que os sacos com nome tornaram a distribuição viável mas "desumanizaram um bocadinho" a AMAP (E-3), e o RF-ENT-06 gera as etiquetas desses sacos; (3) se preferem manter o WhatsApp para a comunicação informal e usar o sistema só para a gestão. **EN:** stakeholders value the personal relationship between producers and co-producers (E-3, D-D). Automating the basket contents (RF-ENT-02) and collection confirmation (RF-ENT-05, RF-ENT-05) **was requested** by the stakeholders (E-2, E-3) and is not in question. Still to validate: (1) whether exclusions and preferences, currently handled informally because the producer knows each co-producer (E-3), should be recorded in the system (RF-SUB-03) or keep being agreed directly; (2) how to avoid making the AMAP more impersonal, since named bags made distribution viable but made the AMAP "a little dehumanised" (E-3), and RF-ENT-06 generates the labels for those bags; (3) whether they would rather keep WhatsApp for informal communication and use the system only for management.

## Como passar para o SRS / Moving to the SRS
| Pasta / Folder | Secção do template / Template section |
|---|---|
| `RF01`…`RF08` | 3. System features (uma feature por ficheiro: Description, Stimulus/Response, Functional requirements) |
| `diagramas/ModeloDominio*` | 4. Data requirements (logical data model) · 5. Domain model |
| `diagramas/DiagramaContexto*` | 2.1 Product perspective |
| `RNF` §Interfaces | 6. External interface requirements |
| `RNF` §Qualidade | 7. Quality attributes |
| `RNF` §i18n | 8. Internationalization and localization |
| `RNF` §Restrições | 2.4 Design and implementation constraints · 9. Other requirements |
| *(a fazer / to do)* | 11. Product backlog: user stories + horas estimadas / estimated hours |

## Como contribuir / How to contribute
- **PT:** acrescentar requisitos no fim da tabela da área certa, com o próximo número livre, e atualizar **as duas versões (PT e EN)**. Mudar a prioridade ou o estado só depois de o grupo concordar, indicando a fonte (ex.: "Validado – sessão 20/10").
- **EN:** add requirements at the end of the right area's table, with the next free number, and update **both versions (PT and EN)**. Change priority or status only after group agreement, stating the source (e.g. "Validated – session 20/10").
