# Diagrama de contexto e atores

**Atualizado em:** 14/10/2026 · Secção do SRS: 2.1 Product perspective

Mostra quem usa a FAIR-AMAP, que funcionalidades usa cada ator e com que sistemas externos a plataforma comunica. Os pagamentos e as faturas ficam **fora do sistema**, segundo a proposta de âmbito C6 (a validar).

**Imagem (para o SRS):** [imagens/DiagramaContextoPT.png](imagens/DiagramaContextoPT.png)

```mermaid
flowchart LR
    INT([Interessado])
    COP([Coprodutor])
    PROD([Produtor])
    GEST([Gestão da AMAP<br/>grupos de trabalho])
    ADM([Administrador FAIR])
    INV([Rede REGENERAR /<br/>investigadores])

    subgraph FAIR["FAIR-AMAP"]
        MEM[RF01 Gestão da AMAP<br/>e membros]
        CAT[RF02 Catálogo<br/>e ofertas]
        SUB[RF03 Ciclos e<br/>subscrições]
        ENT[RF04 Calendário<br/>e entregas]
        PAG[RF05 Pagamentos]
        COM[RF06 Comunicação]
        CMD[RF07 Comunidade]
        REL[RF08 Relatórios<br/>e indicadores]
    end

    EMAIL[[Serviço de email]]
    BANCO[[MB Way / banco<br/>fora do sistema]]
    FAT[[Programa de faturação<br/>do produtor]]

    INT --> MEM
    COP --> SUB & ENT & PAG & CMD
    PROD --> CAT & SUB & ENT & PAG & COM
    GEST --> MEM & SUB & ENT & COM & CMD & REL
    ADM --> MEM
    REL -. dados anonimizados .-> INV
    COM --> EMAIL
    COP -. paga diretamente .-> BANCO
    BANCO -. recebe .-> PROD
    PROD -. emite fatura .-> FAT
    PAG -. regista nº da fatura .- FAT
```

## Notas
- **Cobrança centralizada** (proposta do grupo de 21/10): o coprodutor faz um só pagamento através de um **prestador de pagamentos licenciado**, que o divide pelos produtores; o sistema calcula, pede e regista os pagamentos, mas não guarda o dinheiro (RF-PAG-02 a 04, RNF-RES-02).
- A **faturação está fora do âmbito** (E-6): cada produtor emite as faturas no seu próprio programa (RNF-RES-01).
- A **gestão da AMAP** pode ser uma pessoa, uma comissão ou vários grupos de trabalho voluntários (D-C §4.5).
