# week3

> **定义 1.3.2 (简单随机样本)**
> 
> 设总体 $X$ 的分布为 $F$, $X_1,X_2,\ldots,X_n$ 是从 $X$ 中抽取的容量为 $n$ 的样本. 若 $X_1,X_2,\ldots,X_n$ 相互独立, 且都与总体 $X$ 同分布, 则称它们是简单随机样本, 简称样本. (教材 $\S1.3$, p7)

> **定义 2.2.1 (卡方分布)**
> 
> 设 $X_1,X_2,\ldots,X_n$ 独立同分布, 且 $X_1\sim N(0,1)$, 令 $\xi=X_1^{2}+X_2^{2}+\cdots+X_n^{2}$, 则称 $\xi$ 是自由度为 $n$ 的卡方变量, 其分布称为自由度为 $n$ 的卡方分布, 记作 $\xi\sim\chi^{2}(n)$, $n$ 为独立随机变量的个数. (教材 $\S2.2$, p23)

> **定理 2.2.1 (卡方分布的密度)**
> 
> 设 $\xi\sim\chi^{2}(n)$, 则 $\xi$ 的密度函数为 $f(x)=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}\mathrm{e}^{-x/2}$ ($x>0$), $f(x)=0$ ($x\le0$), 其中 $\Gamma(\alpha)=\int_{0}^{+\infty}x^{\alpha-1}\mathrm{e}^{-x}\,\mathrm{d}x$ ($\alpha>0$) 是伽马函数. (教材 $\S2.2$, p24)

> **定义 2.2.2 (t 分布)**
> 
> 设 $X\sim N(0,1)$, $Y\sim\chi^{2}(n)$, 且 $X$ 与 $Y$ 相互独立, 则称 $T=\frac{X}{\sqrt{Y/n}}$ 为自由度为 $n$ 的 t 变量, 其分布称为自由度为 $n$ 的 t 分布, 记作 $T\sim t(n)$. (教材 $\S2.2$, p29)

> **定理 2.2.2 (t 分布的密度)**
> 
> 设 $T\sim t(n)$, 则 $T$ 的密度函数为 $f(t)=\frac{\Gamma\left(\left(n+1\right)/2\right)}{\Gamma\left(n/2\right)\sqrt{n\pi}}\left(1+\frac{t^{2}}{n}\right)^{-\left(n+1\right)/2}$, $-\infty<t<+\infty$. (教材 $\S2.2$, p29)

> **定义 2.2.3 (F 分布)**
> 
> 设 $X\sim\chi^{2}(m)$, $Y\sim\chi^{2}(n)$, 且 $X$ 与 $Y$ 相互独立, 则称 $F=\frac{X/m}{Y/n}$ 为自由度为 $m$ 和 $n$ 的 F 变量, 其分布称为 F 分布, 记作 $F\sim F(m,n)$, $m$ 为第一自由度, $n$ 为第二自由度. (教材 $\S2.2$, p33)

> **定理 2.2.3 (F 分布的密度)**
> 
> 设 $F\sim F(m,n)$, 则 $F$ 的密度函数为 $f(x)=\frac{\Gamma\left(\left(m+n\right)/2\right)}{\Gamma\left(m/2\right)\Gamma\left(n/2\right)}\left(\frac{m}{n}\right)^{m/2}x^{m/2-1}\left(1+\frac{m}{n}x\right)^{-\left(m+n\right)/2}$ ($x>0$), $f(x)=0$ ($x\le0$). (教材 $\S2.2$, p33)

## 习题 2.2-1 (三个由正态样本构造的分布)

设 $X_1,X_2,X_3,X_4,X_5$ 是来自总体 $X$ 的样本, 且 $X\sim N(0,1)$.

(1) 确定 $a,b$ 使得 $a\left(X_1-2X_2+3X_3\right)^{2}+b\left(4X_4-5X_5\right)^{2}$ 服从 $\chi^{2}$ 分布, 并指出自由度;

