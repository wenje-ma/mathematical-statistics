# Assignment 15

> **Pivotal Quantity Method** (Construction of a Confidence Interval)<br>Let $X_1,X_2,\dots,X_n$ be a sample from a population, with unknown parameter $\theta$. If one can construct a function $G\left(X_1,X_2,\dots,X_n,\theta\right)$ of the sample and $\theta$ whose distribution is completely known and independent of $\theta$, then $G$ is called a pivotal quantity. For a given confidence level $1-\alpha$, choose $c_1,c_2$ such that $P\left\{c_1\le G\le c_2\right\}=1-\alpha$, then equivalently rewrite the inequality $c_1\le G\le c_2$ as $\hat\theta_1\le\theta\le\hat\theta_2$, yielding the confidence interval $\left[\hat\theta_1,\hat\theta_2\right]$ for $\theta$ with confidence level $1-\alpha$.

> **Confidence Interval for the Parameter of an Exponential Distribution**<br>Let $X_1,X_2,\dots,X_n$ be a sample from the exponential-distribution population $E\left(\lambda\right)$, whose density function is $f\left(x\right)=\lambda e^{-\lambda x},\ x> 0$. By the additivity of the $\chi^2$ distribution, the pivotal quantity is $$T=2\lambda\sum_{i=1}^n X_i=2n\lambda\bar X\sim\chi^2\left(2n\right).$$ Hence the confidence interval for the mean $\theta=\frac{1}{\lambda}$ with confidence level $1-\alpha$ is $$\left[\frac{2n\bar X}{\chi^2_{\alpha/2}\left(2n\right)},\ \frac{2n\bar X}{\chi^2_{1-\alpha/2}\left(2n\right)}\right],$$ where $\chi^2_{\alpha/2}\left(2n\right)$ and $\chi^2_{1-\alpha/2}\left(2n\right)$ are respectively the upper $\alpha/2$ and upper $1-\alpha/2$ quantiles of the $\chi^2$ distribution with $2n$ degrees of freedom.

> **Large-sample Method** (Approximate Confidence Interval for the Parameter of a Two-point Distribution)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the two-point distribution $B\left(1,p\right)$, with $\bar X$ the sample mean. By the central limit theorem, when $n$ is sufficiently large, $\frac{\bar X-p}{\sqrt{p\left(1-p\right)/n}}\overset{\mathrm{d}}{\to}N\left(0,1\right)$. Estimating $p$ by $\bar X$, the confidence interval for the parameter $p$ with approximate confidence level $1-\alpha$ is $$\left[\bar X-u_{\alpha/2}\sqrt{\frac{\bar X\left(1-\bar X\right)}{n}},\ \bar X+u_{\alpha/2}\sqrt{\frac{\bar X\left(1-\bar X\right)}{n}}\right],$$ where $u_{\alpha/2}$ is the upper $\alpha/2$ quantile of the standard normal distribution.

### Problem 1

(Problem 4.3-1) Suppose the lifetime of an electronic product follows an exponential distribution $E\left(\lambda\right)$, whose density function is $f\left(x\right)=\lambda e^{-\lambda x},\ x> 0$, where $\lambda> 0$. A sample of size $9$ is drawn from a batch of products of this distribution, and the measured lifetimes (in kh) are $15,45,50,53,60,65,70,83,90$. Find the confidence interval and the upper and lower confidence bounds for the mean lifetime $\frac{1}{\lambda}$ with confidence level $90\%$.

### Solution to Problem 1

By **Confidence Interval for the Parameter of an Exponential Distribution**, the pivotal quantity is $T=2n\lambda\bar X\sim\chi^2\left(2n\right)$. The sample mean is

$$
\bar X=\frac{15+45+50+53+60+65+70+83+90}{9}=\frac{531}{9}=59,
$$

so $2n\bar X=18\times59=1062$, and the degrees of freedom are $2n=18$.

By **Pivotal Quantity Method** (Construction of a Confidence Interval), for confidence level $1-\alpha=0.90$, i.e. $\alpha=0.10$, we have

$$
P\left\{\chi^2_{0.05}\left(18\right)\le 2n\lambda\bar X\le\chi^2_{0.95}\left(18\right)\right\}=0.90.
$$

From the table, $\chi^2_{0.05}\left(18\right)=9.390$ and $\chi^2_{0.95}\left(18\right)=28.869$. Solving the inequality, the confidence interval for the mean lifetime $\theta=\frac{1}{\lambda}$ with confidence level $90\%$ is

$$
\left[\frac{1062}{28.869},\ \frac{1062}{9.390}\right]=\left[36.79,\ 113.09\right]\ \text{kh}.
$$

The one-sided upper confidence bound $\theta_U$ satisfies $P\left\{\theta\le\theta_U\right\}=0.90$, i.e. $P\left\{2n\lambda\bar X\ge\chi^2_{0.10}\left(18\right)\right\}=0.90$, so

$$
\theta_U=\frac{2n\bar X}{\chi^2_{0.10}\left(18\right)}=\frac{1062}{10.865}=97.75.
$$

The one-sided lower confidence bound $\theta_L$ satisfies $P\left\{\theta\ge\theta_L\right\}=0.90$, i.e. $P\left\{2n\lambda\bar X\le\chi^2_{0.90}\left(18\right)\right\}=0.90$, so

$$
\theta_L=\frac{2n\bar X}{\chi^2_{0.90}\left(18\right)}=\frac{1062}{25.989}=40.86.
$$

$\blacksquare$

### Problem 2

