# week8

> **例 2.1.3 (顺序统计量的分布)**
> 
> 设总体 $X$ 的密度函数为 $f(x)$, 分布函数为 $F(x)$, $X_{(k)}$ 为第 $k$ 个顺序统计量, 则 $X_{(k)}$ 的密度函数为 $g_k(y)=\frac{n!}{(k-1)!(n-k)!}\left[F(y)\right]^{k-1}\left[1-F(y)\right]^{n-k}f(y)$. (教材 $\S2.1$, p21)

> **定义 2.2.1 (卡方分布)**
> 
> 设 $X_1,\ldots,X_n$ 独立同分布于 $N(0,1)$, 则称 $\sum_{i=1}^{n}X_i^{2}$ 服从自由度为 $n$ 的卡方分布, 记为 $\chi^{2}(n)$. (教材 $\S2.2$, p23)

> **定理 2.2.1 (卡方分布的密度函数)**
> 
> $\chi^{2}(n)$ 的密度函数为 $f(y)=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}y^{n/2-1}\mathrm{e}^{-y/2}$ ($y>0$), $f(y)=0$ ($y\le0$). (教材 $\S2.2$, p24)

> **定义 3.2.1 (矩估计)**
> 
> 设 $F=\left\{f(x,\theta):\theta\in\Theta\right\}$ 是参数分布族, $\theta=\left(\theta_1,\ldots,\theta_m\right)$, $X_1,\ldots,X_n$ 是样本, 总体 $k$ 阶原点矩 $\alpha_k\left(\theta_1,\ldots,\theta_m\right)$ 存在. 令 $\alpha_k\left(\theta_1,\ldots,\theta_m\right)=A_k=\frac{1}{n}\sum_{i=1}^{n}X_i^{k}$, $k=1,2,\ldots,m$, 解此方程组所得 $\theta$ 的估计称为矩估计. (教材 $\S3.2$, p73)

> **定义 3.3.1 (似然函数)**
> 
> 设总体 $X$ 的密度函数 (或分布列) 为 $f(x,\theta)$, $x_1,\ldots,x_n$ 为样本观察值, 称 $L\left(\theta\right)=\prod_{i=1}^{n}f\left(x_i,\theta\right)$ ($\theta\in\Theta$) 为样本的似然函数. (教材 $\S3.3$, p82)

> **定义 3.3.2 (极大似然估计)**
> 
> 若似然函数在 $\hat{\theta}$ 处达到极大值, 即 $L\left(\hat{\theta},x_1,\ldots,x_n\right)=\sup_{\theta\in\Theta}L\left(\theta,x_1,\ldots,x_n\right)$, 则称 $\hat{\theta}\left(x_1,\ldots,x_n\right)$ 为极大似然估计值, $\hat{\theta}\left(X_1,\ldots,X_n\right)$ 为极大似然估计量. (教材 $\S3.3$, p84)

> **定义 3.4.1 (无偏估计)**
> 
> 设 $\hat{\theta}\left(X_1,\ldots,X_n\right)$ 为 $\theta$ 的估计量, 若对任意 $\theta\in\Theta$ 都有 $E\left[\hat{\theta}\left(X_1,\ldots,X_n\right)\right]=\theta$, 则称 $\hat{\theta}$ 为 $\theta$ 的无偏估计; 对可估函数 $g(\theta)$ 同理定义 $g$ 的无偏估计. (教材 $\S3.4$, p93)

> **定义 3.4.2 (有效性)**
> 
> 设 $\hat{\theta}_1$ 与 $\hat{\theta}_2$ 是 $\theta$ 的两个无偏估计, 若对一切 $\theta\in\Theta$ 有 $D\left(\hat{\theta}_1\right)\le D\left(\hat{\theta}_2\right)$, 且不等号至少对某个 $\theta$ 成立, 则称 $\hat{\theta}_1$ 比 $\hat{\theta}_2$ 有效. (教材 $\S3.4$, p96)

> **定义 3.4.3 (相合性)**
> 
> 设 $\hat{\theta}_n=\hat{\theta}_n\left(X_1,\ldots,X_n\right)$ 为 $\theta$ 的估计量, 若 $\hat{\theta}_n$ 依概率收敛到 $\theta$, 即对任意 $\theta\in\Theta$ 及 $\varepsilon>0$ 有 $\lim_{n\to\infty}P\left\{\left|\hat{\theta}_n-\theta\right|\ge\varepsilon\right\}=0$, 则称 $\hat{\theta}_n$ 为 $\theta$ 的相合估计. (教材 $\S3.4$, p97)

