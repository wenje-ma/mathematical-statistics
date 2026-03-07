# week2

> **定义 1.3.2 (简单随机样本)**
> 
> 设总体 $X$ 的分布为 $F$, $X_1,X_2,\ldots,X_n$ 是从 $X$ 中抽取的容量为 $n$ 的样本. 若 $X_1,X_2,\ldots,X_n$ 相互独立, 且都与总体 $X$ 同分布, 则称它们是简单随机样本, 简称样本. (教材 $\S1.3$, p7)

> **定义 1.4.1 (统计量)**
> 
> 设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, $g(X_1,X_2,\ldots,X_n)$ 是样本的函数, 且除依赖于样本外不依赖于任何其他的未知量, 则称 $g(X_1,X_2,\ldots,X_n)$ 为统计量. (教材 $\S1.4$, p12)

> **定义 1.4.2 (顺序统计量)**
> 
> 把 $X_1,X_2,\ldots,X_n$ 按从小到大的顺序排列为 $X_{(1)}\le X_{(2)}\le\cdots\le X_{(n)}$, 称 $\left(X_{(1)},X_{(2)},\ldots,X_{(n)}\right)$ 为顺序统计量. (教材 $\S1.4$, p14)

> **定义 1.5.1 (经验分布函数)**
> 
> 设 $X_{(1)}\le\cdots\le X_{(n)}$ 是样本的顺序统计量, 对任意实数 $x$, 当 $x<X_{(1)}$ 时取 $F_n(x)=0$, 当 $X_{(r)}\le x<X_{(r+1)}$, $r=1,2,\ldots,n-1$ 时取 $F_n(x)=r/n$, 当 $x\ge X_{(n)}$ 时取 $F_n(x)=1$, 称 $F_n(x)$ 为经验分布函数. (教材 $\S1.5$, p15)

> **公式 (1.5.2) (经验分布函数的示性表示)**
> 
> 记 $I_A(\cdot)$ 为集合 $A$ 的示性函数, 则 $F_n(x)=\frac{1}{n}\sum_{i=1}^{n}I_{\left(-\infty,x\right]}\left(X_i\right)$. (教材 $\S1.5$, p16)

> **例 2.1.2 (正态样本均值的抽样分布)**
> 
> 设 $X_1,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, 则 $\bar{X}=\frac{1}{n}\sum_{k=1}^{n}X_k$ 的抽样分布为 $N\left(\mu,\frac{\sigma^{2}}{n}\right)$. (教材 $\S2.1$, p21)

> **例 2.1.3 (顺序统计量的分布)**
> 
> 设总体 $X$ 的分布函数为 $F(x)$, 密度函数为 $f(x)$, 则第 $r$ 个顺序统计量的密度为 $f_{(r)}(x)=\frac{n!}{(r-1)!(n-r)!}\left[F(x)\right]^{r-1}\left[1-F(x)\right]^{n-r}f(x)$; 特别地 $f_{(1)}(x)=n\left[1-F(x)\right]^{n-1}f(x)$, $f_{(n)}(x)=n\left[F(x)\right]^{n-1}f(x)$, 且 $X_{(1)}$ 与 $X_{(n)}$ 的分布函数分别为 $1-\left[1-F(x)\right]^{n}$ 与 $\left[F(x)\right]^{n}$. (教材 $\S2.1$, p21)

## 习题 1-10 (经验分布函数的两条数字特征)

设 $F(x)$ 为总体 $X$ 的分布函数, $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, $F_n(x)$ 为其经验分布函数, 证明对任意给定实数 $x$, 有:

(1) $E\left(F_n(x)\right)=F(x)$;

(2) $D\left(F_n(x)\right)=\frac{1}{n}F(x)\left(1-F(x)\right)$.

### 解答 1-10

固定 $x$, 记 $Y_i=I_{\left(-\infty,x\right]}\left(X_i\right)$. 由**公式 (1.5.2) (经验分布函数的示性表示)**,

$$
F_n(x)=\frac{1}{n}\sum_{i=1}^{n}Y_i.
$$

$Y_i$ 只取 $0,1$ 两值, 且 $\left\{Y_i=1\right\}$ 就是 $\left\{X_i\le x\right\}$. 由**定义 1.3.2 (简单随机样本)**, 各 $X_i$ 与总体 $X$ 同分布, 故

