
# Previsão de Churn — Telecom X

## 📌 Visão Geral

Este projeto tem como objetivo prever a evasão de clientes (churn) de uma empresa de telecomunicações, utilizando técnicas de machine learning. A solução foi desenvolvida com foco na análise exploratória, preparação de dados, escolha de modelo e avaliação preditiva.

---

## 🔍 Objetivo

Construir um modelo capaz de identificar clientes propensos a cancelarem seus contratos, permitindo à empresa agir preventivamente com estratégias de retenção.

---

## 🧩 Etapas do Projeto

- Importação e limpeza de dados
- Análise exploratória (EDA)
- Tratamento de variáveis categóricas
- Normalização de dados
- Construção e avaliação de modelos
- Exportação do modelo final

---

## 🧪 Modelos Avaliados

### 1. Regressão Logística

- Accuracy: 79.35%
- Precision: 63.52%
- Recall: 52.14%
- F1 Score: 57.27%
- ROC AUC: 0.8432

### 2. Random Forest

- Accuracy: 78.14%
- Precision: 61.87%
- Recall: 45.99%
- F1 Score: 52.76%
- ROC AUC: 0.8129

> **Conclusão**: A Regressão Logística apresentou melhor performance geral, com destaque no recall e na área sob a curva ROC, sendo escolhida como modelo final.

---

## 🔎 Principais Variáveis Relevantes

- Tipo de contrato (mensal tem maior churn)
- Método de pagamento (boleto e débito automático têm maior churn)
- Adesão a serviços adicionais (ausência de suporte técnico ou segurança está ligada ao churn)
- Tipo de serviço de internet
- Valor mensal da fatura

---

## 🧠 Estratégias de Retenção Sugeridas

- Incentivar contratos de maior duração (trimestral/anual)
- Oferecer pacotes com serviços de segurança e suporte
- Monitorar mensalmente os clientes com maior risco e agir com campanhas direcionadas

---

## 💾 Exportação do Modelo

O modelo final foi salvo utilizando a biblioteca `joblib`:

```python
import joblib
joblib.dump(modelo_lr, 'modelo_regressao_logistica.pkl')
```

Para carregar o modelo em produção:

```python
modelo_carregado = joblib.load('modelo_regressao_logistica.pkl')
```

---

## 🛠️ Tecnologias Utilizadas

- Python
- Pandas, NumPy
- Scikit-learn
- Seaborn, Matplotlib
- Joblib

---

❗Esse projeto faz parte da conclusão da 
