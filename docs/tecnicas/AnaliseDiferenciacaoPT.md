# Técnica 4: Análise de diferenciação

**Momento:** iniciada antes da elicitação (preparar entrevistas), depois da análise de concorrência; concluída depois da última sessão com o cliente (10/11)
**Responsável:** Liane Duarte
**Estado:** concluída

## Porquê esta técnica

- A análise de concorrência (técnica 1) e a dinâmica de mercado (técnica 3) mostram **o que já existe**. As entrevistas mostram **o que os stakeholders precisam**. Falta cruzar as duas coisas para perceber **onde a FAIR-AMAP pode oferecer mais valor** do que as soluções existentes.
- Responde à pergunta de negócio: *porque é que uma AMAP como as da BioGoods usaria a FAIR-AMAP em vez de uma plataforma que já existe, ou em vez de continuar com Excel, Google Forms e WhatsApp?*
- Evita duas armadilhas: especificar apenas o que todos os concorrentes já fazem (sem razão para escolher a FAIR-AMAP) ou propor funcionalidades "diferentes" que ninguém pediu.
- Transforma as diferenças encontradas em **requisitos candidatos** e em **perguntas de validação**.

## Objetivos

1. **Listar as necessidades** recolhidas nas entrevistas, com a sessão de origem.
2. **Verificar, para cada necessidade, se as soluções existentes a cobrem** (com base na análise de concorrência).
3. **Identificar lacunas**: necessidades que nenhuma solução cobre, ou que cobrem mal para o contexto das AMAP portuguesas.
4. **Propor diferenciações** e convertê-las em **requisitos candidatos**.
5. **Preparar perguntas de validação** para confirmar com os stakeholders se a diferenciação tem valor real.

## Entradas

- Resumos e complementos das sessões de 23/09, 29/09 e 06/10 e a entrevista de 10/11 (E-8) (`docs/interviews`).
- Documentos analisados (`docs/doc_AMAP`): [formulário de encomendas da AMAP Porto Baixa](../doc_AMAP/FormularioEncomendas_AMAPPortoBaixa_PT.md) e [reportagem do Público sobre a AMAP Porto](../doc_AMAP/ReportagemPublico_AMAPPorto_PT.md).
- Matriz de funcionalidades da análise de concorrência ([técnica 1](CompetitorAnalysis.md), Jakub Piwko): AMAPJ, Juntagrico, Katuma (Open Food Network) e Local Line, e as lacunas de mercado identificadas. A dinâmica de mercado ([técnica 3](MarketDynamic.md), João Mata) ainda não tem resultados, por isso não foi usada.
- Soluções de exemplo (secção «Other solutions considered» da [técnica 1](CompetitorAnalysis.md)): GrownBy, Farmigo, CSAware e Local Food Marketplace. Os sites foram consultados a 11/11/2026 (ver "Soluções de exemplo" abaixo).
- Sistema atual descrito pelos stakeholders: Excel, Google Forms, email e WhatsApp (técnica 2, Bruno Alves).
- Lista final de requisitos ([requisitos](../requisitos/README.md)): FR-01 a FR-45 e NFR-01 a NFR-24.

## Método

1. Extrair das entrevistas uma lista de necessidades, cada uma com a sessão de origem e o stakeholder (produtor, coprodutor, cliente).
2. Para cada necessidade, consultar a matriz da análise de concorrência e os sites das soluções de exemplo, e classificar a cobertura:
   - **Coberta**: pelo menos uma das soluções analisadas tem a funcionalidade. Passa a requisito base, não diferenciador.
   - **Parcial**: existe, mas não se adapta ao modelo AMAP (ex.: pensado para venda à unidade e não para subscrição de cabaz, ou para um só produtor).
   - **Não referida**: a funcionalidade não aparece na técnica 1 nem nos sites consultados. É tratada como lacuna provável, mas não demonstrada (ver "Limitações").
