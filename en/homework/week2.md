# Assignment 2

> **Sampling Distribution** (Definition)<br>A statistic is a function of the sample $X_1,X_2,\dots,X_n$, and the sample $X_1,X_2,\dots,X_n$ are random variables. Hence a statistic is also a random variable, and the distribution of a statistic is called a sampling distribution.

> **Theorem** (Distribution of Order Statistics)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, let the distribution function of $X$ be $F\left(x\right)$, and let $\left(X_{\left(1\right)},X_{\left(2\right)},\dots,X_{\left(n\right)}\right)$ be its order statistics. Then for $1\le r\le n$, the distribution function of $X_{\left(r\right)}$ is $$F_{\left(r\right)}\left(x\right)=P\left\{X_{\left(r\right)}\le x\right\}=\sum_{k=r}^n\binom{n}{k}\left[F\left(x\right)\right]^k\left[1-F\left(x\right)\right]^{n-k}=r\binom{n}{r}\int_0^{F\left(x\right)}t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t.$$ If the population $X$ is continuous with density function $f\left(x\right)$, then the density function of $X_{\left(r\right)}$ is $$f_{\left(r\right)}\left(x\right)=F_{\left(r\right)}'\left(x\right)=r\binom{n}{r}\left[F\left(x\right)\right]^{r-1}\left[1-F\left(x\right)\right]^{n-r}f\left(x\right).$$ In particular, when $r=1$, the distribution function and density function of the smallest order statistic $X_{\left(1\right)}$ are respectively $$F_{\left(1\right)}\left(x\right)=1-\left[1-F\left(x\right)\right]^n,\quad f_{\left(1\right)}\left(x\right)=n\left[1-F\left(x\right)\right]^{n-1}f\left(x\right);$$ when $r=n$, the distribution function and density function of the largest order statistic $X_{\left(n\right)}$ are respectively $$F_{\left(n\right)}\left(x\right)=\left[F\left(x\right)\right]^n,\quad f_{\left(n\right)}\left(x\right)=n\left[F\left(x\right)\right]^{n-1}f\left(x\right).$$

> **Basic Knowledge** (Additivity of the Poisson Distribution)<br>Let $X_1,X_2,\dots,X_n$ be mutually independent, with $X_i\sim P\left(\lambda_i\right)$. Then $\sum_{i=1}^n X_i\sim P\left(\sum_{i=1}^n\lambda_i\right)$.

> **Basic Knowledge** (Additivity of the Normal Distribution)<br>Let $X_1,X_2,\dots,X_n$ be mutually independent, with $X_i\sim N\left(\mu_i,\sigma_i^2\right)$. Then $\sum_{i=1}^n X_i\sim N\left(\sum_{i=1}^n\mu_i,\sum_{i=1}^n\sigma_i^2\right)$.

### Problem 1

(Problem 2.1-1) Let $X_1,X_2,\dots,X_n$ be a sample from a Poisson-distributed population $P\left(\lambda\right)$, with probability mass function $P\left\{X=x\right\}=\frac{\lambda^x}{x!}e^{-\lambda},\ x=0,1,2,\dots$, where $\lambda> 0$. Find the sampling distribution of $T=\sum_{i=1}^n X_i$.

### Solution to Problem 1

By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are mutually independent and each $X_i\sim P\left(\lambda\right)$. By **Basic Knowledge** (Additivity of the Poisson Distribution), the sum of independent Poisson variables still follows a Poisson distribution with the parameters added, so
$$
T=\sum_{i=1}^n X_i\sim P\left(n\lambda\right).
$$

That is, the probability mass function of $T$ is
$$
P\left\{T=t\right\}=\frac{\left(n\lambda\right)^t}{t!}e^{-n\lambda},\quad t=0,1,2,\dots
$$

$\blacksquare$

### Problem 2

(Problem 2.1-2) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, $\mu\in\mathbb R,\ \sigma^2> 0$. Find the sampling distribution of $T=\sum_{i=1}^n X_i$.

### Solution to Problem 2

