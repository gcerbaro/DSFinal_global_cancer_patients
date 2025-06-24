## Descrição do Projeto
Trabalho final para a disciplina de Data Science - UPF 2025/1.
Este projeto busca prever a gravidade da condição de pacientes oncológicos através das características demográficas e clínicas
presentes em um dataset com dados coletados entre 2015 e 2024 através de um modelo de machine learning de aprendizado supervisionado. Para isso, além da própria modelagem, o projeto também conta com análise exploratória e normalização dos dados.

O projeto inclui:

- Visualizações gráficas para análise dos principais aspectos do dataset;
- Limpeza e preparação dos dados;
- Modelos de Machine Learning para predição do tipo de câncer;
- Discussão dos resultados e conclusões.

# Url no github
- [text](https://github.com/gcerbaro/DSFinal_global_cancer_patients)

---

## 

- **Origem:**  
[text](https://www.kaggle.com/datasets/zahidmughal2343/global-cancer-patients-2015-2024/data)

O dataset utilizado contém 50.000 registros de pacientes com câncer, com 14 colunas de dados que cobrem desde informações de ambiente (poluição do ar), de estilo de vida (tabagismo, consumo de álcool), estágio da doença, custo de tratamento e demais dados demográficos. O dataset conta com registros recolhidos de pacientes ao redor do mundo entre 2015 e 2024.

- **Variáveis Principais:**

| Variável           | Tipo        | Descrição                                      |
|--------------------|-------------|------------------------------------------------|
| Cancer_Type        | Categórica  | Tipo do câncer diagnosticado                     |
| Survival_Years     | Numérica    | Tempo médio de sobrevivência em anos            |
| Treatment_Cost_USD | Numérica    | Custo médio do tratamento em dólares             |
| Age                | Numérica    | Idade do paciente                                |
| Country_Region     | Categórica  | País ou região do paciente                        |
| Cancer_Stage       | Ordinal     | Estágio do câncer (1 a 5)                        |
| Genetic_Risk       | Numérica    | Índice de risco genético                          |
| Alcohol_Use        | Numérica    | Nível de uso de álcool                            |
| Gender             | Categórica  | Gênero do paciente (Male, Female, Other)        |

- **Transformações Realizadas:**
  - Filtragem de outliers usando Z-score (limite de 3 desvios padrão) aplicada apenas nas colunas numéricas para garantir qualidade dos dados.
  - Aplicação de *One Hot Encoding* para variáveis categóricas: `Cancer_Type`, `Gender`, e `Country_Region`, facilitando análises quantitativas e correlações.
  - Agrupamentos e cálculo de médias para gerar insights resumidos.

---
## Limpeza e normalização
Para realizar a limpeza e normalização do dataset foram utilizadas algumas técnicas para garantir melhor qualidade em analise posterior, dentre estas estao:

- **Remoção**: remoção de dados nulos, duplicados e irrelevantes para treinamento do modelo.
- **Tratamento**: tratamento de variaveis categoricas, com One Hot Encoding, e ordianais, convertidos para escala numerica.
- **Filtro**: filtragem de outliers via usando IQR para distringuir quais valores eram distorcidos da maioria.
- **Normalização**: normalização dos dados para facilitar o treinamento do modelo utilizando Min-Max Scaling, que converte todos os valores numericos para um intervalo entre 0 e 1.

---

## Resultados Obtidos

1. Tipos de Câncer por Média de Sobrevivência
Gráfico de barras mostrando os tipos de câncer com maior tempo médio de sobrevivência.

  - ![Image](https://github.com/user-attachments/assets/df33ff37-7c2e-4866-9ef0-5013ff13fab2)

2. Tipos de Câncer por Risco Genético Médio
Mostra quais tipos de câncer possuem maior risco genético associado.

  - ![Image](https://github.com/user-attachments/assets/d661ed92-960e-4d6f-b26e-2006832d69a6)

3. Média de Sobrevivência por Gênero
Compara o tempo médio de vida após diagnóstico entre gêneros.

  - ![Image](https://github.com/user-attachments/assets/577014ca-9cb6-4edf-bdc4-c37564714611)

4. Média da Idade por Estágio do Câncer
Associação entre idade média dos pacientes e estágio da doença.

  - ![Image](https://github.com/user-attachments/assets/ed8d364c-00f8-4f02-b32b-86110ad9608f)


5. Distribuição da Idade dos Pacientes
Histograma mostrando a faixa etária predominante entre os pacientes.

  - ![Image](https://github.com/user-attachments/assets/0ed8d763-86d5-4794-8054-b6e551a65651)


6. Distribuição do Custo de Tratamento
Análise da frequência dos diferentes custos de tratamento.

  - ![Image](https://github.com/user-attachments/assets/e0a48e7f-2d4c-4c7e-a4db-d9b35829190b)


7. Sobrevivência x Custo do Tratamento
Gráfico de dispersão que analisa a relação entre custo e tempo de vida.

  - ![Image](https://github.com/user-attachments/assets/4050b3c4-ea9b-4b47-9174-c9bc2586af40)


8. Distribuição por Gênero
Gráfico de pizza com a proporção de pacientes por gênero.

  - ![Image](https://github.com/user-attachments/assets/c60e2b24-5480-4acd-a10b-a39bc14298ae)


9. Correlação com Target_Severity_Score
Barplot com as variáveis mais correlacionadas com a gravidade dos casos.

  - ![Image](https://github.com/user-attachments/assets/a2b1acaf-0575-40b4-9a33-a2812b8ae0a5)


10. Média de Sobrevivência por Gênero (One Hot Encoding)
Exibe os resultados médios de sobrevivência a partir das variáveis codificadas.

  - ![Image](https://github.com/user-attachments/assets/3f58c162-7c84-40f7-9dfe-1cc47a87ace3)


11. Dispersão: Fatores de Risco x Target_Severity_Score
Regplots comparando fatores de risco como tabagismo, álcool, risco genético, etc. com a gravidade.

  - ![Image](https://github.com/user-attachments/assets/07562eb5-b2af-4ff2-91f8-a6e2e4b8c332)


12. Variáveis Correlacionadas com a Severidade
Visualização multivariada para explorar correlações simultâneas.

  - ![Image](https://github.com/user-attachments/assets/744ea238-4225-45a6-a606-bf37ffbe4c85)

13. Severidade Média por Tipo de Câncer e Gênero
Mostra como a gravidade varia entre homens e mulheres por tipo de câncer.

  - ![Image](https://github.com/user-attachments/assets/2c6ac3a5-2232-4389-bf27-62f2d0d6568b)


14. Sobrevivência por Estágios do Câncer
Mostra a tendência de sobrevivência para cada estágio da doença.

  - ![Image](https://github.com/user-attachments/assets/c995e3f2-e647-4d70-ad8c-6d9f4885ad0f)

---

## Modelagem
- Utilizado modelo de machine learning do tipo aprendizado supervisionado
- Random Forest Regressor
- 100 árvores utilizadas e a média das predições das árvores individuais gerou o resultado final.
- Resultados avaliados através de MSE, R², dispersão Real X Previsto e distribuição de erros. 

---

## Resultados

- O Erro Quadrado Médio (MSE) igual a 0.0007.
- O Coeficiente de Determinação (R²) de 0.9778 ou 97.8% .
- A partir do gráfico de dispersão Real x Previsto verificou-se que a distribuição dos valores seguiram
conforme à linha central, o que indica pouca discrepância entre os valores reais e os previstos pelo modelo e boa generalização.
- A distribuição dos erros concentrou-se em torno ao zero, com poucos outliers, distribuição simétrica e desvio padrão pequeno, indicando erros pequenos e aleatórios, ou seja, sem um viés específico.
- O modelo obteve bons resultados e aparenta ser capaz de avaliar a gravidade da doença enfrentada por um paciente, podendo auxiliar na escolha do tratamento mais eficiente ou na escolha de medidas de urgência para casos mais graves.

---

## Grupo
- Giovanni A. Cerbaro ([text](https://github.com/gcerbaro))
- Felipe F. Picasso ([text](https://github.com/FelipeFPicasso))
- Nicolas C. Todero ([text](https://github.com/NicolasComin))

---
