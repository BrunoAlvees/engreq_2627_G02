# 1 Introdução

**Responsável:** Liane Duarte · **Atualizado em:** 11/11/2026 · **Estado:** rascunho para revisão
**Fontes:** [requisitos/README.md](../requisitos/README.md) (convenções), [interviews/](../interviews/), [doc_AMAP/](../doc_AMAP/), [tecnicas/](../tecnicas/)

> **Nota para o Word:** no template do Word os títulos são numerados automaticamente, por isso os números abaixo servem só de referência. Os links para ficheiros do repositório passam a texto simples (ex.: "ver secção 2.5"). O SRS é entregue em inglês: o texto a colar é o da versão EN.

## 1.1 Objetivo

Este documento especifica os requisitos de software da FAIR-AMAP, versão 1.0, uma plataforma web de apoio à organização e ao funcionamento do dia a dia das AMAP (Associações para a Manutenção da Agricultura de Proximidade), também conhecidas como CSA (Community Supported Agriculture). O produto é especificado para a FAIR Software Solutions, uma startup que pretende disponibilizar software para a distribuição e venda de produtos alimentares alinhado com os Objetivos de Desenvolvimento Sustentável (ODS) da Agenda 2030. A FAIR-AMAP não cria AMAP. Apoia as AMAP que já existem em tarefas que hoje são feitas com folhas de cálculo, formulários online, email e aplicações de mensagens: adesões, subscrições, entregas, pagamentos e comunicação entre produtores e coprodutores. Este SRS cobre toda a versão 1.0: as oito funcionalidades da secção 3, os requisitos de dados e de qualidade e as interfaces externas.

Os requisitos foram levantados através de entrevistas com stakeholders e da análise de documentos, de soluções concorrentes e do mercado. Este documento destina-se aos seguintes leitores:
- **FAIR Software Solutions (cliente):** confirmar que a solução especificada corresponde aos seus objetivos de negócio e às decisões de âmbito que tomou.
- **Stakeholders (produtores, coprodutores e gestão da AMAP):** verificar que os requisitos refletem o funcionamento das suas AMAP e aquilo de que precisam.
- **Gestores de projeto:** planear e estimar o desenvolvimento, a partir do product backlog da secção 11.
- **Programadores e designers:** compreender as funcionalidades, os dados, as restrições e os atributos de qualidade que o sistema tem de cumprir.
- **Testers:** derivar casos de teste dos requisitos funcionais e dos atributos de qualidade quantificados.

## 1.2 Convenções do documento

**Redação dos requisitos.** Cada requisito é uma frase verificável, escrita como "O sistema deve…" ("The system shall…" na versão inglesa). Os requisitos funcionais estão em tabelas com as colunas **ID · Requisito · Ator · Prioridade**.

**Identificadores.**
- `FR-nn`: requisitos funcionais (FR-01 a FR-45), numerados de seguida pela ordem das funcionalidades da secção 3.
- `NFR-nn`: requisitos não funcionais (NFR-01 a NFR-24), nas secções 2.4, 6, 7, 8 e 9.
- As funcionalidades identificam-se pelo número da secção (3.1 a 3.8).
- `AS-nn` e `DE-nn`: pressupostos e dependências (secção 2.5). `L-n`: limitações da elicitação (secção 10.4).

**Prioridade (MoSCoW).**

| Código | Significado |
|---|---|
| **M** | Must: obrigatório na primeira versão |
| **S** | Should: importante, mas a solução funciona sem ele |
| **C** | Could: desejável, se houver tempo |

O que fica fora do âmbito está indicado na secção 1.3.

**Estado.** As secções 2.4, 6 e 10.4 indicam até que ponto um requisito ou restrição foi confirmado, com os valores seguintes. A secção 2.5 usa valores próprios para os pressupostos.

| Estado | Significado |
|---|---|
| Proposto | Tem fonte, mas não foi validado com o cliente; inclui as decisões do grupo sobre perguntas que não foi possível fazer (secção 10.4) |
| A validar | Depende de uma dúvida em aberto, indicada junto ao estado |
| Ideia | Proposta do grupo a avaliar na implementação |
| Validado | Confirmado pelo cliente ou por um stakeholder, com a fonte |

**Fontes.** As secções 2.4, 2.5, 6, 10 e o anexo 12.3 indicam as suas fontes com os códigos abaixo. As sessões estão detalhadas no anexo 12.3; as outras fontes estão nas referências da secção 1.4.

| Código | Fonte |
|---|---|
| E-1 a E-8 | Sessões com stakeholders e indicações do professor nas aulas (lista em 12.3.1) |
| D-A a D-F | Documentos da AMAP Porto e da rede nacional de AMAP (referências [3] a [8]) |
| DOC-nn | Requisitos candidatos da análise documental [26] |
| CA | Análise de concorrência [25] |
| N01 a N19 | Necessidades da análise de diferenciação [28] |
| C1 a C9, DV-nn | Diferenças entre fontes e dúvidas sobre os processos atuais [26] |
| PA-nn | Perguntas em aberto ao cliente (repositório [24]) |
| Hip. | Hipótese do grupo, sem fonte de stakeholder |

**Termos.** "AMAP" e "CSA" usam-se como sinónimos. Um **coprodutor** é um consumidor que subscreve os produtos de uma AMAP; um **produtor** é um agricultor ou transformador que os fornece; a **gestão da AMAP** é a pessoa, comissão ou grupo de trabalho que organiza a AMAP. Os outros termos estão definidos no glossário (anexo 12.1).

**Tipografia e datas.** O negrito assinala termos e decisões importantes. As datas escrevem-se dd/mm/aaaa (ou dd/mm quando o ano é 2026).

## 1.3 Âmbito do projeto

