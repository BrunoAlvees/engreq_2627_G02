# 11 Product backlog

**Responsável:** Jakub Piwko · **Atualizado em:** 14/11/2026 · **Estado:** rascunho, funcionalidades 3.1–3.8; story points a acordar pelo grupo (Planning Poker)
**Fontes:** requisitos funcionais da secção 3 e [requisitos/](../requisitos/README.md), critérios de aceitação em [12.4](12.4_AcceptanceCriteriaPT.md), classes de utilizadores em [2.2](2.2_UserClassesPT.md)

Esta secção resume as funcionalidades sob a forma de **user stories**: *Como <classe de utilizadores (2.2)>, quero <objetivo>, para <benefício>*. As stories são numeradas 1, 2, 3… em todo o backlog. Um requisito (N.º RI) pode dar origem a várias stories, e uma story pode cobrir mais do que um requisito. O detalhe de cada story está nos critérios de aceitação dos seus requisitos (anexo 12.4).

**Estimativas.** As stories são estimadas em **story points (SP)** na escala 1, 2, 3, 5, 8. Uma story maior do que 8 SP é dividida em stories mais pequenas. Referência: 1 SP = uma pequena alteração a um ecrã existente; 2 SP = um ecrã simples; 3 SP = um formulário com validação e uma notificação; 5 SP = um fluxo com vários estados, ou regras usadas por outras funcionalidades; 8 SP = a maior story permitida. Para dar a estimativa em horas pedida pelo modelo, **1 SP ≈ 4 horas** de um programador, incluindo conceção, implementação, testes e revisão (referência do grupo, a confirmar).

**Prioridade** usa os valores MoSCoW da secção 1.2. Uma story tem a prioridade do seu requisito, salvo indicação em contrário.

**Versão (caminho do MVP).** O **MVP** é a versão mais pequena com a qual uma AMAP consegue realizar um ciclo de subscrição completo na plataforma durante a experiência piloto em Portugal (E-8): os membros aderem, subscrevem, recebem e levantam os cabazes e pagam. Como regra, as stories Must estão no **MVP**, as Should na **R2** e as Could na **R3**; as exceções são explicadas abaixo de cada tabela.

## 11.1 Funcionalidade 3.1 – Gestão da AMAP e dos membros

