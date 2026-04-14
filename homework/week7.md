# week7

> **例 2.1.3 (顺序统计量的分布)**
> 
> 设总体 $X$ 的密度函数为 $f(x)$, 分布函数为 $F(x)$, $X_{(k)}$ 为第 $k$ 个顺序统计量, 则 $X_{(k)}$ 的密度函数为 $g_k(y)=\frac{n!}{(k-1)!(n-k)!}\left[F(y)\right]^{k-1}\left[1-F(y)\right]^{n-k}f(y)$. (教材 $\S2.1$, p21)

> **定义 2.4.2 (指数族的自然形式)**
> 
> 若指数族可写为 $f(x,\varphi)=C(\varphi)\exp\left\{\sum_{i=1}^{k}\varphi_iT_i(x)\right\}h(x)$, 则称其为指数族的自然形式, 集合 $\Theta^{*}=\left\{\varphi:\int_{\mathcal{X}}\exp\left\{\sum_{i=1}^{k}\varphi_iT_i(x)\right\}h(x)\,\mathrm{d}x<+\infty\right\}$ 称为自然参数空间. (教材 $\S2.4$, p57)

> **定理 2.5.1 (因子分解定理)**
> 
> 设样本的联合密度 (或联合分布列) 为 $f\left(x_1,\ldots,x_n,\theta\right)$, $T=T\left(X_1,\ldots,X_n\right)$ 是统计量, 则 $T$ 为充分统计量的充要条件是 $f\left(x_1,\ldots,x_n,\theta\right)=g\left(t\left(x_1,\ldots,x_n\right),\theta\right)h\left(x_1,\ldots,x_n\right)$, 其中 $h$ 不依赖于 $\theta$. (教材 $\S2.5$, p63)

> **定义 2.6.1 (完备统计量)**
> 
> 设分布族为 $\left\{f(x,\theta):\theta\in\Theta\right\}$, $T=T\left(X_1,\ldots,X_n\right)$ 为统计量. 若对任何满足 $E_{\theta}\left[\varphi\left(T\right)\right]=0$ (对一切 $\theta\in\Theta$) 的函数 $\varphi$, 都有 $P_{\theta}\left\{\varphi\left(T\right)=0\right\}=1$ 对一切 $\theta$, 则称 $T$ 为完备统计量; 完备统计量的任一可测函数仍为完备统计量. (教材 $\S2.6$, p67)

> **定理 2.6.1 (指数族中统计量的完备性)**
> 
> 设 $X_1,\ldots,X_n$ 是从自然形式为 $f(x,\theta)=C(\theta)\exp\left\{\sum_{i=1}^{k}\theta_iT_i(x)\right\}h(x)$ 的指数族中抽取的样本, $\theta\in\Theta^{*}$, 若自然参数空间 $\Theta^{*}$ 有内点, 则 $\left(T_1,\ldots,T_k\right)$ 为完备统计量. (教材 $\S2.6$, p68)

> **定义 3.2.1 (矩估计)**
> 
> 设 $F=\left\{f(x,\theta):\theta\in\Theta\right\}$ 是参数分布族, $\theta=\left(\theta_1,\ldots,\theta_m\right)$, $X_1,\ldots,X_n$ 是样本, 总体 $k$ 阶原点矩 $\alpha_k\left(\theta_1,\ldots,\theta_m\right)$ 存在. 令 $\alpha_k\left(\theta_1,\ldots,\theta_m\right)=A_k=\frac{1}{n}\sum_{i=1}^{n}X_i^{k}$, $k=1,2,\ldots,m$, 解此方程组所得 $\theta$ 的估计称为矩估计. (教材 $\S3.2$, p73)

> **定义 3.3.1 (似然函数)**
> 
> 设总体 $X$ 的密度函数 (或分布列) 为 $f(x,\theta)$, $x_1,\ldots,x_n$ 为样本观察值, 称 $L\left(\theta\right)=L\left(\theta,x_1,\ldots,x_n\right)=\prod_{i=1}^{n}f\left(x_i,\theta\right)$ ($\theta\in\Theta$) 为样本的似然函数. (教材 $\S3.3$, p82)