A FAIR-AMAP é uma plataforma web, que também se pode instalar no telemóvel (PWA), para ajudar as AMAP que já existem a organizar o seu trabalho. Cada AMAP mantém as suas regras: a plataforma serve várias AMAP independentes, cada uma com um ou vários produtores, e as diferenças entre elas resolvem-se por configuração.

**Problema.** Hoje os produtores e a gestão gerem cada AMAP com folhas de cálculo, formulários online e mensagens de WhatsApp. O peso não está num processo difícil, mas no **número de pequenas tarefas**: abrir e fechar encomendas, confirmá-las, lembrar as datas de entrega, acompanhar os pagamentos e saber quem levantou o cabaz.

**Objetivos.**
- Reduzir o trabalho manual dos produtores e da gestão da AMAP em cada ciclo de subscrição.
- Dar aos coprodutores informação clara sobre o que encomendaram, o que vão levantar, quando e quanto devem.
- Simplificar os pagamentos: o coprodutor faz um só pagamento por período, dividido pelos produtores através de um prestador de pagamentos licenciado.
- Manter a relação direta entre produtores e coprodutores, que é central nas AMAP: a plataforma simplifica o processo, mas não substitui esse contacto.

**Funcionalidades principais** (secção 3):
1. Gestão da AMAP e dos membros (3.1)
2. Catálogo e ofertas (3.2)
3. Ciclos e subscrições (3.3)
4. Calendário e entregas (3.4)
5. Pagamentos e faturação (3.5): cálculo, cobrança e acompanhamento dos pagamentos; as faturas continuam a ser emitidas por cada produtor
6. Comunicação e notificações (3.6)
7. Comunidade e organização (3.7)
8. Relatórios e indicadores (3.8)

**Fora do âmbito.**
- Fundar ou promover novas AMAP: a FAIR-AMAP apoia as AMAP que já existem e se registam para a usar.
- Emitir faturas: cada produtor continua a faturar como hoje (NFR-18).
- Guardar o dinheiro dos coprodutores: os pagamentos passam por um prestador licenciado (NFR-19).
- Cabazes que juntam produtos de vários produtores.

**Objetivos de negócio.** A FAIR prevê uma experiência piloto em Portugal, com a plataforma quase gratuita para recolher feedback, e mais tarde uma fee mínima por AMAP mais uma percentagem das transações (NFR-21). O produto apoia uma distribuição alimentar local, sazonal e justa, em linha com os ODS que orientam a missão da FAIR.

## 1.4 Referências

**Unidade curricular**
1. ISEP, ENGREQ – Engenharia de Requisitos, *Trabalho Prático n.º 1*, versão 1.0, docentes Jorge Santos e Bruno Silva, Mestrado em Engenharia Informática, 2026/2027.
2. *Template de Especificação de Requisitos de Software* fornecido pelos docentes, ENGREQ, 2026/2027.

**Documentos das AMAP**

3. D-A: AMAP Porto Baixa, *Encomendas AMAP Porto Baixa – Jul a Dez 2026* (formulário de encomendas).
4. D-B: AMAP UPTEC Baixa, *Termos e Condições – AMAP UPTEC Baixa*, versão 01.
5. D-C: AMAP Porto, *Guia para novos coprodutores (consumidores)*, versão antiga.
6. D-D: M. Leite Gonçalves, "Quando o Porto se enche de frutas e legumes que ainda cheiram a terra", *Público*, 28/09/2023.
7. D-E: Rede de AMAP, *Carta de Princípios das AMAP*, 15/12/2018. https://amap.movingcause.org/carta-de-principios/
8. D-F: Rede de AMAP, *Perguntas frequentes*. https://amap.movingcause.org/perguntas-frequentes/
9. D. Martins, *Quinta da Serrinha* (apresentação), 2024.
10. S. Araújo, *A BioGoods* (apresentação na sessão de 29/09), setembro de 2026.

**Soluções concorrentes**

11. AMAPJ. https://agritechobservatory.review.fao.org/es/amapj
12. Juntagrico. https://gappsy.com/tools/juntagrico/
13. Katuma / Open Food Network. https://katuma.org/en, https://openfoodnetwork.org/
14. Local Line. https://localline.co/pricing-for-farms
15. GrownBy. https://grownby.com/
16. Farmigo. https://farmigo.com/
17. CSAware. https://www.csaware.com/
18. Local Food Marketplace. https://home.localfoodmarketplace.com/

**Normas e regulamentação**

19. Regulamento (UE) 2016/679 (Regulamento Geral sobre a Proteção de Dados, RGPD).
20. Diretiva (UE) 2015/2366 relativa aos serviços de pagamento (PSD2).
21. Autoridade Tributária e Aduaneira (AT), regras sobre software de faturação certificado.
22. W3C, *Web Content Accessibility Guidelines (WCAG) 2.1*, 2018.
23. Nações Unidas, *Transformar o nosso mundo: Agenda 2030 de Desenvolvimento Sustentável*, 2015.

**Documentos do projeto**

24. Grupo 02, *Repositório do projeto FAIR-AMAP*. https://github.com/BrunoAlvees/engreq_2627_G02
25. Grupo 02, *T1 – Análise de concorrência* (docs/tecnicas/CompetitorAnalysis.md).
26. Grupo 02, *T2 – Análise documental: resultados e dúvidas sobre os processos atuais* (docs/tecnicas/ResultadosAnaliseDocumentalPT.md, docs/tecnicas/DuvidasProcessosAtuaisPT.md).
27. Grupo 02, *T3 – Dinâmica de mercado* (docs/tecnicas/MarketDynamic.md).
28. Grupo 02, *T4 – Análise de diferenciação* (docs/tecnicas/AnaliseDiferenciacaoPT.md).
