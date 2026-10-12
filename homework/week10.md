# 作业 10

> **定义 3.4.1**（无偏估计）<br>设 $\hat\theta=\hat\theta\left(X_1,X_2,\dots,X_n\right)$ 为未知参数 $\theta$ 的估计量，若对任意 $\theta\in\Theta$ 都有 $$E\left[\hat\theta\left(X_1,X_2,\dots,X_n\right)\right]=\theta,$$ 则称 $\hat\theta$ 为 $\theta$ 的无偏估计. 对 $g\left(\theta\right)$ 的估计量 $\hat g$，若 $E\left[\hat g\right]=g\left(\theta\right)$，则称 $\hat g$ 为 $g\left(\theta\right)$ 的无偏估计.

> **定义 3.4.2**（有效性）<br>设 $\hat\theta_1$ 与 $\hat\theta_2$ 都是 $\theta$ 的无偏估计，若对一切 $\theta\in\Theta$ 都有 $D\left(\hat\theta_1\right)\le D\left(\hat\theta_2\right)$，且不等号至少对某个 $\theta$ 成立，则称 $\hat\theta_1$ 比 $\hat\theta_2$ 有效.

> **定义 3.4.3**（相合估计）<br>设对每个自然数 $n$，$\hat\theta_n=\hat\theta_n\left(X_1,X_2,\dots,X_n\right)$ 为 $\theta$ 的估计量，若对任意 $\theta\in\Theta$ 及任意 $\varepsilon>0$，都有 $$\lim_{n\to\infty}P\left\{\left|\hat\theta_n-\theta\right|\ge\varepsilon\right\}=0,$$ 则称 $\hat\theta_n$ 为 $\theta$ 的（弱）相合估计.

> **基础知识**（切比雪夫不等式与大数定律）<br>对任意随机变量 $Y$ 及 $\varepsilon>0$，有 $P\left\{\left|Y-EY\right|\ge\varepsilon\right\}\le\frac{D\left(Y\right)}{\varepsilon^2}$；独立同分布且期望存在时，由大数定律 $\bar X_n\xrightarrow{P}E\left(X\right)$；依概率收敛经连续函数映射保持不变.

### 习题一

（习题 3.4-1）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，求 $c$ 使得 $c\sum_{i=1}^{n-1}\left(X_{i+1}-X_i\right)^2$ 是 $\sigma^2$ 的无偏估计.

### 解答 习题一

由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 相互独立且均服从 $N\left(\mu,\sigma^2\right)$. 记相邻差 $Y_i=X_{i+1}-X_i$，$i=1,2,\dots,n-1$. 因独立正态变量的线性组合仍为正态变量，

$$
Y_i\sim N\left(0,\sigma^2+\sigma^2\right)=N\left(0,2\sigma^2\right),
$$

故 $E\left(Y_i\right)=0$，$E\left(Y_i^2\right)=D\left(Y_i\right)=2\sigma^2$. 于是

$$
E\left[c\sum_{i=1}^{n-1}\left(X_{i+1}-X_i\right)^2\right]=c\sum_{i=1}^{n-1}E\left(Y_i^2\right)=c\left(n-1\right)\cdot 2\sigma^2.
$$

由**定义 3.4.1**（无偏估计），令上式等于 $\sigma^2$，解得

$$
c=\frac{1}{2\left(n-1\right)}.
$$

$\blacksquare$

### 习题二

（习题 3.4-5）设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，且 $X$ 的密度函数为

$$
f\left(x,\theta\right)=\begin{cases}e^{-\left(x-\theta\right)},&x>\theta,\\0,&\text{其他}.\end{cases}
$$

(1) 求参数 $\theta$ 的矩估计 $\hat\theta_1$，并判断 $\hat\theta_1$ 是否是 $\theta$ 的无偏估计？

(2) 求参数 $\theta$ 的极大似然估计 $\hat\theta_2$，并判断 $\hat\theta_2$ 是否是 $\theta$ 的无偏估计？

### 解答 习题二

(1) 由密度函数，$X=\theta+Y$，其中 $Y\sim E\left(1\right)$ 为标准指数分布，故 $E\left(X\right)=\theta+1$. 用样本矩代替总体矩，令 $\bar X=\theta+1$，得矩估计

$$
\hat\theta_1=\bar X-1.
$$

