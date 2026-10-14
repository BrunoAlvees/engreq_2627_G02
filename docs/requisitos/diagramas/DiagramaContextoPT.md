# Diagrama de contexto e atores

**Atualizado em:** 14/10/2026 · Secção do SRS: 2.1 Product perspective

Mostra quem usa a FAIR-AMAP, que funcionalidades usa cada ator e com que sistemas externos a plataforma comunica. Os pagamentos e as faturas ficam **fora do sistema**, segundo a proposta de âmbito C6 (a validar).

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
- O **coprodutor paga diretamente ao produtor** (transferência, MB Way ou numerário). O sistema só calcula, mostra e regista os pagamentos (RF-PAG-03 a 05).
- O **produtor emite as faturas no seu próprio programa**. O sistema só regista a referência da fatura (RF-PAG-07).
- A **gestão da AMAP** pode ser uma pessoa, uma comissão ou vários grupos de trabalho voluntários (D-C §4.5).
