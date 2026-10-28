# RF06 – Comunicação e notificações

**Atualizado em:** 21/10/2026 · [Convenções e fontes](README.md)

## Descrição
Substitui as mensagens de WhatsApp e os emails soltos por avisos automáticos e por canais de comunicação dentro da plataforma: lembretes de entrega, avisos da AMAP e mensagens entre produtor e coprodutor. Hoje os coprodutores esquecem-se das entregas e a produtora envia todas as semanas um WhatsApp com a composição do cabaz.

## Sequências estímulo/resposta
- Falta um dia para a entrega → o sistema envia um lembrete a cada coprodutor com o que vai levantar.
- A gestão publica um aviso → todos os membros da AMAP o recebem.
- O produtor publica uma notícia da produção → os seus coprodutores recebem-na.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-COM-01 | O sistema deve enviar um lembrete antes de cada entrega, com a antecedência configurada, indicando o que o coprodutor vai levantar. | Sistema | M | E-1 §3.8, E-2 §14, E-3 §9, N5 | Proposto |
| RF-COM-02 | O sistema deve notificar automaticamente: abertura de ciclo, novas ofertas, composição do cabaz, alteração de datas, disponibilidade de produtos, cabaz não levantado e nova nota de pagamento. | Sistema | M | E-1 §4, E-2 §4, D-A, D-C | Proposto |
| RF-COM-03 | O sistema deve permitir à gestão da AMAP enviar avisos a todos os membros ou a um grupo (ex.: só coprodutores). | Gestão | M | D-C §4.6, E-3 §12 | Proposto |
| RF-COM-04 | O sistema deve permitir mensagens entre produtor e coprodutor, e do produtor para todos os seus coprodutores. | Produtor, Coprodutor | S | D-A, D-C §4.6, E-2 §2, N19 | Proposto |
| RF-COM-05 | O sistema deve permitir ao produtor publicar notícias sobre a produção (ex.: estado das culturas, uma praga, estragos do tempo), que ficam no seu perfil público e são enviadas aos seus coprodutores. Uma notícia pode ficar associada a uma falta de produto (RF-ENT-08), para explicar porque é que o cabaz não traz esse produto. | Produtor | S | E-1 §3.8, N19, Brainstorm 21/10 | Proposto |
| RF-COM-06 | O sistema deve permitir a cada utilizador escolher como recebe as notificações (ex.: email ou notificação na aplicação). | Coprodutor, Produtor | S | Hip. (E-3 §12: WhatsApp e email) | A validar |
