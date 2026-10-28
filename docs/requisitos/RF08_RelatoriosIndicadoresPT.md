# RF08 – Relatórios e indicadores

**Atualizado em:** 21/10/2026 · [Convenções e fontes](README.md)

## Descrição
Produz relatórios de trabalho para os produtores e a gestão (encomendas, pagamentos) e indicadores sobre os benefícios da AMAP para organizações da rede, financiadores e investigadores. O cliente (23/09) considerou os indicadores interessantes, mas não prioritários. A Carta de Princípios pede que as AMAP avaliem os seus benefícios de forma continuada e transparente.

## Sequências estímulo/resposta
- O produtor pede o relatório das encomendas do ciclo → o sistema gera-o e permite exportá-lo (substitui o Excel).
- A gestão pede os indicadores do ano → o sistema calcula o número de coprodutores, as pessoas alimentadas, os produtores apoiados e a retenção.
- Um investigador pede dados → só são exportados dados anonimizados ou de quem deu consentimento.

## Requisitos funcionais
| ID | Requisito | Ator | Prior. | Fonte | Estado |
|---|---|---|---|---|---|
| RF-REL-01 | O sistema deve permitir ao produtor exportar as encomendas e entregas (por ciclo, data, AMAP e produto) num formato de folha de cálculo. | Produtor | S | E-2 §2 | Proposto |
| RF-REL-02 | O sistema deve mostrar ao produtor, por mês, os valores devidos, recebidos e em atraso. | Produtor | S | E-2 §2, DV-19 | Proposto |
| RF-REL-03 | O sistema deve calcular indicadores dos benefícios da AMAP: número de coprodutores, pessoas alimentadas, produtores apoiados e retenção entre ciclos. | Gestão | S | D-D, D-E, E-1 §3.4, DOC-37, N15 | A validar (prioridade) |
| RF-REL-04 | O sistema deve calcular indicadores ambientais (ex.: quilómetros percorridos, CO2, desperdício evitado). | Gestão | C | E-1 (aula 1) | A validar (prioridade) |
| RF-REL-05 | O sistema deve permitir exportar dados para organizações da rede e investigadores, só anonimizados ou de membros que deram consentimento. | Gestão | C | E-1 §3.4, D-A (consentimento), RF-MEM-05 | Proposto |