> **定义 3.3.2 (极大似然估计)**
> 
> 若似然函数在 $\hat{\theta}$ 处达到极大值, 即 $L\left(\hat{\theta},x_1,\ldots,x_n\right)=\sup_{\theta\in\Theta}L\left(\theta,x_1,\ldots,x_n\right)$, 则称 $\hat{\theta}\left(x_1,\ldots,x_n\right)$ 为极大似然估计值, $\hat{\theta}\left(X_1,\ldots,X_n\right)$ 为极大似然估计量. (教材 $\S3.3$, p84)

## 习题 2.6-6 (指数总体样本均值的完备性)

设 $X_1,X_2,\ldots,X_n$ 是来自指数分布 $E(\lambda)$ 的样本, 其密度函数为 $f(x)=\lambda\mathrm{e}^{-\lambda{}x}$ ($x>0$), $f(x)=0$ ($x\le0$). 证明 $\bar{X}$ 为完备统计量.

### 解答 2.6-6

记 $T=\sum_{i=1}^{n}X_i$. 联合密度为

$$
f\left(x_1,\ldots,x_n,\lambda\right)=\lambda^{n}\exp\left\{-\lambda\sum_{i=1}^{n}x_i\right\},
$$

按**定义 2.4.2 (指数族的自然形式)**, 取 $\varphi=-\lambda$, $T_1(x)=\sum x_i$, $C(\varphi)=\left(-\varphi\right)^{n}$, $h=1$, 自然参数空间为 $\Theta^{*}=\left(-\infty,0\right)$, 每点都是内点. 由**定理 2.6.1 (指数族中统计量的完备性)**, $T$ 是完备统计量.

$\bar{X}=T/n$ 是 $T$ 的可测函数. 由**定义 2.6.1 (完备统计量)** 所附的说明, 完备统计量的任一可测函数仍为完备统计量, 故 $\bar{X}$ 完备.

$\blacksquare$

## 习题 2.6-7 (正态总体按已知参数分情况的完备统计量)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本.

(1) 在 $\mu$ 已知时, 给出 $\sigma^{2}$ 的一个完备统计量;

(2) 在 $\sigma^{2}$ 已知时, 给出 $\mu$ 的一个完备统计量.

### 解答 2.6-7

联合密度为

$$
f\left(x_1,\ldots,x_n,\mu,\sigma^{2}\right)=\left(2\pi\sigma^{2}\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^{2}}\sum_{i=1}^{n}\left(x_i-\mu\right)^{2}\right\}.
$$

(1) $\mu$ 已知时, 只余 $\sigma^{2}$ 未知. 记 $T_1(x)=\sum_{i=1}^{n}\left(x_i-\mu\right)^{2}$, 把密度写成自然形式

$$
f\left(x,\varphi\right)=C(\varphi)\exp\left\{\varphi T_1(x)\right\},\qquad \varphi=-\frac{1}{2\sigma^{2}},\quad C(\varphi)=\left(-\frac{\pi}{\varphi}\right)^{-n/2},
$$

自然参数空间 $\Theta^{*}=\left(-\infty,0\right)$ 有内点. 由**定理 2.6.1 (指数族中统计量的完备性)**, $T=\sum_{i=1}^{n}\left(X_i-\mu\right)^{2}$ 是 $\sigma^{2}$ 的完备统计量.

$\blacksquare$

(2) $\sigma^{2}$ 已知时, 只余 $\mu$ 未知. 把平方展开, 密度写成

$$
f\left(x,\varphi\right)=C(\varphi)\exp\left\{\varphi T_1(x)\right\}h(x),\qquad \varphi=\frac{\mu}{\sigma^{2}},\quad T_1(x)=\sum_{i=1}^{n}x_i,
$$

