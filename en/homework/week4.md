# Assignment 4

> **Lemma 2.3.1** (Expectations of the Sample Mean and Sample Variance)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, with $E\left(X\right)=\mu$, $D\left(X\right)=\sigma^2$, and let $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ and $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$ be the sample mean and the sample variance respectively. Then $$E\left(\bar X\right)=\mu,\quad D\left(\bar X\right)=\frac{\sigma^2}{n},\quad E\left(S^2\right)=\sigma^2.$$

> **Theorem 2.3.3** (Distributions of the Sample Mean and Sample Variance of a Normal Population)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, and let $\bar X$ and $S^2$ be the sample mean and the sample variance respectively. Then:<br>(1) $\bar X\sim N\left(\mu,\sigma^2/n\right)$, i.e. $\frac{\bar X-\mu}{\sigma/\sqrt n}\sim N\left(0,1\right)$;<br>(2) $\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$;<br>(3) $\bar X$ and $S^2$ are mutually independent.

> **Theorem 2.3.4**<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$. Then $$\frac{1}{\sigma^2}\sum_{i=1}^n\left(X_i-\mu\right)^2\sim\chi^2\left(n\right).$$

> **Definition 2.2.2** ($t$ Distribution)<br>Let the random variables $X\sim N\left(0,1\right)$ and $Y\sim\chi^2\left(n\right)$, with $X$ and $Y$ mutually independent. Then $T=\frac{X}{\sqrt{Y/n}}$ is called a $t$ variable with $n$ degrees of freedom, denoted by $T\sim t\left(n\right)$.

> **Definition 2.2.3** ($F$ Distribution)<br>Let the random variables $X\sim\chi^2\left(m\right)$ and $Y\sim\chi^2\left(n\right)$, with $X$ and $Y$ mutually independent. Then $F=\frac{X/m}{Y/n}$ is called an $F$ variable with degrees of freedom $m$ and $n$, denoted by $F\sim F\left(m,n\right)$.

> **Properties of the $\chi^2$ Distribution** (Additivity)<br>Let $X_1\sim\chi^2\left(n_1\right)$ and $X_2\sim\chi^2\left(n_2\right)$, with $X_1$ and $X_2$ mutually independent. Then $X_1+X_2\sim\chi^2\left(n_1+n_2\right)$.

> **Basic Knowledge** (Central Limit Theorem)<br>Let $X_1,X_2,\dots,X_n$ be independent and identically distributed, with $E\left(X_i\right)=\mu$ and $D\left(X_i\right)=\sigma^2> 0$. Then $$\frac{\bar X-\mu}{\sigma/\sqrt n}\xrightarrow{L}N\left(0,1\right).$$

> **Basic Knowledge** (Slutsky's Lemma)<br>Let the sequence of random variables satisfy $X_n\xrightarrow{L}X$ and $Y_n\xrightarrow{P}c$ ($c$ is a constant). Then $X_n/Y_n\xrightarrow{L}X/c$ ($c\ne0$).

### Problem 1

(Problem 2.3-2) Let $X_1,X_2,\dots,X_n$ be a sample from a Poisson-distributed population $P\left(\lambda\right)$, $\lambda> 0$. Find $E\left(\bar X\right)$, $D\left(\bar X\right)$, and $E\left(S^2\right)$.

### Solution to Problem 1

The population $X\sim P\left(\lambda\right)$, so $E\left(X\right)=\lambda$ and $D\left(X\right)=\lambda$. By **Lemma 2.3.1** (Expectations of the Sample Mean and Sample Variance),

$$
E\left(\bar X\right)=E\left(X\right)=\lambda,\quad D\left(\bar X\right)=\frac{D\left(X\right)}{n}=\frac{\lambda}{n},\quad E\left(S^2\right)=D\left(X\right)=\lambda.
$$

$\blacksquare$

### Problem 2

(Problem 2.3-4) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, $\mu\in\mathbb R$, $\sigma^2> 0$. Find $E\left(\bar X\right)$, $D\left(\bar X\right)$, $E\left(S^2\right)$, and $D\left(S^2\right)$.

### Solution to Problem 2

By **Lemma 2.3.1** (Expectations of the Sample Mean and Sample Variance),

$$
E\left(\bar X\right)=\mu,\quad D\left(\bar X\right)=\frac{\sigma^2}{n},\quad E\left(S^2\right)=\sigma^2.
$$

It remains to find $D\left(S^2\right)$. By conclusion (2) of **Theorem 2.3.3** (Distributions of the Sample Mean and Sample Variance of a Normal Population),

$$
\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right).
$$

