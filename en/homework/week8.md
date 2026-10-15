# Assignment 8

> **Definition 3.2.1** (Method of Moments Estimator)<br>Let $\mathcal{F}=\left\{f\left(x;\theta\right):\theta\in\Theta\right\}$ be a parametric family of distributions, where $\theta=\left(\theta_1,\theta_2,\dots,\theta_m\right)$, $\Theta$ is the parameter space, and $X_1,X_2,\dots,X_n$ is a sample drawn from this family. Suppose the $k$-th raw moment of the population $\alpha_k=E\left(X^k\right)$ exists and, as a function of $\theta$, is denoted by $\alpha_k=\alpha_k\left(\theta_1,\theta_2,\dots,\theta_m\right)$. Let the $k$-th raw moment of the sample be $A_k=\frac{1}{n}\sum_{i=1}^n X_i^k$, take $k=1,2,\dots,m$, and equate the population moments to the sample moments to set up the system of equations $$\alpha_k\left(\theta_1,\theta_2,\dots,\theta_m\right)=A_k,\quad k=1,2,\dots,m,$$ whose solution $\hat\theta_i=\hat\theta_i\left(X_1,X_2,\dots,X_n\right)$ is called the method of moments estimator of $\theta_i$. One may also estimate the population $k$-th central moment by the sample $k$-th central moment to set up the corresponding equations. If one wishes to estimate a function of the parameters $g\left(\theta_1,\dots,\theta_m\right)$, then $g\left(\hat\theta_1,\dots,\hat\theta_m\right)$ is taken as its method of moments estimator.

> **Example 3.2.1 Conclusion** (Method of Moments Estimators of the Population Mean and Variance)<br>Let the mean $\mu$ and the variance $\sigma^2$ of the population $X$ both exist and be unknown, and let $X_1,X_2,\dots,X_n$ be a sample from the population $X$. Then the method of moments estimator of the population mean is $\hat\mu=\bar X=\frac{1}{n}\sum_{i=1}^n X_i$, and the method of moments estimator of the population variance is $$\hat\sigma^2=S_n^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2.$$

### Problem 1

(Problem 3.2-3) Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and the density function $f\left(x\right)$ of $X$ is as follows. Find the method of moments estimators of the unknown parameters.

(1) $f\left(x,\theta\right)=\begin{cases}\left(\theta+1\right)x^\theta,&0<x<1,\\0,&\text{其他},\end{cases}$ where $\theta>-1$ is an unknown parameter;

(2) $f\left(x,\theta\right)=\begin{cases}\theta e^{-\theta x},&x>0,\\0,&x\le 0,\end{cases}$ where $\theta>0$ is an unknown parameter;

(3) $f\left(x,\theta\right)=\frac{1}{2\theta}e^{-\frac{\left|x\right|}{\theta}},\ -\infty<x<+\infty$, where $\theta>0$ is an unknown parameter;

(4) $f\left(x,\theta\right)=\begin{cases}1,&\theta-0.5\le x\le\theta+0.5,\\0,&\text{其他},\end{cases}$ where $\theta\in\mathbb R$ is an unknown parameter;

(5) $f\left(x,\mu,\sigma^2\right)=\begin{cases}\frac{1}{\sqrt{2\pi}\sigma x}e^{-\frac{\left(\ln x-\mu\right)^2}{2\sigma^2}},&x>0,\\0,&x\le 0,\end{cases}$ where $\mu\in\mathbb R$ and $\sigma>0$ are unknown parameters;

(6) $f\left(x,\mu,\lambda\right)=\begin{cases}\lambda e^{-\lambda\left(x-\mu\right)},&x>\mu,\\0,&\text{其他},\end{cases}$ where $\mu\in\mathbb R$ and $\lambda>0$ are unknown parameters.

### Solution to Problem 1

By **Definition 3.2.1** (Method of Moments Estimator), equate the corresponding population moments to the sample moments and solve for the unknown parameters.

(1) The first raw moment of the population is

$$
E\left(X\right)=\int_0^1 x\cdot\left(\theta+1\right)x^\theta\,\mathrm dx=\frac{\theta+1}{\theta+2}.
$$

By **Definition 3.2.1**, setting $E\left(X\right)=\bar X$, i.e. $\frac{\theta+1}{\theta+2}=\bar X$, and solving gives

$$
\hat\theta=\frac{2\bar X-1}{1-\bar X}.
$$

(2) The first raw moment of the population is $E\left(X\right)=\frac{1}{\theta}$. Setting $E\left(X\right)=\bar X$, i.e. $\frac{1}{\theta}=\bar X$, gives

$$
\hat\theta=\frac{1}{\bar X}.
$$

(3) Since the density is symmetric about the origin, $E\left(X\right)=0$, which contains no unknown parameter, so we instead use the first absolute moment. Computing gives

