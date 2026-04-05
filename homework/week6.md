# week6

> **定义 1.3.2 (简单随机样本)**
> 
> 设总体 $X$ 的分布为 $F$, $X_1,X_2,\ldots,X_n$ 是从 $X$ 中抽取的容量为 $n$ 的样本. 若 $X_1,X_2,\ldots,X_n$ 相互独立, 且都与总体 $X$ 同分布, 则称它们是简单随机样本, 简称样本. (教材 $\S1.3$, p7)

> **定义 2.4.1 (指数族)**
> 
> 设 $F=\left\{f(x,\theta):\theta\in\Theta\right\}$ 是样本空间 $\mathcal{X}$ 上的分布族, 其中 $f(x,\theta)=C(\theta)\exp\left\{\sum_{i=1}^{k}Q_i(\theta)T_i(x)\right\}h(x)$, $C(\theta)>0$, $h(x)>0$, 且支撑集 $\left\{x:f(x,\theta)>0\right\}$ 与 $\theta$ 无关, 则称此分布族为指数型分布族, 简称指数族. (教材 $\S2.4$, p54)

> **定义 2.4.2 (指数族的自然形式)**
> 
> 若指数族可写为 $f(x,\varphi)=C(\varphi)\exp\left\{\sum_{i=1}^{k}\varphi_iT_i(x)\right\}h(x)$, 则称其为指数族的自然形式, 集合 $\Theta^{*}=\left\{\varphi:\int_{\mathcal{X}}\exp\left\{\sum_{i=1}^{k}\varphi_iT_i(x)\right\}h(x)\,\mathrm{d}x<+\infty\right\}$ 称为自然参数空间. (教材 $\S2.4$, p57)

> **定义 2.5.1 (充分统计量)**
> 
> 设样本 $X_1,\ldots,X_n$ 的分布族为 $\left\{f\left(x_1,\ldots,x_n,\theta\right):\theta\in\Theta\right\}$, $T=T\left(X_1,\ldots,X_n\right)$ 为统计量. 若在给定 $T$ 的条件下样本的条件分布与参数 $\theta$ 无关, 则称 $T$ 为参数 $\theta$ 的充分统计量. (教材 $\S2.5$, p60)

> **定理 2.5.1 (因子分解定理)**
> 
> 设样本的联合密度 (或联合分布列) 为 $f\left(x_1,\ldots,x_n,\theta\right)$, $T=T\left(X_1,\ldots,X_n\right)$ 是统计量, 则 $T$ 为充分统计量的充要条件是 $f\left(x_1,\ldots,x_n,\theta\right)=g\left(t\left(x_1,\ldots,x_n\right),\theta\right)h\left(x_1,\ldots,x_n\right)$, 其中 $h$ 不依赖于 $\theta$. (教材 $\S2.5$, p63)

> **定义 2.6.1 (完备统计量)**
> 
> 设分布族为 $\left\{f(x,\theta):\theta\in\Theta\right\}$, $T=T\left(X_1,\ldots,X_n\right)$ 为统计量. 若对任何满足 $E_{\theta}\left[\varphi\left(T\left(X_1,\ldots,X_n\right)\right)\right]=0$ (对一切 $\theta\in\Theta$) 的函数 $\varphi$, 都有 $P_{\theta}\left\{\varphi\left(T\left(X_1,\ldots,X_n\right)\right)=0\right\}=1$ 对一切 $\theta\in\Theta$, 则称 $T$ 为完备统计量. (教材 $\S2.6$, p67)

> **定理 2.6.1 (指数族中统计量的完备性)**
> 
> 设 $X_1,\ldots,X_n$ 是从自然形式为 $f(x,\theta)=C(\theta)\exp\left\{\sum_{i=1}^{k}\theta_iT_i(x)\right\}h(x)$ 的指数族中抽取的样本, $\theta\in\Theta^{*}$, 若自然参数空间 $\Theta^{*}$ 有内点, 则 $\left(T_1,\ldots,T_k\right)$ 为完备统计量. (教材 $\S2.6$, p68)

## 习题 2.4-7 (对数正态总体的样本分布族)

设 $X_1,X_2,\ldots,X_n$ 是来自对数正态分布的样本, 其密度函数为

$$
f\left(x,\mu,\sigma^{2}\right)=\frac{1}{\sqrt{2\pi}\sigma x}\exp\left\{-\frac{\left(\ln x-\mu\right)^{2}}{2\sigma^{2}}\right\},\quad x>0,
$$

其中 $\mu\in\mathbb{R}$, $\sigma>0$, $f=0$ (其他). 证明样本分布族是指数族, 并表成指数族的自然形式, 求出自然参数空间.

### 解答 2.4-7

