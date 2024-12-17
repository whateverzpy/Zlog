+++
weight = -4
image = ''
categories = ['大学学习']
date = '2024-12-17T14:28:43+08:00'
title = '大学物理 B 期末复习知识点'
description = '大学物理 B 的一些重要公式归纳总结（持续更新中）'
tags = ['大学物理']
lastmod = '2024-12-17T15:41:43+08:00'
+++

## 热学

### 理想气体物态方程

$$
pV=NkT \\
pV=\nu RT
$$

其中 $N$ 为气体分子数，$\nu$ 为气体物质的量。

### 理想气体压强公式

#### 分子平均平动动能

$$
\overline{\varepsilon}_{\mathrm{k}}=\frac{1}{2}m\overline{v^2}=\frac{3}{2}kT
$$

其中 $m$ 为单个分子的质量。

#### 理想气体压强公式

$$
p=\frac{1}{3}nm\overline{v^2}=\frac{2}{3}n\overline{\varepsilon}_{\mathrm{k}}
$$

其中 $n$ 为单位体积内的分子数。

### 理想气体内能

物质的量为 $\nu$ 的理想气体的内能为

$$
E=\frac{i}{2}\nu RT=\frac{i}{2}pV
$$

其中 $i$ 为分子自由度。

<table>
  <tr>
    <td rowspan="2">分子类型</td>
    <td rowspan="2">单原子分子</td>
    <td colspan="2">双原子分子</td>
    <td colspan="2">三原子分子</td>
  </tr>
  <tr>
    <td>刚性</td>
    <td>非刚性</td>
    <td>刚性</td>
    <td>非刚性</td>
  </tr>
  <tr>
    <td>分子自由度 $i$</td>
    <td>3</td>
    <td>5</td>
    <td>7</td>
    <td>6</td>
    <td>12</td>
  </tr>
</table>

### 麦克斯韦气体分子速率分布律

#### 最概然速率 \$v_p\$

$$
\left.\frac{\mathrm{d}f(v)}{\mathrm{d}v}\right|_{v=v_p}=0
$$

$$
v_p=\sqrt{\frac{2kT}{m}}=\sqrt{\frac{2RT}{M}}
$$

其中 $M$ 为气体的摩尔质量。

#### 平均速率 \$\overline{v}\$

$$
\overline{v}=\int_0^{+\infty}vf(v)\ \mathrm{d}v
$$

$$
\overline{v}=\sqrt{\frac{8kT}{\pi m}}=\sqrt{\frac{8RT}{\pi M}}
$$

#### 方均根速率 \$v\_{rms}\$

$$
\overline{v^2}=\int_0^{+\infty}v^2f(v)\ \mathrm{d}v
$$

$$
v_{rms}=\sqrt{\overline{v^2}}=\sqrt{\frac{3kT}{m}}=\sqrt{\frac{3RT}{M}}
$$

### 分子的平均碰撞频率和平均自由程

$$
\overline{\lambda}=\frac{\overline{v}}{\overline{Z}}
$$

$$
\overline{Z}=\sqrt{2}\pi d^2\overline{v}n
$$

其中 $d$ 为分子直径，也称分子的有效直径。

$$
\overline{\lambda}=\frac{1}{\sqrt{2}\pi d^2 n}=\frac{kT}{\sqrt{2}\pi d^2p}
$$

### 热力学第一定律

$$
Q=W+\Delta E
$$

### 摩尔热容

#### 摩尔定容热容

$$
C_{V,\mathrm{m}}=\frac{\mathrm{d}Q_{V,\mathrm{m}}}{\mathrm{d}T}
$$

理论值 $\frac{i}{2}R$

#### 摩尔定压热容

$$
C_{p,\mathrm{m}}=\frac{\mathrm{d}Q_{p,\mathrm{m}}}{\mathrm{d}T}
$$

理论值 $\frac{i+2}{2}R$

#### 绝热系数（热容比）

$$
\gamma=\frac{C_{p,\mathrm{m}}}{C_{V,\mathrm{m}}}
$$

理论值 $\frac{i+2}{i}$

#### 固体热容

##### 晶体内能

物质的量为 $\nu$ 的理想晶体的内能为

$$
E=3\nu RT
$$

##### 理想晶体摩尔热容

$$
C_{\mathrm{m}}=\frac{E_m}{T}=3R
$$

##### 比热容

$$
c=\frac{C}{m'}
$$

其中 $m'$ 是固体质量。

### 理想气体的绝热过程

$$
pV^{\gamma}=\text{常量}\\
V^{\gamma-1}T=\text{常量}\\
p^{\gamma-1}T^{-\gamma}=\text{常量}
$$

注意三个常量并不相同。

### 循环过程

$$
\eta=\frac{W}{Q_1}=1-\frac{|Q_2|}{Q_1}
$$

其中 $W$ 是对外做功，$Q_1$ 是吸收热量，$Q_2$ 是放出热量。

### 熵

$$
\Delta S=S_B-S_A\int_A^B\frac{\mathrm{d}Q}{T}
$$

#### 玻耳兹曼关系式

$$
S=k\ln{W}
$$

其中 $W$ 为热力学概率，是分子热运动的系统无序度的量度。