By **Properties of the $\chi^2$ Distribution**, the variance of $\chi^2\left(k\right)$ is $2k$, so

$$
D\left(\frac{\left(n-1\right)S^2}{\sigma^2}\right)=2\left(n-1\right).
$$

Hence

$$
\frac{\left(n-1\right)^2}{\sigma^4}D\left(S^2\right)=2\left(n-1\right),
$$

which gives

$$
D\left(S^2\right)=\frac{2\sigma^4}{n-1}.
$$

$\blacksquare$

### Problem 3

(Problem 2.3-5) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, $\mu\in\mathbb R$, $\sigma^2> 0$, with $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ and $S_n^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2$. Further let $X_{n+1}\sim N\left(\mu,\sigma^2\right)$, with $X_{n+1}$ independent of $X_1,X_2,\dots,X_n$. Find the constant $c$ such that $c\frac{X_{n+1}-\bar X}{S_n}$ follows a $t$ distribution, and state the degrees of freedom.

### Solution to Problem 3

By conclusion (1) of **Theorem 2.3.3** (Distributions of the Sample Mean and Sample Variance of a Normal Population), $\bar X\sim N\left(\mu,\sigma^2/n\right)$. Also, $X_{n+1}\sim N\left(\mu,\sigma^2\right)$ and is independent of $\bar X$, so by the additivity of the normal distribution,

$$
X_{n+1}-\bar X\sim N\left(0,\sigma^2+\frac{\sigma^2}{n}\right)=N\left(0,\frac{n+1}{n}\sigma^2\right),
$$

which standardizes to

$$
\frac{X_{n+1}-\bar X}{\sigma\sqrt{\left(n+1\right)/n}}\sim N\left(0,1\right).
$$

On the other hand, $S_n^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2$ and the unbiased sample variance $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$ satisfy $nS_n^2=\left(n-1\right)S^2$. By conclusion (2) of **Theorem 2.3.3**,

$$
\frac{nS_n^2}{\sigma^2}=\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right).
$$

By conclusion (3) of **Theorem 2.3.3**, $\bar X$ and $S^2$ are mutually independent; also $X_{n+1}$ is independent of $X_1,\dots,X_n$, so $X_{n+1}-\bar X$ and $S_n^2$ are mutually independent. By **Definition 2.2.2** ($t$ Distribution),

$$
T=\frac{\frac{X_{n+1}-\bar X}{\sigma\sqrt{\left(n+1\right)/n}}}{\sqrt{\frac{nS_n^2/\sigma^2}{n-1}}}=\sqrt{\frac{n-1}{n+1}}\cdot\frac{X_{n+1}-\bar X}{S_n}\sim t\left(n-1\right).
$$

Therefore $c=\sqrt{\frac{n-1}{n+1}}$, with $n-1$ degrees of freedom. $\blacksquare$

### Problem 4

(Problem 2.3-7) Let $X_1,X_2,\dots,X_{n+m}$ be a sample from the normal population $N\left(0,\sigma^2\right)$, $\sigma^2> 0$. Find the constant $c$ such that $F=c\frac{\sum_{i=1}^n X_i^2}{\sum_{i=n+1}^{n+m}X_i^2}$ follows an $F$ distribution, and state the degrees of freedom.

