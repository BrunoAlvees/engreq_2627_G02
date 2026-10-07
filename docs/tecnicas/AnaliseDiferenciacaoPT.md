# Técnica 4: Análise de diferenciação

**Responsável:** Liane Duarte
**Estado:** em curso

## Porquê esta técnica

- A análise de concorrência (técnica 1) e a dinâmica de mercado (técnica 3) mostram **o que já existe**. As entrevistas mostram **o que os stakeholders precisam**. Falta cruzar as duas coisas para perceber **onde a FAIR-AMAP pode oferecer mais valor** do que as soluções existentes.
- Responde à pergunta de negócio: *porque é que uma AMAP como as da BioGoods usaria a FAIR-AMAP em vez de uma plataforma que já existe, ou em vez de continuar com Excel, Google Forms e WhatsApp?*
- Evita duas armadilhas: especificar apenas o que todos os concorrentes já fazem (sem razão para escolher a FAIR-AMAP) ou propor funcionalidades "diferentes" que ninguém pediu.
- Transforma as diferenças encontradas em **requisitos candidatos** e em **perguntas de validação** para as próximas sessões.

## Objetivos

1. **Listar as necessidades** recolhidas nas entrevistas, com a sessão de origem.
2. **Verificar, para cada necessidade, se as soluções existentes a cobrem** (com base na análise de concorrência).
3. **Identificar lacunas**: necessidades que nenhuma solução cobre, ou que cobrem mal para o contexto das AMAP portuguesas.
4. **Propor diferenciações** e convertê-las em **requisitos candidatos**.
5. **Preparar perguntas de validação** para confirmar com os stakeholders se a diferenciação tem valor real.

## Entradas

- Resumos e complementos das sessões de 23/09, 29/09 e 06/10 (`docs/interviews`).
- Matriz de funcionalidades da análise de concorrência (técnica 1, Jakob) e da dinâmica de mercado (técnica 3, João Mata).
- Lista de softwares de exemplo (`docs/ExampleSoftwares.md`): GrownBy, Farmigo, CSAware, Local Food Marketplace.
- Sistema atual descrito pelos stakeholders: Excel, Google Forms, email e WhatsApp (técnica 2, Bruno Alves).

## Método

1. Extrair das entrevistas uma lista de necessidades, cada uma com a sessão de origem e o stakeholder (produtor, coprodutor, cliente).
2. Para cada necessidade, consultar a matriz da análise de concorrência e classificar:
   - **Coberta**: as soluções existentes já resolvem. Passa a requisito base, não diferenciador.
   - **Parcial**: existe, mas não se adapta ao modelo AMAP (ex.: pensado para venda à unidade e não para subscrição de cabaz).
   - **Lacuna**: nenhuma solução analisada resolve.
3. Para as necessidades **parciais** e **lacunas**, preencher a grelha de diferenciação (ver abaixo).
4. Rever as hipóteses iniciais do grupo face ao que as entrevistas mostraram.
5. Levar as perguntas de validação à próxima sessão e atualizar o estado de cada proposta.

### Grelha de diferenciação

Para cada proposta: **necessidade** → **solução existente ou lacuna** → **diferenciação proposta** → **requisito candidato** → **pergunta de validação**.

## Necessidades identificadas até agora

| #   | Necessidade                                                                                                                                    | Origem                               | Cobertura no mercado |
| --- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------ | -------------------- |
| N1  | Saber a composição do cabaz antes da entrega, sem depender de um WhatsApp semanal                                                            | 29/09 (produtor)                     | *a preencher*      |
| N2  | Ver**pessoa a pessoa** o que cada coprodutor recebe, com exclusões (alergias, intolerâncias, gostos) e substituições                 | 29/09 (produtor), 06/10 (coprodutor) | *a preencher*      |
| N3  | Confirmar o levantamento do cabaz, feito pelo próprio coprodutor; hoje o espaço não é vigiado e já ficaram cabazes até ao dia seguinte   | 29/09, 06/10                         | *a preencher*      |
| N4  | Indicar uma ausência e escolher o destino do cabaz entre opções definidas pela AMAP (amigo, doação, distribuição pelos outros, sorteio) | 29/09, 06/10                         | *a preencher*      |
| N5  | Lembretes das datas de entrega                                                                                                                 | 29/09, 06/10                         | *a preencher*      |
| N6  | Consultar o que encomendou e quanto deve; hoje o coprodutor guarda a cópia do formulário e copia as tabelas de preços                       | 06/10 (coprodutor)                   | *a preencher*      |
| N7  | Regras de pagamento diferentes por produtor (antecipado ou com base no que foi efetivamente entregue) na mesma AMAP                            | 06/10                                | *a preencher*      |
| N8  | Reduzir o número de operações de pagamento quando há vários produtores e coprodutores                                                     | 23/09 (cliente)                      | *a preencher*      |
| N9  | Saber quanto pesa o que vai levantar (coprodutores que vão a pé)                                                                             | 06/10                                | *a preencher*      |
| N10 | Receber ofertas pontuais de excedentes, com gestão de quantidades pelo produtor                                                               | 06/10                                | *a preencher*      |
| N11 | Acesso fácil às regras da AMAP                                                                                                               | 06/10                                | *a preencher*      |
| N12 | Renovação antecipada do compromisso (cerca de 3 meses), para planear as culturas                                                             | 29/09 (produtor)                     | *a preencher*      |
| N13 | Duração da subscrição configurável e lista de produtos extra aberta                                                                       | 29/09                                | *a preencher*      |
| N14 | AMAP uniprodutor e multiprodutor; cabazes multiprodutor como cenário ideal                                                                    | 29/09                                | *a preencher*      |
| N15 | Indicadores (KPI) e relatórios para organizações ligadas às CSA e investigadores, alinhados com os ODS                                     | 23/09 (cliente)                      | *a preencher*      |

