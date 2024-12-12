+++
weight = -2
image = ''
categories = ['大学学习']
date = '2024-12-10T21:28:16+08:00'
title = '最优化方法作业'
description = '记录一次最优化方法作业的解答'
tags = ['最优化', '作业']
lastmod = '2024-12-12T03:08:00+08:00'
+++

## 题目 1

$$
\begin{cases}
\min &f(\mathbf{x})=(x_1-\frac{9}{4})^2+(x_2-2)^2 \\
s.t.&x_2-x_1^2\ge0, \\
&x_1+x_2\le6, \\
&x_1,x_2\ge0
\end{cases}
$$

验证 $\mathbf{x}^*=(1.5,2.25)^T$ 是 K-T 点。

### 解答

$$
\begin{cases}
g_1(\mathbf{x})=x_1^2-x_2 \\
g_2(\mathbf{x})=x_1+x_2-6 \\
g_3(\mathbf{x})=-x_1 \\
g_4(\mathbf{x})=-x_2
\end{cases}
$$

显然仅有 $g_1(\mathbf{x}^*)=0$，$I=\{1\}$，计算梯度

$$
\begin{aligned}
&\nabla f(\mathbf{x})=\begin{bmatrix}2x_1-\frac{9}{2} \\ 2x_2-4\end{bmatrix}^T \\
&\nabla g_1(\mathbf{x})=\begin{bmatrix}2x_1 \\ -1\end{bmatrix}^T
\end{aligned}
$$

将 $\mathbf{x}^*$ 代入得

$$
\begin{cases}
-\frac{3}{2}+3u_1=0 \\
\frac{1}{2}-u_1=0
\end{cases}
$$

解得 $u_1=\frac{1}{2}\ge0$，故 $\mathbf{x}^*=(1.5,2.25)^T$ 是 K-T 点。

## 题目 2

通过 K-T 条件求解下列问题

$$
\begin{cases}
\min &f(\mathbf{x})=-3x_1+x_2-x_3^2 \\
s.t.&x_1+x_2+x_3\le0, \\
&-x_1+2x_2+x_3^2=0
\end{cases}
$$

### 解答

计算梯度

$$
\nabla f(\mathbf{x})=\begin{bmatrix}-3 \\ 1 \\ -2x_3\end{bmatrix}^T
$$

海塞矩阵

$$
\nabla^2f(\mathbf{x})=\begin{bmatrix}0 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & -2\end{bmatrix}
$$

不是正定矩阵或半正定矩阵，因此该问题不是凸优化，可以观察到，若令

$$
x_1=0,x_2=- \frac{1}{2}x_3^2
$$

显然有 $f(\mathbf{x})$ 无界，不存在最优解。
