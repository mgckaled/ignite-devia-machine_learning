<!-- markdownlint-disable MD024 -->
<!-- markdownlint-disable MD033 -->

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
  - [Engenharia de *Features*](#engenharia-de-features)
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

> [voltar](#sumário) para o topo.

## Descrição do Problema

Um laboratório de análises clínicas, com base de dados de pacientes que realizaram exames de diabetes, gostaria de prever, com base em características com idade, peso e altura, qual o resultado esperado do exame para novos pacientes.

Para isso, iremos treinar um algoritimo supervisionado (dado que temos dados reais dos resultados) para criar um modelo preditivo que atenda as necessidade do laboratório.

> [voltar](#sumário) para o topo.

## Carga de Dados

Fonte de dados: [`datasets/exames_diabetes.csv`](../../datasets/exames_diabetes.csv).

> [voltar](#sumário) para o topo.

## Engenharia de *Features*

> [voltar](#sumário) para o topo.

## Visualização de Dados

> [voltar](#sumário) para o topo.

## Separação de Dados entre Treino e Teste

> [voltar](#sumário) para o topo.

## Treinamento do Modelo

> [voltar](#sumário) para o topo.

## Validação do Modelo

> [voltar](#sumário) para o topo.

## Visualizar Métricas do Modelo

> [voltar](#sumário) para o topo.
>
> [voltar](./notes.md) para página anterior.
