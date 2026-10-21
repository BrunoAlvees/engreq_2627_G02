# RF02 – Catálogo e ofertas

**Atualizado em:** 14/10/2026 · [Convenções e fontes](README.md)

## Descrição
Permite a cada produtor manter o seu catálogo (cabazes, produtos extra e avulso) e definir, para cada produto, as variantes, o tipo de preço, a periodicidade e a capacidade. Hoje o catálogo vive no Google Forms: muitas opções ficam em texto livre e há produtos que existem mas não aparecem (ex.: cogumelos secos).

## Sequências estímulo/resposta
- O produtor cria um produto e indica o tipo de preço e a periodicidade → o produto fica disponível para o próximo ciclo.
- O produtor reutiliza o catálogo do ciclo anterior → o sistema copia os produtos e o produtor só ajusta preços e datas.
- A capacidade de um produto esgota → o sistema deixa de aceitar subscrições e propõe a lista de espera.
- O produtor tem um excedente ou um produto novo → publica uma oferta pontual, limitada a X coprodutores ou a uma quantidade por pessoa.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-CAT-01 | O sistema deve permitir ao produtor criar, alterar e desativar produtos no seu catálogo, sem uma lista fechada de produtos. | Produtor | M | E-2 §5, E-3 §11 | Proposto |
| RF-CAT-02 | O sistema deve distinguir os tipos de produto cabaz, extra e avulso. | Produtor | M | D-A, E-2 §4–5 | Proposto |
| RF-CAT-03 | O sistema deve permitir a um produtor oferecer vários tipos de cabaz, cada um com nome, descrição, peso aproximado, número de variedades e preço. | Produtor | M | E-2 §4, D-A, DOC-07 | Proposto |
| RF-CAT-04 | O sistema deve permitir variantes de um produto (ex.: escalão de preço, tamanho, variedade, sem glúten), cada uma com o seu preço. | Produtor | M | D-A, E-3, DOC-06 | Proposto |
| RF-CAT-05 | O sistema deve suportar três tipos de preço: quota mensal fixa, preço por unidade e preço por kg com o peso real registado na entrega. | Produtor | M | D-A, E-2 §7, DOC-05 | Proposto |
| RF-CAT-06 | O sistema deve permitir definir a periodicidade de cada produto: quinzenal, mensal, trimestral, entrega única, só em certos meses ou em datas escolhidas pelo coprodutor. | Produtor | M | D-A, E-1 §3.3, DOC-04 | Proposto |
| RF-CAT-07 | O sistema deve permitir definir uma capacidade máxima por produto e por AMAP e gerir uma lista de espera quando é atingida. | Produtor | M | D-A, E-1 §3.5, DOC-08 | Proposto |
| RF-CAT-08 | O sistema deve mostrar a ficha de cada produto: descrição, certificação, conservação e validade, origem (produção própria ou de outro produtor) e IVA incluído. | Coprodutor | S | D-A, DOC-16 | Proposto |
| RF-CAT-09 | O sistema deve mostrar a ficha de cada produtor: descrição, localização, forma de produção, certificações e contactos. | Coprodutor | S | D-A, E-1 §3.6, DOC-16 | Proposto |
| RF-CAT-10 | O sistema deve permitir ao produtor publicar ofertas pontuais (ex.: excedentes ou produtos novos), que os coprodutores podem encomendar fora da subscrição. O produtor pode limitar a oferta a um número máximo de coprodutores (por ordem de chegada) e/ou a uma quantidade máxima por pessoa. | Produtor, Coprodutor | S | E-3 §11, N10, Brainstorm 14/10 | Proposto |
| RF-CAT-11 | O sistema deve permitir ao produtor reutilizar o catálogo de um ciclo anterior ao preparar um novo ciclo. | Produtor | S | E-1 (aula 1) | Proposto |
| RF-CAT-12 | O sistema deve permitir ao produtor indicar alternativas a um produto (ex.: cogumelos secos quando não há frescos). | Produtor | C | E-3 §3, §11 | Proposto |
| RF-CAT-13 | O sistema deve evitar a duplicação entre cabaz e avulso (ex.: reduzir o mirtilo avulso quando o cabaz já o inclui). | Sistema | C | D-A, DOC-15 | Proposto |
| RF-CAT-14 | Nas ofertas pontuais, o sistema deve permitir ao produtor indicar a quantidade disponível, descontá-la à medida que chegam encomendas, fechar a oferta quando esgota e ajustar a quantidade a qualquer momento. | Produtor | S | E-3 §11, RF-CAT-10, Brainstorm 14/10 | Proposto |
| RF-CAT-15 | O sistema deve permitir ao produtor definir um desconto nos produtos extra para quem já subscreve um cabaz. | Produtor | C | E-2 (notas do grupo), C9 | A validar (C9, DV-24) |
