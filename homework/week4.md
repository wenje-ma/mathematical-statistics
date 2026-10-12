# 作业 4

> **引理 2.3.1**（样本均值与样本方差的期望）<br>设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的一个样本，且 $E\left(X\right)=\mu$，$D\left(X\right)=\sigma^2$，$\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ 和 $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$ 分别为样本均值和样本方差，则 $$E\left(\bar X\right)=\mu,\qquad D\left(\bar X\right)=\frac{\sigma^2}{n},\qquad E\left(S^2\right)=\sigma^2.$$

> **定理 2.3.3**（正态总体样本均值与样本方差的分布）<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，$\bar X$ 和 $S^2$ 分别为样本均值和样本方差，则有：<br>(1) $\bar X\sim N\left(\mu,\sigma^2/n\right)$，即 $\frac{\bar X-\mu}{\sigma/\sqrt n}\sim N\left(0,1\right)$；<br>(2) $\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$；<br>(3) $\bar X$ 和 $S^2$ 相互独立.

> **定理 2.3.4**<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，则 $$\frac{1}{\sigma^2}\sum_{i=1}^n\left(X_i-\mu\right)^2\sim\chi^2\left(n\right).$$

> **定义 2.2.2**（$t$ 分布）<br>设随机变量 $X\sim N\left(0,1\right)$，$Y\sim\chi^2\left(n\right)$，且 $X$ 与 $Y$ 相互独立，则称 $T=\frac{X}{\sqrt{Y/n}}$ 为自由度为 $n$ 的 $t$ 变量，记作 $T\sim t\left(n\right)$.

> **定义 2.2.3**（$F$ 分布）<br>设随机变量 $X\sim\chi^2\left(m\right)$，$Y\sim\chi^2\left(n\right)$，且 $X$ 与 $Y$ 相互独立，则称 $F=\frac{X/m}{Y/n}$ 为自由度为 $m$ 和 $n$ 的 $F$ 变量，记作 $F\sim F\left(m,n\right)$.

> **$\chi^2$ 分布的性质**（可加性）<br>设 $X_1\sim\chi^2\left(n_1\right)$，$X_2\sim\chi^2\left(n_2\right)$，且 $X_1$ 与 $X_2$ 相互独立，则 $X_1+X_2\sim\chi^2\left(n_1+n_2\right)$.

> **基础知识**（中心极限定理）<br>设 $X_1,X_2,\dots,X_n$ 独立同分布，且 $E\left(X_i\right)=\mu$，$D\left(X_i\right)=\sigma^2>0$，则 $$\frac{\bar X-\mu}{\sigma/\sqrt n}\xrightarrow{L}N\left(0,1\right).$$

> **基础知识**（Slutsky 引理）<br>设随机变量序列 $X_n\xrightarrow{L}X$，$Y_n\xrightarrow{P}c$（$c$ 为常数），则 $X_n/Y_n\xrightarrow{L}X/c$（$c\ne0$）.

### 习题一

（习题 2.3-2）设 $X_1,X_2,\dots,X_n$ 是来自泊松分布总体 $P\left(\lambda\right)$，$\lambda>0$ 的样本，求 $E\left(\bar X\right)$，$D\left(\bar X\right)$，$E\left(S^2\right)$.

### 解答 习题一

总体 $X\sim P\left(\lambda\right)$，故 $E\left(X\right)=\lambda$，$D\left(X\right)=\lambda$. 由**引理 2.3.1**（样本均值与样本方差的期望），

$$
E\left(\bar X\right)=E\left(X\right)=\lambda,\qquad D\left(\bar X\right)=\frac{D\left(X\right)}{n}=\frac{\lambda}{n},\qquad E\left(S^2\right)=D\left(X\right)=\lambda.
$$

$\blacksquare$

### 习题二

（习题 2.3-4）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$，$\mu\in\mathbb R$，$\sigma^2>0$ 的样本，求 $E\left(\bar X\right)$，$D\left(\bar X\right)$，$E\left(S^2\right)$，$D\left(S^2\right)$.

### 解答 习题二

由**引理 2.3.1**（样本均值与样本方差的期望），

$$
E\left(\bar X\right)=\mu,\qquad D\left(\bar X\right)=\frac{\sigma^2}{n},\qquad E\left(S^2\right)=\sigma^2.
$$

求 $D\left(S^2\right)$. 由**定理 2.3.3**（正态总体样本均值与样本方差的分布）之结论 (2)，

$$
\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right).
$$

由**$\chi^2$ 分布的性质**，$\chi^2\left(k\right)$ 的方差为 $2k$，故

$$
D\left(\frac{\left(n-1\right)S^2}{\sigma^2}\right)=2\left(n-1\right).
$$

于是

$$
\frac{\left(n-1\right)^2}{\sigma^4}D\left(S^2\right)=2\left(n-1\right),
$$

