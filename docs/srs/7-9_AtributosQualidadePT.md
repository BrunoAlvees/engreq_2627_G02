# 7 Atributos de qualidade · 8 Internacionalização · 9 Outros requisitos

**Responsável:** Bruno Alves · **Atualizado em:** 14/11/2026 · **Estado:** pronto para o relatório
**Fontes:** [RNF_AtributosQualidadePT.md](../requisitos/RNF_AtributosQualidadePT.md) §1–§5 e códigos de fonte em [requisitos/README.md](../requisitos/README.md)

# 7 Atributos de qualidade

Esta secção especifica os requisitos não funcionais sobre a qualidade com que o FAIR-AMAP tem de funcionar. Cada um está escrito de forma a poder ser verificado. Os valores numéricos marcados **Hip.** na coluna das fontes são propostas do grupo: nenhum stakeholder os indicou, e têm de ser confirmados com a FAIR antes do desenvolvimento. Os requisitos de interfaces (NFR-15 a NFR-17) estão na secção 6, e os que funcionam como restrições (NFR-18 a NFR-24) estão na secção 2.4.

## 7.1 Usabilidade

A maioria dos coprodutores usa o sistema no telemóvel, muitas vezes no ponto de levantamento, e os produtores querem gastar o mínimo de tempo possível com a gestão ("só produzir", E-2). Por isso, a usabilidade mede-se pelo tempo e pelo número de passos das tarefas mais frequentes.

| ID | Requisito | Prio. | Fonte | Estado |
|---|---|---|---|---|
| NFR-01 | O sistema deve ser uma **aplicação web responsiva** (telemóvel e computador) que não exige instalação e que pode ser instalada no ecrã inicial do telemóvel como **PWA**, sem passar pelas lojas de aplicações. O sistema deve explicar de forma simples como instalar a aplicação (Android e iPhone) e ativar as notificações. | M | E-3; decisão do grupo de 21/10 | Proposto |
| NFR-02 | As tarefas mais frequentes devem ser rápidas: um coprodutor que já usou o sistema subscreve um ciclo completo em **10 minutos** ou menos, sem ajuda; cada tarefa recorrente do produtor (publicar o conteúdo do cabaz, registar uma falta, confirmar um pagamento) demora **2 minutos** ou menos; o coprodutor vê o que vai levantar e quanto deve a **2 cliques** ou menos da página inicial. | S | E-2 §3, E-3 §1, §10, CA; Hip. (valores) | Proposto |
| NFR-03 | O sistema deve cumprir as **WCAG 2.1, nível AA**. | S | Hip. | Proposto |

**Verificação:** o NFR-02 verifica-se com testes de usabilidade com pelo menos cinco coprodutores e dois produtores de uma AMAP piloto, cronometrando cada tarefa; o NFR-03 com um verificador automático de acessibilidade e uma revisão manual dos ecrãs principais.

## 7.2 Desempenho

A carga concentra-se em poucos momentos: o último dia de cada período de subscrição e a hora da distribuição, quando muitos coprodutores abrem a aplicação ao mesmo tempo.

| ID | Requisito | Prio. | Fonte | Estado |
|---|---|---|---|---|
| NFR-09 | O sistema deve suportar AMAPs com até **200 coprodutores** e várias AMAPs na mesma instalação. | M | E-2 §3, §6, D-D | Proposto |
| NFR-10 | As páginas principais devem carregar em **2 segundos** ou menos em 95% dos pedidos, mesmo no último dia de subscrição. | S | Hip. | Proposto |

**Justificação:** hoje as AMAPs têm até cerca de 50 coprodutores, mas uma CSA portuguesa já tem cerca de 200 (E-2); dimensionar para 200 por AMAP deixa margem para crescer. O NFR-10 verifica-se com um teste de carga que simula todos os coprodutores de uma AMAP de 200 membros a subscrever na mesma hora.

## 7.3 Segurança

O FAIR-AMAP guarda dados pessoais (contactos, NIF, pagamentos) e, para alguns coprodutores, dados de saúde (alergias e intolerâncias). A segurança e a privacidade seguem o RGPD; os papéis de responsável e subcontratante estão no NFR-08.

| ID | Requisito | Prio. | Fonte | Estado |
|---|---|---|---|---|
| NFR-04 | O acesso deve exigir **autenticação**. Cada papel só acede aos dados de que precisa: um produtor só vê os coprodutores que lhe compram. | M | D-B §3.1, RGPD | Proposto |
| NFR-05 | Todas as comunicações devem ser **cifradas** (HTTPS/TLS). | M | RGPD art. 32.º | Proposto |
| NFR-06 | Alergias e intolerâncias são **dados de saúde**: só devem ser guardadas com consentimento explícito, só ser visíveis para os produtores que entregam a esse coprodutor, e nunca aparecer em etiquetas ou folhas impressas (que mostram só o nome e as substituições feitas). | M | E-2 §4, RGPD art. 9.º, brainstorm 14/10 | Proposto |
| NFR-07 | O sistema deve registar **quem alterou** encomendas, entregas e pagamentos, e **quando** (registo de auditoria). | S | Hip. (C3: valores contestados) | Proposto |
| NFR-08 | O sistema deve permitir o **cumprimento do RGPD**: produtores como responsáveis conjuntos, FAIR como subcontratante, registo das atividades de tratamento, notificação de violações em 72 h, e apagamento ou anonimização dos dados pessoais quando termina o prazo de conservação de cada finalidade, salvo obrigação legal (p. ex. fiscal). | M | D-B, D-B §3.1, RGPD arts. 5.º, 26.º, 28.º, 30.º, 33.º | Proposto |

