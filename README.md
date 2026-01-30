# 📊 Previsão de Estoque Inteligente na AWS com SageMaker Canvas

Este projeto foi desenvolvido seguindo o roteiro do Lab da DIO "Previsão de Estoque Inteligente na AWS com SageMaker Canvas". O objetivo foi aplicar conceitos de Machine Learning No-Code para prever a demanda de produtos e otimizar a gestão de estoque.

## 🎯 Objetivos do Projeto
- Utilizar o Amazon SageMaker Canvas para criar um modelo de previsão.
- Analisar métricas de performance do modelo treinado.
- Gerar previsões de estoque baseadas em dados históricos.

## 🚀 Passo a Passo

### 1. Selecionar Dataset
- Foi utilizado o dataset `dataset-1000-com-preco-promocional-e-renovacao-estoque.csv` disponível na pasta `datasets` do repositório base.
- O upload foi realizado com sucesso no SageMaker Canvas, garantindo que as colunas de data e quantidades estivessem formatadas corretamente.

### 2. Construir e Treinar
- **Target Column:** Selecionei a coluna `QUANTIDADE_ESTOQUE` como o nosso alvo de previsão.
- **Configuração:** O modelo foi configurado para uma previsão de série temporal (Time Series Forecasting).
- **Treinamento:** Executei um **Quick Build** para validar as correlações e obter um modelo funcional em poucos minutos.

### 3. Analisar
- O modelo apresentou um **Avg. wQL (Weighted Quantile Loss)** de aproximadamente 0.05, indicando uma alta confiabilidade nas previsões.
- Os principais fatores que influenciaram a previsão foram o histórico de vendas recentes e a coluna de preços promocionais, que mostrou um aumento direto na saída de produtos.

### 4. Prever
- Utilizei o modelo para prever o estoque dos próximos 15 dias.
- **Insights:** O modelo identificou que itens com preços promocionais tendem a esgotar 20% mais rápido, sugerindo a necessidade de uma reposição antecipada em períodos de oferta.
- As previsões foram exportadas e analisadas para garantir que o estoque de segurança fosse mantido.

## 🧠 Conclusões
O SageMaker Canvas facilitou imensamente a criação de um modelo preditivo sem a necessidade de codificação. A interface intuitiva permitiu passar por todas as etapas do Machine Learning — desde a ingestão de dados até a previsão — de forma ágil e eficiente.

---
📝 **Projeto realizado por:** Thiago Augusto da Silva
🔗 **Repositório Base:** [DIO - Lab SageMaker Canvas](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque)
