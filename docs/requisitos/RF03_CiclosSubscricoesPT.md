# RF03 – Ciclos e subscrições

**Atualizado em:** 21/10/2026 · [Convenções e fontes](README.md)

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
| RF-SUB-01 | O sistema deve permitir criar um ciclo com duração configurável (ex.: 3, 6 ou 12 meses), data de abertura e data-limite de subscrição. | Gestão | M | E-1 §3.5, E-2 §7, D-A, DOC-01, N13 | Proposto |
| RF-SUB-02 | O sistema deve permitir que a duração do compromisso do coprodutor seja diferente da duração do ciclo de ofertas. | Gestão | C | E-1 §3.5 | A validar (PA-02) |
| RF-SUB-03 | O sistema deve permitir ao coprodutor subscrever, num só passo, produtos de vários produtores da mesma AMAP. | Coprodutor | M | D-A, E-3 §1 | Proposto |
| RF-SUB-04 | O sistema deve permitir escolher, em cada subscrição, a quantidade, a variante e, quando aplicável, as datas de entrega (ex.: carne). | Coprodutor | M | D-A, N17 | Proposto |
| RF-SUB-05 | O sistema deve oferecer opções estruturadas para os pedidos que hoje vão para texto livre (ex.: opções da carne, avulso em vez de cabaz, variar o pão ao longo do ciclo). | Coprodutor | S | D-A, DOC-14, N17 | Proposto |
| RF-SUB-06 | O sistema deve permitir ao coprodutor registar exclusões (alergias, intolerâncias, gostos) e ao produtor indicar a substituição feita. | Coprodutor, Produtor | M | E-2 §4, E-3 §14, N2 | Proposto |
| RF-SUB-07 | O sistema deve aceitar pedidos após a data-limite apenas como pendentes, até a gestão os aprovar ou recusar. | Gestão | S | D-A | Proposto |
| RF-SUB-08 | O sistema deve permitir a cada produtor definir se o coprodutor pode alterar a encomenda e, se sim, até quanto tempo antes de cada entrega (ex.: pão até domingo para a entrega de terça). | Produtor | S | E-3 §3, Brainstorm 14/10 | Proposto |
| RF-SUB-09 | O sistema deve enviar ao coprodutor a confirmação da subscrição, com os produtos, as datas e os valores por produtor. | Sistema | M | D-C §4.2, E-3 §1, DOC-17 | Proposto |
| RF-SUB-10 | O sistema deve permitir ao coprodutor consultar, a qualquer momento, as subscrições em curso e o histórico. | Coprodutor | M | E-3 §1, N6, DOC-17 | Proposto |
| RF-SUB-11 | O sistema deve pedir aos coprodutores, com antecedência configurável (ex.: 3 meses antes do novo ciclo), que indiquem se renovam, partindo da encomenda anterior. Cada AMAP escolhe o modo: **(A) intenção**, só indicativa, para o produtor planear; ou **(B) confirmação obrigatória** até uma data, perdendo o lugar para a lista de espera quem não confirmar. | Coprodutor, Gestão | S | E-2 §7, N12, DV-11, C8, Brainstorm 14/10 | A validar (DV-12) |
| RF-SUB-12 | *(Rejeitado no brainstorm de 14/10: os novos membros já têm as entregas experimentais, RF-MEM-03.)* | — | — | — | Rejeitado |
| RF-SUB-13 | O sistema deve permitir ao produtor pedir a confirmação ou alteração de uma encomenda antes de uma entrega futura (ex.: azeite de dezembro igual ao de setembro). | Produtor | C | D-A, DOC-13, N18 | Proposto |
| RF-SUB-14 | O sistema deve mostrar ao produtor o total encomendado por produto, variante, data de entrega e AMAP, para planear a produção e a colheita. | Produtor | M | E-2 §2, §13, E-1 §3.5 | Proposto |
| RF-SUB-15 | O sistema deve permitir ao produtor consultar as preferências e exclusões agregadas para planear a produção do ciclo seguinte. | Produtor | C | E-1 (aula 1) | Proposto |
| RF-SUB-16 | O sistema deve permitir ao coprodutor alterar a sua encomenda durante o ciclo, dentro das regras definidas por cada produtor (RF-SUB-08). | Coprodutor | S | E-3 §3, Brainstorm 14/10 | Proposto |