> **定义 3.5.3 (一致最小方差无偏估计)**
> 
> 设 $g^{*}\left(X_1,\ldots,X_n\right)$ 为 $g(\theta)$ 的无偏估计, 若对 $g(\theta)$ 的任一无偏估计 $g\left(X_1,\ldots,X_n\right)$ 都有 $D\left[g^{*}\left(X_1,\ldots,X_n\right)\right]\le D\left[g\left(X_1,\ldots,X_n\right)\right]$, 则称 $g^{*}$ 为 $g(\theta)$ 的一致最小方差无偏估计. (教材 $\S3.5$, p102)

> **定理 3.5.1 (Lemann-Scheffe 定理)**
> 
> 设 $T\left(X\right)=T\left(X_1,\ldots,X_n\right)$ 是充分完备统计量, 若 $g\left(T\left(X\right)\right)$ 是 $g(\theta)$ 的无偏估计, 则 $g\left(T\left(X\right)\right)$ 是 $g(\theta)$ 唯一的一致最小方差无偏估计. (教材 $\S3.5$, p104)

> **推论 3.5.1 (指数族中的一致最小方差无偏估计)**
> 
> 设样本的分布为指数族自然形式 $f(x,\theta)=C(\theta)\exp\left\{\sum_{j=1}^{k}\theta_jT_j(x)\right\}h(x)$, $\theta\in\Theta^{*}$, $T\left(X\right)=\left(T_1\left(X\right),\ldots,T_k\left(X\right)\right)$. 若自然参数空间 $\Theta^{*}$ 作为 $\mathbb{R}^{k}$ 的子集有内点, 且 $h\left(T\left(X\right)\right)$ 是 $g(\theta)$ 的无偏估计, 则 $h\left(T\left(X\right)\right)$ 是 $g(\theta)$ 唯一的一致最小方差无偏估计. (教材 $\S3.5$, p105)

## 习题 3.3-6 (双参数指数分布的极大似然估计)

设 $X_1,X_2,\ldots,X_n$ 是来自双参数指数分布总体的样本, 密度函数为 $f\left(x,\mu,\lambda\right)=\lambda\exp\left\{-\lambda\left(x-\mu\right)\right\}$ ($x>\mu$), $f=0$ (其他), 其中 $-\infty<\mu<+\infty$, $\lambda>0$ 未知, 分别求 $\mu$, $\lambda$ 和 $\alpha=P\left\{X_1\ge t\right\}$ ($t>\mu$) 的极大似然估计.

### 解答 3.3-6

由**定义 3.3.1 (似然函数)**,

$$
L\left(\mu,\lambda\right)=\lambda^{n}\exp\left\{-\lambda\sum_{i=1}^{n}\left(x_i-\mu\right)\right\},\qquad \mu<x_{(1)}.
$$

(1) $\mu$. 对固定 $\lambda>0$, $L$ 在 $\left(-\infty,x_{(1)}\right)$ 上关于 $\mu$ 严格递增, 故上确界在端点处取得, 且端点不可达而 $L$ 单调, 于是按**定义 3.3.2 (极大似然估计)** 取

$$
\hat{\mu}=X_{(1)}.
$$

$\blacksquare$

(2) $\lambda$. 把 $\mu$ 换成 $\hat{\mu}$ 后, 对数似然为

$$
\ln L\left(\hat{\mu},\lambda\right)=n\ln\lambda-\lambda\sum_{i=1}^{n}\left(x_i-x_{(1)}\right),
$$

求导并令其为零得 $n/\lambda-\sum\left(x_i-x_{(1)}\right)=0$, 故

$$
\hat{\lambda}=\frac{n}{\sum_{i=1}^{n}\left(X_i-X_{(1)}\right)};
$$

此时二阶导数为 $-n/\lambda^{2}<0$, 是极大值点.

$\blacksquare$

(3) $\alpha$. 直接计算

$$
\alpha=P\left\{X_1\ge t\right\}=\int_{t}^{+\infty}\lambda\mathrm{e}^{-\lambda\left(x-\mu\right)}\,\mathrm{d}x=\mathrm{e}^{-\lambda\left(t-\mu\right)}.
$$

