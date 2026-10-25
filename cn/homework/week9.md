# 作业 9

> **定义 3.3.2**（极大似然估计）<br>设总体的密度函数（或分布列）为 $f\left(x;\theta\right)$，$X_1,X_2,\dots,X_n$ 为来自该总体的样本，其观察值为 $x_1,x_2,\dots,x_n$. 若似然函数 $L\left(\theta\right)=L\left(\theta;x_1,x_2,\dots,x_n\right)$ 在 $\hat\theta=\hat\theta\left(x_1,x_2,\dots,x_n\right)$ 处达到极大值，即 $$L\left(\hat\theta\right)=\sup_{\theta\in\Theta}L\left(\theta\right),$$ 则称 $\hat\theta\left(x_1,x_2,\dots,x_n\right)$ 为 $\theta$ 的极大似然估计值，称 $\hat\theta\left(X_1,X_2,\dots,X_n\right)$ 为极大似然估计量，简称 MLE.

> **似然函数与对数似然函数**<br>对连续型总体，似然函数为 $L\left(\theta\right)=\prod_{i=1}^n f\left(x_i;\theta\right)$；对离散型总体，似然函数为 $L\left(\theta\right)=\prod_{i=1}^n P\left(X=x_i;\theta\right)$. 称 $$\ln L\left(\theta\right)=\sum_{i=1}^n\ln f\left(x_i;\theta\right)$$ 为对数似然函数，$L\left(\theta\right)$ 与 $\ln L\left(\theta\right)$ 在同一参数处取得极值.

> **极大似然估计的求法**<br>若似然函数关于 $\theta$ 可微，则 $\hat\theta$ 由对数似然方程 $\frac{\mathrm{d}\ln L}{\mathrm{d}\theta}=0$（多参数时为方程组）求得，当驻点唯一且为极大值点时即为 MLE；若似然函数不可微，则按**定义 3.3.2**（极大似然估计）直接比较似然函数在参数空间上的极大值点.

> **极大似然估计的不变性**<br>若 $\hat\theta$ 为 $\theta$ 的 MLE，$g\left(\theta\right)$ 为具有单值反函数的已知函数，则 $g\left(\hat\theta\right)$ 为 $g\left(\theta\right)$ 的 MLE.

### 习题一

（习题 3.3-3）设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，且 $X$ 的密度函数 $f\left(x\right)$ 如下所示，求其中未知参数的极大似然估计：

(1) $f\left(x,\theta\right)=\begin{cases}\left(\theta+1\right)x^\theta,&0< x< 1,\\0,&\text{其他},\end{cases}$ 其中 $\theta> -1$ 为未知参数；

(2) $f\left(x,\theta\right)=\begin{cases}\theta e^{-\theta x},&x> 0,\\0,&x\le0,\end{cases}$ 其中 $\theta> 0$ 为未知参数；

(3) $f\left(x,\theta\right)=\frac{1}{2\theta}e^{-\frac{\left|x\right|}{\theta}},\ -\infty< x< +\infty$，其中 $\theta> 0$ 为未知参数；

(4) $f\left(x,\theta\right)=\begin{cases}1,&\theta-0.5\le x\le\theta+0.5,\\0,&\text{其他},\end{cases}$ 其中 $\theta\in\mathbb R$ 为未知参数；

(5) $f\left(x,\mu,\sigma^2\right)=\begin{cases}\frac{1}{\sqrt{2\pi}\sigma x}e^{-\frac{\left(\ln x-\mu\right)^2}{2\sigma^2}},&x> 0,\\0,&x\le0,\end{cases}$ 其中 $\mu\in\mathbb R,\ \sigma^2> 0$ 为未知参数.

### 解答 习题一

由**似然函数与对数似然函数**，对每个密度写出似然函数并按**极大似然估计的求法**求 MLE.

(1) 似然函数为

$$
L\left(\theta\right)=\prod_{i=1}^n\left(\theta+1\right)x_i^\theta=\left(\theta+1\right)^n\left(\prod_{i=1}^n x_i\right)^\theta,\quad 0< x_i< 1.
$$

对数似然函数为 $\ln L\left(\theta\right)=n\ln\left(\theta+1\right)+\theta\sum_{i=1}^n\ln x_i$. 由**极大似然估计的求法**，令

$$
\frac{\mathrm{d}\ln L}{\mathrm{d}\theta}=\frac{n}{\theta+1}+\sum_{i=1}^n\ln x_i=0,
$$

