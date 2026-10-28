# RF03 – Ciclos e subscrições

**Atualizado em:** 28/10/2026 · [Convenções e fontes](README.md)

## Descrição
Organiza o trabalho em ciclos (hoje semestrais na AMAP Porto; trimestrais ou anuais noutras) e permite ao coprodutor subscrever os produtos de cada ciclo, com as suas opções e exclusões. Substitui o formulário Google e a cópia por email que os coprodutores guardam para saber o que encomendaram. Também dá ao produtor a visão das encomendas para planear a produção.

## Sequências estímulo/resposta
- A gestão abre um ciclo → o sistema avisa os membros ativos e aceita subscrições até à data-limite.
- O coprodutor escolhe cabazes, extras, variantes e datas → o sistema mostra o resumo e o valor mensal estimado por produtor e confirma a subscrição.
- Um pedido chega depois da data-limite → fica pendente até a gestão o aprovar.
- Aproxima-se o fim do ciclo → o sistema convida o coprodutor a renovar, com a encomenda anterior pré-preenchida.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-SUB-01 | O sistema deve permitir criar ciclos de subscrição com duração configurável, data de abertura e data-limite de subscrição. | Gestão | M | E-1 §3.5, E-2 §7, D-A, DOC-01, N13 | Proposto |
| RF-SUB-02 | O sistema deve permitir ao coprodutor subscrever, num só passo, produtos de vários produtores da mesma AMAP, com as suas opções, e receber a confirmação. | Coprodutor, Sistema | M | D-A, D-C §4.2, E-3 §1, DOC-14, DOC-17, N17 | Proposto |
| RF-SUB-03 | O sistema deve permitir ao coprodutor registar exclusões (alergias, intolerâncias, gostos) e ao produtor indicar a substituição feita. | Coprodutor, Produtor | M | E-2 §4, E-3 §14, N2 | Proposto |
| RF-SUB-04 | O sistema deve aplicar os prazos de subscrição e as regras de cada produtor para alterar encomendas durante o ciclo. | Coprodutor, Produtor, Gestão | S | D-A, E-3 §3, DOC-13, N18, Brainstorm 14/10 | Proposto |
| RF-SUB-05 | O sistema deve permitir ao coprodutor consultar, a qualquer momento, as subscrições em curso e o histórico. | Coprodutor | M | E-3 §1, N6, DOC-17 | Proposto |
| RF-SUB-06 | O sistema deve perguntar aos coprodutores, com antecedência, se renovam, partindo da encomenda anterior. | Coprodutor, Gestão | S | E-2 §7, N12, DV-11, C8, Brainstorm 14/10 | A validar (DV-12) |
| RF-SUB-07 | O sistema deve dar ao produtor a informação para planear a produção: totais encomendados e preferências agregadas. | Produtor | M | E-1 §3.5, E-1 (aula 1), E-2 §2, §13 | Proposto |

## Critérios de aceitação

**RF-SUB-01 – Ciclos**
- A duração do ciclo é configurável (ex.: 3, 6 ou 12 meses), com data de abertura e data-limite de subscrição.
- *(Could, a validar PA-02)* A duração do compromisso do coprodutor pode ser diferente da duração do ciclo de ofertas.

**RF-SUB-02 – Subscrever**
- Num só passo, o coprodutor subscreve produtos de vários produtores da mesma AMAP.
- Em cada produto escolhe a quantidade, a variante e, quando aplicável, as datas de entrega (ex.: carne).
- Os pedidos que hoje vão para texto livre têm opções estruturadas (ex.: opções da carne, avulso em vez de cabaz, variar o pão ao longo do ciclo).
- O sistema envia a confirmação com os produtos, as datas e os valores por produtor.

**RF-SUB-03 – Exclusões e substituições**
- O coprodutor regista exclusões (alergias, intolerâncias, gostos); as alergias são dados de saúde (RNF-SEG-03).
- O produtor indica a substituição feita.

**RF-SUB-04 – Prazos e alterações**
- Os pedidos depois da data-limite ficam pendentes até a gestão os aprovar ou recusar.
- Cada produtor define se o coprodutor pode alterar a encomenda e até quanto tempo antes de cada entrega (ex.: pão até domingo para a entrega de terça).
- O coprodutor pode alterar a encomenda durante o ciclo, dentro dessas regras.
- *(Could)* O produtor pode pedir a confirmação ou alteração de uma encomenda antes de uma entrega futura (ex.: azeite de dezembro igual ao de setembro).

**RF-SUB-05 – Consultar subscrições**
- O coprodutor vê as subscrições em curso e o histórico a qualquer momento, sem precisar da cópia do formulário recebida por email.

**RF-SUB-06 – Renovação**
- A antecedência é configurável (ex.: 3 meses antes do novo ciclo), porque as culturas são plantadas com antecedência.
- Cada AMAP escolhe o modo: **(A) intenção**, só indicativa, para o produtor planear; ou **(B) confirmação obrigatória** até uma data, perdendo o lugar para a lista de espera quem não confirmar.

**RF-SUB-07 – Planeamento da produção**
- O produtor vê o total encomendado por produto, variante, data de entrega e AMAP, para planear a produção e a colheita.
- *(Could)* O produtor vê as preferências e exclusões agregadas para planear a produção do ciclo seguinte.

## Correspondência com a versão anterior
Na revisão de 28/10, os 15 requisitos ativos foram agrupados em 7, para reduzir o detalhe (indicação do professor). O detalhe passou para os critérios de aceitação.

| Novo | Junta os anteriores |
|---|---|
| RF-SUB-01 | 01, 02 |
| RF-SUB-02 | 03, 04, 05, 09 |
| RF-SUB-03 | 06 |
| RF-SUB-04 | 07, 08, 13, 16 |
| RF-SUB-05 | 10 |
| RF-SUB-06 | 11 |
| RF-SUB-07 | 14, 15 |
| — | 12 (rejeitado no brainstorm de 14/10: os novos membros já têm as entregas experimentais, RF-MEM-03) |
