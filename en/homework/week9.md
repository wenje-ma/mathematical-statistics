# Assignment 9

> **Definition 3.3.2** (Maximum Likelihood Estimator)<br>Let the density function (or probability mass function) of the population be $f\left(x;\theta\right)$, and let $X_1,X_2,\dots,X_n$ be a sample from this population with observed values $x_1,x_2,\dots,x_n$. If the likelihood function $L\left(\theta\right)=L\left(\theta;x_1,x_2,\dots,x_n\right)$ attains its maximum at $\hat\theta=\hat\theta\left(x_1,x_2,\dots,x_n\right)$, i.e. $$L\left(\hat\theta\right)=\sup_{\theta\in\Theta}L\left(\theta\right),$$ then $\hat\theta\left(x_1,x_2,\dots,x_n\right)$ is called the maximum likelihood estimate of $\theta$, and $\hat\theta\left(X_1,X_2,\dots,X_n\right)$ is called the maximum likelihood estimator, abbreviated as MLE.

> **Likelihood Function and Log-likelihood Function**<br>For a continuous population, the likelihood function is $L\left(\theta\right)=\prod_{i=1}^n f\left(x_i;\theta\right)$; for a discrete population, the likelihood function is $L\left(\theta\right)=\prod_{i=1}^n P\left(X=x_i;\theta\right)$. The function $$\ln L\left(\theta\right)=\sum_{i=1}^n\ln f\left(x_i;\theta\right)$$ is called the log-likelihood function, and $L\left(\theta\right)$ and $\ln L\left(\theta\right)$ attain their extrema at the same parameter.

> **How to Find the MLE**<br>If the likelihood function is differentiable with respect to $\theta$, then $\hat\theta$ is found from the log-likelihood equation $\frac{\mathrm{d}\ln L}{\mathrm{d}\theta}=0$ (a system of equations when there are multiple parameters); when the stationary point is unique and is a maximum point, it is the MLE. If the likelihood function is not differentiable, then by **Definition 3.3.2** (Maximum Likelihood Estimator) directly compare the maximum point of the likelihood function over the parameter space.

> **Invariance of the MLE**<br>If $\hat\theta$ is the MLE of $\theta$ and $g\left(\theta\right)$ is a known function with a single-valued inverse, then $g\left(\hat\theta\right)$ is the MLE of $g\left(\theta\right)$.

### Problem 1

(Problem 3.3-3) Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and the density function $f\left(x\right)$ of $X$ is as follows. Find the maximum likelihood estimators of the unknown parameters:

(1) $f\left(x,\theta\right)=\begin{cases}\left(\theta+1\right)x^\theta,&0<x<1,\\0,&\text{其他},\end{cases}$ where $\theta>-1$ is an unknown parameter;

(2) $f\left(x,\theta\right)=\begin{cases}\theta e^{-\theta x},&x>0,\\0,&x\le0,\end{cases}$ where $\theta>0$ is an unknown parameter;

(3) $f\left(x,\theta\right)=\frac{1}{2\theta}e^{-\frac{\left|x\right|}{\theta}},\ -\infty<x<+\infty$, where $\theta>0$ is an unknown parameter;

(4) $f\left(x,\theta\right)=\begin{cases}1,&\theta-0.5\le x\le\theta+0.5,\\0,&\text{其他},\end{cases}$ where $\theta\in\mathbb R$ is an unknown parameter;

(5) $f\left(x,\mu,\sigma^2\right)=\begin{cases}\frac{1}{\sqrt{2\pi}\sigma x}e^{-\frac{\left(\ln x-\mu\right)^2}{2\sigma^2}},&x>0,\\0,&x\le0,\end{cases}$ where $\mu\in\mathbb R,\ \sigma^2>0$ are unknown parameters.

### Solution to Problem 1

By **Likelihood Function and Log-likelihood Function**, write out the likelihood function for each density and find the MLE according to **How to Find the MLE**.

(1) The likelihood function is

$$
L\left(\theta\right)=\prod_{i=1}^n\left(\theta+1\right)x_i^\theta=\left(\theta+1\right)^n\left(\prod_{i=1}^n x_i\right)^\theta,\quad 0<x_i<1.
$$

The log-likelihood function is $\ln L\left(\theta\right)=n\ln\left(\theta+1\right)+\theta\sum_{i=1}^n\ln x_i$. By **How to Find the MLE**, setting

$$
\frac{\mathrm{d}\ln L}{\mathrm{d}\theta}=\frac{n}{\theta+1}+\sum_{i=1}^n\ln x_i=0,
$$

