# week4

> **定义 2.2.1 (卡方分布)**
> 
> 设 $X_1,X_2,\ldots,X_n$ 独立同分布, 且 $X_1\sim{}N\left(0,1\right)$, 令 $\xi=X_1^{2}+\cdots+X_n^{2}$, 则称 $\xi$ 是自由度为 $n$ 的卡方变量, 记作 $\xi\sim\chi^{2}\left(n\right)$. (教材 $\S2.2$, p23)

> **定义 2.2.2 (t 分布)**
> 
> 设 $X\sim{}N\left(0,1\right)$, $Y\sim\chi^{2}\left(n\right)$, 且 $X$ 与 $Y$ 相互独立, 则称 $T=\frac{X}{\sqrt{Y/n}}$ 为自由度为 $n$ 的 t 变量, 记作 $T\sim{}t\left(n\right)$. (教材 $\S2.2$, p29)

> **定义 2.2.3 (F 分布)**
> 
> 设 $X\sim\chi^{2}\left(m\right)$, $Y\sim\chi^{2}\left(n\right)$, 且 $X$ 与 $Y$ 相互独立, 则称 $F=\frac{X/m}{Y/n}$ 为自由度为 $m$ 和 $n$ 的 F 变量, 记作 $F\sim{}F\left(m,n\right)$. (教材 $\S2.2$, p33)

> **引理 2.3.1 (样本均值与样本方差的期望)**
> 
> 设 $X_1,\ldots,X_n$ 是来自总体 $X$ 的样本, $E\left(X\right)=\mu$, $D\left(X\right)=\sigma^{2}$, 则 $E\left(\bar{X}\right)=\mu$, $D\left(\bar{X}\right)=\frac{\sigma^{2}}{n}$, $E\left(S^{2}\right)=\sigma^{2}$. (教材 $\S2.3$, p43)

> **定理 2.3.3 (正态样本均值与样本方差的分布)**
> 
> 设 $X_1,\ldots,X_n$ 是来自 $N\left(\mu,\sigma^{2}\right)$ 的样本, 则 $\bar{X}\sim{}N\left(\mu,\frac{\sigma^{2}}{n}\right)$; $\frac{\left(n-1\right)S^{2}}{\sigma^{2}}\sim\chi^{2}\left(n-1\right)$; 且 $\bar{X}$ 与 $S^{2}$ 相互独立. (教材 $\S2.3$, p43)

> **定理 2.3.4 (正态样本对总体均值的平方和)**
> 
> 设 $X_1,\ldots,X_n$ 是来自 $N\left(\mu,\sigma^{2}\right)$ 的样本, 则 $\frac{1}{\sigma^{2}}\sum_{i=1}^{n}\left(X_i-\mu\right)^{2}\sim\chi^{2}\left(n\right)$. (教材 $\S2.3$, p45)

## 习题 2.3-2 (泊松样本的三条数字特征)

设 $X_1,X_2,\ldots,X_n$ 是来自泊松分布总体 $P\left(\lambda\right)$, $\lambda>0$ 的样本, 求 $E\left(\bar{X}\right)$, $D\left(\bar{X}\right)$, $E\left(S^{2}\right)$.

### 解答 2.3-2

泊松分布的均值为 $\lambda$, 方差为 $\lambda$, 即 $\mu=\sigma^{2}=\lambda$. 由**引理 2.3.1 (样本均值与样本方差的期望)**,

$$
E\left(\bar{X}\right)=\mu=\lambda,\quad{}D\left(\bar{X}\right)=\frac{\sigma^{2}}{n}=\frac{\lambda}{n},\quad{}E\left(S^{2}\right)=\sigma^{2}=\lambda.
$$

$\blacksquare$

## 习题 2.3-4 (正态样本的四条数字特征)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$, $\mu\in\mathbb{R}$, $\sigma^{2}>0$ 的样本, 求 $E\left(\bar{X}\right)$, $D\left(\bar{X}\right)$, $E\left(S^{2}\right)$, $D\left(S^{2}\right)$.

### 解答 2.3-4

由**引理 2.3.1 (样本均值与样本方差的期望)**,

$$
E\left(\bar{X}\right)=\mu,\quad{}D\left(\bar{X}\right)=\frac{\sigma^{2}}{n},\quad{}E\left(S^{2}\right)=\sigma^{2}.
$$

$D\left(S^{2}\right)$ 需要用分布. 由**定理 2.3.3 (正态样本均值与样本方差的分布)**, $\frac{\left(n-1\right)S^{2}}{\sigma^{2}}\sim\chi^{2}\left(n-1\right)$. 卡方分布 $n-1$ 自由度的方差为 $2\left(n-1\right)$, 故

$$
D\left(\frac{\left(n-1\right)S^{2}}{\sigma^{2}}\right)=\frac{\left(n-1\right)^{2}}{\sigma^{4}}D\left(S^{2}\right)=2\left(n-1\right),
$$

由此 $D\left(S^{2}\right)=\frac{2\sigma^{4}}{n-1}$.

$\blacksquare$

