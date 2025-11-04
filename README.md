#### Predições Churn — Model Fitness


## Projeto de Análise e Predição de Rotatividade de Clientes

Este projeto foi desenvolvido como parte do curso de Análise de Dados da TripleTen, com o objetivo de ajudar a rede de academias Model Fitness a entender e reduzir a rotatividade de clientes (churn) por meio de análise exploratória de dados, modelagem preditiva e segmentação de clientes.


## Objetivos do Projeto

Prever a probabilidade de rotatividade dos clientes para o próximo mês.

Identificar padrões comportamentais e traçar o perfil dos clientes fiéis e dos que tendem a sair.

Encontrar os fatores mais relevantes que influenciam o churn.

Propor estratégias de retenção baseadas em insights obtidos a partir dos dados.


## Preparação e Modelagem dos Dados

O projeto conta com um processo completo de preparação e análise dos dados, realizado dentro do notebook principal.

As etapas incluem:

-> Carregamento dos dados brutos a partir do arquivo gym_churn_us.csv.

-> Limpeza, análise descritiva e padronização das variáveis para garantir a qualidade dos dados.

-> Modelagem, com treinamento e avaliação de algoritmos de classificação.

-> Clusterização, para segmentar clientes em grupos de comportamento semelhantes.


## Principais Insights

-> Distribuição de Características

-> Clientes mais jovens e com contratos curtos (1 mês) tendem a sair mais.

-> Aqueles com lifetime maior e frequência regular de treinos são mais leais.

-> Uma queda brusca na frequência de visitas no mês atual é um forte indicador de churn.

-> Clientes fiéis gastam mais em serviços adicionais, como café, massagem e produtos esportivos.


## Correlações Relevantes

A matriz de correlação revela os relacionamentos entre variáveis numéricas. Alguns destaques importantes:

-> Churn vs. Lifetime: correlação negativa forte (≈ -0.55) -> quanto maior o tempo na academia, menor a chance de churn.

-> Churn vs. Contract_period: também negativa (≈ -0.51) —> contratos mais longos reduzem a rotatividade.

-> Churn vs. Avg_class_frequency_current_month: negativa (≈ -0.47) —> menor frequência recente indica maior risco de saída.

-> Forte correlação entre frequência total e atual: clientes que costumam treinar mais, mantêm esse hábito.


## Modelagem Preditiva

Modelos Treinados: 

-> Regressão Logística

-> Random Forest Classifier

Desempenho (melhor modelo — Regressão Logística):

| Métrica                          | Resultado |
| -------------------------------- | --------- |
| **Acurácia**                     | 92.4%     |
| **Precision (classe 1 - churn)** | 88%       |
| **Recall (classe 1 - churn)**    | 81%       |

- A **Regressão Logística** apresentou ligeiramente **melhor desempenho em todas as métricas principais** para a classe mais importante (clientes que saíram).
- Portanto, este modelo é o mais indicado para uso prático, oferecendo bom equilíbrio entre precisão e sensibilidade na identificação de clientes em risco de churn.


### Taxa de Rotatividade por Cluster

Com base na variável `Churn`, identificamos os seguintes comportamentos de saída por agrupamento:

- **Cluster 0**: maior taxa de churn (53,9%) — grupo altamente desengajado. Ações urgentes de retenção são recomendadas.
- **Cluster 2**: também com alta taxa (47,7%) — representa outro grupo de risco que merece atenção.
- **Cluster 4**: churn moderado (26,7%) — pode ser estabilizado com comunicações e incentivos.
- **Cluster 3**: baixa taxa de churn (7,8%) — representa clientes leais.
- **Cluster 1**: menor churn (2,4%) — grupo mais estável e fiel da base.


## Recomendações Estratégicas

-> Incentivar contratos longos com descontos progressivos ou bônus.

-> Oferecer programas de fidelidade e benefícios para quem mantém alta frequência.

-> Criar alertas automáticos para clientes com queda na frequência mensal.

-> Promover serviços adicionais (massagem, café, etc.) para aumentar o engajamento.


## Conclusão

O projeto mostrou que é possível prever a rotatividade com alta precisão e segmentar os clientes de forma estratégica, permitindo que a Model Fitness tome decisões baseadas em dados para aumentar a retenção e reduzir o churn.


## Estrutura

```

📁 predicoes_model_fitness/
├── data/
│   └── gym_churn_us.csv
├── notebook/
│   └── predicoes_model_fitness.ipynb
├── requirements.txt
└── README.md

```


## Autor

Gustavo Savi
Junior Data Analyst
