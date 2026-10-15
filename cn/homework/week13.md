# 作业 13

> **定义 4.1.1**（区间估计）<br>设 $\mathcal{F}=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ 是一个参数分布族，其中 $\Theta$ 为参数空间，$g\left(\theta\right)$ 是定义在 $\Theta$ 上的一个已知函数，$X_1,X_2,\dots,X_n$ 是从分布族 $\mathcal{F}$ 中的某总体抽取的样本. 令 $g_1\left(X_1,X_2,\dots,X_n\right)$ 和 $g_2\left(X_1,X_2,\dots,X_n\right)$ 是定义在样本空间上的函数，并且满足 $g_1\left(X_1,X_2,\dots,X_n\right)\le g_2\left(X_1,X_2,\dots,X_n\right)$，则称随机区间 $\left[g_1\left(X_1,X_2,\dots,X_n\right),g_2\left(X_1,X_2,\dots,X_n\right)\right]$ 是 $g\left(\theta\right)$ 的一个区间估计.

> **定义 4.1.4**（置信区间）<br>设 $\left[\theta_1\left(X_1,X_2,\dots,X_n\right),\theta_2\left(X_1,X_2,\dots,X_n\right)\right]$ 是参数 $\theta$ 的一个区间估计. 对给定 $0<\alpha<1$，如果对于任意的 $\theta\in\Theta$，都有 $P_\theta\left\{\theta_1\left(X_1,X_2,\dots,X_n\right)\le\theta\le\theta_2\left(X_1,X_2,\dots,X_n\right)\right\}\ge1-\alpha$ 成立，则称 $\left[\theta_1,\theta_2\right]$ 是参数 $\theta$ 的置信水平为 $1-\alpha$ 的置信区间.

> **定义 4.1.5**（置信限）<br>设 $\theta_L\left(X_1,X_2,\dots,X_n\right)$ 和 $\theta_U\left(X_1,X_2,\dots,X_n\right)$ 是定义在样本空间上取值在参数空间的统计量，给定 $0<\alpha<1$，对任意的 $\theta\in\Theta$ 都有 $P_\theta\left\{\theta\ge\theta_L\right\}\ge1-\alpha$ 和 $P_\theta\left\{\theta\le\theta_U\right\}\ge1-\alpha$ 成立，则称 $\theta_L$ 和 $\theta_U$ 是参数 $\theta$ 的置信水平为 $1-\alpha$ 的单侧置信下限和单侧置信上限.

> **抽样分布**（正态样本的抽样分布）<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，则 $\bar X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right)$，从而 $\frac{\sqrt n\left(\bar X-\mu\right)}{\sigma}\sim N\left(0,1\right)$. 当 $\sigma^2$ 未知时，$\frac{\sqrt n\left(\bar X-\mu\right)}{S}\sim t\left(n-1\right)$，其中 $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$ 为样本方差.

### 习题一

（习题 4.1-4）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，其中 $\mu\in\mathbb R$ 为未知参数，$\sigma>0$ 已知，记 $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$，则当 $\mu$ 的置信区间为 $\left[\bar X-\frac{\sigma}{\sqrt n}u_{0.05},\bar X+\frac{\sigma}{\sqrt n}u_{0.05}\right]$ 时，求置信水平.

### 解答 习题一

由**定义 4.1.1**（区间估计），该随机区间为 $\left[\theta_1,\theta_2\right]=\left[\bar X-\frac{\sigma}{\sqrt n}u_{0.05},\bar X+\frac{\sigma}{\sqrt n}u_{0.05}\right]$. 由**定义 4.1.4**（置信区间），其置信水平为

$$
P_\mu\left\{\bar X-\frac{\sigma}{\sqrt n}u_{0.05}\le\mu\le\bar X+\frac{\sigma}{\sqrt n}u_{0.05}\right\}.
$$

将不等式变形，等价于

$$
P_\mu\left\{-u_{0.05}\le\frac{\sqrt n\left(\bar X-\mu\right)}{\sigma}\le u_{0.05}\right\}.
$$

由**抽样分布**（正态样本的抽样分布），当 $\sigma$ 已知时，$\frac{\sqrt n\left(\bar X-\mu\right)}{\sigma}\sim N\left(0,1\right)$. 设 $Z\sim N\left(0,1\right)$，其中 $u_{0.05}$ 为标准正态分布的上 $0.05$ 分位数，即 $P\left(Z\ge u_{0.05}\right)=0.05$，由对称性 $P\left(Z\le-u_{0.05}\right)=0.05$. 因此

$$
P\left\{-u_{0.05}\le Z\le u_{0.05}\right\}=1-P\left\{Z>u_{0.05}\right\}-P\left\{Z<-u_{0.05}\right\}=1-0.05-0.05=0.90.
$$

故该置信区间的置信水平为 $0.90$. $\blacksquare$

### 习题二

（习题 4.1-5）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，其中 $\mu\in\mathbb R$，$\sigma>0$ 为未知参数，记 $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$，$S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$，则当 $\mu$ 的置信上限为 $\bar X+\frac{S}{\sqrt n}t_{0.05}\left(n-1\right)$ 时，求置信水平.

### 解答 习题二

由**定义 4.1.5**（置信限），单侧置信上限 $\theta_U=\bar X+\frac{S}{\sqrt n}t_{0.05}\left(n-1\right)$ 的置信水平为

$$
P_\mu\left\{\mu\le\bar X+\frac{S}{\sqrt n}t_{0.05}\left(n-1\right)\right\}.
$$

将不等式变形，等价于

$$
P_\mu\left\{\frac{\sqrt n\left(\bar X-\mu\right)}{S}\le t_{0.05}\left(n-1\right)\right\}.
$$

由**抽样分布**（正态样本的抽样分布），当 $\sigma$ 未知时，$\frac{\sqrt n\left(\bar X-\mu\right)}{S}\sim t\left(n-1\right)$. 设 $T\sim t\left(n-1\right)$，其中 $t_{0.05}\left(n-1\right)$ 为 $t$ 分布的上 $0.05$ 分位数，即 $P\left(T\ge t_{0.05}\left(n-1\right)\right)=0.05$. 因此

$$
P\left\{T\le t_{0.05}\left(n-1\right)\right\}=1-P\left\{T>t_{0.05}\left(n-1\right)\right\}=1-0.05=0.95.
$$

故该单侧置信上限的置信水平为 $0.95$. $\blacksquare$