其中 $C(\varphi)=\left(2\pi\sigma^{2}\right)^{-n/2}\exp\left\{-n\sigma^{2}\varphi^{2}/2\right\}$, $h(x)=\exp\left\{-\sum x_i^{2}/\left(2\sigma^{2}\right)\right\}$ 不含 $\mu$. 自然参数空间为 $\Theta^{*}=\mathbb{R}$, 每点都是内点. 由**定理 2.6.1 (指数族中统计量的完备性)**, $T=\sum_{i=1}^{n}X_i$ 是 $\mu$ 的完备统计量.

$\blacksquare$

## 习题 2.6-10 (均匀总体的充分但不完备统计量)

设 $X_1,X_2,\ldots,X_n$ 是来自均匀分布总体 $U[\theta,2\theta]$, $\theta>0$ 的样本, 证明 $\left(X_{(1)},X_{(n)}\right)$ 是充分统计量但不是完备统计量.

### 解答 2.6-10

(1) 充分性. 联合密度为

$$
f\left(x_1,\ldots,x_n,\theta\right)=\theta^{-n}I\left\{x_{(1)}\ge\theta\right\}I\left\{x_{(n)}\le2\theta\right\},
$$

其中 $I$ 为示性函数. 取 $t=\left(x_{(1)},x_{(n)}\right)$, $g\left(t,\theta\right)=\theta^{-n}I\left\{t_1\ge\theta\right\}I\left\{t_2\le2\theta\right\}$, $h(x)=1$, 则 $h$ 不含 $\theta$, 由**定理 2.5.1 (因子分解定理)**, $T=\left(X_{(1)},X_{(n)}\right)$ 是充分统计量.

$\blacksquare$

(2) 不完备性. 由**例 2.1.3 (顺序统计量的分布)** 中两端顺序统计量的矩的计算, 对 $U[a,b]$,

$$
E\left(X_{(1)}\right)=a+\frac{b-a}{n+1},\qquad E\left(X_{(n)}\right)=b-\frac{b-a}{n+1}.
$$

本题 $a=\theta$, $b=2\theta$, 故

$$
E\left(X_{(1)}\right)=\theta+\frac{\theta}{n+1}=\frac{n+2}{n+1}\theta,\qquad E\left(X_{(n)}\right)=2\theta-\frac{\theta}{n+1}=\frac{2n+1}{n+1}\theta.
$$

取 $T$ 的函数

$$
\psi\left(T\right)=\left(n+2\right)X_{(n)}-\left(2n+1\right)X_{(1)}.
$$

它满足

$$
E\left[\psi\left(T\right)\right]=\frac{\left(n+2\right)\left(2n+1\right)-\left(2n+1\right)\left(n+2\right)}{n+1}\theta=0
$$

对一切 $\theta>0$ 成立; 但 $\psi\left(T\right)$ 不恒为零 (样本的最小值与最大值不必满足 $\left(n+2\right)X_{(n)}=\left(2n+1\right)X_{(1)}$). 由**定义 2.6.1 (完备统计量)**, $T$ 不是完备统计量.

$\blacksquare$

## 习题 3.2-3 (六种总体的矩估计)

设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, 且 $X$ 的密度函数 $f(x)$ 如下所示, 求其中未知参数的矩估计.

(1) $f\left(x,\theta\right)=\left(\theta+1\right)x^{\theta}$ ($0<x<1$), $f=0$ (其他), $\theta>-1$;

(2) $f\left(x,\theta\right)=\theta\exp\left\{-\theta x\right\}$ ($x>0$), $f=0$ ($x\le0$), $\theta>0$;

(3) $f\left(x,\theta\right)=\frac{1}{2\theta}\exp\left\{-\frac{\left|x\right|}{\theta}\right\}$, $-\infty<x<+\infty$, $\theta>0$;

(4) $f\left(x,\theta\right)=1$ ($\theta-0.5\le x\le\theta+0.5$), $f=0$ (其他), $\theta\in\mathbb{R}$;

(5) $f\left(x,\mu,\sigma^{2}\right)=\frac{1}{\sqrt{2\pi}\sigma x}\exp\left\{-\frac{\left(\ln x-\mu\right)^{2}}{2\sigma^{2}}\right\}$ ($x>0$), $f=0$ ($x\le0$), $\mu\in\mathbb{R}$, $\sigma>0$;