解得 $\hat\theta=-1-\frac{n}{\sum_{i=1}^n\ln x_i}$. 因 $0< x_i< 1$，$\sum_{i=1}^n\ln x_i< 0$，故 $\hat\theta> -1$；又 $\frac{\mathrm{d}^2\ln L}{\mathrm{d}\theta^2}=-\frac{n}{\left(\theta+1\right)^2}< 0$，故该驻点为极大值点. 于是

$$
\hat\theta=-1-\frac{n}{\sum_{i=1}^n\ln X_i}.
$$

(2) 似然函数为

$$
L\left(\theta\right)=\prod_{i=1}^n\theta e^{-\theta x_i}=\theta^n e^{-\theta\sum_{i=1}^n x_i},\quad x_i> 0.
$$

对数似然函数为 $\ln L\left(\theta\right)=n\ln\theta-\theta\sum_{i=1}^n x_i$. 令 $\frac{\mathrm{d}\ln L}{\mathrm{d}\theta}=\frac{n}{\theta}-\sum_{i=1}^n x_i=0$，解得

$$
\hat\theta=\frac{1}{\bar X},\quad \bar X=\frac{1}{n}\sum_{i=1}^n X_i.
$$

(3) 似然函数为

$$
L\left(\theta\right)=\prod_{i=1}^n\frac{1}{2\theta}e^{-\frac{\left|x_i\right|}{\theta}}=\left(2\theta\right)^{-n}e^{-\frac{1}{\theta}\sum_{i=1}^n\left|x_i\right|}.
$$

对数似然函数为 $\ln L\left(\theta\right)=-n\ln\left(2\theta\right)-\frac{1}{\theta}\sum_{i=1}^n\left|x_i\right|$. 令 $\frac{\mathrm{d}\ln L}{\mathrm{d}\theta}=-\frac{n}{\theta}+\frac{1}{\theta^2}\sum_{i=1}^n\left|x_i\right|=0$，解得

$$
\hat\theta=\frac{1}{n}\sum_{i=1}^n\left|X_i\right|.
$$

(4) 当且仅当全部样本落入 $\left[\theta-0.5,\theta+0.5\right]$，即 $\theta-0.5\le x_{\left(1\right)}$ 且 $x_{\left(n\right)}\le\theta+0.5$ 时，$L\left(\theta\right)=1$，否则 $L\left(\theta\right)=0$. 由**定义 3.3.2**（极大似然估计），凡使似然函数达到最大值 $1$ 的 $\theta$ 均为 MLE，故 MLE 不唯一，为区间

$$
\hat\theta\in\left[X_{\left(n\right)}-0.5,\ X_{\left(1\right)}+0.5\right],
$$

其中 $X_{\left(1\right)}=\min\left\{X_1,\dots,X_n\right\}$，$X_{\left(n\right)}=\max\left\{X_1,\dots,X_n\right\}$.

(5) 令 $y_i=\ln x_i$，似然函数为

$$
L\left(\mu,\sigma^2\right)=\prod_{i=1}^n\frac{1}{\sqrt{2\pi}\sigma x_i}e^{-\frac{\left(y_i-\mu\right)^2}{2\sigma^2}}=\frac{1}{\left(2\pi\sigma^2\right)^{n/2}\prod_{i=1}^n x_i}e^{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(y_i-\mu\right)^2}.
$$

其中 $\prod_{i=1}^n x_i$ 与参数无关. 对数似然函数为

$$
\ln L\left(\mu,\sigma^2\right)=-\frac{n}{2}\ln\left(2\pi\sigma^2\right)-\sum_{i=1}^n\ln x_i-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(y_i-\mu\right)^2.
$$

由**极大似然估计的求法**，令 $\frac{\partial\ln L}{\partial\mu}=0$ 得 $\hat\mu=\bar y=\frac{1}{n}\sum_{i=1}^n\ln x_i$；令 $\frac{\partial\ln L}{\partial\left(\sigma^2\right)}=0$ 得

$$
\hat\sigma^2=\frac{1}{n}\sum_{i=1}^n\left(\ln X_i-\frac{1}{n}\sum_{j=1}^n\ln X_j\right)^2.
$$

$\blacksquare$

### 习题二

（习题 3.3-4）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，其中 $\mu\in\mathbb R,\ \sigma> 0$，

(1) 若 $\mu$ 未知，$\sigma$ 已知，求 $\mu$ 的极大似然估计；

