# Assignment 10

> **Definition 3.4.1** (Unbiased Estimator)<br>Let $\hat\theta=\hat\theta\left(X_1,X_2,\dots,X_n\right)$ be an estimator of the unknown parameter $\theta$. If for every $\theta\in\Theta$ one has $$E\left[\hat\theta\left(X_1,X_2,\dots,X_n\right)\right]=\theta,$$ then $\hat\theta$ is called an unbiased estimator of $\theta$. For an estimator $\hat g$ of $g\left(\theta\right)$, if $E\left[\hat g\right]=g\left(\theta\right)$, then $\hat g$ is called an unbiased estimator of $g\left(\theta\right)$.

> **Definition 3.4.2** (Efficiency)<br>Let both $\hat\theta_1$ and $\hat\theta_2$ be unbiased estimators of $\theta$. If for all $\theta\in\Theta$ one has $D\left(\hat\theta_1\right)\le D\left(\hat\theta_2\right)$, with the strict inequality holding for at least one $\theta$, then $\hat\theta_1$ is called more efficient than $\hat\theta_2$.

> **Definition 3.4.3** (Consistent Estimator)<br>For each natural number $n$, let $\hat\theta_n=\hat\theta_n\left(X_1,X_2,\dots,X_n\right)$ be an estimator of $\theta$. If for every $\theta\in\Theta$ and every $\varepsilon>0$ one has $$\lim_{n\to\infty}P\left\{\left|\hat\theta_n-\theta\right|\ge\varepsilon\right\}=0,$$ then $\hat\theta_n$ is called a (weakly) consistent estimator of $\theta$.

