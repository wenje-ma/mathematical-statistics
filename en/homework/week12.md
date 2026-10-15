# Assignment 12

> **Definition 3.6.1** (Regular Distribution Family)<br>If a one-parameter distribution family $\mathcal F=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ satisfies: (1) the parameter space $\Theta$ is an open interval on the line; (2) for any $\theta\in\Theta$, $f\left(x,\theta\right)>0$, i.e. the support of the distribution does not depend on the parameter; (3) $\frac{\partial f\left(x,\theta\right)}{\partial\theta}$ exists for any $\theta\in\Theta$; (4) the integration and differentiation operations on $f\left(x,\theta\right)$ can be interchanged; (5) the Fisher information exists and $0<I\left(\theta\right)=E\left[\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right]^2<+\infty$, then the family is called a Cramér–Rao regular distribution family, where $$I\left(\theta\right)=E\left[\left(\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right)^2\right]$$ is the Fisher information of the family.

> **Theorem 3.6.1** (One-parameter Cramér–Rao Inequality)<br>Let the distribution family $\mathcal F=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ be a Cramér–Rao regular distribution family, let the estimable function $g\left(\theta\right)$ be differentiable over the parameter space, let $X_1,X_2,\dots,X_n$ be a sample drawn from this population, and let $\hat g\left(X\right)=\hat g\left(X_1,X_2,\dots,X_n\right)$ be any unbiased estimator of $g\left(\theta\right)$, with differentiation under the integral sign with respect to $\theta$ permissible. Then $$D\left[\hat g\left(X\right)\right]\ge\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)}.$$ The right-hand side $\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)}$ is called the Cramér–Rao lower bound. If some unbiased estimator attains this bound, then it must be a uniformly minimum variance unbiased estimator.

> **Definition 3.6.2** (Efficiency)<br>Let $\hat g\left(X\right)$ be an unbiased estimator of $g\left(\theta\right)$. Then the ratio $$e\left(\theta\right)=\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)D\left[\hat g\left(X\right)\right]}$$ is called the efficiency of the unbiased estimator $\hat g\left(X\right)$, where $0<e\left(\theta\right)\le1$.

> **Definition 3.6.3** (Efficient Estimator)<br>When $e\left(\theta\right)\equiv1$, $\hat g\left(X\right)$ is called an efficient estimator of $g\left(\theta\right)$. An efficient estimator is always a uniformly minimum variance unbiased estimator.

> **Corollary 3.5.1** (Sufficient and Complete Statistic under the Natural Form of an Exponential Family)<br>Let the distribution of the sample be in the natural form of an exponential family. If the natural parameter space has an interior point, then $T\left(X\right)$ is a sufficient and complete statistic; in this case, if $h\left(T\left(X\right)\right)$ is an unbiased estimator of $g\left(\theta\right)$, then by **Theorem 3.5.1** (L–S Theorem), it is the unique uniformly minimum variance unbiased estimator of $g\left(\theta\right)$.

> **Sampling Distribution** (Sampling Distribution for a Normal Sample)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$. Then $\bar X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right)$. In particular, when $\sigma^2=1$, $\bar X\sim N\left(\mu,\frac{1}{n}\right)$.

### Problem 1

(Problem 3.6-1) Let the density function or probability mass function of the population $X$ be $f\left(x,\theta\right)$, and suppose the Fisher information $I\left(\theta\right)$ exists. If the second derivative $\frac{\partial^2 f\left(x,\theta\right)}{\partial\theta^2}$ exists for all $\theta\in\Theta$, prove that the Fisher information is

$$
I\left(\theta\right)=-E\left[\frac{\partial^2\ln f\left(X,\theta\right)}{\partial\theta^2}\right].
$$

### Solution to Problem 1

By **Definition 3.6.1** (Regular Distribution Family), $f\left(x,\theta\right)$ is the density function (the discrete case is analogous), and integration and differentiation can be interchanged. Since $\int f\left(x,\theta\right)\,\mathrm dx=1$, differentiating with respect to $\theta$ and using regularity condition (4) gives

