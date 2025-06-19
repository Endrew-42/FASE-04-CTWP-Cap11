
# Classificação de Grãos com Machine Learning

Este repositório apresenta o desenvolvimento de um modelo de aprendizado de máquina para automatizar a classificação de grãos de trigo, com base no conjunto de dados "Seeds Dataset", disponibilizado pela UCI Machine Learning Repository.

## Objetivo

O objetivo principal desta atividade é aplicar a metodologia CRISP-DM para construir, avaliar e otimizar modelos de classificação capazes de distinguir entre três variedades de grãos de trigo: Kama, Rosa e Canadian. A automação deste processo busca reduzir erros humanos e aumentar a eficiência em cooperativas agrícolas de pequeno porte.

## Dataset

- Fonte: UCI Machine Learning Repository (https://archive.ics.uci.edu/dataset/236/seeds)
- Total de amostras: 210
- Classes: 3 tipos de grãos de trigo
- Atributos:
  - Area
  - Perimeter
  - Compactness
  - Length
  - Width
  - Asymmetry
  - Groove
  - Label (classe alvo)

## Metodologia CRISP-DM Aplicada

### 1. Entendimento do Negócio
A classificação manual de grãos pode ser imprecisa e demorada. A proposta é utilizar aprendizado de máquina para automatizar esse processo, reduzindo erros e aumentando a produtividade.

### 2. Entendimento dos Dados
Foi realizada uma análise exploratória com uso de histogramas, boxplots e gráficos de dispersão para compreender a distribuição dos dados e relações entre os atributos.

#### Exemplos de visualizações:

**Histograma dos Atributos**
![Histograma](imagens/01_histograma.png)

**Boxplot dos Atributos**
![Boxplot](imagens/02_boxplot.png)

**Pairplot - Relações entre atributos**
![Pairplot](imagens/03_pairplot.png)

### 3. Preparação dos Dados
- Carregamento e nomeação dos atributos
- Cálculo de estatísticas descritivas
- Padronização dos dados com StandardScaler
- Separação entre treino (70%) e teste (30%)

### 4. Modelagem
Foram aplicados três algoritmos de classificação:
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Random Forest

Cada modelo foi treinado com os dados de treino e testado no conjunto de teste. Foram utilizadas as seguintes métricas de avaliação:
- Acurácia
- Precisão
- Recall
- F1-Score
- Matriz de confusão

### 5. Avaliação
Todos os modelos apresentaram desempenho satisfatório, mas o modelo com melhor resultado geral foi o **Random Forest**, com acurácia superior a 97%. O KNN também apresentou desempenho relevante e foi submetido à otimização de hiperparâmetros com GridSearchCV.

### 6. Implementação
O código foi desenvolvido no Google Colab e organizado conforme solicitado, com todos os passos reproduzíveis e comentados. O repositório segue a estrutura definida pelo tutor da disciplina.

## Resultados

O modelo Random Forest obteve os melhores resultados em termos de acurácia e equilíbrio entre as métricas. O uso de atributos como Área, Perímetro, Comprimento e Sulco demonstrou alta capacidade discriminativa entre as classes.

## Conclusão

A utilização de aprendizado de máquina para classificação de grãos mostrou-se viável e eficiente. A aplicação prática pode contribuir significativamente para a automação de processos em ambientes agrícolas, aumentando a precisão na triagem e otimizando recursos humanos.

## Tecnologias Utilizadas

- Python
- Google Colab
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn

## Estrutura do Repositório

- `seeds_classificacao.ipynb`: Notebook principal com código e análises
- `imagens/`: Gráficos gerados durante a análise
- `README.md`: Documento explicativo do projeto