$\alpha$ 是 $\left(\mu,\lambda\right)$ 的函数, 由极大似然估计在函数变换下的不变性, 把 $\left(\hat{\mu},\hat{\lambda}\right)$ 代入得

$$
\hat{\alpha}=\exp\left\{-\hat{\lambda}\left(t-\hat{\mu}\right)\right\}=\exp\left\{-\frac{n\left(t-X_{(1)}\right)}{\sum_{i=1}^{n}\left(X_i-X_{(1)}\right)}\right\}.
$$

$\blacksquare$

## 习题 3.4-1 (相邻差平方和的无偏化系数)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, 求 $c$ 使得 $c\sum_{i=1}^{n-1}\left(X_{i+1}-X_i\right)^{2}$ 是 $\sigma^{2}$ 的无偏估计.

### 解答 3.4-1

由 $X_i$ 相互独立同分布, $D\left(X_{i+1}-X_i\right)=D\left(X_{i+1}\right)+D\left(X_i\right)=2\sigma^{2}$, 且 $E\left(X_{i+1}-X_i\right)=0$, 故

$$
E\left[\left(X_{i+1}-X_i\right)^{2}\right]=D\left(X_{i+1}-X_i\right)=2\sigma^{2}.
$$

于是

$$
E\left[c\sum_{i=1}^{n-1}\left(X_{i+1}-X_i\right)^{2}\right]=2c\left(n-1\right)\sigma^{2}.
$$

按**定义 3.4.1 (无偏估计)**, 要求此式对一切 $\sigma^{2}$ 等于 $\sigma^{2}$, 故

$$
c=\frac{1}{2\left(n-1\right)}.
$$

$\blacksquare$

## 习题 3.4-5 (平移指数总体的矩估计与极大似然估计的无偏性)

设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, 且 $X$ 的密度函数为 $f\left(x,\theta\right)=\exp\left\{-\left(x-\theta\right)\right\}$ ($x>\theta$), $f=0$ (其他).

(1) 求参数 $\theta$ 的矩估计 $\hat{\theta}_1$, 并判断 $\hat{\theta}_1$ 是否是 $\theta$ 的无偏估计;

(2) 求参数 $\theta$ 的极大似然估计 $\hat{\theta}_2$, 并判断 $\hat{\theta}_2$ 是否是 $\theta$ 的无偏估计.

### 解答 3.4-5

(1) 一阶矩为

$$
\alpha_1=\int_{\theta}^{+\infty}x\mathrm{e}^{-\left(x-\theta\right)}\,\mathrm{d}x=\theta+1.
$$

按**定义 3.2.1 (矩估计)**, 令 $\theta+1=\bar{X}$, 得 $\hat{\theta}_1=\bar{X}-1$, 且

$$
E\left(\hat{\theta}_1\right)=E\left(\bar{X}\right)-1=\theta+1-1=\theta,
$$

由**定义 3.4.1 (无偏估计)**, $\hat{\theta}_1$ 是 $\theta$ 的无偏估计.

$\blacksquare$

(2) 似然函数为 $L\left(\theta\right)=\exp\left\{-\sum_{i=1}^{n}\left(x_i-\theta\right)\right\}$ ($\theta<x_{(1)}$), 它关于 $\theta$ 严格递增, 故按**定义 3.3.2 (极大似然估计)** 得 $\hat{\theta}_2=X_{(1)}$.

由**例 2.1.3 (顺序统计量的分布)**, $n$ 个独立同分布样本的最小值的分布为

$$
P\left\{X_{(1)}>y\right\}=\left[P\left\{X_1>y\right\}\right]^{n}=\mathrm{e}^{-n\left(y-\theta\right)},\qquad y>\theta,
$$

即 $X_{(1)}-\theta\sim E(n)$, 故

$$
E\left(\hat{\theta}_2\right)=E\left(X_{(1)}\right)=\theta+\frac{1}{n}\ne\theta.
$$

由**定义 3.4.1 (无偏估计)**, $\hat{\theta}_2$ 不是 $\theta$ 的无偏估计, 其偏倚为 $1/n$ (估计偏高).

$\blacksquare$

## 习题 3.4-7 (帕累托型总体两个无偏估计的有效性比较)

