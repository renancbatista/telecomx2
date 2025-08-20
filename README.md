# Previsão de Churn – Telecom X

## Objetivo
Desenvolver um modelo para identificar clientes com alto risco de cancelamento (*churn*), permitindo ações proativas de retenção.

---

## Etapas Realizadas
1. Importação e limpeza dos dados.
2. Análise exploratória (histogramas, barras, correlações, etc.).
3. Engenharia de features — criação de novas variáveis informativas.
4. Preparação dos dados — codificação, normalização, balanceamento (p.ex. SMOTE).
5. Treinamento e avaliação de múltiplos modelos (Regressão Logística, Random Forest, XGBoost).
6. Escolha do modelo final e ajuste de threshold para priorizar recall.
7. Salvamento dos artefatos com `pickle` ou `joblib`.
8. Insights e recomendações baseadas nas variáveis mais importantes.

---

## Resultados do Modelo
- Métricas comparativas (accuracy, precision, recall, F1, ROC AUC) para cada modelo.
- Interpretabilidade: variáveis com maior impacto no churn.
- Gráfico ROC comparando modelos.
- Estratégia de threshold otimizada para identificar o máximo possível de clientes que cancelarão.

---

## Como Executar
1. Baixe o repositório.
2. No terminal ou Jupyter, execute o notebook `TelecomX_Churn_Prediction.ipynb`.
3. Os artefatos serão salvos com `joblib` ou similar.
4. Insira os insights do modelo no README e no notebook para contextualização estratégica.

---

