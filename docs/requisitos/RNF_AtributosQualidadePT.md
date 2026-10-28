# RNF – Atributos de qualidade, interfaces e restrições

**Atualizado em:** 21/10/2026 · [Convenções e fontes](README.md)

Os requisitos não funcionais têm de ser **específicos e verificáveis** (template do SRS). Os valores numéricos marcados "Hip." são propostas do grupo para discutir e validar. Não foram ditos por nenhum stakeholder.

## 1. Usabilidade
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| RNF-USA-01 | O sistema deve ser uma aplicação web adaptável ao ecrã (telemóvel e computador), sem obrigar a instalar nada, e poder ser instalada no ecrã inicial do telemóvel como PWA (sem passar pelas lojas de aplicações). | M | E-3 (hoje usa-se WhatsApp, email e notas no telemóvel); decisão do grupo de 21/10 (evita os custos e a publicação na App Store e na Play Store) | Proposto |
| RNF-USA-02 | Um coprodutor que já usou o sistema deve conseguir subscrever um ciclo completo em **10 minutos** ou menos, sem ajuda. | S | Hip. | A validar |
| RNF-USA-03 | As tarefas recorrentes do produtor (publicar a composição do cabaz, registar uma falta, confirmar um pagamento) devem demorar **2 minutos** ou menos cada. | S | E-2 §3 ("só produzir"), CA ("pouco esforço para os agricultores"), Hip. (valor) | A validar |
| RNF-USA-04 | O sistema deve cumprir as WCAG 2.1, nível AA. | S | Hip. | A validar |
| RNF-USA-05 | O coprodutor deve conseguir ver o que vai levantar na próxima entrega e quanto deve no máximo a **2 cliques** da página inicial. | S | E-3 §1, §10, Hip. (valor) | A validar |
| RNF-USA-06 | O sistema deve mostrar ao utilizador, de forma simples, como instalar a aplicação no ecrã inicial do telemóvel (instruções para Android e iPhone) e como ativar as notificações. | S | Decisão do grupo de 21/10 (RNF-USA-01, RNF-INT-05) | Proposto |

## 2. Segurança e proteção de dados
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| RNF-SEG-01 | O acesso deve exigir autenticação. Cada papel só acede aos dados de que precisa: o produtor só vê os coprodutores que lhe compram. | M | D-B §3.1, RGPD | Proposto |
| RNF-SEG-02 | Todas as comunicações devem ser cifradas (HTTPS/TLS). | M | RGPD art. 32.º | Proposto |
| RNF-SEG-03 | As alergias e intolerâncias são dados de saúde: só devem ser guardadas com consentimento explícito e só ficar visíveis para os produtores que entregam a esse coprodutor. | M | E-2 §4, RGPD art. 9.º | A validar |
| RNF-SEG-04 | O sistema deve registar quem alterou encomendas, entregas e pagamentos, e quando (registo de auditoria). | S | Hip. (C3: valores em disputa) | Proposto |
| RNF-SEG-05 | O sistema deve permitir cumprir o RGPD: produtores como responsáveis conjuntos, FAIR como subcontratante, registo das atividades de tratamento e notificação de violações em 72 h. | M | D-B, RGPD arts. 26.º, 28.º, 30.º, 33.º | Proposto |
| RNF-SEG-06 | Os dados pessoais devem ser apagados ou anonimizados quando termina o prazo de conservação de cada finalidade, salvo obrigação legal (ex.: fiscal). | S | D-B §3.1, RGPD art. 5.º | Proposto |
| RNF-SEG-07 | As etiquetas e folhas impressas não devem mostrar alergias, intolerâncias nem outros dados de saúde, só o nome e as substituições feitas. | M | RNF-SEG-03, Brainstorm 14/10 | Proposto |

## 3. Desempenho e capacidade
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| RNF-DES-01 | O sistema deve suportar AMAP com até **200 coprodutores** e várias AMAP na mesma instalação. | M | E-2 §3, §6 (até ~50 por AMAP; uma CSA com ~200), D-D (34 em 2023) | Proposto |
| RNF-DES-02 | As páginas principais devem abrir em **2 segundos** ou menos em 95% dos pedidos, mesmo no último dia de subscrição. | S | Hip. | A validar |