$$
\frac{\partial}{\partial\theta}\int f\left(x,\theta\right)\,\mathrm dx=\int\frac{\partial f\left(x,\theta\right)}{\partial\theta}\,\mathrm dx=0.
$$

Substituting $\frac{\partial f}{\partial\theta}=f\cdot\frac{\partial\ln f}{\partial\theta}$ into the above gives

$$
\int\frac{\partial\ln f\left(x,\theta\right)}{\partial\theta}f\left(x,\theta\right)\,\mathrm dx=E\left[\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right]=0.
$$

Differentiating the above once more with respect to $\theta$, and interchanging the order of integration and differentiation using regularity condition (4), gives

$$
\frac{\partial}{\partial\theta}E\left[\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right]=\int\frac{\partial}{\partial\theta}\left[\frac{\partial\ln f\left(x,\theta\right)}{\partial\theta}f\left(x,\theta\right)\right]\,\mathrm dx=0.
$$

Expanding the integrand,

$$
\frac{\partial}{\partial\theta}\left[\frac{\partial\ln f}{\partial\theta}f\right]=\frac{\partial^2\ln f}{\partial\theta^2}f+\frac{\partial\ln f}{\partial\theta}\cdot\frac{\partial f}{\partial\theta}=\frac{\partial^2\ln f}{\partial\theta^2}f+\left(\frac{\partial\ln f}{\partial\theta}\right)^2f.
$$

Integrating both sides, noting that the integral of the first term is $E\left[\frac{\partial^2\ln f\left(X,\theta\right)}{\partial\theta^2}\right]$ and the integral of the second term is $E\left[\left(\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right)^2\right]=I\left(\theta\right)$, we get

$$
E\left[\frac{\partial^2\ln f\left(X,\theta\right)}{\partial\theta^2}\right]+I\left(\theta\right)=0.
$$

Rearranging gives

$$
I\left(\theta\right)=-E\left[\frac{\partial^2\ln f\left(X,\theta\right)}{\partial\theta^2}\right].
$$

$\blacksquare$

### Problem 2

(Problem 3.6-2) Let the probability mass function of the population $X$ be

$$
P\left\{X=x\right\}=\left(x-1\right)\theta^2\left(1-\theta\right)^{x-2},\quad x=2,3,\dots
$$

where $0<\theta<1$. Find the Fisher information $I\left(\theta\right)$.

### Solution to Problem 2

By **Definition 3.6.1** (Regular Distribution Family), the Fisher information is $I\left(\theta\right)=E\left[\left(\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right)^2\right]$. Taking the logarithm of the probability mass function,

$$
\ln P\left\{X=x\right\}=\ln\left(x-1\right)+2\ln\theta+\left(x-2\right)\ln\left(1-\theta\right).
$$

Differentiating with respect to $\theta$,

$$
\frac{\partial\ln P\left\{X=x\right\}}{\partial\theta}=\frac{2}{\theta}-\frac{x-2}{1-\theta}.
$$

By the conclusion of **Problem 1**, $I\left(\theta\right)=-E\left[\frac{\partial^2\ln f}{\partial\theta^2}\right]$. Differentiating once more,

$$
\frac{\partial^2\ln P\left\{X=x\right\}}{\partial\theta^2}=-\frac{2}{\theta^2}-\frac{x-2}{\left(1-\theta\right)^2}.
$$

This distribution is the negative binomial distribution $NB\left(r=2,\theta\right)$, whose mean is $E\left(X\right)=\frac{2}{\theta}$, so $E\left(X-2\right)=\frac{2}{\theta}-2=\frac{2\left(1-\theta\right)}{\theta}$. Hence

$$
I\left(\theta\right)=-E\left[-\frac{2}{\theta^2}-\frac{X-2}{\left(1-\theta\right)^2}\right]=\frac{2}{\theta^2}+\frac{E\left(X-2\right)}{\left(1-\theta\right)^2}=\frac{2}{\theta^2}+\frac{2\left(1-\theta\right)}{\theta\left(1-\theta\right)^2}=\frac{2}{\theta^2}+\frac{2}{\theta\left(1-\theta\right)}.
$$

