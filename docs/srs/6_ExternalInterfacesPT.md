# 6 Requisitos de interfaces externas

**Responsável:** Leonor Marinho · **Atualizado em:** 12/11/2026 · **Estado:** atualizado com a E-8, para revisão
**Fontes:** [NFR](../requisitos/RNF_AtributosQualidadePT.md) §1 e §6, [diagrama de contexto](../requisitos/diagramas/DiagramaContextoPT.md), ficheiros de funcionalidades [RF01–RF08](../requisitos/README.md); códigos de fonte em [requisitos/README.md](../requisitos/README.md)

Esta secção descreve como a FAIR-AMAP se liga aos seus **utilizadores** (6.1), a outro **software** (6.2), a **hardware** (6.3) e aos **canais de comunicação** (6.4). Os requisitos propriamente ditos estão no ficheiro dos NFR; aqui são apenas referenciados (`NFR-nn`) e explicados. As escolhas de interface que nenhum stakeholder confirmou estão marcadas como *Proposto* ou *A validar*.

## 6.1 Interfaces com o utilizador

### 6.1.1 Características gerais

| # | Característica | Requisitos relacionados | Fonte | Estado |
|---|---|---|---|---|
| UI-1 | **Aplicação web responsiva** para telemóvel e computador, sem nada para instalar. Pode ser adicionada ao ecrã principal do telemóvel como **PWA**, e a própria aplicação explica como (Android e iPhone) e como ativar as notificações. | NFR-01 | E-3, decisão do grupo de 21/10 | Proposto |
| UI-2 | **Mobile first.** Os coprodutores usam o telemóvel no ponto de entrega e em pé (E-3 §10); os produtores e a gestão da AMAP usam tanto o telemóvel como o computador. | NFR-01 | E-3, E-2 | Proposto |
| UI-3 | **Língua:** português europeu, preparado para outras línguas. Valores em euros com IVA, datas no formato dd/mm/aaaa, fuso horário de Portugal. | NFR-13, NFR-14 | CA, D-A | Proposto |
| UI-4 | **Acessibilidade:** WCAG 2.1 nível AA. | NFR-03 | Hip. | A validar |
| UI-5 | **Rapidez das tarefas principais:** um coprodutor que já tenha usado o sistema subscreve um ciclo em 10 minutos ou menos, e vê o que vai levantar e o que deve a menos de 2 cliques da página inicial. | NFR-02 | Hip. (valores) | A validar |
| UI-6 | **Os perfis veem ecrãs diferentes.** Cada utilizador só vê o que o seu perfil permite; a mesma pessoa pode ter vários perfis (por exemplo, coprodutor e membro de um grupo de trabalho). | NFR-04, FR-06 | D-B §3.1, E-1 §3.2 | Proposto |
| UI-7 | **Contactos sempre visíveis** entre produtores e coprodutores, para que a aplicação não substitua a relação pessoal. | princípio 2 (brainstorm de 14/10), N19 | E-3, D-D | Proposto |
| UI-8 | **Mensagens de erro e de confirmação** em linguagem simples, que dizem o que fazer a seguir, e cada subscrição ou encomenda termina com uma confirmação que o utilizador pode consultar mais tarde (hoje é a cópia do formulário enviada por email). | FR-18, FR-21 | E-3 §2 | Proposto |
| UI-9 | **Dados sensíveis** (alergias e intolerâncias) nunca aparecem nas folhas ou etiquetas impressas, que só mostram o nome e as substituições feitas. | NFR-06, FR-29 | E-2 §4, RGPD art. 9.º | A validar |

### 6.1.2 Ecrãs principais por classe de utilizador