$$
P\left\{Y_i=1\right\}=P\left\{X_i\le x\right\}=F(x),\quad P\left\{Y_i=0\right\}=1-F(x),
$$

即 $Y_i\sim B\left(1,F(x)\right)$; 又各 $X_i$ 相互独立, 故 $Y_1,\ldots,Y_n$ 相互独立. 于是

$$
E\left(Y_i\right)=F(x),\quad D\left(Y_i\right)=F(x)\left(1-F(x)\right),\quad i=1,2,\ldots,n.
$$

(1) 取期望的线性性,

$$
E\left(F_n(x)\right)=\frac{1}{n}\sum_{i=1}^{n}E\left(Y_i\right)=\frac{1}{n}\cdot nF(x)=F(x).
$$

$\blacksquare$

(2) 独立随机变量之和的方差等于方差之和,

$$
D\left(F_n(x)\right)=D\left(\frac{1}{n}\sum_{i=1}^{n}Y_i\right)=\frac{1}{n^{2}}\sum_{i=1}^{n}D\left(Y_i\right)=\frac{1}{n^{2}}\cdot nF(x)\left(1-F(x)\right)=\frac{1}{n}F(x)\left(1-F(x)\right).
$$

$\blacksquare$

## 习题 2.1-1 (泊松样本和的抽样分布)

设 $X_1,X_2,\ldots,X_n$ 是来自泊松分布总体 $P(\lambda)$ 的样本, 其分布列为

$$
P\left\{X=x\right\}=\frac{\lambda^{x}}{x!}\mathrm{e}^{-\lambda},\quad x=0,1,2,\ldots,
$$

其中 $\lambda>0$. 求 $T=\sum_{i=1}^{n}X_i$ 的抽样分布.

### 解答 2.1-1

由**定义 1.4.1 (统计量)**, $T$ 是样本的函数且不含未知量, 是统计量. 由**定义 1.3.2 (简单随机样本)**, $X_1,\ldots,X_n$ 独立同分布. 泊松变量的特征函数为

$$
\varphi_{X}(s)=E\left(\mathrm{e}^{\mathrm{i}sX}\right)=\exp\left\{\lambda\left(\mathrm{e}^{\mathrm{i}s}-1\right)\right\},
$$

这一步用 $\mathrm{e}^{\mathrm{i}sX}$ 的展开 $\sum_{x\ge0}\frac{\lambda^{x}}{x!}\mathrm{e}^{\mathrm{i}sx}\mathrm{e}^{-\lambda}=\exp\left\{\lambda\mathrm{e}^{\mathrm{i}s}\right\}\mathrm{e}^{-\lambda}$. 由独立性, 和的特征函数等于各特征函数之积,

$$
\varphi_{T}(s)=\prod_{i=1}^{n}\varphi_{X}(s)=\left[\exp\left\{\lambda\left(\mathrm{e}^{\mathrm{i}s}-1\right)\right\}\right]^{n}=\exp\left\{n\lambda\left(\mathrm{e}^{\mathrm{i}s}-1\right)\right\}.
$$

最后一式正是 $P(n\lambda)$ 的特征函数. 特征函数与分布一一对应, 故

$$
T\sim P(n\lambda),
$$

即 $\sum_{i=1}^{n}X_i$ 的抽样分布是参数为 $n\lambda$ 的泊松分布.

$\blacksquare$

## 习题 2.1-2 (正态样本和的抽样分布)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$, $\mu\in\mathbb{R}$, $\sigma^{2}>0$ 的样本, 求 $T=\sum_{i=1}^{n}X_i$ 的抽样分布.

### 解答 2.1-2

由**例 2.1.2 (正态样本均值的抽样分布)**, $\bar{X}=\frac{1}{n}T$ 的抽样分布为 $N\left(\mu,\frac{\sigma^{2}}{n}\right)$. 正态变量经线性变换仍服从正态分布: 若 $Y\sim N\left(a,b^{2}\right)$, 则 $cY\sim N\left(ca,c^{2}b^{2}\right)$. 取 $c=n$, $Y=\bar{X}$,

$$
T=n\bar{X}\sim N\left(n\mu,\ n^{2}\cdot\frac{\sigma^{2}}{n}\right)=N\left(n\mu,n\sigma^{2}\right).
$$

