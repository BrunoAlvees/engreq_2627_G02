# RNF – Atributos de qualidade, interfaces e restrições

**Atualizado em:** 28/10/2026 · [Convenções e fontes](README.md)

Os requisitos não funcionais têm de ser **específicos e verificáveis** (template do SRS). Os valores numéricos marcados "Hip." são propostas do grupo para discutir e validar. Não foram ditos por nenhum stakeholder.

## 1. Usabilidade
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| NFR-01 | O sistema deve ser uma aplicação web adaptável ao ecrã (telemóvel e computador), sem obrigar a instalar nada, e poder ser instalada no ecrã inicial do telemóvel como PWA, sem passar pelas lojas de aplicações. O sistema deve explicar de forma simples como instalar a aplicação (Android e iPhone) e ativar as notificações. | M | E-3 (hoje usa-se WhatsApp, email e notas no telemóvel); decisão do grupo de 21/10 (evita os custos e a publicação na App Store e na Play Store) | Proposto |
| NFR-02 | As tarefas mais frequentes devem ser rápidas: um coprodutor que já usou o sistema subscreve um ciclo completo em **10 minutos** ou menos, sem ajuda; cada tarefa recorrente do produtor (publicar a composição do cabaz, registar uma falta, confirmar um pagamento) demora **2 minutos** ou menos; o coprodutor vê o que vai levantar e quanto deve a **2 cliques** da página inicial. | S | E-2 §3 ("só produzir"), E-3 §1, §10, CA ("pouco esforço para os agricultores"), Hip. (valores) | A validar |
| NFR-03 | O sistema deve cumprir as WCAG 2.1, nível AA. | S | Hip. | A validar |

## 2. Segurança e proteção de dados
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| NFR-04 | O acesso deve exigir autenticação. Cada papel só acede aos dados de que precisa: o produtor só vê os coprodutores que lhe compram. | M | D-B §3.1, RGPD | Proposto |
| NFR-05 | Todas as comunicações devem ser cifradas (HTTPS/TLS). | M | RGPD art. 32.º | Proposto |
| NFR-06 | As alergias e intolerâncias são dados de saúde: só devem ser guardadas com consentimento explícito, só ficar visíveis para os produtores que entregam a esse coprodutor e nunca aparecer em etiquetas ou folhas impressas (aí só o nome e as substituições feitas). | M | E-2 §4, RGPD art. 9.º, Brainstorm 14/10 | A validar |
| NFR-07 | O sistema deve registar quem alterou encomendas, entregas e pagamentos, e quando (registo de auditoria). | S | Hip. (C3: valores em disputa) | Proposto |
| NFR-08 | O sistema deve permitir cumprir o RGPD: produtores como responsáveis conjuntos, FAIR como subcontratante, registo das atividades de tratamento, notificação de violações em 72 h e eliminação ou anonimização dos dados pessoais quando termina o prazo de conservação de cada finalidade, salvo obrigação legal (ex.: fiscal). | M | D-B, D-B §3.1, RGPD arts. 5.º, 26.º, 28.º, 30.º, 33.º | Proposto |

## 3. Desempenho e capacidade
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| NFR-09 | O sistema deve suportar AMAP com até **200 coprodutores** e várias AMAP na mesma instalação. | M | E-2 §3, §6 (até ~50 por AMAP; uma CSA com ~200), D-D (34 em 2023) | Proposto |
| NFR-10 | As páginas principais devem abrir em **2 segundos** ou menos em 95% dos pedidos, mesmo no último dia de subscrição. | S | Hip. | A validar |

## 4. Disponibilidade e fiabilidade
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| NFR-11 | O sistema deve estar disponível durante os horários de distribuição de cada AMAP e nos últimos 3 dias de cada período de subscrição; as manutenções planeadas fazem-se fora desses períodos. Deve ser feita uma cópia de segurança diária, com perda máxima de 24 horas de dados. | S | D-A (distribuição à terça 17h30–19h30, prazos de subscrição), E-3 §9 (confirmação de levantamento), decisão do grupo de 28/10 (requisito ligado ao uso real, em vez de uma percentagem genérica) | Proposto |
| NFR-12 | A confirmação de levantamento deve funcionar com rede fraca no local de entrega: fica guardada no telemóvel e é enviada quando houver ligação. | C | Brainstorm 14/10, Hip. | Ideia (avaliar na implementação) |

