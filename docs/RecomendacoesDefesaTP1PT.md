# Recomendações do professor depois da defesa do TP1

**Autora:** Liane Duarte · **Data:** 26/11/2026 · **Estado:** para o grupo ler antes do TP2

## Contexto
Na aula a seguir às defesas, o professor apontou os **erros mais comuns dos grupos** no TP1. Nem todos eram necessariamente nossos, por isso cada ponto foi comparado com o nosso SRS final (`engreq_tp1_SRS_g002.pdf`) para ver se se aplicava a nós. Na nossa defesa (18/11), as críticas diretas foram ao **modelo de domínio** e à falta de resposta sobre **KPIs, indicadores e relatórios**.

> **Se alguém se lembrar de mais alguma coisa que o professor tenha dito na defesa ou na aula seguinte, acrescente-a neste documento** (na secção "Outras observações", no fim).

## Resumo

| # | Recomendação | Aplicava-se a nós? |
|---|---|---|
| 1 | O modelo de domínio tem de ter as classes do glossário e definir bem o modelo de negócio | Sim |
| 2 | O cabaz tem de ser decomposto nos produtos que o compõem | Sim |
| 3 | O modelo conceptual é estático, não a descrição de um processo | Sim |
| 4 | O modelo conceptual deve ter classes, não conceitos todos juntos | Em parte |
| 5 | Fazia sentido um diagrama de componentes | Sim |
| 6 | Considerar as pessoas que apanham os produtos no campo | Sim |
| 7 | Validar com o professor durante as aulas, não só no fim | Em parte |
| 8 | Usar IA é recomendado, mas o relatório tem de dizer para que foi usada | Em parte |

## Detalhe

### 1. Modelo de domínio alinhado com o glossário
- **No TP1:** termos do glossário (12.1) como *Basket*, *Basket contents*, *Production plan*, *Distribution point*, *Commitment period* e *Substitution* não aparecem como classes no modelo de domínio (5.1 a 5.6). O *Distribution point* do glossário passa a `PICKUP_POINT` no modelo de dados.
- **No TP2:** cada conceito do glossário que seja do negócio tem uma classe com o mesmo nome no modelo, e vice-versa.

### 2. Cabaz decomposto nos produtos
- **No TP1:** o cabaz é um `PRODUCT` do tipo *basket*. O seu conteúdo é só um campo de texto (`DELIVERY_DATE.basket_contents`), e o `DELIVERED_ITEM` regista a quantidade do cabaz, não dos legumes. Assim não é possível calcular indicadores como "quantos kg de alface foram vendidos" (a pergunta sobre KPIs na defesa).
- **No TP2:** criar uma classe para o conteúdo do cabaz (ex.: *Basket item*: produto, quantidade/kg, data de entrega), para que os indicadores (3.8, FR-43) sejam calculáveis a partir do modelo.

### 3. Modelo estático, não processo
- **No TP1:** a Figura 16 (mapa de contextos) tem setas de fluxo como *"subscriptions generate the deliveries"* e *"split payment"*, e o texto da 5.1 descreve uma sequência.
- **No TP2:** o modelo de domínio mostra só conceitos, atributos e associações. O comportamento fica nos diagramas de atividades e de estados (12.2).

### 4. Classes, não tudo junto
- **No TP1:** havia diagramas de classes (Fig. 17 a 22), mas a primeira figura da secção 5 é o mapa de contextos, que agrupa os conceitos em caixas sem classes.
- **No TP2:** abrir a secção com o diagrama de classes. Se o mapa de contextos se mantiver, deve aparecer como apoio e não como o modelo.

### 5. Diagrama de componentes
- **No TP1:** só havia o diagrama de contexto (Fig. 1) e o mapa de contextos. A 2.4.3 (Arquitetura) não tem diagrama.
- **No TP2:** acrescentar um diagrama de componentes: aplicação, serviços, base de dados e sistemas externos (prestador de pagamentos, notificações).

### 6. Quem apanha os produtos no campo
- **No TP1:** não havia trabalhadores agrícolas nem apanhadores nos stakeholders (10.1), nas classes de utilizadores (2.2) nem nos requisitos.
- **No TP2:** considerá-los como stakeholder/ator, com o que precisam do sistema (ex.: lista do que apanhar para cada entrega, a partir do conteúdo dos cabazes).

### 7. Validar durante as aulas
- **No TP1:** houve contributos do professor em aula (E-4 a E-7, 12.3.5), mas sobretudo como resposta a dúvidas. A única validação formal foi a E-8, a 10/11, cinco dias antes da entrega, e os mock-ups ficaram por validar (10.2.3).
- **No TP2:** mostrar ao professor os modelos e requisitos à medida que ficam prontos, e registar o que ele disser.

### 8. Declarar o uso de IA
- **No TP1:** a IA só é mencionada nos mock-ups (6.1.3, Claude Design).
- **No TP2:** incluir uma secção que diga que ferramentas foram usadas, para quê (ex.: redação, revisão, diagramas, mock-ups, código) e como o grupo reviu o resultado.

## Outras observações
_Acrescentem aqui o que se lembrarem, com o vosso nome. Exemplo:_
- _(Nome) — o que o professor disse e a que parte do trabalho se refere._