把指数中的平方展开:

$$
-\frac{\left(\ln x-\mu\right)^{2}}{2\sigma^{2}}=-\frac{\left(\ln x\right)^{2}}{2\sigma^{2}}+\frac{\mu}{\sigma^{2}}\ln x-\frac{\mu^{2}}{2\sigma^{2}}.
$$

单个密度于是写成

$$
f\left(x,\mu,\sigma^{2}\right)=\frac{1}{\sqrt{2\pi}\sigma}\mathrm{e}^{-\frac{\mu^{2}}{2\sigma^{2}}}\cdot\frac{1}{x}\cdot\exp\left\{\frac{\mu}{\sigma^{2}}\ln x-\frac{1}{2\sigma^{2}}\left(\ln x\right)^{2}\right\},
$$

支撑集 $\left(0,+\infty\right)$ 与参数无关. 联合密度为各边缘之积,

$$
f\left(x_1,\ldots,x_n,\mu,\sigma^{2}\right)=\left(2\pi\right)^{-n/2}\sigma^{-n}\mathrm{e}^{-\frac{n\mu^{2}}{2\sigma^{2}}}\prod_{i=1}^{n}\frac{1}{x_i}\exp\left\{\frac{\mu}{\sigma^{2}}\sum_{i=1}^{n}\ln x_i-\frac{1}{2\sigma^{2}}\sum_{i=1}^{n}\left(\ln x_i\right)^{2}\right\}.
$$

由**定义 2.4.1 (指数族)**, 取 $Q_1=\mu/\sigma^{2}$, $T_1=\sum\ln x_i$, $Q_2=-1/\left(2\sigma^{2}\right)$, $T_2=\sum\left(\ln x_i\right)^{2}$, $h(x)=\prod x_i^{-1}$, 即知样本分布族是指数族.

自然形式取

$$
\varphi_1=\frac{\mu}{\sigma^{2}},\qquad \varphi_2=-\frac{1}{2\sigma^{2}},
$$

则 $\sigma^{2}=-1/\left(2\varphi_2\right)$, $\mu=\varphi_1\sigma^{2}=-\varphi_1/\left(2\varphi_2\right)$, 故

$$
f\left(x,\varphi\right)=C(\varphi)\prod_{i=1}^{n}\frac{1}{x_i}\exp\left\{\varphi_1\sum_{i=1}^{n}\ln x_i+\varphi_2\sum_{i=1}^{n}\left(\ln x_i\right)^{2}\right\},
$$

$$
C(\varphi)=\left(2\pi\right)^{-n/2}\left(-\frac{1}{2\varphi_2}\right)^{-n/2}\exp\left\{\frac{n\varphi_1^{2}}{4\varphi_2}\right\}.
$$

按**定义 2.4.2 (指数族的自然形式)**, $x>0$ 上积分有限与 $\varphi$ 的取值无关, 而原参数范围 $\mu\in\mathbb{R}$, $\sigma>0$ 对应 $\varphi_1\in\mathbb{R}$, $\varphi_2<0$, 故自然参数空间为

$$
\Theta^{*}=\left\{\left(\varphi_1,\varphi_2\right):\varphi_1\in\mathbb{R},\ \varphi_2<0\right\}.
$$

$\blacksquare$

## 习题 2.5-1 (泊松总体和的充分性)

设 $X_1,X_2,\ldots,X_n$ 是来自泊松分布总体 $P(\lambda)$, $\lambda>0$ 的样本,

(1) 分别用定义法和因子分解定理法证明 $\sum X_i$ 为充分统计量;

(2) 若 $n=2$, 则 $X_1+2X_2$ 不是充分统计量.

### 解答 2.5-1

(1) 联合分布列为

$$
P\left\{X_1=x_1,\ldots,X_n=x_n\right\}=\mathrm{e}^{-n\lambda}\frac{\lambda^{\sum x_i}}{\prod_{i=1}^{n}x_i!}.
$$

定义法. 记 $T=\sum X_i$, 由泊松分布的可加性 (逐项卷积即得), $T\sim P(n\lambda)$, 故

$$
P\left\{T=t\right\}=\mathrm{e}^{-n\lambda}\frac{\left(n\lambda\right)^{t}}{t!}.
$$

给定 $T=t$ 后, 条件概率

$$
P\left\{X_1=x_1,\ldots,X_n=x_n\mid T=t\right\}=\frac{\mathrm{e}^{-n\lambda}\lambda^{t}\left/\prod x_i!\right.}{\mathrm{e}^{-n\lambda}\left(n\lambda\right)^{t}/t!}=\frac{t!}{n^{t}\prod_{i=1}^{n}x_i!},
$$

