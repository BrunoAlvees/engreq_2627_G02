# Diagrama de contexto e atores

**Atualizado em:** 28/10/2026 · Secção do SRS: 2.1 Product perspective

Mostra quem usa a FAIR-AMAP, que funcionalidades usa cada ator e com que sistemas externos a plataforma comunica. A cobrança é **centralizada através de um prestador de pagamentos licenciado** (proposta do grupo de 21/10) e a **faturação está fora do âmbito** (E-6).

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
    PUSH[[Notificações push<br/>no telemóvel - PWA]]
    PSP[[Prestador de pagamentos<br/>licenciado - MB Way,<br/>Multibanco, cartão]]

    INT --> MEM
    COP --> SUB & ENT & PAG & CMD
    PROD --> CAT & SUB & ENT & PAG & COM
    GEST --> MEM & SUB & ENT & COM & CMD & REL
    ADM --> MEM & PAG
    REL -. dados anonimizados .-> INV
    COM --> EMAIL & PUSH
    PAG -- pedido de pagamento --> PSP
    COP -. paga uma vez .-> PSP
    PSP -. confirma o pagamento .-> PAG
    PSP -. divide e transfere .-> PROD
```

## Notas
- **Cobrança centralizada** (proposta do grupo de 21/10): o coprodutor faz um só pagamento através de um **prestador de pagamentos licenciado**, que o divide pelos produtores; o sistema calcula, pede e regista os pagamentos, mas não guarda o dinheiro (RF-PAG-02 a 04, RNF-RES-02).
- A **faturação está fora do âmbito** (E-6): cada produtor emite as faturas no seu próprio programa (RNF-RES-01).
- As **notificações** chegam por email e, se o utilizador as ativar, por push no telemóvel (RNF-INT-01).
- O **administrador FAIR** usa os pagamentos para calcular o valor que a FAIR cobra (RF-PAG-05).
- A **gestão da AMAP** pode ser uma pessoa, uma comissão ou vários grupos de trabalho voluntários (D-C §4.5).
