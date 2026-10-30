# RF08 – Relatórios e indicadores

**Atualizado em:** 28/10/2026 · [Convenções e fontes](README.md)

## Descrição
Produz relatórios de trabalho para os produtores e indicadores sobre os benefícios da AMAP para organizações da rede, financiadores e investigadores. O cliente (23/09) considerou os indicadores interessantes, mas "nice to have, not a must". A Carta de Princípios pede que as AMAP avaliem os seus benefícios de forma continuada e transparente.

## Sequências estímulo/resposta
- O produtor pede o relatório das encomendas do ciclo → o sistema gera-o e permite exportá-lo (substitui o Excel).
- A gestão pede os indicadores do ano → o sistema calcula o número de coprodutores, as pessoas alimentadas, os produtores apoiados e a retenção.
- Um investigador pede dados → só são exportados dados anonimizados ou de quem deu consentimento.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| FR-42 | O sistema deve permitir ao produtor exportar as encomendas e entregas para uma folha de cálculo. | Produtor | S | E-2 §2 (contas e planeamento em Excel) | Proposto |
| FR-43 | O sistema deve calcular indicadores sobre os benefícios sociais e ambientais da AMAP. | Gestão | C | E-1 §3.4 ("nice to have, not a must"), D-D, D-E, DOC-37, N15 | Proposto |
| FR-44 | O sistema deve permitir exportar dados para organizações da rede e investigadores, só anonimizados ou de membros que deram consentimento. | Gestão | C | E-1 §3.4, D-A (consentimento), FR-05, RGPD | Proposto |

## Critérios de aceitação

**FR-42 – Exportar encomendas e entregas**
- A exportação pode ser filtrada por ciclo, data, AMAP e produto, em CSV ou XLSX (NFR-16).
- Os valores devidos, recebidos e em atraso estão no FR-33.

**FR-43 – Indicadores**
- Indicadores sociais: número de coprodutores, pessoas alimentadas, produtores apoiados e retenção entre ciclos.
- Indicadores ambientais (ex.: quilómetros percorridos, CO2, desperdício evitado).
- Servem os relatórios exigidos pelos projetos financiados das organizações que gerem as AMAP (E-1) e a avaliação de benefícios pedida pela Carta de Princípios (D-E).

**FR-44 – Dados para a rede e investigadores**
- Só são exportados dados anonimizados ou de membros que deram consentimento (FR-05).

## Correspondência com a versão anterior
Na revisão de 28/10, os 5 requisitos anteriores foram reduzidos a 3, para reduzir o detalhe (indicação do professor). O detalhe passou para os critérios de aceitação.

| Novo | Junta os anteriores |
|---|---|
| FR-42 | 01 |
| FR-43 | 03, 04 |
| FR-44 | 05 |
| *(FR-33)* | 02 (valores devidos, recebidos e em atraso, já cobertos pelo acompanhamento de pagamentos) |