| N.º US | N.º RI | User story | SP | Horas | Prior. | Versão |
|---|---|---|---|---|---|---|
| 1 | FR-01 | Como pessoa que gere uma AMAP, quero registar a minha AMAP e enviar os seus documentos (nome, localização, representante, NIF), para que possa ser autorizada. | 3 | 12 | M | MVP |
| 2 | FR-01, FR-06 | Como administrador FAIR, quero verificar os documentos de uma nova AMAP, autorizá-la e atribuir o seu primeiro gestor, para que só AMAP reais usem a plataforma. | 2 | 8 | M | MVP |
| 3 | FR-01 | Como gestão da AMAP, quero definir o local, o dia e a hora de entrega da minha AMAP e o seu número máximo de coprodutores, para que os membros saibam onde e quando levantar. | 2 | 8 | M | MVP |
| 4 | FR-01, NFR-24 | Como gestão da AMAP, quero configurar as regras de funcionamento da minha AMAP (duração do ciclo, prazos de subscrição, opções de ausência e de saída), para que a plataforma siga o modo de funcionamento da minha AMAP. | 5 | 20 | M | MVP |
| 5 | FR-02 | Como interessado, quero ver a página pública de uma AMAP (produtores, local, horário, vagas), para decidir se quero aderir. | 3 | 12 | S | R2 |
| 6 | FR-02 | Como interessado, quero pesquisar todas as AMAP da plataforma por localização, para encontrar uma perto de mim. | 3 | 12 | C | R3 |
| 7 | FR-03, FR-04, FR-05 | Como interessado, quero pedir a adesão a uma AMAP registando-me (nome, email, telefone) e aceitando os seus Termos e o Guia, para que a gestão possa analisar o meu pedido. | 3 | 12 | M | MVP |
| 8 | FR-03 | Como gestão da AMAP, quero aprovar ou rejeitar pedidos de adesão e ver o estado de cada pessoa, para saber quem está na AMAP. | 3 | 12 | M | MVP |
| 9 | FR-03 | Como interessado, quero entrar na lista de espera quando a AMAP está cheia e ser avisado quando abrir uma vaga, para não ter de estar sempre a verificar. | 3 | 12 | M | MVP |
| 10 | FR-03 | Como gestão da AMAP, quero que os novos membros tenham um número configurável de entregas experimentais antes de subscreverem, para que possam experimentar a AMAP primeiro. | 3 | 12 | S | R2 |
| 11 | FR-04, FR-08 | Como produtor, quero um perfil público com a minha localização, produtos e provas do meu modo de produção (certificados ou fotografias), para que os coprodutores confiem nos meus produtos. | 3 | 12 | M | MVP |
| 12 | FR-05 | Como membro, quero dar ou retirar consentimentos opcionais e consultar, exportar, corrigir ou pedir a eliminação dos meus dados, para exercer os meus direitos ao abrigo do RGPD. | 5 | 20 | M | MVP |
| 13 | FR-06 | Como gestão da AMAP, quero atribuir e retirar papéis, podendo uma pessoa ter vários, para que cada pessoa veja apenas o que o seu papel permite. | 5 | 20 | M | MVP |
| 14 | FR-07 | Como coprodutor, quero pertencer a várias AMAP e ver todas as minhas entregas num só calendário, para ter um cabaz todas as semanas. | 3 | 12 | S | R2 |
| 15 | FR-07 | Como coprodutor, quero pedir para sair a meio do período, para que, se a gestão aceitar, as entregas restantes me sejam reembolsadas e os produtores sejam avisados para parar. | 5 | 20 | S | R2 |
| 16 | FR-08 | Como produtor, quero candidatar-me a uma AMAP, ou aceitar o seu convite, com o meu modo de produção e certificados, para que a AMAP me possa avaliar. | 3 | 12 | M | MVP |
| 17 | FR-08 | Como gestão da AMAP, quero registar a visita à quinta e aprovar ou rejeitar um produtor, para que os produtores aprovados fiquem ativos ou entrem na lista de espera. | 3 | 12 | M | MVP |
| 18 | FR-09 | Como produtor, quero anunciar que vou sair de uma AMAP, com o respetivo pré-aviso, para que a gestão e os coprodutores sejam avisados e possam planear. | 3 | 12 | S | R2 |
| 19 | FR-09 | Como gestão da AMAP, quero que o sistema calcule o que cada coprodutor pagou e não recebeu quando um produtor sai, e registar o reembolso ou a compensação, para que ninguém perca dinheiro. | 5 | 20 | S | R2 |
| 20 | FR-10 | Como gestão da AMAP, quero definir uma data de fim para a minha AMAP e exportar primeiro os seus dados, para guardarmos os nossos registos antes de os dados pessoais serem anonimizados. | 3 | 12 | C | R3 |
| 21 | FR-45 | Como gestão da AMAP ou produtor, quero importar membros, subscrições e produtos a partir de um modelo de folha de cálculo, com pré-visualização das linhas que não foi possível ler, para não voltar a introduzir os dados à mão. | 5 | 20 | C | R3 |

**Total da funcionalidade 3.1:** 73 SP ≈ 292 horas · MVP 40 SP (160 h) · R2 22 SP (88 h) · R3 11 SP (44 h).

**Notas:**
- A **story 4** cobre o painel de regras gerais do FR-01. As regras de outras funcionalidades são configuradas nas suas próprias stories (entregas experimentais na story 10, renovação na funcionalidade 3.3), para que nenhuma story ultrapasse 8 SP.
- **Story 10 (S):** o FR-03 é Must, mas as entregas experimentais não foram confirmadas pelo cliente na E-8 (AS-11). A lista de espera (story 9) foi confirmada e fica no MVP.
- Depois da aprovação (story 17), o produtor indica as datas e os produtos que pode entregar através do catálogo (funcionalidade 3.2) e do calendário (funcionalidade 3.4).

## 11.2 Funcionalidade 3.2 – Catálogo e ofertas

