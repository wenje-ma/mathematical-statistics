# 作业 11

> **引理 3.5.1**（改进无偏估计的方法）<br>设 $T=T\left(X_1,X_2,\dots,X_n\right)$ 是一个充分统计量，而 $\hat g\left(X_1,X_2,\dots,X_n\right)$ 是 $g\left(\theta\right)$ 的一个无偏估计，则 $h\left(T\right)=E\left[\hat g\left(X_1,X_2,\dots,X_n\right)\mid T\right]$ 是 $g\left(\theta\right)$ 的无偏估计，且对任意 $\theta$，有 $D\left[h\left(T\right)\right]\le D\left[\hat g\left(X_1,X_2,\dots,X_n\right)\right]$，等号当且仅当 $\hat g\left(X_1,X_2,\dots,X_n\right)=h\left(T\right)$ 几乎处处成立.

> **定理 3.5.1**（Lehmann-Scheffé 定理，简称 L-S 定理）<br>设 $T\left(X\right)=T\left(X_1,X_2,\dots,X_n\right)$ 是充分完备统计量，若 $g\left(T\left(X\right)\right)$ 是 $g\left(\theta\right)$ 的一个无偏估计，则 $g\left(T\left(X\right)\right)$ 是 $g\left(\theta\right)$ 唯一的一致最小方差无偏估计.

> **推论 3.5.1**（指数族自然形式下的充分完备统计量）<br>设样本的分布为指数族的自然形式 $f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k\theta_iT_i\left(x\right)\right\}h\left(x\right)$，若自然参数空间作为 $\mathbb R^k$ 的子集有内点，则 $T\left(X\right)=\left(T_1\left(X\right),\dots,T_k\left(X\right)\right)$ 为充分完备统计量；此时若 $h\left(T\left(X\right)\right)$ 是 $g\left(\theta\right)$ 的无偏估计，则它是 $g\left(\theta\right)$ 唯一的一致最小方差无偏估计.

> **例 3.5.3**（两点分布的充分完备统计量）<br>设 $X_1,X_2,\dots,X_n$ 是来自两点分布 $B\left(1,p\right)$，$0<p<1$ 的样本，则 $T\left(X_1,X_2,\dots,X_n\right)=\sum_{i=1}^n X_i\sim B\left(n,p\right)$ 是 $p$ 的充分完备统计量，且 $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ 为 $p$ 的唯一一致最小方差无偏估计.

> **例 3.5.7**（正态总体的充分完备统计量）<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$，$\mu\in\mathbb R,\ \sigma^2>0$ 的样本，则 $T\left(X\right)=\left(\bar X,\sum_{i=1}^n\left(X_i-\bar X\right)^2\right)$ 是 $\left(\mu,\sigma^2\right)$ 的充分完备统计量，其中 $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$.

> **抽样分布**（正态样本的抽样分布）<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，记 $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$，$S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$，则 $\bar X\sim N\left(\mu,\frac{\sigma^2}{n}\right)$，$\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$，且 $\bar X$ 与 $S^2$ 相互独立. 特别地，当 $\mu=0$ 时，$T=\sum_{i=1}^n X_i^2=\sigma^2\cdot\frac{\sum_{i=1}^n X_i^2}{\sigma^2}\sim\sigma^2\chi^2\left(n\right)$.

> **基础知识**（$\chi^2$ 分布的矩）<br>若 $Y\sim\chi^2\left(k\right)$，则 $E\left(Y\right)=k$，$D\left(Y\right)=2k$，$E\left(Y^2\right)=k\left(k+2\right)$，$E\left(\frac{1}{Y}\right)=\frac{1}{k-2}\ \left(k>2\right)$，$E\left(\sqrt Y\right)=\sqrt 2\,\frac{\Gamma\left(\frac{k+1}{2}\right)}{\Gamma\left(\frac{k}{2}\right)}$.

### 习题一

（习题 3.5-4）设 $X_1,X_2,\dots,X_n$ 是来自两点分布总体 $B\left(1,p\right)$，$0<p<1$ 的样本，其中 $0<p<1$ 为未知参数：