(2) 确定 $c$ 使得 $c\sum_{i=1}^{3}X_i\left/\sqrt{\sum_{i=4}^{5}X_i^{2}}\right.$ 服从 $t$ 分布, 并指出自由度;

(3) 确定 $d$ 使得 $d\sum_{i=1}^{3}X_i^{2}\left/\sum_{i=4}^{5}X_i^{2}\right.$ 服从 $F$ 分布, 并指出自由度.

### 解答 2.2-1

各 $X_i$ 独立同分布, 都服从 $N(0,1)$. 独立正态变量的线性组合仍服从正态分布, 其均值为系数与均值之积的和, 方差为系数平方之和, 故

$$
X_1-2X_2+3X_3\sim N\left(0,\ 1+4+9\right)=N(0,14),\qquad 4X_4-5X_5\sim N\left(0,\ 16+25\right)=N(0,41).
$$

(1) 由上式, $\frac{X_1-2X_2+3X_3}{\sqrt{14}}\sim N(0,1)$, $\frac{4X_4-5X_5}{\sqrt{41}}\sim N(0,1)$. 两组变量互不涉及同一 $X_i$, 故两个标准化变量相互独立. 由**定义 2.2.1 (卡方分布)**, 取

$$
a=\frac{1}{14},\qquad b=\frac{1}{41},
$$

则两项分别是两个独立 $N(0,1)$ 变量的平方, 其和为 $\chi^{2}$ 变量, 自由度为 $2$.

$\blacksquare$

(2) 记 $U=\sum_{i=1}^{3}X_i$, $V=\sum_{i=4}^{5}X_i^{2}$. 由独立性, $U\sim N(0,3)$, 故 $U/\sqrt{3}\sim N(0,1)$. 又 $X_4,X_5$ 是 $N(0,1)$ 变量, 由**定义 2.2.1 (卡方分布)**, $V\sim\chi^{2}(2)$. $U$ 只含 $X_1,X_2,X_3$, $V$ 只含 $X_4,X_5$, 故 $U$ 与 $V$ 相互独立. 按**定义 2.2.2 (t 分布)**,

$$
\frac{U/\sqrt{3}}{\sqrt{V/2}}\sim t(2).
$$

把它写成题目中的形状:

$$
\frac{U}{\sqrt{3}}\cdot\frac{\sqrt{2}}{\sqrt{V}}=\sqrt{\frac{2}{3}}\,\frac{U}{\sqrt{V}},
$$

故 $c=\sqrt{\frac{2}{3}}$, 自由度为 $2$.

$\blacksquare$

(3) 由**定义 2.2.1 (卡方分布)**, $\sum_{i=1}^{3}X_i^{2}\sim\chi^{2}(3)$, $\sum_{i=4}^{5}X_i^{2}\sim\chi^{2}(2)$, 且两者独立. 按**定义 2.2.3 (F 分布)**,

$$
\frac{\left(\sum_{i=1}^{3}X_i^{2}\right)/3}{\left(\sum_{i=4}^{5}X_i^{2}\right)/2}\sim F(3,2).
$$

两个分母中的 $3$ 与 $2$ 移进系数, 得 $d=\frac{2}{3}$, 第一自由度为 $3$, 第二自由度为 $2$.

$\blacksquare$

## 习题 2.2-2 (卡方分布的各阶原点矩)

设随机变量 $X$ 服从自由度为 $n$ 的 $\chi^{2}$ 分布, 证明:

$$
E\left(X^{k}\right)=\frac{2^{k}\Gamma\left(n/2+k\right)}{\Gamma\left(n/2\right)},\quad k=1,2,\ldots
$$

特别地, 有 $E(X)=n$, $D(X)=2n$.

### 解答 2.2-2

由**定理 2.2.1 (卡方分布的密度)**, $X$ 的密度只在 $x>0$ 处非零, 且为 $\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}\mathrm{e}^{-x/2}$. 故

