# RF01 – Gestão da AMAP e dos membros

**Atualizado em:** 21/10/2026 · [Convenções e fontes](README.md)

## Descrição
Permite criar e configurar AMAP independentes (com um ou vários produtores) e gerir o percurso de cada pessoa: pedido de adesão, entregas experimentais, lista de espera, inscrição, dados pessoais e consentimentos. Hoje, a adesão é feita por contacto direto com a produtora principal, os dados chegam por Google Forms e não há registo do estado de cada membro.

## Sequências estímulo/resposta
- O interessado pesquisa AMAP perto de si → o sistema mostra as AMAP, os produtores e se há vaga.
- O interessado pede para aderir → o sistema regista o pedido e avisa quem o trata. Se não houver vaga, coloca-o na lista de espera.
- A gestão aceita o pedido → o interessado passa a "em experiência" e, depois das entregas experimentais, recebe o convite para subscrever o ciclo.
- O coprodutor pede para eliminar os seus dados → o sistema regista o pedido e controla o prazo de resposta.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-MEM-01 | O sistema deve permitir criar uma AMAP com nome, ponto de entrega, dia e horário de distribuição, contacto e regras de funcionamento. | Gestão da AMAP, Admin FAIR | M | D-A, E-2 §6, DOC-33 | Proposto |
| RF-MEM-02 | O sistema deve suportar várias AMAP independentes, cada uma com as suas regras, e permitir que um produtor participe em várias AMAP. | Admin FAIR | M | E-2 §1, §11, CA | Proposto |
| RF-MEM-03 | O sistema deve suportar AMAP com um único produtor e AMAP com vários produtores, que podem oferecer produtos iguais ou diferentes. | Gestão da AMAP | M | E-2 §3, N14 | Proposto |
| RF-MEM-04 | O sistema deve permitir pesquisar AMAP por localização e ver os produtores, os produtos e a existência de vagas. | Interessado | S | E-1 §3.1 | Proposto |
| RF-MEM-05 | O sistema deve permitir a um interessado pedir a adesão a uma AMAP e registar quem trata o pedido (produtor principal ou gestão). | Interessado, Gestão | M | E-1 §3.1, E-4, DOC-38 | Proposto |
| RF-MEM-06 | O sistema deve colocar o interessado numa lista de espera ordenada quando a AMAP não tem vagas, e avisá-lo quando houver vaga. | Sistema | M | E-1 §3.1, D-A, DV-02, DV-03, N16 | A validar (DV-03) |
| RF-MEM-07 | O sistema deve permitir entregas experimentais antes da subscrição, com um número configurável por AMAP. | Gestão, Produtor | S | E-4 (2 entregas), D-C (1 entrega), DOC-23 | A validar (DV-01) |
| RF-MEM-08 | O sistema deve guardar o estado de cada membro: interessado, em lista de espera, em experiência, ativo ou saído. | Sistema | M | DOC-38, E-4 | Proposto |
| RF-MEM-09 | O sistema deve permitir à gestão da AMAP aprovar ou recusar um pedido de inscrição. | Gestão | S | D-B §3.2, DOC-22 | Proposto |
| RF-MEM-10 | O sistema deve registar o coprodutor com nome, email e telemóvel, e pedir o NIF apenas se ele quiser fatura com NIF. | Coprodutor | M | D-A, D-B, DOC-18, DOC-39, CIVA art. 40.º | Proposto |
| RF-MEM-11 | O sistema deve registar o produtor com descrição, localização, contactos e evidências da forma de produção (certificados ou fotografias e descrição da exploração). | Produtor | M | E-1 §3.6, D-A, DOC-16 | A validar (quem verifica?) |
| RF-MEM-12 | O sistema deve exigir a aceitação dos Termos e Condições e do Guia da AMAP, com declaração de maioridade, e guardar a versão e a data aceites. | Coprodutor | M | D-A, D-B, DOC-19 | Proposto |
| RF-MEM-13 | O sistema deve permitir dar e retirar consentimentos opcionais (ex.: uso dos dados em estudos), guardando a prova (data e versão). | Coprodutor | M | D-A, D-B, DOC-20, DOC-40, RGPD art. 7.º | Proposto |
| RF-MEM-14 | O sistema deve permitir ao titular consultar, exportar, corrigir e pedir a eliminação dos seus dados, e controlar o prazo de resposta (1 mês). | Coprodutor, Gestão | M | D-B §3.1, DOC-40, RGPD art. 12.º | Proposto |
| RF-MEM-15 | O sistema deve indicar, por AMAP, os responsáveis pelo tratamento dos dados (os produtores) e o ponto de contacto. | Gestão | S | D-B §3.1, DOC-21, RGPD art. 26.º | Proposto |
| RF-MEM-16 | O sistema deve permitir atribuir papéis (coprodutor, produtor, gestão da AMAP, administrador) com permissões diferentes; uma pessoa pode ter vários papéis. | Admin FAIR, Gestão | M | E-1 §3.2, D-C §4.5, CA (AMAPJ) | Proposto |
| RF-MEM-17 | O sistema deve permitir transferir uma subscrição para outro coprodutor até ao fim do ciclo, quando alguém desiste. | Coprodutor, Gestão | S | D-F, DOC-32, C5 | Proposto |
| RF-MEM-18 | O sistema deve permitir registar a saída de um coprodutor a meio do ciclo, com o motivo, tratando os acertos caso a caso. | Gestão, Produtor | C | E-2 §7 | Proposto |