## 习题 2.3-5 (引入一个新观测构造 t 统计量)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$, $\mu\in\mathbb{R}$, $\sigma^{2}>0$ 的样本, 且 $\bar{X}=\frac{1}{n}\sum_{i=1}^{n}X_i$, $S_n^{2}=\frac{1}{n}\sum_{i=1}^{n}\left(X_i-\bar{X}\right)^{2}$, 又设 $X_{n+1}\sim{}N\left(\mu,\sigma^{2}\right)$, 且 $X_{n+1}$ 与 $X_1,\ldots,X_n$ 独立, 求常数 $c$ 使得 $c\frac{X_{n+1}-\bar{X}}{S_n}$ 服从 $t$ 分布, 并指出分布的自由度.

### 解答 2.3-5

记 $\bar{X}$ 与 $S_n^{2}$ 如上. 由**定理 2.3.3 (正态样本均值与样本方差的分布)**, $\bar{X}\sim{}N\left(\mu,\sigma^{2}/n\right)$, $\bar{X}$ 与 $S^{2}=\frac{n}{n-1}S_n^{2}$ 相互独立, 且 $\frac{\left(n-1\right)S^{2}}{\sigma^{2}}=\frac{nS_n^{2}}{\sigma^{2}}\sim\chi^{2}\left(n-1\right)$.

$X_{n+1}\sim{}N\left(\mu,\sigma^{2}\right)$ 且与 $X_1,\ldots,X_n$ 独立, 故与 $\bar{X}$, $S_n^{2}$ 都独立. 两个独立正态变量之差仍正态, 均值为零, 方差相加:

$$
X_{n+1}-\bar{X}\sim{}N\left(0,\sigma^{2}+\frac{\sigma^{2}}{n}\right)=N\left(0,\frac{n+1}{n}\sigma^{2}\right).
$$

标准化得 $\sqrt{\frac{n}{n+1}}\frac{X_{n+1}-\bar{X}}{\sigma}\sim{}N\left(0,1\right)$, 它与 $S_n^{2}$ 独立. 按**定义 2.2.2 (t 分布)**,

$$
\frac{\sqrt{\frac{n}{n+1}}\frac{X_{n+1}-\bar{X}}{\sigma}}{\sqrt{\frac{nS_n^{2}}{\sigma^{2}}\left/\left(n-1\right)\right.}}\sim{}t\left(n-1\right).
$$

把 $\sigma$ 消去, 分子分母同乘 $\sigma$:

$$
\frac{\sqrt{\frac{n}{n+1}}\left(X_{n+1}-\bar{X}\right)}{\sqrt{\frac{nS_n^{2}}{n-1}}}=\sqrt{\frac{n}{n+1}}\cdot\sqrt{\frac{n-1}{n}}\cdot\frac{X_{n+1}-\bar{X}}{S_n}=\sqrt{\frac{n-1}{n+1}}\,\frac{X_{n+1}-\bar{X}}{S_n}.
$$

故 $c=\sqrt{\frac{n-1}{n+1}}$, 自由度为 $n-1$.

$\blacksquare$

## 习题 2.3-7 (两段平方和之比构造 F 统计量)

设 $X_1,X_2,\ldots,X_{m+n}$ 是来自正态总体 $N\left(0,\sigma^{2}\right)$, $\sigma^{2}>0$ 的样本, 求常数 $c$ 使得 $F=c\frac{\sum_{i=1}^{n}X_i^{2}}{\sum_{i=n+1}^{m+n}X_i^{2}}$ 服从 $F$ 分布, 并指出分布的自由度.

### 解答 2.3-7

把 $\frac{X_i}{\sigma}$ 看成一列独立 $N\left(0,1\right)$ 变量. 由**定义 2.2.1 (卡方分布)**,

$$
\frac{1}{\sigma^{2}}\sum_{i=1}^{n}X_i^{2}\sim\chi^{2}\left(n\right),\quad\frac{1}{\sigma^{2}}\sum_{i=n+1}^{m+n}X_i^{2}\sim\chi^{2}\left(m\right),
$$

两段涉及的 $X_i$ 不同, 故这两个卡方变量相互独立. 按**定义 2.2.3 (F 分布)**,

$$
\frac{\left(\frac{1}{\sigma^{2}}\sum_{i=1}^{n}X_i^{2}\right)\left/\right.n}{\left(\frac{1}{\sigma^{2}}\sum_{i=n+1}^{m+n}X_i^{2}\right)\left/\right.m}\sim{}F\left(n,m\right).
$$

约去 $\sigma^{2}$, 该式等于 $\frac{m}{n}\frac{\sum_{i=1}^{n}X_i^{2}}{\sum_{i=n+1}^{m+n}X_i^{2}}$, 故 $c=\frac{m}{n}$, 第一自由度为 $n$, 第二自由度为 $m$.

$\blacksquare$

## 习题 2.3-8 (均值平方与样本方差拼成卡方)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$, $\mu\in\mathbb{R}$, $\sigma^{2}>0$ 的样本, 求常数 $a$ 和 $b$ 使得 $a\left(\bar{X}-\mu\right)^{2}+bS^{2}\sim\chi^{2}\left(n\right)$.

### 解答 2.3-8

