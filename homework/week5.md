# 作业 5

> **定义 2.4.1**（指数族）<br>设 $\mathcal{F}=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ 是定义在样本空间 $\mathcal{X}$ 上的分布族，其中 $\Theta$ 为参数空间. 若 $f\left(x,\theta\right)$ 可以表示为 $$f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k Q_i\left(\theta\right)T_i\left(x\right)\right\}h\left(x\right),$$ 则称此分布族为指数型分布族，简称指数族. 其中 $C\left(\theta\right)>0$ 和 $Q_i\left(\theta\right)$ 定义在参数空间 $\Theta$ 上，$h\left(x\right)>0$ 和 $T_i\left(x\right)$ 定义在样本空间 $\mathcal{X}$ 上，且支撑集 $\left\{x:f\left(x,\theta\right)>0\right\}$ 与 $\theta$ 无关.

> **定义 2.4.2**（指数族的自然形式）<br>如果指数族有下列形式 $$f\left(x,\varphi\right)=C\left(\varphi\right)\exp\left\{\sum_{i=1}^k\varphi_i T_i\left(x\right)\right\}h\left(x\right),$$ 则称其为指数族的自然形式，也称为标准形式. 集合 $$\Theta^{*}=\left\{\varphi=\left(\varphi_1,\dots,\varphi_k\right):\int\exp\left\{\sum_{i=1}^k\varphi_i T_i\left(x\right)\right\}h\left(x\right)\,\mathrm{d}x<+\infty\right\}$$ 称为自然参数空间.

### 习题一

（习题 2.4-3）设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，且 $X$ 的密度函数为

$$
f\left(x\right)=\begin{cases}\theta x^{\theta-1},&0<x<1,\\0,&\text{其他},\end{cases}
$$

其中 $\theta>0$. 证明样本分布族是指数族，并表示成指数族的自然形式，求出自然参数空间.

### 解答 习题一

由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 相互独立且与总体 $X$ 同分布，故样本的联合密度函数为

$$
f\left(x_1,x_2,\dots,x_n,\theta\right)=\prod_{i=1}^n\theta x_i^{\theta-1}=\theta^n\left(\prod_{i=1}^n x_i\right)^{\theta-1}=\theta^n\exp\left\{\left(\theta-1\right)\sum_{i=1}^n\ln x_i\right\}.
$$

将其改写为

$$
f\left(x_1,\dots,x_n,\theta\right)=\theta^n\exp\left\{\theta\sum_{i=1}^n\ln x_i\right\}\cdot\frac{1}{\prod_{i=1}^n x_i},\quad 0<x_i<1.
$$

取 $C\left(\theta\right)=\theta^n$，$Q\left(\theta\right)=\theta$，$T\left(x_1,\dots,x_n\right)=\sum_{i=1}^n\ln x_i$，$h\left(x_1,\dots,x_n\right)=\frac{1}{\prod_{i=1}^n x_i}$. 其支撑集 $\left\{x:f\left(x,\theta\right)>0\right\}=\left(0,1\right)$ 与 $\theta$ 无关，故由**定义 2.4.1**（指数族），该样本分布族是指数族.

令自然参数 $\varphi=\theta$，由**定义 2.4.2**（指数族的自然形式），自然形式为