| Classe de utilizador | Ecrã | O que mostra ou permite fazer | Requisitos |
|---|---|---|---|
| Candidato a membro | **Página pública da AMAP / portal de AMAP** | Produtores e como produzem, local e dia de entrega, regras, vagas livres; botão para pedir adesão (ou entrar na lista de espera) | FR-02, FR-03, FR-04 |
| Coprodutor | **Início** | Próxima entrega (data, local, o que vai levantar, peso aproximado), valor em dívida, lembretes pendentes | FR-21, FR-25, FR-31, FR-35 |
| Coprodutor | **Subscrever um ciclo** | Produtos de todos os produtores da AMAP num só formulário, com opções, data-limite e confirmação no fim | FR-17, FR-18, FR-19 |
| Coprodutor | **Ausência** | Comunicar uma ausência, escolher o que acontece ao cabaz entre as opções definidas pela AMAP, indicar quem o levanta | FR-27 |
| Coprodutor | **Levantamento** | Confirmar o levantamento do cabaz com um **botão** (obrigatório, também com rede fraca); opcionalmente, ler o código QR da etiqueta do saco | FR-28, FR-29, NFR-12 |
| Coprodutor | **Pagamentos** | Valor por produtor e por período, um só pagamento, histórico | FR-31, FR-32, FR-21 |
| Produtor | **Cabaz e catálogo** | Gerir o catálogo, publicar o conteúdo do próximo cabaz, publicar ofertas pontuais | FR-11 a FR-16, FR-25 |
| Produtor | **Planeamento e entregas** | Totais encomendados e preferências agregadas; registar faltas, compensações e quantidades efetivamente entregues | FR-23, FR-26 |
| Gestão da AMAP | **Calendário e distribuição** | Calendário de entregas por produtor, folha de distribuição imprimível e etiquetas dos sacos, cabazes por levantar | FR-24, FR-28, FR-29 |
| Gestão da AMAP | **Membros e pagamentos** | Pedidos de adesão e lista de espera, perfis, avisos aos membros, estado dos pagamentos e pagamentos em atraso | FR-03, FR-06, FR-33, FR-36 |
| Administrador da FAIR | **Administração da plataforma** | Criar e configurar AMAP, suporte, encargos da FAIR | FR-01, FR-34 |

### 6.1.3 Esboços de interface

Esboços de baixa fidelidade (em texto) de três ecrãs-chave. Mostram apenas o conteúdo e a ordem, não o desenho final. Devem ser substituídos por imagens quando o grupo tiver uma ferramenta de design.

**Início do coprodutor (telemóvel)**

```
┌──────────────────────────────┐
│ FAIR-AMAP      AMAP Baixa  ≡ │
├──────────────────────────────┤
│ Próxima entrega              │
│ Terça-feira 18/11 · 17:30-19:30 │
│ UPTEC, Porto                 │
│                              │
│ Vai levantar:                │
│  • Cabaz da quinta (~4 kg)   │
│     – sem pimentos → cenouras│
│  • Ovos ×1 dúzia             │
│  Total ≈ 5 kg                │
│                              │
│ [ Não posso levantar ]       │
├──────────────────────────────┤
│ Valor em dívida este mês     │
│ 32,00 €        [ Pagar ]     │
├──────────────────────────────┤
│ Início · Encomendas · Pagar · Contactos│
└──────────────────────────────┘
```

**Subscrever um ciclo (telemóvel)**

```
┌──────────────────────────────┐
│ Jan–Jun 2027 · fecha a 04/12 │
├──────────────────────────────┤
│ BioGoods                     │
│  (•) Cabaz da quinta 32 €/mês│
│  ( ) Cabaz de fruta          │
│  [ ] Ovos                    │
│ Quinta da Serrinha           │
│  [ ] Azeite                  │
│ Exclusões: [ pimentos      ] │
├──────────────────────────────┤
│ Total por mês: 32,00 €       │
│ [ Confirmar subscrição ]     │
└──────────────────────────────┘
```

**Produtor: registar uma entrega (telemóvel ou computador)**

```
┌──────────────────────────────┐
│ Entrega 18/11 · AMAP Baixa   │
├──────────────────────────────┤
│ Conteúdo do cabaz [ editar ] │
│  cenouras, batatas, couve ...│
│ Há ovos?         (•) Sim     │
│                  ( ) Não     │
│ Faltas / compensação:        │
│  [ ______________________ ]  │
│ [ Guardar e avisar membros ] │
└──────────────────────────────┘
```

> Os nomes dos produtos e os valores nos esboços são exemplos retirados das entrevistas (cabaz de cerca de 4 kg, 32 € por mês, entrega às terças-feiras); não são requisitos.

## 6.2 Interfaces de software

