# RNF – Atributos de qualidade, interfaces e restrições

**Atualizado em:** 21/10/2026 · [Convenções e fontes](README.md)

Os requisitos não funcionais têm de ser **específicos e verificáveis** (template do SRS). Os valores numéricos marcados "Hip." são propostas do grupo para discutir e validar. Não foram ditos por nenhum stakeholder.

## 1. Usabilidade
| ID | Requisito | Prior. | Fonte | Estado |
|---|---|---|---|---|
| RNF-USA-01 | O sistema deve poder ser usado em telemóvel e em computador (interface adaptável ao ecrã), sem instalar nada para as funções do coprodutor. | M | Hip. (E-3: hoje usa-se WhatsApp, email e notas no telemóvel) | A validar |
| RNF-USA-02 | Um coprodutor que já usou o sistema deve conseguir subscrever um ciclo completo em **10 minutos** ou menos, sem ajuda. | S | Hip. | A validar |
| RNF-USA-03 | As tarefas recorrentes do produtor (publicar a composição do cabaz, registar uma falta, confirmar um pagamento) devem demorar **2 minutos** ou menos cada. | S | E-2 §3 ("só produzir"), CA ("pouco esforço para os agricultores"), Hip. (valor) | A validar |
| RNF-USA-04 | O sistema deve cumprir as WCAG 2.1, nível AA. | S | Hip. | A validar |
| RNF-USA-05 | O coprodutor deve conseguir ver o que vai levantar na próxima entrega e quanto deve no máximo a **2 cliques** da página inicial. | S | E-3 §1, §10, Hip. (valor) | A validar |

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
| RNF-INT-04 | O sistema deve poder integrar-se com um prestador de pagamentos licenciado (ex.: MB Way), capaz de dividir um pagamento por vários produtores. | S | CA, PSD2, E-1, E-5 | A validar (C6) |

## 7. Restrições de conceção e de negócio
| ID | Restrição | Prior. | Fonte | Estado |
|---|---|---|---|---|
| RNF-RES-01 | O sistema não deve emitir faturas, porque isso exigiria software certificado pela AT. Cada produtor fatura no seu programa. | M | Resultados técnica 2 §5, C4 | A validar (C6) |
| RNF-RES-02 | O sistema não deve guardar diretamente o dinheiro dos coprodutores (PSD2). Os pagamentos são feitos diretamente a cada produtor (modelo A) ou, em alternativa, recolhidos num só pagamento e divididos pelos produtores através de um prestador de pagamentos licenciado (modelo B). | M | D-C §4.3, PSD2, E-3 (modelo A); E-1, E-2 §13, E-5 (modelo B) | A validar (C6) |
| RNF-RES-03 | A solução deve respeitar a Carta de Princípios das AMAP: não pode atuar como intermediário comercial entre produtor e coprodutor. | M | D-C §4.1, D-E, CA | A validar (C6) |
| RNF-RES-04 | O modelo de cobrança da FAIR não deve depender de uma comissão por cabaz ou por transação. | S | CA, D-E; em conflito com E-1 §4 (fee mínima + volume) e E-5 (cobrança centralizada) | A validar (DV-25) |
| RNF-RES-05 | A solução deve ser uma plataforma partilhada por várias AMAP (multi-AMAP), com os dados de cada AMAP separados. | M | CA ("instância comum para as AMAP portuguesas"), E-2 §1 | Proposto |
| RNF-RES-06 | A solução deve ser mantida pela FAIR ao longo do tempo (correções, atualizações de segurança e evolução). | S | E-1 (softwares de amadores deixam de ser mantidos) | A validar |
| RNF-RES-07 | As diferenças entre AMAP (duração do ciclo, dias de entrega, regras de ausência, regras de cada produtor) devem ser tratadas por configuração, sem desenvolvimento específico para cada AMAP. | M | Princípio 1 do brainstorm de 14/10, E-2 §1, §11 | Proposto |
