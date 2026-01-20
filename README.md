# Clustering de Ativos Big Tech (K-Means)

## Objetivo do Projeto
O objetivo deste projeto foi aplicar técnicas de **Aprendizado Não-Supervisionado** para agrupar as maiores empresas de tecnologia (Big Techs) com base em seus perfis de risco e retorno históricos.

## Metodologia e Pipeline
1. **Sincronização de Dados:** Os ativos foram sincronizados a partir do IPO da META, garantindo um período de análise comum para todos.
2. **Feature Engineering:** Cálculo de **Retorno Médio Anualizado** e **Volatilidade Anualizada**.
3. **Escalonamento:** Aplicação de `StandardScaler` para normalizar as grandezas.
4. **Otimização:** Uso do **Método do Cotovelo (Elbow Method)** para definir o número ideal de 3 clusters.

## Perfis Identificados
* **Cluster 0 (Roxo - "Conservadoras"):** Baixa volatilidade e retornos estáveis (ex: IBM, CSCO, INTC).
* **Cluster 1 (Amarelo - "Alta Volatilidade"):** Ativos de crescimento agressivo e risco elevado (ex: TSLA, NVDA, NFLX).
* **Cluster 2 (Verde - "Crescimento Sólido"):** Equilíbrio ideal entre risco e retorno (ex: AAPL, MSFT, GOOGL).


## Artefatos Gerados
* `models/kmeans_big_tech.pkl`: Modelo treinado.
* `models/cluster_scaler.pkl`: Scaler para novos dados.
* `notebooks/01_Clustering_Analysis.ipynb`: Notebook com todo o pipeline.