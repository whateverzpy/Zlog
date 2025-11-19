+++
weight = -5
image = ''
categories = ['大学学习']
date = '2025-06-17T19:12:38+08:00'
title = '信号与系统期末复习知识点'
description = '信号与系统一些重要公式和知识点的归纳总结'
tags = ['信号与系统']
lastmod = '2025-06-22T22:39:00+08:00'
+++

## 绪论

### 冲激信号相关

$$
\delta(t)f(t)=\delta(t)f(0)
$$

$$
\int_{-\infty}^{\infty}\delta(t-t_0)f(t)\mathrm{d}t=f(t_0)
$$

### 线性时不变系统

#### 叠加性与均匀性

对于给定的系统，$e_1(t)$、$r_1(t)$ 和 $e_2(t)$、$r_2(t)$ 分别代表两对激励与响应，则当激励是 $C_1e_1(t)+C_2e_2(t)$ 时，响应为 $C_1r_1(t)+C_2r_2(t)$。

#### 时不变特性

对于给定的系统，若激励为 $e(t)$，产生响应为 $r(t)$，则当激励为 $e(t-t_0)$ 时，响应为 $r(t-t_0)$。

#### 微分特性

对于给定的系统，若激励为 $e(t)$，产生响应为 $r(t)$，则当激励为 $e'(t)$ 时，响应为 $r'(t)$。

## 连续时间系统的时域分析

### 微分方程的建立

| 电学量   | 关系               |
| -------- | ------------------ |
| 电阻 $R$ | $v=Ri$             |
| 电感 $L$ | $v=L\frac{di}{dt}$ |
| 电容 $C$ | $i=C\frac{dv}{dt}$ |

### 零输入响应与零状态响应

零输入响应 $r_{zi}(t)$ 符合起始状态 $r^{(k)}(0_-)$ 的约束，并且 $r^{(k)}(0_-)=r^{(k)}(0_+)$；零状态响应 $r_{zs}(t)$ 符合 $r^{(k)}(0_-)=0$ 的约束。
齐次解称为系统的自由响应，特解称为系统的强迫响应。

### 卷积

零状态响应

$$
r(t)=e(t)*h(t)=\int_0^t e(\tau)h(t-\tau)\mathrm{d}\tau
$$

#### 卷积的性质

$$
f(t)*\delta(t-t_0)=f(t-t_0)
$$

$$
f(t)*\delta'(t)=f'(t)
$$

$$
f(t)*u(t)=\int_{-\infty}^t f(\lambda)\mathrm{d}\lambda
$$

## 傅里叶变换

常用公式

$$
\cos{\omega t}=\frac{1}{2}(e^{j\omega t}+e^{-j\omega t})
$$

$$
\sin{\omega t}=\frac{1}{2j}(e^{j\omega t}-e^{-j\omega t})
$$

### 傅里叶级数

#### 三角函数形式

$$
f(t)=a_0+\sum_{n=1}^{\infty}[a_n\cos(n\omega_1 t)+b_n\sin(n\omega_1 t)]
$$

直流分量

$$
a_0=\frac{1}{T_1}\int_{t_0}^{t_0+T_1} f(t)\mathrm{d}t
$$

余弦分量的幅度

$$
a_n=\frac{2}{T_1}\int_{t_0}^{t_0+T_1} f(t)\cos(n\omega_1 t)\mathrm{d}t
$$

正弦分量的幅度

$$
b_n=\frac{2}{T_1}\int_{t_0}^{t_0+T_1} f(t)\sin(n\omega_1 t)\mathrm{d}t
$$

同频率项加以合并，写成另一种形式

$$
f(t)=c_0+\sum_{n=1}^{\infty}c_n\cos(n\omega_1 t+\varphi_n)
$$

其中

$$
\begin{cases}
c_0=a_0\\
c_n=\sqrt{a_n^2+b_n^2}\\
\cos{\varphi_n}=\frac{a_n}{c_n}\\
\sin{\varphi_n}=-\frac{b_n}{c_n}\\
\tan{\varphi_n}=-\frac{b_n}{a_n}
\end{cases}
$$

#### 指数形式

$$
f(t)=\sum_{n=-\infty}^{\infty}F(n\omega_1)e^{jn\omega_1 t}
$$

其中

$$
F(n\omega_1)=F_n=\frac{1}{T_1}\int_{t_0}^{t_0+T_1} f(t)e^{-jn\omega_1 t}\mathrm{d}t
$$

$F_n$ 与其他系数有如下关系

