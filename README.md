
# Projeto Alura Store — Análise das Lojas

## Propósito da análise
Este projeto analisa o desempenho de quatro lojas para ajudar o Sr. João a decidir qual delas deve ser vendida. Foram considerados:

- Faturamento total por loja
- Categorias de produtos mais e menos vendidas
- Média das avaliações dos clientes
- Produtos mais e menos vendidos
- Frete médio por loja
- Distribuição geográfica das vendas (latitude e longitude)

A análise foi feita em Python, usando Pandas e Matplotlib no Google Colab.

## Estrutura do projeto
AluraStoreBrasil/
- AluraStoreBrasil.ipynb (notebook principal com análise e gráficos)
- README.md (este documento explicativo)
- loja_1.csv
- loja_2.csv
- loja_3.csv
- loja_4.csv
- imagens/ (opcional: pasta para exportar figuras geradas)

## Exemplos de gráficos e insights

### Exemplos de gráficos (todos em Matplotlib)
- Barras: faturamento total por loja
- Linhas: comparação de volume por categoria entre lojas
- Pizza: participação dos produtos mais vendidos (Top 5)
- Hist2d (heatmap simples): concentração de vendas por latitude/longitude
- Dispersão por loja: pontos de vendas por localização (lon × lat)

### Principais insights resumidos
- A Loja 1 apresentou o maior faturamento; a Loja 4, o menor.
- Móveis e Eletrônicos foram, em geral, as categorias mais vendidas em todas as lojas.
- As avaliações médias ficaram próximas entre as lojas, com leve destaque para a Loja 3.
- Lojas 3 e 4 tendem a praticar frete médio mais baixo, o que ajuda na conversão.
- As vendas se concentram em algumas regiões; Lojas 3 e 4 mostraram maior presença nessas áreas densas.

### Conclusão prática (para o relatório)
- Se a meta é reduzir o ponto fraco operacional, vender a Loja 4 (menor desempenho).
- Se a meta é levantar mais capital para reinvestir, vender a Loja 1 (maior faturamento e valorização).

## Instruções para executar o notebook

### Passo a passo no Google Colab
1. Acesse: https://colab.research.google.com/
2. Abra o arquivo “AluraStoreBrasil.ipynb” (faça upload local ou abra direto do GitHub).
3. Verifique as importações no início do notebook:
   import pandas as pd
   import matplotlib.pyplot as plt
   (opcional) import seaborn as sns
   (opcional) folium para mapa interativo
4. Atenção ao formato brasileiro de números: ao ler os CSVs, use decimal=',' e encoding='utf-8', por exemplo:
   df = pd.read_csv('loja_1.csv', decimal=',', encoding='utf-8')
5. Execute as células em ordem (Menu → Executar tudo). Os gráficos aparecerão no próprio Colab.
6. (Opcional) Para salvar figuras, use:
   plt.savefig('imagens/nome_grafico.png', dpi=300)

### Observações úteis
- Se algum gráfico ficar muito comprimido, ajuste o figsize (ex.: plt.figure(figsize=(10,6))).
- Para tabelas, use df.head() e df.describe() para ver amostras e estatísticas.
- Se usar mapas interativos, instale folium no Colab (uma vez) com:
  !pip install folium

Fim.