解得

$$
D\left(S^2\right)=\frac{2\sigma^4}{n-1}.
$$

$\blacksquare$

### 习题三

（习题 2.3-5）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$，$\mu\in\mathbb R$，$\sigma^2>0$ 的样本，且 $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$，$S_n^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2$，又设 $X_{n+1}\sim N\left(\mu,\sigma^2\right)$，且 $X_{n+1}$ 与 $X_1,X_2,\dots,X_n$ 独立，求常数 $c$ 使得 $c\frac{X_{n+1}-\bar X}{S_n}$ 服从 $t$ 分布，并指出分布的自由度.

### 解答 习题三

由**定理 2.3.3**（正态总体样本均值与样本方差的分布）之结论 (1)，$\bar X\sim N\left(\mu,\sigma^2/n\right)$. 又 $X_{n+1}\sim N\left(\mu,\sigma^2\right)$ 且与 $\bar X$ 独立，由正态分布的可加性，

$$
X_{n+1}-\bar X\sim N\left(0,\sigma^2+\frac{\sigma^2}{n}\right)=N\left(0,\frac{n+1}{n}\sigma^2\right),
$$

标准化得

$$
\frac{X_{n+1}-\bar X}{\sigma\sqrt{\left(n+1\right)/n}}\sim N\left(0,1\right).
$$

另一方面，$S_n^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2$ 与无偏样本方差 $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$ 满足 $nS_n^2=\left(n-1\right)S^2$. 由**定理 2.3.3** 之结论 (2)，

$$
\frac{nS_n^2}{\sigma^2}=\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right).
$$

由**定理 2.3.3** 之结论 (3)，$\bar X$ 与 $S^2$ 相互独立，又 $X_{n+1}$ 与 $X_1,\dots,X_n$ 独立，故 $X_{n+1}-\bar X$ 与 $S_n^2$ 相互独立. 由**定义 2.2.2**（$t$ 分布），

$$
T=\frac{\frac{X_{n+1}-\bar X}{\sigma\sqrt{\left(n+1\right)/n}}}{\sqrt{\frac{nS_n^2/\sigma^2}{n-1}}}=\sqrt{\frac{n-1}{n+1}}\cdot\frac{X_{n+1}-\bar X}{S_n}\sim t\left(n-1\right).
$$

因此 $c=\sqrt{\frac{n-1}{n+1}}$，自由度为 $n-1$. $\blacksquare$

### 习题四

（习题 2.3-7）设 $X_1,X_2,\dots,X_{n+m}$ 是来自正态总体 $N\left(0,\sigma^2\right)$，$\sigma^2>0$ 的样本，求常数 $c$ 使得 $F=c\frac{\sum_{i=1}^n X_i^2}{\sum_{i=n+1}^{n+m}X_i^2}$ 服从 $F$ 分布，并指出分布的自由度.

### 解答 习题四

由**定义 2.2.1**（$\chi^2$ 分布），因 $X_i/\sigma\sim N\left(0,1\right)$ 且相互独立，故

$$
\frac{1}{\sigma^2}\sum_{i=1}^n X_i^2\sim\chi^2\left(n\right),\qquad\frac{1}{\sigma^2}\sum_{i=n+1}^{n+m}X_i^2\sim\chi^2\left(m\right).
$$

两式所依赖的样本互不重叠，故二者相互独立. 由**定义 2.2.3**（$F$ 分布），

$$
F=\frac{\left(\frac{1}{\sigma^2}\sum_{i=1}^n X_i^2\right)/n}{\left(\frac{1}{\sigma^2}\sum_{i=n+1}^{n+m}X_i^2\right)/m}=\frac{m}{n}\cdot\frac{\sum_{i=1}^n X_i^2}{\sum_{i=n+1}^{n+m}X_i^2}\sim F\left(n,m\right).
$$

因此 $c=\frac{m}{n}$，自由度为 $\left(n,m\right)$. $\blacksquare$

### 习题五

（习题 2.3-8）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$，$\mu\in\mathbb R$，$\sigma^2>0$ 的样本，求常数 $a$ 和 $b$ 使得 $a\left(\bar X-\mu\right)^2+bS^2\sim\chi^2\left(n\right)$.

### 解答 习题五

由**定理 2.3.3**（正态总体样本均值与样本方差的分布）之结论 (1)，

$$
\frac{\bar X-\mu}{\sigma/\sqrt n}\sim N\left(0,1\right),
$$

平方得

$$
\frac{n\left(\bar X-\mu\right)^2}{\sigma^2}\sim\chi^2\left(1\right).
$$

由**定理 2.3.3** 之结论 (2)，

$$
\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right).
$$

