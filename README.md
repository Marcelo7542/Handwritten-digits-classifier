English description Below

Eu explorei neste repositório o conjunto de dados MNIST com o objetivo de criar modelos para classificar dígitos escritos à mão. 
O projeto está estruturado em várias etapas, representadas por diferentes arquivos, cada um abordando aspectos específicos da classificação. 
Na última etapa, também exploro brevemente a classificação multilabel.

Estrutura do Projeto:

1. Arquivo: Seeing-Mnist
Comecei explorando o conjunto de dados MNIST, analisando as imagens e os rótulos para entender sua estrutura.
Decidi começar com algo mais simples: criar um classificador binário para identificar o dígito 2.

Inclui:

Visualização dos Dados: Exibição de imagens e seus rótulos.

Classificação Binária: Uso de SGDClassifier para prever o dígito 2.

Métricas de Avaliação: Matriz de confusão, precisão, recall, F1-score, curvas ROC e PR.


2. Arquivo: Seeing-Mnist-multiclasse
Extensão da classificação para múltiplas classes (de 0 a 9), testei diferentes modelos e escolhi o RandomForestClassifier por causa dos melhores resultados.

Modelos Testados:
SVC.

LogisticRegression.

SGDClassifier.

RandomForestClassifier (modelo final escolhido).

GaussianNB.

KNeighborsClassifier.

DummyClassifier (baseline).



3. Arquivo: Mnist-RFC
Foquei na otimização de hiperparâmetros do RandomForestClassifier e na análise dos resultados usando matrizes de confusão detalhadas.

Otimização de Hiperparâmetros:
Usei o GridSearchCV para ajustar parâmetros como número de estimadores, profundidade máxima, entre outros.

Visualização de Erros:
Utilizei matrizes de confusão para identificar erros e entender as confusões mais frequentes entre as classes.


4. Arquivo: Mnist-Multilabel
Neste arquivo, exploro a classificação multilabel, onde um dado pode pertencer a múltiplas classes simultaneamente.
Por exemplo, classifiquei os dígitos com base em propriedades como:

Par ou Ímpar;

Maior ou Menor que 5;

Criação de Rótulos Multilabel;

Criei rótulos derivados das características dos dígitos originais para formar um conjunto de dados multilabel.

Modelos Utilizados:

KNeighborsClassifier: Para previsões multilabel iniciais.

ClassifierChain com RandomForestClassifier: Para lidar com dependências entre rótulos.

Métricas de Avaliação.

Utilizei o F1-score com média macro para medir o desempenho do modelo.


5. Arquivo: Data-Augmentation


Neste arquivo, utilizei técnicas de aumento de dados (data augmentation) para aumentar a diversidade do conjunto de treinamento. 
A principal técnica utilizada foi o deslocamento das imagens em várias direções (direita, esquerda, cima e baixo).

O que foi feito:

Aumento de Dados: Criação de imagens deslocadas para aumentar a quantidade de exemplos no conjunto de treinamento.

Visualização de Erros: Análise das matrizes de confusão para visualizar como o aumento de dados afetou a performance do modelo.


Resultados
O modelo final foi avaliado utilizando várias métricas:

Precisão

Recall

F1-Score

Os modelos foram avaliados com base nas matrizes de confusão.





MNIST Dataset Exploration for Handwritten Digit Classification

In this repository, I explored the MNIST dataset with the goal of creating models to classify handwritten digits. The project is structured in several stages, represented by different files, each addressing specific aspects of classification. In the final stage, I also briefly explore multilabel classification.

Project Structure:

1. File: Seeing-Mnist
   
I started by exploring the MNIST dataset, analyzing the images and labels to understand its structure. I decided to begin with something simpler: creating a binary classifier to identify the digit 2.

Included:

Data Visualization: 

Displaying images and their labels.

Binary Classification: 

Using SGDClassifier to predict the digit 2.

Evaluation Metrics: 

Confusion matrix, accuracy, recall, F1-score, ROC and PR curves.

2. File:

   Seeing-Mnist-Multiclass
   
I extended the classification to multiple classes (from 0 to 9), testing different models and choosing RandomForestClassifier due to the best results.

Models Tested:

SVC

Logistic Regression

SGDClassifier

RandomForestClassifier (final chosen model)

GaussianNB

KNeighborsClassifier

DummyClassifier (baseline)

3. File: Mnist-RFC
   
I focused on hyperparameter optimization for the RandomForestClassifier and analyzed the results using detailed confusion matrices.

Hyperparameter Optimization:

I used GridSearchCV to tune parameters such as the number of estimators, maximum depth, and more.

Error Visualization:

I used confusion matrices to identify errors and understand the most frequent misclassifications between classes.

4. File: Mnist-Multilabel
   
In this file, I explored multilabel classification, where a sample can belong to multiple classes simultaneously. For example, I classified digits based on properties like:

Even or Odd

Greater than or Less than 5

Creating Multilabel Targets:

I created labels derived from the characteristics of the original digits to form a multilabel dataset.

Models Used:

KNeighborsClassifier: 

For initial multilabel predictions.

ClassifierChain with RandomForestClassifier: 

To handle dependencies between labels.

Evaluation Metrics:

I used F1-score with macro averaging to measure the model's performance.

5. File:

Data-Augmentation

In this file, I used data augmentation techniques to increase the diversity of the training set. The main technique used was shifting the images in multiple directions (right, left, up, and down).

What Was Done:

Data Augmentation: 

Created shifted images to increase the number of examples in the training set.

Error Visualization: 

Analyzed confusion matrices to visualize how data augmentation affected the model's performance.

Results

The final model was evaluated using various metrics:

Accuracy

Recall

F1-Score

The models were evaluated based on confusion matrices.