其中 $\sum x_i=t$. 该式与 $\lambda$ 无关, 按**定义 2.5.1 (充分统计量)**, $T$ 是充分统计量.

$\blacksquare$

因子分解法. 把联合分布列拆成

$$
\mathrm{e}^{-n\lambda}\frac{\lambda^{\sum x_i}}{\prod x_i!}=g\left(t,\lambda\right)h(x),\qquad g\left(t,\lambda\right)=\mathrm{e}^{-n\lambda}\lambda^{t},\quad h(x)=\frac{1}{\prod_{i=1}^{n}x_i!},
$$

$h$ 不含 $\lambda$. 由**定理 2.5.1 (因子分解定理)**, $T=\sum X_i$ 是充分统计量.

$\blacksquare$

(2) 取 $n=2$, $T=X_1+2X_2$. 考察 $T=2$ 的两个样本点 $\left(2,0\right)$ 与 $\left(0,1\right)$:

$$
P\left\{X_1=2,X_2=0\right\}=\mathrm{e}^{-2\lambda}\frac{\lambda^{2}}{2},\qquad P\left\{X_1=0,X_2=1\right\}=\mathrm{e}^{-2\lambda}\lambda.
$$

故 $P\left\{T=2\right\}=\mathrm{e}^{-2\lambda}\left(\frac{\lambda^{2}}{2}+\lambda\right)$, 两个条件概率为

$$
P\left\{\left(2,0\right)\mid T=2\right\}=\frac{\lambda}{\lambda+2},\qquad P\left\{\left(0,1\right)\mid T=2\right\}=\frac{2}{\lambda+2},
$$

比值随 $\lambda$ 改变. 条件分布依赖参数, 按**定义 2.5.1 (充分统计量)**, $X_1+2X_2$ 不是充分统计量.

$\blacksquare$

## 习题 2.5-5 (瑞利总体的充分统计量)

设 $X_1,X_2,\ldots,X_n$ 是来自瑞利分布的样本, 其密度函数为 $f(x)=2\theta x\mathrm{e}^{-\theta x^{2}}$ ($x>0$), $f(x)=0$ (其他). 试给出一个充分统计量.

### 解答 2.5-5

联合密度为各边缘之积,

$$
f\left(x_1,\ldots,x_n,\theta\right)=\left(2\theta\right)^{n}\prod_{i=1}^{n}x_i\exp\left\{-\theta\sum_{i=1}^{n}x_i^{2}\right\}=g\left(t,\theta\right)h(x),
$$

其中 $t=\sum x_i^{2}$, $g\left(t,\theta\right)=\left(2\theta\right)^{n}\mathrm{e}^{-\theta t}$, $h(x)=\prod x_i$ 不含 $\theta$. 由**定理 2.5.1 (因子分解定理)**, $T=\sum_{i=1}^{n}X_i^{2}$ 是充分统计量.

$\blacksquare$

## 习题 2.5-6 (指数总体和的充分性)

设 $X_1,X_2,\ldots,X_n$ 是来自指数分布 $E(\lambda)$ 的样本, 其密度函数为 $f(x)=\lambda\mathrm{e}^{-\lambda{}x}$ ($x>0$), $f(x)=0$ (其他). 证明 $\sum_{i=1}^{n}X_i$ 是充分统计量.

### 解答 2.5-6

联合密度为

$$
f\left(x_1,\ldots,x_n,\lambda\right)=\lambda^{n}\exp\left\{-\lambda\sum_{i=1}^{n}x_i\right\}.
$$

取 $t=\sum x_i$, $g\left(t,\lambda\right)=\lambda^{n}\mathrm{e}^{-\lambda t}$, $h(x)=1$. $h$ 不含 $\lambda$, 由**定理 2.5.1 (因子分解定理)**, $T=\sum_{i=1}^{n}X_i$ 是充分统计量.

$\blacksquare$

## 习题 2.5-7 (正态总体按已知参数分情况的充分统计量)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本.

(1) 在 $\mu$ 已知时, 给出 $\sigma^{2}$ 的一个充分统计量;

(2) 在 $\sigma^{2}$ 已知时, 给出 $\mu$ 的一个充分统计量.

### 解答 2.5-7

联合密度为

$$
f\left(x_1,\ldots,x_n,\mu,\sigma^{2}\right)=\left(2\pi\sigma^{2}\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^{2}}\sum_{i=1}^{n}\left(x_i-\mu\right)^{2}\right\}.
$$

(1) 取 $t=\sum\left(x_i-\mu\right)^{2}$. 此时 $\mu$ 是已知常数, 上式写成 $g\left(t,\sigma^{2}\right)h(x)$, 其中

