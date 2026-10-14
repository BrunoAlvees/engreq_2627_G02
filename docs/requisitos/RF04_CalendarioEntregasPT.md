# RF04 – Calendário e entregas

**Atualizado em:** 14/10/2026 · [Convenções e fontes](README.md)

## Descrição
Gere o calendário de distribuição e tudo o que acontece em cada entrega: composição do cabaz, disponibilidade, faltas, ausências, levantamento e cabazes esquecidos. É a área com mais problemas no sistema atual: não há confirmação de levantamento, os cabazes ficam no exterior depois das 19h30 e as ausências e faltas são combinadas por mensagem.

## Sequências estímulo/resposta
- O produtor publica a composição do cabaz → cada coprodutor vê o que vai levantar, já com as suas exclusões e o peso aproximado.
- O coprodutor indica que vai faltar → escolhe o destino do cabaz entre as opções da AMAP e o produtor é avisado.
- O coprodutor levanta o cabaz → confirma o levantamento no sistema.
- O horário de distribuição termina com cabazes por confirmar → o sistema avisa o coprodutor e o produtor.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-ENT-01 | O sistema deve gerar o calendário de entregas do ciclo a partir do dia, do horário, da frequência e do local da AMAP, e permitir alterar datas (ex.: feriados). | Gestão, Produtor | M | D-A, E-3 §2, DOC-02, DOC-33 | A validar (C1: quem aprova?) |
| RF-ENT-02 | O sistema deve permitir dias de entrega diferentes por AMAP e que um produtor sirva AMAP diferentes em semanas alternadas. | Gestão, Produtor | M | E-2 §6 | Proposto |
| RF-ENT-03 | O sistema deve permitir ao produtor indicar as datas do calendário a que não vai, e datas próprias para certos produtos (ex.: carne, azeite). | Produtor | M | D-A, DOC-03 | Proposto |
| RF-ENT-04 | O sistema deve permitir vários pontos de entrega numa AMAP. | Gestão | C | E-2 §6 | Proposto |
| RF-ENT-05 | O sistema deve permitir ao produtor publicar a composição do cabaz antes de cada entrega. | Produtor | M | E-2 §4, N1 | Proposto |
| RF-ENT-06 | O sistema deve mostrar a cada coprodutor o que vai levantar em cada data, de todos os produtores, tendo em conta exclusões e substituições, e o peso aproximado. | Coprodutor | M | E-2 §4, E-3 §10, N2, N9 | Proposto |
| RF-ENT-07 | O sistema deve permitir ao produtor confirmar a disponibilidade de um produto antes da entrega (ex.: cogumelos, pães sazonais) e avisar os coprodutores afetados. | Produtor | S | D-A, E-3 §3, DOC-12 | Proposto |
| RF-ENT-08 | O sistema deve permitir registar faltas de produto numa entrega e a compensação dada (desconto ou substituição noutra entrega). | Produtor | S | E-3 §7, DOC-34 | Proposto |
| RF-ENT-09 | O sistema deve permitir distribuir uma falta por AMAP em rotação, em vez de entregas parciais dentro da mesma AMAP. | Produtor | C | E-3 §7 | Proposto |
| RF-ENT-10 | O sistema deve permitir registar a quantidade ou o peso real entregue a cada coprodutor (ex.: carne). | Produtor | M | D-A | Proposto |
| RF-ENT-11 | O sistema deve permitir ao coprodutor indicar uma ausência e escolher o destino do cabaz numa lista definida pela AMAP (amigo ou familiar, doação, distribuição pelos outros, sorteio…). | Coprodutor | M | E-2 §9, E-3 §6, N4, DOC-25 | Proposto |
| RF-ENT-12 | O sistema deve permitir ao coprodutor indicar quem vai levantar o cabaz em seu nome. | Coprodutor | S | E-2 §10, E-3 §9 | Proposto |
| RF-ENT-13 | O sistema deve permitir confirmar o levantamento de cada cabaz, pelo próprio coprodutor ou por quem levanta em seu nome. | Coprodutor | M | E-2 §10, E-3 §9, N3 | A validar (obrigatória?) |
| RF-ENT-14 | No fim do horário, o sistema deve assinalar os cabazes não confirmados e avisar o coprodutor e o produtor. | Sistema | S | D-B §3.3, E-2 §10, DOC-26 | Proposto |
| RF-ENT-15 | O sistema deve gerar a folha de distribuição de cada data (o que cada coprodutor leva, de cada produtor) e as etiquetas dos sacos (ex.: "Nome 1 de 2"), para imprimir. | Gestão, Produtor | M | D-C §4.5, E-3 §8, DOC-27, DOC-35 | A validar (DV-13) |