| N.º US | N.º RI | User story | SP | Horas | Prior. | Versão |
|---|---|---|---|---|---|---|
| 22 | FR-11 | Como produtor, quero criar, editar e desativar produtos de três tipos (cabaz, extra, pontual), sem lista fechada, para que o meu catálogo corresponda ao que produzo. | 3 | 12 | M | MVP |
| 23 | FR-11 | Como produtor, quero copiar o catálogo do ciclo anterior e ajustar apenas preços e datas, para não o refazer em cada ciclo. | 2 | 8 | M | R2 |
| 24 | FR-12 | Como produtor, quero oferecer vários tipos de cabaz, cada um com nome, descrição, peso aproximado, número de variedades e preço, para que os coprodutores escolham o cabaz que lhes convém. | 3 | 12 | M | MVP |
| 25 | FR-12 | Como produtor, quero acrescentar variantes a um produto (ex.: tamanho, variedade, sem glúten), cada uma com o seu preço, para que os coprodutores não tenham de as pedir em texto livre. | 3 | 12 | M | MVP |
| 26 | FR-13 | Como produtor, quero definir o tipo de preço de cada produto (mensalidade fixa, por unidade, ou por kg com o peso real registado na entrega), para que os coprodutores paguem o valor certo. | 5 | 20 | M | MVP |
| 27 | FR-13 | Como produtor, quero definir a periodicidade de cada produto (quinzenal, mensal, trimestral, pontual, só em certos meses ou em datas escolhidas pelo coprodutor), para que as entregas sigam a minha produção. | 5 | 20 | M | MVP |
| 28 | FR-14 | Como produtor, quero definir quantos coprodutores aceito por produto, para que as subscrições fechem e a lista de espera abra quando atingir o meu limite. | 3 | 12 | M | MVP |
| 29 | FR-15 | Como coprodutor, quero ver a ficha de um produto (descrição, certificação, conservação, origem, preço com IVA), para saber o que estou a comprar. | 2 | 8 | S | R2 |
| 30 | FR-16 | Como produtor, quero publicar uma oferta pontual com a quantidade disponível e um limite por pessoa ou por número de coprodutores, que fecha quando se esgota, para vender os excedentes. | 5 | 20 | S | R2 |

**Total da funcionalidade 3.2:** 31 SP ≈ 124 horas · MVP 22 SP (88 h) · R2 9 SP (36 h).

**Notas:**
- **Story 23 (M, R2):** copiar o catálogo só é necessário a partir do segundo ciclo, por isso não faz parte do MVP, embora o FR-11 seja Must.
- A capacidade da própria AMAP é definida na story 3; a story 28 acrescenta a capacidade por produtor (FR-14, E-8) e reutiliza a lista de espera da story 9.
- Os pontos *(Could)* dos critérios de aceitação do FR-12 e do FR-13 (alternativas, duplicações, desconto nos extras) não entram no backlog até serem validados com o cliente (C9, DV-24).

## 11.3 Funcionalidade 3.3 – Ciclos e subscrições

| N.º US | N.º RI | User story | SP | Horas | Prior. | Versão |
|---|---|---|---|---|---|---|
| 31 | FR-17 | Como gestão da AMAP, quero abrir um ciclo com a sua duração, data de abertura e prazo de subscrição, para que os membros sejam avisados e possam subscrever até ao prazo. | 3 | 12 | M | MVP |
| 32 | FR-18 | Como coprodutor, quero escolher produtos de vários produtores da minha AMAP num só passo, com quantidade e variante, para não preencher um formulário por produtor. | 5 | 20 | M | MVP |
| 33 | FR-18 | Como coprodutor, quero escolher as datas de entrega e as opções estruturadas quando um produto as exige (ex.: carne, avulso em vez de cabaz), para não ter de as escrever em texto livre. | 3 | 12 | M | MVP |
| 34 | FR-18 | Como coprodutor, quero ver um resumo com o valor mensal estimado por produtor e receber uma confirmação, para saber o que encomendei e quanto vou pagar. | 3 | 12 | M | MVP |
| 35 | FR-19, NFR-06 | Como coprodutor, quero registar as minhas exclusões (alergias, intolerâncias, preferências), visíveis apenas para os meus produtores, para que o meu cabaz seja adaptado. | 3 | 12 | M | MVP |
| 36 | FR-19 | Como produtor, quero ver as exclusões dos meus coprodutores e registar a substituição feita, para adaptar cada cabaz. | 2 | 8 | M | MVP |
| 37 | FR-20 | Como gestão da AMAP, quero que os pedidos de subscrição depois do prazo fiquem pendentes até eu os aprovar ou recusar, para que membros atrasados ainda possam entrar quando for possível. | 3 | 12 | S | R2 |
| 38 | FR-20 | Como produtor, quero definir até quando os coprodutores podem alterar a encomenda antes de cada entrega, para que a possam alterar durante o ciclo sem me contactar. | 5 | 20 | S | R2 |
| 39 | FR-21 | Como coprodutor, quero ver as minhas subscrições atuais e o histórico a qualquer momento, para já não precisar da cópia do formulário recebida por email. | 2 | 8 | M | MVP |
| 40 | FR-22 | Como coprodutor, quero ser questionado com antecedência sobre se vou renovar, com a encomenda anterior já preenchida, para que renovar seja um só passo e os produtores possam planear. | 3 | 12 | S | R2 |
| 41 | FR-22 | Como gestão da AMAP, quero escolher se a renovação é uma intenção ou uma confirmação obrigatória até um prazo, após o qual os lugares não confirmados passam para a lista de espera, para que a regra se adapte à minha AMAP. | 3 | 12 | S | R2 |
| 42 | FR-23 | Como produtor, quero ver os totais encomendados por produto, variante, data de entrega e AMAP, para planear a produção e a colheita. | 3 | 12 | M | MVP |

