+++
weight = -4
image = ''
categories = ['大学学习']
date = '2024-12-17T14:28:43+08:00'
title = '大学物理 B 期末复习知识点'
description = '大学物理 B 的一些重要公式归纳总结（持续更新中）'
tags = ['大学物理']
lastmod = '2024-12-19T00:14:43+08:00'
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

#### 卡诺定理

对于可逆卡诺热机

$$
\eta=1-\frac{T_2}{T_1}
$$

其中 $T_1$ 为高温热源温度，$T_2$ 为低温热源温度。

### 熵

$$
\Delta S=S_B-S_A=\int_A^B\frac{\mathrm{d}Q}{T}
$$

#### 玻耳兹曼关系式

$$
S=k\ln{W}
$$

其中 $W$ 为热力学概率，是分子热运动的系统无序度的量度。

## 光学

可见光谱范围 360-400nm 到 760-830nm

### 杨氏双缝干涉

波程差

$$
\Delta r=r_2-r_1\approx d\sin{\theta}
$$

其中 $d$ 为双缝间的距离。

明条纹中心

$$
\Delta r=\pm k\lambda
$$

$$
x=\pm\frac{d'}{d}k\lambda
$$

其中 $d'$ 为双缝与光屏间的距离。

暗条纹中心

$$
\Delta r=\pm\frac{2k+1}{2}\lambda
$$

$$
x=\pm\frac{d'}{d}\frac{2k+1}{2}\lambda
$$

相邻明纹或暗纹中心间距

$$
\Delta x=\frac{d'}{d}\lambda
$$

#### 半波损失

光从折射率较小的介质射向折射率较大的介质时，反射光的相位较之入射光的相位跃变了 $\pi$，相当于附加了半个波长的波程差，称之为半波损失。

### 劈尖干涉

劈尖厚度为 $d$ 处的光程差

$$
\Delta =2nd+\frac{\lambda}{2}
$$

其中 $n$ 为劈尖层介质的折射率。明暗条纹中心条件与[双缝干涉](#杨氏双缝干涉)类似。

相邻明纹或暗纹中心间距 $b$

$$
b\approx\frac{\lambda}{2n\theta}
$$

### 牛顿环

与劈尖干涉类似，介质层厚度为 $d$ 处的光程差

$$
\Delta =2nd+\frac{\lambda}{2}
$$

明环半径

$$
r=\sqrt{(k-\frac{1}{2})\frac{R\lambda}{n}}
$$

其中 $R$ 为平凸透镜的曲率半径。

暗环半径

$$
r=\sqrt{\frac{kR\lambda}{n}}
$$

### 菲涅耳衍射和夫琅禾费衍射

菲涅耳衍射中，光源和光屏，与衍射孔之间的距离是有限的；反之，光源和光屏都移到无限远处，这种衍射叫做夫琅禾费衍射。

### 夫琅禾费单缝衍射

明条纹中心

$$
b\sin{\theta}=\pm\frac{2k+1}{2}\lambda
$$

其中 $b$ 为单缝宽度。

暗条纹中心

$$
b\sin{\theta}=\pm k\lambda
$$

注意这里的明暗关系与双缝干涉正好相反。

中央明纹宽度

$$
\Delta x_0=2x_1=\frac{2\lambda f}{b}
$$

其余相邻暗纹之间距离

$$
\Delta x=\frac{\lambda f}{b}
$$

### 光学仪器的分辨本领

瑞利判据指出，当一个点光源的衍射图样的中央明纹与另一个点光源的衍射图样的第一级暗纹重合时，这两个点光源恰好可以被分辨。

对于夫琅禾费圆孔衍射，最小分辨角

$$
\theta_0=\frac{1.22\lambda}{D}
$$

### 衍射光栅

设光栅不透光的宽度为 $b'$，透光的宽度为 $b$，则光栅常量

$$
d=b+b'
$$

明暗条纹中心条件与[双缝干涉](#杨氏双缝干涉)类似。注意光栅光谱中一般不包含中央明条纹。

当入射光线与光栅平面法线成角度 $i$ 时，明暗条纹中心条件变为

$$
d(\sin{\theta}+\sin{i})=\pm k\lambda
$$

$$
d(\sin{\theta}+\sin{i})=\pm\frac{2k+1}{2}\lambda
$$

### 马吕斯定律

从检偏器透出的光的振幅为

$$
E=E_0\cos{\alpha}
$$

光强为

$$
I=I_0\cos^2{\alpha}
$$

### 反射光和折射光的偏振

当光从折射率为 $n_1$ 的介质射入折射率为 $n_2$ 的介质中时，入射角 $i_B$ 满足

$$
\tan{i_B}=\frac{n_2}{n_1}
$$

时，反射光为偏振光，只有垂直于入射面的光振动，$i_B$ 叫做起偏角或布儒斯特角。当入射角为起偏角时，反射光与折射光相互垂直。

### 双折射

对于某些晶体，当光线进入晶体后，一束入射光线可以有两束折射光，且都是线偏振光，寻常光线（o 光）和非常光线（e 光）。\
当光线在晶体的某一表面入射时，此表面的法线与晶体的光轴所构成的平面叫做晶体的主截面，o 光的光振动垂直于主截面，e 光的光振动在主截面内。

### 几何光学

折射定律

$$
n_1\sin{i_1}=n_2\sin{i_2}
$$

薄透镜的高斯公式

$$
\frac{f'}{p'}+\frac{f}{p}=1
$$

其中 $f,f'$ 分别为物方焦距和像方焦距，$p$ 为物距，$p'$ 为像距（注意正负关系）。

## 近代物理

### 黑体辐射

#### 斯特藩-玻耳兹曼定律

$$
M(T)=\sigma T^4
$$

其中 $M(T)$ 为黑体的辐出度，是单位时间内从温度为 $T$ 的黑体的单位面积上，所辐射出的各种波长的电磁波的能量总和。

#### 维恩位移定律

单色辐出度 $M_{\lambda}(T)$ 的峰值对应的波长 $\lambda_{\mathrm{m}}$ 与 $T$ 成反比

$$
\lambda_{\mathrm{m}}T=b
$$

#### 瑞利-金斯公式

$$
M_{\nu}(T)\mathrm{d}\nu=\frac{2\pi\nu^2}{c^2}kT\mathrm{d}\nu
$$

#### 维恩公式

$$
M_{\nu}(T)\mathrm{d}\nu=\frac{2\pi h\nu^3}{c^2}\frac{\mathrm{d}\nu}{e^{\frac{h\nu}{kT}}}
$$

#### 普朗克黑体辐射公式

$$
M_{\nu}(T)\mathrm{d}\nu=\frac{2\pi h\nu^3}{c^2}\frac{\mathrm{d}\nu}{e^{\frac{h\nu}{kT}}-1}
$$

### 光电效应

遏止电势差 $U_0$

$$
E_{\mathrm{k},\max}=eU_0
$$

#### 实验规律

1. 对某一种金属来说，只有当入射光频率大于截止频率 $\nu_0$ 时，电子才能从金属表面逸出，电路中才有光电流；
2. 用不同频率的光照射金属 $K$ 的表面时，只要入射光频率大于截止频率，遏止电势差与入射光频率具有线性关系；
3. 随着加速电势差的增大，光电流趋于一个饱和值，且在入射光频率不变的情况下，饱和光电流与入射光强度成正比；
4. 无论入射光强度如何，只要其频率大于截止频率，则当光照射到金属表面上时，几乎立即就有光电子逸出。

#### 爱因斯坦方程

$$
h\nu=\frac{1}{2}mv^2+W
$$

其中 $W$ 为逸出功。

截止频率 $\nu_0$

$$
\nu_0=\frac{W}{h}
$$

### 氢原子的玻尔理论

氢原子光谱公式的一般形式

$$
\sigma=\frac{1}{\lambda}=R\left(\frac{1}{n_{\mathrm{f}}^2}-\frac{1}{n_{\mathrm{i}}^2}\right)
$$

#### 量子化条件

电子以速度 $v$ 在半径为 $r$ 的圆周上绕核运动时，只有电子的角动量 $L$ 等于 $\frac{h}{2\pi}$ 的整数倍的那些轨道才是稳定的，即

$$
L=mvr=n\frac{h}{2\pi}
$$

氢原子具有的能量

$$
E_n=\frac{E_1}{n^2}
$$

其中 $E_1=-13.6\ \mathrm{eV}$

电子轨道半径

$$
r_n=a_0n^2
$$

其中 $a_0$ 是电子的第一个（即 $n=1$）轨道的半径，叫做玻尔半径。

#### 氢原子光谱线系

| 谱线系名称及发现年代        | 谱线波段 | $n_f$ | $n_i$     | 谱线公式                                                                     |
| --------------------------- | -------- | ----- | --------- | ---------------------------------------------------------------------------- |
| 莱曼 (Lyman) 系, 1916       | 紫外线   | 1     | 2, 3, ... | $\sigma = \frac{1}{\lambda} = R\left(\frac{1}{1^2} - \frac{1}{n_i^2}\right)$ |
| 巴耳末 (Balmer) 系, 1885    | 可见光   | 2     | 3, 4, ... | $\sigma = \frac{1}{\lambda} = R\left(\frac{1}{2^2} - \frac{1}{n_i^2}\right)$ |
| 帕邢 (Paschen) 系, 1908     | 红外线   | 3     | 4, 5, ... | $\sigma = \frac{1}{\lambda} = R\left(\frac{1}{3^2} - \frac{1}{n_i^2}\right)$ |
| 布拉开 (Brackett) 系, 1922  | 红外线   | 4     | 5, 6, ... | $\sigma = \frac{1}{\lambda} = R\left(\frac{1}{4^2} - \frac{1}{n_i^2}\right)$ |
| 普丰德 (Pfund) 系, 1924     | 红外线   | 5     | 6, 7, ... | $\sigma = \frac{1}{\lambda} = R\left(\frac{1}{5^2} - \frac{1}{n_i^2}\right)$ |
| 汉弗莱 (Humphreys) 系, 1953 | 红外线   | 6     | 7, 8, ... | $\sigma = \frac{1}{\lambda} = R\left(\frac{1}{6^2} - \frac{1}{n_i^2}\right)$ |

### 德布罗意波

以动量 $p$ 运动的实物粒子的波的波长为

$$
\lambda=\frac{h}{p}
$$

### 不确定关系

$$
\Delta x\Delta p_x\geq h
$$

### 量子物理

#### 四个量子数

1. 主量子数 $n$：决定电子能级、电子云平均距离；$n=1$ 时，氢原子能量处于最小允许值的定态，称氢原子处于基态；$n=2,3,\dots$ 时，氢原子处于激发态
2. 角量子数 $l$：决定电子云形状、轨道角动量；$l$ 的可能值为 $0,1,2,\dots,(n-1)$\
   氢原子中电子的角动量 $L$ 为

   $$
   L=\sqrt{l(l+1)}\frac{h}{2\pi}=\sqrt{l(l+1)}\hbar
   $$

   其中 $\hbar$ 为约化普朗克常量

3. 磁量子数 $m_l$：决定电子云空间取向；$m_l$ 的可能值为 $0,\pm 1,\pm 2,\dots,\pm l$\
   角动量在 $z$ 轴上的分量 $L_z$ 为

   $$
   L_z=m_l\hbar
   $$

4. 自旋磁量子数 $m_s$：决定电子自旋状态方向；$m_s$ 的可能值为 $\pm\frac{1}{2}$

#### 多电子原子中的电子分布

1. 泡利不相容原理：在一个原子中，不可能有两个或两个以上的电子具有完全相同的量子态；
2. 能量最小原理：在原子系统内，每个电子趋向于占有最低的能级，当原子中电子的能量最小时，整个原子的能量最小，这时原子处于最稳定的状态，即基态。

#### 一维势阱问题

##### 无限深方势阱

势阱中粒子可能的能量值为

$$
E=n^2\frac{h^2}{8ma^2}
$$

其中 $a$ 为无限深方势阱的宽度。

波函数

$$
\Psi(x)=\sqrt{\frac{2}{a}}\sin{\frac{n\pi}{a}x}
$$

概率密度

$$
|\Psi^2(x)|=\frac{2}{a}\sin^2{\frac{n\pi}{a}x}
$$

##### 一维方势垒

一维线性谐振子势函数

$$
E_{\mathrm{p}}x=\frac{1}{2}kx^2=\frac{1}{2}m\omega^2x^2
$$

其中 $m$ 为振子质量，$\omega$ 为固有频率；

能量本征值

$$
E_n=\left(n+\frac{1}{2}\right)\hbar\omega=\left(n+\frac{1}{2}\right)h\nu
$$