$$
\begin{cases}
F_0=c_0=a_0\\
F_n=|F_n|e^{j\varphi_n}=\frac{1}{2}(a_n-jb_n)\\
F_{-n}=|F_n|e^{-j\varphi_n}=\frac{1}{2}(a_n+jb_n)\\
|F_n|=|F_{-n}|=\frac{1}{2}c_n=\frac{1}{2}\sqrt{a_n^2+b_n^2}
\end{cases}
$$

### 傅里叶变换

#### 非周期信号

$$
F(\omega)=\mathcal{F}[f(t)]=\int_{-\infty}^{\infty}f(t)e^{-j\omega t}\mathrm{d}t
$$

$$
f(t)=\mathcal{F}^{-1}[F(\omega)]=\frac{1}{2\pi}\int_{-\infty}^{\infty}F(\omega)e^{j\omega t}\mathrm{d}\omega
$$

#### 周期信号

$$
F(\omega)=\mathcal{F}[f(t)]=2\pi\sum_{n=-\infty}^{\infty}F_n\delta(\omega-n\omega_1)
$$

#### 傅里叶变换的性质

| 性质 | $f(t)$ | $F(\omega)$ |
| ---- | ------ | ----------- |
| 对称性 | $F(t)$ | $2\pi F(-\omega)$ |
| 尺度变换 | $f(at)$ | $\frac{1}{\vert a\vert}F\left(\frac{\omega}{a}\right)$ |
| 时移 | $f(t-t_0)$ | $F(\omega)e^{-j\omega t_0}$ |
| 频移 | $f(t)e^{j\omega_0 t}$ | $F(\omega-\omega_0)$ |
| 时域微分 | $\frac{\mathrm{d}^n f(t)}{\mathrm{d}t^n}$ | $(j\omega)^n F(\omega)$ |
| 频域微分 | $(-jt)^n f(t)$ | $\frac{\mathrm{d}^n F(\omega)}{\mathrm{d}\omega^n}$ |
| 时域卷积 | $f_1(t)*f_2(t)$ | $F_1(\omega)F_2(\omega)$ |
| 频域卷积 | $f_1(t)f_2(t)$ | $\frac{1}{2\pi}F_1(\omega)*F_2(\omega)$ |

#### 常见信号的傅里叶变换

| 信号名称 | 时间函数 $f(t)$ | 频谱函数 $F(\omega)$ |
| -------- | ---------------- | ------------------- |
| 矩形脉冲 | $E\left[u(t+\frac{\tau}{2})-u(t-\frac{\tau}{2})\right]$ | $E\tau\mathrm{Sa}(\frac{\omega\tau}{2})$ |
| 抽样脉冲 | $\mathrm{Sa}(\omega_c t)=\frac{\sin{\omega_c t}}{\omega_c t}$ | $\frac{\pi}{\omega_c}[u(\omega+\omega_c)-u(\omega-\omega_c)]$ |
| 冲激函数 | $E\delta(t)$ | $E$ |
| 阶跃函数 | $Eu(t)$ | $\frac{E}{j\omega} + \pi E\delta(\omega)$ |
| 直流信号 | $E$ | $2\pi E\delta(\omega)$ |
| 余弦信号 | $E\cos{\omega_0 t}$ | $\pi E[\delta(\omega+\omega_0)+\delta(\omega-\omega_0)]$ |
| 正弦信号 | $E\sin{\omega_0 t}$ | $j\pi E[\delta(\omega+\omega_0)-\delta(\omega-\omega_0)]$ |

### 抽样定理

一个频谱受限的信号 $f(t)$，如果频谱只占据 $-\omega_m$ 到 $\omega_m$ 的范围，则信号 $f(t)$ 可以用等间隔的抽样值唯一地表示，最低抽样频率为 $f_s=2f_m$。

## 拉普拉斯变换

$$
F(s)=\mathcal{L}[f(t)]=\int_{0}^{\infty}f(t)e^{-st}\mathrm{d}t
$$

$$
f(t)=\mathcal{L}^{-1}[F(s)]=\frac{1}{2\pi j}\int_{\sigma-j\infty}^{\sigma+j\infty}F(s)e^{st}\mathrm{d}s
$$

### 拉普拉斯变换的性质

