# Assignment 6

> **Definition 2.5.1** (Sufficient Statistic)<br>Let the distribution family of the sample $X_1,X_2,\dots,X_n$ be $f\left(x_1,x_2,\dots,x_n,\theta\right)$, $\theta\in\Theta$, where $\Theta$ is the parameter space. Let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a statistic. If, conditional on $T$, the conditional distribution of the sample $X_1,X_2,\dots,X_n$ does not depend on the parameter $\theta$, then the statistic $T\left(X_1,X_2,\dots,X_n\right)$ is called a sufficient statistic for the parameter $\theta$.

> **Theorem 2.5.1** (Factorization Theorem)<br>Let the joint density function (or joint probability mass function) of the sample $X_1,X_2,\dots,X_n$ be $f\left(x_1,x_2,\dots,x_n,\theta\right)$, which depends on the parameter $\theta$, and let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a statistic. Then $T$ is a sufficient statistic if and only if $f\left(x_1,x_2,\dots,x_n,\theta\right)$ can be factored as $$f\left(x_1,x_2,\dots,x_n,\theta\right)=g\left(T\left(x_1,x_2,\dots,x_n\right),\theta\right)h\left(x_1,\dots,x_n\right),$$ where $h\left(x_1,\dots,x_n\right)$ does not depend on the parameter $\theta$.

> **Corollary 2.5.1**<br>Let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a sufficient statistic for $\theta$, and let $S\left(T\right)$ be a single-valued invertible function. Then $S\left(T\right)$ is also a sufficient statistic for $\theta$.

### Problem 1

(Problem 2.5-1) Let $X_1,X_2,\dots,X_n$ be a sample from a Poisson-distributed population $P\left(\lambda\right)$, $\lambda> 0$.

(1) Using respectively the definition method and the factorization-theorem method, prove that $\sum_{i=1}^n X_i$ is a sufficient statistic;

(2) if $n=2$, then $X_1+2X_2$ is not a sufficient statistic.

### Solution to Problem 1

The probability mass function of the Poisson distribution $P\left(\lambda\right)$ is $P\left\{X=x\right\}=\frac{e^{-\lambda}\lambda^x}{x!},\ x=0,1,2,\dots$, where $\lambda> 0$. By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are mutually independent and identically distributed.

(1) Prove that $T=\sum_{i=1}^n X_i$ is a sufficient statistic.

The factorization-theorem method: by **Theorem 2.5.1** (Factorization Theorem), the joint probability mass function of the sample is

$$
P\left(x_1,\dots,x_n,\lambda\right)=\prod_{i=1}^n\frac{e^{-\lambda}\lambda^{x_i}}{x_i!}=\frac{e^{-n\lambda}\lambda^{\sum_{i=1}^n x_i}}{\prod_{i=1}^n x_i!}.
$$

Take $g\left(T,\lambda\right)=e^{-n\lambda}\lambda^{\sum_{i=1}^n x_i}$ and $h\left(x_1,\dots,x_n\right)=\frac{1}{\prod_{i=1}^n x_i!}$, where $h$ does not depend on $\lambda$, so $T=\sum_{i=1}^n X_i$ is a sufficient statistic for $\lambda$.

The definition method: by **Basic Knowledge** (Additivity of the Poisson Distribution), $T=\sum_{i=1}^n X_i\sim P\left(n\lambda\right)$, so $P\left\{T=t\right\}=\frac{e^{-n\lambda}\left(n\lambda\right)^\top}{t!}$. Conditional on $T=t$, when $\sum_{i=1}^n x_i=t$,

$$
P\left\{X_1=x_1,\dots,X_n=x_n\mid T=t\right\}=\frac{P\left\{X_1=x_1,\dots,X_n=x_n,\ T=t\right\}}{P\left\{T=t\right\}}=\frac{\prod_{i=1}^n\frac{e^{-\lambda}\lambda^{x_i}}{x_i!}}{\frac{e^{-n\lambda}\left(n\lambda\right)^\top}{t!}}=\frac{t!}{n^\top\prod_{i=1}^n x_i!}.
$$

This conditional probability mass function does not depend on the parameter $\lambda$, so by **Definition 2.5.1** (Sufficient Statistic), $T=\sum_{i=1}^n X_i$ is a sufficient statistic for $\lambda$.

(2) When $n=2$, prove that $X_1+2X_2$ is not a sufficient statistic.

Write $T'=X_1+2X_2$. Taking $t=2$, there are two cases in which $\left(X_1,X_2\right)$ satisfies $X_1+2X_2=2$: $\left(2,0\right)$ and $\left(0,1\right)$. Conditional on $T'=2$,

$$
P\left\{X_1=2,X_2=0\mid T'=2\right\}=\frac{P\left\{X_1=2,X_2=0\right\}}{P\left\{T'=2\right\}}=\frac{\frac{e^{-\lambda}\lambda^2}{2!}\cdot e^{-\lambda}}{\frac{e^{-\lambda}\lambda^2}{2!}\cdot e^{-\lambda}+e^{-\lambda}\cdot\frac{e^{-\lambda}\lambda}{1!}}=\frac{\frac{\lambda^2}{2}}{\frac{\lambda^2}{2}+\lambda}=\frac{\lambda}{\lambda+2}.
$$