(2) 若 $\mu$ 已知，$\sigma$ 未知，求 $\sigma^2$ 的极大似然估计.

### 解答 习题二

正态总体的密度函数为 $f\left(x;\mu,\sigma^2\right)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{\left(x-\mu\right)^2}{2\sigma^2}}$. 由**似然函数与对数似然函数**，似然函数为

$$
L\left(\mu,\sigma^2\right)=\left(2\pi\sigma^2\right)^{-\frac{n}{2}}e^{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2}.
$$

(1) 当 $\sigma$ 已知时，与 $\mu$ 有关的部分为指数上的 $-\sum_{i=1}^n\left(x_i-\mu\right)^2$. 由**极大似然估计的求法**，令

$$
\frac{\mathrm{d}}{\mathrm{d}\mu}\sum_{i=1}^n\left(x_i-\mu\right)^2=-2\sum_{i=1}^n\left(x_i-\mu\right)=0,
$$

解得 $\hat\mu=\bar X=\frac{1}{n}\sum_{i=1}^n X_i$，此时残差平方和最小，故为 MLE.

(2) 当 $\mu$ 已知时，对数似然函数为

$$
\ln L\left(\sigma^2\right)=-\frac{n}{2}\ln\left(2\pi\sigma^2\right)-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2.
$$

令 $\frac{\mathrm{d}\ln L}{\mathrm{d}\left(\sigma^2\right)}=-\frac{n}{2\sigma^2}+\frac{1}{2\sigma^4}\sum_{i=1}^n\left(x_i-\mu\right)^2=0$，解得

$$
\hat\sigma^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\mu\right)^2.
$$

$\blacksquare$

### 习题三

（习题 3.3-6）设 $X_1,X_2,\dots,X_n$ 是来自双参数指数分布总体的样本，且密度函数为

$$
f\left(x,\mu,\lambda\right)=\begin{cases}\lambda\exp\left\{-\lambda\left(x-\mu\right)\right\},&x> \mu,\\0,&\text{其他},\end{cases}
$$

其中 $-\infty< \mu< +\infty,\ \lambda> 0$ 为未知参数，分别求 $\mu,\lambda$ 和 $\alpha=P\left\{X_1\ge t\right\}$（$t> \mu$）的极大似然估计.

### 解答 习题三

由**似然函数与对数似然函数**，当 $\mu\le x_{\left(1\right)}$ 时似然函数为

$$
L\left(\mu,\lambda\right)=\prod_{i=1}^n\lambda e^{-\lambda\left(x_i-\mu\right)}=\lambda^n e^{-\lambda\sum_{i=1}^n x_i+n\lambda\mu},
$$

当 $\mu> x_{\left(1\right)}$ 时 $L=0$. 由**极大似然估计的求法**，对固定的 $\lambda> 0$，$L\left(\mu,\lambda\right)=e^{n\lambda\mu}\cdot\lambda^n e^{-\lambda\sum x_i}$ 关于 $\mu$ 单调递增，故在允许范围内 $\mu$ 取最大时达极大值，即

$$
\hat\mu=X_{\left(1\right)}=\min\left\{X_1,\dots,X_n\right\}.
$$

将 $\hat\mu=x_{\left(1\right)}$ 代入，得剖面对数似然函数

$$
\ln L\left(x_{\left(1\right)},\lambda\right)=n\ln\lambda-\lambda\sum_{i=1}^n\left(x_i-x_{\left(1\right)}\right).
$$

令 $\frac{\mathrm{d}\ln L}{\mathrm{d}\lambda}=\frac{n}{\lambda}-\sum_{i=1}^n\left(x_i-x_{\left(1\right)}\right)=0$，解得

$$
\hat\lambda=\frac{n}{\sum_{i=1}^n\left(X_i-X_{\left(1\right)}\right)}=\frac{1}{\bar X-X_{\left(1\right)}}.
$$

对生存概率，由 $X-\mu\sim E\left(\lambda\right)$，

$$
\alpha=P\left\{X_1\ge t\right\}=e^{-\lambda\left(t-\mu\right)}.
$$

由**极大似然估计的不变性**，

$$
\hat\alpha=e^{-\hat\lambda\left(t-\hat\mu\right)}=\exp\left\{-\frac{t-X_{\left(1\right)}}{\bar X-X_{\left(1\right)}}\right\}.
$$

$\blacksquare$