(6) $f\left(x,\mu,\lambda\right)=\lambda\exp\left\{-\lambda\left(x-\mu\right)\right\}$ ($x>\mu$), $f=0$ (其他), $\mu\in\mathbb{R}$, $\lambda>0$.

### 解答 3.2-3

各小题都按**定义 3.2.1 (矩估计)** 把总体矩写成参数的函数, 再令其等于相应的样本矩. 记 $\bar{X}=A_1$, $A_2=\frac{1}{n}\sum X_i^{2}$.

(1) $\alpha_1=\int_{0}^{1}x\left(\theta+1\right)x^{\theta}\,\mathrm{d}x=\frac{\theta+1}{\theta+2}$. 令 $\frac{\theta+1}{\theta+2}=\bar{X}$, 解出

$$
\hat{\theta}=\frac{2\bar{X}-1}{1-\bar{X}}.
$$

$\blacksquare$

(2) $\alpha_1=1/\theta$. 令 $1/\theta=\bar{X}$, 得 $\hat{\theta}=1/\bar{X}$.

$\blacksquare$

(3) 密度关于原点对称, $\alpha_1=0$ 不含参数, 故改用二阶矩: $\alpha_2=\int x^{2}\frac{1}{2\theta}\mathrm{e}^{-\left|x\right|/\theta}\,\mathrm{d}x=2\theta^{2}$. 令 $2\theta^{2}=A_2$, 得

$$
\hat{\theta}=\sqrt{\frac{A_2}{2}}=\sqrt{\frac{1}{2n}\sum_{i=1}^{n}X_i^{2}}.
$$

$\blacksquare$

(4) $\alpha_1=\theta$. 令 $\theta=\bar{X}$, 得 $\hat{\theta}=\bar{X}$.

$\blacksquare$

(5) 对数正态的一阶矩与二阶矩为 $\alpha_1=\mathrm{e}^{\mu+\sigma^{2}/2}$, $\alpha_2=\mathrm{e}^{2\mu+2\sigma^{2}}$. 取对数得方程组

$$
\ln A_1=\mu+\frac{\sigma^{2}}{2},\qquad \ln A_2=2\mu+2\sigma^{2}.
$$

第二式减去第一式的两倍, 得 $\sigma^{2}=\ln A_2-2\ln A_1$; 再由第一式 $\mu=\ln A_1-\sigma^{2}/2=2\ln A_1-\frac{1}{2}\ln A_2$. 故

$$
\hat{\sigma}^{2}=\ln\frac{A_2}{A_1^{2}},\qquad \hat{\mu}=\ln\frac{A_1^{2}}{\sqrt{A_2}}.
$$

$\blacksquare$

(6) 平移指数的均值与方差为 $\alpha_1=\mu+1/\lambda$, $\alpha_2=2/\lambda^{2}+2\mu/\lambda+\mu^{2}$, 故 $\alpha_2-\alpha_1^{2}=1/\lambda^{2}$. 令 $\alpha_1=\bar{X}$, $\alpha_2-\alpha_1^{2}=A_2-\bar{X}^{2}=\frac{1}{n}\sum\left(X_i-\bar{X}\right)^{2}$, 得

$$
\hat{\lambda}=\frac{1}{\sqrt{A_2-\bar{X}^{2}}},\qquad \hat{\mu}=\bar{X}-\sqrt{A_2-\bar{X}^{2}}.
$$

$\blacksquare$

## 习题 3.2-5 (正态总体下事件概率的矩估计)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, 求 $P\left\{X>1\right\}$ 的矩估计.

### 解答 3.2-5

由**定义 3.2.1 (矩估计)**, 正态总体的矩估计为 $\hat{\mu}=\bar{X}$, $\hat{\sigma}^{2}=A_2-\bar{X}^{2}=\frac{1}{n}\sum\left(X_i-\bar{X}\right)^{2}$, 记 $\hat{\sigma}=\sqrt{\hat{\sigma}^{2}}$.

$P\left\{X>1\right\}=1-\Phi\left(\frac{1-\mu}{\sigma}\right)$, 把参数换成估计并把 $\Phi$ 保留, 得

