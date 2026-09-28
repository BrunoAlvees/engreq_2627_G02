# FAIR-AMAP - Informação conhecida sobre o projeto

**Atualizado em:** 28/09/2026

Este documento reúne a informação disponível no enunciado e a informação da primeira entrevista, realizada em 23/09, com base na informação recolhida e partilhada pelos elementos do grupo.

A informação da entrevista representa o entendimento atual do grupo e ainda não constitui uma especificação validada pelo cliente. Os pontos que exigem esclarecimento estão identificados ao longo do documento. O enunciado sustenta as secções 1 e 6.

## 1. Contexto do projeto

A FAIR Software Solutions é uma startup que pretende desenvolver soluções de software para facilitar a distribuição e a venda de produtos alimentares, no contexto da Agenda 2030 para o Desenvolvimento Sustentável, que integra 17 Objetivos de Desenvolvimento Sustentável (ODS).

A empresa identificou uma oportunidade de negócio no domínio das AMAP/CSA e procura uma equipa para especificar os requisitos funcionais e não funcionais de uma solução para este mercado, abrangendo os seus processos.

O enunciado apresenta AMAP e CSA como formas de organização que aproximam consumidores e produtores em torno da produção de alimentos saudáveis, da sustentabilidade, da regeneração dos ecossistemas e de condições de vida mais dignas para os produtores. Uma AMAP/CSA é constituída por um grupo de consumidores que apoia ativa e diretamente um ou mais agricultores e produtores, assegurando o escoamento da sua produção.

## 2. Objetivo e âmbito da solução

A empresa não pretende criar CSA. Pretende fornecer software que facilite a organização e o funcionamento das CSA, nomeadamente das que apresentam dificuldades de organização.

A orientação para os ODS foi também reforçada na entrevista.

## 3. Funcionamento descrito na entrevista

### 3.1. Adesão de consumidores

O consumidor procura uma CSA de que goste ou que esteja próxima e solicita uma vaga. Se houver vaga, pode aderir. Caso contrário, fica em lista de espera.

### 3.2. Gestão da CSA

A gestão da CSA pode ser assegurada por uma pessoa ou por um grupo/comissão. Foi referido que uma CSA pode funcionar através de uma associação ou como um grupo de pessoas sem uma entidade jurídica própria.

A gestão acompanha os pagamentos, as entregas dos produtores e as recolhas dos consumidores, e define o calendário das entregas. Foi também apontada como responsável por lidar com situações em que o processo não corre como previsto. Os procedimentos concretos para resolver cada situação ainda não ficaram definidos.

### 3.3. Compromisso com o produtor e entregas

O modelo habitual descrito é a subscrição de um cabaz durante um período, com produtos sazonais, em vez da compra pontual de uma lista fixa de produtos e quantidades. Foram dados exemplos de compromissos de seis meses ou um ano, sem estabelecer uma duração obrigatória.

O compromisso permite ao produtor planear a produção com maior previsibilidade. O coprodutor aceita que o conteúdo e a dimensão das entregas possam variar com a época e com a produção disponível.

As entregas são periódicas. Foram mencionadas frequências semanais, quinzenais e mensais como possibilidades, dependendo do funcionamento da CSA.

### 3.4. Indicadores

Foi referido que alguns indicadores de desempenho (KPI) seriam interessantes. Não foram registados indicadores concretos nem uma decisão de os tornar obrigatórios.

Foi referida a utilidade dos KPI e relatórios para organizações ligadas às CSA e para investigadores. O grupo reteve a indicação de que seriam desejáveis, mas a sua prioridade formal ainda precisa de confirmação com o cliente.

### 3.5. Ofertas e subscrições

Os produtores indicam na plataforma o que vão produzir e quando, criando ofertas com o que podem fornecer e a capacidade disponível. Os coprodutores registados na CSA selecionam e subscrevem essas ofertas. As quantidades usadas na explicação são exemplos, não limites estabelecidos para o sistema.

Foi descrito um ciclo comum de três meses, antes do qual os produtores preparam as ofertas. Essa duração foi apresentada como habitual, não como uma regra universal. O ciclo de organização das ofertas e a duração do compromisso do coprodutor não devem ser tratados como necessariamente iguais.

### 3.6. Registo do produtor e evidências da forma de produção

A informação reunida pelo grupo refere-se ao registo do produtor. É referido que, normalmente, o produtor apresenta certificações relacionadas com a forma de produção. Os nomes exatos das certificações não são suficientemente claros.

É também mencionado que produtores pequenos sem certificação apresentam fotografias da exploração e da forma como trabalham e produzem. Não ficaram definidos critérios de aceitação, responsáveis pela verificação ou equivalência entre fotografias e certificação.

### 3.7. Relação entre produtores e coprodutores

O coprodutor mantém uma relação continuada com o produtor e partilha parte da responsabilidade pelo processo de produção, através do compromisso assumido. A relação inclui proximidade e conhecimento dos produtores, podendo envolver diálogo sobre o que produzir. Os direitos e deveres concretos ainda precisam de ser detalhados.

Foram descritas visitas às explorações que permitem aos coprodutores conhecer a produção e reforçar a relação com os produtores. Por vezes, os coprodutores também ajudam nas atividades agrícolas. Trata-se de uma prática do negócio mencionada na entrevista, não de um pedido explícito para o software gerir visitas ou essas atividades.

### 3.8. Distribuição e comunicação

