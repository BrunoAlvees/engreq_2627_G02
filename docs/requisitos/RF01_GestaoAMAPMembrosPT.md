# RF01 – Gestão da AMAP e dos membros

**Atualizado em:** 28/10/2026 · [Convenções e fontes](README.md)

## Descrição
Permite criar e configurar AMAP independentes (com um ou vários produtores) e gerir o percurso de cada pessoa: pedido de adesão, entregas experimentais, lista de espera, inscrição, dados pessoais e consentimentos. Hoje, a adesão é feita por contacto direto com a produtora principal, os dados chegam por Google Forms e não há registo do estado de cada membro.

## Sequências estímulo/resposta
- O interessado abre a página pública da AMAP (ou pesquisa no portal) → vê a apresentação, os produtores e se há vaga.
- O interessado pede para aderir → o sistema regista o pedido e avisa quem o trata. Se não houver vaga, coloca-o na lista de espera.
- A gestão aceita o pedido → o interessado passa a "em experiência" e, depois das entregas experimentais, recebe o convite para subscrever o ciclo.
- O coprodutor pede para eliminar os seus dados → o sistema regista o pedido e controla o prazo de resposta.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-MEM-01 | O sistema deve permitir criar e configurar AMAP independentes, com um ou vários produtores e as suas próprias regras de funcionamento. | Gestão da AMAP, Admin FAIR | M | D-A, E-2 §1, §3, §6, §11, CA, N14, DOC-33, princípio 1 | Proposto |
| RF-MEM-02 | O sistema deve disponibilizar uma página pública de cada AMAP e um portal com todas as AMAP da plataforma, a partir dos quais um interessado pode pedir a adesão. | Interessado | S | E-1 §3.1, D-C, D-D, CA, Brainstorm 14/10 | Proposto |
| RF-MEM-03 | O sistema deve gerir o processo de adesão de um interessado, do pedido até se tornar membro ativo, incluindo a lista de espera e as entregas experimentais. | Interessado, Gestão, Sistema | M | E-1 §3.1, E-4, D-A, D-B §3.2, D-C, DOC-22, DOC-23, DOC-38, N16 | Proposto |
| RF-MEM-04 | O sistema deve permitir registar os coprodutores e dar a cada produtor um perfil público com a sua forma de produção. | Coprodutor, Produtor | M | E-1 §3.6, D-A, D-B, D-E, DOC-16, DOC-18, DOC-39 | Proposto |
| RF-MEM-05 | O sistema deve recolher a aceitação dos termos e os consentimentos dos membros e permitir-lhes exercer os seus direitos sobre os dados pessoais (RGPD). | Coprodutor, Gestão | M | D-A, D-B §3.1, DOC-19, DOC-20, DOC-21, DOC-40, RGPD arts. 7.º, 12.º, 26.º | Proposto |
| RF-MEM-06 | O sistema deve permitir atribuir papéis com permissões diferentes, podendo uma pessoa ter vários papéis. | Admin FAIR, Gestão | M | E-1 §3.2, D-C §4.5, CA (AMAPJ) | Proposto |
| RF-MEM-07 | O sistema deve permitir que um coprodutor pertença a várias AMAP e registar a sua saída a meio de uma subscrição. | Coprodutor, Gestão | S | E-2 §6, §7, §9, D-F, DOC-32, C5, Brainstorm 14/10 | Proposto |

## Critérios de aceitação

**RF-MEM-01 – Criar e configurar AMAP**
- Uma AMAP tem nome, ponto de entrega, dia e horário de distribuição, contacto e regras de funcionamento.
- Pode haver várias AMAP independentes na plataforma, e um produtor pode participar em várias.
- Uma AMAP pode ter um só produtor ou vários, com produtos iguais ou diferentes.
- Um painel de regras permite à gestão configurar o que varia entre AMAP: duração do ciclo, prazos de subscrição, número de entregas experimentais, modo de renovação (RF-SUB-06), destinos possíveis do cabaz nas ausências (RF-ENT-11) e documentos (Termos, Guia).

**RF-MEM-02 – Página pública e portal**
- A página da AMAP mostra a apresentação, os princípios, os produtores e produtos, o local e horário e se há vagas.
- A página tem a opção "Quero aderir", que inicia o pedido de adesão (RF-MEM-03).
- *(Could)* O portal lista todas as AMAP da plataforma, com pesquisa por localização e ligação para a página de cada uma.

**RF-MEM-03 – Processo de adesão**
- O interessado pede a adesão e o sistema regista quem trata o pedido (produtor principal ou gestão).
- Se não houver vagas, o interessado entra numa lista de espera ordenada por ordem de chegada; a gestão pode alterar a ordem, registando o motivo; o interessado é avisado quando houver vaga (decisão do grupo de 21/10).
- Antes de subscrever, pode fazer entregas experimentais; o número é configurável por AMAP (ex.: 1 ou 2), o que resolve a diferença entre E-4 e D-C (DV-01).
- A gestão pode aprovar ou recusar o pedido.
- O sistema guarda o estado de cada pessoa: interessado, em lista de espera, em experiência, ativo ou saído.

**RF-MEM-04 – Registo de coprodutores e perfil do produtor**
- O coprodutor regista-se com nome, email e telemóvel; o NIF só é pedido se quiser fatura com NIF (CIVA art. 40.º).
- O produtor tem um perfil público com descrição, localização, contactos e evidências da forma de produção (certificados ou fotografias e descrição da exploração).
- As evidências não são verificadas pela plataforma nem pela gestão da AMAP: ficam visíveis aos coprodutores, que avaliam diretamente (lógica de confiança da Carta de Princípios; PA-01 resolvida pelo grupo em 21/10).

**RF-MEM-05 – Termos, consentimentos e RGPD**
- A inscrição exige aceitar os Termos e Condições e o Guia da AMAP, com declaração de maioridade; o sistema guarda a versão e a data aceites.
- O membro pode dar e retirar consentimentos opcionais (ex.: uso dos dados em estudos), com prova da data e da versão.
- O titular pode consultar, exportar, corrigir e pedir a eliminação dos seus dados; o sistema controla o prazo de resposta (1 mês).
- Cada AMAP indica os responsáveis pelo tratamento dos dados (os produtores) e o ponto de contacto.

**RF-MEM-06 – Papéis e permissões**
- Papéis: coprodutor, produtor, gestão da AMAP e administrador FAIR, cada um com permissões diferentes.
- Uma pessoa pode ter vários papéis (ex.: coprodutor e membro da gestão).

**RF-MEM-07 – Várias AMAP e saída a meio**
- Um coprodutor pode ser membro de várias AMAP (ex.: para ter entregas todas as semanas) e ver as entregas de todas num só calendário.
- A saída a meio da subscrição fica registada com o motivo; escolhe-se o que acontece às entregas seguintes: transferir a subscrição para um substituto ou doar as entregas restantes a uma instituição.
- Os acertos de pagamento são tratados caso a caso.

## Correspondência com a versão anterior
Na revisão de 28/10, os 21 requisitos anteriores foram agrupados em 7, para reduzir o detalhe (indicação do professor). O detalhe passou para os critérios de aceitação.

| Novo | Junta os anteriores |
|---|---|
| RF-MEM-01 | 01, 02, 03, 21 |
| RF-MEM-02 | 04, 19 |
| RF-MEM-03 | 05, 06, 07, 08, 09 |
| RF-MEM-04 | 10, 11 |
| RF-MEM-05 | 12, 13, 14, 15 |
| RF-MEM-06 | 16 |
| RF-MEM-07 | 17, 18 (já fundido no 17), 20 |
