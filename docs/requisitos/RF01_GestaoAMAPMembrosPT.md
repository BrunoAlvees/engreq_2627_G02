# RF01 – Gestão da AMAP e dos membros

**Atualizado em:** 21/10/2026 · [Convenções e fontes](README.md)

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
| RF-MEM-01 | O sistema deve permitir criar uma AMAP com nome, ponto de entrega, dia e horário de distribuição, contacto e regras de funcionamento. | Gestão da AMAP, Admin FAIR | M | D-A, E-2 §6, DOC-33 | Proposto |
| RF-MEM-02 | O sistema deve suportar várias AMAP independentes, cada uma com as suas regras, e permitir que um produtor participe em várias AMAP. | Admin FAIR | M | E-2 §1, §11, CA | Proposto |
| RF-MEM-03 | O sistema deve suportar AMAP com um único produtor e AMAP com vários produtores, que podem oferecer produtos iguais ou diferentes. | Gestão da AMAP | M | E-2 §3, N14 | Proposto |
| RF-MEM-04 | O sistema deve disponibilizar uma página pública de cada AMAP (apresentação, princípios, produtores e produtos, local e horário, vagas) com a opção "Quero aderir", que inicia o pedido de adesão. | Interessado | S | E-1 §3.1, D-C, D-D, Brainstorm 14/10 | Proposto |
| RF-MEM-05 | O sistema deve permitir a um interessado pedir a adesão a uma AMAP e registar quem trata o pedido (produtor principal ou gestão). | Interessado, Gestão | M | E-1 §3.1, E-4, DOC-38 | Proposto |
| RF-MEM-06 | O sistema deve colocar o interessado numa lista de espera ordenada quando a AMAP não tem vagas, e avisá-lo quando houver vaga. | Sistema | M | E-1 §3.1, D-A, DV-02, DV-03, N16 | A validar (DV-03) |
| RF-MEM-07 | O sistema deve permitir entregas experimentais antes da subscrição, com um número configurável por AMAP. | Gestão, Produtor | S | E-4 (2 entregas), D-C (1 entrega), DOC-23 | A validar (DV-01) |
| RF-MEM-08 | O sistema deve guardar o estado de cada membro: interessado, em lista de espera, em experiência, ativo ou saído. | Sistema | M | DOC-38, E-4 | Proposto |
| RF-MEM-09 | O sistema deve permitir à gestão da AMAP aprovar ou recusar um pedido de inscrição. | Gestão | S | D-B §3.2, DOC-22 | Proposto |
| RF-MEM-10 | O sistema deve registar o coprodutor com nome, email e telemóvel, e pedir o NIF apenas se ele quiser fatura com NIF. | Coprodutor | M | D-A, D-B, DOC-18, DOC-39, CIVA art. 40.º | Proposto |
| RF-MEM-11 | O sistema deve registar o produtor com descrição, localização, contactos e evidências da forma de produção (certificados ou fotografias e descrição da exploração). | Produtor | M | E-1 §3.6, D-A, DOC-16 | A validar (PA-01) |
| RF-MEM-12 | O sistema deve exigir a aceitação dos Termos e Condições e do Guia da AMAP, com declaração de maioridade, e guardar a versão e a data aceites. | Coprodutor | M | D-A, D-B, DOC-19 | Proposto |
| RF-MEM-13 | O sistema deve permitir dar e retirar consentimentos opcionais (ex.: uso dos dados em estudos), guardando a prova (data e versão). | Coprodutor | M | D-A, D-B, DOC-20, DOC-40, RGPD art. 7.º | Proposto |
| RF-MEM-14 | O sistema deve permitir ao titular consultar, exportar, corrigir e pedir a eliminação dos seus dados, e controlar o prazo de resposta (1 mês). | Coprodutor, Gestão | M | D-B §3.1, DOC-40, RGPD art. 12.º | Proposto |
| RF-MEM-15 | O sistema deve indicar, por AMAP, os responsáveis pelo tratamento dos dados (os produtores) e o ponto de contacto. | Gestão | S | D-B §3.1, DOC-21, RGPD art. 26.º | Proposto |
| RF-MEM-16 | O sistema deve permitir atribuir papéis (coprodutor, produtor, gestão da AMAP, administrador) com permissões diferentes; uma pessoa pode ter vários papéis. | Admin FAIR, Gestão | M | E-1 §3.2, D-C §4.5, CA (AMAPJ) | Proposto |
| RF-MEM-17 | O sistema deve permitir registar a saída de um coprodutor a meio da subscrição, com o motivo, e escolher o que acontece às entregas seguintes: transferir a subscrição para um substituto ou doar as entregas restantes a uma instituição. Os acertos de pagamento são tratados caso a caso. | Coprodutor, Gestão | S | D-F, DOC-32, C5, E-2 §7, E-2 §9 (doação), Brainstorm 14/10 | Proposto |
| RF-MEM-18 | *(Fundido no RF-MEM-17 no brainstorm de 14/10.)* | — | — | — | Rejeitado |
| RF-MEM-19 | O sistema deve disponibilizar um portal público com todas as AMAP da plataforma, com pesquisa por localização e ligação para a página de cada AMAP. | Interessado | C | E-1 §3.1, CA, Brainstorm 14/10 | Proposto |
| RF-MEM-20 | O sistema deve permitir que um coprodutor seja membro de várias AMAP (ex.: para ter entregas todas as semanas) e ver as entregas de todas num só calendário. | Coprodutor | S | E-2 §6, Brainstorm 14/10 | Proposto |
| RF-MEM-21 | O sistema deve ter um painel de regras da AMAP, onde a gestão configura o que varia entre AMAP: duração do ciclo, prazos de subscrição, número de entregas experimentais, modo de renovação (RF-SUB-11), destinos possíveis do cabaz nas ausências (RF-ENT-11) e documentos (Termos, Guia). | Gestão | M | Princípio 1, E-2 §1, §11, Brainstorm 14/10 | Proposto |
