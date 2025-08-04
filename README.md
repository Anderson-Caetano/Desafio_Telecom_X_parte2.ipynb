# 📊 Análise de Evasão de Clientes (Churn) - Telecom X

Este projeto tem como objetivo investigar os fatores que influenciam a evasão de clientes (churn) em uma operadora de telecomunicações fictícia chamada **Telecom X**. Através de análise de dados, visualizações, engenharia de atributos e modelagem preditiva, buscamos entender o comportamento dos clientes e prever quais têm maior probabilidade de deixar a empresa.

---

## 🧠 Objetivos

- Explorar e tratar os dados de clientes da Telecom X.
- Identificar padrões associados à evasão.
- Construir modelos preditivos capazes de antecipar o churn.
- Oferecer insights e recomendações para reduzir a perda de clientes.

---

## 📁 Estrutura do Projeto

O projeto foi desenvolvido em um Jupyter Notebook, dividido em etapas claras:

### 1. 📌 Extração
- Leitura dos dados diretamente de uma URL externa em formato JSON.
- Conversão para DataFrame com pandas.

### 2. 🧼 Transformação
- Expansão de colunas aninhadas com `json_normalize`.
- Remoção de colunas irrelevantes.
- Padronização dos nomes de colunas.
- Codificação da variável churn (0 = ativo, 1 = evadiu).
- Aplicação de One-Hot Encoding.

### 3. 📊 Carga e Análise
- Verificação de dados nulos.
- Análise da distribuição da variável alvo.
- Visualização do desequilíbrio e aplicação do SMOTE.

### 4. ⚖️ Normalização
- Aplicada em modelos que requerem (ex: Regressão Logística).
- Uso do `StandardScaler`.

### 5. 🔁 Correlação
- Análise de variáveis numéricas com a variável alvo.
- Matriz de correlação com `seaborn`.

### 6. 📈 Exploração Visual
- Boxplots de comparação entre `tempo de contrato`, `valor mensal` e `churn`.
- Análise do número de serviços contratados.

### 7. ✂️ Divisão dos Dados
- Separação treino/teste (70/30) com preservação do balanceamento.

### 8. 🤖 Modelagem
- Modelos aplicados:
  - Regressão Logística
  - Random Forest
- Avaliação com:
  - Acurácia
  - Precisão
  - Recall
  - F1-score
  - ROC AUC
  - Matriz de Confusão

### 9. 💾 Salvamento e Predições
- Modelos salvos com `joblib`.
- Exemplo de uso em novos dados.

### 10. 📝 Relatório Final
- Sumário com introdução, tratamento dos dados, análises, insights e recomendações.

---

## 🔍 Principais Insights

- Clientes com **menor tempo de contrato** tendem a evadir mais.
- **Valores mensais mais altos** estão associados a maior churn.
- Menor número de **serviços contratados** = menor engajamento.
- **Random Forest** teve o melhor desempenho (ROC AUC ≈ 0.83).

---

## 📌 Tecnologias Utilizadas

- Python 3.11
- pandas
- seaborn
- matplotlib
- scikit-learn
- imblearn (SMOTE)
- joblib

---

## ▶️ Como Executar

```bash
git clone https://git@github.com:Anderson-Caetano/Desafio_Telecom_X_parte2.ipynb.git