## 5. Internacionalização e localização
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| NFR-13 | A interface deve estar em **português europeu** e preparada para outras línguas (ex.: inglês, francês). | M | CA (nenhuma solução analisada tem interface em português) | Proposto |
| NFR-14 | Valores em euros com IVA incluído, datas no formato dd/mm/aaaa e fuso horário de Portugal. | M | D-A | Proposto |

## 6. Interfaces externas
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| NFR-15 | O sistema deve enviar notificações por **email** e, quando o utilizador as ativar, por **push** no telemóvel (através da PWA). *(Could)* Pode também enviar por **WhatsApp** (ou SMS) através da API oficial do WhatsApp Business, com mensagens individuais e não através de um bot num grupo. | M | D-A, D-C §4.6, E-2 §2, E-3 §9, §12, decisões do grupo de 21/10 e 28/10 (os bots não oficiais violam as regras do WhatsApp) | Proposto |
| NFR-16 | O sistema deve exportar dados para folha de cálculo (CSV/XLSX). | S | E-2 §2 (Excel atual) | Proposto |
| NFR-17 | O sistema deve poder integrar-se com um prestador de pagamentos licenciado (ex.: MB Way), capaz de dividir um pagamento por vários produtores. | S | Proposta do grupo (a partir de E-5), CA, PSD2, E-1 | Proposto |

## 7. Restrições de conceção e de negócio
| ID | Restrição | Prior. | Fonte | Estado |
|---|---|---|---|---|
| NFR-18 | O sistema não deve emitir faturas: a faturação está fora do âmbito. Cada produtor fatura no seu programa. | M | E-6; Resultados técnica 2 §5, C4 | Validado |
| NFR-19 | O sistema não deve guardar diretamente o dinheiro dos coprodutores (PSD2). A cobrança é centralizada: o coprodutor faz um só pagamento, dividido pelos produtores através de um prestador de pagamentos licenciado (opção do grupo em 21/10). | M | Proposta do grupo (a partir de E-5), PSD2, E-1, E-2 §13 | Proposto |
| NFR-20 | A solução deve respeitar a Carta de Princípios das AMAP: não pode atuar como intermediário comercial entre produtor e coprodutor. | M | D-E (Carta de Princípios), D-C §4.1, E-2, E-3 §5, CA; interpretação do grupo (técnica 2, resultados §5) | A validar (C6) |
| NFR-21 | A FAIR cobra uma fee mínima por produtor mais uma percentagem sobre o volume de pagamentos que passa pela plataforma; os valores são definidos pela FAIR. | S | Proposta do grupo (a partir de E-1 §4, E-5); CA e D-E preferiam sem comissão | Proposto |
| NFR-22 | A solução deve ser uma plataforma partilhada por várias AMAP (multi-AMAP), com os dados de cada AMAP separados. | M | CA ("instância comum para as AMAP portuguesas"), E-2 §1 | Proposto |
| NFR-23 | A solução deve ser mantida pela FAIR ao longo do tempo (correções, atualizações de segurança e evolução). | S | E-1 (softwares de amadores deixam de ser mantidos) | Proposto |
| NFR-24 | As diferenças entre AMAP e entre produtores da mesma AMAP (duração do ciclo, datas e modo de entrega, prazos de alteração, momento do pagamento, regras de ausência) devem ser tratadas por configuração, sem desenvolvimento específico para cada AMAP ou produtor. | M | Princípio 1 do brainstorm de 14/10, E-2 §1, §11, E-3 §2–§4, §8 | Proposto |

## Correspondência com a versão anterior
Na revisão de 28/10, os 32 requisitos anteriores foram reduzidos a 22, juntando os que medem a mesma coisa (indicação do professor de reduzir o detalhe).

| Novo | Junta os anteriores |
|---|---|
| NFR-01 | USA-01, USA-06 |
| NFR-02 | USA-02, USA-03, USA-05 |
| NFR-03 | USA-04 |
| NFR-06 | SEG-03, SEG-07 |
| NFR-08 | SEG-05, SEG-06 |
| NFR-11 | DIS-01 (99,5% substituído pelos períodos de uso real), DIS-02 |
| NFR-12 | DIS-03 |
| NFR-15 | INT-01, INT-03, INT-05 |
| NFR-17 | INT-04 |
| *(restantes)* | sem alteração |
