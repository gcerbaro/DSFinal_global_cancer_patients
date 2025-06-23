# Análise de Dados de Pacientes com Câncer (2015-2024)

## Descrição do Projeto

Este projeto realiza uma análise exploratória de um dataset contendo informações sobre pacientes com câncer coletadas entre 2015 e 2024. O objetivo é entender o perfil demográfico, clínico e os fatores de risco associados, além de avaliar custos de tratamento e taxas de sobrevivência.

O projeto inclui:

- Limpeza e preparação dos dados;
- Visualizações gráficas para análise dos principais aspectos do dataset;
- Modelos de Machine Learning para predição do tipo de câncer;
- Discussão dos resultados e conclusões.

## Dataset

O dataset utilizado contém 50.000 registros de pacientes, com informações como idade, gênero, país, tipo e estágio do câncer, fatores de risco (tabagismo, uso de álcool, obesidade, poluição do ar), custo do tratamento e anos de sobrevivência.

## Tecnologias Utilizadas

- Python
- Pandas
- Matplotlib / Seaborn
- Scikit-learn
- Google Colab (ambiente para execução)

## Como Executar

1. git clone: https://github.com/gcerbaro/DSFinal_global_cancer_patients.git


---

## 3. Dataset Utilizado

- **Origem:**  
  O dataset foi obtido do repositório GitHub acima, contendo registros globais de pacientes com câncer de 2015 a 2024.

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

## 4. Modelos Utilizados / Desenvolvidos

Este projeto focou na análise exploratória e visualização de dados, sem uso de modelos preditivos. As principais técnicas e ferramentas utilizadas foram:

- **Filtros estatísticos:** para limpeza de dados (remoção de outliers).
- **Agrupamentos e cálculos estatísticos:** para média, contagem e correlações.
- **Visualização gráfica:** gráficos de barras, histogramas, scatter plots, mapas de calor (heatmaps) para correlação.
- **One Hot Encoding:** para tratar variáveis categóricas e permitir análises de correlação e média por categorias.

---

## 5. Resultados Obtidos

