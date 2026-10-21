# Context and actors diagram

**Updated on:** 14/10/2026 · SRS section: 2.1 Product perspective

Shows who uses FAIR-AMAP, which features each actor uses and which external systems the platform communicates with. Payments and invoices stay **outside the system**, following scope proposal C6 (to validate).

**Image (for the SRS):** [imagens/DiagramaContextoEN.png](imagens/DiagramaContextoEN.png)

```mermaid
flowchart LR
    INT([Prospective member])
    COP([Co-producer])
    PROD([Producer])
    GEST([AMAP management<br/>working groups])
    ADM([FAIR administrator])
    INV([REGENERAR network /<br/>researchers])

    subgraph FAIR["FAIR-AMAP"]
        MEM[RF01 AMAP and<br/>member management]
        CAT[RF02 Catalogue<br/>and offers]
        SUB[RF03 Cycles and<br/>subscriptions]
        ENT[RF04 Calendar<br/>and deliveries]
        PAG[RF05 Payments]
        COM[RF06 Communication]
        CMD[RF07 Community]
        REL[RF08 Reports<br/>and indicators]
    end

    EMAIL[[Email service]]
    BANCO[[MB Way / bank<br/>outside the system]]
    FAT[[Producer's invoicing<br/>software]]

    INT --> MEM
    COP --> SUB & ENT & PAG & CMD
    PROD --> CAT & SUB & ENT & PAG & COM
    GEST --> MEM & SUB & ENT & COM & CMD & REL
    ADM --> MEM
    REL -. anonymised data .-> INV
    COM --> EMAIL
    COP -. pays directly .-> BANCO
    BANCO -. receives .-> PROD
    PROD -. issues invoice .-> FAT
    PAG -. records invoice number .- FAT
```

## Notes

- The **co-producer pays the producer directly** (bank transfer, MB Way or cash). The system only calculates, shows and records payments (RF-PAG-03 to 05).
- The **producer issues invoices in their own software**. The system only records the invoice reference (RF-PAG-07).
- **AMAP management** may be one person, a committee or several volunteer working groups (D-C §4.5).
