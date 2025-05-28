# Construção de um modelo de Regressão para previsão de vendas com base em investimentos em Marketing.

Este artigo explora o desenvolvimento e a aplicação de um modelo de machine learning criado para prever vendas com base em investimentos em marketing.

# Análise exploratória

O primeiro passo no desenvolvimento do modelo de previsão de vendas é a realização de uma análise exploratória dos dados (EDA, do inglês Exploratory Data Analysis). Esta etapa é crucial para entender a natureza e a qualidade dos dados disponíveis. Através da EDA, podemos identificar padrões, tendências e possíveis anomalias que precisam ser tratadas antes de prosseguir.

A análise exploratória inclui a inspeção de distribuições de variáveis, correlações entre variáveis e a identificação de outliers. Além disso, é nesta fase que reconhecemos a necessidade de limpeza dos dados e de técnicas de data wrangling.

Durante a análise exploratória dos dados, algumas observações importantes foram feitas:

a) Todos os valores presentes nas colunas estão no formato float64, o que é adequado para análises numéricas.

b) Não há valores negativos, já que o mínimo de cada coluna é maior do que 0. Isso é um indicativo positivo, pois garante a consistência e integridade dos dados.

c) Foi identificado pelo menos um valor na coluna Newspaper que se enquadra como outlier pelo critério de z-score. Através de uma investigação com o setor, esses dados podem ser excluídos pois não se trata de uma amostra representativa de reposta do investimento.

Após a remoção dos outliers, a ferramenta Seaborn é utilizada para a visualização dos dados. Seaborn é uma biblioteca para a criação de gráficos estatísticos em Python, que facilita o entendimento da distribuição dos dados e das possíveis correlações entre as variáveis

![image](https://github.com/user-attachments/assets/b295a13e-2441-42dc-9e38-08ae5281f488)
