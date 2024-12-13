+++
weight = -3
image = ''
categories = ['大学学习']
date = '2024-12-12T17:40:44+08:00'
title = '概率论与数理统计的记忆知识点'
description = '临近期末考试整理的一些需要特别记忆的考点'
tags = ['概率论', '数理统计']
lastmod = '2024-12-13T16:22:44+08:00'
+++

## 关于

尽管是纯粹的数学学科，但还是有很多公式是需要特别记忆的，以及一些非常容易忽视的概念性的内容，整理的过程中也能发现一些规律，并不需要死记硬背。（顺便测试下博客的内嵌 PDF 功能）

## 概率的公理化定义

设随机试验 $E$ 的样本空间为 $S$，如果对每一个事件 $A$，都有一个实数 $P(A)$ 与之对应，且满足以下公理：

1. $P(A) \geq 0$；
2. $P(S) = 1$；
3. 对于互不相容的事件 $A_1,A_2,\dots,A_n$，有

   $$
   P(A_1+A_2+\dots+A_n+\dots)=P(A_1)+P(A_2)+\dots+P(A_n)+\dots
   $$

   则称实数 $P(A)$ 为事件 $A$ 的概率。

## 分布函数

设 $X$ 为一随机变量，称

$$
F(x)=P(X \leq x)
$$

为 $X$ 的分布函数。注意 $F(x)$ 是右连续的，如分段时区间应当写成左闭右开的形式。

### 性质

1. $0\leq F(x)\leq 1$；
2. $F(x)$ 是单调非减的；
3. $\lim_{x\to-\infty}F(x)=0,\lim_{x\to\infty}F(x)=1$；
4. $F(x^+)=F(x)$，即 $F(x)$ 是右连续的。

## 协方差与相关系数

$$
\text{Cov}(X,Y) = E(XY) - E(X)E(Y)
$$

$$
D(X + Y) = D(X) + 2 \text{Cov}(X,Y) + D(Y)
$$

$$
\rho = \frac{\text{Cov}(X,Y)}{\sqrt{D(X)} \sqrt{D(Y)}}
$$

## 切比雪夫不等式

$$
P(|X - E(X)| \geq \varepsilon) \leq \frac{D(X)}{\varepsilon^2}
$$

## 中心极限定理

### 独立同分布的中心极限定理（林德伯格-莱维中心极限定理）

设 $X_1,X_2,\dots,X_n$ 独立同分布，且具有有限的数学期望和方差 $E(X_i)=\mu,D(X_i)=\sigma^2$，则

$$
\lim_{n \to \infty} P\left(\frac{\sum_{i=1}^n X_i - n \mu}{\sqrt{n} \sigma} \leq x \right) = \Phi(x) = \int_{-\infty}^x \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}} dx
$$

### 棣莫弗-拉普拉斯定理

在 $n$ 重伯努利试验中，成功概率为 $p$，成功次数为 $Y_n$，则

$$
\lim_{n \to \infty} P\left( \frac{Y_n - np}{\sqrt{npq}} \leq x \right) = \Phi(x) = \int_{-\infty}^x \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}} dx
$$

## 数理统计中的三大分布

### \$\chi^2\$ 分布

设 $X_1,X_2,\dots,X_n$ 为 $n$ 个 $(n\geq1)$ 相互独立的随机变量，它们都服从标准正态分布 $N(0,1)$。

$$
Y=\sum_{i=1}^n X_i^2
$$

则随机变量 $Y$ 服从自由度为 $n$ 的 $\chi^2$ 分布，记作 $Y\sim\chi^2(n)$，且有

$$
E(Y)=n,D(Y)=2n
$$

### \$t\$ 分布

设随机变量 $X,Y$ 相互独立，且 $X\sim N(0,1),Y\sim\chi^2(n)$。

$$
T=\frac{X}{\sqrt{\frac{Y}{n}}}
$$

则随机变量 $T$ 服从自由度为 $n$ 的 $t$ 分布，记作 $T\sim t(n)$。

### \$F\$ 分布

设随机变量 $X,Y$ 相互独立，且 $X\sim\chi^2(n_1),Y\sim\chi^2(n_2)$。

$$
F=\frac{\frac{X}{n_1}}{\frac{Y}{n_2}}
$$

则随机变量 $F$ 服从第一自由度为 $n_1$，第二自由度为 $n_2$ 的 $F$ 分布，记作 $F\sim F(n_1,n_2)$。

## 统计量及抽样分布

设 $X_1, X_2, \dots, X_n$ 为总体 $X$ 的容量为 $n$ 的样本，$T(x_1,x_2, \dots, x_n)$ 是定义在样本空间上不依赖于位置参数的一个连续函数，则称随机变量 $T(X_1,X_2, \dots, X_n)$ 为一个统计量。

$$
\overline{X}= \frac{1}{n} \sum_{i=1}^n X_i
$$

$$
S^2 = \frac{1}{n-1} \sum_{i=1}^n (X_i - \overline{X})^2=\frac{1}{n-1}\left(\sum_{i=1}^n X_i^2 - n\overline{X}^2\right)
$$