> **Basic Knowledge** (Chebyshev's Inequality and the Law of Large Numbers)<br>For any random variable $Y$ and $\varepsilon>0$, one has $P\left\{\left|Y-EY\right|\ge\varepsilon\right\}\le\frac{D\left(Y\right)}{\varepsilon^2}$; when the variables are independent and identically distributed with finite expectation, the law of large numbers gives $\bar X_n\xrightarrow{P}E\left(X\right)$; convergence in probability is preserved under the mapping by a continuous function.

### Problem 1

(Problem 3.4-1) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$. Find $c$ such that $c\sum_{i=1}^{n-1}\left(X_{i+1}-X_i\right)^2$ is an unbiased estimator of $\sigma^2$.

### Solution to Problem 1

By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are mutually independent and all follow $N\left(\mu,\sigma^2\right)$. Write the adjacent differences as $Y_i=X_{i+1}-X_i$, $i=1,2,\dots,n-1$. Since a linear combination of independent normal variables is still a normal variable,

$$
Y_i\sim N\left(0,\sigma^2+\sigma^2\right)=N\left(0,2\sigma^2\right),
$$

so $E\left(Y_i\right)=0$ and $E\left(Y_i^2\right)=D\left(Y_i\right)=2\sigma^2$. Hence

$$
E\left[c\sum_{i=1}^{n-1}\left(X_{i+1}-X_i\right)^2\right]=c\sum_{i=1}^{n-1}E\left(Y_i^2\right)=c\left(n-1\right)\cdot 2\sigma^2.
$$

By **Definition 3.4.1** (Unbiased Estimator), setting the above equal to $\sigma^2$ and solving gives

$$
c=\frac{1}{2\left(n-1\right)}.
$$

$\blacksquare$

### Problem 2

(Problem 3.4-5) Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and the density function of $X$ is

$$
f\left(x,\theta\right)=\begin{cases}e^{-\left(x-\theta\right)},&x>\theta,\\0,&\text{其他}.\end{cases}
$$

(1) Find the method of moments estimator $\hat\theta_1$ of the parameter $\theta$, and determine whether $\hat\theta_1$ is an unbiased estimator of $\theta$;

(2) Find the maximum likelihood estimator $\hat\theta_2$ of the parameter $\theta$, and determine whether $\hat\theta_2$ is an unbiased estimator of $\theta$.

### Solution to Problem 2

(1) From the density function, $X=\theta+Y$, where $Y\sim E\left(1\right)$ is the standard exponential distribution, so $E\left(X\right)=\theta+1$. Replacing the population moment by the sample moment and setting $\bar X=\theta+1$ gives the method of moments estimator

$$
\hat\theta_1=\bar X-1.
$$

From $E\left(\bar X\right)=E\left(X\right)=\theta+1$, we get $E\left(\hat\theta_1\right)=\left(\theta+1\right)-1=\theta$. By **Definition 3.4.1** (Unbiased Estimator), $\hat\theta_1=\bar X-1$ is an unbiased estimator of $\theta$.

(2) The likelihood function is

$$
L\left(\theta\right)=\prod_{i=1}^n e^{-\left(x_i-\theta\right)}=e^{-\sum_{i=1}^n\left(x_i-\theta\right)}=e^{-\sum_{i=1}^n x_i+n\theta},
$$

which is nonzero if and only if $\theta\le x_{\left(1\right)}$. By **Definition 3.3.2** (Maximum Likelihood Estimator), $L\left(\theta\right)=e^{n\theta}\cdot e^{-\sum x_i}$ is increasing in $\theta$, so the maximum is attained at the largest allowable $\theta$, namely

$$
\hat\theta_2=X_{\left(1\right)}=\min\left\{X_1,X_2,\dots,X_n\right\}.
$$

Since $X_i-\theta\sim E\left(1\right)$, the smallest order statistic satisfies $X_{\left(1\right)}-\theta\sim E\left(n\right)$, so $E\left(X_{\left(1\right)}-\theta\right)=\frac{1}{n}$, i.e. $E\left(\hat\theta_2\right)=\theta+\frac{1}{n}\ne\theta$. By **Definition 3.4.1** (Unbiased Estimator), $\hat\theta_2$ is not an unbiased estimator of $\theta$ (it is an asymptotically unbiased estimator).

$\blacksquare$

### Problem 3

(Problem 3.4-7) Let $X_1,X_2$ be a sample from the population $X$, and the density function of $X$ is

$$
f\left(x,\theta\right)=\begin{cases}k\theta^k x^{-\left(k+1\right)},&x>\theta,\\0,&\text{其他},\end{cases}
$$

where $k>2$ is known and $\theta>0$ is an unknown parameter.

(1) Prove that both $T_1=\frac{k-1}{2k}\left(X_1+X_2\right)$ and $T_2=\frac{2k-1}{2k}\min\left\{X_1,X_2\right\}$ are unbiased estimators of $\theta$;

(2) indicate which of $T_1$ and $T_2$ is more efficient.

### Solution to Problem 3

(1) First compute the first and second moments of $X$:

$$
E\left(X\right)=\int_\theta^{+\infty}x\cdot k\theta^k x^{-\left(k+1\right)}\,\mathrm{d}x=k\theta^k\int_\theta^{+\infty}x^{-k}\,\mathrm{d}x=\frac{k}{k-1}\theta.
$$

Hence

$$
E\left(T_1\right)=E\left[\frac{k-1}{2k}\left(X_1+X_2\right)\right]=\frac{k-1}{2k}\cdot 2\cdot\frac{k}{k-1}\theta=\theta.
$$

Write $X_{\left(1\right)}=\min\left\{X_1,X_2\right\}$; by independence, for $x>\theta$,

$$
P\left(X_{\left(1\right)}>x\right)=\left[P\left(X_1>x\right)\right]^2=\left(\frac{\theta}{x}\right)^{2k},
$$

so the density function of $X_{\left(1\right)}$ is $2k\theta^{2k}x^{-\left(2k+1\right)}$, and therefore

$$
E\left(X_{\left(1\right)}\right)=\int_\theta^{+\infty}x\cdot 2k\theta^{2k}x^{-\left(2k+1\right)}\,\mathrm{d}x=\frac{2k}{2k-1}\theta.
$$

Hence

$$
E\left(T_2\right)=E\left[\frac{2k-1}{2k}X_{\left(1\right)}\right]=\frac{2k-1}{2k}\cdot\frac{2k}{2k-1}\theta=\theta.
$$

By **Definition 3.4.1** (Unbiased Estimator), both $T_1$ and $T_2$ are unbiased estimators of $\theta$.

(2) Now compare the variances. From

$$
E\left(X^2\right)=\int_\theta^{+\infty}x^2\cdot k\theta^k x^{-\left(k+1\right)}\,\mathrm{d}x=\frac{k}{k-2}\theta^2,
$$

we get

$$
D\left(X\right)=E\left(X^2\right)-\left[E\left(X\right)\right]^2=\frac{k}{k-2}\theta^2-\frac{k^2}{\left(k-1\right)^2}\theta^2=\frac{k\theta^2}{\left(k-1\right)^2\left(k-2\right)}.
$$

Hence

$$
D\left(T_1\right)=\left(\frac{k-1}{2k}\right)^2\cdot 2D\left(X\right)=\frac{\left(k-1\right)^2}{4k^2}\cdot\frac{2k\theta^2}{\left(k-1\right)^2\left(k-2\right)}=\frac{\theta^2}{2k\left(k-2\right)}.
$$

Also,

$$
E\left(X_{\left(1\right)}^2\right)=\int_\theta^{+\infty}x^2\cdot 2k\theta^{2k}x^{-\left(2k+1\right)}\,\mathrm{d}x=\frac{2k}{2k-2}\theta^2=\frac{k}{k-1}\theta^2,
$$

so

$$
D\left(T_2\right)=\left(\frac{2k-1}{2k}\right)^2\left[E\left(X_{\left(1\right)}^2\right)-\left(E\left(X_{\left(1\right)}\right)\right)^2\right]=\frac{\theta^2}{4k\left(k-1\right)}.
$$

Since $4k\left(k-1\right)>2k\left(k-2\right)$ ($k>2$), we have $D\left(T_2\right)<D\left(T_1\right)$. By **Definition 3.4.2** (Efficiency), $T_2$ is more efficient than $T_1$.

$\blacksquare$

### Problem 4

(Problem 3.4-10) Let $\hat\theta_n$ be an estimator of $\theta$. Prove that if, as $n\to+\infty$, $E\left(\hat\theta_n\right)\to\theta$ and $D\left(\hat\theta_n\right)\to0$, then $\hat\theta_n$ is a consistent estimator of $\theta$.

### Solution to Problem 4

By **Basic Knowledge** (Chebyshev's Inequality), for any $\varepsilon>0$,

$$
P\left\{\left|\hat\theta_n-\theta\right|\ge\varepsilon\right\}\le\frac{E\left[\left(\hat\theta_n-\theta\right)^2\right]}{\varepsilon^2}.
$$

Decompose the mean squared error into the sum of the variance and the squared bias:

$$
E\left[\left(\hat\theta_n-\theta\right)^2\right]=D\left(\hat\theta_n\right)+\left[E\left(\hat\theta_n\right)-\theta\right]^2.
$$

By the assumptions $E\left(\hat\theta_n\right)\to\theta$ and $D\left(\hat\theta_n\right)\to0$, we have $E\left[\left(\hat\theta_n-\theta\right)^2\right]\to0$, and hence

$$
\lim_{n\to\infty}P\left\{\left|\hat\theta_n-\theta\right|\ge\varepsilon\right\}=0.
$$

By **Definition 3.4.3** (Consistent Estimator), $\hat\theta_n$ is a consistent estimator of $\theta$.

$\blacksquare$

### Problem 5

(Problem 3.4-12) Let $X_1,X_2,\dots,X_n$ be a sample from the uniform distribution $U\left[0,\theta\right]$, $\theta>0$. Prove that $\sqrt\left[n\right]{X_1X_2\cdots X_n}$ is a consistent estimator of $\theta/e$.

### Solution to Problem 5

Letting $U_i=\frac{X_i}{\theta}$, then $U_1,U_2,\dots,U_n$ are mutually independent and all follow $U\left[0,1\right]$. For $U\sim U\left[0,1\right]$,

$$
E\left[\ln U\right]=\int_0^1\ln u\,\mathrm{d}u=\left[u\ln u-u\right]_0^1=-1.
$$

Write $Z_i=\ln U_i$, then $Z_1,Z_2,\dots,Z_n$ are mutually independent, with $E\left(Z_i\right)=-1$. By **Basic Knowledge** (Law of Large Numbers),

$$
\frac{1}{n}\sum_{i=1}^n Z_i\xrightarrow{P}-1.
$$

Moreover,

$$
\frac{1}{n}\sum_{i=1}^n\ln X_i=\ln\theta+\frac{1}{n}\sum_{i=1}^n\ln U_i=\ln\theta+\frac{1}{n}\sum_{i=1}^n Z_i\xrightarrow{P}\ln\theta-1=\ln\frac{\theta}{e}.
$$

Since convergence in probability is preserved under the mapping by a continuous function,

$$
\sqrt\left[n\right]{X_1X_2\cdots X_n}=\exp\left(\frac{1}{n}\sum_{i=1}^n\ln X_i\right)\xrightarrow{P}\exp\left(\ln\frac{\theta}{e}\right)=\frac{\theta}{e}.
$$

By **Definition 3.4.3** (Consistent Estimator), $\sqrt\left[n\right]{X_1X_2\cdots X_n}$ is a consistent estimator of $\theta/e$.

$\blacksquare$
