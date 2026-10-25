# Assignment 11

> **Lemma 3.5.1** (Method for Improving an Unbiased Estimator)<br>Let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a sufficient statistic, and let $\hat g\left(X_1,X_2,\dots,X_n\right)$ be an unbiased estimator of $g\left(\theta\right)$. Then $h\left(T\right)=E\left[\hat g\left(X_1,X_2,\dots,X_n\right)\mid T\right]$ is an unbiased estimator of $g\left(\theta\right)$, and for any $\theta$, $D\left[h\left(T\right)\right]\le D\left[\hat g\left(X_1,X_2,\dots,X_n\right)\right]$, with equality if and only if $\hat g\left(X_1,X_2,\dots,X_n\right)=h\left(T\right)$ almost everywhere.

> **Theorem 3.5.1** (Lehmann–Scheffé Theorem, abbreviated as L–S Theorem)<br>Let $T\left(X\right)=T\left(X_1,X_2,\dots,X_n\right)$ be a sufficient and complete statistic. If $g\left(T\left(X\right)\right)$ is an unbiased estimator of $g\left(\theta\right)$, then $g\left(T\left(X\right)\right)$ is the unique uniformly minimum variance unbiased estimator of $g\left(\theta\right)$.

> **Corollary 3.5.1** (Sufficient and Complete Statistic under the Natural Form of an Exponential Family)<br>Let the distribution of the sample be in the natural form of an exponential family $f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k\theta_iT_i\left(x\right)\right\}h\left(x\right)$. If the natural parameter space, as a subset of $\mathbb R^k$, has an interior point, then $T\left(X\right)=\left(T_1\left(X\right),\dots,T_k\left(X\right)\right)$ is a sufficient and complete statistic; in this case, if $h\left(T\left(X\right)\right)$ is an unbiased estimator of $g\left(\theta\right)$, then it is the unique uniformly minimum variance unbiased estimator of $g\left(\theta\right)$.

> **Example 3.5.3** (Sufficient and Complete Statistic for the Two-point Distribution)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the two-point distribution $B\left(1,p\right)$, $0< p< 1$. Then $T\left(X_1,X_2,\dots,X_n\right)=\sum_{i=1}^n X_i\sim B\left(n,p\right)$ is a sufficient and complete statistic for $p$, and $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ is the unique uniformly minimum variance unbiased estimator of $p$.

> **Example 3.5.7** (Sufficient and Complete Statistic for a Normal Population)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, $\mu\in\mathbb R,\ \sigma^2> 0$. Then $T\left(X\right)=\left(\bar X,\sum_{i=1}^n\left(X_i-\bar X\right)^2\right)$ is a sufficient and complete statistic for $\left(\mu,\sigma^2\right)$, where $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$.

> **Sampling Distribution** (Sampling Distribution for a Normal Sample)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, and write $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ and $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$. Then $\bar X\sim N\left(\mu,\frac{\sigma^2}{n}\right)$, $\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$, and $\bar X$ and $S^2$ are mutually independent. In particular, when $\mu=0$, $T=\sum_{i=1}^n X_i^2=\sigma^2\cdot\frac{\sum_{i=1}^n X_i^2}{\sigma^2}\sim\sigma^2\chi^2\left(n\right)$.

> **Basic Knowledge** (Moments of the $\chi^2$ Distribution)<br>If $Y\sim\chi^2\left(k\right)$, then $E\left(Y\right)=k$, $D\left(Y\right)=2k$, $E\left(Y^2\right)=k\left(k+2\right)$, $E\left(\frac{1}{Y}\right)=\frac{1}{k-2}\ \left(k> 2\right)$, and $E\left(\sqrt Y\right)=\sqrt 2\,\frac{\Gamma\left(\frac{k+1}{2}\right)}{\Gamma\left(\frac{k}{2}\right)}$.

### Problem 1

(Problem 3.5-4) Let $X_1,X_2,\dots,X_n$ be a sample from a two-point-distribution population $B\left(1,p\right)$, $0< p< 1$, where $0< p< 1$ is an unknown parameter:

(1) Find the uniformly minimum variance unbiased estimator of $p^m$, where $m> 0$ is a natural number;

