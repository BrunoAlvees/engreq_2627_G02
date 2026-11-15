# 5 Modelo de domínio

**Responsável:** Bruno Alves · **Atualizado em:** 14/11/2026 · **Estado:** pronto para o relatório
**Fontes:** secção 3 (FR-01 a FR-45), entrevista de 10/11 (E-8), [diagramas de estado (12.2)](../requisitos/diagramas/DiagramasEstadoPT.md). Substitui o primeiro [modelo de domínio](../requisitos/diagramas/ModeloDominioPT.md), de 14/10. Diagramas: `requisitos/diagramas/imagens/Dominio*EN.drawio` e `.png` (só em inglês, porque são para o relatório).

# 5 Modelo de domínio

O modelo de domínio descreve os principais conceitos do FAIR-AMAP e as relações entre eles, com a linguagem das AMAP e sem depender de tecnologia. Está organizado em cinco bounded contexts: partes do domínio com vocabulário e regras próprios, alinhadas com as funcionalidades da secção 3. O modelo lógico de dados e o dicionário de dados que dele resultam estão na secção 4.

## 5.1 Visão geral do modelo de domínio

O núcleo do domínio é a AMAP e os seus membros: todos os outros contextos referem uma AMAP, uma pessoa e o papel que essa pessoa tem nela. As subscrições feitas num ciclo geram as entregas e os valores a pagar; as entregas e os pagamentos geram os avisos enviados aos membros. Dois sistemas externos completam o quadro: o prestador de pagamentos licenciado, que divide cada pagamento pelos produtores, e os serviços de notificação.

![Bounded contexts do FAIR-AMAP (context map)](DominioContextosEN.png)

| Bounded context | Objetivo | Funcionalidades | Conceitos principais |
|---|---|---|---|
| Membership (adesão) | Quem pertence a cada AMAP, com que papel e estado, e com que regras | 3.1 | FAIR (plataforma), AMAP, regras da AMAP, pessoa, adesão, consentimento, pedido de desistência, candidatura de produtor, visita à exploração |
| Catálogo e subscrições | O que cada produtor oferece em cada ciclo e o que cada coprodutor subscreve | 3.2, 3.3 | Perfil do produtor, produto, variante, ciclo, oferta, subscrição, linha de subscrição, exclusão |
| Entregas | O que acontece em cada data de entrega, para cada coprodutor | 3.4 | Data de entrega, entrega, item entregue, falta, ausência, levantamento, etiqueta do saco |
| Pagamentos | Quanto paga cada coprodutor, a quem, e o que a FAIR cobra | 3.5 | Regras de pagamento, pedido de pagamento, parte do produtor, pagamento, valor cobrado pela FAIR |
| Comunicação e comunidade | Notificações, mensagens, documentos e a vida da AMAP como comunidade | 3.6, 3.7, 3.8 | Notificação, aviso, mensagem, notícia, documento, evento, grupo de trabalho, turno da escala, assembleia, feedback, exportação de dados |

## 5.2 Membership (adesão)

A FAIR gere a plataforma: define o modelo de preços, é a subcontratante no tratamento de dados (NFR-08) e os seus administradores autorizam cada AMAP e atribuem o primeiro gestor (FR-01, FR-06). Uma AMAP regista-se na plataforma e, depois de autorizada, as suas regras (duração do ciclo, entregas experimentais, modo de renovação, destinos do cabaz nas ausências, regras de desistência) são configuradas pela sua própria gestão (FR-01, NFR-24). Uma pessoa pode ter várias adesões: em várias AMAP, ou como produtor e gestão da mesma AMAP (FR-06, FR-07). A adesão tem o papel e o estado, cujo ciclo de vida está nos diagramas de estado da secção 12.2. Os consentimentos guardam a versão e a data de cada documento aceite (FR-05). Um produtor entra através de uma candidatura, normalmente depois de uma visita à exploração (FR-08); um coprodutor que quer sair a meio do período faz um pedido de desistência (FR-07).

![Diagrama de classes – Membership](DominioMembershipEN.png)

## 5.3 Catálogo e subscrições

Cada produtor tem um perfil público e um catálogo de produtos (cabazes, extras e produtos pontuais), cada um com uma ou mais variantes e o seu tipo de preço (FR-11 a FR-13). Uma oferta coloca uma variante num ciclo, com o preço e a capacidade desse ciclo, para que o catálogo possa ser reutilizado de um ciclo para o seguinte (FR-11, FR-14). Um coprodutor faz uma subscrição por ciclo, com uma linha por oferta escolhida, possivelmente de vários produtores (FR-18). As exclusões (alergias, intolerâncias, gostos) pertencem ao coprodutor e não a uma subscrição (FR-19, NFR-06).

![Diagrama de classes – Catálogo e subscrições](DominioCatalogoEN.png)

## 5.4 Entregas

Cada ciclo tem um calendário de datas de entrega por produtor (FR-24). Em cada data, cada coprodutor com subscrição tem uma entrega, cujo estado é prevista, ausente, levantada, não levantada ou cancelada (diagrama de estados na 12.2). Os itens entregues registam a quantidade ou o peso real e a substituição feita (FR-26); as faltas registam a compensação (FR-26). Uma entrega pode ter uma ausência, com o destino do cabaz e quem o levanta (FR-27), e fecha com um levantamento, confirmado com o botão ou com o código QR da etiqueta do saco (FR-28, FR-29).

![Diagrama de classes – Entregas](DominioEntregasEN.png)

## 5.5 Pagamentos

As regras de pagamento indicam os meios aceites pela AMAP, a conta de cada produtor e quando é cobrado cada produto (FR-30). Um pedido de pagamento junta, para um coprodutor e um período, as partes de todos os produtores (FR-31). O coprodutor paga-o com um só pagamento, processado pelo prestador licenciado, que transfere a parte de cada produtor; o sistema nunca guarda o dinheiro (FR-32, NFR-19). Os pagamentos feitos fora da plataforma registam-se à mão (FR-32). O valor cobrado pela FAIR é o que a FAIR cobra a cada AMAP por período: uma mensalidade por AMAP mais uma percentagem das transações (FR-34, NFR-21).

![Diagrama de classes – Pagamentos](DominioPagamentosEN.png)

## 5.6 Comunicação e comunidade

Este contexto junta o que mantém os membros informados e organizados. As notificações são geradas por acontecimentos dos outros contextos e enviadas pelos canais que cada pessoa escolhe (FR-35, FR-38); os avisos, as mensagens e as notícias são escritos pela gestão ou pelos produtores (FR-36, FR-37). Os documentos guardam as suas versões (FR-39). Os eventos, grupos de trabalho, turnos da escala, assembleias e o feedback apoiam o lado comunitário da AMAP (FR-40, FR-41), e as exportações de dados só têm dados anonimizados ou de membros que deram consentimento (FR-44). Os indicadores (FR-43) calculam-se a partir dos outros contextos e não são guardados.

![Diagrama de classes – Comunicação e comunidade](DominioComunicacaoEN.png)
