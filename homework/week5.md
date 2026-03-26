# week5

> **定义 1.3.2 (简单随机样本)**
> 
> 设总体 $X$ 的分布为 $F$, $X_1,X_2,\ldots,X_n$ 是从 $X$ 中抽取的容量为 $n$ 的样本. 若 $X_1,X_2,\ldots,X_n$ 相互独立, 且都与总体 $X$ 同分布, 则称它们是简单随机样本, 简称样本. (教材 $\S1.3$, p7)

> **例 2.1.3 (顺序统计量的分布)**
> 
> 设总体 $X$ 的分布函数为 $F(x)$, 密度函数为 $f(x)$, 则第 $r$ 个顺序统计量的密度为 $f_{(r)}(x)=\frac{n!}{(r-1)!(n-r)!}\left[F(x)\right]^{r-1}\left[1-F(x)\right]^{n-r}f(x)$; 特别地 $X_{(n)}$ 的分布函数为 $\left[F(x)\right]^{n}$. (教材 $\S2.1$, p21)

> **定理 2.2.1 (卡方分布的密度)**
> 
> 设 $\xi\sim\chi^{2}(n)$, 则 $\xi$ 的密度函数为 $f(x)=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}\mathrm{e}^{-x/2}$ ($x>0$), $f(x)=0$ ($x\le0$). (教材 $\S2.2$, p24)

> **定义 2.3.1 (极限分布)**
> 
> 当样本容量 $n$ 趋于无穷时, 统计量的分布趋于某个确定的分布, 则称该分布为该统计量的极限分布, 亦称渐近分布. (教材 $\S2.3$, p49)

> **定理 2.3.9 (斯卢茨基引理)**
> 
> 设 $\left\{X_n\right\}$ 与 $\left\{Y_n\right\}$ 是两个随机变量序列, 当 $n\to+\infty$ 时 $X_n\xrightarrow{L}N(0,1)$, $Y_n\xrightarrow{P}c$ ($c$ 为常数), 则 $X_n/Y_n\xrightarrow{L}N(0,1)$ 且 $X_nY_n\xrightarrow{L}N(0,c)$, 后者指 $N\left(0,c^{2}\right)$. (教材 $\S2.3$, p51)

> **定义 2.4.1 (指数族)**
> 
> 设 $F=\left\{f(x,\theta):\theta\in\Theta\right\}$ 是样本空间 $\mathcal{X}$ 上的分布族, 其中 $f(x,\theta)=C(\theta)\exp\left\{\sum_{i=1}^{k}Q_i(\theta)T_i(x)\right\}h(x)$, $C(\theta)>0$, $Q_i(\theta)$ 定义在 $\Theta$ 上, $h(x)>0$, $T_i(x)$ 定义在 $\mathcal{X}$ 上, 且支撑集 $\left\{x:f(x,\theta)>0\right\}$ 与 $\theta$ 无关, 则称此分布族为指数型分布族, 简称指数族. (教材 $\S2.4$, p54)

> **定义 2.4.2 (指数族的自然形式)**
> 
> 若指数族可写为 $f(x,\varphi)=C(\varphi)\exp\left\{\sum_{i=1}^{k}\varphi_iT_i(x)\right\}h(x)$, 则称其为指数族的自然形式, 集合 $\Theta^{*}=\left\{\varphi:\int_{\mathcal{X}}\exp\left\{\sum_{i=1}^{k}\varphi_iT_i(x)\right\}h(x)\,\mathrm{d}x<+\infty\right\}$ 称为自然参数空间. (教材 $\S2.4$, p57)

> **定理 2.4.1 (自然参数空间的凸性)**
> 
> 在指数族的自然形式下, 自然参数空间 $\Theta^{*}$ 是凸集. (教材 $\S2.4$, p58)

## 习题 2.3-19 (均匀总体样本均值的极限分布)