## 4. Disponibilidade e fiabilidade
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| RNF-DIS-01 | O sistema deve estar disponível **99,5%** do tempo e não deve ter manutenções planeadas durante as distribuições nem nos últimos dias de subscrição. | S | Hip. (D-A: distribuição à terça 17h30–19h30) | A validar |
| RNF-DIS-02 | Deve ser feita uma cópia de segurança diária, e deve ser possível recuperar os dados com uma perda máxima de 24 horas. | S | Hip. | A validar |
| RNF-DIS-03 | A confirmação de levantamento deve funcionar com rede fraca no local de entrega: fica guardada no telemóvel e é enviada quando houver ligação. | C | Brainstorm 14/10, Hip. | Ideia (avaliar na implementação) |

## 5. Internacionalização e localização
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| RNF-I18N-01 | A interface deve estar em **português europeu** e preparada para outras línguas (ex.: inglês, francês). | M | CA (nenhuma solução analisada tem interface em português) | Proposto |
| RNF-I18N-02 | Valores em euros com IVA incluído, datas no formato dd/mm/aaaa e fuso horário de Portugal. | M | D-A | Proposto |

## 6. Interfaces externas
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| RNF-INT-01 | O sistema deve enviar notificações por email. | M | D-A, D-C §4.6 | Proposto |
| RNF-INT-02 | O sistema deve exportar dados para folha de cálculo (CSV/XLSX). | S | E-2 §2 (Excel atual) | Proposto |
| RNF-INT-03 | O sistema deve poder enviar notificações por SMS ou WhatsApp. | C | E-3 §12, Hip. | A validar |
| RNF-INT-04 | O sistema deve poder integrar-se com um prestador de pagamentos licenciado (ex.: MB Way), capaz de dividir um pagamento por vários produtores. | S | Proposta do grupo (a partir de E-5), CA, PSD2, E-1 | Proposto |
| RNF-INT-05 | O sistema deve enviar notificações push para o telemóvel (através da PWA), além do email, quando o utilizador as ativar. | S | E-2 §2, E-3 §9 (lembretes de entrega), decisão do grupo de 21/10 | Proposto |

## 7. Restrições de conceção e de negócio
| ID | Restrição | Prior. | Fonte | Estado |
|---|---|---|---|---|
| RNF-RES-01 | O sistema não deve emitir faturas: a faturação está fora do âmbito. Cada produtor fatura no seu programa. | M | E-6; Resultados técnica 2 §5, C4 | Validado |
| RNF-RES-02 | O sistema não deve guardar diretamente o dinheiro dos coprodutores (PSD2). A cobrança é centralizada: o coprodutor faz um só pagamento, dividido pelos produtores através de um prestador de pagamentos licenciado (opção do grupo em 21/10). | M | Proposta do grupo (a partir de E-5), PSD2, E-1, E-2 §13 | Proposto |
| RNF-RES-03 | A solução deve respeitar a Carta de Princípios das AMAP: não pode atuar como intermediário comercial entre produtor e coprodutor. | M | D-E (Carta de Princípios), D-C §4.1, E-2, E-3 §5, CA; interpretação do grupo (técnica 2, resultados §5) | A validar (C6) |
| RNF-RES-04 | A FAIR cobra uma fee mínima por produtor mais uma percentagem sobre o volume de pagamentos que passa pela plataforma; os valores são definidos pela FAIR. | S | Proposta do grupo (a partir de E-1 §4, E-5); CA e D-E preferiam sem comissão | Proposto |
| RNF-RES-05 | A solução deve ser uma plataforma partilhada por várias AMAP (multi-AMAP), com os dados de cada AMAP separados. | M | CA ("instância comum para as AMAP portuguesas"), E-2 §1 | Proposto |
| RNF-RES-06 | A solução deve ser mantida pela FAIR ao longo do tempo (correções, atualizações de segurança e evolução). | S | E-1 (softwares de amadores deixam de ser mantidos) | Proposto |
| RNF-RES-07 | As diferenças entre AMAP e entre produtores da mesma AMAP (duração do ciclo, datas e modo de entrega, prazos de alteração, momento do pagamento, regras de ausência) devem ser tratadas por configuração, sem desenvolvimento específico para cada AMAP ou produtor. | M | Princípio 1 do brainstorm de 14/10, E-2 §1, §11, E-3 §2–§4, §8 | Proposto |