设 $X_1,X_2$ 是来自总体 $X$ 的样本, 且 $X$ 的密度函数为 $f\left(x,\theta\right)=k\theta^{k}x^{-(k+1)}$ ($x>\theta$), $f=0$ (其他), $k>2$, $\theta>0$ 为未知参数.

(1) 证明 $T_1=\frac{k-1}{2k}\left(X_1+X_2\right)$ 和 $T_2=\frac{2k-1}{2k}\min\left\{X_1,X_2\right\}$ 都是 $\theta$ 的无偏估计;

(2) 指出 $T_1$ 和 $T_2$ 哪一个有效.

### 解答 3.4-7

先算总体矩:

$$
E\left(X\right)=k\theta^{k}\int_{\theta}^{+\infty}x^{-k}\,\mathrm{d}x=\frac{k}{k-1}\theta,
$$

$$
E\left(X^{2}\right)=k\theta^{k}\int_{\theta}^{+\infty}x^{-k+1}\,\mathrm{d}x=\frac{k}{k-2}\theta^{2},
$$

$$
D\left(X\right)=\frac{k}{k-2}\theta^{2}-\frac{k^{2}}{\left(k-1\right)^{2}}\theta^{2}=\frac{k\theta^{2}}{\left(k-2\right)\left(k-1\right)^{2}}.
$$

(1) $E\left(T_1\right)=\frac{k-1}{2k}\cdot\frac{2k}{k-1}\theta=\theta$.

由**例 2.1.3 (顺序统计量的分布)** 的思路, $P\left\{X>y\right\}=\left(\theta/y\right)^{k}$, 故

$$
P\left\{\min\left\{X_1,X_2\right\}>y\right\}=\left(\frac{\theta}{y}\right)^{2k},
$$

即 $\min\left\{X_1,X_2\right\}$ 服从参数为 $2k$ 的同类分布, 于是 $E\left[\min\right]=\frac{2k}{2k-1}\theta$, $E\left(T_2\right)=\theta$. 由**定义 3.4.1 (无偏估计)**, 二者都是无偏估计.

$\blacksquare$

(2) 由独立性,

$$
D\left(T_1\right)=\left(\frac{k-1}{2k}\right)^{2}\cdot2\cdot\frac{k\theta^{2}}{\left(k-2\right)\left(k-1\right)^{2}}=\frac{k\theta^{2}}{2\left(k-2\right)\left(k-1\right)^{2}}.
$$

再把 $k$ 换成 $2k$ 代入同型方差公式, 得 $D\left[\min\right]=\frac{2k\theta^{2}}{\left(2k-2\right)\left(2k-1\right)^{2}}=\frac{k\theta^{2}}{\left(k-1\right)\left(2k-1\right)^{2}}$, 故

$$
D\left(T_2\right)=\left(\frac{2k-1}{2k}\right)^{2}\frac{k\theta^{2}}{\left(k-1\right)\left(2k-1\right)^{2}}=\frac{\theta^{2}}{4k\left(k-1\right)}.
$$

两方差之比为

$$
\frac{D\left(T_2\right)}{D\left(T_1\right)}=\frac{\left(k-2\right)\left(k-1\right)}{2k^{2}}=\frac{k^{2}-3k+2}{2k^{2}}<1,
$$

最后一式等价于 $k^{2}+3k-2>0$, 对 $k>2$ 成立. 故 $D\left(T_2\right)<D\left(T_1\right)$, 由**定义 3.4.2 (有效性)**, $T_2=\frac{2k-1}{2k}\min\left\{X_1,X_2\right\}$ 比 $T_1$ 有效.

$\blacksquare$

## 习题 3.4-10 (期望与方差趋于极限时估计的相合性)

设 $\hat{\theta}_n$ 是 $\theta$ 的估计量, 证明: 若 $n\to+\infty$ 时 $E\left(\hat{\theta}_n\right)\to\theta$, $D\left(\hat{\theta}_n\right)\to0$, 则 $\hat{\theta}_n$ 是 $\theta$ 的相合估计.

### 解答 3.4-10

对任意 $\varepsilon>0$, 由切比雪夫不等式,

$$
P\left\{\left|\hat{\theta}_n-\theta\right|\ge\varepsilon\right\}\le\frac{E\left[\left(\hat{\theta}_n-\theta\right)^{2}\right]}{\varepsilon^{2}}.
$$

