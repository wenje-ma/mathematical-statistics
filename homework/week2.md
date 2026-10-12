# 作业 2

> **抽样分布**（定义）<br>统计量是样本 $X_1,X_2,\dots,X_n$ 的函数，而样本 $X_1,X_2,\dots,X_n$ 是随机变量. 因此，统计量也是随机变量，统计量的分布称为抽样分布.

> **定理**（顺序统计量的分布）<br>设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，且 $X$ 的分布函数为 $F\left(x\right)$，$\left(X_{\left(1\right)},X_{\left(2\right)},\dots,X_{\left(n\right)}\right)$ 是其顺序统计量，则对 $1\le r\le n$，$X_{\left(r\right)}$ 的分布函数为 $$F_{\left(r\right)}\left(x\right)=P\left\{X_{\left(r\right)}\le x\right\}=\sum_{k=r}^n\binom{n}{k}\left[F\left(x\right)\right]^k\left[1-F\left(x\right)\right]^{n-k}=r\binom{n}{r}\int_0^{F\left(x\right)}t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t.$$ 若总体 $X$ 为连续型且有密度函数 $f\left(x\right)$，则 $X_{\left(r\right)}$ 的密度函数为 $$f_{\left(r\right)}\left(x\right)=F_{\left(r\right)}'\left(x\right)=r\binom{n}{r}\left[F\left(x\right)\right]^{r-1}\left[1-F\left(x\right)\right]^{n-r}f\left(x\right).$$ 特别地，当 $r=1$ 时，最小顺序统计量 $X_{\left(1\right)}$ 的分布函数和密度函数分别为 $$F_{\left(1\right)}\left(x\right)=1-\left[1-F\left(x\right)\right]^n,\qquad f_{\left(1\right)}\left(x\right)=n\left[1-F\left(x\right)\right]^{n-1}f\left(x\right);$$ 当 $r=n$ 时，最大顺序统计量 $X_{\left(n\right)}$ 的分布函数和密度函数分别为 $$F_{\left(n\right)}\left(x\right)=\left[F\left(x\right)\right]^n,\qquad f_{\left(n\right)}\left(x\right)=n\left[F\left(x\right)\right]^{n-1}f\left(x\right).$$

> **基础知识**（泊松分布的可加性）<br>设 $X_1,X_2,\dots,X_n$ 相互独立，且 $X_i\sim P\left(\lambda_i\right)$，则 $\sum_{i=1}^n X_i\sim P\left(\sum_{i=1}^n\lambda_i\right)$.

> **基础知识**（正态分布的可加性）<br>设 $X_1,X_2,\dots,X_n$ 相互独立，且 $X_i\sim N\left(\mu_i,\sigma_i^2\right)$，则 $\sum_{i=1}^n X_i\sim N\left(\sum_{i=1}^n\mu_i,\sum_{i=1}^n\sigma_i^2\right)$.

### 习题一

（习题 2.1-1）设 $X_1,X_2,\dots,X_n$ 是来自泊松分布总体 $P\left(\lambda\right)$ 的样本，其分布列为 $P\left\{X=x\right\}=\frac{\lambda^x}{x!}e^{-\lambda},\ x=0,1,2,\dots$，其中 $\lambda>0$. 求 $T=\sum_{i=1}^n X_i$ 的抽样分布.

### 解答 习题一

由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 相互独立且每个 $X_i\sim P\left(\lambda\right)$. 由**基础知识**（泊松分布的可加性），独立泊松变量之和仍服从泊松分布，且参数相加，故
$$
T=\sum_{i=1}^n X_i\sim P\left(n\lambda\right).
$$

即 $T$ 的分布列为
$$
P\left\{T=t\right\}=\frac{\left(n\lambda\right)^t}{t!}e^{-n\lambda},\qquad t=0,1,2,\dots
$$

$\blacksquare$

### 习题二

（习题 2.1-2）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$，$\mu\in\mathbb R,\ \sigma^2>0$ 的样本，求 $T=\sum_{i=1}^n X_i$ 的抽样分布.

### 解答 习题二

