# Análise e Previsão de Churn de Clientes

Este projeto tem como objetivo analisar os fatores que influenciam a evasão de clientes (Churn) e desenvolver modelos preditivos para identificar clientes em risco.

## Sumário do Projeto

O projeto seguiu as seguintes etapas principais:

1.  **Preparação dos Dados**: Carregamento, limpeza (tratamento de valores ausentes e remoção de colunas irrelevantes) e pré-processamento (codificação de variáveis categóricas).
2.  **Análise Exploratória de Dados (AED)**: Análise de correlação para identificar as variáveis mais relevantes para a previsão de Churn.
3.  **Modelagem Preditiva**: Aplicação e avaliação de modelos de Machine Learning (Árvore de Decisão e Random Forest) para prever o Churn.
4.  **Avaliação de Modelos**: Comparação de desempenho dos modelos usando métricas relevantes (com foco no Recall) e análise de matrizes de confusão.
5.  **Identificação de Fatores de Churn e Estratégias de Retenção**: Baseado nos resultados da análise e modelagem, identificar os principais drivers de Churn e propor estratégias para reter clientes.

## Preparação dos Dados

Os dados foram carregados do arquivo `df_limpo.csv`. As etapas de limpeza incluíram a remoção da coluna `customerID` e a exclusão de linhas com valores ausentes nas colunas `Total.Day` e `account.Charges.Total`. Variáveis categóricas com "No internet service" foram padronizadas para "No". A codificação de variáveis categóricas foi realizada utilizando One-Hot Encoding para as features e Label Encoding para a variável alvo 'Churn'.

## Análise de Correlação

Uma análise de correlação foi realizada para entender a relação entre as variáveis e o Churn. As variáveis com maior correlação (positiva ou negativa) com 'Churn_encoded' foram identificadas e interpretadas.

*   **Fatores com maior correlação positiva com Churn:** Contrato Mês a Mês, Serviço de Internet Fibra Óptica, Método de Pagamento Cheque Eletrônico.
*   **Fatores com maior correlação negativa com Churn:** Tempo de Permanência, Contrato de Dois Anos, Ausência de Serviço de Internet.

## Modelagem Preditiva e Avaliação

Foram aplicados modelos de Árvore de Decisão e Random Forest. A avaliação foi focada na métrica Recall, considerando o maior custo de Falsos Negativos em problemas de Churn. O modelo de Árvore de Decisão com Under-sampling apresentou um desempenho promissor em termos de Recall na validação cruzada.

*(Detalhes adicionais sobre as métricas e comparação dos modelos podem ser adicionados aqui, se desejado)*

## Principais Fatores de Churn e Estratégias de Retenção

Com base na análise, os principais fatores que influenciam o Churn incluem o tipo de contrato, o serviço de internet utilizado, o método de pagamento e o tempo de permanência do cliente.

Foram propostas estratégias de retenção como:

*   Incentivar contratos de longo prazo.
*   Melhorar a qualidade e a percepção dos serviços de internet (especialmente Fibra Óptica).
*   Avaliar e otimizar métodos de pagamento (como Cheque Eletrônico).
*   Desenvolver programas de fidelidade e engajamento.



## Bibliotecas Utilizadas

As principais bibliotecas utilizadas neste projeto incluem:

*   pandas
*   seaborn
*   matplotlib
*   scikit-learn (sklearn)
*   imblearn
*   numpy

### RESUMO VERSÕES BIBLIOTECAS UTILIZADAS

| Biblioteca   | Versão                                          | Observação                                           |
| :----------- | :---------------------------------------------- | :--------------------------------------------------- |
| pandas       | 2.2.2                                           |                                                      |
| seaborn      | 0.13.2                                          |                                                      |
| matplotlib   | 3.10.0                                          |                                                      |
| scikit-learn | 1.6.1                                           |                                                      |
| imblearn     | 0.13.0                                          |                                                      |
| numpy        | 2.0.2                                           |                                                      |
| `python` | 3.11.13 (main, Jun 4 2025, 08:57:29) [GCC 11.4.0] |                                                      |

---