**Total da funcionalidade 3.3:** 38 SP ≈ 152 horas · MVP 24 SP (96 h) · R2 14 SP (56 h).

**Notas:**
- **Stories 32–34:** o FR-18 (subscrever num só passo) é o centro do MVP e ultrapassaria 8 SP numa só story, por isso é dividido em escolher os produtos, escolher datas e opções, e o resumo com confirmação.
- No MVP, as subscrições fecham simplesmente no prazo definido na story 31; os pedidos atrasados (story 37) e as alterações à encomenda durante o ciclo (story 38) ficam para a R2.
- **Stories 40–41 (R2):** a renovação só é necessária no fim do primeiro ciclo, e o modo de renovação ainda está por validar (DV-12).

## 11.4 Funcionalidade 3.4 – Calendário e entregas

| N.º US | N.º RI | User story | SP | Horas | Prior. | Versão |
|---|---|---|---|---|---|---|
| 43 | FR-24 | Como gestão da AMAP, quero que as datas de distribuição do ciclo sejam criadas a partir do dia e da hora da AMAP, e alterar datas isoladas (ex.: feriados), para que todos saibam quando há distribuição. | 3 | 12 | M | MVP |
| 44 | FR-24 | Como produtor, quero definir as minhas datas de entrega no ciclo, dentro do horário de distribuição da AMAP, com a minha periodicidade, datas específicas por produto e modo de entrega, para que os coprodutores saibam quando entrego. | 5 | 20 | M | MVP |
| 45 | FR-24 | Como coprodutor, quero ver num só calendário as datas de entrega de todos os produtores a quem compro, para saber o que chega em cada data. | 3 | 12 | M | MVP |
| 46 | FR-25 | Como produtor, quero publicar a composição do cabaz antes de cada entrega, para deixar de a enviar por WhatsApp. | 3 | 12 | M | MVP |
| 47 | FR-25 | Como coprodutor, quero ver o que vou levantar em cada data, de todos os produtores, já com as minhas exclusões e o peso aproximado, para planear como levo tudo para casa. | 3 | 12 | M | MVP |
| 48 | FR-26 | Como produtor, quero confirmar a disponibilidade de um produto antes da entrega, para que os coprodutores afetados sejam avisados a tempo. | 3 | 12 | M | MVP |
| 49 | FR-26 | Como produtor, quero registar as faltas e a compensação dada (desconto ou substituição), para que os coprodutores não paguem o que não receberam. | 3 | 12 | M | MVP |
| 50 | FR-26 | Como produtor, quero registar a quantidade ou o peso real entregue a cada coprodutor (ex.: carne), para que os produtos vendidos ao kg sejam cobrados corretamente. | 2 | 8 | M | MVP |
| 51 | FR-27 | Como coprodutor, quero indicar uma ausência, escolher o destino do meu cabaz entre as opções da AMAP e indicar quem o levanta, para que o cabaz não se perca e o produtor seja avisado. | 3 | 12 | M | MVP |
| 52 | FR-28 | Como coprodutor, ou quem levanta em seu nome, quero confirmar o levantamento com um botão na aplicação, para que o produtor saiba que o cabaz foi levantado. | 2 | 8 | M | MVP |
| 53 | NFR-12 | Como coprodutor num ponto de levantamento com rede fraca, quero que a minha confirmação fique guardada no telemóvel e seja enviada mais tarde, para não ter de esperar por rede. | 3 | 12 | C | R3 |
| 54 | FR-28 | Como produtor, quero que o sistema lembre quem ainda não confirmou e assinale os cabazes não levantados no fim do horário de distribuição, para eu saber no próprio dia. | 3 | 12 | M | MVP |
| 55 | FR-28 | Como voluntário, gestão da AMAP ou produtor, quero confirmar um levantamento em nome de um coprodutor sem telemóvel, para que todos os levantamentos fiquem registados. | 2 | 8 | M | MVP |
| 56 | FR-29 | Como gestão da AMAP, quero imprimir a folha de distribuição de cada data em PDF A4, com o que cada coprodutor leva de cada produtor, para que a distribuição funcione sem telemóveis. | 3 | 12 | S | R2 |
| 57 | FR-29, FR-28 | Como produtor com impressora, quero folhas A4 de etiquetas para os sacos, cada uma com um código QR, para que os coprodutores confirmem lendo o código e sejam avisados se o saco não for o seu. | 5 | 20 | S | R2 |

