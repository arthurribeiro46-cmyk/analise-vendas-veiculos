# Análise de Vendas de Veículos — Ciência de Dados

## 1. Sobre o projeto

Este projeto aplica técnicas de Ciência de Dados e Machine Learning a um conjunto **sintético** de vendas de veículos usados. O objetivo é explorar os dados e construir modelos para responder a duas perguntas:

1. Quais características ajudam a explicar o preço de venda de um veículo?
2. É possível classificar se um veículo será vendido em até 30 dias?

O notebook foi desenvolvido em Python e pode ser executado no Google Colab ou em um ambiente Jupyter.

> **Importante:** o conjunto de dados padrão é sintético, gerado pelo próprio notebook para fins didáticos. Portanto, os resultados não devem ser interpretados como conclusões sobre o mercado real de veículos.

## 2. O que foi feito

- Análise exploratória dos dados: estrutura, estatísticas, valores ausentes, duplicatas e visualizações.
- Limpeza dos dados e tratamento de valores extremos.
- Preenchimento de valores ausentes e transformação de variáveis categóricas em variáveis numéricas.
- Análise de correlação entre variáveis.
- **Regressão linear múltipla** para estimar o preço de venda.
- **Classificação supervisionada** para prever venda rápida (até 30 dias), utilizando:
  - Regressão logística;
  - K vizinhos mais próximos (KNN);
  - Árvore de decisão;
  - Random Forest;
  - Gradient Boosting.
- Avaliação dos modelos por meio de métricas e visualizações, incluindo MAE, RMSE e R² para regressão e acurácia, precisão, recall, F1-score e matriz de confusão para classificação.

## 3. Tecnologias e bibliotecas

- Python
- Pandas e NumPy
- Matplotlib e Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

## 4. Como executar

### Opção A — Google Colab

1. Baixe o arquivo `vendas_veiculos_ciencia_de_dados.ipynb` deste repositório.
2. Acesse https://colab.research.google.com/.
3. Clique em **Arquivo → Fazer upload de notebook** e selecione o arquivo.
4. Execute as células em ordem, de cima para baixo.

O notebook gera automaticamente uma base sintética por padrão, então não é necessário baixar um arquivo de dados separado.

### Opção B — Jupyter local

1. Instale Python 3 e Jupyter Notebook.
2. Instale as bibliotecas utilizadas:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

3. Abra o notebook e execute as células em ordem.

## 5. Resumo dos resultados

Na execução registrada do notebook, a comparação dos classificadores apresentou os seguintes resultados:

| Modelo | Acurácia de teste | Precisão (classe 1) | Recall (classe 1) | F1-score (classe 1) |
|---|---:|---:|---:|---:|
| Regressão logística | 0,714 | 0,568 | 0,748 | 0,646 |
| KNN (k=37) | 0,698 | 0,637 | 0,316 | 0,422 |
| Árvore de decisão (profundidade=2) | 0,702 | 0,560 | 0,684 | 0,616 |
| Random Forest (grid) | 0,676 | 0,527 | 0,704 | 0,603 |
| Gradient Boosting | 0,731 | 0,654 | 0,485 | 0,557 |

Pelo critério de **F1-score da classe 1**, a regressão logística foi selecionada como o melhor classificador nesta execução, com F1-score de **0,646**. O Gradient Boosting apresentou a maior acurácia de teste nesta tabela (0,731), mostrando que o melhor modelo depende da métrica escolhida.

A regressão linear múltipla foi utilizada separadamente para estimar o preço de venda. Suas métricas de regressão são calculadas pelo notebook durante a execução.

> Os valores podem variar caso o código, os dados ou os parâmetros sejam alterados. Os resultados se referem ao conjunto sintético utilizado no projeto.

## 6. Limitações e próximos passos

- Validar os resultados com uma base real de vendas.
- Testar o modelo em dados novos que não tenham sido usados no treinamento ou na escolha de parâmetros.
- Explorar outros parâmetros e métodos de tratamento de dados.
- Investigar como o preço anunciado em relação ao mercado influencia a rapidez da venda.

## 7. Estrutura do repositório

```text
analise-vendas-veiculos/
├── vendas_veiculos_ciencia_de_dados.ipynb
└── README.md
```

## 8. Autor

Projeto acadêmico desenvolvido para a disciplina de Ciência de Dados.
