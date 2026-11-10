# Parte 2: Outliers de crescimento e notícias

Projeto Integrador Python e Matemática, **Indicador 3: População e Crescimento Demográfico**.
Parte individual do **Integrante 2** no painel da startup **Radar Urbano**.

**Pergunta de negócio:** onde estão os outliers de crescimento (cidades que cresceram exageradamente e cidades que encolheram)?

## Como rodar

```bash
pip install -r requirements.txt
streamlit run app.py
```

Para refazer a base tratada a partir dos arquivos do IBGE:

```bash
python etl/tratar_outliers.py
```

## Arquivos

| Arquivo | O que faz |
|---|---|
| `app.py` | Menu lateral, filtros (Região, UF, Porte) e upload |
| `etl/tratar_outliers.py` | ETL: junta Censo 2010 e 2022, calcula o crescimento e marca os outliers |
| `estatisticas.py` | Média, mediana, moda, quartis, IQR, amplitude, variância, desvio padrão |
| `secoes/outliers.py` | Tela de outliers: regra 1,5 × IQR, boxplot, efeito na média, ranking |
| `secoes/noticias.py` | Notícias e infográficos sobre transição demográfica |
| `dados/tratados/outliers_crescimento.csv` | Base tratada com a situação de cada município |
| `dados/tratados/limites_outliers_uf.csv` | Q1, Q3, IQR e limites de cada estado |
| `imagens/fotos/` | Coloque aqui fotos de expansão urbana (aparecem sozinhas na tela de notícias) |
| `ANALISE.md` | Análise descritiva |

## Regra de outlier

- IQR = Q3 - Q1
- Outlier se o crescimento for menor que Q1 - 1,5 × IQR ou maior que Q3 + 1,5 × IQR

Fonte: IBGE, Censos Demográficos 2010 e 2022 (SIDRA, tabela 4709).