Combining over a common denominator,

$$
I\left(\theta\right)=\frac{2\left(1-\theta\right)+2\theta}{\theta^2\left(1-\theta\right)}=\frac{2}{\theta^2\left(1-\theta\right)}.
$$

$\blacksquare$

### Problem 3

(Problem 3.6-4) Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and the density function of $X$ is

$$
f\left(x,\theta\right)=
\begin{cases}
\frac{1}{\theta}e^{-\frac{x}{\theta}},& x>0,\\[6pt\right]
0,& x\le0,
\end{cases}
$$

where $\theta>0$ is an unknown parameter. Find the uniformly minimum variance unbiased estimator of $\theta$, and prove that its variance equals the Cramér–Rao lower bound, i.e. it is an efficient estimator.

### Solution to Problem 3

By **Corollary 3.5.1** (Sufficient and Complete Statistic under the Natural Form of an Exponential Family), this density function can be written as

$$
f\left(x,\theta\right)=\frac{1}{\theta}\exp\left\{-\frac{x}{\theta}\right\}=\theta^{-1}\exp\left\{-\frac{1}{\theta}x\right\},\quad x>0,
$$

which is a one-parameter exponential family; the natural parameter space $\left\{-\frac{1}{\theta}:\theta>0\right\}=\left(-\infty,0\right)$ has an interior point, so $T=\sum_{i=1}^n X_i$ is a sufficient and complete statistic. This population is the exponential distribution $E\left(\frac{1}{\theta}\right)$, whose mean is $E\left(X\right)=\theta$. By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are independent and identically distributed, so

$$
E\left(\bar X\right)=\frac{1}{n}\sum_{i=1}^n E\left(X_i\right)=\theta.
$$

Since $\bar X=\frac{T}{n}$ is a function of the sufficient and complete statistic $T$ and is unbiased, by **Theorem 3.5.1** (L–S Theorem), $\bar X$ is the unique uniformly minimum variance unbiased estimator of $\theta$.

We now prove that $\bar X$ attains the Cramér–Rao lower bound. By **Definition 3.6.1** (Regular Distribution Family), the log-density is

$$
\ln f\left(x,\theta\right)=-\ln\theta-\frac{x}{\theta},\quad x>0.
$$

Differentiating with respect to $\theta$,

$$
\frac{\partial\ln f}{\partial\theta}=-\frac{1}{\theta}+\frac{x}{\theta^2}=\frac{x-\theta}{\theta^2}.
$$

Since $E\left(X\right)=\theta$ and $D\left(X\right)=\theta^2$,

$$
I\left(\theta\right)=E\left[\left(\frac{X-\theta}{\theta^2}\right)^2\right]=\frac{D\left(X\right)}{\theta^4}=\frac{\theta^2}{\theta^4}=\frac{1}{\theta^2}.
$$

By **Theorem 3.6.1** (One-parameter Cramér–Rao Inequality), for $g\left(\theta\right)=\theta$, $g'\left(\theta\right)=1$, the Cramér–Rao lower bound is

$$
\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)}=\frac{1}{n\cdot\frac{1}{\theta^2}}=\frac{\theta^2}{n}.
$$

On the other hand, the variance of $\bar X$ is

$$
D\left(\bar X\right)=\frac{1}{n}D\left(X\right)=\frac{\theta^2}{n}.
$$

Thus $D\left(\bar X\right)=\frac{\theta^2}{n}$ exactly equals the Cramér–Rao lower bound. By **Definition 3.6.3** (Efficient Estimator), $\bar X$ is an efficient estimator of $\theta$, and hence also a uniformly minimum variance unbiased estimator of $\theta$. $\blacksquare$

### Problem 4

(Problem 3.6-6) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,1\right)$, where $\mu\in\mathbb R$ is an unknown parameter. Prove:

(1) $\bar X^2-\frac{1}{n}$ is a uniformly minimum variance unbiased estimator of $\mu^2$;

(2) the variance of $\bar X^2-\frac{1}{n}$ is greater than the Cramér–Rao lower bound, i.e. it is not an efficient estimator.

### Solution to Problem 4

