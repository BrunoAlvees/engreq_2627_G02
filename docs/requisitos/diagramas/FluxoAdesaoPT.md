# Fluxo de adesão – coprodutores e produtores

**Responsável:** João Mata · **Atualizado em:** 13/11/2026 · **Secção do SRS:** Apêndice – Modelos de análise
**Fontes:** FR-01 a FR-08 e FR-14 em [RF01_GestaoAMAPMembrosPT.md](../RF01_GestaoAMAPMembrosPT.md) · [3.1](../../srs/3.1_AMAPMemberManagementEN.md) · [E-8](../../interviews/10-11-2026/Entrevista10_11PT.md) §1.3, §2.1, §2.2

Estes diagramas de atividades mostram o percurso de uma pessoa desde o primeiro contacto até ser membro ativo de uma AMAP. Complementam os casos de uso "Pedir adesão" (FR-03) e "Candidatar-se a uma AMAP" (FR-08) da secção 3.1. Os estados alcançados em cada fluxo estão detalhados nos [diagramas de estados](DiagramasEstadoPT.md).

## 1. Adesão de um coprodutor

**Imagem (para o SRS):** [imagens/FluxoAdesaoCoprodutorPT.png](imagens/FluxoAdesaoCoprodutorPT.png)

```mermaid
flowchart TD
    A([Início]) --> B[O candidato a coprodutor abre a página<br/>pública da AMAP ou pesquisa no portal]
    B --> C[Seleciona 'Quero aderir', preenche nome,<br/>email e telefone e aceita os Termos]
    C --> D{Aceita os Termos?}
    D -- Não --> X1([Pedido não submetido])
    D -- Sim --> E[O sistema regista o pedido e avisa<br/>quem o trata: gestão ou produtor principal]
    E --> G{Há lugares na AMAP?}
    G -- Não --> H[O sistema coloca a pessoa na<br/>lista de espera, por ordem de chegada]
    H --> I[Abre um lugar: o sistema avisa<br/>a primeira pessoa da lista]
    I --> F
    G -- Sim --> F{A gestão aprova?}
    F -- Não --> X2([Pessoa avisada; pedido rejeitado])
    F -- Sim --> J[Estado 'em experiência': o sistema marca<br/>as entregas experimentais definidas pela AMAP]
    J --> K[Fazem-se as entregas experimentais]
    K --> L[O sistema convida a pessoa a subscrever<br/>o ciclo atual ou o seguinte]
    L --> M{Subscreve?}
    M -- Não --> X3([Estado 'saiu'])
    M -- Sim --> N[Subscrição confirmada e<br/>primeiro pedido de pagamento]
    N --> O([Coprodutor ativo])
```

**Notas**
- **Os lugares existem a dois níveis:** a capacidade máxima da AMAP e o número de coprodutores que cada produtor aceita por produto (E-8 §2.2, FR-14).
- **O número de entregas experimentais** é configurado por AMAP (ex.: 1 ou 2), o que resolve a diferença entre a E-4 e o D-C (DV-01).
- **A gestão pode mudar a ordem da lista de espera**, registando o motivo (decisão do grupo de 21/10, FR-03).
- O que acontece quando uma pessoa não subscreve depois da experiência é um **pressuposto do grupo**; não foi discutido com o cliente.

## 2. Adesão de um produtor

**Imagem (para o SRS):** [imagens/FluxoAdesaoProdutorPT.png](imagens/FluxoAdesaoProdutorPT.png)

```mermaid
flowchart TD
    A([Início]) --> B{Como começa?}
    B -- Candidatura --> C[O produtor seleciona 'Candidatar-me'<br/>na página da AMAP]
    B -- Convite --> D[A gestão convida o produtor;<br/>o produtor abre o convite]
    C --> E
    D --> E[O produtor preenche nome, localização, produtos<br/>principais, modo de produção e envia documentos,<br/>ex.: certificado biológico]
    E --> F[O sistema regista a candidatura<br/>e avisa a gestão]
    F --> G{Visita à quinta?}
    G -- Sim --> H[Membros da AMAP visitam a quinta e registam<br/>a visita: data, quem foi, notas]
    G -- Não --> I
    H --> I{A gestão aprova?}
    I -- Não --> X1([Produtor avisado; candidatura rejeitada])
    I -- Sim --> J{A AMAP tem capacidade?}
    J -- Não --> K[O produtor fica em lista de espera<br/>e é avisado quando abrir um lugar]
    K --> L
    J -- Sim --> L[O produtor fica ativo na AMAP;<br/>documentos visíveis no perfil público]
    L --> M[O produtor indica as datas em que pode entregar<br/>e o que pode entregar]
    M --> N([Produtor ativo, pronto para o próximo ciclo])
```

**Notas**
- Um produtor **convidado** é convidado a candidatar-se, com a seleção praticamente feita (E-8 §2.1).
- A **visita à quinta** é habitual mas não obrigatória; o processo pode variar entre AMAP, mas há sempre um registo do produtor (E-8 §2.1).
- Um produtor pode estar em **várias AMAP**; cada candidatura é separada (E-8 §2.1, NFR-22).

## 3. Adesão de uma AMAP à plataforma (contexto)

Os fluxos do produtor e do coprodutor partem do princípio de que a AMAP já existe. Quando não existe, a AMAP é registada primeiro.

**Imagem (para o SRS):** [imagens/FluxoAdesaoAMAPPT.png](imagens/FluxoAdesaoAMAPPT.png)

```mermaid
flowchart TD
    A([Início]) --> B[Uma pessoa regista uma nova AMAP]
    B --> C[O administrador FAIR pede a documentação:<br/>nome da AMAP, localização, responsável, NIF]
    C --> D[A pessoa envia os documentos]
    D --> E{O administrador FAIR autoriza?}
    E -- Não --> X1([Registo não autorizado])
    E -- Sim --> F[AMAP criada; a pessoa passa a ser<br/>o seu primeiro gestor]
    F --> G{A AMAP foi criada por um produtor?}
    G -- Sim --> H[O produtor candidata-se à AMAP como produtor<br/>e aceita a candidatura como gestor]
    G -- Não --> I
    H --> I[A gestão configura as regras da AMAP<br/>e abre a página pública]
    I --> J([AMAP pronta para receber produtores e coprodutores])
```

**Nota:** numa AMAP criada por um produtor, este fica com os papéis de gestão e de produtor (E-8 §2.1, FR-06).
