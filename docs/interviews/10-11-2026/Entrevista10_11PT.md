# FAIR-AMAP - Entrevista com stakeholders de 10/11

**Atualizado em:** 10/11/2026 · Fonte nos requisitos: **E-8**

Este documento resume a entrevista feita na aula PL de 10/11/2026 (30 minutos). O professor fez o papel dos stakeholders: **representante da FAIR** (cliente) e **gestão de uma AMAP**. O guião está em [PerguntasEntrevista10_11PT](PerguntasEntrevista10_11PT.md).

A informação foi registada durante a entrevista. Os pontos pouco claros estão assinalados como "a confirmar".

## 1. Representante da FAIR

### 1.1. Modelo de negócio
- Está prevista uma **experiência piloto em Portugal**, em que o software é disponibilizado de forma **quase gratuita**, para recolher feedback. O número de AMAP em Portugal não chega para justificar o negócio.
- No futuro, a FAIR pensa cobrar uma **fee mínima por cada AMAP** mais uma **percentagem do valor das transações**.
- As transações são **pagamentos aos produtores**.

### 1.2. Pagamentos
- O grupo propôs receber os pagamentos através de um prestador (tipo Stripe) e distribuí-los pelos produtores. O cliente **aceitou** a proposta.
- As **taxas dos meios de pagamento** (ex.: MB Way) são um **custo do produtor**: os preços que define já devem contemplar essa estrutura de custos.
- Em alternativa, a taxa pode ser **descontada no valor transferido** ao produtor, desde que isso seja **transparente**.

### 1.3. Entrada de uma AMAP na plataforma
- O software deve funcionar para **várias AMAP**, cada uma com as suas próprias regras.
- A AMAP **regista-se** e alguém da FAIR que gere o sistema **pede documentação**: nome da AMAP, localização, representante, NIF, etc. Depois de submetida, o registo fica feito.

## 2. Gestão da AMAP

### 2.1. Entrada de um produtor
- O produtor pode **candidatar-se** ou ser **convidado**. Quem é convidado é convidado a candidatar-se, já com a seleção praticamente feita.
- A candidatura é uma página onde o produtor indica:
  - nome e localização;
  - os produtos que o caracterizam e os mais importantes;
  - o modo de produção (biológico ou não).
- Pode carregar documentos, por exemplo o certificado de produção biológica, Demeter, GRASP ou GlobalG.A.P. *(nomes a confirmar)*.
- Estes elementos servem para a **gestão da AMAP avaliar** a candidatura. Tipicamente há uma **visita** às instalações e depois o produtor é selecionado ou não.
- O produtor selecionado passa a **produtor ativo**.
- O processo pode variar de AMAP para AMAP, mas há sempre um **registo de produtor**.
- **AMAP criada por um produtor:** regista a AMAP. Depois de a AMAP ser autorizada, ele fica com os papéis de **gestor e produtor**: candidata-se como produtor e aceita a candidatura como gestor.
- Um produtor pode estar em **várias AMAP**.

### 2.2. Vagas e capacidade
- O limite de vagas aplica-se **sobretudo aos coprodutores**.
- Os produtores podem estar registados como ativos ou não. Uma candidatura aceite, de um produtor ou de um coprodutor, pode passar a **ativa** ou ficar em **lista de espera** se não houver vagas.
- A capacidade existe **a dois níveis**:
  - A **AMAP** pode ter uma capacidade máxima (ex.: 100), que depende das instalações, da capacidade de transporte e do espaço.
  - **Cada produtor** diz quantos coprodutores aceita. Exemplo: um produtor de fruta entrega 25 cabazes e outro mais 30, por isso 55 coprodutores podem subscrever fruta.

### 2.3. Saída de um produtor
- É **muito pouco comum**.
- **No fim de um período de subscrição:** o produtor deixa de estar ativo.
- **A meio de um período:** deixa de fazer entregas, as entregas previstas são **canceladas** e as **contas têm de ser acertadas** (devolução).