By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are mutually independent and each $X_i\sim N\left(\mu,\sigma^2\right)$. By **Basic Knowledge** (Additivity of the Normal Distribution), the sum of independent normal variables still follows a normal distribution with the means and variances added respectively, so
$$
T=\sum_{i=1}^n X_i\sim N\left(n\mu,n\sigma^2\right).
$$

$\blacksquare$

### Problem 3

(Problem 2.1-3) Let $X\sim B\left(n,p\right)$, $0< p< 1$. For $r\ge1$, prove:
$$
P\left\{X\ge r\right\}=\sum_{k=r}^n\binom{n}{k}p^k\left(1-p\right)^{n-k}=r\binom{n}{r}\int_0^p t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t.
$$

### Solution to Problem 3

Write $G\left(p\right)=\sum_{k=r}^n\binom{n}{k}p^k\left(1-p\right)^{n-k}$, where $r\ge1$. Differentiating with respect to $p$ gives
$$
G'\left(p\right)=\sum_{k=r}^n\binom{n}{k}\left[kp^{k-1}\left(1-p\right)^{n-k}-\left(n-k\right)p^k\left(1-p\right)^{n-k-1}\right].
$$

Using the identities $k\binom{n}{k}=n\binom{n-1}{k-1}$ and $\left(n-k\right)\binom{n}{k}=n\binom{n-1}{k}$, the above becomes
$$
G'\left(p\right)=\sum_{k=r}^n n\binom{n-1}{k-1}p^{k-1}\left(1-p\right)^{n-k}-\sum_{k=r}^n n\binom{n-1}{k}p^k\left(1-p\right)^{n-k-1}.
$$

Setting $j=k-1$ in the first term, $j$ runs from $r-1$ to $n-1$; setting $j=k$ in the second term, $j$ runs from $r$ to $n$. The two expressions cancel term by term except for the first term $j=r-1$, so
$$
G'\left(p\right)=n\binom{n-1}{r-1}p^{r-1}\left(1-p\right)^{n-r}=r\binom{n}{r}p^{r-1}\left(1-p\right)^{n-r},
$$

where we used $n\binom{n-1}{r-1}=r\binom{n}{r}$. Also, since $r\ge1$, $G\left(0\right)=\sum_{k=r}^n\binom{n}{k}0^k\cdot1=0$, so by the Newton–Leibniz formula,
$$
G\left(p\right)=\int_0^p G'\left(t\right)\,\mathrm{d}t=r\binom{n}{r}\int_0^p t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t.
$$

That is, $P\left\{X\ge r\right\}=\sum_{k=r}^n\binom{n}{k}p^k\left(1-p\right)^{n-k}=r\binom{n}{r}\int_0^p t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t$. $\blacksquare$

### Problem 4

(Problem 2.1-5) Let $X_1,X_2,\dots,X_n$ be a sample from an exponential-distribution population $E\left(\lambda\right)$, whose density function is
$$
f\left(x\right)=\begin{cases}\lambda e^{-\lambda x},&x> 0,\\0,&x\le0,\end{cases}
$$
where $\lambda> 0$. Find:

(1) the density function of $X_{\left(1\right)}$;

(2) $E\left(X_{\left(1\right)}\right),D\left(X_{\left(1\right)}\right)$.

### Solution to Problem 4

The distribution function of the exponential distribution $E\left(\lambda\right)$ is $F\left(x\right)=1-e^{-\lambda x}\left(x> 0\right)$, and its density function is $f\left(x\right)=\lambda e^{-\lambda x}\left(x> 0\right)$.

(1) By **Theorem** (Distribution of Order Statistics), the density function of the smallest order statistic $X_{\left(1\right)}$ is
$$
f_{\left(1\right)}\left(x\right)=n\left[1-F\left(x\right)\right]^{n-1}f\left(x\right)=n\left(e^{-\lambda x}\right)^{n-1}\cdot\lambda e^{-\lambda x}=n\lambda e^{-n\lambda x},\quad x> 0.
$$

