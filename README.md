Notebook de Análise e Previsão de Churn - TelecomX

Este notebook (telecomx_churn_analysis.ipynb) contém o pipeline completo para a análise e previsão de churn de clientes da TelecomX. Ele abrange desde o carregamento e pré-processamento dos dados até a modelagem, avaliação e otimização de modelos de Machine Learning.

Conteúdo do Notebook

O notebook está dividido nas seguintes seções:

1.
Configuração e Carregamento de Dados: Importação de bibliotecas e carregamento do dataset JSON, com desaninhamento das colunas aninhadas.

2.
Análise Exploratória de Dados (EDA): Exploração das distribuições das variáveis, identificação de valores ausentes e visualização da relação entre as features e a variável alvo (churn). Gráficos gerados são salvos em reports/figures/.

3.
Pré-processamento e Engenharia de Features: Limpeza dos dados, tratamento de valores ausentes, conversão de tipos e criação de novas features relevantes para a modelagem.

4.
Divisão de Dados e Pré-processamento com Pipeline: Divisão dos dados em conjuntos de treino e teste, e aplicação de transformações (escalonamento e One-Hot Encoding) usando ColumnTransformer e Pipeline para consistência. O pré-processador ajustado é salvo em models/.

5.
Modelagem e Avaliação: Treinamento e avaliação de modelos de Regressão Logística, Random Forest e XGBoost. Métricas como Acurácia, Precisão, Recall, F1-Score e AUC são calculadas. Os modelos treinados são salvos em models/ e um sumário de avaliação em reports/model_evaluation_summary.md.

6.
Otimização do Modelo e Análise de Resultados: Ajuste do threshold de classificação para o modelo de Regressão Logística (visando um recall específico) e otimização de hiperparâmetros para o Random Forest usando RandomizedSearchCV. Os modelos otimizados e o threshold são salvos em models/.

7.
Conclusão e Próximos Passos: Sumário das descobertas e sugestões para futuras etapas do projeto, como implementação em produção e monitoramento contínuo.

Como Executar

Para executar este notebook, siga os passos abaixo:

1.
Pré-requisitos: Certifique-se de ter o Python 3.8+ e o pip instalados.

2.
Ambiente Virtual: É altamente recomendado criar e ativar um ambiente virtual:

3.
Instalar Dependências: Instale todas as bibliotecas necessárias listadas no arquivo requirements.txt (localizado na raiz do projeto):

4.
Executar Jupyter: Navegue até o diretório telecomx_churn/notebooks/ e inicie o Jupyter Notebook ou JupyterLab:

5.
Abrir o Notebook: No navegador, abra o arquivo telecomx_churn_analysis.ipynb e execute as células sequencialmente.

Dados

O dataset original (Telco-Customer-Churn.json) deve estar localizado em telecomx_churn/data/raw/. Ele será automaticamente carregado pelo notebook.

Artefatos Gerados

Durante a execução do notebook, os seguintes artefatos serão gerados e salvos nas respectivas pastas:

•
data/processed/: Dados pré-processados (X_train, X_test, y_train, y_test).

•
models/: Modelos treinados (model_logistic_regression.pkl, model_random_forest.pkl, model_xgboost.pkl), o pré-processador (preprocessor.pkl), o threshold otimizado (optimal_threshold_lr.pkl) e o melhor modelo Random Forest otimizado (best_random_forest_model.pkl).

•
reports/figures/: Imagens geradas durante a EDA.

•
reports/model_evaluation_summary.md: Sumário da avaliação de todos os modelos.

Contribuição

Sinta-se à vontade para inspecionar, modificar e melhorar este notebook. Sugestões e pull requests são bem-vindos!

