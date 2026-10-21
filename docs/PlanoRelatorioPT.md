# Plano do relatório (SRS): divisão de secções e diagramas

**Estado:** proposta para o grupo aprovar
**Atualizado em:** 21/10/2026
**Template:** `LABDSOFT - Requirements template for TP1 v1.1`

A nota é dada em função da defesa: **cada elemento tem de conhecer o documento todo**, não só as suas secções. Por isso cada secção é revista por outro elemento.

## 1. Divisão das secções

| Elemento | Secções do SRS | Secção 3 – System features | Revê as secções de |
|---|---|---|---|
| **Bruno Alves** | 4 Requisitos de dados · 5 Modelo de domínio · 12.2 Modelos de análise | **3.3** RF03 Ciclos e subscrições · **3.4** RF04 Calendário e entregas · coerência da secção 3 | Liane |
| **Liane Duarte** | 1 Introdução (já em curso) · 2 Descrição geral | **3.6** RF06 Comunicação · **3.7** RF07 Comunidade | João |
| **João Mata** | 6 Interfaces externas · 7 Atributos de qualidade · 8 Internacionalização · 9 Outros requisitos | **3.5** RF05 Pagamentos e faturação | Jakub |
| **Jakub** | 11 Product backlog (prioridades e estimativas em horas) | **3.2** RF02 Catálogo e ofertas · **3.8** RF08 Relatórios e indicadores | Leonor |
| **Leonor** | 10 Processo de elicitação · 12.1 Glossário · 12.3 Dados da elicitação | **3.1** RF01 Gestão da AMAP e membros | Bruno |

### Secção 3 – System features
- Cada **3.x** corresponde a um ficheiro `docs/requisitos/RF0x_*` e segue o template: **Description**, **Stimulus/Response Sequences** e **Functional Requirements** (com ID, ator, prioridade, fonte e estado).
- Cada elemento adapta os seus ficheiros RF a este formato.
- O Bruno verifica a **coerência da secção 3**: mesmo formato, nenhum requisito repetido entre funcionalidades e referências cruzadas corretas (ex.: RF03 subscrições ↔ RF05 pagamentos).

## 2. Diagramas

| Diagrama | Secção do SRS | Responsável | Estado |
|---|---|---|---|
| Diagrama de contexto | 2.1 Product perspective | Liane | ✅ Existe (`docs/requisitos/diagramas/`) |
| **Diagrama de casos de uso geral** (todos os atores e casos de uso principais) | 2.2 User classes and characteristics | Liane | Por fazer |
| **Diagrama de casos de uso por funcionalidade** | Em cada 3.x, antes das sequências estímulo/resposta | Responsável de cada RF | Por fazer |
| Modelo lógico de dados (entidades, atributos, tipos e chaves) | 4.1 Logical data model | Bruno | 1.ª versão no modelo de domínio |
| Mapa de contextos (bounded contexts e relações) | 5.1 Domain model overview | Bruno | Por fazer |
| Diagrama por bounded context (Membros e AMAP · Ofertas e subscrições · Entregas · Pagamentos) | 5.2–5.4 | Bruno | Por fazer |
| Processo atual (as-is): Google Forms → Excel → WhatsApp → entrega → valor mensal | 12.2 Analysis models | Bruno | Por fazer |
| Processo proposto (to-be): o ciclo completo com a plataforma | 12.2 Analysis models | Bruno | Por fazer |
| *(Opcional)* Diagramas de sequência dos fluxos mais complexos | 3.x correspondente | Responsável de cada RF | Opcional |
| *(Opcional)* Diagrama de estados da entrega (por levantar → levantado / cedido / não levantado) | 3.4 ou 12.2 | Bruno | Opcional |

### Casos de uso: onde ficam
O template não tem uma secção própria para casos de uso. Proposta:
- **Um diagrama geral em 2.2**, para a visão de conjunto (junto ao diagrama de contexto da 2.1).
- **Um diagrama por funcionalidade em cada 3.x**: cada sequência estímulo/resposta corresponde a um caso de uso.
- O **diagrama de contexto** mostra o sistema e os **sistemas externos**; o **diagrama de casos de uso** mostra **o que cada ator faz** dentro do sistema. São complementares.
- **A confirmar com o professor** se quer casos de uso e onde.

### Como fazer os diagramas
- **Mermaid** dentro dos `.md`, exportado para PNG em `docs/requisitos/diagramas/imagens/`, como os que já existem.
- Para os processos as-is e to-be pode usar-se **BPMN** (draw.io ou bpmn.io), exportado para PNG.
- Cada diagrama tem versão **PT e EN**.

## 3. Regras comuns
- Cada elemento descreve **a sua técnica** na secção 10.2 e envia à Leonor as **suas horas** para a secção 10.3.
- Todos os requisitos indicam a **fonte** (entrevista, documento ou técnica) e a **prioridade**.
- Usar os IDs e a terminologia que já estão em `docs/requisitos/` (RF01–RF08, RNF) e no glossário.
- Cada secção tem versão **PT e EN**.
- Antes da defesa, fazer uma sessão em que cada elemento explica as suas secções aos restantes.

## 4. A decidir
- [ ] Aprovação desta divisão por todos os elementos.
- [ ] Onde se escreve o texto: Markdown no repositório (ex.: `docs/srs/`) e montagem final no `.docx`, ou diretamente num `.docx` partilhado.
- [ ] Quem monta o `.docx` final e garante a consistência.
- [ ] Prazo interno para as secções estarem prontas para revisão.
- [ ] Confirmar com o professor os casos de uso.

## Aprovação
| Elemento | Aprovo (✔) / Comentários |
|---|---|
| Bruno Alves | |
| Liane Duarte | |
| João Mata | |
| Jakub | |
| Leonor | |