设 $X_1,X_2,\ldots,X_n$ 是来自均匀分布总体 $U(0,\theta)$, $\theta>0$ 的样本, 求 $\frac{\bar{X}-\theta/2}{\sqrt{\theta^{2}/\left(12n\right)}}$ 的极限分布.

### 解答 2.3-19

$U(0,\theta)$ 的均值与方差为

$$
E\left(X_1\right)=\frac{\theta}{2},\qquad D\left(X_1\right)=\frac{\theta^{2}}{12}.
$$

把题中的统计量写成标准形状:

$$
\frac{\bar{X}-\theta/2}{\sqrt{\theta^{2}/\left(12n\right)}}=\frac{\bar{X}-E\left(X_1\right)}{\sqrt{D\left(X_1\right)/n}}.
$$

$X_1,\ldots,X_n$ 独立同分布, 方差有限且为正, 由中心极限定理, 样本均值的标准化依分布收敛于 $N(0,1)$. 按**定义 2.3.1 (极限分布)**, 该统计量的极限分布是 $N(0,1)$.

$\blacksquare$

## 习题 2.3-20 (泊松总体用样本均值估计方差的极限分布)

若 $X_1,X_2,\ldots,X_n$ 是来自泊松分布总体 $P(\lambda)$, $\lambda>0$ 的样本, 求 $\frac{\bar{X}-\lambda}{\sqrt{\bar{X}/n}}$ 的极限分布.

### 解答 2.3-20

泊松分布 $P(\lambda)$ 的均值与方差同为 $\lambda$. 由中心极限定理,

$$
U_n=\frac{\bar{X}-\lambda}{\sqrt{\lambda/n}}\xrightarrow{L}N(0,1).
$$

又由大数定律, $\bar{X}\xrightarrow{P}\lambda$, 函数 $1/x$ 在 $x=\lambda>0$ 处连续, 故

$$
V_n=\sqrt{\frac{\lambda}{\bar{X}}}\xrightarrow{P}1.
$$

把题中的统计量写成 $U_nV_n$:

$$
\frac{\bar{X}-\lambda}{\sqrt{\bar{X}/n}}=\frac{\bar{X}-\lambda}{\sqrt{\lambda/n}}\cdot\sqrt{\frac{\lambda}{\bar{X}}}=U_nV_n.
$$

由**定理 2.3.9 (斯卢茨基引理)**, $U_nV_n\xrightarrow{L}N(0,1)$. 按**定义 2.3.1 (极限分布)**, 所求极限分布为 $N(0,1)$.

$\blacksquare$

## 习题 2.3-21 (均匀总体的最大顺序统计量与极差)

设 $X_1,X_2,\ldots,X_n$ 是来自均匀分布总体 $U(0,1)$ 的样本, $X_{(1)},\ldots,X_{(n)}$ 为顺序统计量,

(1) 若使 $P\left\{X_{(n)}\ge0.99\right\}$ 至少为 $0.95$, 则样本容量至少取多少?

(2) 求极差 $R_n=X_{(n)}-X_{(1)}$ 的密度函数;

(3) 当 $n$ 趋于无穷时, 求 $Z=2n\left(1-R_n\right)$ 的极限分布.

### 解答 2.3-21

$U(0,1)$ 的分布函数为 $F(x)=x$ ($0\le x\le1$). 由**例 2.1.3 (顺序统计量的分布)**, $X_{(n)}$ 的分布函数为 $\left[F(x)\right]^{n}=x^{n}$.

(1) 由上式,

$$
P\left\{X_{(n)}\ge0.99\right\}=1-P\left\{X_{(n)}<0.99\right\}=1-0.99^{n}.
$$

要求 $1-0.99^{n}\ge0.95$, 即 $0.99^{n}\le0.05$, 取对数

$$
n\ge\frac{\ln0.05}{\ln0.99}=\frac{-2.9957}{-0.01005}\approx298.1.
$$

故样本容量至少取 $299$.

$\blacksquare$