(2) Find the uniformly minimum variance unbiased estimator of $p\left(1-p\right)$.

### Solution to Problem 1

By **Example 3.5.3** (Sufficient and Complete Statistic for the Two-point Distribution), $T=\sum_{i=1}^n X_i\sim B\left(n,p\right)$ is a sufficient and complete statistic for $p$. By **Theorem 3.5.1** (L–S Theorem), as long as one finds a function $h\left(T\right)$ of $T$ that is an unbiased estimator of the function to be estimated, it is the unique uniformly minimum variance unbiased estimator of that function.

(1) We wish to estimate $g\left(p\right)=p^m$. Let $h\left(T\right)$ satisfy $E\left[h\left(T\right)\right]=p^m$. Since $T\sim B\left(n,p\right)$, its probability mass function is $P\left\{T=t\right\}=\binom{n}{t}p^t\left(1-p\right)^{n-t}$, $t=0,1,\dots,n$. Take

$$
h\left(t\right)=
\begin{cases}
\frac{\binom{n-m}{t-m}}{\binom{n}{t}},& t=m,m+1,\dots,n,\\[6pt\right]
0,& t=0,1,\dots,m-1.
\end{cases}
$$

Then for any $0< p< 1$,

$$
E\left[h\left(T\right)\right]=\sum_{t=m}^n\frac{\binom{n-m}{t-m}}{\binom{n}{t}}\binom{n}{t}p^t\left(1-p\right)^{n-t}=\sum_{t=m}^n\binom{n-m}{t-m}p^t\left(1-p\right)^{n-t}.
$$

Letting $s=t-m$, by the binomial theorem,

$$
E\left[h\left(T\right)\right]=p^m\sum_{s=0}^{n-m}\binom{n-m}{s}p^s\left(1-p\right)^{n-m-s}=p^m\left[p+\left(1-p\right)\right]^{n-m}=p^m.
$$

Hence $h\left(T\right)$ is an unbiased estimator of $p^m$ and is a function of the sufficient and complete statistic $T$; by **Theorem 3.5.1** (L–S Theorem), the unique uniformly minimum variance unbiased estimator of $p^m$ is

$$
\hat g_1=
\begin{cases}
\frac{\binom{n-m}{T-m}}{\binom{n}{T}},& T=m,m+1,\dots,n,\\[6pt\right]
0,& T=0,1,\dots,m-1,
\end{cases}\quad T=\sum_{i=1}^n X_i.
$$

(2) We wish to estimate $g\left(p\right)=p\left(1-p\right)$. By **Example 3.5.4** (already derived by the undetermined-coefficient method in the textbook), an unbiased estimator of $g\left(p\right)=p\left(1-p\right)$ is $g\left(T\right)=\frac{T\left(n-T\right)}{n\left(n-1\right)}$. Verify its unbiasedness: since $T\sim B\left(n,p\right)$, $E\left(T\right)=np$ and $D\left(T\right)=np\left(1-p\right)$, so

$$
E\left[T\left(n-T\right)\right]=nE\left(T\right)-E\left(T^2\right)=n^2p-\left[D\left(T\right)+\left(E\left(T\right)\right)^2\right]=n^2p-\left[np\left(1-p\right)+n^2p^2\right]=n\left(n-1\right)p\left(1-p\right).
$$

Hence $E\left[\frac{T\left(n-T\right)}{n\left(n-1\right)}\right]=p\left(1-p\right)$. Also, $\frac{T\left(n-T\right)}{n\left(n-1\right)}$ is a function of the sufficient and complete statistic $T$; by **Theorem 3.5.1** (L–S Theorem), the unique uniformly minimum variance unbiased estimator of $p\left(1-p\right)$ is

$$
\hat g_2=\frac{T\left(n-T\right)}{n\left(n-1\right)},\quad T=\sum_{i=1}^n X_i.
$$

$\blacksquare$

### Problem 2

(Problem 3.5-6) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(0,\sigma^2\right)$, where $\sigma> 0$ is an unknown parameter. Find respectively the uniformly minimum variance unbiased estimators of $\sigma$ and $\sigma^4$.

### Solution to Problem 2

