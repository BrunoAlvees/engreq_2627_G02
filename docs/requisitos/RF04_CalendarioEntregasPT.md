# RF04 – Calendário e entregas

**Atualizado em:** 21/10/2026 · [Convenções e fontes](README.md)

## Descrição
Gere o calendário de distribuição e tudo o que acontece em cada entrega: composição do cabaz, disponibilidade, faltas, ausências, levantamento e cabazes esquecidos. É a área com mais problemas no sistema atual: não há confirmação de levantamento, os cabazes ficam no exterior depois das 19h30 e as ausências e faltas são combinadas por mensagem.

## Sequências estímulo/resposta
- O produtor publica a composição do cabaz → cada coprodutor vê o que vai levantar, já com as suas exclusões e o peso aproximado.
- O coprodutor indica que vai faltar → escolhe o destino do cabaz entre as opções da AMAP e o produtor é avisado.
- O coprodutor levanta o cabaz → confirma o levantamento na aplicação (ou, se a ideia RF-ENT-19 avançar, lê o QR do saco).
- O horário de distribuição termina com cabazes por confirmar → o sistema avisa o coprodutor e o produtor.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-ENT-01 | O sistema deve permitir à gestão da AMAP definir o local e o horário de distribuição (dia da semana e horas) e alterá-los pontualmente (ex.: feriados). | Gestão | M | D-A, D-B §3.3, DOC-33, Brainstorm 14/10 | Proposto |
| RF-ENT-02 | O sistema deve permitir dias de entrega diferentes por AMAP e que um produtor sirva AMAP diferentes em semanas alternadas. | Gestão, Produtor | M | E-2 §6 | Proposto |
| RF-ENT-03 | O sistema deve permitir a cada produtor definir as suas datas de entrega no ciclo, dentro do horário da AMAP, com periodicidade própria e datas específicas por produto (ex.: Biogoods quinzenal; Quinta da Serrinha em setembro e dezembro; pão em todas as datas menos duas). O coprodutor vê num só calendário as datas de todos os produtores a quem compra. | Produtor | M | E-3 §2 (os produtores definem as datas), D-A, DOC-03, C1, Brainstorm 14/10, N18 | Proposto |
| RF-ENT-04 | O sistema deve permitir vários pontos de entrega numa AMAP. | Gestão | C | E-2 §6 | Proposto |
| RF-ENT-05 | O sistema deve permitir ao produtor publicar a composição do cabaz antes de cada entrega. | Produtor | M | E-2 §4, N1 | Proposto |
| RF-ENT-06 | O sistema deve mostrar a cada coprodutor o que vai levantar em cada data, de todos os produtores, tendo em conta exclusões e substituições, e o peso aproximado. | Coprodutor | M | E-2 §4, E-3 §10, N2, N9 | Proposto |
| RF-ENT-07 | O sistema deve permitir ao produtor confirmar a disponibilidade de um produto antes da entrega (ex.: cogumelos, pães sazonais) e avisar os coprodutores afetados. | Produtor | S | D-A, E-3 §3, DOC-12, N18 | Proposto |
| RF-ENT-08 | O sistema deve permitir registar faltas de produto numa entrega e a compensação dada (desconto ou substituição noutra entrega). | Produtor | S | E-3 §7, DOC-34 | Proposto |
| RF-ENT-09 | O sistema deve permitir distribuir uma falta por AMAP em rotação, em vez de entregas parciais dentro da mesma AMAP. | Produtor | C | E-3 §7 | Proposto |
| RF-ENT-10 | O sistema deve permitir registar a quantidade ou o peso real entregue a cada coprodutor (ex.: carne). | Produtor | M | D-A | Proposto |
| RF-ENT-11 | O sistema deve permitir ao coprodutor indicar uma ausência e escolher o destino do cabaz numa lista definida pela AMAP (amigo ou familiar, doação, distribuição pelos outros, sorteio…). | Coprodutor | M | E-2 §9, E-3 §6, N4, DOC-25 | Proposto |
| RF-ENT-12 | O sistema deve permitir ao coprodutor indicar quem vai levantar o cabaz em seu nome. | Coprodutor | S | E-2 §10, E-3 §9 | Proposto |
| RF-ENT-13 | O sistema deve permitir confirmar o levantamento de cada cabaz, pelo próprio coprodutor ou por quem levanta em seu nome. | Coprodutor | M | E-2 §10, E-3 §9, N3 | A validar (obrigatória?) |
| RF-ENT-14 | No fim do horário, o sistema deve assinalar os cabazes não confirmados e avisar o coprodutor e o produtor. | Sistema | S | D-B §3.3, E-2 §10, DOC-26 | Proposto |
| RF-ENT-15 | O sistema deve gerar a folha de distribuição de cada data (o que cada coprodutor leva, de cada produtor), em PDF A4 para imprimir. As etiquetas dos sacos estão no RF-ENT-18. | Gestão, Produtor | M | D-C §4.5, E-3 §8, DOC-27, DOC-35 | A validar (DV-13) |
| RF-ENT-16 | Depois do horário de distribuição, o sistema deve pedir ao coprodutor que confirme o levantamento, se ainda não o fez. | Sistema | S | Brainstorm 14/10 (as pessoas esquecem-se de confirmar), E-3 §9 | Proposto |
| RF-ENT-17 | O sistema deve permitir a um voluntário, à gestão ou ao produtor confirmar o levantamento em nome de um coprodutor sem telemóvel. | Gestão, Produtor | S | Brainstorm 14/10 | Proposto |
| RF-ENT-18 | O sistema deve gerar, em PDF A4, etiquetas para os sacos com nome, "Saco x de y", produtor e data, sem dados de saúde. | Sistema, Produtor | S | E-3 §8 ("Nome 1 de 2"), CA (CSAware: etiquetas), Brainstorm 14/10 | Proposto |
| RF-ENT-19 | **Ideia:** cada etiqueta pode ter um QR code individual. Ao ler o QR, o coprodutor confirma o levantamento desse saco, e o sistema avisa se o saco não for dele. | Coprodutor | C | Brainstorm 14/10; E-3 §9 (pão levado pela pessoa errada); nenhuma solução analisada tem esta funcionalidade | Ideia (avaliar na implementação) |

## Nota: brainstorm de 14/10 sobre o levantamento
- **Lá fora** usa-se sobretudo uma **folha impressa** onde cada um marca o seu nome (a "liste d'émargement" das AMAP francesas, gerada pelo Cagette; a folha de registo da Lancaster Farm Fresh, nos EUA). Não encontrámos nenhuma solução com confirmação por QR code.
- **Decisão do grupo:** a base é a **confirmação na aplicação** (RF-ENT-13), com lembrete para quem se esquece (RF-ENT-16). Uma folha única não traz vantagem sobre a aplicação.
- O **QR individual por saco** (RF-ENT-19) evitaria trocas de sacos, mas obriga o produtor a imprimir e colar etiquetas todas as semanas. Fica como **ideia**, a avaliar na implementação e a validar com os stakeholders (DV-27, DV-28).