由**定理 2.3.3** 之结论 (3)，$\bar X$ 与 $S^2$ 相互独立，故上述两个 $\chi^2$ 变量相互独立. 由**$\chi^2$ 分布的性质**（可加性），

$$
\frac{n\left(\bar X-\mu\right)^2}{\sigma^2}+\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(1\right)+\chi^2\left(n-1\right)=\chi^2\left(n\right).
$$

因此 $a=\frac{n}{\sigma^2}$，$b=\frac{n-1}{\sigma^2}$. $\blacksquare$

### 习题六

（习题 2.3-9）设 $X_1,X_2$ 是来自正态总体 $N\left(0,\sigma^2\right)$，$\sigma^2>0$ 的样本，求 $Y=\left(\frac{X_1+X_2}{X_1-X_2}\right)^2$ 的分布，并写出分布的自由度.

### 解答 习题六

由正态分布的可加性，$X_1+X_2\sim N\left(0,2\sigma^2\right)$，$X_1-X_2\sim N\left(0,2\sigma^2\right)$. 二者的协方差为

$$
\mathrm{Cov}\left(X_1+X_2,\ X_1-X_2\right)=\mathrm{Cov}\left(X_1,X_1\right)-\mathrm{Cov}\left(X_2,X_2\right)=\sigma^2-\sigma^2=0.
$$

因 $\left(X_1+X_2,\ X_1-X_2\right)$ 服从二维正态分布，协方差为零即相互独立. 标准化得

$$
U=\frac{X_1+X_2}{\sigma\sqrt2}\sim N\left(0,1\right),\qquad V=\frac{X_1-X_2}{\sigma\sqrt2}\sim N\left(0,1\right),
$$

且 $U$ 与 $V$ 相互独立.

于是

$$
Y=\left(\frac{X_1+X_2}{X_1-X_2}\right)^2=\left(\frac{U}{V}\right)^2=\frac{U^2}{V^2}.
$$

由**定义 2.2.1**（$\chi^2$ 分布），$U^2\sim\chi^2\left(1\right)$，$V^2\sim\chi^2\left(1\right)$，且二者相互独立. 由**定义 2.2.3**（$F$ 分布），

$$
Y=\frac{U^2/1}{V^2/1}\sim F\left(1,1\right).
$$

自由度为 $\left(1,1\right)$. $\blacksquare$

### 习题七

（习题 2.3-12）设 $X_1,X_2,X_3,X_4$ 是来自正态总体 $N\left(0,\sigma^2\right)$，$\sigma^2>0$ 的样本，记 $Y=\frac{X_1}{\sqrt{X_2^2+X_3^2+X_4^2}}$.

(1) 求 $c$ 使得 $cY$ 服从 $t$ 分布，并指出分布的自由度；

(2) 求 $E\left(cY\right)$，$D\left(cY\right)$.

### 解答 习题七

(1) 由 $X_1\sim N\left(0,\sigma^2\right)$，标准化得 $X_1/\sigma\sim N\left(0,1\right)$. 由**定义 2.2.1**（$\chi^2$ 分布），

$$
\frac{X_2^2+X_3^2+X_4^2}{\sigma^2}\sim\chi^2\left(3\right).
$$

$X_1$ 与 $X_2,X_3,X_4$ 互不重叠，故 $X_1/\sigma$ 与 $\left(X_2^2+X_3^2+X_4^2\right)/\sigma^2$ 相互独立. 由**定义 2.2.2**（$t$ 分布），

$$
T=\frac{X_1/\sigma}{\sqrt{\frac{X_2^2+X_3^2+X_4^2}{\sigma^2}/3}}=\sqrt3\cdot\frac{X_1}{\sqrt{X_2^2+X_3^2+X_4^2}}=\sqrt3\,Y\sim t\left(3\right).
$$

因此 $c=\sqrt3$，自由度为 $3$.

(2) 由 $T\sim t\left(3\right)$ 且 $3>1$，$E\left(T\right)=0$，故 $E\left(cY\right)=0$. 由 $t$ 分布的性质，当 $n>2$ 时 $D\left(T\right)=\frac{n}{n-2}$，故

$$
D\left(cY\right)=D\left(T\right)=\frac{3}{3-2}=3.
$$

$\blacksquare$

### 习题八

（习题 2.3-19）设 $X_1,X_2,\dots,X_n$ 是来自均匀分布总体 $U\left(0,\theta\right)$，$\theta>0$ 的样本，求 $\frac{\bar X-\theta/2}{\sqrt{\theta^2/12n}}$ 的极限分布.

### 解答 习题八

总体 $X\sim U\left(0,\theta\right)$，故 $E\left(X\right)=\frac{\theta}{2}$，$D\left(X\right)=\frac{\theta^2}{12}$. 由**基础知识**（中心极限定理），

$$
\frac{\bar X-\theta/2}{\sqrt{\theta^2/12n}}\xrightarrow{L}N\left(0,1\right).
$$