(Problem 4.3-3) Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and the density function of $X$ is $f\left(x,\theta\right)=\begin{cases}\frac{\theta}{x^2},&x> \theta,\\0,&\text{其他},\end{cases}$ where $\theta> 0$. Find the confidence interval for the parameter $\theta$ with confidence level $1-\alpha$.

### Solution to Problem 2

First find the distribution function of the population. For $x> \theta$,

$$
F\left(x,\theta\right)=\int_\theta^x\frac{\theta}{t^2}\,\mathrm dt=\theta\left[-\frac{1}{t}\right]_\theta^x=1-\frac{\theta}{x}.
$$

By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are mutually independent and identically distributed with the population. Consider the minimum order statistic $X_{\left(1\right)}=\min\left\{X_1,\dots,X_n\right\}$. For $t> \theta$,

$$
P\left\{X_{\left(1\right)}\ge t\right\}=\prod_{i=1}^n P\left\{X_i\ge t\right\}=\left[1-F\left(t,\theta\right)\right]^n=\left(\frac{\theta}{t}\right)^n.
$$

Construct the pivotal quantity $G=\frac{X_{\left(1\right)}}{\theta}$. Since $X_i> \theta$ always holds, $G\ge1$. For $t\ge1$,

$$
P\left\{G\ge t\right\}=P\left\{X_{\left(1\right)}\ge\theta t\right\}=\left(\frac{\theta}{\theta t}\right)^n=t^{-n},
$$

whose distribution is independent of $\theta$, so $G$ is a pivotal quantity.

By **Pivotal Quantity Method** (Construction of a Confidence Interval), noting that $G\ge1$, take

$$
P\left\{1\le G\le\alpha^{-1/n}\right\}=P\left\{G\le\alpha^{-1/n}\right\}=1-\left(\alpha^{-1/n}\right)^{-n}=1-\alpha.
$$

That is,

$$
P\left\{1\le\frac{X_{\left(1\right)}}{\theta}\le\alpha^{-1/n}\right\}=1-\alpha.
$$

Equivalently rewritten as

$$
P\left\{\alpha^{1/n}X_{\left(1\right)}\le\theta\le X_{\left(1\right)}\right\}=1-\alpha.
$$

Hence the confidence interval for the parameter $\theta$ with confidence level $1-\alpha$ is

$$
\left[\alpha^{1/n}X_{\left(1\right)},\ X_{\left(1\right)}\right].
$$

$\blacksquare$

### Problem 3

(Problem 4.3-4) Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and the density function of $X$ is $f\left(x\right)=\begin{cases}2\lambda x e^{-\lambda x^2},&x> 0,\\0,&\text{其他},\end{cases}$ where $\lambda> 0$. Find the confidence interval for the parameter $\lambda$ with confidence level $1-\alpha$.

### Solution to Problem 3

Let $Y=X^2$. When $y> 0$, by the density transformation formula for functions of a random variable,

$$
f_Y\left(y\right)=f\left(\sqrt y\right)\left|\frac{\mathrm d\sqrt y}{\mathrm dy}\right|=2\lambda\sqrt y\,e^{-\lambda y}\cdot\frac{1}{2\sqrt y}=\lambda e^{-\lambda y},
$$

i.e. $Y\sim E\left(\lambda\right)$. By **Definition 1.3.2** (Simple Random Sample), $Y_i=X_i^2$ are mutually independent and all follow $E\left(\lambda\right)$.

By **Confidence Interval for the Parameter of an Exponential Distribution**, the pivotal quantity is

$$
2\lambda\sum_{i=1}^n Y_i=2\lambda\sum_{i=1}^n X_i^2\sim\chi^2\left(2n\right).
$$

By **Pivotal Quantity Method** (Construction of a Confidence Interval),

$$
P\left\{\chi^2_{1-\alpha/2}\left(2n\right)\le 2\lambda\sum_{i=1}^n X_i^2\le\chi^2_{\alpha/2}\left(2n\right)\right\}=1-\alpha.
$$

Solving the inequality, the confidence interval for the parameter $\lambda$ with confidence level $1-\alpha$ is

$$
\left[\frac{\chi^2_{1-\alpha/2}\left(2n\right)}{2\sum_{i=1}^n X_i^2},\ \frac{\chi^2_{\alpha/2}\left(2n\right)}{2\sum_{i=1}^n X_i^2}\right].
$$

$\blacksquare$

### Problem 4

(Problem 4.3-10) A random sample of $100$ items is drawn from a batch of goods, and $16$ defective items are found. Find the confidence interval for the defective rate of this batch with approximate confidence level $95\%$.

### Solution to Problem 4

Let the defective rate be $p$. Then the sample mean, i.e. the frequency, is $\bar X=\frac{16}{100}=0.16$, and the sample size is $n=100$.

By **Large-sample Method** (Approximate Confidence Interval for the Parameter of a Two-point Distribution), the confidence interval for $p$ with approximate confidence level $1-\alpha$ is

$$
\left[\bar X-u_{\alpha/2}\sqrt{\frac{\bar X\left(1-\bar X\right)}{n}},\ \bar X+u_{\alpha/2}\sqrt{\frac{\bar X\left(1-\bar X\right)}{n}}\right].
$$

Taking $1-\alpha=0.95$, then $\alpha=0.05$, $u_{0.025}=1.96$, and

$$
\sqrt{\frac{\bar X\left(1-\bar X\right)}{n}}=\sqrt{\frac{0.16\times0.84}{100}}=\sqrt{0.001344}=0.0367.
$$

Hence the confidence interval for the defective rate $p$ with approximate confidence level $95\%$ is

$$
\left[0.16-1.96\times0.0367,\ 0.16+1.96\times0.0367\right]=\left[0.088,\ 0.232\right].
$$

$\blacksquare$