$$
E\left(X^{k}\right)=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}\int_{0}^{+\infty}x^{n/2+k-1}\mathrm{e}^{-x/2}\,\mathrm{d}x.
$$

作代换 $x=2u$, 则 $\mathrm{d}x=2\,\mathrm{d}u$, 且

$$
E\left(X^{k}\right)=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}\int_{0}^{+\infty}\left(2u\right)^{n/2+k-1}\mathrm{e}^{-u}\,2\,\mathrm{d}u=\frac{2^{k}}{\Gamma\left(n/2\right)}\int_{0}^{+\infty}u^{n/2+k-1}\mathrm{e}^{-u}\,\mathrm{d}u.
$$

最后的积分就是 $\Gamma\left(n/2+k\right)$, 故

$$
E\left(X^{k}\right)=\frac{2^{k}\Gamma\left(n/2+k\right)}{\Gamma\left(n/2\right)}.
$$

$\blacksquare$

取 $k=1$, 用 $\Gamma(\alpha+1)=\alpha\Gamma(\alpha)$:

$$
E(X)=\frac{2\Gamma\left(n/2+1\right)}{\Gamma\left(n/2\right)}=2\cdot\frac{n}{2}=n.
$$

取 $k=2$,

$$
E\left(X^{2}\right)=\frac{4\Gamma\left(n/2+2\right)}{\Gamma\left(n/2\right)}=4\left(\frac{n}{2}+1\right)\frac{n}{2}=n^{2}+2n,
$$

故 $D(X)=E\left(X^{2}\right)-\left[E(X)\right]^{2}=n^{2}+2n-n^{2}=2n$.

$\blacksquare$

## 习题 2.2-3 (概率积分变换与卡方和)

设某连续型总体 $X$ 的分布函数 $F(x)$ 是连续的严格单调递增函数, $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, 证明:

(1) $Y=F(X)\sim U(0,1)$;

(2) $U=-2\sum_{i=1}^{n}\ln Y_i\sim\chi^{2}(2n)$.

### 解答 2.2-3

(1) $F$ 严格单调递增且连续, 故其值域含于 $(0,1)$, 反函数 $F^{-1}$ 存在, 且 $F$ 连续保证 $P\left\{X=x\right\}=0$. 对 $0<y<1$,

$$
P\left\{Y\le y\right\}=P\left\{F(X)\le y\right\}=P\left\{X\le F^{-1}(y)\right\}=F\left(F^{-1}(y)\right)=y,
$$

其中第二步用了 $F$ 严格递增 (等价号可换为小于等于). 又 $P\left\{Y\le y\right\}=0$ ($y\le0$), $=1$ ($y\ge1$), 这正是 $U(0,1)$ 的分布函数.

$\blacksquare$

(2) 记 $Y_i=F\left(X_i\right)$, 由 (1) 及**定义 1.3.2 (简单随机样本)**, $Y_1,\ldots,Y_n$ 独立同分布, 都服从 $U(0,1)$. 记 $W_i=-2\ln Y_i$, 对 $t>0$,

$$
P\left\{W_i>t\right\}=P\left\{-2\ln Y_i>t\right\}=P\left\{Y_i<\mathrm{e}^{-t/2}\right\}=\mathrm{e}^{-t/2},
$$

故 $W_i$ 的分布函数为 $1-\mathrm{e}^{-t/2}$ ($t>0$), 密度为 $\frac{1}{2}\mathrm{e}^{-t/2}$. 由**定理 2.2.1 (卡方分布的密度)** 取 $n=2$, 该密度正是 $\chi^{2}(2)$ 的密度, 故 $W_i\sim\chi^{2}(2)$.

