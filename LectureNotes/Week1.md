# 6.036 Week1

## Chapter01 Introduction

In general, we need to solve these two problems in Machine Learning:

* estimation
* generalization

We can describe problems and their solutions using six characteristics, three of which
characterize the problem and three of which characterize the solution:

* Problem class
* Assumptions
* Evaluation criteria
* Model type
* Model class
* Algorithm

课上提到了一个很有意思的观点: 我们可以将机器学习视作在传统程序上做出更高程度的抽象

与传统程序的数据结构和算法相比，机器学习依然离不开编写的程序代码，区别是什么呢？区别是传统的heuristic方式编写的程序将数据结构作为输入将数据结构作为输出，而编写的机器学习框架的程序将数据作为输入，将最终的模型作为输出。输出的模型可以视作一个算法、一个黑盒，输出的模型可以处理输入的数据，产生 estimation/generalization，甚至也可以将数据作为输入，将模型、模式等作为输出(Learning algorithms)

这也是为什么 leslie kaelbling 在课上说机器学习存在某种 boundary:

> But after that, basically, all of the ways that we think about solving machine learning problems, coming up with machine learning algorithms, is going to be, actually, to use optimization methods, right?
> So what we're going to do is write down an objective function, like the training error, come up with a hypothesis class, and then use computational optimization methods to try to find the best element of the hypothesis class, according to our objective function. So that's really kind of the standard method.
> And that's where I feel like there's some kind of a boundary -- a machine learning person has to be partly a kind of a statistical analysis and generalization person and partly a computer scientist, right? And it's up until the point that you frame it as an optimization problem that you're really kind of worrying about the statistical and generalization aspects. And once you frame your question as an optimization problem, it becomes a problem in numerical algorithms. And so, and sort of, then, your role changes a little bit. And you become an optimization person.

## Chapter02 Linear classifiers