## Revisão das hipóteses iniciais

O README das técnicas propunha três hipóteses de diferenciação. Face às entrevistas:

| Hipótese                                          | Estado após as entrevistas                                                                                                  | Necessidades relacionadas |
| -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ------------------------- |
| Gestão de exceções nas recolhas                 | **Reforçada.** Os dois stakeholders referiram problemas no levantamento e nas ausências.                             | N3, N4, N5                |
| Equilíbrio sazonal dos cabazes                    | **Enfraquecida.** Na sessão de 29/09, a produtora disse que esta questão provavelmente não tem impacto no software. | —                        |
| Simplificação de pagamentos a vários produtores | **Reforçada.** Cada produtor tem regras próprias e o coprodutor não tem forma simples de saber quanto deve.         | N6, N7, N8                |

## Propostas de diferenciação (rascunho)

As propostas seguintes ainda dependem da análise de concorrência. Não são vantagens competitivas demonstradas nem requisitos acordados.

### D1: Levantamento e ausências

- **Necessidade:** N3, N4, N5.
- **Solução existente ou lacuna:** *a preencher com a análise de concorrência.*
- **Diferenciação proposta:** fluxo completo à volta da entrega: lembrete, aviso de ausência com escolha do destino do cabaz, confirmação de levantamento pelo coprodutor e alerta ao produtor quando um cabaz não é levantado.
- **Requisitos candidatos:**
  - O sistema deve permitir ao coprodutor confirmar o levantamento do cabaz.
  - O sistema deve permitir ao coprodutor indicar uma ausência e escolher o destino do cabaz entre as opções definidas pela AMAP.
  - O sistema deve avisar o produtor dos cabazes não levantados no dia da entrega.
- **Perguntas de validação:** a confirmação deve ser obrigatória? Quem recebe o alerta quando um cabaz não é levantado? O que acontece se ninguém confirmar?

### D2: Pagamentos com vários produtores

- **Necessidade:** N6, N7, N8.
- **Solução existente ou lacuna:** *a preencher com a análise de concorrência.*
- **Diferenciação proposta:** um resumo mensal por coprodutor com o valor devido a cada produtor, calculado segundo as regras de cada um (antecipado ou com base no entregue), e o histórico das encomendas.
- **Requisitos candidatos:**
  - O sistema deve permitir configurar a regra de pagamento de cada produtor.
  - O sistema deve mostrar ao coprodutor o valor a pagar a cada produtor em cada mês.
  - O sistema deve permitir ao coprodutor consultar as encomendas feitas no período.
- **Perguntas de validação:** a AMAP quer centralizar os pagamentos ou manter o pagamento direto a cada produtor? Quem emite a fatura em cada caso?

### D3: Cabaz personalizado e informação antes da entrega

- **Necessidade:** N1, N2, N9.
- **Solução existente ou lacuna:** *a preencher com a análise de concorrência.*
- **Diferenciação proposta:** composição do cabaz publicada pelo produtor e mostrada a cada coprodutor já com as suas exclusões e substituições, e com o peso aproximado.
- **Requisitos candidatos:**
  - O sistema deve permitir ao produtor publicar a composição do cabaz de cada entrega.
  - O sistema deve mostrar a cada coprodutor o seu cabaz, tendo em conta as exclusões registadas.
- **Perguntas de validação:** o peso é útil para todos ou só para alguns coprodutores? O produtor tem tempo para publicar a composição todas as semanas?

## Resultados esperados (evidências)

- Tabela de necessidades com a classificação de cobertura no mercado.
- Grelha de diferenciação preenchida para as necessidades parciais e lacunas.
- Lista de requisitos candidatos diferenciadores.
- Perguntas de validação para a próxima sessão e respetivas respostas.
- Registo de horas por elemento do grupo.

## Registo de trabalho

| Data  | Elemento     | Tarefa                                                                | Horas |
| ----- | ------------ | --------------------------------------------------------------------- | ----- |
| 07/10 | Liane Duarte | Objetivos, método, necessidades das entrevistas e propostas iniciais |       |
