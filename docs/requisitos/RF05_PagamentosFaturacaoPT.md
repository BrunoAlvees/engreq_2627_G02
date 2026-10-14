# RF05 – Pagamentos e faturação

**Atualizado em:** 14/10/2026 · [Convenções e fontes](README.md)

## Descrição
Calcula quanto cada coprodutor deve a cada produtor e acompanha os pagamentos. Na AMAP Porto, cada produtor recebe diretamente, com meios e momentos próprios: quota mensal dos cabazes, carne depois da pesagem, cogumelos a cada entrega. Hoje a BioGoods faz as contas em Excel e envia o valor por mensagem, e o coprodutor não tem forma simples de saber quanto deve.

**Proposta de âmbito (C6, a validar):** o sistema **calcula, mostra e regista** os pagamentos, mas **não recebe dinheiro nem emite faturas**. Isto respeita a Carta de Princípios (sem intermediários) e evita as obrigações de software de faturação certificado e da PSD2.

## Sequências estímulo/resposta
- Chega o início do mês → o sistema gera a nota de pagamento de cada coprodutor por produtor e envia-a.
- O coprodutor paga por MB Way e marca a nota como paga → o produtor confirma a receção.
- O produtor regista o peso real da carne entregue → o valor entra na nota seguinte.
- Uma nota fica por pagar depois do prazo → o sistema avisa o coprodutor e o produtor.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-PAG-01 | O sistema deve permitir a cada produtor configurar os meios de pagamento que aceita (transferência, MB Way, numerário) e as instruções de pagamento. | Produtor | M | D-A, D-C §4.3, CA, DOC-10 | Proposto |
| RF-PAG-02 | O sistema deve permitir configurar, por produtor e por produto, o momento do pagamento: antecipado no ciclo, no início de cada mês, a cada entrega ou depois da pesagem. | Produtor | M | D-A, E-1 §3.9, E-3 §4, N7 | A validar (C3) |
| RF-PAG-03 | O sistema deve calcular a nota de pagamento de cada coprodutor por produtor e período: quotas fixas + extras + produtos pesados − faltas compensadas. | Sistema | M | E-2 §2, D-A, E-3 §4, DOC-09 | A validar (C3) |
| RF-PAG-04 | O sistema deve enviar a nota de pagamento ao coprodutor e mostrar-lhe, numa só vista, quanto deve a cada produtor e o histórico de pagamentos. | Sistema, Coprodutor | M | E-3 §4, N6, N8, DOC-17 | Proposto |
| RF-PAG-05 | O sistema deve permitir ao coprodutor marcar um pagamento como feito (com comprovativo opcional) e ao produtor confirmar a receção. | Coprodutor, Produtor | M | D-C §4.3, E-3 §4, DOC-11 | Proposto |
| RF-PAG-06 | O sistema deve mostrar ao produtor o estado dos pagamentos por coprodutor e avisar de pagamentos em atraso. | Sistema, Produtor | S | DV-19, DV-20 | A validar (DV-20) |
| RF-PAG-07 | O sistema deve permitir ao produtor registar a fatura que emitiu no seu programa (número, data, documento), sem a emitir no sistema. | Produtor | S | D-F, DOC-36, C4 | A validar (C6) |
| RF-PAG-08 | O sistema deve guardar a taxa de IVA de cada produto e o regime de IVA de cada produtor, e mostrar os preços com IVA incluído. | Produtor | C | D-A, DOC-41 | Proposto |
| RF-PAG-09 | O sistema deve permitir à gestão da AMAP registar a quota anual de cada membro e o fundo comum, e produzir o relatório anual de contas. | Gestão | C | D-C §4.3, §4.5, DOC-24 | A validar (DV-22) |
| RF-PAG-10 | O sistema deve permitir concentrar numa só operação os pagamentos de um coprodutor a vários produtores, com a AMAP a receber e a pagar aos produtores. | Gestão | W | E-1 §3.9, E-2 §13 | A validar (C6) |
| RF-PAG-11 | O sistema deve permitir pagamentos online integrados, através de um prestador de pagamentos licenciado. | Coprodutor | W | E-1 §3.9, PSD2 | A validar (C6) |
| RF-PAG-12 | O sistema deve emitir faturas em nome do produtor ou da AMAP. | Produtor, Gestão | W | E-1 §3.9, E-2 §13 | A validar (C6) |