由 $E\left(\bar X\right)=E\left(X\right)=\theta+1$，得 $E\left(\hat\theta_1\right)=\left(\theta+1\right)-1=\theta$. 由**定义 3.4.1**（无偏估计），$\hat\theta_1=\bar X-1$ 是 $\theta$ 的无偏估计.

(2) 似然函数为

$$
L\left(\theta\right)=\prod_{i=1}^n e^{-\left(x_i-\theta\right)}=e^{-\sum_{i=1}^n\left(x_i-\theta\right)}=e^{-\sum_{i=1}^n x_i+n\theta},
$$

其非零当且仅当 $\theta\le x_{\left(1\right)}$. 由**定义 3.3.2**（极大似然估计），$L\left(\theta\right)=e^{n\theta}\cdot e^{-\sum x_i}$ 关于 $\theta$ 单调递增，故在允许范围内取 $\theta$ 最大时达极大值，即

$$
\hat\theta_2=X_{\left(1\right)}=\min\left\{X_1,X_2,\dots,X_n\right\}.
$$

由 $X_i-\theta\sim E\left(1\right)$，最小顺序统计量满足 $X_{\left(1\right)}-\theta\sim E\left(n\right)$，故 $E\left(X_{\left(1\right)}-\theta\right)=\frac{1}{n}$，即 $E\left(\hat\theta_2\right)=\theta+\frac{1}{n}\ne\theta$. 由**定义 3.4.1**（无偏估计），$\hat\theta_2$ 不是 $\theta$ 的无偏估计（它是渐近无偏估计）.

$\blacksquare$

### 习题三

（习题 3.4-7）设 $X_1,X_2$ 是来自总体 $X$ 的样本，且 $X$ 的密度函数为

$$
f\left(x,\theta\right)=\begin{cases}k\theta^k x^{-\left(k+1\right)},&x>\theta,\\0,&\text{其他},\end{cases}
$$

其中 $k>2$ 已知，$\theta>0$ 为未知参数.

(1) 证明 $T_1=\frac{k-1}{2k}\left(X_1+X_2\right)$ 和 $T_2=\frac{2k-1}{2k}\min\left\{X_1,X_2\right\}$ 都是 $\theta$ 的无偏估计；

(2) 指出 $T_1$ 和 $T_2$ 哪一个有效.

### 解答 习题三

(1) 先求 $X$ 的一、二阶矩：

$$
E\left(X\right)=\int_\theta^{+\infty}x\cdot k\theta^k x^{-\left(k+1\right)}\,\mathrm{d}x=k\theta^k\int_\theta^{+\infty}x^{-k}\,\mathrm{d}x=\frac{k}{k-1}\theta.
$$

故

$$
E\left(T_1\right)=E\left[\frac{k-1}{2k}\left(X_1+X_2\right)\right]=\frac{k-1}{2k}\cdot 2\cdot\frac{k}{k-1}\theta=\theta.
$$

记 $X_{\left(1\right)}=\min\left\{X_1,X_2\right\}$，由独立性，对 $x>\theta$，

$$
P\left(X_{\left(1\right)}>x\right)=\left[P\left(X_1>x\right)\right]^2=\left(\frac{\theta}{x}\right)^{2k},
$$

故 $X_{\left(1\right)}$ 的密度函数为 $2k\theta^{2k}x^{-\left(2k+1\right)}$，从而

$$
E\left(X_{\left(1\right)}\right)=\int_\theta^{+\infty}x\cdot 2k\theta^{2k}x^{-\left(2k+1\right)}\,\mathrm{d}x=\frac{2k}{2k-1}\theta.
$$

于是

$$
E\left(T_2\right)=E\left[\frac{2k-1}{2k}X_{\left(1\right)}\right]=\frac{2k-1}{2k}\cdot\frac{2k}{2k-1}\theta=\theta.
$$

由**定义 3.4.1**（无偏估计），$T_1$ 与 $T_2$ 都是 $\theta$ 的无偏估计.

(2) 再比较方差. 由

$$
E\left(X^2\right)=\int_\theta^{+\infty}x^2\cdot k\theta^k x^{-\left(k+1\right)}\,\mathrm{d}x=\frac{k}{k-2}\theta^2,
$$

得

$$
D\left(X\right)=E\left(X^2\right)-\left[E\left(X\right)\right]^2=\frac{k}{k-2}\theta^2-\frac{k^2}{\left(k-1\right)^2}\theta^2=\frac{k\theta^2}{\left(k-1\right)^2\left(k-2\right)}.
$$

故