This conditional probability depends on the parameter $\lambda$, so by **Definition 2.5.1** (Sufficient Statistic), $X_1+2X_2$ is not a sufficient statistic for $\lambda$.

$\blacksquare$

### Problem 2

(Problem 2.5-5) Let $X_1,X_2,\dots,X_n$ be a sample from the Rayleigh distribution, whose density function is

$$
f\left(x\right)=\begin{cases}2\theta x e^{-\theta x^2},&x> 0,\\0,&\text{其他},\end{cases}
$$

where $\theta> 0$. Give a sufficient statistic.

### Solution to Problem 2

By **Definition 1.3.2** (Simple Random Sample), the joint density function of the sample is

$$
f\left(x_1,\dots,x_n,\theta\right)=\prod_{i=1}^n 2\theta x_i e^{-\theta x_i^2}=\left(2\theta\right)^n\exp\left\{-\theta\sum_{i=1}^n x_i^2\right\}\cdot\prod_{i=1}^n x_i.
$$

Take $g\left(T,\theta\right)=\left(2\theta\right)^n\exp\left\{-\theta\sum_{i=1}^n x_i^2\right\}$ and $h\left(x_1,\dots,x_n\right)=\prod_{i=1}^n x_i$, where $h$ does not depend on $\theta$. By **Theorem 2.5.1** (Factorization Theorem), $T=\sum_{i=1}^n X_i^2$ is a sufficient statistic for $\theta$.

$\blacksquare$

### Problem 3

(Problem 2.5-6) Let $X_1,X_2,\dots,X_n$ be a sample from the exponential distribution $E\left(\lambda\right)$, whose density function is

$$
f\left(x\right)=\begin{cases}\lambda e^{-\lambda x},&x> 0,\\0,&x\le0,\end{cases}
$$

where $\lambda> 0$. Prove that $\sum_{i=1}^n X_i$ is a sufficient statistic.

### Solution to Problem 3

By **Definition 1.3.2** (Simple Random Sample), the joint density function of the sample is

$$
f\left(x_1,\dots,x_n,\lambda\right)=\prod_{i=1}^n\lambda e^{-\lambda x_i}=\lambda^n\exp\left\{-\lambda\sum_{i=1}^n x_i\right\}.
$$

Take $g\left(T,\lambda\right)=\lambda^n\exp\left\{-\lambda\sum_{i=1}^n x_i\right\}$ and $h\left(x_1,\dots,x_n\right)=1$, where $h$ does not depend on $\lambda$. By **Theorem 2.5.1** (Factorization Theorem), $T=\sum_{i=1}^n X_i$ is a sufficient statistic for $\lambda$.

$\blacksquare$

### Problem 4

(Problem 2.5-7) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$.

(1) When $\mu$ is known, give a sufficient statistic for $\sigma^2$;

(2) when $\sigma^2$ is known, give a sufficient statistic for $\mu$.

### Solution to Problem 4

By **Definition 1.3.2** (Simple Random Sample), the joint density function of the sample is

$$
f\left(x_1,\dots,x_n,\mu,\sigma^2\right)=\left(2\pi\sigma^2\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2\right\}.
$$

(1) When $\mu$ is known, find a sufficient statistic for $\sigma^2$.

When $\mu$ is known, only $\sigma^2$ in the above expression is an unknown parameter. Take $g\left(T,\sigma^2\right)=\left(2\pi\sigma^2\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2\right\}$ and $h=1$, where $h$ does not depend on $\sigma^2$. By **Theorem 2.5.1** (Factorization Theorem), $T=\sum_{i=1}^n\left(X_i-\mu\right)^2$ is a sufficient statistic for $\sigma^2$.

(2) When $\sigma^2$ is known, find a sufficient statistic for $\mu$.

Expanding the squared term: $\sum_{i=1}^n\left(x_i-\mu\right)^2=\sum_{i=1}^n x_i^2-2\mu\sum_{i=1}^n x_i+n\mu^2$, and substituting into the joint density gives

$$
f=\left(2\pi\sigma^2\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n x_i^2\right\}\cdot\exp\left\{\frac{\mu}{\sigma^2}\sum_{i=1}^n x_i-\frac{n\mu^2}{2\sigma^2}\right\}.
$$

When $\sigma^2$ is known, take $g\left(T,\mu\right)=\exp\left\{\frac{\mu}{\sigma^2}\sum_{i=1}^n x_i-\frac{n\mu^2}{2\sigma^2}\right\}$ and $h\left(x_1,\dots,x_n\right)=\left(2\pi\sigma^2\right)^{-n/2}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n x_i^2\right\}$, where $h$ does not depend on $\mu$. By **Theorem 2.5.1** (Factorization Theorem), $T=\sum_{i=1}^n X_i$ is a sufficient statistic for $\mu$. By **Corollary 2.5.1**, $\overline X=\frac{1}{n}\sum_{i=1}^n X_i$ is also a sufficient statistic for $\mu$.

$\blacksquare$
