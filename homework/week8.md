# 作业 8

> **定义 3.2.1**（矩估计）<br>设 $\mathcal{F}=\left\{f\left(x;\theta\right):\theta\in\Theta\right\}$ 是一个参数分布族，其中 $\theta=\left(\theta_1,\theta_2,\dots,\theta_m\right)$，$\Theta$ 为参数空间，$X_1,X_2,\dots,X_n$ 是从该分布族中抽取的样本. 假设总体的 $k$ 阶原点矩 $\alpha_k=E\left(X^k\right)$ 存在，其作为 $\theta$ 的函数记为 $\alpha_k=\alpha_k\left(\theta_1,\theta_2,\dots,\theta_m\right)$. 令样本的 $k$ 阶原点矩为 $A_k=\frac{1}{n}\sum_{i=1}^n X_i^k$，取 $k=1,2,\dots,m$，令总体矩等于样本矩，建立方程组 $$\alpha_k\left(\theta_1,\theta_2,\dots,\theta_m\right)=A_k,\qquad k=1,2,\dots,m,$$ 其解 $\hat\theta_i=\hat\theta_i\left(X_1,X_2,\dots,X_n\right)$ 即称为 $\theta_i$ 的矩估计. 也可用样本 $k$ 阶中心矩去估计总体 $k$ 阶中心矩而建立相应方程. 若要估计参数的函数 $g\left(\theta_1,\dots,\theta_m\right)$，则以 $g\left(\hat\theta_1,\dots,\hat\theta_m\right)$ 作为其矩估计.

> **例 3.2.1 结论**（总体均值与方差的矩估计）<br>设总体 $X$ 的均值 $\mu$ 与方差 $\sigma^2$ 都存在且未知，$X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，则总体均值的矩估计为 $\hat\mu=\bar X=\frac{1}{n}\sum_{i=1}^n X_i$，总体方差的矩估计为 $$\hat\sigma^2=S_n^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2.$$

### 习题一

（习题 3.2-3）设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，且 $X$ 的密度函数 $f\left(x\right)$ 如下所示，求其中未知参数的矩估计.

(1) $f\left(x,\theta\right)=\begin{cases}\left(\theta+1\right)x^\theta,&0<x<1,\\0,&\text{其他},\end{cases}$ 其中 $\theta>-1$ 为未知参数；

(2) $f\left(x,\theta\right)=\begin{cases}\theta e^{-\theta x},&x>0,\\0,&x\le 0,\end{cases}$ 其中 $\theta>0$ 为未知参数；

(3) $f\left(x,\theta\right)=\frac{1}{2\theta}e^{-\frac{\left|x\right|}{\theta}},\ -\infty<x<+\infty$，其中 $\theta>0$ 为未知参数；

(4) $f\left(x,\theta\right)=\begin{cases}1,&\theta-0.5\le x\le\theta+0.5,\\0,&\text{其他},\end{cases}$ 其中 $\theta\in\mathbb R$ 为未知参数；

(5) $f\left(x,\mu,\sigma^2\right)=\begin{cases}\frac{1}{\sqrt{2\pi}\sigma x}e^{-\frac{\left(\ln x-\mu\right)^2}{2\sigma^2}},&x>0,\\0,&x\le 0,\end{cases}$ 其中 $\mu\in\mathbb R$，$\sigma>0$ 为未知参数；

(6) $f\left(x,\mu,\lambda\right)=\begin{cases}\lambda e^{-\lambda\left(x-\mu\right)},&x>\mu,\\0,&\text{其他},\end{cases}$ 其中 $\mu\in\mathbb R$，$\lambda>0$ 为未知参数.

### 解答 习题一

由**定义 3.2.1**（矩估计），令相应的总体矩等于样本矩，解出未知参数.

(1) 总体一阶原点矩为

$$
E\left(X\right)=\int_0^1 x\cdot\left(\theta+1\right)x^\theta\,\mathrm dx=\frac{\theta+1}{\theta+2}.
$$

由**定义 3.2.1**，令 $E\left(X\right)=\bar X$，即 $\frac{\theta+1}{\theta+2}=\bar X$，解得

$$
\hat\theta=\frac{2\bar X-1}{1-\bar X}.
$$

(2) 总体一阶原点矩为 $E\left(X\right)=\frac{1}{\theta}$. 令 $E\left(X\right)=\bar X$，即 $\frac{1}{\theta}=\bar X$，得

$$
\hat\theta=\frac{1}{\bar X}.
$$

(3) 因密度关于原点对称，$E\left(X\right)=0$，不含未知参数，改用一阶绝对矩. 计算得