3. Para as necessidades **parciais** e **não referidas**, preencher a grelha de diferenciação (ver abaixo).
4. Rever as hipóteses iniciais do grupo face ao que as entrevistas mostraram.
5. Levar as perguntas de validação às sessões seguintes e registar as respostas. As que ficaram sem resposta depois da última sessão (10/11) passam a decisão do grupo, coerente com as secções 2.5 e 10.4 do SRS.
6. Ligar cada proposta aos requisitos finais.

### Grelha de diferenciação

Para cada proposta: **necessidade** → **solução existente ou lacuna** → **diferenciação proposta** → **requisitos** → **validação**.

## Soluções de exemplo

Os sites das quatro soluções de exemplo foram consultados a 11/11/2026, para completar a matriz da técnica 1. A informação vem só do que cada site publica.

| | GrownBy | Farmigo | CSAware | Local Food Marketplace |
|---|---|---|---|---|
| **O que é** | App de venda direta das explorações aos consumidores, de uma cooperativa de agricultores | Software de gestão de CSA, para explorações, herdshares e food hubs | Software de gestão de CSA e food hubs, da LocalHarvest | Software para food hubs, explorações e CSA |
| **País e língua** | EUA, inglês | EUA (provável), inglês | EUA, inglês | EUA, inglês |
| **Subscrições** | Partilhas por época, personalizáveis, com preço por levantamento | Partilhas fixas ou personalizáveis; quinzenais, por época ou anuais | Partilhas fixas ou personalizáveis | Subscrições contínuas ou por época, partilhas personalizáveis |
| **Personalização** | Extras (ovos, carne, cogumelos) | Pausas, trocas, mudança do ponto de levantamento, extras, oferta de cabazes | Lista de produtos a evitar, extras, pausa da subscrição | Trocas, extras, cabazes compostos |
| **Levantamento** | Ponto de levantamento por subscrição | Vários pontos, listas de presença no dia, listas de preparação | Etiquetas e folhas de assinatura, listas de preparação, pontos com capacidade | Listas de preparação, etiquetas, rotas de entrega |
| **Comunicação** | Não indicado | Não detalhado | Newsletters, blogue, SMS com lembretes | Email "What's in the Box", lembretes de renovação, SMS |
| **Capacidade** | Não indicado | Limite de inscrições e lista de espera | Capacidade por ponto de levantamento | Não indicado |
| **Pagamentos** | Online, SNAP/EBT | ACH, cartão, cheque, débito automático | Cartão, PayPal, eCheck, SNAP | Cartão, e-check; pagamento automático aos produtores (Stripe), no modelo de food hub |
| **Vários produtores** | Marketplace com várias explorações, cada uma com a sua loja | Não referido | Não referido | Food hub que vende produtos de vários produtores |
| **Preço** | Não indicado | 2% das vendas, mínimo 150$/mês | 2% das vendas, mínimo 100$/mês | 129$ a 349$/mês, mais módulos extra |

**O que mostram:** as funcionalidades de gestão de subscrições (extras, trocas, pausas, lembretes, composição do cabaz, capacidade) já são comuns no mercado americano. Nenhuma das quatro está em português, refere a Europa ou o RGPD, aceita MB Way, ou junta vários produtores numa mesma CSA com um só pagamento sem intermediário. As que mostram preço cobram uma percentagem das vendas com um mínimo mensal, ou uma mensalidade fixa.

## Necessidades e cobertura no mercado

Tipo: **Base** (requisito esperado em qualquer solução, sem valor diferenciador) · **Diferenciação** (a FAIR-AMAP pode fazer melhor do que as soluções analisadas).