$\blacksquare$

## 习题 2.1-3 (二项尾和的分式恒等式)

设 $X\sim B(n,p)$, $0<p<1$, 对 $k\ge 1$, 证明:

$$
P\left\{X\ge r\right\}=\sum_{k=r}^{n}\binom{n}{k}p^{k}\left(1-p\right)^{n-k}=\frac{n!}{(r-1)!(n-r)!}\int_{0}^{p}t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t.
$$

### 解答 2.1-3

第一个等号只是把事件 $\left\{X\ge r\right\}$ 按 $X$ 的取值拆开: $X$ 取 $k$ 的概率为 $\binom{n}{k}p^{k}\left(1-p\right)^{n-k}$, 把 $k=r,r+1,\ldots,n$ 的概率相加即得, 这里用到 $X$ 取 $0,1,\ldots,n$ 之外的值概率为零.

$\blacksquare$

再证第二个等号. 记

$$
A(p)=\sum_{k=r}^{n}\binom{n}{k}p^{k}\left(1-p\right)^{n-k},\quad B(p)=\frac{n!}{(r-1)!(n-r)!}\int_{0}^{p}t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t.
$$

在 $p=0$ 处, $A(0)$ 的每一项都含因子 $p^{k}$, $k\ge r\ge1$, 故 $A(0)=0$; 积分区间退化为一点, 故 $B(0)=0$. 只需再证 $A'(p)=B'(p)$, 两者便恒等.

先算 $B'$. 由积分上限函数的求导公式,

$$
B'(p)=\frac{n!}{(r-1)!(n-r)!}p^{r-1}\left(1-p\right)^{n-r}.
$$

再算 $A'$. 逐项求导,

$$
A'(p)=\sum_{k=r}^{n}\binom{n}{k}\left[kp^{k-1}\left(1-p\right)^{n-k}-\left(n-k\right)p^{k}\left(1-p\right)^{n-k-1}\right].
$$

把求和拆成两项, 第一项用 $k\binom{n}{k}=n\binom{n-1}{k-1}$, 第二项用 $\left(n-k\right)\binom{n}{k}=n\binom{n-1}{k}$:

$$
A'(p)=n\sum_{k=r}^{n}\binom{n-1}{k-1}p^{k-1}\left(1-p\right)^{n-k}-n\sum_{k=r}^{n}\binom{n-1}{k}p^{k}\left(1-p\right)^{n-k-1}.
$$

第一项中 $k=r,\ldots,n$ 时 $k-1=r-1,\ldots,n-1$, 第二项中 $k=r,\ldots,n$ 只有 $k\le n-1$ 的项不为零. 两串的下标只在 $k=r$ 处错开一项, 其余逐项相消:

$$
A'(p)=n\binom{n-1}{r-1}p^{r-1}\left(1-p\right)^{n-r}=\frac{n!}{(r-1)!(n-r)!}p^{r-1}\left(1-p\right)^{n-r}.
$$

故 $A'(p)=B'(p)$, 且 $A(0)=B(0)$, 于是 $A(p)=B(p)$ 对 $0<p<1$ 成立.

$\blacksquare$

## 习题 2.1-5 (指数样本最小顺序统计量的分布与矩)

设 $X_1,X_2,\ldots,X_n$ 是来自指数分布总体 $E(\lambda)$ 的样本, 其密度函数为 $f(x)=\lambda\mathrm{e}^{-\lambda{}x}$ ($x>0$), $f(x)=0$ ($x\le0$), 其中 $\lambda>0$. 求:

(1) $X_{(1)}$ 的密度函数;

(2) $E\left(X_{(1)}\right)$, $D\left(X_{(1)}\right)$.

### 解答 2.1-5

指数总体的分布函数为 $F(x)=1-\mathrm{e}^{-\lambda{}x}$ ($x>0$), $F(x)=0$ ($x\le0$). $X_{(1)}$ 按**定义 1.4.2 (顺序统计量)** 是最小顺序统计量.

(1) 由**例 2.1.3 (顺序统计量的分布)** 中 $f_{(1)}$ 的公式, 当 $x>0$ 时

$$
f_{(1)}(x)=n\left[1-F(x)\right]^{n-1}f(x)=n\left(\mathrm{e}^{-\lambda{}x}\right)^{n-1}\lambda\mathrm{e}^{-\lambda{}x}=n\lambda\mathrm{e}^{-n\lambda{}x},
$$

