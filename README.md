# Telecom_X2_Alura_Parte2


📊 Relatório Técnico: Previsão de Evasão de Clientes (Churn) – Telecom X

🎯 Objetivo

Este projeto tem como finalidade prever a evasão de clientes (churn) da empresa fictícia Telecom X, utilizando técnicas de análise estatística e modelos de machine learning. Com base em dados históricos, o foco está em:

- Entender os principais fatores associados ao churn;
- Desenvolver modelos preditivos eficazes;
- Apoiar a empresa na redução da perda de clientes.

🔍 Etapas Desenvolvidas

- Limpeza e preparação dos dados
- Análise estatística e de correlação
- Regressão linear exploratória
- Construção de modelos preditivos
- Avaliação e comparação dos modelos

📈 Análise Estatística e Correlação

A análise estatística indicou forte correlação positiva entre a variável `account_charges_total` e a evasão de clientes.

Variáveis como tempo de contrato, tipo de serviço e uso de serviços adicionais também demonstraram associação significativa.

🤖 Modelos Preditivos

Foram utilizados dois modelos:

- **Regressão Logística**: simples, interpretável, servindo como baseline.
- **Random Forest**: modelo mais robusto, capaz de capturar interações complexas entre variáveis.

🔢 Métricas de Avaliação

| Modelo             | Acurácia | Precisão | Recall | F1-score |
|--------------------|----------|----------|--------|----------|
| Regressão Logística | 0.7365     | 0.0000  | 0.0000   | 0.0000     |
| Random Forest      |  0.6313     | 0.3073     | 0.3183   | 0.3127     |

🎯 Importância das variáveis (Random Forest)

- `account_charges_total`
- Tipo de contrato (`contract_type`)
- Tempo como cliente (`tenure`)
- Serviços adicionais contratados

✅ Conclusões da Análise Estatística

- Correlação positiva: `account_charges_total`, `streaming_services`, `monthly_charges`
- Correlação negativa: `tenure` (tempo de permanência), `contract_type=Two year`

A regressão linear exploratória apontou que maiores gastos mensais e totais estão associados a maior risco de churn.

🧠 Conclusão da Modelagem

- **Regressão Logística**: desempenho razoável, com boa capacidade de identificar casos de churn.
- **Random Forest**: modelo com melhor desempenho geral, superior em todas as métricas avaliadas.

Decisão final: utilizar o Random Forest como modelo principal para previsão de churn.

📌 Recomendações Estratégicas

- Criar campanhas de retenção para clientes com gastos totais elevados.
- Monitorar tipos de contrato e serviços mais associados ao churn.
- Oferecer benefícios personalizados para clientes com maior risco de evasão.
- Reavaliar pacotes com maior índice de insatisfação.

📂 Estrutura do Projeto

```bash
📦 telecom-x-churn-prediction/
├── data/
│   └── df_tratado.csv
├── notebooks/
│   ├── 01_exploratory_analysis.ipynb
│   ├── 02_modeling.ipynb
├── images/
│   └── confusion_matrix.png
├── churn_model.py
├── requirements.txt
└── README.md