$$
f\left(x_1,\dots,x_n,\varphi\right)=\varphi^n\exp\left\{\varphi\sum_{i=1}^n\ln x_i\right\}\frac{1}{\prod_{i=1}^n x_i}=C\left(\varphi\right)\exp\left\{\varphi T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

其中 $C\left(\varphi\right)=\varphi^n$. 自然参数空间满足

$$
\Theta^{*}=\left\{\varphi:\int_0^1\exp\left\{\varphi\ln x\right\}\cdot\frac{1}{x}\,\mathrm{d}x<+\infty\right\}=\left\{\varphi:\int_0^1 x^{\varphi-1}\,\mathrm{d}x<+\infty\right\}.
$$

由于 $\int_0^1 x^{\varphi-1}\mathrm{d}x=\frac{1}{\varphi}$ 当且仅当 $\varphi>0$ 时收敛，故自然参数空间为

$$
\Theta^{*}=\left(0,+\infty\right).
$$

$\blacksquare$

### 习题二

（习题 2.4-4）设 $X_1,X_2,\dots,X_n$ 是来自拉普拉斯（Laplace）分布的样本，其密度函数为

$$
f\left(x\right)=\frac{1}{2\theta}e^{-\left|x\right|/\theta},\quad-\infty<x<+\infty,\ \theta>0.
$$

证明样本分布族是指数族，并表示成指数族的自然形式，求出自然参数空间.

### 解答 习题二

由**定义 1.3.2**（简单随机样本），样本的联合密度函数为

$$
f\left(x_1,\dots,x_n,\theta\right)=\prod_{i=1}^n\frac{1}{2\theta}e^{-\left|x_i\right|/\theta}=\left(2\theta\right)^{-n}\exp\left\{-\frac{1}{\theta}\sum_{i=1}^n\left|x_i\right|\right\}.
$$

取 $C\left(\theta\right)=\left(2\theta\right)^{-n}$，$Q\left(\theta\right)=-\frac{1}{\theta}$，$T\left(x_1,\dots,x_n\right)=\sum_{i=1}^n\left|x_i\right|$，$h\left(x_1,\dots,x_n\right)=1$. 其支撑集为 $\left(-\infty,+\infty\right)$，与 $\theta$ 无关，故由**定义 2.4.1**（指数族），该样本分布族是指数族.

令自然参数 $\varphi=-\frac{1}{\theta}$，则 $\theta=-\frac{1}{\varphi}$，由**定义 2.4.2**（指数族的自然形式），自然形式为

$$
f\left(x_1,\dots,x_n,\varphi\right)=\left(-\frac{\varphi}{2}\right)^n\exp\left\{\varphi\sum_{i=1}^n\left|x_i\right|\right\}=C\left(\varphi\right)\exp\left\{\varphi T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

其中 $C\left(\varphi\right)=\left(-\frac{\varphi}{2}\right)^n$. 自然参数空间满足

$$
\Theta^{*}=\left\{\varphi:\int_{-\infty}^{+\infty}\exp\left\{\varphi\left|x\right|\right\}\,\mathrm{d}x<+\infty\right\}=\left\{\varphi:2\int_0^{+\infty}e^{\varphi x}\,\mathrm{d}x<+\infty\right\}.
$$

由于 $\int_0^{+\infty}e^{\varphi x}\mathrm{d}x=\frac{1}{-\varphi}$ 当且仅当 $\varphi<0$ 时收敛，故自然参数空间为

$$
\Theta^{*}=\left(-\infty,0\right).
$$

$\blacksquare$

### 习题三

（习题 2.4-5）设 $X_1,X_2,\dots,X_n$ 是来自瑞利（Rayleigh）分布的样本，其密度函数为

$$
f\left(x\right)=\begin{cases}2\theta x e^{-\theta x^2},&x>0,\\0,&\text{其他},\end{cases}
$$

其中 $\theta>0$. 证明样本分布族是指数族，并表示成指数族的自然形式，求出自然参数空间.

### 解答 习题三

由**定义 1.3.2**（简单随机样本），样本的联合密度函数为

$$
f\left(x_1,\dots,x_n,\theta\right)=\prod_{i=1}^n 2\theta x_i e^{-\theta x_i^2}=\left(2\theta\right)^n\left(\prod_{i=1}^n x_i\right)\exp\left\{-\theta\sum_{i=1}^n x_i^2\right\}.
$$

取 $C\left(\theta\right)=\left(2\theta\right)^n$，$Q\left(\theta\right)=-\theta$，$T\left(x_1,\dots,x_n\right)=\sum_{i=1}^n x_i^2$，$h\left(x_1,\dots,x_n\right)=\prod_{i=1}^n x_i$. 其支撑集为 $\left(0,+\infty\right)$，与 $\theta$ 无关，故由**定义 2.4.1**（指数族），该样本分布族是指数族.

令自然参数 $\varphi=-\theta$，则 $\theta=-\varphi$，由**定义 2.4.2**（指数族的自然形式），自然形式为

$$
f\left(x_1,\dots,x_n,\varphi\right)=\left(-2\varphi\right)^n\exp\left\{\varphi\sum_{i=1}^n x_i^2\right\}\prod_{i=1}^n x_i=C\left(\varphi\right)\exp\left\{\varphi T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

其中 $C\left(\varphi\right)=\left(-2\varphi\right)^n$. 自然参数空间满足

$$
\Theta^{*}=\left\{\varphi:\int_0^{+\infty}\exp\left\{\varphi x^2\right\}x\,\mathrm{d}x<+\infty\right\}.
$$

令 $u=x^2$，则 $\mathrm{d}u=2x\,\mathrm{d}x$，积分化为 $\frac{1}{2}\int_0^{+\infty}e^{\varphi u}\mathrm{d}u=\frac{1}{2\left(-\varphi\right)}$，当且仅当 $\varphi<0$ 时收敛，故自然参数空间为

$$
\Theta^{*}=\left(-\infty,0\right).
$$

$\blacksquare$

### 习题四

（习题 2.4-6）设 $X_1,X_2,\dots,X_n$ 是来自指数分布 $E\left(\lambda\right)$ 的样本，指数分布的密度函数为

$$
f\left(x\right)=\begin{cases}\lambda e^{-\lambda x},&x>0,\\0,&\text{其他},\end{cases}
$$

其中 $\lambda>0$. 证明样本分布族是指数族，并表示成指数族的自然形式，求出自然参数空间.

### 解答 习题四

由**定义 1.3.2**（简单随机样本），样本的联合密度函数为

$$
f\left(x_1,\dots,x_n,\lambda\right)=\prod_{i=1}^n\lambda e^{-\lambda x_i}=\lambda^n\exp\left\{-\lambda\sum_{i=1}^n x_i\right\}.
$$

取 $C\left(\lambda\right)=\lambda^n$，$Q\left(\lambda\right)=-\lambda$，$T\left(x_1,\dots,x_n\right)=\sum_{i=1}^n x_i$，$h\left(x_1,\dots,x_n\right)=1$. 其支撑集为 $\left(0,+\infty\right)$，与 $\lambda$ 无关，故由**定义 2.4.1**（指数族），该样本分布族是指数族.

令自然参数 $\varphi=-\lambda$，则 $\lambda=-\varphi$，由**定义 2.4.2**（指数族的自然形式），自然形式为

$$
f\left(x_1,\dots,x_n,\varphi\right)=\left(-\varphi\right)^n\exp\left\{\varphi\sum_{i=1}^n x_i\right\}=C\left(\varphi\right)\exp\left\{\varphi T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

其中 $C\left(\varphi\right)=\left(-\varphi\right)^n$. 自然参数空间满足

$$
\Theta^{*}=\left\{\varphi:\int_0^{+\infty}e^{\varphi x}\,\mathrm{d}x<+\infty\right\}.
$$

由于 $\int_0^{+\infty}e^{\varphi x}\mathrm{d}x=\frac{1}{-\varphi}$ 当且仅当 $\varphi<0$ 时收敛，故自然参数空间为

$$
\Theta^{*}=\left(-\infty,0\right).
$$

$\blacksquare$

### 习题五

（习题 2.4-7）设 $X_1,X_2,\dots,X_n$ 是来自对数正态分布的样本，其密度函数为

$$
f\left(x,\mu,\sigma^2\right)=\begin{cases}\frac{1}{\sqrt{2\pi}\sigma x}\exp\left\{-\frac{\left(\ln x-\mu\right)^2}{2\sigma^2}\right\},&x>0,\\0,&\text{其他},\end{cases}
$$

其中 $\mu\in\mathbb R,\ \sigma>0$. 证明样本分布族是指数族，并表示成指数族的自然形式，求出自然参数空间.

### 解答 习题五

由**定义 1.3.2**（简单随机样本），样本的联合密度函数为

$$
f\left(x_1,\dots,x_n,\mu,\sigma^2\right)=\left(2\pi\sigma^2\right)^{-n/2}\left(\prod_{i=1}^n x_i\right)^{-1}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(\ln x_i-\mu\right)^2\right\}.
$$

展开平方项：$\sum_{i=1}^n\left(\ln x_i-\mu\right)^2=\sum_{i=1}^n\left(\ln x_i\right)^2-2\mu\sum_{i=1}^n\ln x_i+n\mu^2$，代入得

$$
f=\left(2\pi\sigma^2\right)^{-n/2}\sigma^{-n}\exp\left\{-\frac{n\mu^2}{2\sigma^2}\right\}\exp\left\{\frac{\mu}{\sigma^2}\sum_{i=1}^n\ln x_i-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(\ln x_i\right)^2\right\}\cdot\left(\prod_{i=1}^n x_i\right)^{-1}.
$$

取 $C\left(\mu,\sigma^2\right)=\left(2\pi\right)^{-n/2}\sigma^{-n}\exp\left\{-\frac{n\mu^2}{2\sigma^2}\right\}$，$Q_1\left(\mu,\sigma^2\right)=\frac{\mu}{\sigma^2}$，$T_1=\sum_{i=1}^n\ln x_i$，$Q_2\left(\mu,\sigma^2\right)=-\frac{1}{2\sigma^2}$，$T_2=\sum_{i=1}^n\left(\ln x_i\right)^2$，$h=\left(\prod_{i=1}^n x_i\right)^{-1}$. 其支撑集为 $\left(0,+\infty\right)$，与参数无关，故由**定义 2.4.1**（指数族），该样本分布族是指数族.

令自然参数 $\varphi_1=\frac{\mu}{\sigma^2}$，$\varphi_2=-\frac{1}{2\sigma^2}$，由**定义 2.4.2**（指数族的自然形式），自然形式为

$$
f\left(x_1,\dots,x_n,\varphi_1,\varphi_2\right)=\left(-\frac{\varphi_2}{\pi}\right)^{n/2}\exp\left\{\frac{n\varphi_1^2}{4\varphi_2}\right\}\exp\left\{\varphi_1\sum_{i=1}^n\ln x_i+\varphi_2\sum_{i=1}^n\left(\ln x_i\right)^2\right\}\left(\prod_{i=1}^n x_i\right)^{-1}.
$$

自然参数空间满足

$$
\Theta^{*}=\left\{\left(\varphi_1,\varphi_2\right):\int_0^{+\infty}\exp\left\{\varphi_1\ln x+\varphi_2\left(\ln x\right)^2\right\}\frac{1}{x}\,\mathrm{d}x<+\infty\right\}.
$$

令 $u=\ln x$，则 $\mathrm{d}u=\frac{\mathrm{d}x}{x}$，积分化为

$$
\int_{-\infty}^{+\infty}\exp\left\{\varphi_1 u+\varphi_2 u^2\right\}\,\mathrm{d}u=\sqrt{\frac{\pi}{-\varphi_2}}\exp\left\{-\frac{\varphi_1^2}{4\varphi_2}\right\},
$$

当且仅当 $\varphi_2<0$ 时收敛（此时对任意 $\varphi_1$ 均收敛），故自然参数空间为

$$
\Theta^{*}=\left\{\left(\varphi_1,\varphi_2\right):-\infty<\varphi_1<+\infty,\ \varphi_2<0\right\}.
$$

$\blacksquare$