| # | Necessidade | Origem | Cobertura no mercado | Tipo | Requisitos |
|---|---|---|---|---|---|
| N1 | Saber a composição do cabaz antes da entrega, sem depender de um WhatsApp semanal | 29/09 (produtor) | Coberta: emails "What's in the Box" (Local Food Marketplace) | Base | FR-25 |
| N2 | Ver **pessoa a pessoa** o que cada coprodutor recebe, com exclusões (alergias, intolerâncias, gostos) e substituições | 29/09 (produtor), 06/10 (coprodutor) | Parcial: lista de produtos a evitar (CSAware) e trocas (Farmigo, Local Food Marketplace); alergias e a vista pessoa a pessoa para o produtor não são referidas | Diferenciação (D3) | FR-19, FR-25, NFR-06 |
| N3 | Confirmar o levantamento do cabaz, feito pelo próprio coprodutor; hoje o espaço não é vigiado e já ficaram cabazes até ao dia seguinte | 29/09, 06/10, 10/11 | Parcial: listas de presença (Farmigo), folhas de assinatura e etiquetas (CSAware), distribuições (AMAPJ, Juntagrico); a confirmação pelo coprodutor na aplicação não é referida | Diferenciação (D1) | FR-28, FR-29, NFR-12 |
| N4 | Indicar uma ausência e escolher o destino do cabaz entre opções definidas pela AMAP (amigo, doação, distribuição pelos outros, sorteio) | 29/09, 06/10 | Parcial: pausas e mudança do ponto de levantamento (Farmigo, CSAware); escolher o destino do cabaz não é referido | Diferenciação (D1) | FR-27 |
| N5 | Lembretes das datas de entrega | 29/09, 06/10 | Coberta: lembretes por SMS (CSAware, Local Food Marketplace) | Base | FR-35 |
| N6 | Consultar o que encomendou e quanto deve; hoje o coprodutor guarda a cópia do formulário e copia as tabelas de preços | 06/10 (coprodutor), formulário | Parcial: contratos (AMAPJ) e saldos em dívida (CSAware), mas por exploração | Diferenciação (D2) | FR-21, FR-31 |
| N7 | Regras de pagamento diferentes por produtor e até por produto (mensal com nota de pagamento, a cada entrega, carne só depois de pesada) na mesma AMAP | 06/10, formulário | Parcial: o AMAPJ tem o papel de tesoureiro e as outras soluções pagamentos online, pensados para uma exploração; regras diferentes por produtor na mesma AMAP não são referidas | Diferenciação (D2) | FR-30, FR-31, NFR-24 |
| N8 | Reduzir o número de operações de pagamento quando há vários produtores e coprodutores | 23/09 (cliente) | Parcial: o Local Food Marketplace paga os produtores automaticamente, mas no modelo de food hub, em que o hub é o vendedor; um só pagamento dividido por vários produtores sem intermediário não é referido. MB Way não é aceite por nenhuma | Diferenciação (D2) | FR-32, FR-33, NFR-17, NFR-19 |
| N9 | Saber quanto pesa o que vai levantar (coprodutores que vão a pé) | 06/10 | Não referida | Diferenciação (D3) | FR-25 |
| N10 | Receber ofertas pontuais de excedentes, com gestão de quantidades pelo produtor | 06/10 | Coberta: lojas de extras ligadas à subscrição (Farmigo, CSAware, Local Food Marketplace, GrownBy) | Base | FR-16 |
| N11 | Acesso fácil às regras da AMAP | 06/10 | Não referida | Base | FR-39 |
| N12 | Renovação antecipada do compromisso (cerca de 3 meses), para planear as culturas | 29/09 (produtor) | Coberta: contratos por época (AMAPJ), subscrições (Juntagrico, Local Line) e lembretes de renovação (Local Food Marketplace) | Base | FR-22 |
| N13 | Duração da subscrição configurável e lista de produtos extra aberta | 29/09 | Coberta: contratos (AMAPJ), subscrições por época, quinzenais ou anuais (Farmigo), extras (todas) | Base | FR-11, FR-17 |
| N14 | AMAP uniprodutor e multiprodutor; cabazes multiprodutor como cenário ideal | 29/09 | Coberta: o AMAPJ tem contratos e o papel de referente por produtor, e o Katuma e o Local Food Marketplace juntam vários produtores num hub. Os cabazes multiprodutor ficaram fora do âmbito | Base | FR-01 |
| N15 | Indicadores (KPI) e relatórios para organizações ligadas às CSA e investigadores, alinhados com os ODS; a AMAP Porto já fez um levantamento de quantas pessoas alimenta | 23/09 (cliente), reportagem | Não referida | Diferenciação (pedido do cliente, prioridade baixa) | FR-43, FR-44 |
| N16 | Capacidade limitada por produto e por AMAP e lista de espera para novos membros | formulário, 10/11 | Parcial: limite de inscrições e lista de espera (Farmigo), capacidade por ponto de levantamento (CSAware); capacidade por produtor na mesma AMAP não é referida | Diferenciação (D4) | FR-03, FR-14 |
| N17 | Encomendar de forma estruturada o que hoje vai para os comentários livres: outras quantidades, datas parciais (ex.: frango), produtos avulsos em vez de cabaz, preferências | formulário | Coberta em parte: partilhas personalizáveis, trocas e extras (Farmigo, CSAware, Local Food Marketplace); escolher as datas de cada produto não é referido | Base, com regras por produtor (D4) | FR-18, FR-20 |
| N18 | Os produtores indicarem as entregas em que vão falhar ou em que o produto não é garantido (pão, cogumelos), e pedirem reconfirmação de encomendas pouco frequentes (azeite) | formulário | Não referida | Diferenciação (D4) | FR-20, FR-24, FR-26 |
| N19 | Manter a relação pessoal entre produtores e coprodutores; o software não deve tornar a AMAP impessoal | 06/10, reportagem | Parcial: AMAPJ e Juntagrico focam a organização; Katuma, Local Line, GrownBy e Local Food Marketplace seguem a lógica de loja ou de food hub, e a técnica 1 conclui que comissões sobre os cabazes chocam com a ética das AMAP | Diferenciação (D5) | FR-04, FR-37, FR-40, NFR-20 |