| # | Interface | Direção e dados | Finalidade | Requisitos relacionados | Estado |
|---|---|---|---|---|---|
| SI-1 | **Prestador de pagamentos licenciado** (por exemplo, Stripe; MB Way como meio de pagamento), capaz de dividir um pagamento por vários produtores | Saída: pedido de pagamento com valores por produtor. Entrada: confirmação e estado do pagamento | Um pagamento por coprodutor por período, sem o sistema guardar o dinheiro. As comissões dos meios de pagamento são um custo do produtor ou são deduzidas de forma transparente do valor transferido (E-8) | NFR-17, NFR-19, FR-32, FR-33 | Validado (E-8) |
| SI-2 | **Serviço de email** | Saída: notificações, lembretes e avisos. Entrada: estado de entrega (opcional) | Lembretes, confirmações, avisos da gestão | NFR-15, FR-35, FR-36 | Proposto |
| SI-3 | **Web push** através da PWA | Saída: notificações push para telemóveis | As mesmas notificações no telemóvel, quando o utilizador as ativa. **No iPhone, o push só funciona se a PWA estiver instalada no ecrã principal**; caso contrário, o utilizador só recebe email | NFR-01, NFR-15 | Proposto |
| SI-4 | **WhatsApp Business API** (ou SMS) | Saída: mensagens individuais (não um bot num grupo) | Canal opcional, porque o WhatsApp é o canal usado hoje | NFR-15 *(Could)* | Ideia |
| SI-5 | **Exportação para folha de cálculo** (CSV/XLSX) | Saída: encomendas, entregas e pagamentos | Para quem trabalha hoje em Excel | NFR-16, FR-42 | Proposto |
| SI-6 | **Geração de PDF** (A4) | Saída: folha de distribuição e etiquetas dos sacos | Impressos no ponto de distribuição. A etiqueta com o nome pode ter um **código QR opcional**, lido para confirmar o levantamento (E-8) | FR-28, FR-29 | Proposto |
| SI-7 | **Exportação de dados anonimizados** para organizações da rede e investigadores | Saída: dados anonimizados, ou dados de membros que deram consentimento | Relatórios e indicadores | FR-44, FR-05 | Proposto |
| SI-8 | **Importação de dados existentes** de folhas de cálculo (CSV/XLSX) e de respostas de formulários | Entrada: membros, subscrições e produtos que já estão em Excel e Google Forms | Evitar que cada AMAP tenha de reintroduzir tudo à mão quando começa a usar a plataforma | FR-45, pressuposto DE-08 em [2.5](2.5_PressupostosDependenciasPT.md) | Ideia |

**Fora do âmbito:** software de faturação. O sistema não emite faturas; cada produtor mantém a faturação no seu próprio software (NFR-18, E-6), pelo que não existe interface com esse software.

## 6.3 Interfaces de hardware

A FAIR-AMAP é uma aplicação web e **não tem interface direta com hardware específico**. Funciona nos próprios dispositivos dos utilizadores:

- **Telemóveis e tablets** (Android e iPhone), com um navegador atual, para a PWA, as notificações push e a confirmação do levantamento (NFR-01, NFR-12).
- **Computadores** com um navegador atual, para a gestão e os produtores.
- **Impressoras** (A4) para a folha de distribuição e as etiquetas dos sacos (FR-29). O sistema apenas gera o PDF. Nem todos os produtores têm impressora, pelo que imprimir é opcional (E-8).
- **Câmara do telemóvel** (opcional), para ler o código QR da etiqueta do saco e confirmar o levantamento. O docente chamou-lhe "uma funcionalidade gira" (E-8). Quem não tem impressora ou não lê o código toca apenas no botão da aplicação (FR-28).

## 6.4 Interfaces de comunicação

| # | Requisito | Requisitos relacionados | Estado |
|---|---|---|---|
| CI-1 | Todo o tráfego entre navegador, aplicação e servidores usa **HTTPS/TLS**. | NFR-05 | Proposto |
| CI-2 | As notificações seguem por **email**, **web push** e, opcionalmente, **WhatsApp/SMS**. O utilizador escolhe os canais. | NFR-15, FR-38 | Proposto |
| CI-3 | A integração com o prestador de pagamentos usa a **API segura** (HTTPS) do prestador. Os dados de cartão ou bancários **nunca são guardados** pela FAIR-AMAP. | NFR-17, NFR-19, FR-32 | Proposto |
| CI-4 | A confirmação do levantamento funciona com **rede fraca**: fica guardada no telemóvel e é enviada quando houver ligação. | NFR-12 | Ideia |
| CI-5 | Os dados pessoais nas mensagens limitam-se ao necessário; os dados de saúde **nunca** são enviados por email, push ou WhatsApp. | NFR-06, NFR-08 | A validar |
| CI-6 | Os objetivos de rapidez das páginas (2 segundos ou menos para 95% dos pedidos) aplicam-se à comunicação entre o utilizador e o servidor. | NFR-10 | A validar |

## Pontos em aberto

- **Prestador de pagamentos e canais:** o cliente aceitou a cobrança através de um prestador como o Stripe (E-8, pelo que a C6 está resolvida). Continua em aberto: que prestador e se o MB Way é oferecido como meio, e que canais querem os coprodutores (muitos usam hoje o WhatsApp).
- **Esboços de interface:** são suficientes para o SRS, ou o docente espera maquetas? A perguntar na próxima sessão.
- **Novos identificadores:** `UI-n`, `SI-n` e `CI-n` são locais a esta secção. Se o grupo preferir, podem passar a `NFR-nn` (o próximo número livre é NFR-25), atualizando PT e EN.