| 性质 | 内容 |
| ---- | ---- |
| 对 $t$ 微分 | $\mathcal{L}\left[\frac{\mathrm{d}^n f(t)}{\mathrm{d}t^n}\right]=s^nF(s)-\sum_{r=0}^{n-1}s^{n-r-1}f^{(r)}(0_-)$ |
| 时域平移 | $\mathcal{L}[f(t-t_0)u(t-t_0)]=e^{-st_0}F(s)$ |
| 频域平移 | $\mathcal{L}[f(t)e^{-at}]=F(s+a)$ |
| 尺度变换 | $\mathcal{L}[f(at)]=\frac{1}{a}F\left(\frac{s}{a}\right)$ |
| 初值 | $\lim_{t\to0}f(t)=\lim_{s\to\infty}sF(s)$ |
| 终值 | $\lim_{t\to\infty}f(t)=\lim_{s\to0}sF(s)$ |
| 对 $s$ 微分 | $\mathcal{L}[-tf(t)]=\frac{\mathrm{d}F(s)}{\mathrm{d}s}$ |
| 对 $s$ 积分 | $\mathcal{L}\left[\frac{f(t)}{t}\right]=\int_{s}^{\infty}F(s)\mathrm{d}s$ |

### 常用函数的拉普拉斯变换

| $f(t)$ | $F(s)$ |
| ------ | ------- |
| $\delta(t)$ | $1$ |
| $u(t)$ | $\frac{1}{s}$ |
| $t^n$ | $\frac{n!}{s^{n+1}}$ |
| $\sin{\omega t}$ | $\frac{\omega}{s^2+\omega^2}$ |
| $\cos{\omega t}$ | $\frac{s}{s^2+\omega^2}$ |

### 拉普拉斯逆变换

对于

$$
F(s)=\frac{K_{11}}{(s-p_1)^k}+\frac{K_{12}}{(s-p_1)^{k-1}}+\cdots+\frac{K_{1k}}{s-p_1}+\frac{E(s)}{D(s)}
$$

引入

$$
F_1(s)=(s-p_1)^kF(s)
$$

一般形式

$$
K_{1i}=\frac{1}{(i-1)!}\frac{\mathrm{d}^{i-1}F_1(s)}{\mathrm{d}s^{i-1}}\bigg|_{s=p_1}
$$

### 电路的 $s$ 域分析

| 电学量 | 关系 |
| ------ | ---- |
| 电阻 $R$ | $V_R(s)=RI(s)$ |
| 电感 $L$ | $V_L(s)=sLI_L(s)-Li_L(0)$ |
| 电容 $C$ | $V_C(s)=\frac{1}{sC}I_C(s)+\frac{1}{s}v_C(0)$ |

### 系统函数 $H(s)$

系统零状态响应的拉氏变换与激励的拉氏变换之比称为“系统函数”，以 $H(s)$ 表示。

$$
H(s)=\frac{R(s)}{E(s)}
$$

### 全通函数和最小相移函数

- 全通函数：一个系统函数的极点位于左半平面，零点位于右半平面，而且零点与极点对于 $j\omega$ 轴互为镜像；
- 最小相移函数：一个系统函数的零点仅位于左半平面或 $j\omega$ 轴上。

### 线性系统的稳定性

- 稳定系统：$H(s)$ 全部极点落于 $s$ 左半平面；
- 不稳定系统：$H(s)$ 存在极点落于 $s$ 右半平面或在虚轴上具有二阶以上的极点。
- 临界稳定系统：$H(s)$ 存在极点落于 $s$ 虚轴上且为一阶极点。

## 傅里叶变换的应用

### 系统的物理可实现性

就时间域特性而言，一个物理可实现网络的冲激响应 $h(t)$ 在 $t<0$ 时必须为零。
从频率特性来看，$|H(j\omega)|$ 需满足平方可积条件，即

$$
\int_{-\infty}^{\infty}|H(j\omega)|^2\mathrm{d}\omega<\infty
$$

佩利-维纳准则：对于幅度函数 $|H(j\omega)|$ 物理可实现的必要条件是

$$
\int_{-\infty}^{\infty}\frac{|\ln|H(j\omega)||}{1+\omega^2}\mathrm{d}\omega<\infty
$$

## 离散时间系统的时域分析

### 离散时间信号

1. 单位样值信号

    $$
    \delta(n)=\begin{cases}
    1, & n=0 \\
    0, & n\neq0
    \end{cases}
    $$

2. 单位阶跃序列

    $$
    u(n)=\begin{cases}
    1, & n\geq0 \\
    0, & n<0
    \end{cases}
    $$

3. 二者存在关系

    $$
    \delta(n)=u(n)-u(n-1)\\
    u(n)=\sum_{k=0}^{\infty}\delta(n-k)
    $$

### 单位样值响应相关

离散线性时不变系统作为因果系统的充分必要条件是

$$
h(n)=0\quad(当\ n<0)
$$

对于离散时间系统，稳定系统的充分必要条件是单位样值响应绝对可积，即

$$
\sum_{n=-\infty}^{\infty}|h(n)|\leq M
$$

其中 $M$ 为有界正值。

### 卷积

$$
y(n)=h(n)*x(n)=\sum_{m=-\infty}^{\infty}h(m)x(n-m)
$$