$$
g\left(t,\sigma^{2}\right)=\left(2\pi\sigma^{2}\right)^{-n/2}\mathrm{e}^{-t/\left(2\sigma^{2}\right)},\quad h(x)=1,
$$

$h$ 不含 $\sigma^{2}$. 由**定理 2.5.1 (因子分解定理)**, $T=\sum_{i=1}^{n}\left(X_i-\mu\right)^{2}$ 是 $\sigma^{2}$ 的充分统计量.

$\blacksquare$

(2) 把平方展开,

$$
\sum_{i=1}^{n}\left(x_i-\mu\right)^{2}=\sum_{i=1}^{n}x_i^{2}-2\mu\sum_{i=1}^{n}x_i+n\mu^{2},
$$

此时 $\sigma^{2}$ 是已知常数, 联合密度写成

$$
\left(2\pi\sigma^{2}\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^{2}}\sum_{i=1}^{n}x_i^{2}-\frac{n\mu^{2}}{2\sigma^{2}}\right\}\exp\left\{\frac{\mu}{\sigma^{2}}\sum_{i=1}^{n}x_i\right\}.
$$

取 $t=\sum x_i$, 前一个因子归入 $h(x)$, 则 $g\left(t,\mu\right)=\exp\left\{\mu t/\sigma^{2}\right\}$ 只通过 $t$ 依赖 $\mu$, $h$ 不含 $\mu$. 由**定理 2.5.1 (因子分解定理)**, $T=\sum_{i=1}^{n}X_i$ 是 $\mu$ 的充分统计量.

$\blacksquare$

## 习题 2.6-1 (泊松总体和的完备性)

设 $X_1,X_2,\ldots,X_n$ 是来自泊松分布总体 $P(\lambda)$, $\lambda>0$ 的样本, 证明 $\sum_{i=1}^{n}X_i$ 为完备统计量.

### 解答 2.6-1

记 $T=\sum_{i=1}^{n}X_i$, 由泊松分布的可加性, $T\sim P(n\lambda)$, 即

$$
P_{\lambda}\left\{T=k\right\}=\mathrm{e}^{-n\lambda}\frac{\left(n\lambda\right)^{k}}{k!},\qquad k=0,1,2,\ldots
$$

设实函数 $\varphi$ 满足 $E_{\lambda}\left[\varphi(T)\right]=0$ 对一切 $\lambda>0$. 即

$$
\sum_{k=0}^{+\infty}\varphi(k)\mathrm{e}^{-n\lambda}\frac{\left(n\lambda\right)^{k}}{k!}=0,\qquad \lambda>0.
$$

两边乘以 $\mathrm{e}^{n\lambda}>0$, 记 $\delta=n\lambda$ 取遍 $\left(0,+\infty\right)$:

$$
\sum_{k=0}^{+\infty}\frac{\varphi(k)}{k!}\delta^{k}=0,\qquad \delta>0.
$$

左边是 $\delta$ 的幂级数, 在 $\left(0,+\infty\right)$ 上恒为零; 幂级数在非退化区间上恒为零则各项系数全为零, 故 $\varphi(k)/k!=0$, 即 $\varphi(k)=0$ 对一切 $k=0,1,2,\ldots$ 成立, 从而 $P_{\lambda}\left\{\varphi(T)=0\right\}=1$. 按**定义 2.6.1 (完备统计量)**, $T$ 是完备统计量.

$\blacksquare$

## 习题 2.6-5 (瑞利总体的完备统计量)

设 $X_1,X_2,\ldots,X_n$ 是来自瑞利分布的样本, 其密度函数为 $f(x)=2\theta x\mathrm{e}^{-\theta x^{2}}$ ($x>0$), $f(x)=0$ (其他). 试给出一个完备统计量.

### 解答 2.6-5

由**习题 2.5-5** 的分解, 样本分布族的自然形式为

$$
f\left(x_1,\ldots,x_n,\theta\right)=\left(2\theta\right)^{n}\prod_{i=1}^{n}x_i\exp\left\{-\theta\sum_{i=1}^{n}x_i^{2}\right\}.
$$

令 $\varphi=-\theta$, 即

$$
f\left(x,\varphi\right)=C(\varphi)\prod_{i=1}^{n}x_i\exp\left\{\varphi\sum_{i=1}^{n}x_i^{2}\right\},\qquad C(\varphi)=\left(-2\varphi\right)^{n},
$$

按**定义 2.4.2 (指数族的自然形式)**, 自然参数空间为 $\Theta^{*}=\left(-\infty,0\right)$, 其中每一点都是内点. 故由**定理 2.6.1 (指数族中统计量的完备性)**, $T=\sum_{i=1}^{n}X_i^{2}$ 是完备统计量.

$\blacksquare$