$W_1,\ldots,W_n$ 相互独立. 按**定义 2.2.1 (卡方分布)**, $\chi^{2}(2)$ 是 $2$ 个独立 $N(0,1)$ 变量的平方和, 把 $n$ 个这样的平方和再相加, 得到 $2n$ 个独立 $N(0,1)$ 变量的平方和, 故

$$
U=\sum_{i=1}^{n}W_i\sim\chi^{2}(2n).
$$

$\blacksquare$

## 习题 2.2-6 (伽马分布的性质)

设随机变量 $X$ 服从参数为 $\alpha$, $\lambda$ 的伽马分布 $Ga(\alpha,\lambda)$, $\alpha>0$, $\lambda>0$. 证明:

(1) $X$ 的特征函数为 $\varphi(t)=\left(1-\frac{\mathrm{i}t}{\lambda}\right)^{-\alpha}$;

(2) $E\left(X^{k}\right)=\frac{\Gamma\left(\alpha+k\right)}{\Gamma(\alpha)}\frac{1}{\lambda^{k}}$, 特别地, $E(X)=\frac{\alpha}{\lambda}$, $D(X)=\frac{\alpha}{\lambda^{2}}$;

(3) 如果 $X_i\sim Ga\left(\alpha_i,\lambda\right)$, $i=1,2,\ldots,n$ 且 $X_1,\ldots,X_n$ 相互独立, 则 $\sum_{i=1}^{n}X_i\sim Ga\left(\alpha_1+\alpha_2+\cdots+\alpha_n,\lambda\right)$;

(4) 若取 $\alpha=n/2$, $\lambda=1/2$, 则 $Ga\left(n/2,1/2\right)$ 是 $\chi^{2}(n)$ 分布;

(5) 若取 $\alpha=1$, 则 $Ga(1,\lambda)$ 是指数分布.

### 解答 2.2-6

本题的伽马分布取形状参数 $\alpha$ 与率参数 $\lambda$, 密度为

$$
f(x)=\frac{\lambda^{\alpha}}{\Gamma(\alpha)}x^{\alpha-1}\mathrm{e}^{-\lambda{}x}\quad\left(x>0\right),\qquad f(x)=0\quad\left(x\le0\right).
$$

(1) 由定义,

$$
\varphi(t)=E\left(\mathrm{e}^{\mathrm{i}tX}\right)=\frac{\lambda^{\alpha}}{\Gamma(\alpha)}\int_{0}^{+\infty}x^{\alpha-1}\mathrm{e}^{-\left(\lambda-\mathrm{i}t\right)x}\,\mathrm{d}x.
$$

当 $\lambda-\mathrm{i}t$ 的实部 $\lambda>0$ 时, 作代换 $u=\left(\lambda-\mathrm{i}t\right)x$ 得

$$
\int_{0}^{+\infty}x^{\alpha-1}\mathrm{e}^{-\left(\lambda-\mathrm{i}t\right)x}\,\mathrm{d}x=\frac{\Gamma(\alpha)}{\left(\lambda-\mathrm{i}t\right)^{\alpha}},
$$

故 $\varphi(t)=\lambda^{\alpha}\left(\lambda-\mathrm{i}t\right)^{-\alpha}=\left(1-\frac{\mathrm{i}t}{\lambda}\right)^{-\alpha}$.

$\blacksquare$

(2) 直接积分,

$$
E\left(X^{k}\right)=\frac{\lambda^{\alpha}}{\Gamma(\alpha)}\int_{0}^{+\infty}x^{\alpha+k-1}\mathrm{e}^{-\lambda{}x}\,\mathrm{d}x=\frac{\lambda^{\alpha}}{\Gamma(\alpha)}\cdot\frac{\Gamma\left(\alpha+k\right)}{\lambda^{\alpha+k}}=\frac{\Gamma\left(\alpha+k\right)}{\Gamma(\alpha)}\frac{1}{\lambda^{k}}.
$$

$\blacksquare$

由 $\Gamma(\alpha+1)=\alpha\Gamma(\alpha)$, $\Gamma(\alpha+2)=(\alpha+1)\alpha\Gamma(\alpha)$,