By **Corollary 3.5.1** (Sufficient and Complete Statistic under the Natural Form of an Exponential Family), the normal distribution family $N\left(0,\sigma^2\right)$ is a one-parameter exponential family, whose density function can be written as

$$
f\left(x;\sigma^2\right)=\frac{1}{\sqrt{2\pi}\sigma}\exp\left\{-\frac{x^2}{2\sigma^2}\right\}=\frac{1}{\sqrt{2\pi}}\left(\sigma^2\right)^{-\frac{1}{2}}\exp\left\{-\frac{1}{2\sigma^2}x^2\right\}.
$$

The natural parameter space $\left\{-\frac{1}{2\sigma^2}: \sigma> 0\right\}=\left(-\infty,0\right)$, as a subset of $\mathbb R$, has an interior point, so $T=\sum_{i=1}^n X_i^2$ is a sufficient and complete statistic. By **Sampling Distribution** (Sampling Distribution for a Normal Sample), $\frac{T}{\sigma^2}=\sum_{i=1}^n\left(\frac{X_i}{\sigma}\right)^2\sim\chi^2\left(n\right)$.

(1) Find the uniformly minimum variance unbiased estimator of $\sigma$. By **Basic Knowledge** (Moments of the $\chi^2$ Distribution), if $Y\sim\chi^2\left(n\right)$, then $E\left(\sqrt Y\right)=\sqrt 2\,\frac{\Gamma\left(\frac{n+1}{2}\right)}{\Gamma\left(\frac{n}{2}\right)}$. Letting $Y=\frac{T}{\sigma^2}$, then

$$
E\left(\sqrt T\right)=\sigma E\left(\sqrt Y\right)=\sigma\sqrt 2\,\frac{\Gamma\left(\frac{n+1}{2}\right)}{\Gamma\left(\frac{n}{2}\right)}.
$$

Hence

$$
E\left[\frac{\Gamma\left(\frac{n}{2}\right)}{\sqrt 2\,\Gamma\left(\frac{n+1}{2}\right)}\sqrt T\right]=\sigma.
$$

This estimator is a function of the sufficient and complete statistic $T$ and is unbiased; by **Theorem 3.5.1** (L–S Theorem), the unique uniformly minimum variance unbiased estimator of $\sigma$ is

$$
\hat\sigma=\frac{\Gamma\left(\frac{n}{2}\right)}{\sqrt 2\,\Gamma\left(\frac{n+1}{2}\right)}\sqrt T,\quad T=\sum_{i=1}^n X_i^2.
$$

(2) Find the uniformly minimum variance unbiased estimator of $\sigma^4$. By **Basic Knowledge** (Moments of the $\chi^2$ Distribution), if $Y\sim\chi^2\left(n\right)$, then $E\left(Y^2\right)=n\left(n+2\right)$. Since $T=\sigma^2Y$,

$$
E\left(T^2\right)=\sigma^4 E\left(Y^2\right)=\sigma^4 n\left(n+2\right).
$$

Hence $E\left[\frac{T^2}{n\left(n+2\right)}\right]=\sigma^4$. This estimator is a function of the sufficient and complete statistic $T$ and is unbiased; by **Theorem 3.5.1** (L–S Theorem), the unique uniformly minimum variance unbiased estimator of $\sigma^4$ is

$$
\widehat{\sigma^4}=\frac{T^2}{n\left(n+2\right)},\quad T=\sum_{i=1}^n X_i^2.
$$

$\blacksquare$

### Problem 3

(Problem 3.5-7) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, where $\mu\in\mathbb R$ and $\sigma> 0$ are both unknown parameters:

(1) Find respectively the uniformly minimum variance unbiased estimators of $\mu+\sigma^2$ and $\frac{\mu^2}{\sigma^2}$;

(2) Prove that $\hat\mu^2=\bar X^2-\frac{S^2}{n}$ is a uniformly minimum variance unbiased estimator of $\mu^2$.

### Solution to Problem 3