$$
D\left(T_1\right)=\left(\frac{k-1}{2k}\right)^2\cdot 2D\left(X\right)=\frac{\left(k-1\right)^2}{4k^2}\cdot\frac{2k\theta^2}{\left(k-1\right)^2\left(k-2\right)}=\frac{\theta^2}{2k\left(k-2\right)}.
$$

又

$$
E\left(X_{\left(1\right)}^2\right)=\int_\theta^{+\infty}x^2\cdot 2k\theta^{2k}x^{-\left(2k+1\right)}\,\mathrm{d}x=\frac{2k}{2k-2}\theta^2=\frac{k}{k-1}\theta^2,
$$

故

$$
D\left(T_2\right)=\left(\frac{2k-1}{2k}\right)^2\left[E\left(X_{\left(1\right)}^2\right)-\left(E\left(X_{\left(1\right)}\right)\right)^2\right]=\frac{\theta^2}{4k\left(k-1\right)}.
$$

因 $4k\left(k-1\right)>2k\left(k-2\right)$（$k>2$），即 $D\left(T_2\right)<D\left(T_1\right)$. 由**定义 3.4.2**（有效性），$T_2$ 比 $T_1$ 有效.

$\blacksquare$

### 习题四

（习题 3.4-10）设 $\hat\theta_n$ 是 $\theta$ 的估计量，证明：若 $n\to+\infty$ 时，$E\left(\hat\theta_n\right)\to\theta$，$D\left(\hat\theta_n\right)\to0$，则 $\hat\theta_n$ 是 $\theta$ 的相合估计.

### 解答 习题四

由**基础知识**（切比雪夫不等式），对任意 $\varepsilon>0$，

$$
P\left\{\left|\hat\theta_n-\theta\right|\ge\varepsilon\right\}\le\frac{E\left[\left(\hat\theta_n-\theta\right)^2\right]}{\varepsilon^2}.
$$

将均方误差分解为方差与偏差平方之和：

$$
E\left[\left(\hat\theta_n-\theta\right)^2\right]=D\left(\hat\theta_n\right)+\left[E\left(\hat\theta_n\right)-\theta\right]^2.
$$

由题设 $E\left(\hat\theta_n\right)\to\theta$，$D\left(\hat\theta_n\right)\to0$，故 $E\left[\left(\hat\theta_n-\theta\right)^2\right]\to0$，从而

$$
\lim_{n\to\infty}P\left\{\left|\hat\theta_n-\theta\right|\ge\varepsilon\right\}=0.
$$

由**定义 3.4.3**（相合估计），$\hat\theta_n$ 是 $\theta$ 的相合估计.

$\blacksquare$

### 习题五

（习题 3.4-12）设 $X_1,X_2,\dots,X_n$ 是来自均匀分布 $U\left[0,\theta\right]$，$\theta>0$ 的样本，证明 $\sqrt[n]{X_1X_2\cdots X_n}$ 为 $\theta/e$ 的相合估计.

### 解答 习题五

令 $U_i=\frac{X_i}{\theta}$，则 $U_1,U_2,\dots,U_n$ 相互独立且均服从 $U\left[0,1\right]$. 对 $U\sim U\left[0,1\right]$，

$$
E\left[\ln U\right]=\int_0^1\ln u\,\mathrm{d}u=\left[u\ln u-u\right]_0^1=-1.
$$

记 $Z_i=\ln U_i$，则 $Z_1,Z_2,\dots,Z_n$ 相互独立，$E\left(Z_i\right)=-1$. 由**基础知识**（大数定律），

$$
\frac{1}{n}\sum_{i=1}^n Z_i\xrightarrow{P}-1.
$$

而

$$
\frac{1}{n}\sum_{i=1}^n\ln X_i=\ln\theta+\frac{1}{n}\sum_{i=1}^n\ln U_i=\ln\theta+\frac{1}{n}\sum_{i=1}^n Z_i\xrightarrow{P}\ln\theta-1=\ln\frac{\theta}{e}.
$$

由依概率收敛经连续函数映射保持不变，

$$
\sqrt[n]{X_1X_2\cdots X_n}=\exp\left(\frac{1}{n}\sum_{i=1}^n\ln X_i\right)\xrightarrow{P}\exp\left(\ln\frac{\theta}{e}\right)=\frac{\theta}{e}.
$$

由**定义 3.4.3**（相合估计），$\sqrt[n]{X_1X_2\cdots X_n}$ 是 $\theta/e$ 的相合估计.

$\blacksquare$