当 $x\le0$ 时 $f(x)=0$, 故 $f_{(1)}(x)=0$. 这就是参数为 $n\lambda$ 的指数分布的密度.

$\blacksquare$

(2) 由上面的密度, $X_{(1)}\sim E(n\lambda)$, 而 $E(\lambda)$ 的均值为 $1/\lambda$, 方差为 $1/\lambda^{2}$, 故

$$
E\left(X_{(1)}\right)=\frac{1}{n\lambda},\qquad D\left(X_{(1)}\right)=\frac{1}{n^{2}\lambda^{2}}.
$$

$\blacksquare$

## 习题 2.1-6 (正态样本的两端概率)

设 $X_1,X_2,\ldots,X_9$ 是来自正态总体 $N(1,9)$ 的样本, 求:

(1) $P\left\{X_{(1)}>4\right\}$;

(2) $P\left\{X_{(9)}<4\right\}$.

### 解答 2.1-6

记 $\Phi$ 为标准正态分布函数, 则 $X_i\sim N(1,9)$ 时

$$
P\left\{X_i>4\right\}=1-\Phi\left(\frac{4-1}{3}\right)=1-\Phi(1)=0.1587,\quad P\left\{X_i<4\right\}=\Phi(1)=0.8413.
$$

(1) 事件 $\left\{X_{(1)}>4\right\}$ 等价于每个 $X_i$ 都大于 $4$. 由**定义 1.3.2 (简单随机样本)**, 各 $X_i$ 相互独立, 故概率可乘:

$$
P\left\{X_{(1)}>4\right\}=\prod_{i=1}^{9}P\left\{X_i>4\right\}=\left[1-\Phi(1)\right]^{9}=0.1587^{9}\approx 6.37\times10^{-8}.
$$

$\blacksquare$

(2) 同样, $\left\{X_{(9)}<4\right\}$ 等价于每个 $X_i$ 都小于 $4$, 故

$$
P\left\{X_{(9)}<4\right\}=\prod_{i=1}^{9}P\left\{X_i<4\right\}=\left[\Phi(1)\right]^{9}=0.8413^{9}\approx 0.2112.
$$

$\blacksquare$

## 习题 2.1-7 (均匀样本两端顺序统计量的密度)

设 $X_1,X_2,\ldots,X_n$ 是来自均匀分布总体 $U\left[\theta_1,\theta_2\right]$, $\theta_1<\theta_2$ 的样本, 分别求顺序统计量 $X_{(1)}$, $X_{(n)}$ 的密度函数.

### 解答 2.1-7

均匀总体的密度与分布函数为

$$
f(x)=\frac{1}{\theta_2-\theta_1},\qquad F(x)=\frac{x-\theta_1}{\theta_2-\theta_1},\qquad \theta_1\le x\le\theta_2,
$$

在区间外 $f(x)=0$, $F(x)$ 分别取 $0$ 与 $1$. 由**例 2.1.3 (顺序统计量的分布)**, $X_{(1)}$ 与 $X_{(n)}$ 的密度分别为

$$
f_{(1)}(x)=n\left[1-F(x)\right]^{n-1}f(x),\qquad f_{(n)}(x)=n\left[F(x)\right]^{n-1}f(x).
$$

在 $\theta_1\le x\le\theta_2$ 上把 $F$ 与 $f$ 代入. 对 $X_{(1)}$,

$$
f_{(1)}(x)=n\left(\frac{\theta_2-x}{\theta_2-\theta_1}\right)^{n-1}\frac{1}{\theta_2-\theta_1}=\frac{n\left(\theta_2-x\right)^{n-1}}{\left(\theta_2-\theta_1\right)^{n}}.
$$

$\blacksquare$

对 $X_{(n)}$,

$$
f_{(n)}(x)=n\left(\frac{x-\theta_1}{\theta_2-\theta_1}\right)^{n-1}\frac{1}{\theta_2-\theta_1}=\frac{n\left(x-\theta_1\right)^{n-1}}{\left(\theta_2-\theta_1\right)^{n}}.
$$

两者的定义域都是 $\theta_1\le x\le\theta_2$, 区间外取零.

$\blacksquare$