By **Corollary 3.5.1** (Sufficient and Complete Statistic under the Natural Form of an Exponential Family), the normal distribution family $N\left(\mu,1\right)$ is a one-parameter exponential family, whose density function is

$$
f\left(x,\mu\right)=\frac{1}{\sqrt{2\pi}}\exp\left\{-\frac{\left(x-\mu\right)^2}{2}\right\}=\frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}\exp\left\{\mu x-\frac{\mu^2}{2}\right\},
$$

and the natural parameter space $\left\{\mu:\mu\in\mathbb R\right\}$ has an interior point, so $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ is a sufficient and complete statistic for $\mu$.

(1) Prove that $\bar X^2-\frac{1}{n}$ is a uniformly minimum variance unbiased estimator of $\mu^2$. By **Sampling Distribution** (Sampling Distribution for a Normal Sample), $\bar X\sim N\left(\mu,\frac{1}{n}\right)$, so

$$
E\left(\bar X^2\right)=D\left(\bar X\right)+\left[E\left(\bar X\right)\right]^2=\frac{1}{n}+\mu^2.
$$

Hence

$$
E\left(\bar X^2-\frac{1}{n}\right)=E\left(\bar X^2\right)-\frac{1}{n}=\mu^2.
$$

Thus $\bar X^2-\frac{1}{n}$ is an unbiased estimator of $\mu^2$ and is a function of the sufficient and complete statistic $\bar X$; by **Theorem 3.5.1** (L–S Theorem), $\bar X^2-\frac{1}{n}$ is the unique uniformly minimum variance unbiased estimator of $\mu^2$.

(2) Prove that its variance is greater than the Cramér–Rao lower bound. First compute the variance of this estimator. Since $\bar X\sim N\left(\mu,\frac{1}{n}\right)$, let $Z=\sqrt n\,\bar X$, then $Z\sim N\left(\sqrt n\,\mu,1\right)$, i.e. $Z^2$ follows a noncentral $\chi^2$ distribution with $1$ degree of freedom and noncentrality parameter $\lambda=n\mu^2$. By the variance formula of the noncentral $\chi^2$ distribution, $D\left(Z^2\right)=2+4\lambda=2+4n\mu^2$. Also, $\bar X^2=\frac{Z^2}{n^2}$, so

$$
D\left(\bar X^2-\frac{1}{n}\right)=D\left(\bar X^2\right)=\frac{D\left(Z^2\right)}{n^2}=\frac{2+4n\mu^2}{n^2}=\frac{4\mu^2}{n}+\frac{2}{n^2}.
$$

Now compute the Cramér–Rao lower bound. By **Definition 3.6.1** (Regular Distribution Family), the log-density is

$$
\ln f\left(x,\mu\right)=-\frac{1}{2}\ln\left(2\pi\right)-\frac{\left(x-\mu\right)^2}{2}.
$$

Differentiating with respect to $\mu$,

$$
\frac{\partial\ln f}{\partial\mu}=x-\mu.
$$

Thus the Fisher information is

$$
I\left(\mu\right)=E\left[\left(X-\mu\right)^2\right]=D\left(X\right)=1.
$$

The function to be estimated is $g\left(\mu\right)=\mu^2$, with $g'\left(\mu\right)=2\mu$. By **Theorem 3.6.1** (One-parameter Cramér–Rao Inequality), the Cramér–Rao lower bound is

$$
\frac{\left[g'\left(\mu\right)\right]^2}{nI\left(\mu\right)}=\frac{\left(2\mu\right)^2}{n\cdot 1}=\frac{4\mu^2}{n}.
$$

Comparing the two:

$$
D\left(\bar X^2-\frac{1}{n}\right)=\frac{4\mu^2}{n}+\frac{2}{n^2}>\frac{4\mu^2}{n}=\text{C-R 下界}.
$$

The difference between the two is $\frac{2}{n^2}>0$, so the variance of $\bar X^2-\frac{1}{n}$ is strictly greater than the Cramér–Rao lower bound; by **Definition 3.6.3** (Efficient Estimator), it is not an efficient estimator. $\blacksquare$