$$
\widehat{P\left\{X>1\right\}}=1-\Phi\left(\frac{1-\bar{X}}{\hat{\sigma}}\right),\qquad \hat{\sigma}^{2}=\frac{1}{n}\sum_{i=1}^{n}\left(X_i-\bar{X}\right)^{2}.
$$

$\blacksquare$

## 习题 3.2-7 (用分布函数族参数的矩估计)

设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, 且 $X$ 的分布函数为 $F\left(x,\theta\right)=1-x^{-\theta}$ ($x\ge1$), $F=0$ ($x<1$), 其中 $\theta>1$ 为未知参数, 求 $\theta$ 的矩估计.

### 解答 3.2-7

由分布函数求密度: $f\left(x,\theta\right)=\theta x^{-\theta-1}$ ($x\ge1$), 其余处为零. 一阶矩

$$
\alpha_1=\int_{1}^{+\infty}x\theta x^{-\theta-1}\,\mathrm{d}x=\frac{\theta}{\theta-1},
$$

这要求 $\theta>1$, 与题设一致. 令 $\frac{\theta}{\theta-1}=\bar{X}$, 解出

$$
\hat{\theta}=\frac{\bar{X}}{\bar{X}-1}.
$$

$\blacksquare$

## 习题 3.3-3 (五种总体的极大似然估计)

设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, 且 $X$ 的密度函数 $f(x)$ 如下所示, 求其中未知参数的极大似然估计.

(1) $f\left(x,\theta\right)=\left(\theta+1\right)x^{\theta}$ ($0<x<1$), $f=0$ (其他), $\theta>-1$;

(2) $f\left(x,\theta\right)=\theta\exp\left\{-\theta x\right\}$ ($x>0$), $f=0$ ($x\le0$), $\theta>0$;

(3) $f\left(x,\theta\right)=\frac{1}{2\theta}\exp\left\{-\frac{\left|x\right|}{\theta}\right\}$, $-\infty<x<+\infty$, $\theta>0$;

(4) $f\left(x,\theta\right)=1$ ($\theta-0.5\le x\le\theta+0.5$), $f=0$ (其他), $\theta\in\mathbb{R}$;

(5) $f\left(x,\mu,\sigma^{2}\right)=\frac{1}{\sqrt{2\pi}\sigma x}\exp\left\{-\frac{\left(\ln x-\mu\right)^{2}}{2\sigma^{2}}\right\}$ ($x>0$), $f=0$ ($x\le0$), $\mu\in\mathbb{R}$, $\sigma>0$.

### 解答 3.3-3

各小题都按**定义 3.3.1 (似然函数)** 写出 $L$, 再按**定义 3.3.2 (极大似然估计)** 求驻点并验证极大.

(1) $L\left(\theta\right)=\left(\theta+1\right)^{n}\prod_{i=1}^{n}x_i^{\theta}$, 对数似然为 $n\ln\left(\theta+1\right)+\theta\sum\ln x_i$. 求导并令其为零:

$$
\frac{n}{\theta+1}+\sum_{i=1}^{n}\ln x_i=0,
$$

故 $\hat{\theta}=-\frac{n}{\sum_{i=1}^{n}\ln X_i}-1$. 因 $0<x_i<1$ 时 $\ln x_i<0$, 有 $\hat{\theta}>-1$; 且二阶导数为 $-n/\left(\theta+1\right)^{2}<0$, 故是极大值点.

$\blacksquare$

(2) $L\left(\theta\right)=\theta^{n}\exp\left\{-\theta\sum x_i\right\}$, 对数似然 $n\ln\theta-\theta\sum x_i$. 求导得 $n/\theta-\sum x_i=0$, 故 $\hat{\theta}=1/\bar{X}$; 二阶导数为 $-n/\theta^{2}<0$, 是极大值点.

$\blacksquare$

(3) $L\left(\theta\right)=\left(2\theta\right)^{-n}\exp\left\{-\frac{1}{\theta}\sum\left|x_i\right|\right\}$, 对数似然 $-n\ln2-n\ln\theta-\frac{1}{\theta}\sum\left|x_i\right|$. 求导得

