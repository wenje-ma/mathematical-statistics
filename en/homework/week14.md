# Assignment 14

> **Definition 4.2.1** (Pivotal Quantity)<br>Let $G\left(X_1,X_2,\dots,X_n,\theta\right)$ be a measurable function of the sample $\left(X_1,X_2,\dots,X_n\right)$ and the parameter $\theta$. When and only when the distribution of $G\left(X_1,X_2,\dots,X_n,\theta\right)$ does not depend on the parameter $\theta$, $G\left(X_1,X_2,\dots,X_n,\theta\right)$ is called a pivotal quantity.

> **Theorem** (Confidence Interval for the Mean of a Single Normal Population)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, with $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ and $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$. When $\sigma^2$ is known, the confidence interval for $\mu$ with confidence level $1-\alpha$ is $\left[\bar X-\frac{\sigma}{\sqrt n}u_{\alpha/2},\bar X+\frac{\sigma}{\sqrt n}u_{\alpha/2}\right]$; when $\sigma^2$ is unknown, the confidence interval for $\mu$ with confidence level $1-\alpha$ is $\left[\bar X-\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right),\bar X+\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right)\right]$.

> **Theorem** (Confidence Interval for the Variance of a Single Normal Population)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$. When $\mu$ is unknown, the confidence interval for $\sigma^2$ with confidence level $1-\alpha$ is $$\left[\frac{\left(n-1\right)S^2}{\chi^2_{\alpha/2}\left(n-1\right)},\frac{\left(n-1\right)S^2}{\chi^2_{1-\alpha/2}\left(n-1\right)}\right],$$ where $\chi^2_\alpha\left(n-1\right)$ denotes the upper $\alpha$ quantile of the $\chi^2$ distribution with $n-1$ degrees of freedom. Correspondingly, the confidence interval for $\sigma$ with confidence level $1-\alpha$ is the square root of the endpoints of the above interval.

> **Theorem** (Confidence Interval for the Difference of Means of Two Normal Populations)<br>Let $X_1,X_2,\dots,X_m$ be a sample from $N\left(\mu_1,\sigma_1^2\right)$ and $Y_1,Y_2,\dots,Y_n$ a sample from $N\left(\mu_2,\sigma_2^2\right)$, with the two samples independent, $\bar X,\bar Y$ the sample means and $S_1^2,S_2^2$ the sample variances. When $\sigma_1^2,\sigma_2^2$ are both known, the confidence interval for $\mu_2-\mu_1$ is $\left[\bar Y-\bar X-u_{\alpha/2}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}},\bar Y-\bar X+u_{\alpha/2}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}\right]$; when $\sigma_1^2=\sigma_2^2=\sigma^2$ is unknown, the confidence interval for $\mu_2-\mu_1$ is $\left[\bar Y-\bar X-S_w t_{\alpha/2}\left(m+n-2\right)\sqrt{\frac{1}{m}+\frac{1}{n}},\bar Y-\bar X+S_w t_{\alpha/2}\left(m+n-2\right)\sqrt{\frac{1}{m}+\frac{1}{n}}\right]$, where $S_w^2=\frac{\left(m-1\right)S_1^2+\left(n-1\right)S_2^2}{m+n-2}$; when $\sigma_1^2\ne\sigma_2^2$ is unknown, the Welch approximation may be used: $\left[\bar Y-\bar X-t_{\alpha/2}\left(r\right)\sqrt{\frac{S_1^2}{m}+\frac{S_2^2}{n}},\bar Y-\bar X+t_{\alpha/2}\left(r\right)\sqrt{\frac{S_1^2}{m}+\frac{S_2^2}{n}}\right]$, where $r=\frac{\left(S_1^2/m+S_2^2/n\right)^2}{\frac{\left(S_1^2/m\right)^2}{m-1}+\frac{\left(S_2^2/n\right)^2}{n-1}}$.

