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
| RF-REL-01 | O sistema deve permitir ao produtor exportar as encomendas e entregas para uma folha de cálculo. | Produtor | S | E-2 §2 (contas e planeamento em Excel) | Proposto |
| RF-REL-02 | O sistema deve calcular indicadores sobre os benefícios sociais e ambientais da AMAP. | Gestão | C | E-1 §3.4 ("nice to have, not a must"), D-D, D-E, DOC-37, N15 | Proposto |
| RF-REL-03 | O sistema deve permitir exportar dados para organizações da rede e investigadores, só anonimizados ou de membros que deram consentimento. | Gestão | C | E-1 §3.4, D-A (consentimento), RF-MEM-05, RGPD | Proposto |

## Critérios de aceitação

**RF-REL-01 – Exportar encomendas e entregas**
- A exportação pode ser filtrada por ciclo, data, AMAP e produto, em CSV ou XLSX (RNF-INT-02).
- Os valores devidos, recebidos e em atraso estão no RF-PAG-04.

**RF-REL-02 – Indicadores**
- Indicadores sociais: número de coprodutores, pessoas alimentadas, produtores apoiados e retenção entre ciclos.
- Indicadores ambientais (ex.: quilómetros percorridos, CO2, desperdício evitado).
- Servem os relatórios exigidos pelos projetos financiados das organizações que gerem as AMAP (E-1) e a avaliação de benefícios pedida pela Carta de Princípios (D-E).

**RF-REL-03 – Dados para a rede e investigadores**
- Só são exportados dados anonimizados ou de membros que deram consentimento (RF-MEM-05).

## Correspondência com a versão anterior
Na revisão de 28/10, os 5 requisitos anteriores foram reduzidos a 3, para reduzir o detalhe (indicação do professor). O detalhe passou para os critérios de aceitação.

| Novo | Junta os anteriores |
|---|---|
| RF-REL-01 | 01 |
| RF-REL-02 | 03, 04 |
| RF-REL-03 | 05 |
| *(RF-PAG-04)* | 02 (valores devidos, recebidos e em atraso, já cobertos pelo acompanhamento de pagamentos) |
