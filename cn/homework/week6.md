# 作业 6

> **定义 2.5.1**（充分统计量）<br>设样本 $X_1,X_2,\dots,X_n$ 的分布族为 $f\left(x_1,x_2,\dots,x_n,\theta\right)$，$\theta\in\Theta$，$\Theta$ 是参数空间. 设 $T=T\left(X_1,X_2,\dots,X_n\right)$ 为一统计量，若在给定 $T$ 的条件下，样本 $X_1,X_2,\dots,X_n$ 的条件分布与参数 $\theta$ 无关，则称统计量 $T\left(X_1,X_2,\dots,X_n\right)$ 为参数 $\theta$ 的充分统计量.

> **定理 2.5.1**（因子分解定理）<br>设样本 $X_1,X_2,\dots,X_n$ 的联合密度函数（或联合分布列）为 $f\left(x_1,x_2,\dots,x_n,\theta\right)$，依赖于参数 $\theta$，$T=T\left(X_1,X_2,\dots,X_n\right)$ 是一个统计量，则 $T$ 是充分统计量的充要条件是 $f\left(x_1,x_2,\dots,x_n,\theta\right)$ 可以分解为 $$f\left(x_1,x_2,\dots,x_n,\theta\right)=g\left(T\left(x_1,x_2,\dots,x_n\right),\theta\right)h\left(x_1,\dots,x_n\right),$$ 其中 $h\left(x_1,\dots,x_n\right)$ 不依赖于参数 $\theta$.

> **推论 2.5.1**<br>设 $T=T\left(X_1,X_2,\dots,X_n\right)$ 为 $\theta$ 的充分统计量，$S\left(T\right)$ 是单值可逆函数，则 $S\left(T\right)$ 也是 $\theta$ 的充分统计量.

### 习题一

（习题 2.5-1）设 $X_1,X_2,\dots,X_n$ 是来自泊松分布总体 $P\left(\lambda\right)$，$\lambda>0$ 的样本，

(1) 分别用定义法和因子分解定理法证明 $\sum_{i=1}^n X_i$ 为充分统计量；

(2) 若 $n=2$，则 $X_1+2X_2$ 不是充分统计量.

### 解答 习题一

泊松分布 $P\left(\lambda\right)$ 的分布列为 $P\left\{X=x\right\}=\frac{e^{-\lambda}\lambda^x}{x!},\ x=0,1,2,\dots$，其中 $\lambda>0$. 由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 相互独立且同分布.

(1) 证明 $T=\sum_{i=1}^n X_i$ 为充分统计量.

因子分解定理法：由**定理 2.5.1**（因子分解定理），样本的联合分布列为

$$
P\left(x_1,\dots,x_n,\lambda\right)=\prod_{i=1}^n\frac{e^{-\lambda}\lambda^{x_i}}{x_i!}=\frac{e^{-n\lambda}\lambda^{\sum_{i=1}^n x_i}}{\prod_{i=1}^n x_i!}.
$$

取 $g\left(T,\lambda\right)=e^{-n\lambda}\lambda^{\sum_{i=1}^n x_i}$，$h\left(x_1,\dots,x_n\right)=\frac{1}{\prod_{i=1}^n x_i!}$，其中 $h$ 不依赖于 $\lambda$，故 $T=\sum_{i=1}^n X_i$ 是 $\lambda$ 的充分统计量.

定义法：由**基础知识**（泊松分布的可加性），$T=\sum_{i=1}^n X_i\sim P\left(n\lambda\right)$，故 $P\left\{T=t\right\}=\frac{e^{-n\lambda}\left(n\lambda\right)^t}{t!}$. 在给定 $T=t$ 的条件下，当 $\sum_{i=1}^n x_i=t$ 时，

$$
P\left\{X_1=x_1,\dots,X_n=x_n\mid T=t\right\}=\frac{P\left\{X_1=x_1,\dots,X_n=x_n,\ T=t\right\}}{P\left\{T=t\right\}}=\frac{\prod_{i=1}^n\frac{e^{-\lambda}\lambda^{x_i}}{x_i!}}{\frac{e^{-n\lambda}\left(n\lambda\right)^t}{t!}}=\frac{t!}{n^t\prod_{i=1}^n x_i!}.
$$

该条件分布列与参数 $\lambda$ 无关，故由**定义 2.5.1**（充分统计量），$T=\sum_{i=1}^n X_i$ 是 $\lambda$ 的充分统计量.

(2) 当 $n=2$ 时，证明 $X_1+2X_2$ 不是充分统计量.

记 $T'=X_1+2X_2$. 取 $t=2$，则 $\left(X_1,X_2\right)$ 满足 $X_1+2X_2=2$ 的情形有两种：$\left(2,0\right)$ 和 $\left(0,1\right)$. 在给定 $T'=2$ 的条件下，

$$
P\left\{X_1=2,X_2=0\mid T'=2\right\}=\frac{P\left\{X_1=2,X_2=0\right\}}{P\left\{T'=2\right\}}=\frac{\frac{e^{-\lambda}\lambda^2}{2!}\cdot e^{-\lambda}}{\frac{e^{-\lambda}\lambda^2}{2!}\cdot e^{-\lambda}+e^{-\lambda}\cdot\frac{e^{-\lambda}\lambda}{1!}}=\frac{\frac{\lambda^2}{2}}{\frac{\lambda^2}{2}+\lambda}=\frac{\lambda}{\lambda+2}.
$$