$$
E\left|X\right|=\int_{-\infty}^{+\infty}\left|x\right|\frac{1}{2\theta}e^{-\frac{\left|x\right|}{\theta}}\,\mathrm dx=\frac{1}{\theta}\int_0^{+\infty}x e^{-\frac{x}{\theta}}\,\mathrm dx=\theta.
$$

由**定义 3.2.1**，令 $E\left|X\right|$ 等于样本一阶绝对矩 $\frac{1}{n}\sum_{i=1}^n\left|X_i\right|$，得

$$
\hat\theta=\frac{1}{n}\sum_{i=1}^n\left|X_i\right|.
$$

(4) $X\sim U\left[\theta-0.5,\theta+0.5\right]$，其均值 $E\left(X\right)=\theta$. 令 $E\left(X\right)=\bar X$，得

$$
\hat\theta=\bar X.
$$

(5) 令 $Y=\ln X$，由密度形式知 $Y\sim N\left(\mu,\sigma^2\right)$. 对 $Y_1=\ln X_1,\dots,Y_n=\ln X_n$ 应用**例 3.2.1 结论**（总体均值与方差的矩估计），得

$$
\hat\mu=\frac{1}{n}\sum_{i=1}^n\ln X_i,\qquad \hat\sigma^2=\frac{1}{n}\sum_{i=1}^n\left(\ln X_i-\frac{1}{n}\sum_{j=1}^n\ln X_j\right)^2.
$$

(6) 该分布为平移指数分布，其均值与方差分别为 $E\left(X\right)=\mu+\frac{1}{\lambda}$，$D\left(X\right)=\frac{1}{\lambda^2}$. 由**例 3.2.1 结论**，$D\left(X\right)$ 的矩估计为 $S_n^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2$，故令 $\frac{1}{\lambda^2}=S_n^2$，得

$$
\hat\lambda=\frac{1}{S_n}.
$$

再由 $E\left(X\right)=\mu+\frac{1}{\lambda}=\bar X$，得

$$
\hat\mu=\bar X-\frac{1}{\hat\lambda}=\bar X-S_n,\qquad S_n=\sqrt{\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2}.
$$

$\blacksquare$

### 习题二

（习题 3.2-5）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，求 $P\left\{X>1\right\}$ 的矩估计.

### 解答 习题二

由 $X\sim N\left(\mu,\sigma^2\right)$，知

$$
P\left\{X>1\right\}=1-P\left\{X\le 1\right\}=1-\Phi\left(\frac{1-\mu}{\sigma}\right),
$$

其中 $\Phi\left(\cdot\right)$ 为标准正态分布函数. 由**例 3.2.1 结论**（总体均值与方差的矩估计），$\mu$ 与 $\sigma$ 的矩估计分别为

$$
\hat\mu=\bar X=\frac{1}{n}\sum_{i=1}^n X_i,\qquad \hat\sigma=S_n=\sqrt{\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2}.
$$

由**定义 3.2.1**（矩估计）中参数函数的矩估计方法，以 $\hat\mu,\hat\sigma$ 替换 $\mu,\sigma$，得 $P\left\{X>1\right\}$ 的矩估计为

$$
\widehat{P\left\{X>1\right\}}=1-\Phi\left(\frac{1-\bar X}{S_n}\right).
$$

$\blacksquare$

### 习题三

（习题 3.2-7）设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，且 $X$ 的分布函数为

$$
F\left(x;\theta\right)=\begin{cases}1-x^{-\theta},&x\ge 1,\\0,&x<1,\end{cases}
$$

其中 $\theta>1$ 为未知参数，求 $\theta$ 的矩估计.

### 解答 习题三

对分布函数求导，得总体密度函数为

$$
f\left(x;\theta\right)=\theta x^{-\left(\theta+1\right)},\qquad x\ge 1.
$$

计算总体一阶原点矩：

$$
E\left(X\right)=\int_1^{+\infty}x\cdot\theta x^{-\left(\theta+1\right)}\,\mathrm dx=\theta\int_1^{+\infty}x^{-\theta}\,\mathrm dx=\frac{\theta}{\theta-1},
$$

其中积分收敛要求 $\theta>1$. 由**定义 3.2.1**（矩估计），令 $E\left(X\right)=\bar X$，即 $\frac{\theta}{\theta-1}=\bar X$，解得

$$
\bar X\left(\theta-1\right)=\theta\ \Longrightarrow\ \theta\left(\bar X-1\right)=\bar X\ \Longrightarrow\ \hat\theta=\frac{\bar X}{\bar X-1}.
$$

$\blacksquare$
