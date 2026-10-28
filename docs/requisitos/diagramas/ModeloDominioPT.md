# Modelo de domínio

**Atualizado em:** 14/10/2026 · Secções do SRS: 4.1 Logical data model · 5 Domain model

Primeira versão, a partir das entidades identificadas na [análise documental](../../tecnicas/ResultadosAnaliseDocumentalPT.md) (§3) e dos requisitos RF01–RF08. Mostra só as entidades, as relações e os atributos principais. O dicionário de dados completo fica para a secção 4.2 do SRS.

**Imagem (para o SRS):** [imagens/ModeloDominioPT.png](imagens/ModeloDominioPT.png)

```mermaid
erDiagram
    AMAP ||--o{ PONTO_ENTREGA : "tem"
    AMAP ||--o{ MEMBRO : "tem"
    AMAP ||--o{ CICLO : "organiza"
    AMAP ||--o{ DOCUMENTO : "publica"
    AMAP }o--o{ PRODUTOR : "abastecida por"
    PESSOA ||--o{ MEMBRO : "é"
    PESSOA ||--o| PRODUTOR : "representa"
    MEMBRO ||--o{ CONSENTIMENTO : "dá"
    MEMBRO ||--o{ SUBSCRICAO : "faz"
    MEMBRO ||--o{ AUSENCIA : "declara"
    MEMBRO ||--o{ EXCLUSAO : "regista"
    PRODUTOR ||--o{ PRODUTO : "oferece"
    PRODUTO ||--o{ VARIANTE : "tem"
    CICLO ||--o{ DATA_ENTREGA : "calendário"
    CICLO ||--o{ OFERTA : "inclui"
    VARIANTE ||--o{ OFERTA : "oferecida em"
    SUBSCRICAO ||--o{ LINHA_SUBSCRICAO : "contém"
    OFERTA ||--o{ LINHA_SUBSCRICAO : "escolhida em"
    DATA_ENTREGA ||--o{ ENTREGA : "gera"
    MEMBRO ||--o{ ENTREGA : "recebe"
    ENTREGA ||--o{ ITEM_ENTREGUE : "contém"
    ENTREGA ||--o| LEVANTAMENTO : "confirmado por"
    AUSENCIA }o--|| DATA_ENTREGA : "em"
    PRODUTOR ||--o{ NOTA_PAGAMENTO : "emite"
    MEMBRO ||--o{ NOTA_PAGAMENTO : "recebe"
    NOTA_PAGAMENTO ||--o{ PAGAMENTO : "liquidada por"

    AMAP {
        string nome
        string dia_horario
        string contacto
        int vagas
    }
    PESSOA {
        string nome
        string email
        string telemovel
        string nif "opcional"
    }
    MEMBRO {
        string papel "coprodutor, produtor, gestão"
        string estado "interessado, em espera, experiência, ativo, saído"
        int entregas_experimentais
    }
    PRODUTOR {
        string descricao
        string certificacao
        string meios_pagamento
        string regime_iva
    }
    PRODUTO {
        string tipo "cabaz, extra, avulso"
        string periodicidade
        string tipo_preco "quota mensal, unidade, kg"
        int capacidade
    }
    VARIANTE {
        string nome "escalão, tamanho"
        decimal preco
    }
    CICLO {
        date inicio
        date fim
        date data_limite
    }
    SUBSCRICAO {
        string estado "pendente, confirmada"
        date data
    }
    ENTREGA {
        string estado "prevista, levantada, não levantada, ausente"
        decimal peso_real
    }
    AUSENCIA {
        string destino "amigo, doação, distribuição, sorteio"
    }
    LEVANTAMENTO {
        string levantado_por
        datetime hora
    }
    NOTA_PAGAMENTO {
        string periodo
        decimal valor
        string estado "emitida, paga, confirmada, em atraso"
    }
    PAGAMENTO {
        string meio
        date data
        string comprovativo
    }
    CONSENTIMENTO {
        string tipo "termos, guia, estudos"
        string versao
        date data
        date retirado_em
    }
```

## Notas
- **PESSOA** e **MEMBRO** estão separados porque a mesma pessoa pode ser membro de várias AMAP com papéis diferentes (RF-MEM-01, RF-MEM-06).
- **OFERTA** liga um produto/variante a um ciclo e guarda o preço e a capacidade desse ciclo. Permite reutilizar o catálogo entre ciclos (RF-CAT-01).
- A **nota de pagamento** é por produtor e por coprodutor, porque cada produtor recebe diretamente (RF-PAG-03).
- Ainda faltam: grupos de trabalho, escalas, eventos e indicadores (RF07, RF08).
