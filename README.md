# Segmentação de clientes de um atacadista com K-Means

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/M4uroM4rcos/segmentacao-clientes-kmeans/blob/main/segmentacao_clientes.ipynb)

Projeto de mineração de dados que agrupa clientes de um atacadista pelo que eles compram, usando aprendizado não supervisionado (K-Means), e interpreta cada grupo para sugerir ações.

## Pergunta
Que tipos de cliente existem a partir do gasto em cada categoria de produto, e o que fazer com cada grupo?

## Principais resultados
O K-Means (k = 3) encontrou três perfis:

| Grupo | Clientes | Perfil |
|---|---|---|
| Grandes compradores | 147 | Gastam acima da média em todas as categorias |
| Mercado e limpeza | 80 | Muito em detergentes, papel e mercearia; pouco em frescos e congelados |
| Food service de frescos e congelados | 213 | Frescos e congelados na média; pouco em leite, mercearia e limpeza |

Descoberta principal: o grupo "Food service" é formado por 210 clientes do canal hotéis, restaurantes e cafés e só 3 do varejo. O modelo encontrou esse perfil sem usar a coluna de canal.

## Como foi feito
1. Exploração dos dados e consultas em SQL (SQLite).
2. Transformação logarítmica e padronização dos gastos.
3. Escolha do número de grupos com o método do cotovelo e o coeficiente de silhueta.
4. Agrupamento com K-Means e interpretação dos grupos.

## Limitações
- A silhueta ficou em cerca de 0,26, então os grupos se sobrepõem.
- Não há dados de preço nem de margem, então as ações sugeridas são hipóteses a serem testadas.

## Tecnologias
Python, pandas, scikit-learn, matplotlib, SQL (SQLite) e Google Colab.

## Como executar
Clique no botão "Abrir no Colab" acima e use **Ambiente de execução > Executar tudo**.

## Dados
Cardoso, M. (2013). Wholesale customers [Dataset]. UCI Machine Learning Repository. https://doi.org/10.24432/C5030X. Licença: CC BY 4.0.

## Autor
Mauro Marcos Oliveira Martins, [LinkedIn](https://www.linkedin.com/in/mauro-martins-19938b205)