(2) 先求 $\left(X_{(1)},X_{(n)}\right)$ 的联合密度. 对 $0<x<y<1$,

$$
P\left\{X_{(1)}>x,\ X_{(n)}\le y\right\}=\left(y-x\right)^{n},
$$

因为该事件等价于全部 $n$ 个观测落进 $\left(x,y\right]$. 对 $x$ 与 $y$ 各求一次偏导, 得联合密度

$$
f_{(1)(n)}(x,y)=n(n-1)\left(y-x\right)^{n-2},\quad 0<x<y<1.
$$

作变换 $r=y-x$, 保留 $x$, 则 $y=x+r$, 雅可比行列式为 $1$. 在 $x$ 上积分, 范围为 $0<x<1-r$, 得

$$
f_{R_n}(r)=n(n-1)r^{n-2}\left(1-r\right),\quad 0<r<1.
$$

$\blacksquare$

(3) 由 (2), $R_n$ 的分布函数为

$$
F_{R_n}(r)=\int_{0}^{r}n(n-1)s^{n-2}\left(1-s\right)\mathrm{d}s=nr^{n-1}-(n-1)r^{n},\quad 0<r<1.
$$

固定 $z>0$, 当 $n$ 充分大时 $z/\left(2n\right)<1$, 于是

$$
P\left\{Z>z\right\}=P\left\{2n\left(1-R_n\right)>z\right\}=P\left\{R_n<1-\frac{z}{2n}\right\}=F_{R_n}\left(1-\frac{z}{2n}\right).
$$

记 $\varepsilon=z/\left(2n\right)$, 把上式整理,

$$
F_{R_n}\left(1-\varepsilon\right)=n\left(1-\varepsilon\right)^{n-1}-(n-1)\left(1-\varepsilon\right)^{n}=\left(1-\varepsilon\right)^{n-1}\left[n-(n-1)\left(1-\varepsilon\right)\right].
$$

方括号内等于 $1+(n-1)\varepsilon=1+\frac{(n-1)z}{2n}$. 又 $\left(1-\varepsilon\right)^{n-1}\to\mathrm{e}^{-z/2}$, 故

$$
\lim_{n\to+\infty}P\left\{Z>z\right\}=\mathrm{e}^{-z/2}\left(1+\frac{z}{2}\right).
$$

由**定理 2.2.1 (卡方分布的密度)** 取 $n=4$, $\chi^{2}(4)$ 的密度为 $\frac{1}{4}x\mathrm{e}^{-x/2}$, 其尾概率为

$$
\int_{z}^{+\infty}\frac{1}{4}x\mathrm{e}^{-x/2}\,\mathrm{d}x=\frac{1}{4}\left(z+2\right)\mathrm{e}^{-z/2}=\mathrm{e}^{-z/2}\left(1+\frac{z}{2}\right),
$$

与上面的极限一致. 按**定义 2.3.1 (极限分布)**, $Z$ 的极限分布是 $\chi^{2}(4)$.

$\blacksquare$

## 习题 2.4-3 (幂函数总体的样本分布族)

设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, 且 $X$ 的密度函数为 $f(x)=\theta x^{\theta-1}$ ($0<x<1$), $f(x)=0$ (其他), 证明样本分布族是指数族, 并表成指数族的自然形式, 求出自然参数空间.

### 解答 2.4-3

单个边缘密度可写成

$$
f(x,\theta)=\theta x^{\theta-1}=\theta\cdot\frac{1}{x}\exp\left\{\theta\ln x\right\},\quad 0<x<1,
$$

其支撑集 $\left(0,1\right)$ 与 $\theta$ 无关. 由**定义 1.3.2 (简单随机样本)**, 联合密度为各边缘之积,

$$
f\left(x_1,\ldots,x_n,\theta\right)=\theta^{n}\prod_{i=1}^{n}\frac{1}{x_i}\exp\left\{\theta\sum_{i=1}^{n}\ln x_i\right\}=C(\theta)\exp\left\{Q(\theta)T(x)\right\}h(x),
$$