> **Theorem** (Confidence Interval for the Variance Ratio of Two Normal Populations)<br>Let the means of both populations be unknown. Then the confidence interval for $\frac{\sigma_1^2}{\sigma_2^2}$ with confidence level $1-\alpha$ is $$\left[\frac{S_1^2/S_2^2}{F_{\alpha/2}\left(m-1,n-1\right)},\frac{S_1^2/S_2^2}{F_{1-\alpha/2}\left(m-1,n-1\right)}\right],$$ where $F_{\alpha/2}\left(m-1,n-1\right)$ denotes the upper $\alpha/2$ quantile of the $F$ distribution.

### Problem 1

(Problem 4.2-3) Let $X_1,X_2,\dots,X_{21}$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$. Computation gives the sample mean $\bar{x}=32.295$ and the sample standard deviation $s=0.343$.

(1) If $\sigma$ is unknown, find the confidence interval for $\mu$ with confidence level $95\%$;

(2) If $\sigma$ is unknown, find the confidence interval for $\mu$ with confidence level $99\%$.

### Solution to Problem 1

By **Theorem** (Confidence Interval for the Mean of a Single Normal Population), when $\sigma^2$ is unknown, the confidence interval for $\mu$ with confidence level $1-\alpha$ is $\left[\bar X-\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right),\bar X+\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right)\right]$.

In this problem, $n=21$, $\bar{x}=32.295$, $s=0.343$, and the degrees of freedom are $n-1=20$.

(1) The confidence level is $95\%$, i.e. $\alpha=0.05$. From the $t$-distribution table, $t_{0.025}\left(20\right)=2.086$. Computation gives

$$
\frac{s}{\sqrt n}t_{0.025}\left(20\right)=\frac{0.343}{\sqrt{21}}\times2.086=0.156.
$$

Hence the $95\%$ confidence interval for $\mu$ is

$$
\left[32.295-0.156,\ 32.295+0.156\right]=\left[32.139,\ 32.451\right].
$$

(2) The confidence level is $99\%$, i.e. $\alpha=0.01$. From the $t$-distribution table, $t_{0.005}\left(20\right)=2.845$. Computation gives

$$
\frac{s}{\sqrt n}t_{0.005}\left(20\right)=\frac{0.343}{\sqrt{21}}\times2.845=0.213.
$$

Hence the $99\%$ confidence interval for $\mu$ is

$$
\left[32.295-0.213,\ 32.295+0.213\right]=\left[32.082,\ 32.508\right].
$$

$\blacksquare$

### Problem 2

(Problem 4.2-5) Let the population $X\sim N\left(\mu,\sigma_0^2\right)$, where $\sigma_0$ is known. So that the length of the confidence interval for $\mu$ with confidence level $1-\alpha$ does not exceed a given value $k$, find the minimum sample size $n$ that should be taken.

### Solution to Problem 2

By **Definition 4.2.1** (Pivotal Quantity), when $\sigma^2$ is known, the pivotal quantity is $U=\frac{\sqrt n\left(\bar X-\mu\right)}{\sigma_0}\sim N\left(0,1\right)$. By **Theorem** (Confidence Interval for the Mean of a Single Normal Population), the confidence interval for $\mu$ with confidence level $1-\alpha$ is

$$
\left[\bar X-\frac{\sigma_0}{\sqrt n}u_{\alpha/2},\ \bar X+\frac{\sigma_0}{\sqrt n}u_{\alpha/2}\right].
$$

The length of this interval is

$$
l=\frac{2\sigma_0}{\sqrt n}u_{\alpha/2}.
$$

Requiring $l\le k$, i.e.

$$
\frac{2\sigma_0}{\sqrt n}u_{\alpha/2}\le k.
$$

Solving this inequality gives

$$
\sqrt n\ge\frac{2\sigma_0}{k}u_{\alpha/2},\quad n\ge\left(\frac{2\sigma_0}{k}u_{\alpha/2}\right)^2.
$$

Since the sample size $n$ must be a positive integer,

$$
n=\begin{cases}
\left(\frac{2\sigma_0}{k}u_{\alpha/2}\right)^2,&\text{若 }\left(\frac{2\sigma_0}{k}u_{\alpha/2}\right)^2\text{ 为整数},\\[6pt\right]
\left\lfloor\left(\frac{2\sigma_0}{k}u_{\alpha/2}\right)^2\right\rfloor+1,&\text{若 }\left(\frac{2\sigma_0}{k}u_{\alpha/2}\right)^2\text{ 不是整数}.
\end{cases}
$$