Existe habitualmente um local de distribuição onde os produtores deixam os produtos e os consumidores recolhem os cabazes, de acordo com o calendário definido pela organização.

Foi salientado que conhecer o calendário não dispensa avisos sobre as distribuições próximas. Foi também referida a publicação de notícias no software para comunicar acontecimentos relacionados com a produção. Os canais, os destinatários e as permissões de publicação ainda precisam de ser definidos.

### 3.9. Pagamentos e faturação

O momento do pagamento depende das regras da CSA. Foi referido que normalmente ocorre no início do ciclo, permitindo ao produtor investir na produção, embora tenham sido mencionadas outras possibilidades. O compromisso antecipado não implica, por si só, que todos os pagamentos sejam antecipados.

A entidade que emite a fatura depende da configuração da CSA. Foi dado o exemplo de CSA pequenas em que os consumidores pagam diretamente aos agricultores e estes emitem as faturas. Foram também mencionadas CSA formalmente constituídas que cobram uma pequena comissão para suportar custos de funcionamento. Não ficou definida uma regra única de faturação para todos os modelos.

Foi identificada a necessidade de reduzir a quantidade de operações de pagamento quando existem vários coprodutores e produtores. A forma de concentração dos pagamentos ainda está em aberto; o pagamento mensal não foi estabelecido como solução obrigatória.

## 4. Informação mencionada, mas ainda não suficientemente segura

**Informação recolhida que exige esclarecimento.**

Os pontos seguintes ficam preservados como informação provisória, sem serem tratados como regras ou funcionalidades acordadas:

- **Preferências e substituições:** parece existir a intenção de registar preferências dos coprodutores e permitir substituições pontuais nos cabazes. Falta esclarecer quem decide e quais são as regras e limites; não se assume a escolha livre de todos os produtos.
- **Novas ofertas:** foi mencionada a comunicação da disponibilidade de ofertas, mas os destinatários, o momento e o mecanismo precisam de ser esclarecidos. Não está estabelecido um processo de votação.
- **Equilíbrio das entregas:** parece existir a intenção de acompanhar as entregas ao longo do tempo para assegurar um equilíbrio justo. Não ficou definido se esse acompanhamento considera peso, valor, número de entregas ou outro critério.
- **Modelo de cobrança da FAIR:** foi discutido um possível modelo com um valor mínimo e uma componente associada ao volume de utilização ou transações. A entidade pagadora, a base de cálculo e os valores não ficaram suficientemente claros para estabelecer uma regra.
- **Detalhes operacionais:** continuam por definir a formalização e alteração das subscrições, as regras de concentração de pagamentos, a faturação em cada modelo de CSA e os procedimentos perante falhas na produção ou na recolha.

## 5. Orientações do professor após a entrevista

Depois da entrevista, o professor salientou que:

- Nas primeiras entrevistas, devem ser privilegiadas perguntas abertas e abrangentes sobre os processos; perguntas técnicas mais específicas devem ser aprofundadas posteriormente com os intervenientes adequados.

- Não tinham sido feitas perguntas sobre os documentos envolvidos no processo e é necessário conhecer esses documentos.
- É necessário identificar os interessados (stakeholders).

Foi também reforçada a necessidade de compreender o processo completo e o papel dos participantes. A fatura surge como exemplo de um documento que contém informação útil para o levantamento de requisitos. O exemplo não estabelece automaticamente campos ou funcionalidades a implementar no software.

## 6. O que o trabalho académico exige

### 6.1. Organização e método

- O trabalho é realizado em grupos de 4 ou 5 estudantes.
- Deve seguir a metodologia de levantamento de requisitos apresentada na disciplina. Podem ser utilizadas diferentes técnicas e combinadas entre si.
- Sempre que possível, haverá sessões com stakeholders reais nas aulas T, complementadas por análise documental, pesquisa de fontes relevantes e sessões simuladas nas aulas PL, nas quais os docentes representam diferentes stakeholders do cliente.
- As sessões devem ser agendadas individualmente, normalmente durante as aulas práticas, tendo em conta a disponibilidade dos stakeholders da FAIR-AMAP.
- O diretor da FAIR só está disponível para a apresentação inicial do projeto.
- O progresso deve ser registado no repositório, incluindo planeamento, reuniões, tarefas e artefactos.

### 6.2. Entrega

O resultado final deve ser apresentado num documento de especificação de requisitos de software (SRS), para o qual será fornecido um template de exemplo. Deve refletir a especificação completa, o processo utilizado e outros artefactos relevantes.

O enunciado apresenta os seguintes elementos a incluir como exemplos:

- Descrição geral do sistema.
- Funcionalidades do sistema.
- Interfaces externas.
- Outros requisitos não funcionais.
- Prioridades.
- Estimativa, em horas, do desenvolvimento de cada funcionalidade.
- Descrição do método seguido, das técnicas aplicadas, das evidências de suporte, do contexto e do tempo dedicado por analista de negócio/tarefa.

A submissão será feita no Moodle. O documento fornecido não indica a data-limite de entrega nem os detalhes da apresentação.

### 6.3. Avaliação

A avaliação é realizada pelo docente responsável, com base na apresentação, no processo seguido e nos artefactos entregues. Incide sobre a capacidade de:

1. Especificar e analisar requisitos de uma solução de software.
2. Trabalhar em equipa, planear e gerir o projeto, comunicar e documentar a atividade.