Além destas necessidades, a técnica 1 identificou **lacunas de mercado** que não vieram das entrevistas, mas que reforçam a diferenciação (D6): interface em português (só o Katuma a tem), pagamento por MB Way, uma instância partilhada por todas as AMAP portuguesas e pouco esforço exigido aos produtores. As soluções de exemplo confirmam estas lacunas: são todas americanas, em inglês, com meios de pagamento dos EUA.

## Revisão das hipóteses iniciais

O README das técnicas propunha três hipóteses de diferenciação. Face às entrevistas e à sessão de 10/11:

| Hipótese | Estado final | Necessidades relacionadas |
|---|---|---|
| Gestão de exceções nas recolhas | **Confirmada.** Os dois stakeholders referiram problemas no levantamento e nas ausências, e a gestão da AMAP disse em 10/11 que é essencial o coprodutor confirmar o levantamento na aplicação. As soluções analisadas tratam as pausas, mas não o destino do cabaz nem a confirmação pelo coprodutor. | N3, N4, N5 |
| Equilíbrio sazonal dos cabazes | **Abandonada.** Na sessão de 29/09, a produtora disse que esta questão provavelmente não tem impacto no software. | — |
| Simplificação de pagamentos a vários produtores | **Confirmada.** Cada produtor tem regras próprias e o coprodutor não tem forma simples de saber quanto deve. Em 10/11, a FAIR aceitou a cobrança centralizada. | N6, N7, N8 |

## Propostas de diferenciação

A cobertura indicada vem da técnica 1 e das soluções de exemplo. A validação indica a resposta obtida ou, quando não houve resposta, a decisão do grupo.

### D1: Levantamento e ausências

- **Necessidade:** N3, N4 (N5 é base).
- **Solução existente ou lacuna:** as soluções têm listas para quem distribui (listas de presença no Farmigo, folhas de assinatura e etiquetas no CSAware) e permitem pausar a subscrição. Nenhuma refere a confirmação do levantamento pelo próprio coprodutor nem a escolha do destino do cabaz numa ausência (amigo, doação, partilha, sorteio).
- **Diferenciação proposta:** fluxo completo à volta da entrega, do lado do coprodutor: lembrete, aviso de ausência com escolha do destino do cabaz, confirmação de levantamento na aplicação e aviso ao produtor quando um cabaz não é levantado. Funciona em locais sem ninguém a vigiar.
- **Requisitos:** FR-27 (ausências), FR-28 (confirmação de levantamento), FR-29 (folha de distribuição e etiquetas), FR-35 (lembretes), NFR-12 (confirmação com rede fraca).
- **Validação:**
  - *A confirmação deve ser obrigatória?* **Respondida (E-8):** é essencial que o coprodutor possa comunicar o levantamento na aplicação, com um botão. A etiqueta com QR code é opcional, para quem tem impressora.
  - *Quem recebe o alerta? O que acontece se ninguém confirmar?* Sem resposta. **Decisão do grupo:** o sistema assinala os cabazes não levantados ao produtor e à gestão (FR-28).