由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 相互独立且每个 $X_i\sim N\left(\mu,\sigma^2\right)$. 由**基础知识**（正态分布的可加性），独立正态变量之和仍服从正态分布，且均值和方差分别相加，故
$$
T=\sum_{i=1}^n X_i\sim N\left(n\mu,n\sigma^2\right).
$$

$\blacksquare$

### 习题三

（习题 2.1-3）设 $X\sim B\left(n,p\right)$，$0<p<1$，对 $r\ge1$，证明：
$$
P\left\{X\ge r\right\}=\sum_{k=r}^n\binom{n}{k}p^k\left(1-p\right)^{n-k}=r\binom{n}{r}\int_0^p t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t.
$$

### 解答 习题三

记 $G\left(p\right)=\sum_{k=r}^n\binom{n}{k}p^k\left(1-p\right)^{n-k}$，其中 $r\ge1$. 对 $p$ 求导，得
$$
G'\left(p\right)=\sum_{k=r}^n\binom{n}{k}\left[kp^{k-1}\left(1-p\right)^{n-k}-\left(n-k\right)p^k\left(1-p\right)^{n-k-1}\right].
$$

利用恒等式 $k\binom{n}{k}=n\binom{n-1}{k-1}$ 与 $\left(n-k\right)\binom{n}{k}=n\binom{n-1}{k}$，上式化为
$$
G'\left(p\right)=\sum_{k=r}^n n\binom{n-1}{k-1}p^{k-1}\left(1-p\right)^{n-k}-\sum_{k=r}^n n\binom{n-1}{k}p^k\left(1-p\right)^{n-k-1}.
$$

第一项令 $j=k-1$，则 $j$ 从 $r-1$ 到 $n-1$；第二项令 $j=k$，则 $j$ 从 $r$ 到 $n$. 两式除首项 $j=r-1$ 外逐项相消，故
$$
G'\left(p\right)=n\binom{n-1}{r-1}p^{r-1}\left(1-p\right)^{n-r}=r\binom{n}{r}p^{r-1}\left(1-p\right)^{n-r},
$$

其中用到了 $n\binom{n-1}{r-1}=r\binom{n}{r}$. 又因 $r\ge1$，$G\left(0\right)=\sum_{k=r}^n\binom{n}{k}0^k\cdot1=0$，故由牛顿—莱布尼茨公式，
$$
G\left(p\right)=\int_0^p G'\left(t\right)\,\mathrm{d}t=r\binom{n}{r}\int_0^p t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t.
$$

即 $P\left\{X\ge r\right\}=\sum_{k=r}^n\binom{n}{k}p^k\left(1-p\right)^{n-k}=r\binom{n}{r}\int_0^p t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t$. $\blacksquare$

### 习题四

（习题 2.1-5）设 $X_1,X_2,\dots,X_n$ 是来自指数分布总体 $E\left(\lambda\right)$ 的样本，其密度函数为
$$
f\left(x\right)=\begin{cases}\lambda e^{-\lambda x},&x>0,\\0,&x\le0,\end{cases}
$$
其中 $\lambda>0$. 求：

(1) $X_{\left(1\right)}$ 的密度函数；

(2) $E\left(X_{\left(1\right)}\right),D\left(X_{\left(1\right)}\right)$.

### 解答 习题四

指数分布 $E\left(\lambda\right)$ 的分布函数为 $F\left(x\right)=1-e^{-\lambda x}\left(x>0\right)$，密度函数为 $f\left(x\right)=\lambda e^{-\lambda x}\left(x>0\right)$.

(1) 由**定理**（顺序统计量的分布），最小顺序统计量 $X_{\left(1\right)}$ 的密度函数为
$$
f_{\left(1\right)}\left(x\right)=n\left[1-F\left(x\right)\right]^{n-1}f\left(x\right)=n\left(e^{-\lambda x}\right)^{n-1}\cdot\lambda e^{-\lambda x}=n\lambda e^{-n\lambda x},\qquad x>0.
$$

