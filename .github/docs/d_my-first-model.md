# Meu primeiro modelo com Scikit-Learn

O objetivo deste módulo é colocar a "mão na massa" e desenvolver um primeiro modelo de machine learning, com o objetivo de reforçar alguns conceitos, apresentados no módulo 5 (Fundamentos de Machine Learning), bem como fazer uma exploração inicial na biblioteca `scikit-learn` que nos acompanhará em boa parte da trilha.

O arquivo `modelo_diabetes.ipynb`, localizado na raiz do repositório, foi referência para o desenvolvimento do nosso primeiro modelo.

> [voltar](./notes.md) para página anterior.

## Sumário

- [Meu primeiro modelo com Scikit-Learn](#meu-primeiro-modelo-com-scikit-learn)
  - [Sumário](#sumário)
  - [O que é a Biblioteca `Scikit-learn`?](#o-que-é-a-biblioteca-scikit-learn)
  - [Descrição do Problema](#descrição-do-problema)
  - [Carga de Dados](#carga-de-dados)
  - [Transformação de *Features*](#transformação-de-features)
  - [Visualização de Dados](#visualização-de-dados)
  - [Separação de Dados entre Treino e Teste](#separação-de-dados-entre-treino-e-teste)
  - [Treinamento do Modelo](#treinamento-do-modelo)
  - [Validação do Modelo](#validação-do-modelo)
  - [Visualizar Métricas do Modelo](#visualizar-métricas-do-modelo)

## O que é a Biblioteca `Scikit-learn`?

Scikit-learn é uma das bibliotecas mais populares e amplamente usadas para aprendizado de máquina (machine learning) em Python. Ela é conhecida por sua facilidade de uso, eficiência e qualidade em termos de documentação e comunidade de apoio. Aqui estão alguns pontos-chave sobre o Scikit-learn:

1. **Ampla gama de algoritmos:** Scikit-learn oferece uma ampla variedade de algoritmos de aprendizado de máquina para tarefas de classificação, regressão, clusterização, redução de dimensionalidade, seleção de características e muito mais. Ele inclui algoritmos clássicos como regressão logística, árvores de decisão, máquinas de vetores de suporte (SVM), k-means e muitos outros.

2. **Fácil de usar:** Scikit-learn é projetado com ênfase na simplicidade e facilidade de uso. Sua API consistente e intuitiva facilita a construção, treinamento e avaliação de modelos de aprendizado de máquina.

3. **Documentação abrangente:** A biblioteca possui uma documentação extensa e bem escrita, que inclui tutoriais, exemplos e informações detalhadas sobre cada função e classe. Isso torna mais fácil para os desenvolvedores aprenderem a usar o Scikit-learn e tirarem o máximo proveito dela.

4. **Integração com outras bibliotecas:** Scikit-learn é frequentemente usado em conjunto com outras bibliotecas Python, como NumPy, pandas e Matplotlib, para pré-processamento de dados, manipulação de conjuntos de dados e visualização de resultados.

5. **Boa performance:** A biblioteca é otimizada para desempenho e é capaz de lidar com conjuntos de dados de tamanhos razoáveis. No entanto, para tarefas de grande escala ou conjuntos de dados muito grandes, outras bibliotecas de aprendizado de máquina como TensorFlow e PyTorch podem ser mais apropriadas.

6. **Comunidade ativa:** Scikit-learn tem uma comunidade de desenvolvedores ativos e é de código aberto, o que significa que é constantemente atualizado e aprimorado com novos recursos e correções de bugs.

7. **Ferramentas de avaliação:** Scikit-learn oferece uma variedade de métricas de avaliação e funções para ajudar na seleção do modelo, avaliação de desempenho e validação cruzada.

8. **Suporte a fluxos de trabalho de aprendizado de máquina:** A biblioteca oferece suporte para pipelines de pré-processamento de dados e modelagem, facilitando a construção de fluxos de trabalho completos de aprendizado de máquina.

Em resumo, o Scikit-learn é uma escolha sólida para quem deseja começar a explorar o aprendizado de máquina em Python devido à sua facilidade de uso, documentação abrangente e ampla gama de recursos. É particularmente adequado para tarefas de aprendizado de máquina tradicionais e de médio porte, e muitos profissionais de dados e cientistas de dados o consideram uma ferramenta essencial em seu conjunto de ferramentas de aprendizado de máquina.

## Descrição do Problema

Um laboratório de análises clínicas, com base de dados de pacientes que realizaram exames de diabetes, gostaria de prever, com base em características com idade, peso e altura, qual o resultado esperado do exame para novos pacientes.

Para isso, iremos treinar um algoritimo supervisionado (dado que temos dados reais dos resultados) para criar um modelo preditivo que atenda as necessidade do laboratório.

## Carga de Dados

O conjunto de dados contém informações sobre exames médicos de pacientes, como ID do paciente, gênero, idade, peso, altura e resultado do exame de diabetes. Utilizamos as bibliotecas pandas, matplotlib e Seaborn para carregar e visualizar os dados. Criamos um Jupyter Notebook chamado "modelo-diabetes.ipynb" e importamos as bibliotecas necessárias. Em seguida, carregamos o arquivo de dados em um dataframe e visualizamos sua estrutura usando o método "info()". O dataframe possui 100 entradas e colunas que representam as características dos pacientes e os resultados dos exames.

Fonte de dados: [`datasets/exames_diabetes.csv`](../../datasets/exames_diabetes.csv).

## Transformação de *Features*

Nesta parte, discutimos sobre a importância de converter variáveis categóricas em numéricas para utilizá-las em modelos de regressão. Explicamos que a abordagem de substituição direta de valores pode levar a pesos diferentes nas informações e apresentei o conceito de One-Hot Encoding. Mostramos como usar o método get_dummies do pandas para realizar essa conversão, criando variáveis binárias que representam as categorias. Também mencionamos a importância de remover colunas irrelevantes, como a coluna de identificação do paciente.

## Visualização de Dados

Nesta etapa, exploramos a biblioteca Seaborn para visualizar a correlação entre as variáveis de um dataset. Utilizamos o método heatmap para criar um mapa de calor com a matriz de correlação das variáveis. Também aprendemos a adicionar anotações aos valores da matriz para facilitar a visualização das correlações. Além disso, discutimos a importância de definir os limites mínimo e máximo da escala do mapa de calor. Também exploramos o uso do método scatter_matrix do Pandas para criar um gráfico de dispersão com correlação entre as variáveis. Por fim, mencionamos a possibilidade de personalizar a escala de cores dos gráficos.

## Separação de Dados entre Treino e Teste

Nesta etapa, vamos trabalhamos com regressão linear simples no contexto do modelo de diabetes. Primeiro, importamos as bibliotecas necessárias do scikit-learn, como a biblioteca de regressão linear e a função para dividir o conjunto de dados em treino e teste. Também importamos métricas para validar nosso modelo, como o erro absoluto mínimo e o R2-score. Em seguida, preparamos os dados para criar dois modelos: um sem o IMC e outro apenas com o IMC. Dividimos os dados em variáveis dependentes (target) e independentes (explicativas) e removemos as colunas desnecessárias. Em seguida, dividimos o conjunto de dados em treino e teste, usando 70% para treinamento e 30% para teste. Essa divisão é aleatória, mas podemos controlá-la usando o argumento random state. Por fim, criamos quatro conjuntos de dados: xtrain, xtest, ytrain e ytest.

## Treinamento do Modelo

Aqui, aprendemos sobre o treinamento de modelos de regressão linear usando o Scikit-Learn. O treinamento envolve fornecer ao modelo os dados de treinamento, que consistem nas variáveis independentes (X) e na variável dependente (Y). O modelo usa um algoritmo de regressão linear para encontrar um padrão entre as variáveis em X e a variável Y. Em seguida, geramos previsões usando o conjunto de testes e comparamos essas previsões com os dados reais. Também podemos obter os coeficientes da equação da reta gerada pelo modelo. No próximo vídeo, discutiremos métricas de avaliação do modelo.

## Validação do Modelo

Discutimos a avaliação de um modelo de regressão linear. Começamos explorando duas métricas importantes: o R2-score e o Mean Absolute Error (MAE). O R2-score mede o quão bem o modelo explica a variação dos dados, com valores mais próximos de 1 indicando um bom ajuste. Já o MAE calcula a diferença média entre os valores reais e os valores previstos pelo modelo. No exemplo apresentado, o primeiro modelo teve um baixo R2-score e um MAE considerável, indicando um ajuste insatisfatório. Agora, vamos comparar esses resultados com um segundo modelo.

## Visualizar Métricas do Modelo

Discutimos a comparação entre dois modelos de regressão linear. O primeiro modelo é uma regressão linear múltipla, onde todas as variáveis são consideradas, exceto o IMC. O segundo modelo é uma regressão linear simples, onde apenas o IMC é considerado. Analisamos as métricas de desempenho, como o R2-score e o erro quadrático mínimo, para avaliar a eficácia de cada modelo. Também mostramos visualmente as retas de regressão e os resíduos para entender melhor a capacidade de previsão de cada modelo. Concluímos que o segundo modelo, com apenas o IMC como variável, teve um desempenho ligeiramente melhor, mas ainda há espaço para melhorias.

> [voltar](#sumário) para o topo.
>
> [voltar](./notes.md) para página anterior.