(1) 求 $p^m$ 的一致最小方差无偏估计，其中 $m>0$ 为自然数；

(2) 求 $p\left(1-p\right)$ 的一致最小方差无偏估计.

### 解答 习题一

由**例 3.5.3**（两点分布的充分完备统计量），$T=\sum_{i=1}^n X_i\sim B\left(n,p\right)$ 是 $p$ 的充分完备统计量. 由**定理 3.5.1**（L-S 定理），只要找到 $T$ 的函数 $h\left(T\right)$ 使其为待估函数的无偏估计，即为该函数的唯一一致最小方差无偏估计.

(1) 待估 $g\left(p\right)=p^m$. 设 $h\left(T\right)$ 满足 $E\left[h\left(T\right)\right]=p^m$. 由 $T\sim B\left(n,p\right)$，其分布列为 $P\left\{T=t\right\}=\binom{n}{t}p^t\left(1-p\right)^{n-t}$，$t=0,1,\dots,n$. 取

$$
h\left(t\right)=
\begin{cases}
\dfrac{\binom{n-m}{t-m}}{\binom{n}{t}},& t=m,m+1,\dots,n,\\[6pt]
0,& t=0,1,\dots,m-1.
\end{cases}
$$

则对任意 $0<p<1$，

$$
E\left[h\left(T\right)\right]=\sum_{t=m}^n\frac{\binom{n-m}{t-m}}{\binom{n}{t}}\binom{n}{t}p^t\left(1-p\right)^{n-t}=\sum_{t=m}^n\binom{n-m}{t-m}p^t\left(1-p\right)^{n-t}.
$$

令 $s=t-m$，由二项式定理，

$$
E\left[h\left(T\right)\right]=p^m\sum_{s=0}^{n-m}\binom{n-m}{s}p^s\left(1-p\right)^{n-m-s}=p^m\left[p+\left(1-p\right)\right]^{n-m}=p^m.
$$

故 $h\left(T\right)$ 是 $p^m$ 的无偏估计，又是充分完备统计量 $T$ 的函数，由**定理 3.5.1**（L-S 定理），$p^m$ 的唯一一致最小方差无偏估计为

$$
\hat g_1=
\begin{cases}
\dfrac{\binom{n-m}{T-m}}{\binom{n}{T}},& T=m,m+1,\dots,n,\\[6pt]
0,& T=0,1,\dots,m-1,
\end{cases}\qquad T=\sum_{i=1}^n X_i.
$$

(2) 待估 $g\left(p\right)=p\left(1-p\right)$. 由**例 3.5.4**（教材已用待定系数法求得），$g\left(p\right)=p\left(1-p\right)$ 的一个无偏估计为 $g\left(T\right)=\frac{T\left(n-T\right)}{n\left(n-1\right)}$. 验证其无偏性：由 $T\sim B\left(n,p\right)$，$E\left(T\right)=np$，$D\left(T\right)=np\left(1-p\right)$，故

$$
E\left[T\left(n-T\right)\right]=nE\left(T\right)-E\left(T^2\right)=n^2p-\left[D\left(T\right)+\left(E\left(T\right)\right)^2\right]=n^2p-\left[np\left(1-p\right)+n^2p^2\right]=n\left(n-1\right)p\left(1-p\right).
$$

于是 $E\left[\frac{T\left(n-T\right)}{n\left(n-1\right)}\right]=p\left(1-p\right)$. 又 $\frac{T\left(n-T\right)}{n\left(n-1\right)}$ 是充分完备统计量 $T$ 的函数，由**定理 3.5.1**（L-S 定理），$p\left(1-p\right)$ 的唯一一致最小方差无偏估计为

$$
\hat g_2=\frac{T\left(n-T\right)}{n\left(n-1\right)},\qquad T=\sum_{i=1}^n X_i.
$$

$\blacksquare$

### 习题二

（习题 3.5-6）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(0,\sigma^2\right)$ 的样本，其中 $\sigma>0$ 为未知参数，分别求 $\sigma$ 和 $\sigma^4$ 的一致最小方差无偏估计.