### Solution to Problem 4

By **Definition 2.2.1** ($\chi^2$ Distribution), since $X_i/\sigma\sim N\left(0,1\right)$ and are mutually independent,

$$
\frac{1}{\sigma^2}\sum_{i=1}^n X_i^2\sim\chi^2\left(n\right),\quad\frac{1}{\sigma^2}\sum_{i=n+1}^{n+m}X_i^2\sim\chi^2\left(m\right).
$$

The samples on which the two expressions depend do not overlap, so the two are mutually independent. By **Definition 2.2.3** ($F$ Distribution),

$$
F=\frac{\left(\frac{1}{\sigma^2}\sum_{i=1}^n X_i^2\right)/n}{\left(\frac{1}{\sigma^2}\sum_{i=n+1}^{n+m}X_i^2\right)/m}=\frac{m}{n}\cdot\frac{\sum_{i=1}^n X_i^2}{\sum_{i=n+1}^{n+m}X_i^2}\sim F\left(n,m\right).
$$

Therefore $c=\frac{m}{n}$, with $\left(n,m\right)$ degrees of freedom. $\blacksquare$

### Problem 5

(Problem 2.3-8) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, $\mu\in\mathbb R$, $\sigma^2> 0$. Find the constants $a$ and $b$ such that $a\left(\bar X-\mu\right)^2+bS^2\sim\chi^2\left(n\right)$.

### Solution to Problem 5

By conclusion (1) of **Theorem 2.3.3** (Distributions of the Sample Mean and Sample Variance of a Normal Population),

$$
\frac{\bar X-\mu}{\sigma/\sqrt n}\sim N\left(0,1\right),
$$

and squaring gives

$$
\frac{n\left(\bar X-\mu\right)^2}{\sigma^2}\sim\chi^2\left(1\right).
$$

By conclusion (2) of **Theorem 2.3.3**,

$$
\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right).
$$

By conclusion (3) of **Theorem 2.3.3**, $\bar X$ and $S^2$ are mutually independent, so the two $\chi^2$ variables above are mutually independent. By **Properties of the $\chi^2$ Distribution** (Additivity),

$$
\frac{n\left(\bar X-\mu\right)^2}{\sigma^2}+\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(1\right)+\chi^2\left(n-1\right)=\chi^2\left(n\right).
$$

Therefore $a=\frac{n}{\sigma^2}$ and $b=\frac{n-1}{\sigma^2}$. $\blacksquare$

### Problem 6

(Problem 2.3-9) Let $X_1,X_2$ be a sample from the normal population $N\left(0,\sigma^2\right)$, $\sigma^2> 0$. Find the distribution of $Y=\left(\frac{X_1+X_2}{X_1-X_2}\right)^2$, and write down its degrees of freedom.

### Solution to Problem 6

By the additivity of the normal distribution, $X_1+X_2\sim N\left(0,2\sigma^2\right)$ and $X_1-X_2\sim N\left(0,2\sigma^2\right)$. The covariance of the two is

$$
\mathrm{Cov}\left(X_1+X_2,\ X_1-X_2\right)=\mathrm{Cov}\left(X_1,X_1\right)-\mathrm{Cov}\left(X_2,X_2\right)=\sigma^2-\sigma^2=0.
$$

Since $\left(X_1+X_2,\ X_1-X_2\right)$ follows a bivariate normal distribution, zero covariance means mutual independence. Standardizing gives

$$
U=\frac{X_1+X_2}{\sigma\sqrt2}\sim N\left(0,1\right),\quad V=\frac{X_1-X_2}{\sigma\sqrt2}\sim N\left(0,1\right),
$$

and $U$ and $V$ are mutually independent.

Hence

$$
Y=\left(\frac{X_1+X_2}{X_1-X_2}\right)^2=\left(\frac{U}{V}\right)^2=\frac{U^2}{V^2}.
$$

