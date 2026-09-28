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

A entidade responsável pela gestão da CSA tem um papel importante no seu funcionamento. Uma das responsabilidades mencionadas nos apontamentos é garantir que os pagamentos são feitos.

Foi também referido que a organização responsável pela CSA define o calendário das entregas. Os restantes detalhes desse calendário continuam por esclarecer.

### 3.3. Compromisso com o produtor e entregas

Foi referido que, quando alguém assume um compromisso de um ano com um produtor, sabe que as entregas não serão sempre iguais.

Esta informação não estabelece que todos os compromissos tenham obrigatoriamente a duração de um ano nem especifica o que varia entre entregas.

### 3.4. Indicadores

Foi referido que alguns indicadores de desempenho (KPI) seriam interessantes. Não foram registados indicadores concretos nem uma decisão de os tornar obrigatórios.

Foi referida a utilidade dos KPI e relatórios para organizações ligadas às CSA e para investigadores. O grupo reteve a indicação de que seriam desejáveis, mas a sua prioridade formal ainda precisa de confirmação com o cliente.

### 3.5. Informação sobre a produção

Segundo a informação recolhida, os produtores indicam na plataforma o que vão produzir e quando. A escolha de quantidades pelo consumidor não ficou suficientemente esclarecida, pelo que não se estabelece aqui uma regra sobre encomendas.

### 3.6. Registo do produtor e evidências da forma de produção

A informação reunida pelo grupo refere-se ao registo do produtor. É referido que, normalmente, o produtor apresenta certificações relacionadas com a forma de produção. Os nomes exatos das certificações não são suficientemente claros.

É também mencionado que produtores pequenos sem certificação apresentam fotografias da exploração e da forma como trabalham e produzem. Não ficaram definidos critérios de aceitação, responsáveis pela verificação ou equivalência entre fotografias e certificação.

### 3.7. Relação entre produtores e coprodutores

Foram descritas visitas às explorações que permitem aos coprodutores conhecer a produção e reforçar a relação com os produtores. Por vezes, os coprodutores também ajudam nas atividades agrícolas. Trata-se de uma prática do negócio mencionada na entrevista, não de um pedido explícito para o software gerir visitas ou essas atividades.

## 4. Informação mencionada, mas ainda não suficientemente segura

**Informação recolhida que exige esclarecimento.**

Os pontos seguintes ficam preservados como informação provisória, sem serem tratados como regras ou funcionalidades acordadas:

- **Comunicação de problemas:** terá sido referida a apresentação de notícias ou motivos para explicar problemas e atrasos nas colheitas através do software.
- **Ofertas e subscrições:** existem referências a novas ofertas, escolha e subscrição. A informação disponível não permite estabelecer o fluxo, os destinatários ou um requisito de notificações ou votação.
- **Emissão de faturas:** a resposta parece indicar que a entidade emissora depende da forma de organização da CSA, mas os exemplos não ficaram suficientemente claros. Não se identifica uma entidade emissora obrigatória.
- **Concentração de pagamentos:** parece existir interesse em reduzir a quantidade de pagamentos através da sua concentração. O pagamento mensal aparece como pergunta e não como uma regra claramente aceite.
- **Conceito de coprodutor:** a explicação final sugere uma relação próxima e continuada com o produtor, que pode incluir conversar sobre o que produzir e aceitar a variabilidade da produção. Esta interpretação ainda precisa de confirmação; os direitos e responsabilidades concretos não ficam definidos.

## 5. Orientações do professor após a entrevista

Depois da entrevista, o professor salientou que:

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
