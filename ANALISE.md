# Análise descritiva: outliers de crescimento (Integrante 2)

**Base:** 2.458 municípios de BA, MG, PR, RS e SC, crescimento acumulado entre o Censo 2010 e o Censo 2022.

## Cálculo dos limites (todos os estados juntos)

| Medida | Valor |
|---|---|
| Q1 | -5,91% |
| Q3 | 7,99% |
| IQR = Q3 - Q1 | 13,90 p.p. |
| Limite inferior = Q1 - 1,5 × IQR | -26,75% |
| Limite superior = Q3 + 1,5 × IQR | 28,83% |

Qualquer cidade fora da faixa de -26,75% a 28,83% é outlier.

## Resultado

- **94 cidades cresceram exageradamente.** As maiores: Itapoá/SC (+108%), Barra Velha/SC (+103%), Passo de Torres/SC (+95%) e Extrema/MG (+87%).
- **11 cidades encolheram demais.** As maiores quedas: Caatiba/BA (-45,7%) e Ubatã/BA (-35,6%).
- **91% dos outliers que encolheram são cidades pequenas**, de até 20 mil habitantes. Em cidade pequena, poucas pessoas saindo já mudam muito o percentual.

## Efeito dos outliers na média e na mediana

| | Média | Mediana |
|---|---|---|
| Com outliers | 2,55% | 0,77% |
| Sem outliers | 0,96% | 0,23% |

Sem os outliers, a média cai **1,59 p.p.** e a mediana muda só **0,54 p.p.** Isso mostra na prática que a **média é sensível a valores extremos** e a **mediana é robusta**.

## Outliers dentro de cada estado

Quando cada estado tem seus próprios limites: MG tem 30 outliers, BA 17, SC 17, RS 16 e PR 9. Santa Catarina tem o limite superior mais alto (47,24%), porque lá crescer muito é comum, principalmente no litoral.

## Interpretação para os prefeitos

Os outliers não são erro: são cidades reais que precisam de política própria. As que cresceram demais (litoral catarinense, polos industriais) precisam correr com saneamento, mobilidade e moradia. As que encolheram precisam de atenção a serviços para uma população menor e mais velha. Por isso recomendamos usar a mediana como referência e tratar os outliers como casos especiais no planejamento.