### D2: Pagamentos com vários produtores

- **Necessidade:** N6, N7, N8.
- **Solução existente ou lacuna:** as soluções analisadas recebem pagamentos online para uma exploração. O Local Food Marketplace paga vários produtores, mas no modelo de food hub, em que o hub vende os produtos, o que faria da plataforma um intermediário, excluído pela Carta de Princípios das AMAP. Nenhuma aceita MB Way.
- **Diferenciação proposta:** o coprodutor faz um só pagamento por período, calculado segundo as regras de cada produtor e dividido pelos produtores através de um prestador de pagamentos licenciado, sem a plataforma vender nem guardar o dinheiro. O coprodutor vê o que deve a cada produtor e o histórico das encomendas, e cada produtor recebe um resumo de quem pagou.
- **Requisitos:** FR-21 (histórico), FR-30 (regras de pagamento), FR-31 (cálculo por produtor), FR-32 (pagamento único dividido), FR-33 (acompanhamento), NFR-17 (prestador de pagamentos), NFR-19 (o sistema não guarda o dinheiro), NFR-20 (sem intermediação comercial).
- **Validação:**
  - *A AMAP quer centralizar os pagamentos?* **Respondida (E-8):** a FAIR aceitou a cobrança centralizada; as taxas do meio de pagamento são um custo do produtor ou são descontadas de forma transparente.
  - *Quem emite a fatura?* **Respondida (E-6):** a faturação está fora do âmbito; cada produtor fatura no seu programa (NFR-18).

### D3: Cabaz personalizado e informação antes da entrega

- **Necessidade:** N2, N9 (N1 é base).
- **Solução existente ou lacuna:** publicar a composição do cabaz já existe (emails "What's in the Box" no Local Food Marketplace) e o CSAware tem uma lista de produtos a evitar. As alergias, a vista pessoa a pessoa para o produtor e o peso não são referidos.
- **Diferenciação proposta:** composição do cabaz mostrada a cada coprodutor já com as suas exclusões e substituições, e lista para o produtor do que cada pessoa recebe. As alergias são tratadas como dados de saúde.
- **Requisitos:** FR-19 (exclusões e substituições), FR-25 (composição do cabaz), NFR-06 (dados de saúde só com consentimento).
- **Validação:** *o peso é útil para todos? O produtor tem tempo para publicar a composição?* Sem resposta, porque o produtor não foi entrevistado na última sessão. **Decisão do grupo:** a composição do cabaz é requisito (FR-25); o peso aproximado não passou a requisito próprio. Esta diferenciação é fraca: a parte principal já existe no mercado.

### D4: Encomendas flexíveis e capacidade