$$
E\left|X\right|=\int_{-\infty}^{+\infty}\left|x\right|\frac{1}{2\theta}e^{-\frac{\left|x\right|}{\theta}}\,\mathrm dx=\frac{1}{\theta}\int_0^{+\infty}x e^{-\frac{x}{\theta}}\,\mathrm dx=\theta.
$$

By **Definition 3.2.1**, equating $E\left|X\right|$ to the sample first absolute moment $\frac{1}{n}\sum_{i=1}^n\left|X_i\right|$ gives

$$
\hat\theta=\frac{1}{n}\sum_{i=1}^n\left|X_i\right|.
$$

(4) $X\sim U\left[\theta-0.5,\theta+0.5\right]$, whose mean is $E\left(X\right)=\theta$. Setting $E\left(X\right)=\bar X$ gives

$$
\hat\theta=\bar X.
$$

(5) Let $Y=\ln X$; from the form of the density, $Y\sim N\left(\mu,\sigma^2\right)$. Applying **Example 3.2.1 Conclusion** (Method of Moments Estimators of the Population Mean and Variance) to $Y_1=\ln X_1,\dots,Y_n=\ln X_n$ gives

$$
\hat\mu=\frac{1}{n}\sum_{i=1}^n\ln X_i,\quad \hat\sigma^2=\frac{1}{n}\sum_{i=1}^n\left(\ln X_i-\frac{1}{n}\sum_{j=1}^n\ln X_j\right)^2.
$$

(6) This distribution is a shifted exponential distribution, whose mean and variance are respectively $E\left(X\right)=\mu+\frac{1}{\lambda}$ and $D\left(X\right)=\frac{1}{\lambda^2}$. By **Example 3.2.1 Conclusion**, the method of moments estimator of $D\left(X\right)$ is $S_n^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2$, so setting $\frac{1}{\lambda^2}=S_n^2$ gives

$$
\hat\lambda=\frac{1}{S_n}.
$$

Then from $E\left(X\right)=\mu+\frac{1}{\lambda}=\bar X$,

$$
\hat\mu=\bar X-\frac{1}{\hat\lambda}=\bar X-S_n,\quad S_n=\sqrt{\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2}.
$$

$\blacksquare$

### Problem 2

(Problem 3.2-5) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$. Find the method of moments estimator of $P\left\{X>1\right\}$.

### Solution to Problem 2

From $X\sim N\left(\mu,\sigma^2\right)$, we know

$$
P\left\{X>1\right\}=1-P\left\{X\le 1\right\}=1-\Phi\left(\frac{1-\mu}{\sigma}\right),
$$

where $\Phi\left(\cdot\right)$ is the standard normal distribution function. By **Example 3.2.1 Conclusion** (Method of Moments Estimators of the Population Mean and Variance), the method of moments estimators of $\mu$ and $\sigma$ are respectively

$$
\hat\mu=\bar X=\frac{1}{n}\sum_{i=1}^n X_i,\quad \hat\sigma=S_n=\sqrt{\frac{1}{n}\sum_{i=1}^n\left(X_i-\bar X\right)^2}.
$$

By the method of moments estimation method for functions of parameters in **Definition 3.2.1** (Method of Moments Estimator), replacing $\mu,\sigma$ by $\hat\mu,\hat\sigma$, the method of moments estimator of $P\left\{X>1\right\}$ is

$$
\widehat{P\left\{X>1\right\}}=1-\Phi\left(\frac{1-\bar X}{S_n}\right).
$$

$\blacksquare$

### Problem 3

(Problem 3.2-7) Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and the distribution function of $X$ is

$$
F\left(x;\theta\right)=\begin{cases}1-x^{-\theta},&x\ge 1,\\0,&x<1,\end{cases}
$$

where $\theta>1$ is an unknown parameter. Find the method of moments estimator of $\theta$.

### Solution to Problem 3

Differentiating the distribution function gives the population density function

$$
f\left(x;\theta\right)=\theta x^{-\left(\theta+1\right)},\quad x\ge 1.
$$

Computing the first raw moment of the population:

$$
E\left(X\right)=\int_1^{+\infty}x\cdot\theta x^{-\left(\theta+1\right)}\,\mathrm dx=\theta\int_1^{+\infty}x^{-\theta}\,\mathrm dx=\frac{\theta}{\theta-1},
$$

where convergence of the integral requires $\theta>1$. By **Definition 3.2.1** (Method of Moments Estimator), setting $E\left(X\right)=\bar X$, i.e. $\frac{\theta}{\theta-1}=\bar X$, and solving gives

$$
\bar X\left(\theta-1\right)=\theta\ \Longrightarrow\ \theta\left(\bar X-1\right)=\bar X\ \Longrightarrow\ \hat\theta=\frac{\bar X}{\bar X-1}.
$$

$\blacksquare$