By **Example 3.5.7** (Sufficient and Complete Statistic for a Normal Population), $T\left(X\right)=\left(\bar X,\sum_{i=1}^n\left(X_i-\bar X\right)^2\right)$ is a sufficient and complete statistic for $\left(\mu,\sigma^2\right)$, where $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ and $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$. By **Sampling Distribution** (Sampling Distribution for a Normal Sample), $\bar X\sim N\left(\mu,\frac{\sigma^2}{n}\right)$, $\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$, and $\bar X$ and $S^2$ are mutually independent. By **Theorem 3.5.1** (L–S Theorem), any unbiased estimator of the function to be estimated that is a function of $\left(\bar X,S^2\right)$ is a uniformly minimum variance unbiased estimator.

(1) First find the uniformly minimum variance unbiased estimator of $\mu+\sigma^2$. From $E\left(\bar X\right)=\mu$ and $E\left(S^2\right)=\sigma^2$, we get

$$
E\left(\bar X+S^2\right)=E\left(\bar X\right)+E\left(S^2\right)=\mu+\sigma^2.
$$

Since $\bar X+S^2$ is a function of the sufficient and complete statistic $\left(\bar X,S^2\right)$ and is unbiased, by **Theorem 3.5.1** (L–S Theorem), the unique uniformly minimum variance unbiased estimator of $\mu+\sigma^2$ is $\bar X+S^2$.

Next find the uniformly minimum variance unbiased estimator of $\frac{\mu^2}{\sigma^2}$. Since $\bar X$ and $S^2$ are independent, and $E\left(\bar X^2\right)=D\left(\bar X\right)+\left(E\bar X\right)^2=\sigma^2/n+\mu^2$; by **Basic Knowledge** (Moments of the $\chi^2$ Distribution), $\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$, so when $n> 3$,

$$
E\left(\frac{1}{S^2}\right)=\frac{n-1}{\sigma^2}E\left[\frac{1}{\frac{\left(n-1\right)S^2}{\sigma^2}}\right]=\frac{n-1}{\sigma^2}\cdot\frac{1}{\left(n-1\right)-2}=\frac{n-1}{\sigma^2\left(n-3\right)}.
$$

Hence, by independence,

$$
E\left(\frac{\bar X^2}{S^2}\right)=E\left(\bar X^2\right)E\left(\frac{1}{S^2}\right)=\left(\mu^2+\frac{\sigma^2}{n}\right)\cdot\frac{n-1}{\sigma^2\left(n-3\right)}.
$$

Multiplying both sides by $\frac{n-3}{n-1}$ gives

$$
E\left[\frac{n-3}{n-1}\cdot\frac{\bar X^2}{S^2}\right]=\frac{\mu^2}{\sigma^2}+\frac{1}{n}.
$$

Therefore

$$
E\left[\frac{\left(n-3\right)\bar X^2}{\left(n-1\right)S^2}-\frac{1}{n}\right]=\frac{\mu^2}{\sigma^2}.
$$

This estimator is a function of the sufficient and complete statistic $\left(\bar X,S^2\right)$ and is unbiased; by **Theorem 3.5.1** (L–S Theorem), the unique uniformly minimum variance unbiased estimator of $\frac{\mu^2}{\sigma^2}$ is

$$
\frac{\left(n-3\right)\bar X^2}{\left(n-1\right)S^2}-\frac{1}{n}\quad\left(n> 3\right).
$$

(2) Prove that $\hat\mu^2=\bar X^2-\frac{S^2}{n}$ is a uniformly minimum variance unbiased estimator of $\mu^2$. From $E\left(\bar X^2\right)=\mu^2+\frac{\sigma^2}{n}$ and $E\left(S^2\right)=\sigma^2$, we get

$$
E\left(\bar X^2-\frac{S^2}{n}\right)=E\left(\bar X^2\right)-\frac{1}{n}E\left(S^2\right)=\mu^2+\frac{\sigma^2}{n}-\frac{\sigma^2}{n}=\mu^2.
$$

Hence $\bar X^2-\frac{S^2}{n}$ is an unbiased estimator of $\mu^2$ and is a function of the sufficient and complete statistic $\left(\bar X,S^2\right)$; by **Theorem 3.5.1** (L–S Theorem), $\hat\mu^2=\bar X^2-\frac{S^2}{n}$ is the unique uniformly minimum variance unbiased estimator of $\mu^2$. $\blacksquare$