其中 $C(\theta)=\theta^{n}$, $Q(\theta)=\theta$, $T(x)=\sum_{i=1}^{n}\ln x_i$, $h(x)=\prod_{i=1}^{n}x_i^{-1}$. 由**定义 2.4.1 (指数族)**, 样本分布族是指数族.

自然形式取 $\varphi=Q(\theta)=\theta$, 则

$$
f(x,\varphi)=\varphi^{n}\exp\left\{\varphi\sum_{i=1}^{n}\ln x_i\right\}\prod_{i=1}^{n}\frac{1}{x_i}.
$$

按**定义 2.4.2 (指数族的自然形式)**, 自然参数空间为

$$
\Theta^{*}=\left\{\varphi:\int_{0}^{1}\cdots\int_{0}^{1}\exp\left\{\varphi\sum_{i=1}^{n}\ln x_i\right\}\prod_{i=1}^{n}\frac{1}{x_i}\,\mathrm{d}x_1\cdots\mathrm{d}x_n<+\infty\right\}.
$$

被积函数在 $\left(0,1\right)^{n}$ 上连续且可积, 故 $\Theta^{*}$ 就是 $\varphi$ 的取值范围 $\left(0,+\infty\right)$, 它是凸集, 与**定理 2.4.1 (自然参数空间的凸性)** 相符.

$\blacksquare$

## 习题 2.4-4 (拉普拉斯总体的样本分布族)

设 $X_1,X_2,\ldots,X_n$ 是来自拉普拉斯分布的样本, 其密度函数为 $f(x)=\frac{1}{2\theta}\mathrm{e}^{-\left|x\right|/\theta}$, $-\infty<x<+\infty$, $\theta>0$. 证明样本分布族是指数族, 并表成指数族的自然形式, 求出自然参数空间.

### 解答 2.4-4

边缘密度写成

$$
f(x,\theta)=\frac{1}{2\theta}\exp\left\{-\frac{1}{\theta}\left|x\right|\right\},\quad x\in\mathbb{R},
$$

支撑集 $\mathbb{R}$ 与 $\theta$ 无关. 联合密度

$$
f\left(x_1,\ldots,x_n,\theta\right)=\left(2\theta\right)^{-n}\exp\left\{-\frac{1}{\theta}\sum_{i=1}^{n}\left|x_i\right|\right\}=C(\theta)\exp\left\{Q(\theta)T(x)\right\}h(x),
$$

其中 $C(\theta)=\left(2\theta\right)^{-n}$, $Q(\theta)=-1/\theta$, $T(x)=\sum_{i=1}^{n}\left|x_i\right|$, $h(x)=1$. 由**定义 2.4.1 (指数族)**, 样本分布族是指数族.

自然形式取 $\varphi=-1/\theta$, 则 $\theta=-1/\varphi$,

$$
f(x,\varphi)=C(\varphi)\exp\left\{\varphi\sum_{i=1}^{n}\left|x_i\right|\right\},\qquad C(\varphi)=\left(-\frac{2}{\varphi}\right)^{-n}.
$$

按**定义 2.4.2 (指数族的自然形式)**, 自然参数空间为

$$
\Theta^{*}=\left\{\varphi:\int_{\mathbb{R}^{n}}\exp\left\{\varphi\sum_{i=1}^{n}\left|x_i\right|\right\}\mathrm{d}x_1\cdots\mathrm{d}x_n<+\infty\right\}=\left(-\infty,0\right),
$$

因为 $\varphi\ge0$ 时积分发散. 该集合是凸集.

$\blacksquare$

## 习题 2.4-5 (瑞利总体的样本分布族)