该条件概率与参数 $\lambda$ 有关，故由**定义 2.5.1**（充分统计量），$X_1+2X_2$ 不是 $\lambda$ 的充分统计量.

$\blacksquare$

### 习题二

（习题 2.5-5）设 $X_1,X_2,\dots,X_n$ 是来自瑞利分布的样本，其密度函数为

$$
f\left(x\right)=\begin{cases}2\theta x e^{-\theta x^2},&x>0,\\0,&\text{其他},\end{cases}
$$

其中 $\theta>0$. 试给出一个充分统计量.

### 解答 习题二

由**定义 1.3.2**（简单随机样本），样本的联合密度函数为

$$
f\left(x_1,\dots,x_n,\theta\right)=\prod_{i=1}^n 2\theta x_i e^{-\theta x_i^2}=\left(2\theta\right)^n\exp\left\{-\theta\sum_{i=1}^n x_i^2\right\}\cdot\prod_{i=1}^n x_i.
$$

取 $g\left(T,\theta\right)=\left(2\theta\right)^n\exp\left\{-\theta\sum_{i=1}^n x_i^2\right\}$，$h\left(x_1,\dots,x_n\right)=\prod_{i=1}^n x_i$，其中 $h$ 不依赖于 $\theta$. 由**定理 2.5.1**（因子分解定理），$T=\sum_{i=1}^n X_i^2$ 是 $\theta$ 的充分统计量.

$\blacksquare$

### 习题三

（习题 2.5-6）设 $X_1,X_2,\dots,X_n$ 是来自指数分布 $E\left(\lambda\right)$ 的样本，其密度函数为

$$
f\left(x\right)=\begin{cases}\lambda e^{-\lambda x},&x>0,\\0,&x\le0,\end{cases}
$$

其中 $\lambda>0$. 证明 $\sum_{i=1}^n X_i$ 是充分统计量.

### 解答 习题三

由**定义 1.3.2**（简单随机样本），样本的联合密度函数为

$$
f\left(x_1,\dots,x_n,\lambda\right)=\prod_{i=1}^n\lambda e^{-\lambda x_i}=\lambda^n\exp\left\{-\lambda\sum_{i=1}^n x_i\right\}.
$$

取 $g\left(T,\lambda\right)=\lambda^n\exp\left\{-\lambda\sum_{i=1}^n x_i\right\}$，$h\left(x_1,\dots,x_n\right)=1$，其中 $h$ 不依赖于 $\lambda$. 由**定理 2.5.1**（因子分解定理），$T=\sum_{i=1}^n X_i$ 是 $\lambda$ 的充分统计量.

$\blacksquare$

### 习题四

（习题 2.5-7）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，

(1) 在 $\mu$ 已知时，给出 $\sigma^2$ 的一个充分统计量；

(2) 在 $\sigma^2$ 已知时，给出 $\mu$ 的一个充分统计量.

### 解答 习题四

由**定义 1.3.2**（简单随机样本），样本的联合密度函数为

$$
f\left(x_1,\dots,x_n,\mu,\sigma^2\right)=\left(2\pi\sigma^2\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2\right\}.
$$

(1) $\mu$ 已知时，求 $\sigma^2$ 的充分统计量.

当 $\mu$ 已知时，上式中仅 $\sigma^2$ 为未知参数. 取 $g\left(T,\sigma^2\right)=\left(2\pi\sigma^2\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2\right\}$，$h=1$，其中 $h$ 不依赖于 $\sigma^2$. 由**定理 2.5.1**（因子分解定理），$T=\sum_{i=1}^n\left(X_i-\mu\right)^2$ 是 $\sigma^2$ 的充分统计量.

(2) $\sigma^2$ 已知时，求 $\mu$ 的充分统计量.

展开平方项：$\sum_{i=1}^n\left(x_i-\mu\right)^2=\sum_{i=1}^n x_i^2-2\mu\sum_{i=1}^n x_i+n\mu^2$，代入联合密度得

$$
f=\left(2\pi\sigma^2\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n x_i^2\right\}\cdot\exp\left\{\frac{\mu}{\sigma^2}\sum_{i=1}^n x_i-\frac{n\mu^2}{2\sigma^2}\right\}.
$$

当 $\sigma^2$ 已知时，取 $g\left(T,\mu\right)=\exp\left\{\frac{\mu}{\sigma^2}\sum_{i=1}^n x_i-\frac{n\mu^2}{2\sigma^2}\right\}$，$h\left(x_1,\dots,x_n\right)=\left(2\pi\sigma^2\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n x_i^2\right\}$，其中 $h$ 不依赖于 $\mu$. 由**定理 2.5.1**（因子分解定理），$T=\sum_{i=1}^n X_i$ 是 $\mu$ 的充分统计量. 由**推论 2.5.1**，$\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ 也是 $\mu$ 的充分统计量.

$\blacksquare$
