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
SVC
LogisticRegression
SGDClassifier
RandomForestClassifier (modelo final escolhido)
GaussianNB
KNeighborsClassifier
DummyClassifier (baseline)



3. Arquivo: Mnist-RFC
Foquei na otimização de hiperparâmetros do RandomForestClassifier e na análise dos resultados usando matrizes de confusão detalhadas.

Otimização de Hiperparâmetros
Usei o GridSearchCV para ajustar parâmetros como número de estimadores, profundidade máxima, entre outros.

Visualização de Erros
Utilizei matrizes de confusão para identificar erros e entender as confusões mais frequentes entre as classes.


4. Arquivo: Mnist-Multilabel
Neste arquivo, exploro a classificação multilabel, onde um dado pode pertencer a múltiplas classes simultaneamente.
Por exemplo, classifiquei os dígitos com base em propriedades como:

Par ou Ímpar
Maior ou Menor que 5
Criação de Rótulos Multilabel
Criei rótulos derivados das características dos dígitos originais para formar um conjunto de dados multilabel.

Modelos Utilizados
KNeighborsClassifier: Para previsões multilabel iniciais.
ClassifierChain com RandomForestClassifier: Para lidar com dependências entre rótulos.
Métricas de Avaliação
Utilizei o F1-score com média macro para medir o desempenho do modelo.