$$
E(X)=\frac{\alpha}{\lambda},\quad E\left(X^{2}\right)=\frac{\alpha\left(\alpha+1\right)}{\lambda^{2}},\quad D(X)=\frac{\alpha\left(\alpha+1\right)}{\lambda^{2}}-\frac{\alpha^{2}}{\lambda^{2}}=\frac{\alpha}{\lambda^{2}}.
$$

$\blacksquare$

(3) 各 $X_i$ 独立, 特征函数相乘, 由 (1),

$$
\varphi_{\sum X_i}(t)=\prod_{i=1}^{n}\left(1-\frac{\mathrm{i}t}{\lambda}\right)^{-\alpha_i}=\left(1-\frac{\mathrm{i}t}{\lambda}\right)^{-\left(\alpha_1+\cdots+\alpha_n\right)}.
$$

这正是 $Ga\left(\alpha_1+\cdots+\alpha_n,\lambda\right)$ 的特征函数. 特征函数与分布一一对应, 故和服从该伽马分布.

$\blacksquare$

(4) 取 $\alpha=n/2$, $\lambda=1/2$, 密度为

$$
f(x)=\frac{\left(1/2\right)^{n/2}}{\Gamma\left(n/2\right)}x^{n/2-1}\mathrm{e}^{-x/2}=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}\mathrm{e}^{-x/2},\quad x>0,
$$

与**定理 2.2.1 (卡方分布的密度)** 所给 $\chi^{2}(n)$ 的密度完全一致, 故 $Ga\left(n/2,1/2\right)$ 就是 $\chi^{2}(n)$ 分布.

$\blacksquare$

(5) 取 $\alpha=1$, 由 $\Gamma(1)=1$, 密度为 $\lambda\mathrm{e}^{-\lambda{}x}$ ($x>0$), 其余处为零, 这正是参数为 $\lambda$ 的指数分布的密度.

$\blacksquare$

## 习题 2.2-7 (卡方之比与卡方之和的独立性)

设随机变量 $X\sim\chi^{2}(m)$, $Y\sim\chi^{2}(n)$, 且 $X$ 与 $Y$ 相互独立, 证明 $U=X/Y$ 与 $V=X+Y$ 相互独立.

### 解答 2.2-7

由**定理 2.2.1 (卡方分布的密度)**, $\left(X,Y\right)$ 的联合密度为

$$
f(x,y)=\frac{1}{2^{(m+n)/2}\Gamma\left(m/2\right)\Gamma\left(n/2\right)}x^{m/2-1}y^{n/2-1}\mathrm{e}^{-(x+y)/2},\quad x>0,\ y>0.
$$

作变换 $u=x/y$, $v=x+y$, 其逆为 $x=\frac{uv}{1+u}$, $y=\frac{v}{1+u}$, 定义域为 $u>0$, $v>0$. 雅可比行列式为

$$
J=\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}=\frac{v}{\left(1+u\right)^{2}}.
$$

于是 $\left(U,V\right)$ 的联合密度为

$$
g(u,v)=f\left(\frac{uv}{1+u},\frac{v}{1+u}\right)\left|J\right|=\frac{1}{2^{(m+n)/2}\Gamma\left(m/2\right)\Gamma\left(n/2\right)}u^{m/2-1}\left(1+u\right)^{-(m+n)/2}v^{(m+n)/2-1}\mathrm{e}^{-v/2},
$$

它在 $\left(0,+\infty\right)\times\left(0,+\infty\right)$ 上分解为 $u$ 的函数与 $v$ 的函数之积. 由联合密度可分解为边缘密度之积, $U$ 与 $V$ 相互独立; 顺带读出 $V\sim\chi^{2}(m+n)$, $U$ 的密度为 $\frac{\Gamma\left(\left(m+n\right)/2\right)}{\Gamma\left(m/2\right)\Gamma\left(n/2\right)}u^{m/2-1}\left(1+u\right)^{-(m+n)/2}$.