设 $X_1, X_2, \dots, X_n$ 是来自总体 $N(\mu, \sigma^2)$ 的一个样本，则样本均值

$$
\overline{X} \sim N\left( \mu, \frac{\sigma^2}{n} \right)
$$

样本方差 $S^2$ 与样本均值 $\overline{X}$ 相互独立，且

$$
\frac{n-1}{\sigma^2} S^2 \sim \chi^2(n-1)
$$

$$
\frac{(\overline{X} - \mu)\sqrt{n}}{S} \sim t(n-1)
$$

## 评定估计量的标准

### 无偏性

$$
E[\hat{\theta}(X_1,X_2,\dots,X_n)] = \theta
$$

则称 $\hat{\theta}$ 为 $\theta$ 的无偏估计量。

### 有效性

$$
D(\hat{\theta}_1) \leq D(\hat{\theta}_2)
$$

则称 $\hat{\theta}_1$ 较 $\hat{\theta}_2$ 有效。

### 相合性

$\hat{\theta}$ 依概率收敛于 $\theta$，即对任意 $\varepsilon > 0$，有

$$
\lim_{n \to \infty} P\left( |\hat{\theta} - \theta| \geq \varepsilon \right) = 0
$$

则称 $\hat{\theta}$ 为 $\theta$ 的相合估计量。

## 区间估计

设 $x_1, x_2, \dots, x_n$ 是来自总体 $N(\mu, \sigma^2)$ 的一个样本，$\overline{x}, s^2$ 分别为样本均值和样本方差。

### \$\sigma^2\$ 已知

$\mu$ 的一个置信区间为

$$
\left( \overline{x} - u_{\frac{\alpha}{2}} \frac{\sigma}{\sqrt{n}}, \overline{x} + u_{\frac{\alpha}{2}} \frac{\sigma}{\sqrt{n}} \right)
$$

### \$\sigma^2\$ 未知

$\mu$ 的一个置信区间为

$$
\left( \overline{x} - t_{\frac{\alpha}{2}}(n-1) \frac{s}{\sqrt{n}}, \overline{x} + t_{\frac{\alpha}{2}}(n-1) \frac{s}{\sqrt{n}} \right)
$$

### \$\sigma^2\$ 的置信区间

$$
\left( \frac{(n-1)s^2}{\chi^2_{\frac{\alpha}{2}}(n-1)}, \frac{(n-1)s^2}{\chi^2_{1-\frac{\alpha}{2}}(n-1)} \right)
$$

## 常用分布

| **分布**                         | **分布列或概率密度**                                                                                              | **数学期望**        | **方差**              |
| -------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ------------------- | --------------------- |
| $0-1$分布 <br> $B(1, p)$         | $P(X = k) = p^k q^{1-k}$<br>$k = 0, 1$, $0 < p < 1$, $p + q = 1$                                                  | $p$                 | $pq$                  |
| 二项分布 <br> $B(n, p)$          | $P(X = k) = C_n^k p^k q^{n-k}$<br>$k = 0, 1, \dots, n$, $0 < p < 1$, $p + q = 1$                                  | $np$                | $npq$                 |
| 泊松分布 <br> $P(\lambda)$       | $P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$<br>$k = 0, 1, 2, \dots$, $\lambda > 0$                             | $\lambda$           | $\lambda$             |
| 几何分布 <br> $G(p)$             | $P(X = k) = q^{k-1} p$, $k = 1, 2, \dots$<br>$0 < p < 1$, $p + q = 1$                                             | $\frac{1}{p}$       | $\frac{q}{p^2}$       |
| 均匀分布 <br> $U[a, b]$          | $f(x) = \begin{cases} \frac{1}{b-a}, & a \leq x \leq b \\ 0, & \text{其他} \end{cases}$                           | $\frac{a+b}{2}$     | $\frac{(b-a)^2}{12}$  |
| 指数分布 <br> $E(\lambda)$       | $f(x) = \begin{cases} \lambda e^{-\lambda x}, & x > 0 \\ 0, & x \leq 0 \end{cases}$                               | $\frac{1}{\lambda}$ | $\frac{1}{\lambda^2}$ |
| 正态分布 <br> $N(\mu, \sigma^2)$ | $f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}$<br>$-\infty < \mu < +\infty$, $\sigma > 0$ | $\mu$               | $\sigma^2$            |

对于泊松分布，若 $X\sim P(\lambda_1),Y\sim P(\lambda_2)$，则 $X+Y\sim P(\lambda_1+\lambda_2)$。
对于正态分布，若 $X\sim N(0,\sigma^2)$，则 $E(|X|)=\sigma\sqrt{\frac{2}{\pi}},E(X^2)=\sigma^2$。

## \$\Gamma\$ 函数

$$
\Gamma(z) = \int_0^\infty t^{z-1} e^{-t} dt
$$

若 $n$ 为正整数，则

$$
\Gamma(n) = (n-1)!
$$

递推公式

$$
\Gamma(x+1) = x\Gamma(x)
$$

特殊值

$$
\Gamma\left(\frac{1}{2}\right) = \sqrt{\pi}
$$

## PDF 版本

可能不是最新。。。。

{{< pdf "概率论速记.pdf" >}}