By **Definition 2.2.1** ($\chi^2$ Distribution), $U^2\sim\chi^2\left(1\right)$ and $V^2\sim\chi^2\left(1\right)$, and the two are mutually independent. By **Definition 2.2.3** ($F$ Distribution),

$$
Y=\frac{U^2/1}{V^2/1}\sim F\left(1,1\right).
$$

The degrees of freedom are $\left(1,1\right)$. $\blacksquare$

### Problem 7

(Problem 2.3-12) Let $X_1,X_2,X_3,X_4$ be a sample from the normal population $N\left(0,\sigma^2\right)$, $\sigma^2> 0$, and write $Y=\frac{X_1}{\sqrt{X_2^2+X_3^2+X_4^2}}$.

(1) Find $c$ such that $cY$ follows a $t$ distribution, and state the degrees of freedom;

(2) Find $E\left(cY\right)$ and $D\left(cY\right)$.

### Solution to Problem 7

(1) Since $X_1\sim N\left(0,\sigma^2\right)$, standardizing gives $X_1/\sigma\sim N\left(0,1\right)$. By **Definition 2.2.1** ($\chi^2$ Distribution),

$$
\frac{X_2^2+X_3^2+X_4^2}{\sigma^2}\sim\chi^2\left(3\right).
$$

$X_1$ does not overlap with $X_2,X_3,X_4$, so $X_1/\sigma$ and $\left(X_2^2+X_3^2+X_4^2\right)/\sigma^2$ are mutually independent. By **Definition 2.2.2** ($t$ Distribution),

$$
T=\frac{X_1/\sigma}{\sqrt{\frac{X_2^2+X_3^2+X_4^2}{\sigma^2}/3}}=\sqrt3\cdot\frac{X_1}{\sqrt{X_2^2+X_3^2+X_4^2}}=\sqrt3\,Y\sim t\left(3\right).
$$

Therefore $c=\sqrt3$, with $3$ degrees of freedom.

(2) Since $T\sim t\left(3\right)$ and $3> 1$, $E\left(T\right)=0$, so $E\left(cY\right)=0$. By the properties of the $t$ distribution, when $n> 2$, $D\left(T\right)=\frac{n}{n-2}$, so

$$
D\left(cY\right)=D\left(T\right)=\frac{3}{3-2}=3.
$$

$\blacksquare$

### Problem 8

(Problem 2.3-19) Let $X_1,X_2,\dots,X_n$ be a sample from a uniform-distribution population $U\left(0,\theta\right)$, $\theta> 0$. Find the limiting distribution of $\frac{\bar X-\theta/2}{\sqrt{\theta^2/12n}}$.

### Solution to Problem 8

The population $X\sim U\left(0,\theta\right)$, so $E\left(X\right)=\frac{\theta}{2}$ and $D\left(X\right)=\frac{\theta^2}{12}$. By **Basic Knowledge** (Central Limit Theorem),

$$
\frac{\bar X-\theta/2}{\sqrt{\theta^2/12n}}\xrightarrow{L}N\left(0,1\right).
$$

That is, the limiting distribution of this statistic is the standard normal distribution $N\left(0,1\right)$. $\blacksquare$

### Problem 9

(Problem 2.3-20) If $X_1,X_2,\dots,X_n$ is a sample from a Poisson-distributed population $P\left(\lambda\right)$, $\lambda> 0$, find the limiting distribution of $\frac{\bar X-\lambda}{\sqrt{\bar X/n}}$.

### Solution to Problem 9

The population $X\sim P\left(\lambda\right)$, so $E\left(X\right)=\lambda$ and $D\left(X\right)=\lambda$. By **Basic Knowledge** (Central Limit Theorem),

$$
\frac{\bar X-\lambda}{\sqrt{\lambda/n}}\xrightarrow{L}N\left(0,1\right).
$$