**Total da funcionalidade 3.4:** 46 SP ≈ 184 horas · MVP 35 SP (140 h) · R2 8 SP (32 h) · R3 3 SP (12 h).

**Notas:**
- A story 43 baseia-se no dia, hora e local da AMAP definidos na story 3; a story 45 mostra uma AMAP, e a story 14 (R2) alarga-a a várias AMAP.
- **Stories 52–55:** o FR-28 é o único requisito desta funcionalidade validado pelo cliente (E-8): o botão na aplicação é essencial, por isso está no MVP; as etiquetas com QR (story 57) são opcionais (E-8).
- A **story 53** vem do NFR-12, que é Could e ainda é uma ideia a avaliar durante a implementação.

## 11.5 Funcionalidade 3.5 – Pagamentos

| N.º US | N.º RI | User story | SP | Horas | Prior. | Versão |
|---|---|---|---|---|---|---|
| 58 | FR-30 | Como gestão da AMAP, quero escolher que métodos de pagamento do prestador estão disponíveis (ex.: MB Way, referência Multibanco, cartão), para que os membros paguem da forma a que já estão habituados. | 2 | 8 | M | MVP |
| 59 | FR-30, NFR-17 | Como produtor, quero associar a conta onde recebo a minha parte, para ser pago diretamente pelo prestador de pagamentos. | 3 | 12 | M | MVP |
| 60 | FR-30 | Como produtor, quero definir quando cada produto é cobrado (antecipadamente para o ciclo, mensalmente, ou depois da entrega ou da pesagem), para que os pagamentos sigam o meu modo de venda. | 3 | 12 | M | MVP |
| 61 | FR-31 | Como coprodutor, quero que o sistema calcule o meu valor em cada período (mensalidades dos cabazes + extras + produtos pesados − faltas compensadas), discriminado por produtor, para saber exatamente quanto devo. | 5 | 20 | M | MVP |
| 62 | FR-31 | Como coprodutor, quero receber o pedido de pagamento e ver o total, a discriminação por produtor e o meu histórico de pagamentos numa só vista, para deixar de copiar os preços para uma nota. | 3 | 12 | M | MVP |
| 63 | FR-32, NFR-19 | Como coprodutor, quero fazer um único pagamento online por período, registado automaticamente quando o prestador o confirma, para não pagar a cada produtor separadamente. | 5 | 20 | M | MVP |
| 64 | FR-32, NFR-19 | Como produtor, quero que o prestador divida cada pagamento pelos produtores e mostre as comissões descontadas, para receber a minha parte sem que a plataforma guarde o dinheiro. | 3 | 12 | M | MVP |
| 65 | FR-32 | Como gestão da AMAP, quero registar pagamentos feitos fora da plataforma (ex.: numerário), para que o estado de cada membro esteja correto. | 2 | 8 | M | MVP |
| 66 | FR-33 | Como gestão da AMAP ou produtor, quero ver o estado de pagamento de cada coprodutor e ser avisado dos pagamentos em atraso, para os poder acompanhar. | 3 | 12 | M | MVP |
| 67 | FR-33 | Como produtor, quero um resumo por período de quem pagou, quanto, quando e o que cobre, para deixar de fazer as contas em Excel. | 3 | 12 | M | MVP |
| 68 | FR-34 | Como administrador FAIR, quero definir o modelo de preços (valor mínimo por AMAP mais uma percentagem, que pode ser zero durante a experiência piloto) e ver o valor de cada AMAP, para que a FAIR possa cobrar pela plataforma. | 3 | 12 | C | R3 |

