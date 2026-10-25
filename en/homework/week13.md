# Assignment 13

> **Definition 4.1.1** (Interval Estimation)<br>Let $\mathcal{F}=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ be a parametric family of distributions, where $\Theta$ is the parameter space, $g\left(\theta\right)$ is a known function defined on $\Theta$, and $X_1,X_2,\dots,X_n$ is a sample drawn from some population in the family $\mathcal{F}$. Let $g_1\left(X_1,X_2,\dots,X_n\right)$ and $g_2\left(X_1,X_2,\dots,X_n\right)$ be functions defined on the sample space, satisfying $g_1\left(X_1,X_2,\dots,X_n\right)\le g_2\left(X_1,X_2,\dots,X_n\right)$. Then the random interval $\left[g_1\left(X_1,X_2,\dots,X_n\right),g_2\left(X_1,X_2,\dots,X_n\right)\right]$ is called an interval estimate of $g\left(\theta\right)$.

> **Definition 4.1.4** (Confidence Interval)<br>Let $\left[\theta_1\left(X_1,X_2,\dots,X_n\right),\theta_2\left(X_1,X_2,\dots,X_n\right)\right]$ be an interval estimate of the parameter $\theta$. For a given $0< \alpha< 1$, if for every $\theta\in\Theta$ one has $P_\theta\left\{\theta_1\left(X_1,X_2,\dots,X_n\right)\le\theta\le\theta_2\left(X_1,X_2,\dots,X_n\right)\right\}\ge1-\alpha$, then $\left[\theta_1,\theta_2\right]$ is called a confidence interval for the parameter $\theta$ with confidence level $1-\alpha$.

> **Definition 4.1.5** (Confidence Bounds)<br>Let $\theta_L\left(X_1,X_2,\dots,X_n\right)$ and $\theta_U\left(X_1,X_2,\dots,X_n\right)$ be statistics defined on the sample space taking values in the parameter space. Given $0< \alpha< 1$, if for every $\theta\in\Theta$ one has $P_\theta\left\{\theta\ge\theta_L\right\}\ge1-\alpha$ and $P_\theta\left\{\theta\le\theta_U\right\}\ge1-\alpha$, then $\theta_L$ and $\theta_U$ are called the one-sided lower confidence bound and one-sided upper confidence bound of the parameter $\theta$ with confidence level $1-\alpha$.

> **Sampling Distribution** (Sampling Distribution for a Normal Sample)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$. Then $\bar X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right)$, and hence $\frac{\sqrt n\left(\bar X-\mu\right)}{\sigma}\sim N\left(0,1\right)$. When $\sigma^2$ is unknown, $\frac{\sqrt n\left(\bar X-\mu\right)}{S}\sim t\left(n-1\right)$, where $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$ is the sample variance.

### Problem 1

(Problem 4.1-4) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, where $\mu\in\mathbb R$ is an unknown parameter and $\sigma> 0$ is known. Write $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$. When the confidence interval for $\mu$ is $\left[\bar X-\frac{\sigma}{\sqrt n}u_{0.05},\bar X+\frac{\sigma}{\sqrt n}u_{0.05}\right]$, find the confidence level.

### Solution to Problem 1

By **Definition 4.1.1** (Interval Estimation), this random interval is $\left[\theta_1,\theta_2\right]=\left[\bar X-\frac{\sigma}{\sqrt n}u_{0.05},\bar X+\frac{\sigma}{\sqrt n}u_{0.05}\right]$. By **Definition 4.1.4** (Confidence Interval), its confidence level is

$$
P_\mu\left\{\bar X-\frac{\sigma}{\sqrt n}u_{0.05}\le\mu\le\bar X+\frac{\sigma}{\sqrt n}u_{0.05}\right\}.
$$

Rearranging the inequality, equivalently

$$
P_\mu\left\{-u_{0.05}\le\frac{\sqrt n\left(\bar X-\mu\right)}{\sigma}\le u_{0.05}\right\}.
$$

By **Sampling Distribution** (Sampling Distribution for a Normal Sample), when $\sigma$ is known, $\frac{\sqrt n\left(\bar X-\mu\right)}{\sigma}\sim N\left(0,1\right)$. Let $Z\sim N\left(0,1\right)$, where $u_{0.05}$ is the upper $0.05$ quantile of the standard normal distribution, i.e. $P\left(Z\ge u_{0.05}\right)=0.05$; by symmetry $P\left(Z\le-u_{0.05}\right)=0.05$. Therefore

$$
P\left\{-u_{0.05}\le Z\le u_{0.05}\right\}=1-P\left\{Z> u_{0.05}\right\}-P\left\{Z< -u_{0.05}\right\}=1-0.05-0.05=0.90.
$$

Hence the confidence level of this confidence interval is $0.90$. $\blacksquare$

### Problem 2

(Problem 4.1-5) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, where $\mu\in\mathbb R$ and $\sigma> 0$ are unknown parameters. Write $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ and $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$. When the upper confidence bound for $\mu$ is $\bar X+\frac{S}{\sqrt n}t_{0.05}\left(n-1\right)$, find the confidence level.

### Solution to Problem 2

By **Definition 4.1.5** (Confidence Bounds), the confidence level of the one-sided upper confidence bound $\theta_U=\bar X+\frac{S}{\sqrt n}t_{0.05}\left(n-1\right)$ is

$$
P_\mu\left\{\mu\le\bar X+\frac{S}{\sqrt n}t_{0.05}\left(n-1\right)\right\}.
$$

Rearranging the inequality, equivalently

$$
P_\mu\left\{\frac{\sqrt n\left(\bar X-\mu\right)}{S}\le t_{0.05}\left(n-1\right)\right\}.
$$

By **Sampling Distribution** (Sampling Distribution for a Normal Sample), when $\sigma$ is unknown, $\frac{\sqrt n\left(\bar X-\mu\right)}{S}\sim t\left(n-1\right)$. Let $T\sim t\left(n-1\right)$, where $t_{0.05}\left(n-1\right)$ is the upper $0.05$ quantile of the $t$ distribution, i.e. $P\left(T\ge t_{0.05}\left(n-1\right)\right)=0.05$. Therefore

$$
P\left\{T\le t_{0.05}\left(n-1\right)\right\}=1-P\left\{T> t_{0.05}\left(n-1\right)\right\}=1-0.05=0.95.
$$

Hence the confidence level of this one-sided upper confidence bound is $0.95$. $\blacksquare$
