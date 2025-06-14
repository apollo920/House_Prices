# Previsão de Preços de Imóveis com Machine Learning

Este projeto tem como objetivo desenvolver um modelo de Machine Learning para prever os preços de casas com base em diversas características dos imóveis, como número de quartos, área, localização, e qualidade geral. O dataset utilizado é o "House Prices" do Kaggle.

## Estrutura do Projeto

- `train.csv`: Conjunto de dados de treinamento.
- `test.csv`: Conjunto de dados de teste (para submissão, se aplicável).
- `sample_submission.csv`: Exemplo de arquivo de submissão.
- `data_description.txt`: Descrição detalhada das colunas do dataset.
- `script.py`: Script Python contendo todo o pipeline de análise, pré-processamento, treinamento e avaliação dos modelos.
- `report.pdf`: Relatório final com as conclusões e resultados dos modelos.
- `linear_regression_predictions.png`: Gráfico de dispersão das predições do modelo de Regressão Linear vs. valores reais.

## Etapas do Projeto

O projeto foi dividido nas seguintes fases:

1.  **Preparação do Ambiente e Obtenção dos Dados**: Carregamento dos datasets e configuração das bibliotecas necessárias.
2.  **Análise Exploratória dos Dados (EDA)**: Investigação das características dos dados, identificação de correlações entre variáveis (especialmente com `SalePrice`), e detecção/tratamento de outliers.
3.  **Pré-processamento e Preparação dos Dados**: Tratamento de valores ausentes, transformação de variáveis numéricas (logarítmica para `SalePrice` e variáveis com alta assimetria) e encoding de variáveis categóricas (One-Hot Encoding).
4.  **Criação e Treinamento de Modelos de Machine Learning**: Implementação e treinamento de três modelos de regressão: Regressão Linear, Árvore de Decisão e Random Forest.
5.  **Avaliação e Comparação dos Modelos**: Avaliação do desempenho dos modelos utilizando métricas como Root Mean Squared Error (RMSE) e Mean Absolute Error (MAE).
6.  **Visualização Final e Relatório de Conclusões**: Geração de gráficos de predição vs. real e um relatório detalhado dos resultados.

## Resultados

Os modelos foram avaliados com base no RMSE e MAE. O modelo de **Regressão Linear** apresentou o melhor desempenho entre os testados:

-   **Regressão Linear:**
    -   RMSE: 0.1410
    -   MAE: 0.0901
-   **Árvore de Decisão:**
    -   RMSE: 0.2005
    -   MAE: 0.1437
-   **Random Forest:**
    -   RMSE: 0.1431
    -   MAE: 0.0968

O gráfico `linear_regression_predictions.png` visualiza a performance do modelo de Regressão Linear, mostrando a proximidade das predições com os valores reais.

## Como Executar o Projeto

Para replicar este projeto, siga os passos abaixo:

1.  **Clone o repositório** (ou baixe os arquivos fornecidos).
2.  **Instale as dependências**:
    ```bash
    pip install pandas scikit-learn matplotlib seaborn
    ```
3.  **Execute o script Python**:
    ```bash
    python script.py
    ```
    Este script irá realizar todas as etapas de análise, pré-processamento, treinamento e avaliação, gerando o gráfico de predições e o relatório em PDF.

## Conclusão

Este projeto demonstra um pipeline completo para a previsão de preços de imóveis, desde a análise exploratória até a avaliação de modelos. A Regressão Linear se mostrou eficaz para este dataset, fornecendo predições com boa acurácia.