由**定理 2.3.3 (正态样本均值与样本方差的分布)**, $\frac{\sqrt{n}\left(\bar{X}-\mu\right)}{\sigma}\sim{}N\left(0,1\right)$, $\frac{\left(n-1\right)S^{2}}{\sigma^{2}}\sim\chi^{2}\left(n-1\right)$, 且 $\bar{X}$ 与 $S^{2}$ 相互独立.

前一项平方, 由**定义 2.2.1 (卡方分布)** 是 $\chi^{2}\left(1\right)$ 变量; 与后一个 $\chi^{2}\left(n-1\right)$ 变量独立相加, 再按同一定义把 $n$ 个独立 $N\left(0,1\right)$ 平方合并, 和为 $\chi^{2}\left(n\right)$:

$$
\frac{n\left(\bar{X}-\mu\right)^{2}}{\sigma^{2}}+\frac{\left(n-1\right)S^{2}}{\sigma^{2}}\sim\chi^{2}\left(n\right).
$$

故

$$
a=\frac{n}{\sigma^{2}},\quad{}b=\frac{n-1}{\sigma^{2}}.
$$

$\blacksquare$

## 习题 2.3-9 (两样本和差之比的分布)

设 $X_1,X_2$ 是来自正态总体 $N\left(0,\sigma^{2}\right)$, $\sigma^{2}>0$ 的样本, 求 $Y=\left(\frac{X_1+X_2}{X_1-X_2}\right)^{2}$ 的分布, 并写出分布的自由度.

### 解答 2.3-9

记 $U=X_1+X_2$, $V=X_1-X_2$. 由 $X_1,X_2$ 独立同分布 $N\left(0,\sigma^{2}\right)$, 二元正态的线性组合仍正态, 故 $\left(U,V\right)$ 服从二元正态, 且

$$
E\left(U\right)=0,\quad{}E\left(V\right)=0,\quad{}D\left(U\right)=2\sigma^{2},\quad{}D\left(V\right)=2\sigma^{2},\quad\mathrm{Cov}\left(U,V\right)=\sigma^{2}-\sigma^{2}=0.
$$

二元正态中协方差为零等价于独立, 故 $U$ 与 $V$ 相互独立. 于是

$$
\frac{U}{\sqrt{2}\sigma}\sim{}N\left(0,1\right),\quad\frac{V}{\sqrt{2}\sigma}\sim{}N\left(0,1\right),
$$

两者独立. 由**定义 2.2.2 (t 分布)** 取 $n=1$ 可知 $\frac{U/\left(\sqrt{2}\sigma\right)}{V/\left(\sqrt{2}\sigma\right)}=\frac{U}{V}\sim{}t\left(1\right)$; 而 $t\left(1\right)$ 变量的平方, 按**定义 2.2.3 (F 分布)** 取 $m=n=1$, 满足 $F\left(1,1\right)$ 的定义, 故

$$
Y=\left(\frac{U}{V}\right)^{2}\sim{}F\left(1,1\right),
$$

自由度为 $1$ 和 $1$.

$\blacksquare$

## 习题 2.3-12 (用四个正态观测构造 t 统计量)

设 $X_1,X_2,X_3,X_4$ 是来自正态总体 $N\left(0,\sigma^{2}\right)$, $\sigma^{2}>0$ 的样本, 记 $Y=\frac{X_1}{\sqrt{X_2^{2}+X_3^{2}+X_4^{2}}}$,

(1) 求 $c$ 使得 $cY$ 服从 $t$ 分布, 并指出分布的自由度;

(2) 求 $E\left(cY\right)$, $D\left(cY\right)$.

### 解答 2.3-12

(1) 记 $W=X_2^{2}+X_3^{2}+X_4^{2}$. 由**定义 2.2.1 (卡方分布)**, $\frac{W}{\sigma^{2}}\sim\chi^{2}\left(3\right)$; 又 $\frac{X_1}{\sigma}\sim{}N\left(0,1\right)$; 两者涉及的 $X_i$ 不同, 故相互独立. 按**定义 2.2.2 (t 分布)**,

$$
\frac{X_1/\sigma}{\sqrt{\frac{W}{\sigma^{2}}\left/\right.3}}=\frac{X_1/\sigma}{\sqrt{W/\left(3\sigma^{2}\right)}}=\frac{X_1}{\sigma}\cdot\frac{\sqrt{3}\sigma}{\sqrt{W}}=\sqrt{3}\,\frac{X_1}{\sqrt{W}}=\sqrt{3}\,Y.
$$

上式左端是 $t\left(3\right)$ 变量, 故 $cY=\sqrt{3}\,Y\sim{}t\left(3\right)$, 即 $c=\sqrt{3}$, 自由度为 $3$.

$\blacksquare$

(2) $t\left(n\right)$ 的密度关于原点对称, 且 $n=3>1$ 时一阶矩存在, 故

$$
E\left(cY\right)=0.
$$

$t\left(n\right)$ 在 $n>2$ 时方差为 $\frac{n}{n-2}$, 故

$$
D\left(cY\right)=\frac{3}{3-2}=3.
$$

$\blacksquare$
