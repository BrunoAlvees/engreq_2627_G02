# RF05 – Pagamentos e faturação

**Atualizado em:** 21/10/2026 · [Convenções e fontes](README.md)

## Descrição
Calcula quanto cada coprodutor tem de pagar, cobra esse valor num só pagamento e distribui-o pelos produtores. Hoje, na AMAP Porto, cada produtor recebe diretamente, com meios e momentos próprios (quota mensal dos cabazes, carne depois da pesagem, cogumelos a cada entrega). A BioGoods faz as contas em Excel e envia o valor por mensagem, e o coprodutor não tem forma simples de saber quanto deve.

**Proposta do grupo (21/10):** **cobrança centralizada**. O coprodutor faz **um só pagamento** por período, que é **dividido pelos produtores** através de um **prestador de pagamentos licenciado**. Cada produtor recebe um **resumo** de quem pagou, quanto e a que corresponde. A proposta parte da indicação do professor sobre este tipo de aplicações (E-5), do pedido de concentrar os pagamentos (E-1) e do modelo "possível" descrito pela BioGoods (E-2 §13).

**Limites:** o sistema **não guarda o dinheiro** (o prestador licenciado é que o movimenta, PSD2) e **não emite faturas** (cada produtor fatura no seu programa; RNF-RES-01, em aberto).

## Sequências estímulo/resposta
- Chega o início do período → o sistema calcula o valor de cada coprodutor, discriminado por produtor, e envia-lhe o pedido de pagamento.
- O coprodutor paga (ex.: MB Way, referência Multibanco) → o prestador confirma o pagamento, divide o valor pelos produtores e o sistema regista-o automaticamente.
- O produtor regista o peso real da carne entregue → o valor entra no pagamento seguinte.
- Termina o período → cada produtor recebe o resumo de quem pagou, quanto e a que corresponde.
- Um pagamento fica por fazer depois do prazo → o sistema avisa o coprodutor e a gestão da AMAP.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-PAG-01 | O sistema deve permitir à gestão da AMAP escolher os meios de pagamento disponíveis através do prestador (ex.: MB Way, referência Multibanco, cartão) e a cada produtor associar a conta onde recebe a sua parte. | Gestão, Produtor | M | D-A, D-C §4.3, CA, DOC-10, proposta do grupo (a partir de E-5) | Proposto |
| RF-PAG-02 | O sistema deve permitir configurar, por produtor e por produto, quando cada valor é cobrado: antecipado no ciclo, no início de cada mês ou depois da entrega ou pesagem. | Produtor | M | D-A, E-1 §3.9, E-3 §4, N7 | A validar (C3) |
| RF-PAG-03 | O sistema deve calcular o valor a pagar por cada coprodutor em cada período, discriminado por produtor: quotas fixas + extras + produtos pesados − faltas compensadas. | Sistema | M | E-2 §2, D-A, E-3 §4, DOC-09 | A validar (C3) |
| RF-PAG-04 | O sistema deve enviar ao coprodutor o pedido de pagamento e mostrar-lhe, numa só vista, o valor total, o detalhe por produtor e o histórico de pagamentos. | Sistema, Coprodutor | M | E-3 §4, N6, N8, DOC-17 | Proposto |
| RF-PAG-05 | O sistema deve registar automaticamente os pagamentos confirmados pelo prestador e permitir à gestão registar manualmente pagamentos feitos fora da plataforma (ex.: numerário). | Sistema, Gestão | M | D-C §4.3, E-3 §4, DOC-11 | Proposto |
| RF-PAG-06 | O sistema deve mostrar à gestão e a cada produtor o estado dos pagamentos por coprodutor e avisar de pagamentos em atraso. | Sistema, Gestão, Produtor | S | DV-19, DV-20 | A validar (DV-20) |
| RF-PAG-07 | O sistema deve permitir ao produtor registar a fatura que emitiu no seu programa (número, data, documento), sem a emitir no sistema. | Produtor | S | D-F, DOC-36, C4 | A validar (C6) |
| RF-PAG-08 | O sistema deve guardar a taxa de IVA de cada produto e o regime de IVA de cada produtor, e mostrar os preços com IVA incluído. | Produtor | C | D-A, DOC-41 | Proposto |
| RF-PAG-09 | O sistema deve permitir à gestão da AMAP registar a quota anual de cada membro e o fundo comum, e produzir o relatório anual de contas. | Gestão | C | D-C §4.3, §4.5, DOC-24 | A validar (DV-22) |
| RF-PAG-10 | O sistema deve concentrar numa só operação os pagamentos de um coprodutor a vários produtores, sendo o valor dividido pelos produtores através de um prestador de pagamentos licenciado (o sistema não guarda o dinheiro). | Coprodutor, Sistema | M | Proposta do grupo (a partir de E-5), E-1 §3.9, E-2 §13 | Proposto |
| RF-PAG-11 | O sistema deve permitir pagamentos online integrados, através de um prestador de pagamentos licenciado. | Coprodutor | M | Proposta do grupo (a partir de E-5), E-1 §3.9, PSD2 | Proposto |
| RF-PAG-12 | O sistema deve emitir faturas em nome do produtor ou da AMAP. | Produtor, Gestão | W | E-1 §3.9, E-2 §13 | A validar (C6) |
| RF-PAG-13 | O sistema deve gerar, para cada produtor e período, um **resumo dos pagamentos recebidos**: quem pagou, quanto, quando e a que subscrição, produtos ou entregas corresponde. | Sistema, Produtor | M | Proposta do grupo (a partir de E-5), E-2 §2 (contas em Excel), DOC-09 | Proposto |
| RF-PAG-14 | O sistema deve calcular o valor a cobrar pela FAIR a cada produtor ou AMAP, segundo o modelo de cobrança definido (ex.: fee mínima mais uma componente de volume). | Administrador FAIR | C | E-1 §4, E-5 | A validar (DV-25) |