即该统计量的极限分布为标准正态分布 $N\left(0,1\right)$. $\blacksquare$

### 习题九

（习题 2.3-20）若 $X_1,X_2,\dots,X_n$ 是来自泊松分布总体 $P\left(\lambda\right)$，$\lambda>0$ 的样本，求 $\frac{\bar X-\lambda}{\sqrt{\bar X/n}}$ 的极限分布.

### 解答 习题九

总体 $X\sim P\left(\lambda\right)$，故 $E\left(X\right)=\lambda$，$D\left(X\right)=\lambda$. 由**基础知识**（中心极限定理），

$$
\frac{\bar X-\lambda}{\sqrt{\lambda/n}}\xrightarrow{L}N\left(0,1\right).
$$

又由大数定律，$\bar X\xrightarrow{P}\lambda$，故 $\bar X/\lambda\xrightarrow{P}1$，从而 $\sqrt{\bar X/\lambda}\xrightarrow{P}1$. 由**基础知识**（Slutsky 引理），

$$
\frac{\bar X-\lambda}{\sqrt{\bar X/n}}=\frac{\bar X-\lambda}{\sqrt{\lambda/n}}\cdot\sqrt{\frac{\lambda}{\bar X}}\xrightarrow{L}N\left(0,1\right)\cdot1=N\left(0,1\right).
$$

即该统计量的极限分布为标准正态分布 $N\left(0,1\right)$. $\blacksquare$

### 习题十

（习题 2.3-21）设 $X_1,X_2,\dots,X_n$ 是来自均匀分布总体 $U\left(0,1\right)$ 的样本，$X_{\left(1\right)},\dots,X_{\left(n\right)}$ 为顺序统计量，

(1) 若使 $P\left\{X_{\left(n\right)}\ge0.99\right\}$ 至少为 $0.95$，则样本容量至少取多少？

(2) 求极差 $R_n=X_{\left(n\right)}-X_{\left(1\right)}$ 的密度函数；

(3) 当 $n$ 趋于无穷时，求 $Z=2n\left(1-R_n\right)$ 的极限分布.

### 解答 习题十

(1) 总体 $X\sim U\left(0,1\right)$，其分布函数 $F\left(x\right)=x$（$0\le x\le1$）. 由**定理**（顺序统计量的分布），$X_{\left(n\right)}$ 的分布函数为 $F_{\left(n\right)}\left(x\right)=\left[F\left(x\right)\right]^n=x^n$. 故

$$
P\left\{X_{\left(n\right)}\ge0.99\right\}=1-P\left\{X_{\left(n\right)}<0.99\right\}=1-0.99^n.
$$

要求 $1-0.99^n\ge0.95$，即 $0.99^n\le0.05$，解得

$$
n\ge\frac{\ln0.05}{\ln0.99}\approx298.1.
$$

故样本容量至少取 $n=299$.

(2) 由**定理**（顺序统计量的分布），最小与最大顺序统计量的联合密度函数为

$$
f_{\left(1\right),\left(n\right)}\left(x,y\right)=n\left(n-1\right)\left(y-x\right)^{n-2},\qquad0<x<y<1.
$$

令 $r=y-x$，$s=x$，即 $x=s$，$y=s+r$，雅可比行列式 $J=1$. 对 $s$ 积分得 $R_n=X_{\left(n\right)}-X_{\left(1\right)}$ 的密度函数：

$$
f_{R_n}\left(r\right)=\int_0^{1-r}n\left(n-1\right)r^{n-2}\,\mathrm{d}s=n\left(n-1\right)r^{n-2}\left(1-r\right),\qquad0<r<1.
$$

(3) 当 $n\to+\infty$ 时，$X_{\left(n\right)}\to1$，$X_{\left(1\right)}\to0$，故 $R_n\to1$. 考虑中心化与标准化后的变量：

$$
n\left(1-X_{\left(n\right)}\right)\xrightarrow{L}Exp\left(1\right),\qquad nX_{\left(1\right)}\xrightarrow{L}Exp\left(1\right),
$$

且二者渐近独立. 由**$\chi^2$ 分布的性质**（可加性）及**伽马分布**与 $\chi^2$ 分布的关系，两个独立的 $Exp\left(1\right)$ 变量之和服从 $Ga\left(2,1\right)$，即 $\chi^2\left(2\right)/2$. 于是

$$
2n\left(1-R_n\right)=2\left[n\left(1-X_{\left(n\right)}\right)+nX_{\left(1\right)}\right]\xrightarrow{L}2\cdot Ga\left(2,1\right)=Ga\left(2,\frac12\right)=\chi^2\left(4\right).
$$

即 $Z=2n\left(1-R_n\right)$ 的极限分布为 $\chi^2\left(4\right)$. $\blacksquare$
