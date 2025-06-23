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
  - ![Image](https://github.com/user-attachments/assets/3f3a1166-dc6f-4a7a-b23d-b198a1cf4f40)
2. Top 10 Tipos de Câncer por Custo Médio de Tratamento
Análise do custo médio dos tratamentos por tipo de câncer.
  - ![Image](https://github.com/user-attachments/assets/06cd2b10-b256-4ac8-b1d6-0d97ab58c8d4)
3. Top 10 Tipos de Câncer por Risco Genético Médio
Mostra quais tipos de câncer possuem maior risco genético associado.
  - ![Image](https://github.com/user-attachments/assets/032ab4d7-74f7-4edf-b942-90a3a2ffe915)
4. Top 10 Tipos de Câncer por Uso Médio de Álcool
Exibe os tipos de câncer mais associados ao consumo de álcool.
  - ![Image](https://github.com/user-attachments/assets/1c87d634-f803-4960-81da-8ab61509548f)
5. Média de Sobrevivência por Gênero
Compara o tempo médio de vida após diagnóstico entre gêneros.
  - ![Image](https://github.com/user-attachments/assets/b9c0cb76-e2c3-4552-a17a-33aced82ccd8)
6. Top 10 Países por Custo Médio de Tratamento
Ranking dos países com tratamentos mais caros, em média.
  - ![Image](https://github.com/user-attachments/assets/de7cbb00-fc06-497b-8ebd-f3dada6c0b57)
7. Média da Idade por Estágio do Câncer
Associação entre idade média dos pacientes e estágio da doença.
  - ![Image](https://github.com/user-attachments/assets/acd54ea4-c489-465c-a628-5d5fd5aa237e)
8. Distribuição da Idade dos Pacientes
Histograma mostrando a faixa etária predominante entre os pacientes.
  - ![Image](https://github.com/user-attachments/assets/4add57c9-4823-4788-8a0d-0c657dafeeec)
9. Distribuição do Custo de Tratamento
Análise da frequência dos diferentes custos de tratamento.
  - ![Image](https://github.com/user-attachments/assets/c3428535-857b-48f2-a09e-e881cdbd63a1)
10. Sobrevivência x Custo do Tratamento
Gráfico de dispersão que analisa a relação entre custo e tempo de vida.
  - ![Image](https://github.com/user-attachments/assets/8a452c8c-8eb3-4515-b53c-16c267297407)
11. Distribuição por Gênero
Gráfico de pizza com a proporção de pacientes por gênero.
  - ![Image](https://github.com/user-attachments/assets/461b478d-2721-4b07-b847-4d627170c38a)
12. Correlação com Target_Severity_Score
Barplot com as variáveis mais correlacionadas com a gravidade dos casos.
  -
13. Média de Sobrevivência por Gênero (One Hot Encoding)
Exibe os resultados médios de sobrevivência a partir das variáveis codificadas.
  - 
14. Dispersão: Fatores de Risco x Target_Severity_Score
Regplots comparando fatores de risco como tabagismo, álcool, risco genético, etc. com a gravidade.
  - 
15. Pairplot de Variáveis Correlacionadas com a Severidade
Visualização multivariada para explorar correlações simultâneas.
  -  
16. Boxplot: Severidade por Faixas de Tabagismo e Risco Genético
Comparação da gravidade dos casos com faixas de tabagismo e risco genético.
  - 
17. Heatmap: Severidade Média por Tipo de Câncer e Gênero
Mostra como a gravidade varia entre homens e mulheres por tipo de câncer.
  - 
---

## 6. Próximos Passos

- Implementação de modelos preditivos para estimar tempo de sobrevivência ou custo com base em variáveis clínicas e demográficas.
- Exploração de técnicas avançadas de análise multivariada e machine learning.
- Integração de dados adicionais para enriquecer o dataset e análises (ex.: dados genômicos, hábitos de vida).
- Desenvolvimento de um dashboard interativo para facilitar a exploração dos dados por usuários finais.

---