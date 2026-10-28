# RF02 – Catálogo e ofertas

**Atualizado em:** 28/10/2026 · [Convenções e fontes](README.md)

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
| RF-CAT-01 | O sistema deve permitir ao produtor gerir o seu catálogo de cabazes, produtos extra e produtos avulso, sem uma lista fechada de produtos. | Produtor | M | E-1 (aula 1), E-2 §4–5, E-3 §11, D-A, N13 | Proposto |
| RF-CAT-02 | O sistema deve permitir ao produtor oferecer vários tipos de cabaz e variantes de cada produto. | Produtor | M | E-2 §4, E-3 §3, §11, D-A, DOC-06, DOC-07, DOC-15 | Proposto |
| RF-CAT-03 | O sistema deve permitir definir o tipo de preço e a periodicidade de cada produto. | Produtor | M | D-A, E-1 §3.3, E-2 §7, DOC-04, DOC-05, C9 | Proposto |
| RF-CAT-04 | O sistema deve permitir definir uma capacidade máxima por produto e por AMAP e gerir uma lista de espera quando é atingida. | Produtor | M | D-A, E-1 §3.5, DOC-08, N16 | Proposto |
| RF-CAT-05 | O sistema deve mostrar ao coprodutor a ficha de cada produto. | Coprodutor | S | D-A, DOC-16 | Proposto |
| RF-CAT-06 | O sistema deve permitir ao produtor publicar ofertas pontuais (ex.: excedentes ou produtos novos), que os coprodutores podem encomendar fora da subscrição. | Produtor, Coprodutor | S | E-3 §11, N10, Brainstorm 14/10 | Proposto |

## Critérios de aceitação

**RF-CAT-01 – Gerir o catálogo**
- O produtor cria, altera e desativa produtos; não há uma lista fechada (hoje é uma coisa, amanhã pode ser outra).
- Cada produto é de um de três tipos: cabaz, extra ou avulso.
- Ao preparar um novo ciclo, o produtor pode reutilizar o catálogo do ciclo anterior e só ajustar preços e datas.

**RF-CAT-02 – Tipos de cabaz e variantes**
- Um produtor pode oferecer vários tipos de cabaz (ex.: cabaz da quinta, cabaz de fruta), cada um com nome, descrição, peso aproximado, número de variedades e preço.
- Um produto pode ter variantes (ex.: escalão de preço, tamanho, variedade, sem glúten), cada uma com o seu preço.
- *(Could)* O produtor pode indicar alternativas a um produto (ex.: cogumelos secos quando não há frescos).
- *(Could)* O sistema evita a duplicação entre cabaz e avulso (ex.: reduzir o mirtilo avulso quando o cabaz já o inclui).

**RF-CAT-03 – Preço e periodicidade**
- Tipos de preço: quota mensal fixa, preço por unidade e preço por kg com o peso real registado na entrega.
- Periodicidade: quinzenal, mensal, trimestral, entrega única, só em certos meses ou em datas escolhidas pelo coprodutor.
- *(Could, a validar C9 e DV-24)* O produtor pode definir um desconto nos produtos extra para quem já subscreve um cabaz.

**RF-CAT-04 – Capacidade e lista de espera**
- A capacidade máxima é definida por produto e por AMAP.
- Quando a capacidade é atingida, o sistema deixa de aceitar subscrições e propõe a lista de espera.

**RF-CAT-05 – Ficha do produto**
- A ficha mostra a descrição, a certificação, a conservação e validade, a origem (produção própria ou de outro produtor) e o preço com IVA incluído.
- A ficha do produtor está no perfil público do produtor (RF-MEM-04).

**RF-CAT-06 – Ofertas pontuais**
- O produtor pode limitar a oferta a um número máximo de coprodutores (por ordem de chegada) e/ou a uma quantidade máxima por pessoa.
- O produtor indica a quantidade disponível; o sistema desconta-a à medida que chegam encomendas e fecha a oferta quando esgota; o produtor pode ajustar a quantidade a qualquer momento.

## Correspondência com a versão anterior
Na revisão de 28/10, os 15 requisitos anteriores foram agrupados em 6, para reduzir o detalhe (indicação do professor). O detalhe passou para os critérios de aceitação.

| Novo | Junta os anteriores |
|---|---|
| RF-CAT-01 | 01, 02, 11 |
| RF-CAT-02 | 03, 04, 12, 13 |
| RF-CAT-03 | 05, 06, 15 |
| RF-CAT-04 | 07 |
| RF-CAT-05 | 08 |
| RF-CAT-06 | 10, 14 |
| *(RF-MEM-04)* | 09 (ficha do produtor, já coberta pelo perfil público do produtor) |