### 2.4. Saída de um coprodutor
- A regra é sair **no fim do período de subscrição**, mas em certas circunstâncias pode sair antes.
- A desistência **tem de ser aceite**. Se for aceite, os produtores com quem o coprodutor tinha subscrições (ex.: cabaz de legumes por 6 meses) são **informados** para deixarem de fazer entregas, e os **pagamentos são devolvidos**.
- O que acontece se não for aceite **depende de quão formal é a AMAP** *(resposta pouco clara; a confirmar)*.
- Na prática, recusar é muito estranho numa AMAP, que se rege por princípios de correção e coerência. Quem sai fá-lo normalmente porque vai para o estrangeiro. Muitos coprodutores são **expatriados**, estudantes fora do país ou **nómadas digitais** que já usavam AMAP no país de origem. Ninguém os leva a tribunal: comunicam, os produtores são avisados e fica tudo bem.

### 2.5. Documentos assinados na entrada
- **Depende da AMAP.** Algumas (ex.: a da Sara) usam documentos que são **quase contratos**, assinados em papel. Quem desiste e já pagou não recebe o dinheiro de volta. Não é para levar a tribunal, mas é um compromisso.
- Nas AMAP mais informais, como as do Porto, isso não acontece.

### 2.6. Ferramentas dos produtores
- **Depende muito do produtor.** Os maiores podem ter software de apoio à produção; outros não terão grande coisa.

### 2.7. Confirmação de levantamento e etiquetas
- No Porto há sempre uma **etiqueta com o nome**. Umas vezes é **impressa**, outras **escrita à mão** (como a do cabaz da Luisa).
- **Essencial:** a aplicação deve permitir **comunicar o recebimento** do cabaz.
- **Opcional:** quem tem impressora imprime a etiqueta com o nome e um **QR code**, que se lê para confirmar o levantamento. Quem não tem impressora confirma só **carregando num botão** na aplicação.

## 3. Impacto nos requisitos
| Tema | Requisitos | Alteração |
|---|---|---|
| Modelo de cobrança | FR-34, NFR-21 | Fee mínima **por AMAP** (era por produtor) + % das transações; piloto quase gratuito. Validado. |
| Pagamento centralizado e taxas | FR-32, NFR-19 | Aceite pela FAIR; taxas são custo do produtor ou descontadas de forma transparente. Validado. |
| Registo de uma AMAP | FR-01, FR-06 | Registo com documentação, autorizado pelo administrador FAIR. |
| Entrada de produtor | FR-04, FR-08, PA-01, PA-03 | Candidatura ou convite, documentos de certificação, visita típica, avaliação pela gestão. PA-01 e PA-03 respondidas. |
| AMAP criada por um produtor | FR-06 | O produtor fica com os papéis de gestão e produtor. |
| Capacidade | FR-01, FR-14 | Capacidade da AMAP + capacidade por produtor. |
| Saída de produtor | FR-09, PA-04 | Fim do período: inativo. A meio: cancelar entregas e acertar contas. PA-04 respondida em parte. |
| Saída de coprodutor | FR-07 | Só no fim do período; a meio, se a desistência for aceite (com devolução e aviso aos produtores); regras configuráveis por AMAP. |
| Levantamento | FR-28, FR-29 | Botão na aplicação obrigatório; etiqueta com QR opcional. Validado. |

## 4. Perguntas que ficaram por fazer
- Ao **produtor** (não foi entrevistado): antecedência para planear, faltas de produto, compensação quando um produtor sai, aviso prévio para sair (PA-04), quando cobra cada produto (DV-18 a DV-20), mudança de preço a meio do ciclo e cancelamento de entregas (DV-17).
- À **gestão**: renovação (intenção ou confirmação obrigatória), verificação de pagamentos e atrasos, quem monta o formulário de encomenda e o calendário (DV-07, DV-08), entregas experimentais pagas e entrada a meio do ciclo (DV-01, DV-03, DV-05), app ou link e rede no ponto de entrega (DV-28), voluntários e cabazes por levantar (DV-14, DV-15), registo de alergias na aplicação (FR-19), adesão só a produtos de outros produtores (DV-04), confirmação da encomenda ao coprodutor (DV-10).
- À **FAIR**: prazo de conservação dos dados depois da saída (PA-04), PA-02 (ciclo e compromisso), compatibilidade do pagamento centralizado com a Carta de Princípios (C6), contrato ou período de experiência e suporte dado às AMAP, metas de desempenho (NFR-02, NFR-10).
