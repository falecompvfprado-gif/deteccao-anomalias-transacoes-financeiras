# Detecção de Anomalias em Transações Financeiras

Este repositório contém o desafio de projeto desenvolvido para o **Bootcamp Bradesco - GenAI, Dados e Cyber** na plataforma [DIO](https://www.dio.me/). O objetivo principal é construir e avaliar modelos de Machine Learning para identificar transações fraudulentas em cartões de crédito.

## 🎯 Objetivo do Projeto

A detecção de fraudes é um problema clássico de classificação com dados altamente desbalanceados (onde as fraudes representam menos de 0,2% do total). Este projeto aborda o pipeline completo de Ciência de Dados para resolver esse problema, desde a análise inicial até a explicabilidade do modelo final.

## 🛠️ Tecnologias e Bibliotecas Utilizadas

- **Python 3**
- **Pandas** e **NumPy**: Manipulação e análise de dados.
- **Matplotlib**: Visualização de gráficos.
- **Scikit-Learn**: Pré-processamento, divisão de dados e modelos (Regressão Logística e Random Forest).
- **Imbalanced-Learn (SMOTE)**: Balanceamento de dados por oversampling.
- **XGBoost**: Algoritmo avançado de classificação por Gradient Boosting.
- **SHAP (SHapley Additive exPlanations)**: Explicabilidade do modelo.

## 📊 Etapas do Desenvolvimento

1. **Análise e Pré-processamento:** Identificação do desbalanceamento extremo e normalização das variáveis de valores (`Amount`).
2. **Modelagem Base:** Treinamento de uma Regressão Logística e avaliação através de Curvas ROC e Precision-Recall.
3. **Tratamento de Desbalanceamento:** Demonstração teórica de *Undersampling* e aplicação prática do *Oversampling* com **SMOTE**.
4. **Modelos Avançados:** Implementação e comparação do **Random Forest** (com pesos balanceados) e **XGBoost**.
5. **Importância das Variáveis:** Visualização das *features* que mais impactaram o modelo.
6. **Explicabilidade com SHAP:** Uso de valores SHAP para entender o comportamento das predições de forma transparente.

## 🏆 Resultados obtidos

O **XGBoost** apresentou o melhor desempenho geral para o problema de negócio:
- **Precisão:** 0.93 (Minimiza falsos positivos, evitando o bloqueio indevido de clientes legítimos).
- **Recall:** 0.78 (Maximiza a captura de fraudes reais).
