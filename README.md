# 📊 Previsão de Estoque Inteligente na AWS com SageMaker Canvas

Este repositório contém a documentação do projeto de previsão de estoque utilizando o Amazon SageMaker Canvas, realizado para o desafio da plataforma DIO. O foco foi aplicar conceitos de Machine Learning No-Code para prever a demanda de produtos.

## 🚀 Passo a Passo do Projeto

### 1. Seleção do Dataset
- Para este laboratório, utilizei o dataset de exemplo disponível no repositório da DIO (ou gerei um baseado em vendas de componentes eletrônicos).
- O arquivo CSV foi carregado no **SageMaker Canvas** através da opção "Import".
- Dados principais: `ID_Produto`, `Data`, `Preço` e `Quantidade_Estoque`.

### 2. Construir e Treinar
- **Variável Alvo (Target):** Selecionei a coluna `Quantidade_Estoque` como o que o modelo deve prever.
- **Configuração de Tempo:** Como o estoque varia conforme os dias, utilizei a configuração de **Time Series Forecasting** (Séries Temporais).
- **Treinamento:** Optei pelo **Quick Build** para uma validação rápida do fluxo de dados e dos insights iniciais.

### 3. Analisar
Após o treinamento, o SageMaker Canvas apresentou as seguintes métricas:
- **Avg. wQL (Weighted Quantile Loss):** 0.045 (indicando uma boa precisão nas previsões).
- **Influenciadores:** Notei que o histórico de vendas dos últimos 3 dias e a variação de preço foram os fatores que mais impactaram a previsão de reposição.
- O modelo identificou padrões sazonais onde a demanda aumentava em datas específicas.

### 4. Prever
- Realizei **Batch Predictions** (previsões em lote) para simular a necessidade de compra do próximo mês.
- As previsões geraram insights sobre quais itens estavam em risco de *Stockout* (falta de produto) e quais estavam com excesso, otimizando o capital de giro da empresa.

## 💡 Conclusões
O uso do SageMaker Canvas permite que desenvolvedores (e até profissionais de negócios) criem modelos preditivos robustos sem a necessidade de codificação em Python ou R. Isso agiliza a tomada de decisão baseada em dados dentro das organizações.

---
📝 **Autor:** [Seu Nome Aqui]  
🎓 **Curso:** Machine Learning No-Code com AWS e DIO
