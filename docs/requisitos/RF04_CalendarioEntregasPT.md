# RF04 – Calendário e entregas

**Atualizado em:** 28/10/2026 · [Convenções e fontes](README.md)

## Descrição
Gere o calendário de distribuição e tudo o que acontece em cada entrega: composição do cabaz, disponibilidade, faltas, ausências, levantamento e cabazes esquecidos. É a área com mais problemas no sistema atual: não há confirmação de levantamento, os cabazes ficam no exterior depois das 19h30 e as ausências e faltas são combinadas por mensagem.

## Sequências estímulo/resposta
- O produtor publica a composição do cabaz → cada coprodutor vê o que vai levantar, já com as suas exclusões e o peso aproximado.
- O coprodutor indica que vai faltar → escolhe o destino do cabaz entre as opções da AMAP e o produtor é avisado.
- O coprodutor levanta o cabaz → confirma o levantamento na aplicação (ou, se a ideia do QR code avançar, lê o QR do saco).
- O horário de distribuição termina com cabazes por confirmar → o sistema avisa o coprodutor e o produtor.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-ENT-01 | O sistema deve gerir o calendário de entregas de cada AMAP, com o local e horário de distribuição e as datas e o modo de entrega de cada produtor. | Gestão, Produtor | M | D-A, D-B §3.3, E-2 §6, E-3 §2, §8, DOC-03, DOC-33, C1, N18, Brainstorm 14/10 e 21/10 | Proposto |
| RF-ENT-02 | O sistema deve permitir ao produtor publicar a composição do cabaz antes de cada entrega e mostrar a cada coprodutor o que vai levantar. | Produtor, Coprodutor | M | E-2 §4, E-3 §10, N1, N2, N9 | Proposto |
| RF-ENT-03 | O sistema deve permitir ao produtor confirmar a disponibilidade dos produtos e registar as faltas, as compensações e as quantidades reais entregues. | Produtor | M | D-A, E-3 §3, §7, DOC-12, DOC-34, N18 | Proposto |
| RF-ENT-04 | O sistema deve permitir ao coprodutor indicar uma ausência, escolher o destino do cabaz e indicar quem o levanta em seu nome. | Coprodutor | M | E-2 §9, §10, E-3 §6, §9, N4, DOC-25 | Proposto |
| RF-ENT-05 | O sistema deve permitir confirmar o levantamento de cada cabaz e assinalar os cabazes não levantados. | Coprodutor, Gestão, Produtor, Sistema | M | D-B §3.3, E-2 §10, E-3 §9, N3, DOC-26, Brainstorm 14/10 | A validar (obrigatória?) |
| RF-ENT-06 | O sistema deve gerar, em PDF A4 para imprimir, a folha de distribuição de cada data e as etiquetas dos sacos. | Gestão, Produtor, Sistema | S | D-C §4.5, E-3 §8, CA (CSAware: etiquetas), DOC-27, DOC-35, Brainstorm 14/10 | A validar (DV-13) |

## Critérios de aceitação

**RF-ENT-01 – Calendário de entregas**
- A gestão da AMAP define o local e o horário de distribuição (dia da semana e horas) e pode alterá-los pontualmente (ex.: feriados).
- Cada AMAP pode ter o seu dia de entrega, e um produtor pode servir AMAP diferentes em semanas alternadas.
- Cada produtor define as suas datas de entrega no ciclo, dentro do horário da AMAP, com periodicidade própria e datas específicas por produto (ex.: BioGoods quinzenal; Quinta da Serrinha em setembro e dezembro; pão em todas as datas menos duas).
- Cada produtor indica o seu modo de entrega (ex.: saco identificado deixado no ponto de entrega, entrega em mão, rota por vários pontos), que o coprodutor vê.
- O coprodutor vê num só calendário as datas de todos os produtores a quem compra.
- *(Could)* Uma AMAP pode ter vários pontos de entrega.

**RF-ENT-02 – Composição do cabaz**
- O produtor publica a composição do cabaz antes de cada entrega, em vez de a enviar por WhatsApp.
- Cada coprodutor vê o que vai levantar em cada data, de todos os produtores, já com as exclusões e substituições, e o peso aproximado.

**RF-ENT-03 – Disponibilidade e faltas**
- O produtor confirma a disponibilidade de um produto antes da entrega (ex.: cogumelos, pães sazonais) e os coprodutores afetados são avisados.
- O produtor regista as faltas de produto e a compensação dada (desconto ou substituição noutra entrega); pode associar uma notícia que explica a falta (RF-COM-03).
- O produtor regista a quantidade ou o peso real entregue a cada coprodutor (ex.: carne).
- *(Could)* Uma falta pode ser distribuída pelas AMAP em rotação, em vez de entregas parciais dentro da mesma AMAP.

**RF-ENT-04 – Ausências**
- O coprodutor indica a ausência e escolhe o destino do cabaz numa lista definida pela AMAP (amigo ou familiar, doação a uma instituição, distribuição pelos outros, sorteio…). O cabaz é sempre levantado e pago.
- O coprodutor indica quem vai levantar o cabaz em seu nome.
- O produtor é avisado da ausência e do destino escolhido.

**RF-ENT-05 – Confirmação de levantamento**
- O coprodutor, ou quem levanta em seu nome, confirma o levantamento na aplicação.
- Depois do horário de distribuição, o sistema pede a confirmação a quem ainda não a fez.
- No fim do horário, o sistema assinala os cabazes não confirmados e avisa o coprodutor e o produtor.
- Um voluntário, a gestão ou o produtor pode confirmar em nome de um coprodutor sem telemóvel.
- *(Ideia, avaliar na implementação)* Cada etiqueta pode ter um QR code individual: ao lê-lo, o coprodutor confirma o levantamento desse saco e o sistema avisa se o saco não for dele.

**RF-ENT-06 – Folha de distribuição e etiquetas**
- A folha de distribuição de cada data indica o que cada coprodutor leva, de cada produtor.
- As etiquetas dos sacos têm o nome, "Saco x de y", o produtor e a data, sem dados de saúde (RNF-SEG-03).

## Nota: brainstorm de 14/10 sobre o levantamento
- **Lá fora** usa-se sobretudo uma **folha impressa** onde cada um marca o seu nome (a "liste d'émargement" das AMAP francesas, gerada pelo Cagette; a folha de registo da Lancaster Farm Fresh, nos EUA). Não encontrámos nenhuma solução com confirmação por QR code.
- **Decisão do grupo:** a base é a **confirmação na aplicação** (RF-ENT-05), com lembrete para quem se esquece. Uma folha única não traz vantagem sobre a aplicação.
- O **QR individual por saco** evitaria trocas de sacos, mas obriga o produtor a imprimir e colar etiquetas todas as semanas. Fica como **ideia**, a avaliar na implementação e a validar com os stakeholders (DV-27, DV-28).

## Correspondência com a versão anterior
Na revisão de 28/10, os 20 requisitos anteriores foram agrupados em 6, para reduzir o detalhe (indicação do professor). O detalhe passou para os critérios de aceitação.

| Novo | Junta os anteriores |
|---|---|
| RF-ENT-01 | 01, 02, 03, 04, 20 |
| RF-ENT-02 | 05, 06 |
| RF-ENT-03 | 07, 08, 09, 10 |
| RF-ENT-04 | 11, 12 |
| RF-ENT-05 | 13, 14, 16, 17, 19 |
| RF-ENT-06 | 15, 18 |
