# 6.036 Week8

这一节主要讲解了卷积神经网络里的一些基本概念

## 神经网络的设计与问题的领域

这一章开头提到了一点我觉得很关键: 如果我们知道要解决的领域问题的特性，那么我们就可以根据这些特性来设计神经网络的结构

卷积神经网络是一种更加具体的神经网络，通常被用于信号处理(图片、图片序列、声音等等)。信号处理问题具有以下的特性:

1. Spatial locality
2. Translation invariance

## 卷积神经网络的概念

卷积神经网络有许多相关概念，都在 handout 里面进行了非常明晰的陈述，可以直接看

看完这一部分之后我总算明白和理清了很多概念，尤其是什么是卷积这一问题。我接触到卷积其实比接触到卷积神经网络要早，信号的卷积局势信号在时域和频域上变换的过程，但是我就搞不懂了，卷积神经网络这卷积和频域的变换到底他妈有个什么关系？

> If you are already familiar with what a convolution is, you might notice that this definition corresponds to what is often called a correlation and not to a convolution. Indeed, correlation and convolution refer to different operations in signal processing. However, in the neural networks literature, most libraries implement the correlation (as described in this chapter) but call it convolution. The distinction is not significant; in principle, if convolution is required to solve the problem, the network could learn the necessary weights. For a discussion of the difference between convolution and the conventions used in the literature you can read section 9.1 in this excellent book: https://www.deeplearningbook.org

回答是没有任何几把关系，卷积神经网络的卷积应该对应信号与系统中的互相关，over

## 卷积神经网络的训练方法

我们依然可以通过反向传播来得出梯度，计算卷积神经网络中的各参数(包括卷积核各个位置的参数)，具体公式参见 handout