and solving gives $\hat\theta=-1-\frac{n}{\sum_{i=1}^n\ln x_i}$. Since $0<x_i<1$, $\sum_{i=1}^n\ln x_i<0$, so $\hat\theta>-1$; also $\frac{\mathrm{d}^2\ln L}{\mathrm{d}\theta^2}=-\frac{n}{\left(\theta+1\right)^2}<0$, so this stationary point is a maximum point. Hence

$$
\hat\theta=-1-\frac{n}{\sum_{i=1}^n\ln X_i}.
$$

(2) The likelihood function is

$$
L\left(\theta\right)=\prod_{i=1}^n\theta e^{-\theta x_i}=\theta^n e^{-\theta\sum_{i=1}^n x_i},\quad x_i>0.
$$

The log-likelihood function is $\ln L\left(\theta\right)=n\ln\theta-\theta\sum_{i=1}^n x_i$. Setting $\frac{\mathrm{d}\ln L}{\mathrm{d}\theta}=\frac{n}{\theta}-\sum_{i=1}^n x_i=0$ and solving gives

$$
\hat\theta=\frac{1}{\bar X},\quad \bar X=\frac{1}{n}\sum_{i=1}^n X_i.
$$

(3) The likelihood function is

$$
L\left(\theta\right)=\prod_{i=1}^n\frac{1}{2\theta}e^{-\frac{\left|x_i\right|}{\theta}}=\left(2\theta\right)^{-n}e^{-\frac{1}{\theta}\sum_{i=1}^n\left|x_i\right|}.
$$

The log-likelihood function is $\ln L\left(\theta\right)=-n\ln\left(2\theta\right)-\frac{1}{\theta}\sum_{i=1}^n\left|x_i\right|$. Setting $\frac{\mathrm{d}\ln L}{\mathrm{d}\theta}=-\frac{n}{\theta}+\frac{1}{\theta^2}\sum_{i=1}^n\left|x_i\right|=0$ and solving gives

$$
\hat\theta=\frac{1}{n}\sum_{i=1}^n\left|X_i\right|.
$$

(4) $L\left(\theta\right)=1$ if and only if all samples fall in $\left[\theta-0.5,\theta+0.5\right]$, i.e. $\theta-0.5\le x_{\left(1\right)}$ and $x_{\left(n\right)}\le\theta+0.5$, and $L\left(\theta\right)=0$ otherwise. By **Definition 3.3.2** (Maximum Likelihood Estimator), any $\theta$ for which the likelihood function attains its maximum $1$ is an MLE, so the MLE is not unique and is the interval

$$
\hat\theta\in\left[X_{\left(n\right)}-0.5,\ X_{\left(1\right)}+0.5\right],
$$

where $X_{\left(1\right)}=\min\left\{X_1,\dots,X_n\right\}$ and $X_{\left(n\right)}=\max\left\{X_1,\dots,X_n\right\}$.

(5) Letting $y_i=\ln x_i$, the likelihood function is

$$
L\left(\mu,\sigma^2\right)=\prod_{i=1}^n\frac{1}{\sqrt{2\pi}\sigma x_i}e^{-\frac{\left(y_i-\mu\right)^2}{2\sigma^2}}=\frac{1}{\left(2\pi\sigma^2\right)^{n/2}\prod_{i=1}^n x_i}e^{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(y_i-\mu\right)^2}.
$$

Here $\prod_{i=1}^n x_i$ does not depend on the parameters. The log-likelihood function is

$$
\ln L\left(\mu,\sigma^2\right)=-\frac{n}{2}\ln\left(2\pi\sigma^2\right)-\sum_{i=1}^n\ln x_i-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(y_i-\mu\right)^2.
$$

By **How to Find the MLE**, setting $\frac{\partial\ln L}{\partial\mu}=0$ gives $\hat\mu=\bar y=\frac{1}{n}\sum_{i=1}^n\ln x_i$; setting $\frac{\partial\ln L}{\partial\left(\sigma^2\right)}=0$ gives

$$
\hat\sigma^2=\frac{1}{n}\sum_{i=1}^n\left(\ln X_i-\frac{1}{n}\sum_{j=1}^n\ln X_j\right)^2.
$$

$\blacksquare$

### Problem 2

(Problem 3.3-4) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, where $\mu\in\mathbb R,\ \sigma>0$.

(1) If $\mu$ is unknown and $\sigma$ is known, find the maximum likelihood estimator of $\mu$;