设 $X_1,X_2,\ldots,X_n$ 是来自瑞利分布的样本, 其密度函数为 $f(x)=2\theta x\mathrm{e}^{-\theta x^{2}}$ ($x>0$), $f(x)=0$ (其他), $\theta>0$. 证明样本分布族是指数族, 并表示成指数族的自然形式, 求出自然参数空间.

### 解答 2.4-5

边缘密度写成

$$
f(x,\theta)=2\theta x\exp\left\{-\theta x^{2}\right\},\quad x>0,
$$

支撑集 $\left(0,+\infty\right)$ 与 $\theta$ 无关. 联合密度

$$
f\left(x_1,\ldots,x_n,\theta\right)=\left(2\theta\right)^{n}\prod_{i=1}^{n}x_i\exp\left\{-\theta\sum_{i=1}^{n}x_i^{2}\right\}=C(\theta)\exp\left\{Q(\theta)T(x)\right\}h(x),
$$

其中 $C(\theta)=\left(2\theta\right)^{n}$, $Q(\theta)=-\theta$, $T(x)=\sum_{i=1}^{n}x_i^{2}$, $h(x)=\prod_{i=1}^{n}x_i$. 由**定义 2.4.1 (指数族)**, 样本分布族是指数族.

自然形式取 $\varphi=-\theta$, 则

$$
f(x,\varphi)=\left(-2\varphi\right)^{n}\prod_{i=1}^{n}x_i\exp\left\{\varphi\sum_{i=1}^{n}x_i^{2}\right\}.
$$

按**定义 2.4.2 (指数族的自然形式)**, 自然参数空间为

$$
\Theta^{*}=\left\{\varphi:\int_{0}^{+\infty}\cdots\int_{0}^{+\infty}\exp\left\{\varphi\sum_{i=1}^{n}x_i^{2}\right\}\prod_{i=1}^{n}x_i\,\mathrm{d}x_1\cdots\mathrm{d}x_n<+\infty\right\}=\left(-\infty,0\right),
$$

因为 $\varphi\ge0$ 时积分发散. 该集合是凸集.

$\blacksquare$

## 习题 2.4-6 (指数分布的样本分布族)

设 $X_1,X_2,\ldots,X_n$ 是来自指数分布 $E(\lambda)$ 的样本, 指数分布的密度函数为 $f(x)=\lambda\mathrm{e}^{-\lambda{}x}$ ($x>0$), $f(x)=0$ (其他). 证明样本分布族是指数族, 并表示成指数族的自然形式, 求出自然参数空间.

### 解答 2.4-6

边缘密度写成

$$
f(x,\lambda)=\lambda\mathrm{e}^{-\lambda{}x},\quad x>0,
$$

支撑集 $\left(0,+\infty\right)$ 与 $\lambda$ 无关. 联合密度

$$
f\left(x_1,\ldots,x_n,\lambda\right)=\lambda^{n}\exp\left\{-\lambda\sum_{i=1}^{n}x_i\right\}=C(\lambda)\exp\left\{Q(\lambda)T(x)\right\}h(x),
$$

其中 $C(\lambda)=\lambda^{n}$, $Q(\lambda)=-\lambda$, $T(x)=\sum_{i=1}^{n}x_i$, $h(x)=1$. 由**定义 2.4.1 (指数族)**, 样本分布族是指数族.

自然形式取 $\varphi=-\lambda$, 则

$$
f(x,\varphi)=\left(-\varphi\right)^{n}\exp\left\{\varphi\sum_{i=1}^{n}x_i\right\}.
$$

按**定义 2.4.2 (指数族的自然形式)**, 自然参数空间为

$$
\Theta^{*}=\left\{\varphi:\int_{0}^{+\infty}\cdots\int_{0}^{+\infty}\exp\left\{\varphi\sum_{i=1}^{n}x_i\right\}\mathrm{d}x_1\cdots\mathrm{d}x_n<+\infty\right\}=\left(-\infty,0\right),
$$

因为 $\varphi\ge0$ 时积分发散. 该集合是凸集.

$\blacksquare$