Also, by the law of large numbers, $\bar X\xrightarrow{P}\lambda$, so $\bar X/\lambda\xrightarrow{P}1$, and hence $\sqrt{\bar X/\lambda}\xrightarrow{P}1$. By **Basic Knowledge** (Slutsky's Lemma),

$$
\frac{\bar X-\lambda}{\sqrt{\bar X/n}}=\frac{\bar X-\lambda}{\sqrt{\lambda/n}}\cdot\sqrt{\frac{\lambda}{\bar X}}\xrightarrow{L}N\left(0,1\right)\cdot1=N\left(0,1\right).
$$

That is, the limiting distribution of this statistic is the standard normal distribution $N\left(0,1\right)$. $\blacksquare$

### Problem 10

(Problem 2.3-21) Let $X_1,X_2,\dots,X_n$ be a sample from the uniform-distribution population $U\left(0,1\right)$, and let $X_{\left(1\right)},\dots,X_{\left(n\right)}$ be the order statistics.

(1) To make $P\left\{X_{\left(n\right)}\ge0.99\right\}$ at least $0.95$, what is the minimum sample size required?

(2) Find the density function of the range $R_n=X_{\left(n\right)}-X_{\left(1\right)}$;

(3) As $n$ tends to infinity, find the limiting distribution of $Z=2n\left(1-R_n\right)$.

### Solution to Problem 10

(1) The population $X\sim U\left(0,1\right)$ has distribution function $F\left(x\right)=x$ ($0\le x\le1$). By **Theorem** (Distribution of Order Statistics), the distribution function of $X_{\left(n\right)}$ is $F_{\left(n\right)}\left(x\right)=\left[F\left(x\right)\right]^n=x^n$. Hence

$$
P\left\{X_{\left(n\right)}\ge0.99\right\}=1-P\left\{X_{\left(n\right)}< 0.99\right\}=1-0.99^n.
$$

Requiring $1-0.99^n\ge0.95$, i.e. $0.99^n\le0.05$, gives

$$
n\ge\frac{\ln0.05}{\ln0.99}\approx298.1.
$$

Hence the minimum sample size is $n=299$.

(2) By **Theorem** (Distribution of Order Statistics), the joint density function of the smallest and largest order statistics is

$$
f_{\left(1\right),\left(n\right)}\left(x,y\right)=n\left(n-1\right)\left(y-x\right)^{n-2},\quad0< x< y< 1.
$$

Let $r=y-x$, $s=x$, namely $x=s$ and $y=s+r$, with Jacobian determinant $J=1$. Integrating over $s$ gives the density function of $R_n=X_{\left(n\right)}-X_{\left(1\right)}$:

$$
f_{R_n}\left(r\right)=\int_0^{1-r}n\left(n-1\right)r^{n-2}\,\mathrm{d}s=n\left(n-1\right)r^{n-2}\left(1-r\right),\quad0< r< 1.
$$

(3) As $n\to+\infty$, $X_{\left(n\right)}\to1$ and $X_{\left(1\right)}\to0$, so $R_n\to1$. Consider the centered and standardized variables:

$$
n\left(1-X_{\left(n\right)}\right)\xrightarrow{L}Exp\left(1\right),\quad nX_{\left(1\right)}\xrightarrow{L}Exp\left(1\right),
$$

and the two are asymptotically independent. By **Properties of the $\chi^2$ Distribution** (Additivity) and the relationship between the **Gamma Distribution** and the $\chi^2$ distribution, the sum of two independent $Exp\left(1\right)$ variables follows $Ga\left(2,1\right)$, namely $\chi^2\left(2\right)/2$. Hence

$$
2n\left(1-R_n\right)=2\left[n\left(1-X_{\left(n\right)}\right)+nX_{\left(1\right)}\right]\xrightarrow{L}2\cdot Ga\left(2,1\right)=Ga\left(2,\frac12\right)=\chi^2\left(4\right).
$$

That is, the limiting distribution of $Z=2n\left(1-R_n\right)$ is $\chi^2\left(4\right)$. $\blacksquare$
