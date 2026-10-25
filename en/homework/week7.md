# Assignment 7

> **Definition 2.6.1** (Complete Statistic)<br>Let $\mathcal{F}=\left\{f\left(x;\theta\right),\theta\in\Theta\right\}$ be a family of distributions, where $\Theta$ is the parameter space. Let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a statistic. If for any $\Phi\left(\cdot\right)$ satisfying $E\left[\Phi\left(T\left(X_1,X_2,\dots,X_n\right)\right)\right]=0$ for all $\theta\in\Theta$, one has $P_\theta\left\{\Phi\left(T\left(X_1,X_2,\dots,X_n\right)\right)=0\right\}=1$ for all $\theta\in\Theta$, then $T\left(X_1,X_2,\dots,X_n\right)$ is called a complete statistic. If $T$ is a complete statistic, then any measurable function $g\left(T\right)$ of it is also a complete statistic.

> **Theorem 2.6.1** (Completeness of a Statistic in an Exponential Family)<br>Let $X_1,X_2,\dots,X_n$ be a sample drawn from the following exponential family (in natural form): $$f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k\theta_i T_i\left(x\right)\right\}h\left(x\right),\quad \theta=\left(\theta_1,\theta_2,\dots,\theta_k\right)\in\Theta^*\subseteq\mathbb R^k,$$ If its natural parameter space $\Theta^*$ has an interior point, then $T\left(X_1,X_2,\dots,X_n\right)=\left(T_1\left(X_1,\dots,X_n\right),\dots,T_k\left(X_1,\dots,X_n\right)\right)$ is a complete statistic.

> **Theorem 2.5.1** (Factorization Theorem)<br>Let the joint density function (or joint probability mass function) of the sample $X_1,X_2,\dots,X_n$ be $f\left(x_1,x_2,\dots,x_n;\theta\right)$, and let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a statistic. Then $T$ is a sufficient statistic if and only if $f\left(x_1,x_2,\dots,x_n;\theta\right)$ can be factored as $$f\left(x_1,x_2,\dots,x_n;\theta\right)=g\left(T\left(x_1,x_2,\dots,x_n\right),\theta\right)h\left(x_1,x_2,\dots,x_n\right),$$ where $h\left(x_1,x_2,\dots,x_n\right)$ does not depend on the parameter $\theta$.

### Problem 1

(Problem 2.6-1) Let $X_1,X_2,\dots,X_n$ be a sample from a Poisson-distributed population $P\left(\lambda\right)$, $\lambda> 0$. Prove that $\sum_{i=1}^n X_i$ is a complete statistic.

### Solution to Problem 1

By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are mutually independent and each $X_i\sim P\left(\lambda\right)$. The joint probability mass function of the sample is

$$
f\left(x_1,x_2,\dots,x_n;\lambda\right)=\prod_{i=1}^n\frac{e^{-\lambda}\lambda^{x_i}}{x_i!}=e^{-n\lambda}\lambda^{\sum_{i=1}^n x_i}\prod_{i=1}^n\frac{1}{x_i!}.
$$

Letting the natural parameter be $\eta=\ln\lambda$, then $\lambda=e^{\eta}$, and the above takes the natural form of an exponential family