- **Necessidade:** N16, N18 (N10 e N17 são base).
- **Solução existente ou lacuna:** extras, trocas e partilhas personalizáveis já são comuns (Farmigo, CSAware, Local Food Marketplace, GrownBy), e o Farmigo tem limite de inscrições com lista de espera. Não são referidas a capacidade por produtor na mesma AMAP, as regras diferentes de cada produtor (prazos de alteração, datas parciais) nem a indicação, pelo produtor, das entregas em que falha.
- **Diferenciação proposta:** a parte comum (extras, trocas, lista de espera) é base. A diferença está no que é próprio de uma AMAP com vários produtores: capacidade da AMAP e de cada produtor, regras de alteração de cada produtor, calendário do produtor com as entregas em que falha ou em que o produto não é garantido, e pedidos de reconfirmação.
- **Requisitos:** FR-03 (adesão e lista de espera), FR-14 (capacidade), FR-16 (ofertas pontuais), FR-18 (subscrição estruturada), FR-20 (prazos e alterações), FR-24 (calendário), FR-26 (disponibilidade e faltas).
- **Validação:**
  - *Quem gere a lista de espera?* **Respondida (E-8):** a capacidade existe a dois níveis, da AMAP e de cada produtor; uma candidatura aceite passa a ativa ou vai para a lista de espera; a gestão aceita os membros.
  - *Que pedidos aparecem nos comentários? Como se atribuem os excedentes? Com que antecedência o produtor sabe que vai falhar?* Sem resposta. **Decisão do grupo:** as regras ficam configuráveis por produtor (FR-20, NFR-24) e o produtor regista as faltas quando as conhece (FR-26).

### D5: Software que mantém a relação pessoal

- **Necessidade:** N19.
- **Solução existente ou lacuna:** o AMAPJ e o Juntagrico focam a organização, e o Juntagrico coordena o trabalho voluntário. O Katuma, o Local Line, a GrownBy e o Local Food Marketplace seguem a lógica de loja ou de food hub (catálogo, carrinho, comissões), que a técnica 1 considera contrária à ética das AMAP. O Farmigo e o CSAware são ferramentas de gestão de uma exploração, sem organização voluntária.
- **Diferenciação proposta:** tratar a relação pessoal como princípio de desenho e não como funcionalidade: o software trata da gestão (encomendas, pagamentos, ausências) para libertar tempo para o contacto direto, mostra quem é o produtor, permite-lhe comunicar com os seus coprodutores e apoia a organização voluntária da AMAP, sem atuar como intermediário comercial.
- **Requisitos:** FR-04 (perfil do produtor), FR-37 (comunicação do produtor), FR-40 (organização voluntária), NFR-20 (sem intermediação comercial). As exclusões ficam registadas por escolha do coprodutor e só visíveis ao produtor (FR-19, NFR-06).
- **Validação:** *as exclusões devem ficar no sistema? O que tornaria a AMAP impessoal? Preferem manter o WhatsApp?* Sem resposta. **Decisão do grupo:** registo das exclusões com consentimento e visível só ao produtor (FR-19, NFR-06); o WhatsApp mantém-se como canal possível (NFR-15, Could). Na sessão de 10/11, a gestão reforçou que as AMAP se regem por princípios de correção e confiança, o que é coerente com esta proposta.

### D6: Plataforma portuguesa, partilhada e acessível

- **Necessidade:** lacunas de mercado da técnica 1 e pedido do cliente de servir várias AMAP (E-8).
- **Solução existente ou lacuna:** só o Katuma tem interface em português, e é uma plataforma de loja. As ferramentas de organização (AMAPJ, Juntagrico) não estão em português, e a técnica 1 aponta como lacuna não haver uma instância partilhada pelas AMAP portuguesas. As soluções comerciais são americanas, em inglês, com meios de pagamento dos EUA, e cobram 2% das vendas com um mínimo de 100$ a 150$ por mês (Farmigo, CSAware), uma mensalidade de 129$ a 349$ (Local Food Marketplace) ou a partir de 79$ por mês (Local Line). Para uma AMAP de 30 a 50 coprodutores, estes custos são altos.
- **Diferenciação proposta:** uma só plataforma em português para várias AMAP, cada uma com as suas regras, com MB Way e cumprimento do RGPD, quase gratuita na fase piloto e com uma fee por AMAP depois, que importa os dados que já existem e exige pouco tempo aos produtores.
- **Requisitos:** NFR-13 (português europeu), NFR-22 (multi-AMAP), NFR-24 (regras configuráveis), NFR-17 (prestador de pagamentos, ex.: MB Way), NFR-08 (RGPD), NFR-21 (modelo de cobrança e piloto), FR-45 (importação de dados), NFR-02 (tarefas rápidas).
- **Validação:** **Respondida em parte (E-8):** a FAIR quer servir várias AMAP com regras próprias e prevê um piloto quase gratuito em Portugal. As metas de tempo (NFR-02) não foram validadas e ficam como proposta do grupo.