(2) if $\mu$ is known and $\sigma$ is unknown, find the maximum likelihood estimator of $\sigma^2$.

### Solution to Problem 2

The density function of the normal population is $f\left(x;\mu,\sigma^2\right)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{\left(x-\mu\right)^2}{2\sigma^2}}$. By **Likelihood Function and Log-likelihood Function**, the likelihood function is

$$
L\left(\mu,\sigma^2\right)=\left(2\pi\sigma^2\right)^{-\frac{n}{2}}e^{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2}.
$$

(1) When $\sigma$ is known, the part depending on $\mu$ is the $-\sum_{i=1}^n\left(x_i-\mu\right)^2$ in the exponent. By **How to Find the MLE**, setting

$$
\frac{\mathrm{d}}{\mathrm{d}\mu}\sum_{i=1}^n\left(x_i-\mu\right)^2=-2\sum_{i=1}^n\left(x_i-\mu\right)=0,
$$

and solving gives $\hat\mu=\bar X=\frac{1}{n}\sum_{i=1}^n X_i$, at which the residual sum of squares is minimized, so it is the MLE.

(2) When $\mu$ is known, the log-likelihood function is

$$
\ln L\left(\sigma^2\right)=-\frac{n}{2}\ln\left(2\pi\sigma^2\right)-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(x_i-\mu\right)^2.
$$

Setting $\frac{\mathrm{d}\ln L}{\mathrm{d}\left(\sigma^2\right)}=-\frac{n}{2\sigma^2}+\frac{1}{2\sigma^4}\sum_{i=1}^n\left(x_i-\mu\right)^2=0$ and solving gives

$$
\hat\sigma^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\mu\right)^2.
$$

$\blacksquare$

### Problem 3

(Problem 3.3-6) Let $X_1,X_2,\dots,X_n$ be a sample from a two-parameter exponential-distribution population, whose density function is

$$
f\left(x,\mu,\lambda\right)=\begin{cases}\lambda\exp\left\{-\lambda\left(x-\mu\right)\right\},&x>\mu,\\0,&\text{其他},\end{cases}
$$

where $-\infty<\mu<+\infty,\ \lambda>0$ are unknown parameters. Find respectively the maximum likelihood estimators of $\mu,\lambda$ and of $\alpha=P\left\{X_1\ge t\right\}$ ($t>\mu$).

### Solution to Problem 3

By **Likelihood Function and Log-likelihood Function**, when $\mu\le x_{\left(1\right)}$ the likelihood function is

$$
L\left(\mu,\lambda\right)=\prod_{i=1}^n\lambda e^{-\lambda\left(x_i-\mu\right)}=\lambda^n e^{-\lambda\sum_{i=1}^n x_i+n\lambda\mu},
$$

and when $\mu>x_{\left(1\right)}$, $L=0$. By **How to Find the MLE**, for fixed $\lambda>0$, $L\left(\mu,\lambda\right)=e^{n\lambda\mu}\cdot\lambda^n e^{-\lambda\sum x_i}$ is increasing in $\mu$, so the maximum is attained at the largest allowable $\mu$, namely

$$
\hat\mu=X_{\left(1\right)}=\min\left\{X_1,\dots,X_n\right\}.
$$

Substituting $\hat\mu=x_{\left(1\right)}$ gives the profile log-likelihood function

$$
\ln L\left(x_{\left(1\right)},\lambda\right)=n\ln\lambda-\lambda\sum_{i=1}^n\left(x_i-x_{\left(1\right)}\right).
$$

Setting $\frac{\mathrm{d}\ln L}{\mathrm{d}\lambda}=\frac{n}{\lambda}-\sum_{i=1}^n\left(x_i-x_{\left(1\right)}\right)=0$ and solving gives

$$
\hat\lambda=\frac{n}{\sum_{i=1}^n\left(X_i-X_{\left(1\right)}\right)}=\frac{1}{\bar X-X_{\left(1\right)}}.
$$

For the survival probability, since $X-\mu\sim E\left(\lambda\right)$,

$$
\alpha=P\left\{X_1\ge t\right\}=e^{-\lambda\left(t-\mu\right)}.
$$

By **Invariance of the MLE**,

$$
\hat\alpha=e^{-\hat\lambda\left(t-\hat\mu\right)}=\exp\left\{-\frac{t-X_{\left(1\right)}}{\bar X-X_{\left(1\right)}}\right\}.
$$

$\blacksquare$