### 解答 习题二

由**推论 3.5.1**（指数族自然形式下的充分完备统计量），正态分布族 $N\left(0,\sigma^2\right)$ 为单参数指数族，其密度函数可写为

$$
f\left(x;\sigma^2\right)=\frac{1}{\sqrt{2\pi}\sigma}\exp\left\{-\frac{x^2}{2\sigma^2}\right\}=\frac{1}{\sqrt{2\pi}}\left(\sigma^2\right)^{-\frac{1}{2}}\exp\left\{-\frac{1}{2\sigma^2}x^2\right\}.
$$

自然参数空间 $\left\{-\frac{1}{2\sigma^2}: \sigma>0\right\}=\left(-\infty,0\right)$ 作为 $\mathbb R$ 的子集有内点，故 $T=\sum_{i=1}^n X_i^2$ 为充分完备统计量. 由**抽样分布**（正态样本的抽样分布），$\frac{T}{\sigma^2}=\sum_{i=1}^n\left(\frac{X_i}{\sigma}\right)^2\sim\chi^2\left(n\right)$.

(1) 求 $\sigma$ 的一致最小方差无偏估计. 由**基础知识**（$\chi^2$ 分布的矩），若 $Y\sim\chi^2\left(n\right)$，则 $E\left(\sqrt Y\right)=\sqrt 2\,\frac{\Gamma\left(\frac{n+1}{2}\right)}{\Gamma\left(\frac{n}{2}\right)}$. 令 $Y=\frac{T}{\sigma^2}$，则

$$
E\left(\sqrt T\right)=\sigma E\left(\sqrt Y\right)=\sigma\sqrt 2\,\frac{\Gamma\left(\frac{n+1}{2}\right)}{\Gamma\left(\frac{n}{2}\right)}.
$$

于是

$$
E\left[\frac{\Gamma\left(\frac{n}{2}\right)}{\sqrt 2\,\Gamma\left(\frac{n+1}{2}\right)}\sqrt T\right]=\sigma.
$$

该估计量是充分完备统计量 $T$ 的函数且无偏，由**定理 3.5.1**（L-S 定理），$\sigma$ 的唯一一致最小方差无偏估计为

$$
\hat\sigma=\frac{\Gamma\left(\frac{n}{2}\right)}{\sqrt 2\,\Gamma\left(\frac{n+1}{2}\right)}\sqrt T,\qquad T=\sum_{i=1}^n X_i^2.
$$

(2) 求 $\sigma^4$ 的一致最小方差无偏估计. 由**基础知识**（$\chi^2$ 分布的矩），若 $Y\sim\chi^2\left(n\right)$，则 $E\left(Y^2\right)=n\left(n+2\right)$. 由 $T=\sigma^2Y$，

$$
E\left(T^2\right)=\sigma^4 E\left(Y^2\right)=\sigma^4 n\left(n+2\right).
$$

于是 $E\left[\frac{T^2}{n\left(n+2\right)}\right]=\sigma^4$. 该估计量是充分完备统计量 $T$ 的函数且无偏，由**定理 3.5.1**（L-S 定理），$\sigma^4$ 的唯一一致最小方差无偏估计为

$$
\widehat{\sigma^4}=\frac{T^2}{n\left(n+2\right)},\qquad T=\sum_{i=1}^n X_i^2.
$$

$\blacksquare$

### 习题三

（习题 3.5-7）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，其中 $\mu\in\mathbb R$，$\sigma>0$ 都是未知参数：

(1) 分别求 $\mu+\sigma^2$ 和 $\frac{\mu^2}{\sigma^2}$ 的一致最小方差无偏估计；

(2) 证明 $\hat\mu^2=\bar X^2-\frac{S^2}{n}$ 是 $\mu^2$ 的一致最小方差无偏估计.

### 解答 习题三