而

$$
E\left[\left(\hat{\theta}_n-\theta\right)^{2}\right]=D\left(\hat{\theta}_n\right)+\left[E\left(\hat{\theta}_n\right)-\theta\right]^{2}.
$$

由假设, 后一式右边两项都趋于零, 故 $E\left[\left(\hat{\theta}_n-\theta\right)^{2}\right]\to0$, 从而

$$
\lim_{n\to\infty}P\left\{\left|\hat{\theta}_n-\theta\right|\ge\varepsilon\right\}=0.
$$

按**定义 3.4.3 (相合性)**, $\hat{\theta}_n$ 是 $\theta$ 的相合估计.

$\blacksquare$

## 习题 3.4-12 (均匀总体样本几何平均的相合性)

设 $X_1,X_2,\ldots,X_n$ 是来自均匀分布 $U\left[0,\theta\right]$, $\theta>0$ 的样本, 证明 $\sqrt[n]{X_1X_2\cdots X_n}$ 为 $\theta/\mathrm{e}$ 的相合估计.

### 解答 3.4-12

记 $Y_i=\ln X_i$. 因 $X_i/\theta\sim U\left[0,1\right]$, 可写 $Y_i=\ln\theta+\ln U_i$, 其中 $U_i\sim U\left[0,1\right]$, 且

$$
E\left(\ln U_1\right)=\int_{0}^{1}\ln u\,\mathrm{d}u=-1,\qquad E\left[\left(\ln U_1\right)^{2}\right]=\int_{0}^{1}\left(\ln u\right)^{2}\mathrm{d}u=2,
$$

故 $E\left(Y_1\right)=\ln\theta-1$, $D\left(Y_1\right)=2-1=1$. 于是

$$
E\left(\frac{1}{n}\sum_{i=1}^{n}Y_i\right)=\ln\theta-1,\qquad D\left(\frac{1}{n}\sum_{i=1}^{n}Y_i\right)=\frac{1}{n}\to0.
$$

由切比雪夫不等式, 对任意 $\varepsilon>0$,

$$
P\left\{\left|\frac{1}{n}\sum_{i=1}^{n}Y_i-\left(\ln\theta-1\right)\right|\ge\varepsilon\right\}\le\frac{1}{n\varepsilon^{2}}\to0,
$$

即 $\frac{1}{n}\sum Y_i$ 依概率收敛到 $\ln\theta-1$. 再由指数函数的连续性,

$$
\sqrt[n]{X_1X_2\cdots X_n}=\exp\left\{\frac{1}{n}\sum_{i=1}^{n}Y_i\right\}\xrightarrow{P}\mathrm{e}^{\ln\theta-1}=\frac{\theta}{\mathrm{e}}.
$$

按**定义 3.4.3 (相合性)**, 结论成立.

$\blacksquare$

## 习题 3.5-4 (两点分布中 $p^{m}$ 与 $p\left(1-p\right)$ 的一致最小方差无偏估计)

设 $X_1,X_2,\ldots,X_n$ 是来自两点分布总体 $B(1,p)$ 的样本, $0<p<1$ 为未知参数.

(1) 求 $p^{m}$ 的一致最小方差无偏估计, 其中 $m>0$ 为自然数;

(2) 求 $p\left(1-p\right)$ 的一致最小方差无偏估计.

### 解答 3.5-4

样本的联合分布列为

$$
f\left(x_1,\ldots,x_n,p\right)=p^{\sum x_i}\left(1-p\right)^{n-\sum x_i}=C(p)\exp\left\{\theta T(x)\right\},\qquad \theta=\ln\frac{p}{1-p},\quad T=\sum_{i=1}^{n}x_i,
$$

自然参数空间为 $\mathbb{R}$, 有内点. 由**推论 3.5.1 (指数族中的一致最小方差无偏估计)**, $T=\sum_{i=1}^{n}X_i$ 是充分完备统计量.

(1) 记 $\left(T\right)_m=T\left(T-1\right)\cdots\left(T-m+1\right)$ (当 $T<m$ 时取零), $\left(n\right)_m=n\left(n-1\right)\cdots\left(n-m+1\right)$. 把 $\left(T\right)_m$ 按"从 $n$ 个下标中取 $m$ 个互不相同的下标"展开,