1. Top 10 Tipos de Câncer por Média de Sobrevivência
Gráfico de barras mostrando os tipos de câncer com maior tempo médio de sobrevivência.

  - ![Image](https://github.com/user-attachments/assets/df33ff37-7c2e-4866-9ef0-5013ff13fab2)

2. Top 10 Tipos de Câncer por Custo Médio de Tratamento
Análise do custo médio dos tratamentos por tipo de câncer.

  - ![Image](https://github.com/user-attachments/assets/6e86fbc9-3c4b-4e4f-964e-510838336885)


3. Top 10 Tipos de Câncer por Risco Genético Médio
Mostra quais tipos de câncer possuem maior risco genético associado.

  - ![Image](https://github.com/user-attachments/assets/d661ed92-960e-4d6f-b26e-2006832d69a6)


4. Top 10 Tipos de Câncer por Uso Médio de Álcool
Exibe os tipos de câncer mais associados ao consumo de álcool.

  - ![Image](https://github.com/user-attachments/assets/d744e412-f44a-4d20-97f5-416445ac313c)


5. Média de Sobrevivência por Gênero
Compara o tempo médio de vida após diagnóstico entre gêneros.

  - ![Image](https://github.com/user-attachments/assets/577014ca-9cb6-4edf-bdc4-c37564714611)


6. Top 10 Países por Custo Médio de Tratamento
Ranking dos países com tratamentos mais caros, em média.

  - ![Image](https://github.com/user-attachments/assets/326e9f11-c2b2-4b4c-bbd5-f65d41ee57a3)


7. Média da Idade por Estágio do Câncer
Associação entre idade média dos pacientes e estágio da doença.

  - ![Image](https://github.com/user-attachments/assets/ed8d364c-00f8-4f02-b32b-86110ad9608f)


8. Distribuição da Idade dos Pacientes
Histograma mostrando a faixa etária predominante entre os pacientes.

  - ![Image](https://github.com/user-attachments/assets/0ed8d763-86d5-4794-8054-b6e551a65651)


9. Distribuição do Custo de Tratamento
Análise da frequência dos diferentes custos de tratamento.

  - ![Image](https://github.com/user-attachments/assets/e0a48e7f-2d4c-4c7e-a4db-d9b35829190b)


10. Sobrevivência x Custo do Tratamento
Gráfico de dispersão que analisa a relação entre custo e tempo de vida.

  - ![Image](https://github.com/user-attachments/assets/4050b3c4-ea9b-4b47-9174-c9bc2586af40)


11. Distribuição por Gênero
Gráfico de pizza com a proporção de pacientes por gênero.

  - ![Image](https://github.com/user-attachments/assets/c60e2b24-5480-4acd-a10b-a39bc14298ae)


12. Correlação com Target_Severity_Score
Barplot com as variáveis mais correlacionadas com a gravidade dos casos.

  - ![Image](https://github.com/user-attachments/assets/a2b1acaf-0575-40b4-9a33-a2812b8ae0a5)


13. Média de Sobrevivência por Gênero (One Hot Encoding)
Exibe os resultados médios de sobrevivência a partir das variáveis codificadas.

  - ![Image](https://github.com/user-attachments/assets/3f58c162-7c84-40f7-9dfe-1cc47a87ace3)


14. Dispersão: Fatores de Risco x Target_Severity_Score
Regplots comparando fatores de risco como tabagismo, álcool, risco genético, etc. com a gravidade.

  - ![Image](https://github.com/user-attachments/assets/07562eb5-b2af-4ff2-91f8-a6e2e4b8c332)


15. Pairplot de Variáveis Correlacionadas com a Severidade
Visualização multivariada para explorar correlações simultâneas.

  - ![Image](https://github.com/user-attachments/assets/744ea238-4225-45a6-a606-bf37ffbe4c85)


16. Boxplot: Severidade por Faixas de Tabagismo e Risco Genético
Comparação da gravidade dos casos com faixas de tabagismo e risco genético.

  - ![Image](https://github.com/user-attachments/assets/39188ee5-0982-45d9-8364-55198021d62f)


17. Heatmap: Severidade Média por Tipo de Câncer e Gênero
Mostra como a gravidade varia entre homens e mulheres por tipo de câncer.

  - ![Image](https://github.com/user-attachments/assets/2c6ac3a5-2232-4389-bf27-62f2d0d6568b)


18. Boxplot: Severidade por Faixas de Obesidade
Visualiza a relação entre níveis de obesidade e severidade dos casos.

  - ![Image](https://github.com/user-attachments/assets/36ece335-2f8c-41a6-9404-6d4059b0704c)


19. Boxplot: Severidade por Faixas de Poluição do Ar
Mostra o impacto da poluição atmosférica na gravidade dos casos.

  - ![Image](https://github.com/user-attachments/assets/4d929a8f-6929-471c-8710-4ecd1cd51fd2)


20. Scatterplot: Sobrevivência vs Risco Genético
Analisa a relação entre o risco genético e os anos de sobrevivência.

  - ![Image](https://github.com/user-attachments/assets/0fde60e5-b3e7-494f-b86e-49487cd4c92b)


21. Histograma: Distribuição de Tabagismo
Frequência dos níveis de tabagismo entre os pacientes.

  - ![Image](https://github.com/user-attachments/assets/ea982f7e-52c0-4ec8-9b01-f41ce099ea18)


22. Histograma: Distribuição do Nível de Obesidade
Faixa de níveis de obesidade observados.

  - ![Image](https://github.com/user-attachments/assets/93f0bd4d-46a7-4a48-a8bc-c0cc5a28b0af)


23. Gráfico de Barras: Frequência de Estágios do Câncer
Mostra a quantidade de pacientes em cada estágio da doença.

  - ![Image](https://github.com/user-attachments/assets/e81c9131-1d4b-45db-bb39-bb4e1c1567eb)


24. Mapa Geográfico: Distribuição dos Pacientes por País
Visualização espacial da concentração de pacientes por região.

  - ![Image](https://github.com/user-attachments/assets/c764b497-0328-4cdf-960b-76970835f859)



---

## 6. Próximos Passos

- Implementação de modelos preditivos para estimar tempo de sobrevivência ou custo com base em variáveis clínicas e demográficas.
- Exploração de técnicas avançadas de análise multivariada e machine learning.
- Integração de dados adicionais para enriquecer o dataset e análises (ex.: dados genômicos, hábitos de vida).
- Desenvolvimento de um dashboard interativo para facilitar a exploração dos dados por usuários finais.

---