$\blacksquare$

### Problem 3

(Problem 4.2-9) Let $X_1,X_2,\dots,X_{10}$ be a sample from the normal population $N\left(\mu_1,\sigma_1^2\right)$ and $Y_1,Y_2,\dots,Y_{13}$ a sample from the normal population $N\left(\mu_2,\sigma_2^2\right)$, with the two samples independent. Computation gives the ratio of sample variances $\frac{s_1^2}{s_2^2}=0.083$. Find the confidence interval for $\frac{\sigma_1^2}{\sigma_2^2}$ with confidence level $95\%$.

### Solution to Problem 3

By **Theorem** (Confidence Interval for the Variance Ratio of Two Normal Populations), when the means of both populations are unknown, the confidence interval for $\frac{\sigma_1^2}{\sigma_2^2}$ with confidence level $1-\alpha$ is

$$
\left[\frac{S_1^2/S_2^2}{F_{\alpha/2}\left(m-1,n-1\right)},\ \frac{S_1^2/S_2^2}{F_{1-\alpha/2}\left(m-1,n-1\right)}\right].
$$

In this problem, $m=10$, $n=13$, $\frac{s_1^2}{s_2^2}=0.083$, $\alpha=0.05$. From the $F$-distribution table,

$$
F_{0.025}\left(9,12\right)=3.436,\quad F_{0.975}\left(9,12\right)=\frac{1}{F_{0.025}\left(12,9\right)}=0.291.
$$

Substituting into the formula, the lower confidence bound is

$$
\frac{0.083}{3.436}=0.024,
$$

and the upper confidence bound is

$$
\frac{0.083}{0.291}=0.285.
$$

Hence the $95\%$ confidence interval for $\frac{\sigma_1^2}{\sigma_2^2}$ is $\left[0.024,\ 0.283\right]$. $\blacksquare$

### Problem 4

(Problem 4.2-11) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, and let $a,b$ be constants with $0<a<b$. Find the mathematical expectation and variance of the length $L$ of the random interval $\left[\frac{\left(n-1\right)S^2}{b\sigma^2},\frac{\left(n-1\right)S^2}{a\sigma^2}\right]$.

### Solution to Problem 4

This random interval is $\left[\frac{\left(n-1\right)S^2}{b\sigma^2},\frac{\left(n-1\right)S^2}{a\sigma^2}\right]$, whose length is

$$
L=\frac{\left(n-1\right)S^2}{a\sigma^2}-\frac{\left(n-1\right)S^2}{b\sigma^2}=\frac{n-1}{\sigma^2}\left(\frac{1}{a}-\frac{1}{b}\right)S^2.
$$

From the derivation of **Theorem** (Confidence Interval for the Variance of a Single Normal Population), $\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$. Let $Y=\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$, then

$$
L=\left(\frac{1}{a}-\frac{1}{b}\right)Y.
$$

By the properties of the $\chi^2$ distribution, $E\left(Y\right)=n-1$ and $D\left(Y\right)=2\left(n-1\right)$. Therefore

$$
E\left(L\right)=\left(\frac{1}{a}-\frac{1}{b}\right)E\left(Y\right)=\left(n-1\right)\left(\frac{1}{a}-\frac{1}{b}\right),
$$

$$
D\left(L\right)=\left(\frac{1}{a}-\frac{1}{b}\right)^2D\left(Y\right)=2\left(n-1\right)\left(\frac{1}{a}-\frac{1}{b}\right)^2.
$$

$\blacksquare$

### Problem 5

(Problem 4.2-14) Nine shells are randomly selected, and the sample standard deviation of their muzzle velocities is measured to be $s=11\ \text{m/s}$. If the muzzle velocity of a shell follows a normal distribution $N\left(\mu,\sigma^2\right)$, where $\mu,\sigma$ are unknown, find the one-sided upper confidence bound for the standard deviation $\sigma$ with confidence level $95\%$.