$$
\left(T\right)_m=\sum_{\left(i_1,\ldots,i_m\right)\text{互不相同}}\prod_{j=1}^{m}X_{i_j},
$$

共 $\left(n\right)_m$ 项, 每项的期望为 $p^{m}$, 故

$$
E\left[\left(T\right)_m\right]=\left(n\right)_m p^{m},\qquad E\left[\frac{\left(T\right)_m}{\left(n\right)_m}\right]=p^{m}.
$$

于是 $p^{m}$ 的无偏估计为

$$
\widehat{p^{m}}=\frac{T\left(T-1\right)\cdots\left(T-m+1\right)}{n\left(n-1\right)\cdots\left(n-m+1\right)}.
$$

它是充分完备统计量 $T$ 的函数, 由**定理 3.5.1 (Lemann-Scheffe 定理)**, 它是 $p^{m}$ 唯一的一致最小方差无偏估计.

$\blacksquare$

(2) $p\left(1-p\right)=p-p^{2}$. 在 (1) 中取 $m=1$ 得 $\hat{p}=T/n$, 取 $m=2$ 得 $\widehat{p^{2}}=\frac{T\left(T-1\right)}{n\left(n-1\right)}$, 故由无偏估计的线性性,

$$
\widehat{p\left(1-p\right)}=\frac{T}{n}-\frac{T\left(T-1\right)}{n\left(n-1\right)}
$$

是 $p\left(1-p\right)$ 的无偏估计, 且它是 $T$ 的函数, 由**定理 3.5.1 (Lemann-Scheffe 定理)**, 它就是 $p\left(1-p\right)$ 唯一的一致最小方差无偏估计.

$\blacksquare$

## 习题 3.5-6 (正态零均值总体中 $\sigma$ 与 $\sigma^{4}$ 的一致最小方差无偏估计)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(0,\sigma^{2}\right)$ 的样本, $\sigma>0$ 为未知参数, 分别求 $\sigma$ 和 $\sigma^{4}$ 的一致最小方差无偏估计.

### 解答 3.5-6

联合密度为

$$
f\left(x_1,\ldots,x_n,\sigma^{2}\right)=\left(2\pi\sigma^{2}\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^{2}}\sum_{i=1}^{n}x_i^{2}\right\},
$$

以 $\theta=-1/\left(2\sigma^{2}\right)$ 为自然参数, 自然参数空间为 $\left(-\infty,0\right)$, 有内点. 记 $T=\sum_{i=1}^{n}X_i^{2}$. 由**推论 3.5.1 (指数族中的一致最小方差无偏估计)**, $T$ 是充分完备统计量, 且 $T/\sigma^{2}\sim\chi^{2}(n)$ (见**定义 2.2.1 (卡方分布)**).

(1) $\sigma$. 记 $c_n=E\sqrt{\chi^{2}(n)}=\sqrt{2}\,\Gamma\left(\frac{n+1}{2}\right)/\Gamma\left(\frac{n}{2}\right)$ (由**定理 2.2.1 (卡方分布的密度函数)** 的密度直接积分可得), 则

$$
E\left(\sqrt{T}\right)=\sigma c_n,
$$

故 $\hat{\sigma}=\sqrt{T}/c_n$ 是 $\sigma$ 的无偏估计, 它是 $T$ 的函数, 由**定理 3.5.1 (Lemann-Scheffe 定理)**, 它是 $\sigma$ 唯一的一致最小方差无偏估计.

$\blacksquare$

(2) $\sigma^{4}$. 由 $\chi^{2}(n)$ 的矩,

$$
E\left(T^{2}\right)=\sigma^{4}E\left[\left(\chi^{2}(n)\right)^{2}\right]=\sigma^{4}\left(n^{2}+2n\right)=n\left(n+2\right)\sigma^{4},
$$

故

$$
\widehat{\sigma^{4}}=\frac{T^{2}}{n\left(n+2\right)}=\frac{\left(\sum_{i=1}^{n}X_i^{2}\right)^{2}}{n\left(n+2\right)}
$$

是 $\sigma^{4}$ 的无偏估计, 它也是 $T$ 的函数, 由**定理 3.5.1 (Lemann-Scheffe 定理)**, 它是 $\sigma^{4}$ 唯一的一致最小方差无偏估计.

$\blacksquare$
