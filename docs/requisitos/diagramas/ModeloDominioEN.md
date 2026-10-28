# Domain model

**Updated on:** 14/10/2026 · SRS sections: 4.1 Logical data model · 5 Domain model

First version, based on the entities identified in the [document analysis](../../tecnicas/ResultadosAnaliseDocumentalEN.md) (§3) and on requirements RF01–RF08. It shows only the entities, relationships and main attributes. The full data dictionary is left for SRS section 4.2.

**Image (for the SRS):** [imagens/ModeloDominioEN.png](imagens/ModeloDominioEN.png)

```mermaid
erDiagram
    AMAP ||--o{ PICKUP_POINT : "has"
    AMAP ||--o{ MEMBER : "has"
    AMAP ||--o{ CYCLE : "organises"
    AMAP ||--o{ DOCUMENT : "publishes"
    AMAP }o--o{ PRODUCER : "supplied by"
    PERSON ||--o{ MEMBER : "is"
    PERSON ||--o| PRODUCER : "represents"
    MEMBER ||--o{ CONSENT : "gives"
    MEMBER ||--o{ SUBSCRIPTION : "makes"
    MEMBER ||--o{ ABSENCE : "reports"
    MEMBER ||--o{ EXCLUSION : "records"
    PRODUCER ||--o{ PRODUCT : "offers"
    PRODUCT ||--o{ VARIANT : "has"
    CYCLE ||--o{ DELIVERY_DATE : "calendar"
    CYCLE ||--o{ OFFER : "includes"
    VARIANT ||--o{ OFFER : "offered in"
    SUBSCRIPTION ||--o{ SUBSCRIPTION_LINE : "contains"
    OFFER ||--o{ SUBSCRIPTION_LINE : "chosen in"
    DELIVERY_DATE ||--o{ DELIVERY : "generates"
    MEMBER ||--o{ DELIVERY : "receives"
    DELIVERY ||--o{ DELIVERED_ITEM : "contains"
    DELIVERY ||--o| COLLECTION : "confirmed by"
    ABSENCE }o--|| DELIVERY_DATE : "on"
    PRODUCER ||--o{ PAYMENT_NOTE : "issues"
    MEMBER ||--o{ PAYMENT_NOTE : "receives"
    PAYMENT_NOTE ||--o{ PAYMENT : "settled by"

    AMAP {
        string name
        string day_time
        string contact
        int places
    }
    PERSON {
        string name
        string email
        string mobile
        string tax_number "optional"
    }
    MEMBER {
        string role "co-producer, producer, management"
        string status "prospective, waiting, trial, active, left"
        int trial_deliveries
    }
    PRODUCER {
        string description
        string certification
        string payment_methods
        string vat_scheme
    }
    PRODUCT {
        string type "box, extra, loose"
        string frequency
        string price_type "monthly fee, unit, kg"
        int capacity
    }
    VARIANT {
        string name "tier, size"
        decimal price
    }
    CYCLE {
        date start
        date end
        date deadline
    }
    SUBSCRIPTION {
        string status "pending, confirmed"
        date date
    }
    DELIVERY {
        string status "planned, collected, not collected, absent"
        decimal actual_weight
    }
    ABSENCE {
        string destination "friend, donation, sharing, raffle"
    }
    COLLECTION {
        string collected_by
        datetime time
    }
    PAYMENT_NOTE {
        string period
        decimal amount
        string status "issued, paid, confirmed, overdue"
    }
    PAYMENT {
        string method
        date date
        string proof
    }
    CONSENT {
        string type "terms, guide, studies"
        string version
        date date
        date withdrawn_on
    }
```

## Notes
- **PERSON** and **MEMBER** are separate because the same person can be a member of several AMAPs with different roles (RF-MEM-01, RF-MEM-06).
- **OFFER** links a product/variant to a cycle and stores that cycle's price and capacity. This allows reusing the catalogue across cycles (RF-CAT-01).
- The **payment note** is per producer and per co-producer, because each producer is paid directly (RF-PAG-03).
- Still missing: working groups, rotas, events and indicators (RF07, RF08).