**Total da funcionalidade 3.5:** 35 SP ≈ 140 horas · MVP 32 SP (128 h) · R3 3 SP (12 h).

**Notas:**
- **Stories 63–64:** o FR-32 (cobrança centralizada, validada na E-8) é dividido no pagamento do coprodutor e na divisão pelos produtores. A divisão é feita pelo prestador de pagamentos licenciado (NFR-19); as stories cobrem apenas a integração.
- A faturação está fora do âmbito (E-6, NFR-18), por isso não há stories de faturação.
- **Story 68 (C, R3):** a plataforma é quase gratuita durante a experiência piloto (E-8), por isso as cobranças da FAIR não são necessárias no MVP.

## 11.6 Funcionalidade 3.6 – Comunicação e notificações

| N.º US | N.º RI | User story | SP | Horas | Prior. | Versão |
|---|---|---|---|---|---|---|
| 69 | FR-35 | Como coprodutor, quero um lembrete antes de cada entrega, com a antecedência definida pela minha AMAP, que mostre o que vou levantar, para não me esquecer do cabaz. | 3 | 12 | M | MVP |
| 70 | FR-35, NFR-15 | Como utilizador, quero ser avisado automaticamente dos eventos que me dizem respeito (abertura de ciclo, novas ofertas, composição do cabaz, alterações de datas, faltas, cabaz não levantado, pedido de pagamento), para não ter de consultar a aplicação. | 5 | 20 | M | MVP |
| 71 | FR-36 | Como gestão da AMAP, quero enviar um aviso a todos os membros ou a um grupo (ex.: só produtores), para deixar de depender dos grupos de WhatsApp. | 3 | 12 | M | MVP |
| 72 | FR-37 | Como produtor, quero trocar mensagens com um coprodutor e escrever a todos os meus coprodutores, para responder às perguntas num só lugar. | 5 | 20 | S | R2 |
| 73 | FR-37 | Como produtor, quero publicar notícias da produção no meu perfil, enviadas aos meus coprodutores e associáveis a um produto em falta, para que percebam porque falta um produto. | 3 | 12 | S | R2 |
| 74 | FR-38, NFR-15 | Como utilizador, quero escolher se recebo as notificações por email, push ou ambos, para as receber onde as leio. | 3 | 12 | S | R2 |
| 75 | FR-38, NFR-15 | Como utilizador, quero receber notificações individuais no WhatsApp através da API oficial do WhatsApp Business, para as receber na aplicação que mais uso. | 5 | 20 | C | R3 |

**Total da funcionalidade 3.6:** 27 SP ≈ 108 horas · MVP 11 SP (44 h) · R2 11 SP (44 h) · R3 5 SP (20 h).

**Notas:**
- A **story 70** constrói o mecanismo comum de notificações (email no MVP); as outras stories (ex.: 9, 31, 48, 54) apenas definem quando é enviada uma notificação.
- **Story 75 (C):** o FR-38 é Should, mas o WhatsApp é opcional nos seus critérios de aceitação e depende da API do WhatsApp Business (DE-04).

## 11.7 Funcionalidade 3.7 – Comunidade e organização

| N.º US | N.º RI | User story | SP | Horas | Prior. | Versão |
|---|---|---|---|---|---|---|
| 76 | FR-39, FR-05 | Como membro, quero encontrar os Termos e Condições, o Guia e a Carta de Princípios em vigor, com as versões que aceitei guardadas, para conhecer sempre as regras em vigor. | 3 | 12 | M | MVP |
| 77 | FR-40 | Como gestão da AMAP, quero criar grupos de trabalho, atribuir membros e definir as suas tarefas, para que o trabalho voluntário esteja organizado. | 3 | 12 | C | R3 |
| 78 | FR-40 | Como coprodutor, quero inscrever-me numa escala de distribuição e receber um lembrete, para que a distribuição tenha sempre voluntários. | 5 | 20 | C | R3 |
| 79 | FR-40 | Como gestão da AMAP, quero convocar assembleias e reuniões e partilhar as atas, para que todos os membros possam participar e estar informados. | 3 | 12 | C | R3 |
| 80 | FR-41 | Como gestão da AMAP ou produtor, quero criar eventos (ex.: visitas à quinta, workshops) com inscrição dos membros, para que a comunidade se encontre para além das entregas. | 3 | 12 | C | R3 |
| 81 | FR-41 | Como gestão da AMAP, quero recolher a opinião dos coprodutores sobre a qualidade, a variedade, o horário e o formato das entregas, para que a AMAP possa melhorar. | 3 | 12 | C | R3 |