$\blacksquare$

## 习题 2.2-8 (t 分布密度趋于标准正态密度)

以 $f_n(x)$ 表示自由度为 $n$ 的 $t$ 变量的密度函数, 证明:

$$
\lim_{n\to+\infty}f_n(x)=\frac{1}{\sqrt{2\pi}}\mathrm{e}^{-\frac{x^{2}}{2}}.
$$

### 解答 2.2-8

由**定理 2.2.2 (t 分布的密度)**, 把常数与含 $x$ 的因子分开写:

$$
f_n(x)=\frac{\Gamma\left(\frac{n+1}{2}\right)}{\Gamma\left(\frac{n}{2}\right)\sqrt{n\pi}}\left(1+\frac{x^{2}}{n}\right)^{-\frac{n+1}{2}}.
$$

先处理幂因子. 固定 $x$, 记 $a_n=\left(1+\frac{x^{2}}{n}\right)^{-\frac{n}{2}}$, $b_n=\left(1+\frac{x^{2}}{n}\right)^{-\frac{1}{2}}$. 由 $b_n\to1$; 又

$$
\ln a_n=-\frac{n}{2}\ln\left(1+\frac{x^{2}}{n}\right)\to-\frac{x^{2}}{2},
$$

因为 $\ln\left(1+s\right)=s+o(s)$, 取 $s=x^{2}/n$ 得 $\frac{n}{2}\ln\left(1+\frac{x^{2}}{n}\right)\to\frac{x^{2}}{2}$. 故幂因子的极限为 $\mathrm{e}^{-x^{2}/2}$.

再处理常数. 由 $\Gamma\left(\frac{n}{2}+\frac{1}{2}\right)\left/\Gamma\left(\frac{n}{2}\right)\right.\sim\left(\frac{n}{2}\right)^{1/2}$ (斯特林公式的直接推论), 有

$$
\frac{\Gamma\left(\frac{n+1}{2}\right)}{\Gamma\left(\frac{n}{2}\right)\sqrt{n\pi}}\sim\frac{\sqrt{n/2}}{\sqrt{n\pi}}=\frac{1}{\sqrt{2\pi}}.
$$

两因子各自的极限相乘, 得 $\lim_{n\to+\infty}f_n(x)=\frac{1}{\sqrt{2\pi}}\mathrm{e}^{-x^{2}/2}$.

$\blacksquare$

## 习题 2.2-10 (自由度 1,1 的 F 变量的中位点)

设随机变量 $X\sim F(1,1)$, 求 $P\left\{X<1\right\}$.

### 解答 2.2-10

由**定理 2.2.3 (F 分布的密度)** 取 $m=n=1$. 此时 $\Gamma(1)=1$, $\Gamma\left(1/2\right)=\sqrt{\pi}$, $\left(m/n\right)^{m/2}=1$, $m/2-1=-1/2$, 密度为

$$
f(x)=\frac{1}{\pi}x^{-1/2}\left(1+x\right)^{-1},\quad x>0.
$$

于是

$$
P\left\{X<1\right\}=\frac{1}{\pi}\int_{0}^{1}\frac{x^{-1/2}}{1+x}\,\mathrm{d}x.
$$

作代换 $x=t^{2}$, $\mathrm{d}x=2t\,\mathrm{d}t$, 上限 $t=1$:

$$
\int_{0}^{1}\frac{x^{-1/2}}{1+x}\,\mathrm{d}x=2\int_{0}^{1}\frac{1}{1+t^{2}}\,\mathrm{d}t=2\arctan1-2\arctan0=\frac{\pi}{2},
$$

故 $P\left\{X<1\right\}=\frac{1}{\pi}\cdot\frac{\pi}{2}=\frac{1}{2}$.

$\blacksquare$
