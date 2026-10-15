# 作业 7

> **定义 2.6.1**（完备统计量）<br>设 $\mathcal{F}=\left\{f\left(x;\theta\right),\theta\in\Theta\right\}$ 为一分布族，其中 $\Theta$ 为参数空间. 设 $T=T\left(X_1,X_2,\dots,X_n\right)$ 为一统计量，若对任何满足 $E\left[\Phi\left(T\left(X_1,X_2,\dots,X_n\right)\right)\right]=0$ 对一切 $\theta\in\Theta$ 的 $\Phi\left(\cdot\right)$，都有 $P_\theta\left\{\Phi\left(T\left(X_1,X_2,\dots,X_n\right)\right)=0\right\}=1$ 对一切 $\theta\in\Theta$，则称 $T\left(X_1,X_2,\dots,X_n\right)$ 为完备统计量，或完全统计量. 若 $T$ 为完备统计量，则它的任一可测函数 $g\left(T\right)$ 也是完备统计量.

> **定理 2.6.1**（指数族中统计量的完备性）<br>设 $X_1,X_2,\dots,X_n$ 是从如下指数族（自然形式）中抽取的样本：$$f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k\theta_i T_i\left(x\right)\right\}h\left(x\right),\quad \theta=\left(\theta_1,\theta_2,\dots,\theta_k\right)\in\Theta^*\subseteq\mathbb R^k,$$ 若其自然参数空间 $\Theta^*$ 有内点，则 $T\left(X_1,X_2,\dots,X_n\right)=\left(T_1\left(X_1,\dots,X_n\right),\dots,T_k\left(X_1,\dots,X_n\right)\right)$ 为完备统计量.

> **定理 2.5.1**（因子分解定理）<br>设样本 $X_1,X_2,\dots,X_n$ 的联合密度函数（或联合分布列）为 $f\left(x_1,x_2,\dots,x_n;\theta\right)$，$T=T\left(X_1,X_2,\dots,X_n\right)$ 是一个统计量，则 $T$ 为充分统计量的充要条件是 $f\left(x_1,x_2,\dots,x_n;\theta\right)$ 可以分解为 $$f\left(x_1,x_2,\dots,x_n;\theta\right)=g\left(T\left(x_1,x_2,\dots,x_n\right),\theta\right)h\left(x_1,x_2,\dots,x_n\right),$$ 其中 $h\left(x_1,x_2,\dots,x_n\right)$ 不依赖于参数 $\theta$.

### 习题一

（习题 2.6-1）设 $X_1,X_2,\dots,X_n$ 是来自泊松分布总体 $P\left(\lambda\right)$，$\lambda>0$ 的样本，证明 $\sum_{i=1}^n X_i$ 为完备统计量.

### 解答 习题一

由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 相互独立且每个 $X_i\sim P\left(\lambda\right)$. 样本的联合分布列为

$$
f\left(x_1,x_2,\dots,x_n;\lambda\right)=\prod_{i=1}^n\frac{e^{-\lambda}\lambda^{x_i}}{x_i!}=e^{-n\lambda}\lambda^{\sum_{i=1}^n x_i}\prod_{i=1}^n\frac{1}{x_i!}.
$$

令自然参数 $\eta=\ln\lambda$，则 $\lambda=e^{\eta}$，上式化为指数族的自然形式