由**例 3.5.7**（正态总体的充分完备统计量），$T\left(X\right)=\left(\bar X,\sum_{i=1}^n\left(X_i-\bar X\right)^2\right)$ 是 $\left(\mu,\sigma^2\right)$ 的充分完备统计量，其中 $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$，$S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$. 由**抽样分布**（正态样本的抽样分布），$\bar X\sim N\left(\mu,\frac{\sigma^2}{n}\right)$，$\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$，且 $\bar X$ 与 $S^2$ 相互独立. 由**定理 3.5.1**（L-S 定理），待估函数的无偏估计量若为 $\left(\bar X,S^2\right)$ 的函数，则为一致最小方差无偏估计.

(1) 先求 $\mu+\sigma^2$ 的一致最小方差无偏估计. 由 $E\left(\bar X\right)=\mu$，$E\left(S^2\right)=\sigma^2$，得

$$
E\left(\bar X+S^2\right)=E\left(\bar X\right)+E\left(S^2\right)=\mu+\sigma^2.
$$

$\bar X+S^2$ 是充分完备统计量 $\left(\bar X,S^2\right)$ 的函数且无偏，由**定理 3.5.1**（L-S 定理），$\mu+\sigma^2$ 的唯一一致最小方差无偏估计为 $\bar X+S^2$.

再求 $\frac{\mu^2}{\sigma^2}$ 的一致最小方差无偏估计. 由 $\bar X$ 与 $S^2$ 独立，以及 $E\left(\bar X^2\right)=D\left(\bar X\right)+\left(E\bar X\right)^2=\sigma^2/n+\mu^2$；由**基础知识**（$\chi^2$ 分布的矩），$\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$，故当 $n>3$ 时

$$
E\left(\frac{1}{S^2}\right)=\frac{n-1}{\sigma^2}E\left[\frac{1}{\frac{\left(n-1\right)S^2}{\sigma^2}}\right]=\frac{n-1}{\sigma^2}\cdot\frac{1}{\left(n-1\right)-2}=\frac{n-1}{\sigma^2\left(n-3\right)}.
$$

于是由独立性，

$$
E\left(\frac{\bar X^2}{S^2}\right)=E\left(\bar X^2\right)E\left(\frac{1}{S^2}\right)=\left(\mu^2+\frac{\sigma^2}{n}\right)\cdot\frac{n-1}{\sigma^2\left(n-3\right)}.
$$

两边乘 $\frac{n-3}{n-1}$，得

$$
E\left[\frac{n-3}{n-1}\cdot\frac{\bar X^2}{S^2}\right]=\frac{\mu^2}{\sigma^2}+\frac{1}{n}.
$$

因此

$$
E\left[\frac{\left(n-3\right)\bar X^2}{\left(n-1\right)S^2}-\frac{1}{n}\right]=\frac{\mu^2}{\sigma^2}.
$$

该估计量是充分完备统计量 $\left(\bar X,S^2\right)$ 的函数且无偏，由**定理 3.5.1**（L-S 定理），$\frac{\mu^2}{\sigma^2}$ 的唯一一致最小方差无偏估计为

$$
\frac{\left(n-3\right)\bar X^2}{\left(n-1\right)S^2}-\frac{1}{n}\qquad\left(n>3\right).
$$

(2) 证明 $\hat\mu^2=\bar X^2-\frac{S^2}{n}$ 是 $\mu^2$ 的一致最小方差无偏估计. 由 $E\left(\bar X^2\right)=\mu^2+\frac{\sigma^2}{n}$，$E\left(S^2\right)=\sigma^2$，得

$$
E\left(\bar X^2-\frac{S^2}{n}\right)=E\left(\bar X^2\right)-\frac{1}{n}E\left(S^2\right)=\mu^2+\frac{\sigma^2}{n}-\frac{\sigma^2}{n}=\mu^2.
$$

故 $\bar X^2-\frac{S^2}{n}$ 是 $\mu^2$ 的无偏估计，且是充分完备统计量 $\left(\bar X,S^2\right)$ 的函数，由**定理 3.5.1**（L-S 定理），$\hat\mu^2=\bar X^2-\frac{S^2}{n}$ 是 $\mu^2$ 的唯一一致最小方差无偏估计. $\blacksquare$