$$
-\frac{n}{\theta}+\frac{1}{\theta^{2}}\sum_{i=1}^{n}\left|x_i\right|=0,
$$

故 $\hat{\theta}=\frac{1}{n}\sum_{i=1}^{n}\left|X_i\right|$; 二阶导数为 $n/\theta^{2}-2\sum\left|x_i\right|/\theta^{3}$, 在驻点处等于 $-n/\theta^{2}<0$, 是极大值点.

$\blacksquare$

(4) $L\left(\theta\right)=1$ 当且仅当全部 $x_i$ 落进 $\left[\theta-0.5,\theta+0.5\right]$, 否则为零. 该条件等价于

$$
x_{(n)}-0.5\le\theta\le x_{(1)}+0.5.
$$

只要 $x_{(n)}-x_{(1)}\le1$, 此区间非空且其上 $L$ 恒等于 $1$, 已是上确界, 故极大似然估计不唯一, 可取

$$
\hat{\theta}=\frac{X_{(1)}+X_{(n)}}{2}.
$$

$\blacksquare$

(5) $L\left(\mu,\sigma^{2}\right)=\left(2\pi\sigma^{2}\right)^{-n/2}\prod_{i=1}^{n}\frac{1}{x_i}\exp\left\{-\frac{1}{2\sigma^{2}}\sum_{i=1}^{n}\left(\ln x_i-\mu\right)^{2}\right\}$. 记 $y_i=\ln x_i$, 对数似然中的参数部分与正态样本 $\left\{y_i\right\}$ 的完全相同, 故

$$
\hat{\mu}=\frac{1}{n}\sum_{i=1}^{n}\ln X_i,\qquad \hat{\sigma}^{2}=\frac{1}{n}\sum_{i=1}^{n}\left(\ln X_i-\hat{\mu}\right)^{2}.
$$

$\blacksquare$

## 习题 3.3-4 (正态总体分情形的极大似然估计)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, 其中 $\mu\in\mathbb{R}$, $\sigma>0$,

(1) 若 $\mu$ 未知, $\sigma$ 已知, 求 $\mu$ 的极大似然估计;

(2) 若 $\mu$ 已知, $\sigma$ 未知, 求 $\sigma^{2}$ 的极大似然估计.

### 解答 3.3-4

似然函数为

$$
L=\left(2\pi\sigma^{2}\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^{2}}\sum_{i=1}^{n}\left(x_i-\mu\right)^{2}\right\}.
$$

(1) $\sigma$ 已知, 只需求 $\mu$. 对数似然对 $\mu$ 求导:

$$
\frac{\mathrm{d}\ln L}{\mathrm{d}\mu}=\frac{1}{\sigma^{2}}\sum_{i=1}^{n}\left(x_i-\mu\right)=0,
$$

故 $\hat{\mu}=\bar{X}$; 二阶导数为 $-n/\sigma^{2}<0$, 是极大值点.

$\blacksquare$

(2) $\mu$ 已知, 记 $S_0=\frac{1}{n}\sum_{i=1}^{n}\left(X_i-\mu\right)^{2}$. 对 $\sigma^{2}$ 求导:

$$
\frac{\mathrm{d}\ln L}{\mathrm{d}\sigma^{2}}=-\frac{n}{2\sigma^{2}}+\frac{1}{2\sigma^{4}}\sum_{i=1}^{n}\left(x_i-\mu\right)^{2}=0,
$$

故 $\hat{\sigma}^{2}=\frac{1}{n}\sum_{i=1}^{n}\left(X_i-\mu\right)^{2}$. 在驻点处二阶导数为

$$
-\frac{n}{2\sigma^{4}}+\frac{\sum_{i=1}^{n}\left(x_i-\mu\right)^{2}}{\sigma^{6}}=\frac{n}{2\sigma^{4}}-\frac{n}{\sigma^{4}}=-\frac{n}{2\sigma^{4}}<0,
$$

故是极大值点.

$\blacksquare$
