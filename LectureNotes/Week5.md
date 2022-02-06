# 6.036 Week5

这一节主讲的是 Regression 问题，在这个框架下，hypothesis 输出的 y 不再是离散的值，而是连续的实数。

这一节的核心其实是讲述了在求解模型参数过程中，analytical approach 和 iterative optimization approach 各自的特点和两者之间的联系

## 分析方法求解模型参数

可以通过联立方程求解的方式直接求出达到 optimum 时的模型参数，但这存在一定问题；

1. 过拟合
2. 无法求解，比如矩阵不可逆，等等
3. 计算量大(矩阵求逆、矩阵乘法)

## regularization 的作用

1. 缓解过拟合问题
2. 也可以使原本无解的分析算式可以求解(比如 ridge regularization 之后矩阵的对角线上的值会变 heavy，通过不断加大 regular 的幅度，可以使得矩阵正定，从而可逆)

## 迭代优化求解模型参数

减少运算量，当然前提是迭代过程可以达到极值点(convex)

## structural error & estimation error

structural error: This is error that arises because there is no hypothesis h ∈ H that will perform well on the data

estimation error: This is error that arises because we do not have enough data (or the data are in some way unhelpful) to allow us to choose a good h

When we increase λ, we tend to increase structural error but decrease estimation error, and vice versa.

So this is like the essential tension of machine learning. If you pick a really rich hypothesis class, one that can represent all kinds of answers, then you will not have too much structural error because you can represent the complexity of the problem that you need, but you risk not having enough data to nail it down in a good way. On the other hand, fitting a line to that data, you can do that pretty nicely, pretty reliably, without too much data. But it might not be able to give you, even express an answer of the kind that you want.

在构建一个准确的模型的过程中，模型的复杂性和数据的充足性之间存在着矛盾，可以通过 regular parameter 的放缩在两者之间进行权衡