## 7.4 Segurança física (Safety)

O FAIR-AMAP não controla equipamento físico, por isso os danos que pode causar são indiretos. O grupo identificou quatro riscos; cada um está coberto por requisitos que já existem neste SRS, por isso não se acrescentou nenhum requisito novo. Não se aplica nenhuma certificação de segurança.

| Risco | Dano possível | Salvaguarda | Requisitos |
|---|---|---|---|
| Um coprodutor recebe um produto a que é alérgico | Dano para a saúde | As exclusões registadas pelo coprodutor são mostradas ao produtor quando prepara o cabaz, e a substituição fica registada; os dados de saúde ficam privados (nunca nas etiquetas) | FR-19, NFR-06 |
| Perdem-se encomendas, entregas ou pagamentos | O produtor não sabe o que entregar; coprodutores pagam duas vezes ou não pagam | Cópia de segurança diária com perda máxima de 24 h de dados; registo de auditoria de cada alteração | NFR-11, NFR-07 |
| Um coprodutor leva o saco de outro membro | Dano para a saúde se o saco tiver um produto a que é alérgico; o outro membro fica sem cabaz | Cada etiqueta mostra o nome e "Saco x de y"; quando o produtor imprime etiquetas QR, a leitura avisa se o saco não é seu (E-8) | FR-28, FR-29 |
| Dinheiro perdido ou retido pela plataforma | Perda financeira para coprodutores ou produtores | O sistema nunca guarda o dinheiro; os pagamentos passam por um prestador licenciado | NFR-19, NFR-17 |

## 7.5 Disponibilidade e fiabilidade

As AMAPs não precisam do sistema 24 horas por dia: o que importa são as horas de distribuição e o fim de cada período de subscrição. O requisito está ligado a esses períodos em vez de a uma percentagem genérica (decisão do grupo de 28/10).

| ID | Requisito | Prio. | Fonte | Estado |
|---|---|---|---|---|
| NFR-11 | O sistema deve estar disponível nas **horas de distribuição** de cada AMAP e nos **últimos 3 dias de cada período de subscrição**; a manutenção planeada faz-se fora desses períodos. Deve ser feita uma **cópia de segurança diária**, com perda máxima de **24 horas** de dados. | S | D-A, E-3 §9; decisão do grupo de 28/10 | Proposto |
| NFR-12 | A confirmação de levantamento deve funcionar com **rede fraca** no ponto de levantamento: fica guardada no telemóvel e é enviada quando houver ligação. | C | Brainstorm 14/10; Hip. | Ideia |

# 8 Requisitos de internacionalização e localização

A primeira versão é para AMAPs portuguesas: nenhuma das soluções analisadas tem interface em português (CA). O inglês também é preciso desde o início, porque alguns coprodutores são estrangeiros a viver em Portugal (E-8). O modelo de negócio da FAIR só funciona em escala (NFR-21, NFR-22), por isso o sistema tem de estar preparado para outros países sem ser reescrito.

| ID | Requisito | Prio. | Fonte | Estado |
|---|---|---|---|---|
| NFR-13 | A interface deve estar em **português europeu** e **inglês**, e preparada para outras línguas (p. ex. francês). | M | CA, E-8 (coprodutores estrangeiros) | Proposto |
| NFR-14 | O sistema deve mostrar valores em **euros com IVA incluído**, datas no formato **dd/mm/aaaa** e horas no **fuso horário de Portugal**. | M | D-A | Proposto |

**Verificação:** o NFR-13 cumpre-se quando todos os textos da interface vêm de ficheiros de tradução, de modo que uma língua nova só precisa de um ficheiro novo, sem alterar código.

# 9 Outros requisitos

Não há requisitos que não caibam nas secções anteriores. Os restantes requisitos não funcionais são:

- **restrições** da regulamentação, dos princípios das AMAP, do modelo de negócio da FAIR e da arquitetura (NFR-18 a NFR-24): secção 2.4;
- **interfaces externas** (notificações, exportação para folha de cálculo, prestador de pagamentos; NFR-15 a NFR-17): secção 6.

Os requisitos legais (RGPD e PSD2) estão cobertos pelos NFR-04 a NFR-08 (secção 7.3) e pelo NFR-19 (secção 2.4).
