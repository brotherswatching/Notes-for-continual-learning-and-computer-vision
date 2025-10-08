# Notes-for-continual-learning-and-computer-vision
这篇仓库是对我对于修过的分析持续学习课程与计算机视觉课程的简要回顾与总结，水平有限，谬误之处敬请指教。
## 分析持续学习
### 分析学习
1.what
* 通过**闭合形式的解**而非迭代优化的过程来得到网络参数，进行神经网络训练的方法
* 通过线性代数知识（最小二乘法，Moore-Penrose逆）将非线性的学习问题转换为线性，使训练能在一个epoch中完成。
* 这种方法带来的优势有：快训练速度，高解释性。因为避免了迭代，自然也就没有梯度消失与梯度爆炸的问题。在小样本数据库的领域内使用效果尤佳。

2.how
关键在于使用**伪逆**

推导部分coming soon

3.例子
CPNet: Correlation Projection Analytic Learning

ACnnL: Analytic convolutional neural network learning

4.递归分析学习
将一次进行的最小二乘法分成几块线性进行计算。这个性质不会改变权重，也被称为**权重的不变性**
示意图coming soon（p113）

5.分析学习面临的挑战
* 只有一个损失函数-最小均方差（mse）
* 比起梯度迭代的方法，缺少灵活性
* 欠拟合的风险

现在的解决思路：利用预训练模型——冻结**backbone**,只训练头部，实验证明也可以产生好的效果

## 计算机视觉
