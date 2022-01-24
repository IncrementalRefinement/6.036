# 6.036 Week1

## Chapter01 Introduction

In general, we need to solve these two problems in Machine Learning:

* estimation
* generalization

We can describe problems and their solutions using six characteristics, three of which characterize the problem and three of which characterize the solution:

* **Problem class**: What is the nature of the training data and what kinds of queries will
be made at testing time?
* **Assumptions**: What do we know about the source of the data or the form of the solution?
* **Evaluation** criteria: What is the goal of the prediction or estimation system? How will the answers to individual queries be evaluated? How will the overall performance of the system be measured?
* **Model type**: Will an intermediate model be made? What aspects of the data will be modeled? How will the model be used to make predictions?
* **Model class**: What particular parametric class of models will be used? What criterion will we use to pick a particular model from the model class?
* **Algorithm**: What computational process will be used to fit the model to the data and/or to make predictions?

课上提到了一个很有意思的观点: 我们可以将机器学习视作在传统程序上做出更高程度的抽象

与传统程序的数据结构和算法相比，机器学习依然离不开编写的程序代码，区别是什么呢？区别是传统的 heuristic 方式开发的程序将数据结构作为输入，将数据结构作为输出，而机器学习的程序将数据作为输入，将模型作为输出。输出的模型可以视作一个假设、一个算法、一个黑盒
这也是为什么 leslie kaelbling 在课上说机器学习存在某种 boundary:

> But after that, basically, all of the ways that we think about solving machine learning problems, coming up with machine learning algorithms, is going to be, actually, to use optimization methods, right?
> So what we're going to do is write down an objective function, like the training error, come up with a hypothesis class, and then use computational optimization methods to try to find the best element of the hypothesis class, according to our objective function. So that's really kind of the standard method.
> And that's where I feel like there's some kind of a boundary -- a machine learning person has to be partly a kind of a statistical analysis and generalization person and partly a computer scientist, right? And it's up until the point that you frame it as an optimization problem that you're really kind of worrying about the statistical and generalization aspects. And once you frame your question as an optimization problem, it becomes a problem in numerical algorithms. And so, and sort of, then, your role changes a little bit. And you become an optimization person.

## Chapter02 Linear classifiers

### 1. Classification

A mapper from input vector to a value within a discrete set.

You should always some additional process was almost surely required to go from the actual input examples to their feature representation.

real songs, face images --> their feature representation

### 2. Learning Algorithm

A learning algorithm is a procedure that takes a data set Dn as input and returns an element h of H; it looks like.

The difference between hypotheses and Learning Algorithm is shown in the graphs below. In short, learning algorithm produce hypotheses as the output.

input x --> _Hypothesis_ --> output y

DataSet --> _Learning Algorithm_ --> some Hypothesis h

### 3. Linear Classifier

The hypothesis class H of linear classifiers in d dimensions is the set of all vectors in Rd+1.

### 4. Learning linear classifiers

The handout so far uses a not-so-clever but not-so-dumb approach learning algorithm fot this problem. It randomly generates some parameter vectors and picks the one with the least error on the training set.

### 5. Evaluating a learning algorithm

It evaluates the algorithm that produces hypotheses.(Not the hypotheses!)

How should we evaluate the performance of a classifier h? The best method is to measure test error on data that was not used to train it

* Train on a new training set
* Evaluate resulting h on a testing set that does not overlap the training set