$$
f\left(x_1,x_2,\dots,x_n;\eta\right)=e^{-ne^{\eta}}\exp\left\{\eta\sum_{i=1}^n x_i\right\}\prod_{i=1}^n\frac{1}{x_i!}=C\left(\eta\right)\exp\left\{\eta T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

其中 $T=\sum_{i=1}^n x_i$，$h=\prod_{i=1}^n\frac{1}{x_i!}$ 不依赖于参数. 由于 $\lambda>0$，自然参数 $\eta=\ln\lambda\in\left(-\infty,+\infty\right)$，其自然参数空间有内点. 由**定理 2.6.1**（指数族中统计量的完备性），$T=\sum_{i=1}^n X_i$ 为完备统计量. $\blacksquare$

### 习题二

（习题 2.6-5）设 $X_1,X_2,\dots,X_n$ 是来自瑞利分布的样本，其密度函数为

$$
f\left(x\right)=\begin{cases}2\theta x e^{-\theta x^2},&x>0,\\0,&\text{其他},\end{cases}
$$

其中 $\theta>0$. 试给出一个完备统计量.

### 解答 习题二

由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 相互独立且同分布，样本的联合密度函数为

$$
f\left(x_1,x_2,\dots,x_n;\theta\right)=\prod_{i=1}^n 2\theta x_i e^{-\theta x_i^2}=\left(2\theta\right)^n\exp\left\{-\theta\sum_{i=1}^n x_i^2\right\}\prod_{i=1}^n x_i.
$$

令自然参数 $\eta=-\theta$，上式化为指数族的自然形式

$$
f\left(x_1,x_2,\dots,x_n;\eta\right)=\left(-2\eta\right)^n\exp\left\{\eta\sum_{i=1}^n x_i^2\right\}\prod_{i=1}^n x_i=C\left(\eta\right)\exp\left\{\eta T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

其中 $T=\sum_{i=1}^n x_i^2$，$h=\prod_{i=1}^n x_i$ 不依赖于参数. 由于 $\theta>0$，自然参数 $\eta=-\theta\in\left(-\infty,0\right)$，其自然参数空间有内点. 由**定理 2.6.1**（指数族中统计量的完备性），$T=\sum_{i=1}^n X_i^2$ 为完备统计量，故可取完备统计量为 $T=\sum_{i=1}^n X_i^2$. $\blacksquare$

### 习题三

（习题 2.6-6）设 $X_1,X_2,\dots,X_n$ 是来自指数分布 $E\left(\lambda\right)$ 的样本，其密度函数为

$$
f\left(x\right)=\begin{cases}\lambda e^{-\lambda x},&x>0,\\0,&x\le 0,\end{cases}
$$

其中 $\lambda>0$. 证明 $\sum_{i=1}^n X_i$ 为完备统计量.

### 解答 习题三

由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 相互独立且同分布，样本的联合密度函数为

$$
f\left(x_1,x_2,\dots,x_n;\lambda\right)=\prod_{i=1}^n\lambda e^{-\lambda x_i}=\lambda^n\exp\left\{-\lambda\sum_{i=1}^n x_i\right\}.
$$

令自然参数 $\eta=-\lambda$，上式化为指数族的自然形式

$$
f\left(x_1,x_2,\dots,x_n;\eta\right)=\left(-\eta\right)^n\exp\left\{\eta\sum_{i=1}^n x_i\right\}=C\left(\eta\right)\exp\left\{\eta T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

其中 $T=\sum_{i=1}^n x_i$，$h=1$ 不依赖于参数. 由于 $\lambda>0$，自然参数 $\eta=-\lambda\in\left(-\infty,0\right)$，其自然参数空间有内点. 由**定理 2.6.1**（指数族中统计量的完备性），$T=\sum_{i=1}^n X_i$ 为完备统计量. $\blacksquare$

### 习题四

（习题 2.6-7）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本.

(1) 在 $\mu$ 已知时，给出 $\sigma^2$ 的一个完备统计量；

(2) 在 $\sigma^2$ 已知时，给出 $\mu$ 的一个完备统计量.

### 解答 习题四

由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 相互独立且每个 $X_i\sim N\left(\mu,\sigma^2\right)$，样本的联合密度函数为

$$
f\left(x_1,x_2,\dots,x_n;\mu,\sigma^2\right)=\left(2\pi\sigma^2\right)^{-\frac{n}{2}}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2\right\}.
$$

(1) 在 $\mu$ 已知时，将联合密度写为关于 $\sigma^2$ 的指数族自然形式：

$$
f=C\left(\sigma^2\right)\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2\right\}.
$$

令自然参数 $\eta=-\frac{1}{2\sigma^2}$，则 $T=\sum_{i=1}^n\left(x_i-\mu\right)^2$. 由于 $\sigma^2>0$，自然参数 $\eta\in\left(-\infty,0\right)$ 有内点. 由**定理 2.6.1**（指数族中统计量的完备性），$T=\sum_{i=1}^n\left(X_i-\mu\right)^2$ 为 $\sigma^2$ 的一个完备统计量.

(2) 在 $\sigma^2$ 已知时，展开指数部分：

$$
-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2=-\frac{1}{2\sigma^2}\sum_{i=1}^n x_i^2+\frac{\mu}{\sigma^2}\sum_{i=1}^n x_i-\frac{n\mu^2}{2\sigma^2},
$$

其中与 $x_i$ 有关的项除 $\frac{\mu}{\sigma^2}\sum_{i=1}^n x_i$ 外均归入 $C\left(\mu,\sigma^2\right)$，故

$$
f=C'\left(\mu,\sigma^2\right)\exp\left\{\frac{\mu}{\sigma^2}\sum_{i=1}^n x_i\right\}.
$$

令自然参数 $\eta=\frac{\mu}{\sigma^2}$，则 $T=\sum_{i=1}^n x_i$. 由于 $\mu\in\mathbb R$，自然参数 $\eta\in\left(-\infty,+\infty\right)$ 有内点. 由**定理 2.6.1**（指数族中统计量的完备性），$T=\sum_{i=1}^n X_i$ 为 $\mu$ 的一个完备统计量（等价地，样本均值 $\bar X$ 也是）. $\blacksquare$

### 习题五

（习题 2.6-10）设 $X_1,X_2,\dots,X_n$ 是来自均匀分布总体 $U\left[\theta,2\theta\right]$，$\theta>0$ 的样本，证明 $\left(X_{\left(1\right)},X_{\left(n\right)}\right)$ 是充分统计量但不是完备统计量.

### 解答 习题五

先证充分性. 样本的联合密度函数为

$$
f\left(x_1,x_2,\dots,x_n;\theta\right)=\prod_{i=1}^n\frac{1}{\theta}\mathbf 1\left\{\theta\le x_i\le 2\theta\right\}=\theta^{-n}\mathbf 1\left\{\theta\le X_{\left(1\right)},\ X_{\left(n\right)}\le 2\theta\right\}.
$$

它已分解为 $f=g\left(T\left(x_1,\dots,x_n\right),\theta\right)h\left(x_1,\dots,x_n\right)$，其中 $T=\left(X_{\left(1\right)},X_{\left(n\right)}\right)$，$g=\theta^{-n}\mathbf 1\left\{\theta\le X_{\left(1\right)},\ X_{\left(n\right)}\le 2\theta\right\}$，$h=1$ 不依赖于 $\theta$. 由**定理 2.5.1**（因子分解定理），$\left(X_{\left(1\right)},X_{\left(n\right)}\right)$ 是充分统计量.

再证其不完备. 令 $Y_i=\frac{X_i-\theta}{\theta}$，则 $Y_1,Y_2,\dots,Y_n$ 独立同分布于 $U\left[0,1\right]$，且 $X_{\left(1\right)}=\theta\left(1+Y_{\left(1\right)}\right)$，$X_{\left(n\right)}=\theta\left(1+Y_{\left(n\right)}\right)$. 对 $U\left[0,1\right]$ 的顺序统计量，由其密度积分可得 $E\left[Y_{\left(1\right)}\right]=\frac{1}{n+1}$，$E\left[Y_{\left(n\right)}\right]=\frac{n}{n+1}$，故

$$
E\left[X_{\left(1\right)}\right]=\theta\left(1+\frac{1}{n+1}\right)=\frac{\theta\left(n+2\right)}{n+1},\quad E\left[X_{\left(n\right)}\right]=\theta\left(1+\frac{n}{n+1}\right)=\frac{\theta\left(2n+1\right)}{n+1}.
$$

取统计量 $T=\left(X_{\left(1\right)},X_{\left(n\right)}\right)$ 的函数

$$
\Phi\left(T\right)=\left(n+2\right)X_{\left(n\right)}-\left(2n+1\right)X_{\left(1\right)},
$$

则对一切 $\theta>0$，

$$
E\left[\Phi\left(T\right)\right]=\left(n+2\right)\frac{\theta\left(2n+1\right)}{n+1}-\left(2n+1\right)\frac{\theta\left(n+2\right)}{n+1}=0.
$$

但 $\Phi\left(T\right)$ 并不几乎处处为零（它随样本观测而变化，不恒等于 $0$）. 由**定义 2.6.1**（完备统计量），存在这样的非零函数 $\Phi\left(T\right)$ 使 $E\left[\Phi\left(T\right)\right]=0$ 对一切 $\theta$ 成立，故 $\left(X_{\left(1\right)},X_{\left(n\right)}\right)$ 不是完备统计量. $\blacksquare$
