# Logistic回归
**解决分类问题**

#### 假设函数:
要使$0 \le h_\theta(x) \le 1$，令：

$h_\theta(x)=\frac{1}{1+e^{-\Theta^\Tau x}}$，$h_\theta(x)$的意义为：对于输入$x$来说$y=1$的概率为多少。

即$h_\theta(x)=P(y=1|x;\theta)$

当$h_\theta(x) \ge 0.5$，令$y=1$

当$h_\theta(x) \lt 0.5$，令$y=0$

即:

当$\Theta^\tau x \ge 0$，令$y=1$

当$\Theta^\tau x \lt 0$，令$y=0$

#### 决策边界:
$\Theta^\tau x = 0$

**由$\theta$决定决策边界，而不是$x$，$x$只是用来拟合参数$\theta$**

#### 参数:
$\theta_0,\theta_1,\cdots,\theta_n = \Theta$

#### 代价函数:
$$
\text{Cost}(h_\theta(x),y)=\begin{cases}
    -\log(h_\theta(x)), & \text{if $y=1$} \\
    -\log(1-h_\theta(x)), & \text{if $y=0$}
\end{cases}
$$
简化后
$$
\text{Cost}(h_\theta(x),y)=-y\log(h_\theta(x))-(1-y)\log(1-h_\theta(x))
$$

$$
J(\theta)=\frac{1}{m}\sum_{i=1}^m\text{Cost}(h_\theta(x),y) \\
    =-\frac{1}{m}[\sum_{i=1}^my^{(i)}\log h_\theta(x^{(i)})+(1-y^{(i)})\log (1-h_\theta(x^{(i)}))]
$$

#### 梯度下降算法:

重复直到$J(\Theta)$达到局部最小值 {

$$
\theta_j := \theta_j - \alpha\frac{\partial}{\partial\theta_j}J(\theta_0,\cdots,\theta_n)\quad (j=0,\cdots,n)
\\
=\theta_j - \alpha(\frac{1}{m}\sum_{i=1}^m(h_\theta(x^{(i)})-y^{(i)})x^{(i)}_j)
$$

}


#### 多分类问题:
$$
\max_ih_\theta^{(i)}(x)
$$
为预测$y=i$的概率