**Total da funcionalidade 3.7:** 20 SP ≈ 80 horas · MVP 3 SP (12 h) · R3 17 SP (68 h).

**Nota:** as stories 77–78 ainda têm de ser validadas com o cliente (DV-14): os grupos de trabalho e as escalas só aparecem no antigo Guia da AMAP Porto (D-C).

## 11.8 Funcionalidade 3.8 – Relatórios e indicadores

| N.º US | N.º RI | User story | SP | Horas | Prior. | Versão |
|---|---|---|---|---|---|---|
| 82 | FR-42, NFR-16 | Como produtor, quero exportar encomendas e entregas para CSV ou XLSX, filtradas por ciclo, data, AMAP e produto, para continuar a trabalhar nas minhas folhas de cálculo. | 3 | 12 | S | R2 |
| 83 | FR-43 | Como gestão da AMAP, quero ver indicadores sociais (coprodutores, pessoas alimentadas, produtores apoiados, retenção entre ciclos), para reportar aos projetos financiados. | 3 | 12 | C | R3 |
| 84 | FR-43 | Como gestão da AMAP, quero ver indicadores ambientais (ex.: quilómetros percorridos, CO2, desperdício evitado), para mostrar os benefícios da AMAP. | 5 | 20 | C | R3 |
| 85 | FR-44, FR-05 | Como gestão da AMAP, quero exportar dados para organizações da rede e investigadores, apenas anonimizados ou de membros que deram consentimento, para que a investigação seja possível sem violar o RGPD. | 5 | 20 | C | R3 |

**Total da funcionalidade 3.8:** 16 SP ≈ 64 horas · R2 3 SP (12 h) · R3 13 SP (52 h).

**Nota:** a story 84 precisa de dados que a plataforma ainda não recolhe (ex.: distâncias), por isso a sua estimativa é a menos segura.

## 11.9 Resumo

| Funcionalidade | Stories | SP | Horas | MVP | R2 | R3 |
|---|---|---|---|---|---|---|
| 3.1 Gestão da AMAP e dos membros | 1–21 | 73 | 292 | 40 | 22 | 11 |
| 3.2 Catálogo e ofertas | 22–30 | 31 | 124 | 22 | 9 | 0 |
| 3.3 Ciclos e subscrições | 31–42 | 38 | 152 | 24 | 14 | 0 |
| 3.4 Calendário e entregas | 43–57 | 46 | 184 | 35 | 8 | 3 |
| 3.5 Pagamentos | 58–68 | 35 | 140 | 32 | 0 | 3 |
| 3.6 Comunicação e notificações | 69–75 | 27 | 108 | 11 | 11 | 5 |
| 3.7 Comunidade e organização | 76–81 | 20 | 80 | 3 | 0 | 17 |
| 3.8 Relatórios e indicadores | 82–85 | 16 | 64 | 0 | 3 | 13 |
| **Total** | **85** | **286** | **1144** | **167 SP (668 h)** | **67 SP (268 h)** | **52 SP (208 h)** |

**Caminho do MVP.** O MVP (167 SP ≈ 668 h) segue o ciclo de subscrição: a AMAP é autorizada e configurada (3.1) → os produtores preparam o catálogo (3.2) → a gestão abre um ciclo e os coprodutores subscrevem (3.3) → os cabazes são entregues e levantados (3.4) → os coprodutores pagam uma só vez e os produtores recebem a sua parte (3.5), com lembretes e avisos (3.6) e as regras da AMAP disponíveis (3.7). A R2 torna o ciclo mais fácil de repetir (renovação, cópia do catálogo, alterações à encomenda, mensagens); a R3 acrescenta funcionalidades de comunidade e de relatórios.

**Não incluído:** a base técnica comum a todas as stories (preparação do projeto, autenticação, instalação da PWA, alojamento e cópias de segurança, traduções; ex.: NFR-01, NFR-05, NFR-11, NFR-13). O grupo deve decidir se a acrescenta como stories separadas.
