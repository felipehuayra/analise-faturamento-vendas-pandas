
# Análise de Faturamento de Vendas com Pandas

Projeto de análise exploratória de dados de vendas, desenvolvido em Python com a biblioteca **pandas**, como exercício prático após um curso sobre a biblioteca.

O objetivo foi pegar uma base de vendas "crua" (com dados faltantes, texto bagunçado e tipos incorretos) e transformá-la em informações úteis para tomada de decisão: ranking de lojas, produtos mais vendidos, cumprimento de metas por gerente e evolução do faturamento ao longo do tempo.

## Dados utilizados

- `vendas_tech.csv` — histórico de pedidos (loja, produto, quantidade, preço unitário, cliente, data)
- `gerentes_lojas.xlsx` — gerente responsável e meta mensal de cada loja

## Tratamento e limpeza dos dados

- Remoção de colunas irrelevantes
- Preenchimento de valores nulos na coluna "Loja" (vendas sem loja associada → "Online")
- Conversão da coluna de data para o tipo `datetime`
- Padronização de texto (remoção de espaços extras, capitalização consistente)
- Remoção de pedidos duplicados

## Enriquecimento dos dados

- Cálculo do **faturamento** por pedido (quantidade × preço unitário)
- Classificação da venda em **Online** ou **Presencial**
- Mapeamento de cada loja para sua **região** (Sudeste, Nordeste, Sul)

## Análises realizadas

- Ranking de faturamento por loja
- Produtos mais vendidos no canal online
- Cruzamento de vendas por loja e por produto
- Filtros específicos (ex: vendas de um produto em uma região, vendas a partir de determinado ano)
- Comparação entre faturamento mensal por loja e meta estabelecida, identificando quais gerentes bateram a meta em um período
- Evolução do faturamento mês a mês

## Ferramentas

- Python
- pandas
- numpy
- matplotlib (visualização)

## Como executar

1. Clone este repositório
2. Instale as dependências:
   ```bash
   pip install pandas numpy matplotlib openpyxl
   ```
3. Abra o notebook `analise_vendas.ipynb` em um Jupyter Notebook ou IDE

## Status

Projeto de estudo, feito para consolidar conceitos de limpeza, transformação e análise de dados com pandas.
