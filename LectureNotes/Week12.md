# 6.036 Week10

这一讲主要讲了推荐系统，和两种实现方法以及一些优化手段

## Content-based recommendations

提取推荐内容的特征，生成特征向量，然后这个问题就归化成了之前的问题

缺点:

1. 特征化内容比较困难
2. 每个用户的数据较少
3. 没有考虑到相似用户/用户间数据的关联性

## Collaborative filtering

一些优化方法:

* Alternating least squares
* Stochastic gradient descent