$$
f\left(x_1,x_2,\dots,x_n;\eta\right)=e^{-ne^{\eta}}\exp\left\{\eta\sum_{i=1}^n x_i\right\}\prod_{i=1}^n\frac{1}{x_i!}=C\left(\eta\right)\exp\left\{\eta T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

where $T=\sum_{i=1}^n x_i$ and $h=\prod_{i=1}^n\frac{1}{x_i!}$ do not depend on the parameters. Since $\lambda> 0$, the natural parameter $\eta=\ln\lambda\in\left(-\infty,+\infty\right)$, whose natural parameter space has an interior point. By **Theorem 2.6.1** (Completeness of a Statistic in an Exponential Family), $T=\sum_{i=1}^n X_i$ is a complete statistic. $\blacksquare$

### Problem 2

(Problem 2.6-5) Let $X_1,X_2,\dots,X_n$ be a sample from the Rayleigh distribution, whose density function is

$$
f\left(x\right)=\begin{cases}2\theta x e^{-\theta x^2},&x> 0,\\0,&\text{其他},\end{cases}
$$

where $\theta> 0$. Give a complete statistic.

### Solution to Problem 2

By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are mutually independent and identically distributed, and the joint density function of the sample is

$$
f\left(x_1,x_2,\dots,x_n;\theta\right)=\prod_{i=1}^n 2\theta x_i e^{-\theta x_i^2}=\left(2\theta\right)^n\exp\left\{-\theta\sum_{i=1}^n x_i^2\right\}\prod_{i=1}^n x_i.
$$

Letting the natural parameter be $\eta=-\theta$, the above takes the natural form of an exponential family

$$
f\left(x_1,x_2,\dots,x_n;\eta\right)=\left(-2\eta\right)^n\exp\left\{\eta\sum_{i=1}^n x_i^2\right\}\prod_{i=1}^n x_i=C\left(\eta\right)\exp\left\{\eta T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

where $T=\sum_{i=1}^n x_i^2$ and $h=\prod_{i=1}^n x_i$ do not depend on the parameters. Since $\theta> 0$, the natural parameter $\eta=-\theta\in\left(-\infty,0\right)$, whose natural parameter space has an interior point. By **Theorem 2.6.1** (Completeness of a Statistic in an Exponential Family), $T=\sum_{i=1}^n X_i^2$ is a complete statistic, so we may take the complete statistic to be $T=\sum_{i=1}^n X_i^2$. $\blacksquare$

### Problem 3

(Problem 2.6-6) Let $X_1,X_2,\dots,X_n$ be a sample from the exponential distribution $E\left(\lambda\right)$, whose density function is

$$
f\left(x\right)=\begin{cases}\lambda e^{-\lambda x},&x> 0,\\0,&x\le 0,\end{cases}
$$

where $\lambda> 0$. Prove that $\sum_{i=1}^n X_i$ is a complete statistic.

### Solution to Problem 3

By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are mutually independent and identically distributed, and the joint density function of the sample is

$$
f\left(x_1,x_2,\dots,x_n;\lambda\right)=\prod_{i=1}^n\lambda e^{-\lambda x_i}=\lambda^n\exp\left\{-\lambda\sum_{i=1}^n x_i\right\}.
$$

Letting the natural parameter be $\eta=-\lambda$, the above takes the natural form of an exponential family

$$
f\left(x_1,x_2,\dots,x_n;\eta\right)=\left(-\eta\right)^n\exp\left\{\eta\sum_{i=1}^n x_i\right\}=C\left(\eta\right)\exp\left\{\eta T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

where $T=\sum_{i=1}^n x_i$ and $h=1$ do not depend on the parameters. Since $\lambda> 0$, the natural parameter $\eta=-\lambda\in\left(-\infty,0\right)$, whose natural parameter space has an interior point. By **Theorem 2.6.1** (Completeness of a Statistic in an Exponential Family), $T=\sum_{i=1}^n X_i$ is a complete statistic. $\blacksquare$

### Problem 4

(Problem 2.6-7) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$.

(1) When $\mu$ is known, give a complete statistic for $\sigma^2$;

(2) when $\sigma^2$ is known, give a complete statistic for $\mu$.

### Solution to Problem 4

By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are mutually independent and each $X_i\sim N\left(\mu,\sigma^2\right)$, and the joint density function of the sample is

$$
f\left(x_1,x_2,\dots,x_n;\mu,\sigma^2\right)=\left(2\pi\sigma^2\right)^{-\frac{n}{2}}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2\right\}.
$$

(1) When $\mu$ is known, write the joint density in the natural form of an exponential family in $\sigma^2$:

$$
f=C\left(\sigma^2\right)\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2\right\}.
$$

Letting the natural parameter be $\eta=-\frac{1}{2\sigma^2}$, then $T=\sum_{i=1}^n\left(x_i-\mu\right)^2$. Since $\sigma^2> 0$, the natural parameter $\eta\in\left(-\infty,0\right)$ has an interior point. By **Theorem 2.6.1** (Completeness of a Statistic in an Exponential Family), $T=\sum_{i=1}^n\left(X_i-\mu\right)^2$ is a complete statistic for $\sigma^2$.

(2) When $\sigma^2$ is known, expand the exponential part:

$$
-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2=-\frac{1}{2\sigma^2}\sum_{i=1}^n x_i^2+\frac{\mu}{\sigma^2}\sum_{i=1}^n x_i-\frac{n\mu^2}{2\sigma^2},
$$

where all terms involving $x_i$ except $\frac{\mu}{\sigma^2}\sum_{i=1}^n x_i$ are absorbed into $C\left(\mu,\sigma^2\right)$, so

$$
f=C'\left(\mu,\sigma^2\right)\exp\left\{\frac{\mu}{\sigma^2}\sum_{i=1}^n x_i\right\}.
$$

Letting the natural parameter be $\eta=\frac{\mu}{\sigma^2}$, then $T=\sum_{i=1}^n x_i$. Since $\mu\in\mathbb R$, the natural parameter $\eta\in\left(-\infty,+\infty\right)$ has an interior point. By **Theorem 2.6.1** (Completeness of a Statistic in an Exponential Family), $T=\sum_{i=1}^n X_i$ is a complete statistic for $\mu$ (equivalently, the sample mean $\bar X$ is also one). $\blacksquare$

### Problem 5

(Problem 2.6-10) Let $X_1,X_2,\dots,X_n$ be a sample from a uniform-distribution population $U\left[\theta,2\theta\right]$, $\theta> 0$. Prove that $\left(X_{\left(1\right)},X_{\left(n\right)}\right)$ is a sufficient statistic but not a complete statistic.

### Solution to Problem 5

First prove sufficiency. The joint density function of the sample is

$$
f\left(x_1,x_2,\dots,x_n;\theta\right)=\prod_{i=1}^n\frac{1}{\theta}\mathbf 1\left\{\theta\le x_i\le 2\theta\right\}=\theta^{-n}\mathbf 1\left\{\theta\le X_{\left(1\right)},\ X_{\left(n\right)}\le 2\theta\right\}.
$$

It is already factored as $f=g\left(T\left(x_1,\dots,x_n\right),\theta\right)h\left(x_1,\dots,x_n\right)$, where $T=\left(X_{\left(1\right)},X_{\left(n\right)}\right)$, $g=\theta^{-n}\mathbf 1\left\{\theta\le X_{\left(1\right)},\ X_{\left(n\right)}\le 2\theta\right\}$, and $h=1$ does not depend on $\theta$. By **Theorem 2.5.1** (Factorization Theorem), $\left(X_{\left(1\right)},X_{\left(n\right)}\right)$ is a sufficient statistic.

Next prove its incompleteness. Let $Y_i=\frac{X_i-\theta}{\theta}$, then $Y_1,Y_2,\dots,Y_n$ are independent and identically distributed as $U\left[0,1\right]$, and $X_{\left(1\right)}=\theta\left(1+Y_{\left(1\right)}\right)$, $X_{\left(n\right)}=\theta\left(1+Y_{\left(n\right)}\right)$. For the order statistics of $U\left[0,1\right]$, integrating their densities gives $E\left[Y_{\left(1\right)}\right]=\frac{1}{n+1}$ and $E\left[Y_{\left(n\right)}\right]=\frac{n}{n+1}$, so

$$
E\left[X_{\left(1\right)}\right]=\theta\left(1+\frac{1}{n+1}\right)=\frac{\theta\left(n+2\right)}{n+1},\quad E\left[X_{\left(n\right)}\right]=\theta\left(1+\frac{n}{n+1}\right)=\frac{\theta\left(2n+1\right)}{n+1}.
$$

Take a function of the statistic $T=\left(X_{\left(1\right)},X_{\left(n\right)}\right)$

$$
\Phi\left(T\right)=\left(n+2\right)X_{\left(n\right)}-\left(2n+1\right)X_{\left(1\right)},
$$

then for all $\theta> 0$,

$$
E\left[\Phi\left(T\right)\right]=\left(n+2\right)\frac{\theta\left(2n+1\right)}{n+1}-\left(2n+1\right)\frac{\theta\left(n+2\right)}{n+1}=0.
$$

But $\Phi\left(T\right)$ is not almost everywhere zero (it varies with the sample observations and is not identically $0$). By **Definition 2.6.1** (Complete Statistic), there exists such a nonzero function $\Phi\left(T\right)$ for which $E\left[\Phi\left(T\right)\right]=0$ for all $\theta$, so $\left(X_{\left(1\right)},X_{\left(n\right)}\right)$ is not a complete statistic. $\blacksquare$