### Solution to Problem 5

By **Theorem** (Confidence Interval for the Variance of a Single Normal Population), when $\mu$ is unknown, $\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$.

The one-sided upper confidence bound $\sigma_U$ satisfies $P\left(\sigma\le\sigma_U\right)=1-\alpha$. From

$$
P\left(\frac{\left(n-1\right)S^2}{\sigma^2}\ge\chi^2_{1-\alpha}\left(n-1\right)\right)=1-\alpha,
$$

solving for $\sigma$, the one-sided upper confidence bound is

$$
\sigma_U=\sqrt{\frac{\left(n-1\right)S^2}{\chi^2_{1-\alpha}\left(n-1\right)}}.
$$

In this problem, $n=9$, $s=11$, $\alpha=0.05$. From the $\chi^2$-distribution table, $\chi^2_{0.95}\left(8\right)=2.733$ (i.e. the upper $95\%$ quantile, equivalently the lower $5\%$ quantile). Substituting,

$$
\sigma_U=\sqrt{\frac{8\times11^2}{2.733}}=\sqrt{\frac{968}{2.733}}=\sqrt{354.2}=18.82.
$$

Hence the one-sided upper confidence bound for the standard deviation $\sigma$ with confidence level $95\%$ is $18.82\ \text{m/s}$. $\blacksquare$

### Problem 6

(Problem 4.2-20) Two machine tools process the same type of part. Samples of 6 and 9 parts are drawn respectively, their lengths measured, and the sample variances computed to be $s_1^2=0.245$ and $s_2^2=0.357$. Assume the lengths of parts processed by the two machine tools follow normal distributions $N\left(\mu_1,\sigma_1^2\right)$ and $N\left(\mu_2,\sigma_2^2\right)$ respectively. Find the confidence interval for the ratio of the two population standard deviations $\frac{\sigma_1}{\sigma_2}$ with confidence level $95\%$.

### Solution to Problem 6

By **Theorem** (Confidence Interval for the Variance Ratio of Two Normal Populations), the confidence interval for $\frac{\sigma_1^2}{\sigma_2^2}$ with confidence level $1-\alpha$ is

$$
\left[\frac{S_1^2/S_2^2}{F_{\alpha/2}\left(m-1,n-1\right)},\ \frac{S_1^2/S_2^2}{F_{1-\alpha/2}\left(m-1,n-1\right)}\right].
$$

In this problem, $m=6$, $n=9$, $s_1^2=0.245$, $s_2^2=0.357$, $\alpha=0.05$. Computation gives

$$
\frac{s_1^2}{s_2^2}=\frac{0.245}{0.357}=0.686.
$$

From the $F$-distribution table,

$$
F_{0.025}\left(5,8\right)=4.817,\quad F_{0.975}\left(5,8\right)=\frac{1}{F_{0.025}\left(8,5\right)}=0.148.
$$

Hence the $95\%$ confidence interval for $\frac{\sigma_1^2}{\sigma_2^2}$ is

$$
\left[\frac{0.686}{4.817},\ \frac{0.686}{0.148}\right]=\left[0.142,\ 4.637\right].
$$

Taking the square root of both endpoints, the $95\%$ confidence interval for $\frac{\sigma_1}{\sigma_2}$ is

$$
\left[\sqrt{0.142},\ \sqrt{4.637}\right]=\left[0.377,\ 2.153\right].
$$

$\blacksquare$

### Problem 7

(Problem 4.2-21) Samples of sizes $m=10$ and $n=15$ are drawn respectively from the population $X\sim N\left(\mu_1,\sigma_1^2\right)$ and the population $Y\sim N\left(\mu_2,\sigma_2^2\right)$. Computation gives sample means $\bar{x}=82$ and $\bar{y}=76$, and sample variances $s_x^2=56.5$ and $s_y^2=52.4$.

(1) If it is known that $\sigma_1^2=64$ and $\sigma_2^2=49$, find the confidence interval for $\mu_1-\mu_2$ with confidence level $95\%$;