### Ideias vistas nas soluções de exemplo

Algumas funcionalidades das soluções de exemplo não estão nos requisitos. Não foram validadas com os stakeholders e ficam registadas para uma próxima iteração:
- trocas de produtos feitas pelo próprio coprodutor (o FR-19 prevê a substituição feita pelo produtor);
- mudar o ponto de levantamento numa data;
- oferecer um cabaz a outra pessoa.

## Conclusões

**O que é base** (já existe nas soluções analisadas e a FAIR-AMAP tem de ter, mas não a distingue): ciclos e contratos com duração configurável, catálogo e extras, trocas e partilhas personalizáveis, composição do cabaz antes da entrega, renovação, lista de espera, vários produtores por AMAP, papéis, lembretes e acesso às regras (N1, N5, N10 a N14, N17).

**O que diferencia a FAIR-AMAP:**
1. **Plataforma em português, partilhada por várias AMAP, configurável e acessível** (D6). Todas as soluções analisadas, exceto o Katuma, estão só em inglês, e as comerciais cobram uma percentagem das vendas ou uma mensalidade alta para uma AMAP pequena.
2. **Um só pagamento dividido por vários produtores, sem intermediário** (D2). Nenhuma solução analisada o faz sem atuar como vendedor, e foi aceite pela FAIR.
3. **Levantamento e ausências do lado do coprodutor** (D1): confirmação do levantamento na aplicação e escolha do destino do cabaz. As soluções analisadas só têm listas para quem distribui e pausas.
4. **Regras de vários produtores na mesma AMAP** (D4): capacidade por produtor, regras de alteração e faltas de cada produtor.
5. **Ferramenta de organização e não loja**, que mantém a relação pessoal e apoia a organização voluntária (D5).

O cabaz personalizado (D3) e os indicadores (N15) têm valor, mas a parte principal do D3 já existe no mercado e os dois dependem de validação com produtores que não foi possível fazer.

Estas conclusões alimentam o âmbito do projeto (secção 1.3 do SRS) e o resumo das técnicas (secção 10.2).

## Limitações

- A cobertura vem da matriz da técnica 1 e dos sites das soluções de exemplo, a partir de informação pública. "Não referida" quer dizer que a funcionalidade não é mencionada, e não que a solução não a tenha. Nenhuma solução foi testada por dentro.
- O site da GrownBy mostra sobretudo a loja para consumidores; as funcionalidades para as explorações e o preço não estão na página principal.
- Na sessão de 10/11 não houve entrevista a um produtor, por isso as perguntas de D3 e parte de D4 ficaram sem resposta (ver secção 10.4 do SRS).

## Resultados (evidências)

- Tabela de necessidades com a cobertura no mercado e o tipo (base ou diferenciação).
- Comparação das soluções de exemplo.
- Grelha de diferenciação preenchida (D1 a D6), com os requisitos finais.
- Respostas às perguntas de validação e decisões do grupo.
- Conclusões sobre a diferenciação da FAIR-AMAP.
- Registo de horas por elemento do grupo.

## Registo de trabalho

| Data | Elemento | Tarefa | Horas |
|---|---|---|---|
| 30/09 | Liane Duarte | Pesquisa de exemplos de software parecido (GrownBy, Farmigo, CSAware, Local Food Marketplace) | 0.5 |
| 07/10 | Liane Duarte | Objetivos, método, necessidades das entrevistas e propostas iniciais | 2.0 |
| 14/10 | Liane Duarte | Sincronização PT/EN, classificação provisória de N10–N19, propostas D4 e D5 | 1.0 |
| 11/11 | Liane Duarte | Análise dos sites das soluções de exemplo, cobertura de N1–N19, respostas da E-8, ligação aos requisitos finais, proposta D6, conclusões e limitações | 2.5 |
