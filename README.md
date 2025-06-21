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

- Identificação dos **Top 10 tipos de câncer** com maior número de pacientes e suas respectivas médias de sobrevivência e custos de tratamento.
- Visualização clara da distribuição da idade dos pacientes e do custo médio de tratamento.
- Análise do impacto do **risco genético** e do **uso de álcool** em diferentes tipos de câncer.
- Observação da diferença na média de sobrevivência entre gêneros.
- Mapas de correlação que revelam relações entre variáveis numéricas e as categorias codificadas com *one-hot encoding*.
- Gráficos com valores numéricos indicados para melhor entendimento dos dados.
- Apresentação visual do perfil dos pacientes por país, estágio do câncer e sexo.

---

## 6. Próximos Passos

- Implementação de modelos preditivos para estimar tempo de sobrevivência ou custo com base em variáveis clínicas e demográficas.
- Exploração de técnicas avançadas de análise multivariada e machine learning.
- Integração de dados adicionais para enriquecer o dataset e análises (ex.: dados genômicos, hábitos de vida).
- Desenvolvimento de um dashboard interativo para facilitar a exploração dos dados por usuários finais.

---