Hence $X_{\left(1\right)}\sim E\left(n\lambda\right)$, i.e. $X_{\left(1\right)}$ follows the exponential distribution with parameter $n\lambda$.

(2) By the expectation and variance formula of the exponential distribution, $E\left(X_{\left(1\right)}\right)=\frac{1}{n\lambda}$ and $D\left(X_{\left(1\right)}\right)=\frac{1}{\left(n\lambda\right)^2}$. $\blacksquare$

### Problem 5

(Problem 2.1-6) Let $X_1,X_2,\dots,X_9$ be a sample from the normal population $N\left(1,9\right)$. Find:

(1) $P\left\{X_{\left(1\right)}> 4\right\}$;

(2) $P\left\{X_{\left(9\right)}< 4\right\}$.

### Solution to Problem 5

The population $X\sim N\left(1,9\right)$, so the distribution function of $X$ is $F\left(x\right)=\Phi\left(\frac{x-1}{3}\right)$, where $\Phi$ is the standard normal distribution function.

(1) $X_{\left(1\right)}=\min\left\{X_1,\dots,X_9\right\}$, so $X_{\left(1\right)}> 4$ if and only if every $X_i> 4$. By **Definition 1.3.2** (Simple Random Sample), $X_1,\dots,X_9$ are mutually independent and identically distributed, so
$$
P\left\{X_{\left(1\right)}> 4\right\}=P\left\{X_1> 4,\dots,X_9> 4\right\}=\left[P\left\{X_1> 4\right\}\right]^9=\left[1-F\left(4\right)\right]^9=\left[1-\Phi\left(1\right)\right]^9.
$$

(2) $X_{\left(9\right)}=\max\left\{X_1,\dots,X_9\right\}$, so $X_{\left(9\right)}< 4$ if and only if every $X_i< 4$. By independence,
$$
P\left\{X_{\left(9\right)}< 4\right\}=P\left\{X_1< 4,\dots,X_9< 4\right\}=\left[F\left(4\right)\right]^9=\left[\Phi\left(1\right)\right]^9.
$$

$\blacksquare$

### Problem 6

(Problem 2.1-7) Let $X_1,X_2,\dots,X_n$ be a sample from a uniform-distribution population $U\left[\theta_1,\theta_2\right]$, $\theta_1< \theta_2$. Find respectively the density functions of the order statistics $X_{\left(1\right)},X_{\left(n\right)}$.

### Solution to Problem 6

The density function and distribution function of the uniform distribution $U\left[\theta_1,\theta_2\right]$ are respectively
$$
f\left(x\right)=\begin{cases}\frac{1}{\theta_2-\theta_1},&\theta_1\le x\le\theta_2,\\0,&\text{其他},\end{cases}\quad F\left(x\right)=\begin{cases}0,&x< \theta_1,\\\frac{x-\theta_1}{\theta_2-\theta_1},&\theta_1\le x\le\theta_2,\\1,&x> \theta_2.\end{cases}
$$

By **Theorem** (Distribution of Order Statistics), the density function of the smallest order statistic $X_{\left(1\right)}$ is
$$
f_{\left(1\right)}\left(x\right)=n\left[1-F\left(x\right)\right]^{n-1}f\left(x\right)=n\left(\frac{\theta_2-x}{\theta_2-\theta_1}\right)^{n-1}\cdot\frac{1}{\theta_2-\theta_1}=\frac{n\left(\theta_2-x\right)^{n-1}}{\left(\theta_2-\theta_1\right)^n},\quad \theta_1\le x\le\theta_2.
$$

The density function of the largest order statistic $X_{\left(n\right)}$ is
$$
f_{\left(n\right)}\left(x\right)=n\left[F\left(x\right)\right]^{n-1}f\left(x\right)=n\left(\frac{x-\theta_1}{\theta_2-\theta_1}\right)^{n-1}\cdot\frac{1}{\theta_2-\theta_1}=\frac{n\left(x-\theta_1\right)^{n-1}}{\left(\theta_2-\theta_1\right)^n},\quad \theta_1\le x\le\theta_2.
$$

$\blacksquare$
