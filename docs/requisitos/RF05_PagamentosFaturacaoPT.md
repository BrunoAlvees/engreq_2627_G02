# RF05 – Pagamentos e faturação

**Atualizado em:** 28/10/2026 · [Convenções e fontes](README.md)

## Descrição
Calcula quanto cada coprodutor tem de pagar, cobra esse valor num só pagamento e distribui-o pelos produtores. Hoje, na AMAP Porto, cada produtor recebe diretamente, com meios e momentos próprios (quota mensal dos cabazes, carne depois da pesagem, cogumelos a cada entrega). A BioGoods faz as contas em Excel e envia o valor por mensagem, e o coprodutor não tem forma simples de saber quanto deve.

**Proposta do grupo (21/10):** **cobrança centralizada**. O coprodutor faz **um só pagamento** por período, que é **dividido pelos produtores** através de um **prestador de pagamentos licenciado**. Cada produtor recebe um **resumo** de quem pagou, quanto e a que corresponde. A proposta parte da indicação do professor sobre este tipo de aplicações (E-5), do pedido de concentrar os pagamentos (E-1) e do modelo "possível" descrito pela BioGoods (E-2 §13).

**Limites:** o sistema **não guarda o dinheiro** (o prestador licenciado é que o movimenta, PSD2) e **não emite faturas**: a faturação está **fora do âmbito** (E-6, NFR-18).

## Sequências estímulo/resposta
- Chega o início do período → o sistema calcula o valor de cada coprodutor, discriminado por produtor, e envia-lhe o pedido de pagamento.
- O coprodutor paga (ex.: MB Way, referência Multibanco) → o prestador confirma o pagamento, divide o valor pelos produtores e o sistema regista-o automaticamente.
- O produtor regista o peso real da carne entregue → o valor entra no pagamento seguinte.
- Termina o período → cada produtor recebe o resumo de quem pagou, quanto e a que corresponde.
- Um pagamento fica por fazer depois do prazo → o sistema avisa o coprodutor e a gestão da AMAP.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| FR-30 | O sistema deve permitir configurar os pagamentos de cada AMAP e de cada produtor: meios disponíveis, conta onde cada produtor recebe e momento da cobrança de cada produto. | Gestão, Produtor | M | D-A, D-C §4.3, E-1 §3.9, E-3 §4, CA, DOC-10, N7, proposta do grupo (a partir de E-5) | A validar (C3) |
| FR-31 | O sistema deve calcular o valor a pagar por cada coprodutor em cada período, discriminado por produtor, e enviar-lhe o pedido de pagamento. | Sistema, Coprodutor | M | E-2 §2, D-A, E-3 §4, DOC-09, DOC-17, N6, N8 | Proposto |
| FR-32 | O sistema deve cobrar num só pagamento o valor de um coprodutor a vários produtores, sendo o valor dividido pelos produtores através de um prestador de pagamentos licenciado (o sistema não guarda o dinheiro). | Coprodutor, Sistema | M | Proposta do grupo (a partir de E-5), E-1 §3.9, E-2 §13, PSD2, D-C §4.3, DOC-11 | Proposto |
| FR-33 | O sistema deve permitir acompanhar os pagamentos: estado por coprodutor, atrasos e resumo dos pagamentos recebidos por cada produtor. | Sistema, Gestão, Produtor | M | Proposta do grupo (a partir de E-5), E-2 §2, DOC-09, DV-19, DV-20 | Proposto |
| FR-34 | O sistema deve calcular o valor a cobrar pela FAIR a cada produtor ou AMAP, segundo o modelo de cobrança definido. | Administrador FAIR | C | E-1 §4, E-5, NFR-21 | A validar (DV-25) |

## Critérios de aceitação

**FR-30 – Configurar os pagamentos**
- A gestão da AMAP escolhe os meios de pagamento disponíveis através do prestador (ex.: MB Way, referência Multibanco, cartão).
- Cada produtor associa a conta onde recebe a sua parte.
- Por produtor e por produto, define-se quando cada valor é cobrado: antecipado no ciclo, no início de cada mês ou depois da entrega ou pesagem.

**FR-31 – Calcular e pedir o pagamento**
- O valor é calculado assim: quotas fixas dos cabazes + extras + produtos pesados − faltas compensadas. As quotas dos cabazes são fixas; os extras variam com o que foi entregue (D-A).
- O coprodutor recebe o pedido de pagamento e vê, numa só vista, o valor total, o detalhe por produtor e o histórico de pagamentos.

**FR-32 – Cobrança centralizada**
- O coprodutor faz um só pagamento por período, online, através do prestador licenciado.
- O prestador divide o valor pelos produtores; o sistema não guarda o dinheiro (NFR-19).
- Os pagamentos confirmados pelo prestador ficam registados automaticamente; a gestão pode registar à mão pagamentos feitos fora da plataforma (ex.: numerário).

**FR-33 – Acompanhar os pagamentos**
- A gestão e cada produtor veem o estado dos pagamentos por coprodutor e são avisados dos pagamentos em atraso (a validar DV-20).
- Cada produtor recebe, por período, o resumo dos pagamentos recebidos: quem pagou, quanto, quando e a que subscrição, produtos ou entregas corresponde.

**FR-34 – Valor cobrado pela FAIR**
- O modelo de cobrança é uma fee mínima por produtor mais uma percentagem sobre o volume de pagamentos (NFR-21); os valores são definidos pela FAIR.

## Fora do âmbito desta versão
| Antigo | Requisito | Motivo |
|---|---|---|
| RF-PAG-07 | Registar a fatura que o produtor emitiu no seu programa | Rejeitado: a faturação está fora do âmbito (E-6) |
| RF-PAG-08 | Guardar a taxa e o regime de IVA de cada produto e produtor | Rejeitado: a faturação está fora do âmbito (E-6); os preços com IVA incluído estão no NFR-14 |
| RF-PAG-09 | Gerir a quota anual de cada membro, o fundo comum e o relatório anual de contas | Won't (fora desta versão): só aparece no Guia antigo da AMAP Porto (D-C), nenhum stakeholder a referiu; pode já não existir (DV-22) |
| RF-PAG-12 | Emitir faturas em nome do produtor ou da AMAP | Rejeitado: a faturação está fora do âmbito (E-6) |

## Correspondência com a versão anterior
Na revisão de 28/10, os 13 requisitos ativos foram reduzidos a 5, para reduzir o detalhe (indicação do professor). O detalhe passou para os critérios de aceitação.

| Novo | Junta os anteriores |
|---|---|
| FR-30 | 01, 02 |
| FR-31 | 03, 04 |
| FR-32 | 05, 10, 11 |
| FR-33 | 06, 13 |
| FR-34 | 14 |
| — | 07, 08, 09, 12 (ver "Fora do âmbito desta versão") |
