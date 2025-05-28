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

# Modelagem
Para desenvolver e validar o modelo de machine learning, utilizamos a biblioteca scikit-learn, uma das mais populares em Python para machine learning. O processo começa com a importação das bibliotecas necessárias, como train_test_split, LinearRegression e métricas de avaliação como mean_squared_error e r2_score.

Primeiramente, separam-se as variáveis independentes (X), que incluem os investimentos em YouTube, Facebook e Newspaper, e a variável dependente (y), representada pelo valor de vendas. Em seguida, os dados são divididos em conjuntos de treinamento e teste para garantir que o modelo seja treinado e validado de forma eficaz.

O modelo de regressão linear é então criado e treinado usando os dados de treinamento. Após o treinamento, fazemos previsões com o conjunto de teste e verificamos o ajuste do modelo comparando os valores previstos com os valores reais.

A visualização dos resultados é feita através de um gráfico de dispersão, que ilustra a relação entre os valores reais e os valores previstos. Essa análise visual é fundamental para avaliar a precisão do modelo e identificar possíveis melhorias.

![image](https://github.com/user-attachments/assets/c57cc037-0ffd-4e59-ad47-c9521195fa3c)

A comparação visual entre as previsões do modelo e os dados reais indica uma boa aderência, a qual será posteriormente confirmada pelo coeficiente de determinação (R²) apresentado na próxima seção.

# Calculando predição

![image](https://github.com/user-attachments/assets/30b2e896-67f2-4491-81c8-4c1434e5d38a)

O alto valor do coeficiente de determinação (R²) indica uma forte correlação entre o modelo e os dados de teste. Isso sugere que o modelo é capaz de explicar uma grande parte da variabilidade observada nos dados e, portanto, suas previsões, dentro dos limites das variáveis independentes exploradas, demonstram boa aderência aos dados reais.

![image](https://github.com/user-attachments/assets/a9f11563-3524-4f48-b62d-dc939282587a)

Por se tratar de um modelo linear, os coeficientes refletem a influência direta de cada variável independente sobre o valor das vendas. Dessa forma, um coeficiente maior para uma determinada variável indica um maior impacto no retorno do investimento, resultando em um aumento proporcional nas vendas.

# Conclusão

Considerando a faixa de investimentos presente no conjunto de dados, o Facebook apresenta o maior potencial de retorno, seguido pelo Youtube, enquanto o Newspaper demonstra o menor impacto nas vendas.
