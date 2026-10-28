# RF06 – Comunicação e notificações

**Atualizado em:** 28/10/2026 · [Convenções e fontes](README.md)

## Descrição
Substitui as mensagens de WhatsApp e os emails soltos por avisos automáticos e por canais de comunicação dentro da plataforma: lembretes de entrega, avisos da AMAP e mensagens entre produtor e coprodutor. Hoje os coprodutores esquecem-se das entregas e a produtora envia todas as semanas um WhatsApp com a composição do cabaz.

## Sequências estímulo/resposta
- Falta um dia para a entrega → o sistema envia um lembrete a cada coprodutor com o que vai levantar.
- A gestão publica um aviso → todos os membros da AMAP o recebem.
- O produtor publica uma notícia da produção → os seus coprodutores recebem-na.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-COM-01 | O sistema deve enviar notificações automáticas aos utilizadores sobre os acontecimentos que lhes dizem respeito, incluindo um lembrete antes de cada entrega. | Sistema | M | E-1 §3.8, §4, E-2 §4, §14, E-3 §9, D-A, D-C, N5 | Proposto |
| RF-COM-02 | O sistema deve permitir à gestão da AMAP enviar avisos a todos os membros ou a um grupo. | Gestão | M | D-C §4.6, E-3 §12 | Proposto |
| RF-COM-03 | O sistema deve permitir ao produtor comunicar com os seus coprodutores, através de mensagens e de notícias sobre a produção. | Produtor, Coprodutor | S | D-A, D-C §4.6, E-1 §3.8, E-2 §2, N19, Brainstorm 21/10 | Proposto |
| RF-COM-04 | O sistema deve permitir a cada utilizador escolher como recebe as notificações. | Coprodutor, Produtor | S | E-3 §12, RNF-INT-01, decisão do grupo de 21/10 e 28/10 | Proposto |

## Critérios de aceitação

**RF-COM-01 – Notificações automáticas**
- Antes de cada entrega, com a antecedência configurada, o coprodutor recebe um lembrete com o que vai levantar.
- O sistema notifica também: abertura de ciclo, novas ofertas, composição do cabaz, alteração de datas, disponibilidade e faltas de produtos, cabaz não levantado e novo pedido de pagamento.

**RF-COM-02 – Avisos da gestão**
- A gestão envia avisos a todos os membros da AMAP ou a um grupo (ex.: só coprodutores, só produtores).

**RF-COM-03 – Comunicação do produtor**
- O produtor troca mensagens com um coprodutor e pode escrever a todos os seus coprodutores.
- O produtor publica notícias sobre a produção (ex.: estado das culturas, uma praga, estragos do tempo), que ficam no seu perfil público (RF-MEM-04) e são enviadas aos seus coprodutores.
- Uma notícia pode ficar associada a uma falta de produto (RF-ENT-03), para explicar porque é que o cabaz não traz esse produto.

**RF-COM-04 – Canais de notificação**
- Cada utilizador escolhe os canais: email (RNF-INT-01), notificações push no telemóvel (RNF-INT-01) e, opcionalmente, WhatsApp (RNF-INT-01).
- O WhatsApp é usado através da API oficial do WhatsApp Business, com mensagens individuais, e não através de um bot num grupo (os bots não oficiais violam as regras do WhatsApp e podem levar ao bloqueio do número).

## Correspondência com a versão anterior
Na revisão de 28/10, os 6 requisitos anteriores foram agrupados em 4, para reduzir o detalhe (indicação do professor). O detalhe passou para os critérios de aceitação.

| Novo | Junta os anteriores |
|---|---|
| RF-COM-01 | 01, 02 |
| RF-COM-02 | 03 |
| RF-COM-03 | 04, 05 |
| RF-COM-04 | 06 |