## $z$ 变换与离散时间系统的 $z$ 域分析

单边 $z$ 变换定义为

$$
X(z)=\mathcal{Z}[x(n)]=\sum_{n=0}^{\infty}x(n)z^{-n}
$$

双边 $z$ 变换定义为

$$
X(z)=\mathcal{Z}[x(n)]=\sum_{n=-\infty}^{\infty}x(n)z^{-n}
$$

### 典型序列的 $z$ 变换

| 序列 $x(n)$ | $z$ 变换 $X(z)$ |
| ------------ | ------------- |
| $\delta(n)$ | $1$ |
| $u(n)$ | $\frac{z}{z-1},\ \vert z\vert>1$ |
| $a^n u(n)$ | $\frac{z}{z-a},\ \vert z\vert> \vert a\vert$ |
| $\cos{\omega_0 n}$ | $\frac{z(z-\cos{\omega_0})}{z^2-2z\cos{\omega_0}+1},\ \vert z\vert>1$ |
| $\sin{\omega_0 n}$ | $\frac{z\sin{\omega_0}}{z^2-2z\cos{\omega_0}+1},\ \vert z\vert>1$ |

### 逆 $z$ 变换

如果 $X(z)$ 只含有一阶极点，则

$$
X(z)=\sum_{m=0}^{K}\frac{A_m z}{z-z_m}
$$

其中

$$
A_m=(z-z_m)\frac{X(z)}{z}\bigg|_{z=z_m}
$$

如果 $X(z)$ 中含有高阶极点，则

$$
X(z)=\sum_{m=0}^{M}\frac{A_m z}{z-z_m}+\sum_{j=1}^{s}\frac{B_j z}{(z-z_i)^j}
$$

或

$$
X(z)=\sum_{m=0}^{M}\frac{A_m z}{z-z_m}+\sum_{j=1}^{s}\frac{C_j z^j}{(z-z_i)^j}
$$

其中

$$
B_j=\frac{1}{(s-j)!}\frac{\mathrm{d}^{s-j}}{\mathrm{d}z^{s-j}}(z-z_i)^s\frac{X(z)}{z}\bigg|_{z=z_i}
$$

$C_j$ 可由待定系数法求出。

#### 逆 $z$ 变换表

| $z$ 变换 ($\vert z\vert>\vert a\vert$) | 序列 |
| --------- | ---- |
| $\frac{z}{z-a}$ | $a^n u(n)$ |
| $\frac{z^{m+1}}{(z-a)^{m+1}}$ | $\frac{(n+1)(n+2)\cdots(n+m)}{m!}a^n u(n)$ |

### $z$ 变换的主要性质

#### 位移性

双边 $z$ 变换

$$
\mathcal{Z}[x(n-m)]=z^{-m}X(z)
$$

单边 $z$ 变换序列左移

$$
\mathcal{Z}[x(n+m)u(n)]=z^m\left[X(z)-\sum_{k=0}^{m-1}x(k)z^{-k}\right]
$$

单边 $z$ 变换序列右移

$$
\mathcal{Z}[x(n-m)u(n)]=z^{-m}\left[X(z)+\sum_{k=-m}^{-1}x(k)z^{-k}\right]
$$

#### $z$ 域微分

$$
\mathcal{Z}[nx(n)]=-z\frac{\mathrm{d}X(z)}{\mathrm{d}z}
$$

#### $z$ 域尺度变换

$$
\mathcal{Z}[a^n x(n)]=X\left(\frac{z}{a}\right)
$$

#### 初值定理

$$
x(0)=\lim_{z\to\infty}X(z)
$$

#### 终值定理

$$
\lim_{n\to\infty}x(n)=\lim_{z\to1}[(z-1)X(z)]
$$

要求 $X(z)$ 的极点必须处在单位圆内（在单位圆上只能位于 $z=1$ 点且是一阶极点）。

### 离散系统的系统函数

#### $z$~$s$ 平面映射关系

$$
z=e^{sT}\\
z=re^{j\theta}\\
s=\sigma+j\omega\\
r=e^{\sigma T}\\
\theta=\omega T
$$

#### 稳定性和因果性

为使系统稳定应满足

$$
\sum_{n=-\infty}^{\infty}h(n)<\infty
$$

这表明，对于稳定系统 $H(z)$ 的收敛域应包含单位圆在内。\
对于因果系统 $h(n)$，它的 $z$ 变换收敛域包含 $\infty$ 点，通常表示为某圆外区 $a<|z|\leq\infty$。\
稳定因果系统应满足

$$
\begin{cases}
a<|z|\leq\infty \\
a<1
\end{cases}
$$