(2) If $\sigma_1^2=\sigma_2^2$ is unknown, find the confidence interval for $\mu_1-\mu_2$ with confidence level $95\%$;

(3) If nothing is known about $\sigma_1^2,\sigma_2^2$, find the confidence interval for $\mu_1-\mu_2$ with confidence level $95\%$;

(4) Find the confidence interval for $\frac{\sigma_1^2}{\sigma_2^2}$ with confidence level $95\%$.

### Solution to Problem 7

By **Theorem** (Confidence Interval for the Difference of Means of Two Normal Populations) and **Theorem** (Confidence Interval for the Variance Ratio of Two Normal Populations), we consider four cases.

(1) $\sigma_1^2=64$ and $\sigma_2^2=49$ are both known. The confidence interval is

$$
\left[\bar x-\bar y-u_{0.025}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}},\ \bar x-\bar y+u_{0.025}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}\right].
$$

where $\bar x-\bar y=82-76=6$, $u_{0.025}=1.96$,

$$
\sqrt{\frac{64}{10}+\frac{49}{15}}=\sqrt{6.4+3.267}=\sqrt{9.667}=3.109.
$$

The margin of error is $1.96\times3.109=6.094$. Hence the confidence interval is

$$
\left[6-6.094,\ 6+6.094\right]=\left[-0.094,\ 12.094\right].
$$

(2) $\sigma_1^2=\sigma_2^2=\sigma^2$ is unknown. The pooled variance is

$$
s_w^2=\frac{\left(m-1\right)s_x^2+\left(n-1\right)s_y^2}{m+n-2}=\frac{9\times56.5+14\times52.4}{23}=\frac{508.5+733.6}{23}=\frac{1242.1}{23}=54.00.
$$

$s_w=\sqrt{54.00}=7.349$. From the $t$-distribution table, $t_{0.025}\left(23\right)=2.069$. The margin of error is

$$
s_w t_{0.025}\left(23\right)\sqrt{\frac{1}{m}+\frac{1}{n}}=7.349\times2.069\times\sqrt{\frac{1}{10}+\frac{1}{15}}=7.349\times2.069\times0.408=6.206.
$$

Hence the $95\%$ confidence interval for $\mu_1-\mu_2$ is

$$
\left[6-6.206,\ 6+6.206\right]=\left[-0.206,\ 12.206\right].
$$

(3) $\sigma_1^2,\sigma_2^2$ are both unknown and unequal. The Welch approximation is used, and the degrees of freedom are

$$
r=\frac{\left(s_x^2/m+s_y^2/n\right)^2}{\frac{\left(s_x^2/m\right)^2}{m-1}+\frac{\left(s_y^2/n\right)^2}{n-1}}=\frac{\left(5.65+3.493\right)^2}{\frac{5.65^2}{9}+\frac{3.493^2}{14}}=\frac{9.143^2}{3.547+0.872}=\frac{83.59}{4.419}=18.92\approx19.
$$

From the $t$-distribution table, $t_{0.025}\left(19\right)=2.093$. The margin of error is

$$
t_{0.025}\left(19\right)\sqrt{\frac{s_x^2}{m}+\frac{s_y^2}{n}}=2.093\times\sqrt{9.143}=2.093\times3.024=6.329.
$$

Hence the $95\%$ confidence interval for $\mu_1-\mu_2$ is

$$
\left[6-6.329,\ 6+6.329\right]=\left[-0.329,\ 12.329\right].
$$

(4) Find the confidence interval for $\frac{\sigma_1^2}{\sigma_2^2}$. From the $F$-distribution table,

$$
F_{0.025}\left(9,14\right)=3.209,\quad F_{0.975}\left(9,14\right)=\frac{1}{F_{0.025}\left(14,9\right)}=0.263.
$$

$\frac{s_x^2}{s_y^2}=\frac{56.5}{52.4}=1.078$. Hence the confidence interval is

$$
\left[\frac{1.078}{3.209},\ \frac{1.078}{0.263}\right]=\left[0.336,\ 4.100\right].
$$

$\blacksquare$