故 $X_{\left(1\right)}\sim E\left(n\lambda\right)$，即 $X_{\left(1\right)}$ 服从参数为 $n\lambda$ 的指数分布.

(2) 由指数分布的期望与方差公式，$E\left(X_{\left(1\right)}\right)=\frac{1}{n\lambda}$，$D\left(X_{\left(1\right)}\right)=\frac{1}{\left(n\lambda\right)^2}$. $\blacksquare$

### 习题五

（习题 2.1-6）设 $X_1,X_2,\dots,X_9$ 是来自正态总体 $N\left(1,9\right)$ 的样本，求：

(1) $P\left\{X_{\left(1\right)}>4\right\}$；

(2) $P\left\{X_{\left(9\right)}<4\right\}$.

### 解答 习题五

总体 $X\sim N\left(1,9\right)$，故 $X$ 的分布函数为 $F\left(x\right)=\Phi\left(\frac{x-1}{3}\right)$，其中 $\Phi$ 为标准正态分布函数.

(1) $X_{\left(1\right)}=\min\left\{X_1,\dots,X_9\right\}$，故 $X_{\left(1\right)}>4$ 当且仅当每个 $X_i>4$. 由**定义 1.3.2**（简单随机样本），$X_1,\dots,X_9$ 相互独立且同分布，故
$$
P\left\{X_{\left(1\right)}>4\right\}=P\left\{X_1>4,\dots,X_9>4\right\}=\left[P\left\{X_1>4\right\}\right]^9=\left[1-F\left(4\right)\right]^9=\left[1-\Phi\left(1\right)\right]^9.
$$

(2) $X_{\left(9\right)}=\max\left\{X_1,\dots,X_9\right\}$，故 $X_{\left(9\right)}<4$ 当且仅当每个 $X_i<4$. 由独立性，
$$
P\left\{X_{\left(9\right)}<4\right\}=P\left\{X_1<4,\dots,X_9<4\right\}=\left[F\left(4\right)\right]^9=\left[\Phi\left(1\right)\right]^9.
$$

$\blacksquare$

### 习题六

（习题 2.1-7）设 $X_1,X_2,\dots,X_n$ 是来自均匀分布总体 $U\left[\theta_1,\theta_2\right]$，$\theta_1<\theta_2$ 的样本，分别求顺序统计量 $X_{\left(1\right)},X_{\left(n\right)}$ 的密度函数.

### 解答 习题六

均匀分布 $U\left[\theta_1,\theta_2\right]$ 的密度函数与分布函数分别为
$$
f\left(x\right)=\begin{cases}\frac{1}{\theta_2-\theta_1},&\theta_1\le x\le\theta_2,\\0,&\text{其他},\end{cases}\qquad F\left(x\right)=\begin{cases}0,&x<\theta_1,\\\frac{x-\theta_1}{\theta_2-\theta_1},&\theta_1\le x\le\theta_2,\\1,&x>\theta_2.\end{cases}
$$

由**定理**（顺序统计量的分布），最小顺序统计量 $X_{\left(1\right)}$ 的密度函数为
$$
f_{\left(1\right)}\left(x\right)=n\left[1-F\left(x\right)\right]^{n-1}f\left(x\right)=n\left(\frac{\theta_2-x}{\theta_2-\theta_1}\right)^{n-1}\cdot\frac{1}{\theta_2-\theta_1}=\frac{n\left(\theta_2-x\right)^{n-1}}{\left(\theta_2-\theta_1\right)^n},\qquad \theta_1\le x\le\theta_2.
$$

最大顺序统计量 $X_{\left(n\right)}$ 的密度函数为
$$
f_{\left(n\right)}\left(x\right)=n\left[F\left(x\right)\right]^{n-1}f\left(x\right)=n\left(\frac{x-\theta_1}{\theta_2-\theta_1}\right)^{n-1}\cdot\frac{1}{\theta_2-\theta_1}=\frac{n\left(x-\theta_1\right)^{n-1}}{\left(\theta_2-\theta_1\right)^n},\qquad \theta_1\le x\le\theta_2.
$$

$\blacksquare$
