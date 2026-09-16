# Naive Bayes — Estudo e Aplicações

O objetivo deste repositório é apresentar, de forma didática, o funcionamento
e a aplicação dos algoritmos de classificação baseados em **Naive Bayes**,
com foco nos modelos probabilísticos disponíveis no `scikit-learn`.

O projeto apresenta dois estudos utilizando diferentes variantes do Naive Bayes:
**GaussianNB**, **MultinomialNB** e **BernoulliNB**.

O Naive Bayes é uma família de algoritmos de classificação baseada no
**Teorema de Bayes**, que permite calcular a probabilidade de uma determinada
classe a partir das características observadas.

A formulação do Teorema de Bayes é:

$$
P(c|X) = \frac{P(X|c)P(c)}{P(X)}
$$

No contexto de aprendizado de máquina:

- **P(c|X)** → probabilidade de uma amostra pertencer à classe `c`, dado o vetor de características `X`;
- **P(X|c)** → probabilidade de observar as características `X`, considerando a classe `c`;
- **P(c)** → probabilidade a priori da classe `c`;
- **P(X)** → probabilidade de observar o conjunto de características `X`.

O termo **"Naive" (ingênuo)** está relacionado à suposição de que as
características utilizadas pelo modelo são condicionalmente independentes
entre si, dada a classe.

---

## GaussianNB

No primeiro notebook, é apresentado um problema de classificação envolvendo
alunos.

A base de dados contém informações como **horas de estudo, nota anterior e
número de faltas**. A partir dessas características, o modelo busca classificar
se um determinado aluno será **aprovado ou não**.

Nesse estudo, é explorada a aplicação do **GaussianNB**, que assume que as
características numéricas seguem uma distribuição aproximadamente gaussiana
dentro de cada classe.

Além do treinamento e da predição, são analisadas as médias, variâncias,
distribuições das características e métricas de avaliação do modelo.

---

## MultinomialNB × BernoulliNB

No segundo notebook, é realizada uma comparação entre os modelos
**MultinomialNB** e **BernoulliNB** em um problema de classificação de
mensagens.

Os dois modelos utilizam as mesmas mensagens e classes, porém as palavras são
representadas de maneiras diferentes:

- **MultinomialNB** → considera a frequência das palavras;
- **BernoulliNB** → considera apenas a presença ou ausência das palavras.

O objetivo é observar como diferentes formas de representação dos dados podem
influenciar o treinamento, as previsões e o desempenho dos modelos.

Ao final, os resultados são comparados por meio de métricas como
**Accuracy, Precision, Recall e F1-score**, além das matrizes de confusão.
