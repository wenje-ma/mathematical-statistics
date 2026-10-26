# Mathematical Statistics

## Introduction and Basic Concepts

**Definition 1.2.1** (Population)

In mathematical statistics, the entire collection of the objects under study involved in the problem being investigated is called the population. Each element making up the population is called an individual. The number of individuals contained in the population is called the population size. In practice, a population can be described by a random variable $X$ and its distribution; the study of the population is then transformed into the study of the statistical regularity of the random variable $X$ representing the population. Henceforth we shall not distinguish between the population and the corresponding random variable, and both are collectively referred to as the population $X$.

**Definition 1.3.1** (Sample Space)

The set of all possible values of the sample $X_1,X_2,\dots,X_n$ is called the sample space.

**Definition 1.3.2** (Simple Random Sample)

Let there be a population $X$ with distribution $F$, and let $X_1,X_2,\dots,X_n$ be a sample of size $n$ drawn from the population $X$. If

(1) $X_1,X_2,\dots,X_n$ are mutually independent;

(2) $X_1,X_2,\dots,X_n$ have the same distribution $F$ as the population $X$,

then $X_1,X_2,\dots,X_n$ is called a simple random sample of size $n$ drawn from the population $X$, abbreviated as a sample.

**Sample Distribution** (Joint Distribution Function, Joint Probability Mass Function and Joint Density Function)

Let the distribution function of the population $X$ be $F\left(x\right)$, and let $X_1,X_2,\dots,X_n$ be a sample from the population $X$. Then the joint distribution function of the sample is

$$
F^{*}\left(x_1,x_2,\dots,x_n\right)=\prod_{i=1}^n F\left(x_i\right).
$$

If the population $X$ is a discrete random variable with probability mass function $P\left\{X=a_i\right\}=p_i$, then the joint probability mass function of the sample $X_1,X_2,\dots,X_n$ is

$$
P\left\{X_1=x_1,\dots,X_n=x_n\right\}=\prod_{i=1}^n p_{x_i}.
$$

If the population $X$ is a continuous random variable with density function $f\left(x\right)$, then the joint density function of the sample $X_1,X_2,\dots,X_n$ is

$$
f^{*}\left(x_1,x_2,\dots,x_n\right)=\prod_{i=1}^n f\left(x_i\right).
$$

**Definition 1.3.3** (Parameter Space)

In mathematical statistics, the unknown constants appearing in the population distribution or the sample distribution are called parameters. The set of all possible values of the parameter $\theta$ is called the parameter space, denoted by $\Theta$.

**Population Distribution Family and Sample Distribution Family**

Since different parameter values generally correspond to different population distributions, all possible parameter values in the parameter space correspond to a family of population distributions, called the population distribution family, denoted by $\left\{f\left(x;\theta\right):\theta\in\Theta\right\}$. Different parameter values also generally correspond to different sample distributions; all possible parameter values in the parameter space correspond to a family of sample distributions, called the sample distribution family, denoted by

$$
\left\{\prod_{i=1}^n f\left(x_i;\theta\right):\theta\in\Theta\right\}.
$$

**Definition 1.4.1** (Statistic)

Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and let $g\left(X_1,X_2,\dots,X_n\right)$ be a function of the sample $X_1,X_2,\dots,X_n$ that, besides depending on the sample, does not depend on any other unknown quantity; then $g\left(X_1,X_2,\dots,X_n\right)$ is called a statistic. If $x_1,x_2,\dots,x_n$ are the observed values of the sample $X_1,X_2,\dots,X_n$, then $g\left(x_1,x_2,\dots,x_n\right)$ is called an observed value of the statistic $g\left(X_1,X_2,\dots,X_n\right)$. A statistic depends only on the sample and does not depend on any unknown parameter.

**Definition 1.5.1** (Empirical Distribution Function)

Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and let $X_{\left(1\right)}\le X_{\left(2\right)}\le\dots\le X_{\left(n\right)}$ be its order statistics. For any real number $x$, define

$$
F_n\left(x\right)=\begin{cases}0,&x< X_{\left(1\right)},\\\frac{r}{n},&X_{\left(r\right)}\le x< X_{\left(r+1\right)},\ r=1,2,\dots,n-1,\\1,&x\ge X_{\left(n\right)}\end{cases}
$$

as the empirical distribution function of the sample $X_1,X_2,\dots,X_n$.

## Sampling Distributions: Order Statistics and Common Sampling Distributions

**Sampling Distribution** (Definition)

A statistic is a function of the sample $X_1,X_2,\dots,X_n$, and the sample $X_1,X_2,\dots,X_n$ consists of random variables. Therefore a statistic is also a random variable, and the distribution of a statistic is called a sampling distribution.

**Theorem** (Distribution of Order Statistics)

Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, where the distribution function of $X$ is $F\left(x\right)$, and let $\left(X_{\left(1\right)},X_{\left(2\right)},\dots,X_{\left(n\right)}\right)$ be its order statistics. Then for $1\le r\le n$, the distribution function of $X_{\left(r\right)}$ is

$$
F_{\left(r\right)}\left(x\right)=P\left\{X_{\left(r\right)}\le x\right\}=\sum_{k=r}^n\binom{n}{k}\left[F\left(x\right)\right]^k\left[1-F\left(x\right)\right]^{n-k}=r\binom{n}{r}\int_0^{F\left(x\right)}t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t.
$$

If the population $X$ is continuous with density function $f\left(x\right)$, then the density function of $X_{\left(r\right)}$ is

$$
f_{\left(r\right)}\left(x\right)=F_{\left(r\right)}'\left(x\right)=r\binom{n}{r}\left[F\left(x\right)\right]^{r-1}\left[1-F\left(x\right)\right]^{n-r}f\left(x\right).
$$

In particular, when $r=1$, the distribution function and density function of the minimum order statistic $X_{\left(1\right)}$ are respectively

$$
F_{\left(1\right)}\left(x\right)=1-\left[1-F\left(x\right)\right]^n,\quad f_{\left(1\right)}\left(x\right)=n\left[1-F\left(x\right)\right]^{n-1}f\left(x\right);
$$

when $r=n$, the distribution function and density function of the maximum order statistic $X_{\left(n\right)}$ are respectively

$$
F_{\left(n\right)}\left(x\right)=\left[F\left(x\right)\right]^n,\quad f_{\left(n\right)}\left(x\right)=n\left[F\left(x\right)\right]^{n-1}f\left(x\right).
$$

**Basic Knowledge** (Additivity of the Poisson Distribution)

Let $X_1,X_2,\dots,X_n$ be independent, with $X_i\sim P\left(\lambda_i\right)$. Then $\sum_{i=1}^n X_i\sim P\left(\sum_{i=1}^n\lambda_i\right)$.

**Basic Knowledge** (Additivity of the Normal Distribution)

Let $X_1,X_2,\dots,X_n$ be independent, with $X_i\sim N\left(\mu_i,\sigma_i^2\right)$. Then $\sum_{i=1}^n X_i\sim N\left(\sum_{i=1}^n\mu_i,\sum_{i=1}^n\sigma_i^2\right)$.

**Definition 2.2.1** ($\chi^2$ Distribution)

Let $X_1,X_2,\dots,X_n$ be independent and all follow $N\left(0,1\right)$. Then

$$
\chi^2=X_1^2+X_2^2+\dots+X_n^2
$$

is called a $\chi^2$ variable with $n$ degrees of freedom; its distribution is called the $\chi^2$ distribution with $n$ degrees of freedom, denoted by $\chi^2\sim\chi^2\left(n\right)$.

**Theorem 2.2.1** (Density Function of the $\chi^2$ Distribution)

Let $\chi^2\sim\chi^2\left(n\right)$. Then its density function is

$$
f\left(x\right)=\begin{cases}\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2},&x> 0,\\0,&x\le0.\end{cases}
$$

**Properties of the $\chi^2$ Distribution**

Let $\chi^2\sim\chi^2\left(n\right)$. Then $E\left(\chi^2\right)=n$, $D\left(\chi^2\right)=2n$. If $X_1\sim\chi^2\left(n_1\right)$, $X_2\sim\chi^2\left(n_2\right)$, and $X_1$ and $X_2$ are independent, then $X_1+X_2\sim\chi^2\left(n_1+n_2\right)$; this property is called the additivity of the $\chi^2$ distribution.

**Definition 2.2.2** ($t$ Distribution)

Let the random variables $X\sim N\left(0,1\right)$ and $Y\sim\chi^2\left(n\right)$, with $X$ and $Y$ independent. Then the random variable

$$
T=\frac{X}{\sqrt{Y/n}}
$$

is called a $t$ variable with $n$ degrees of freedom; its distribution is called the $t$ distribution with $n$ degrees of freedom, denoted by $T\sim t\left(n\right)$.

**Theorem 2.2.2** (Density Function of the $t$ Distribution)

Let $T\sim t\left(n\right)$. Then its density function is

$$
f\left(t\right)=\frac{\Gamma\left(\left(n+1\right)/2\right)}{\Gamma\left(n/2\right)\sqrt{n\pi}}\left(1+\frac{t^2}{n}\right)^{-\left(n+1\right)/2},\quad-\infty< t< +\infty.
$$

**Definition 2.2.3** ($F$ Distribution)

Let the random variables $X\sim\chi^2\left(m\right)$ and $Y\sim\chi^2\left(n\right)$, with $X$ and $Y$ independent. Then the random variable

$$
F=\frac{X/m}{Y/n}
$$

is called an $F$ variable with degrees of freedom $m$ and $n$; the distribution it follows is called the $F$ distribution, denoted by $F\sim F\left(m,n\right)$.

**Corollary 2.2.1** (Independence of $X/Y$ and $X+Y$)

Let the random variables $X\sim\chi^2\left(m\right)$ and $Y\sim\chi^2\left(n\right)$, with $X$ and $Y$ independent. Then $U=X/Y$ and $V=X+Y$ are independent.

**Gamma Distribution**

If the density function of the random variable $X$ is

$$
f\left(x\right)=\begin{cases}\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}x^{\alpha-1}e^{-\lambda x},&x> 0,\\0,&x\le0,\end{cases}
$$

where $\alpha> 0$ is the shape parameter and $\lambda> 0$ is the scale parameter, then $X$ is said to follow the Gamma distribution with parameters $\left(\alpha,\lambda\right)$, denoted by $X\sim Ga\left(\alpha,\lambda\right)$. When $\alpha=1$, $Ga\left(1,\lambda\right)$ is the exponential distribution; when $\alpha=n/2$ and $\lambda=1/2$, $Ga\left(n/2,1/2\right)$ is the $\chi^2\left(n\right)$ distribution.

**Lemma 2.3.1** (Expectations of the Sample Mean and Sample Variance)

Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, with $E\left(X\right)=\mu$ and $D\left(X\right)=\sigma^2$, and let $\overline X=\frac{1}{n}\sum_{i=1}^n X_i$ and $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\overline X\right)^2$ be the sample mean and sample variance, respectively. Then

$$
E\left(\overline X\right)=\mu,\quad D\left(\overline X\right)=\frac{\sigma^2}{n},\quad E\left(S^2\right)=\sigma^2.
$$

**Theorem 2.3.3** (Distribution of the Sample Mean and Sample Variance of a Normal Population)

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$, and let $\overline X$ and $S^2$ be the sample mean and sample variance, respectively. Then:

(1) $\overline X\sim N\left(\mu,\sigma^2/n\right)$, i.e. $\frac{\overline X-\mu}{\sigma/\sqrt n}\sim N\left(0,1\right)$;

(2) $\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$;

(3) $\overline X$ and $S^2$ are independent.

**Theorem 2.3.4**

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$. Then

$$
\frac{1}{\sigma^2}\sum_{i=1}^n\left(X_i-\mu\right)^2\sim\chi^2\left(n\right).
$$

**Definition 2.2.2** ($t$ Distribution)

Let the random variables $X\sim N\left(0,1\right)$ and $Y\sim\chi^2\left(n\right)$, with $X$ and $Y$ independent. Then $T=\frac{X}{\sqrt{Y/n}}$ is called a $t$ variable with $n$ degrees of freedom, denoted by $T\sim t\left(n\right)$.

**Definition 2.2.3** ($F$ Distribution)

Let the random variables $X\sim\chi^2\left(m\right)$ and $Y\sim\chi^2\left(n\right)$, with $X$ and $Y$ independent. Then $F=\frac{X/m}{Y/n}$ is called an $F$ variable with degrees of freedom $m$ and $n$, denoted by $F\sim F\left(m,n\right)$.

**Properties of the $\chi^2$ Distribution** (Additivity)

Let $X_1\sim\chi^2\left(n_1\right)$, $X_2\sim\chi^2\left(n_2\right)$, and let $X_1$ and $X_2$ be independent. Then $X_1+X_2\sim\chi^2\left(n_1+n_2\right)$.

**Basic Knowledge** (Central Limit Theorem)

Let $X_1,X_2,\dots,X_n$ be independent and identically distributed, with $E\left(X_i\right)=\mu$ and $D\left(X_i\right)=\sigma^2> 0$. Then

$$
\frac{\overline X-\mu}{\sigma/\sqrt n}\xrightarrow{L}N\left(0,1\right).
$$

**Basic Knowledge** (Slutsky's Lemma)

Let the sequence of random variables satisfy $X_n\xrightarrow{L}X$ and $Y_n\xrightarrow{P}c$ ($c$ a constant). Then $X_n/Y_n\xrightarrow{L}X/c$ ($c\ne0$).

## Exponential Families and Sufficient and Complete Statistics

**Definition 2.4.1** (Exponential Family)

Let $\mathcal{F}=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ be a family of distributions defined on the sample space $\mathcal{X}$, where $\Theta$ is the parameter space. If $f\left(x,\theta\right)$ can be expressed as

$$
f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k Q_i\left(\theta\right)T_i\left(x\right)\right\}h\left(x\right),
$$

then this family is called an exponential family of distributions, abbreviated as the exponential family. Here $C\left(\theta\right)> 0$ and $Q_i\left(\theta\right)$ are defined on the parameter space $\Theta$, $h\left(x\right)> 0$ and $T_i\left(x\right)$ are defined on the sample space $\mathcal{X}$, and the support set $\left\{x:f\left(x,\theta\right)> 0\right\}$ does not depend on $\theta$.

**Definition 2.4.2** (Natural Form of an Exponential Family)

If an exponential family has the following form

$$
f\left(x,\varphi\right)=C\left(\varphi\right)\exp\left\{\sum_{i=1}^k\varphi_i T_i\left(x\right)\right\}h\left(x\right),
$$

then it is called the natural form of the exponential family, also known as the standard form. The set

$$
\Theta^{*}=\left\{\varphi=\left(\varphi_1,\dots,\varphi_k\right):\int\exp\left\{\sum_{i=1}^k\varphi_i T_i\left(x\right)\right\}h\left(x\right)\,\mathrm{d}x< +\infty\right\}
$$

is called the natural parameter space.

**Definition 2.5.1** (Sufficient Statistic)

Let the distribution family of the sample $X_1,X_2,\dots,X_n$ be $f\left(x_1,x_2,\dots,x_n,\theta\right)$, $\theta\in\Theta$, where $\Theta$ is the parameter space. Let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a statistic. If, conditional on $T$, the conditional distribution of the sample $X_1,X_2,\dots,X_n$ does not depend on the parameter $\theta$, then the statistic $T\left(X_1,X_2,\dots,X_n\right)$ is called a sufficient statistic for the parameter $\theta$.

**Theorem 2.5.1** (Factorization Theorem)

Let the joint density function (or joint probability mass function) of the sample $X_1,X_2,\dots,X_n$ be $f\left(x_1,x_2,\dots,x_n,\theta\right)$, depending on the parameter $\theta$, and let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a statistic. Then $T$ is a sufficient statistic if and only if $f\left(x_1,x_2,\dots,x_n,\theta\right)$ can be factorized as

$$
f\left(x_1,x_2,\dots,x_n,\theta\right)=g\left(T\left(x_1,x_2,\dots,x_n\right),\theta\right)h\left(x_1,\dots,x_n\right),
$$

where $h\left(x_1,\dots,x_n\right)$ does not depend on the parameter $\theta$.

**Corollary 2.5.1**

Let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a sufficient statistic for $\theta$, and let $S\left(T\right)$ be a one-to-one invertible function. Then $S\left(T\right)$ is also a sufficient statistic for $\theta$.

**Definition 2.6.1** (Complete Statistic)

Let $\mathcal{F}=\left\{f\left(x;\theta\right),\theta\in\Theta\right\}$ be a family of distributions, where $\Theta$ is the parameter space. Let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a statistic. If, for any $\Phi\left(\cdot\right)$ satisfying $E\left[\Phi\left(T\left(X_1,X_2,\dots,X_n\right)\right)\right]=0$ for all $\theta\in\Theta$, one has $P_\theta\left\{\Phi\left(T\left(X_1,X_2,\dots,X_n\right)\right)=0\right\}=1$ for all $\theta\in\Theta$, then $T\left(X_1,X_2,\dots,X_n\right)$ is called a complete statistic. If $T$ is a complete statistic, then any measurable function $g\left(T\right)$ of it is also a complete statistic.

**Theorem 2.6.1** (Completeness of a Statistic in an Exponential Family)

Let $X_1,X_2,\dots,X_n$ be a sample drawn from the following exponential family (natural form):

$$
f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k\theta_i T_i\left(x\right)\right\}h\left(x\right),\quad \theta=\left(\theta_1,\theta_2,\dots,\theta_k\right)\in\Theta^*\subseteq\mathbb R^k,
$$

If its natural parameter space $\Theta^*$ has an interior point, then $T\left(X_1,X_2,\dots,X_n\right)=\left(T_1\left(X_1,\dots,X_n\right),\dots,T_k\left(X_1,\dots,X_n\right)\right)$ is a complete statistic.

**Theorem 2.5.1** (Factorization Theorem)

Let the joint density function (or joint probability mass function) of the sample $X_1,X_2,\dots,X_n$ be $f\left(x_1,x_2,\dots,x_n;\theta\right)$, and let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a statistic. Then $T$ is a sufficient statistic if and only if $f\left(x_1,x_2,\dots,x_n;\theta\right)$ can be factorized as

$$
f\left(x_1,x_2,\dots,x_n;\theta\right)=g\left(T\left(x_1,x_2,\dots,x_n\right),\theta\right)h\left(x_1,x_2,\dots,x_n\right),
$$

where $h\left(x_1,x_2,\dots,x_n\right)$ does not depend on the parameter $\theta$.

## Point Estimation: Method of Moments and Maximum Likelihood Estimation

**Definition 3.2.1** (Method of Moments Estimator)

Let $\mathcal{F}=\left\{f\left(x;\theta\right):\theta\in\Theta\right\}$ be a parametric family of distributions, where $\theta=\left(\theta_1,\theta_2,\dots,\theta_m\right)$, $\Theta$ is the parameter space, and $X_1,X_2,\dots,X_n$ is a sample drawn from this family. Suppose the $k$-th raw moment of the population $\alpha_k=E\left(X^k\right)$ exists; as a function of $\theta$ it is written as $\alpha_k=\alpha_k\left(\theta_1,\theta_2,\dots,\theta_m\right)$. Let the $k$-th raw moment of the sample be $A_k=\frac{1}{n}\sum_{i=1}^n X_i^k$, take $k=1,2,\dots,m$, equate the population moments with the sample moments, and set up the system of equations

$$
\alpha_k\left(\theta_1,\theta_2,\dots,\theta_m\right)=A_k,\quad k=1,2,\dots,m,
$$

Its solution $\widehat\theta_i=\widehat\theta_i\left(X_1,X_2,\dots,X_n\right)$ is called the method of moments estimator of $\theta_i$. One may also use the sample $k$-th central moment to estimate the population $k$-th central moment and set up the corresponding equations. If one wishes to estimate a function of the parameters $g\left(\theta_1,\dots,\theta_m\right)$, then $g\left(\widehat\theta_1,\dots,\widehat\theta_m\right)$ is taken as its method of moments estimator.

**Example 3.2.1 Conclusion** (Method of Moments Estimators of the Population Mean and Variance)

Let the mean $\mu$ and variance $\sigma^2$ of the population $X$ both exist and be unknown, and let $X_1,X_2,\dots,X_n$ be a sample from the population $X$. Then the method of moments estimator of the population mean is $\widehat\mu=\overline X=\frac{1}{n}\sum_{i=1}^n X_i$, and the method of moments estimator of the population variance is

$$
\widehat\sigma^2=S_n^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\overline X\right)^2.
$$

**Definition 3.3.2** (Maximum Likelihood Estimator)

Let the density function (or probability mass function) of the population be $f\left(x;\theta\right)$, and let $X_1,X_2,\dots,X_n$ be a sample from this population with observed values $x_1,x_2,\dots,x_n$. If the likelihood function $L\left(\theta\right)=L\left(\theta;x_1,x_2,\dots,x_n\right)$ attains its maximum at $\widehat\theta=\widehat\theta\left(x_1,x_2,\dots,x_n\right)$, i.e.

$$
L\left(\widehat\theta\right)=\sup_{\theta\in\Theta}L\left(\theta\right),
$$

then $\widehat\theta\left(x_1,x_2,\dots,x_n\right)$ is called the maximum likelihood estimate of $\theta$, and $\widehat\theta\left(X_1,X_2,\dots,X_n\right)$ is called the maximum likelihood estimator, abbreviated as the maximum likelihood estimate.

**Likelihood Function and Log-Likelihood Function**

For a continuous population, the likelihood function is $L\left(\theta\right)=\prod_{i=1}^n f\left(x_i;\theta\right)$; for a discrete population, the likelihood function is $L\left(\theta\right)=\prod_{i=1}^n P\left(X=x_i;\theta\right)$. The function

$$
\ln L\left(\theta\right)=\sum_{i=1}^n\ln f\left(x_i;\theta\right)
$$

is called the log-likelihood function; $L\left(\theta\right)$ and $\ln L\left(\theta\right)$ attain their extrema at the same parameter.

**How to Find the Maximum Likelihood Estimator**

If the likelihood function is differentiable with respect to $\theta$, then $\widehat\theta$ is found from the log-likelihood equation $\frac{\mathrm{d}\ln L}{\mathrm{d}\theta}=0$ (a system of equations when there are multiple parameters); when the stationary point is unique and is a maximum, it is the maximum likelihood estimator. If the likelihood function is not differentiable, then by **Definition 3.3.2** (Maximum Likelihood Estimator) one directly compares the points where the likelihood function attains its maximum over the parameter space.

**Invariance of the Maximum Likelihood Estimator**

If $\widehat\theta$ is the maximum likelihood estimator of $\theta$, and $g\left(\theta\right)$ is a known function with a one-to-one inverse, then $g\left(\widehat\theta\right)$ is the maximum likelihood estimator of $g\left(\theta\right)$.

## Criteria for Evaluating Estimators

**Definition 3.4.1** (Unbiased Estimator)

Let $\widehat\theta=\widehat\theta\left(X_1,X_2,\dots,X_n\right)$ be an estimator of the unknown parameter $\theta$. If for any $\theta\in\Theta$ one has

$$
E\left[\widehat\theta\left(X_1,X_2,\dots,X_n\right)\right]=\theta,
$$

then $\widehat\theta$ is called an unbiased estimator of $\theta$. For an estimator $\widehat g$ of $g\left(\theta\right)$, if $E\left[\widehat g\right]=g\left(\theta\right)$, then $\widehat g$ is called an unbiased estimator of $g\left(\theta\right)$.

**Definition 3.4.2** (Efficiency)

Let $\widehat\theta_1$ and $\widehat\theta_2$ both be unbiased estimators of $\theta$. If for all $\theta\in\Theta$ one has $D\left(\widehat\theta_1\right)\le D\left(\widehat\theta_2\right)$, with the strict inequality holding for at least one $\theta$, then $\widehat\theta_1$ is said to be more efficient than $\widehat\theta_2$.

**Definition 3.4.3** (Consistent Estimator)

For each natural number $n$, let $\widehat\theta_n=\widehat\theta_n\left(X_1,X_2,\dots,X_n\right)$ be an estimator of $\theta$. If for any $\theta\in\Theta$ and any $\varepsilon> 0$ one has

$$
\lim_{n\to\infty}P\left\{\left|\widehat\theta_n-\theta\right|\ge\varepsilon\right\}=0,
$$

then $\widehat\theta_n$ is called a (weakly) consistent estimator of $\theta$.

**Basic Knowledge** (Chebyshev's Inequality and the Law of Large Numbers)

For any random variable $Y$ and $\varepsilon> 0$, one has $P\left\{\left|Y-EY\right|\ge\varepsilon\right\}\le\frac{D\left(Y\right)}{\varepsilon^2}$; when the variables are independent and identically distributed and the expectation exists, by the law of large numbers $\overline X_n\xrightarrow{P}E\left(X\right)$; convergence in probability is preserved under continuous mappings.

## Uniformly Minimum Variance Unbiased Estimation and the Cramér–Rao Inequality

**Lemma 3.5.1** (A Method for Improving an Unbiased Estimator)

Let $T=T\left(X_1,X_2,\dots,X_n\right)$ be a sufficient statistic, and let $\widehat g\left(X_1,X_2,\dots,X_n\right)$ be an unbiased estimator of $g\left(\theta\right)$. Then $h\left(T\right)=E\left[\widehat g\left(X_1,X_2,\dots,X_n\right)\mid T\right]$ is an unbiased estimator of $g\left(\theta\right)$, and for any $\theta$, $D\left[h\left(T\right)\right]\le D\left[\widehat g\left(X_1,X_2,\dots,X_n\right)\right]$, with equality if and only if $\widehat g\left(X_1,X_2,\dots,X_n\right)=h\left(T\right)$ almost everywhere.

**Theorem 3.5.1** (Lehmann–Scheffé Theorem)

Let $T\left(X\right)=T\left(X_1,X_2,\dots,X_n\right)$ be a sufficient and complete statistic. If $g\left(T\left(X\right)\right)$ is an unbiased estimator of $g\left(\theta\right)$, then $g\left(T\left(X\right)\right)$ is the unique uniformly minimum variance unbiased estimator of $g\left(\theta\right)$.

**Corollary 3.5.1** (Sufficient and Complete Statistic in the Natural Form of an Exponential Family)

Let the sample distribution be the natural form of an exponential family $f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k\theta_iT_i\left(x\right)\right\}h\left(x\right)$. If the natural parameter space, as a subset of $\mathbb R^k$, has an interior point, then $T\left(X\right)=\left(T_1\left(X\right),\dots,T_k\left(X\right)\right)$ is a sufficient and complete statistic; in this case, if $h\left(T\left(X\right)\right)$ is an unbiased estimator of $g\left(\theta\right)$, then it is the unique uniformly minimum variance unbiased estimator of $g\left(\theta\right)$.

**Example 3.5.3** (Sufficient and Complete Statistic for the Two-Point Distribution)

Let $X_1,X_2,\dots,X_n$ be a sample from the two-point distribution $B\left(1,p\right)$, $0< p< 1$. Then $T\left(X_1,X_2,\dots,X_n\right)=\sum_{i=1}^n X_i\sim B\left(n,p\right)$ is a sufficient and complete statistic for $p$, and $\overline X=\frac{1}{n}\sum_{i=1}^n X_i$ is the unique uniformly minimum variance unbiased estimator of $p$.

**Example 3.5.7** (Sufficient and Complete Statistic for a Normal Population)

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$, $\mu\in\mathbb R,\ \sigma^2> 0$. Then $T\left(X\right)=\left(\overline X,\sum_{i=1}^n\left(X_i-\overline X\right)^2\right)$ is a sufficient and complete statistic for $\left(\mu,\sigma^2\right)$, where $\overline X=\frac{1}{n}\sum_{i=1}^n X_i$.

**Sampling Distribution** (Sampling Distribution of a Normal Sample)

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$, and write $\overline X=\frac{1}{n}\sum_{i=1}^n X_i$ and $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\overline X\right)^2$. Then $\overline X\sim N\left(\mu,\frac{\sigma^2}{n}\right)$, $\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$, and $\overline X$ and $S^2$ are independent. In particular, when $\mu=0$, $T=\sum_{i=1}^n X_i^2=\sigma^2\cdot\frac{\sum_{i=1}^n X_i^2}{\sigma^2}\sim\sigma^2\chi^2\left(n\right)$.

**Basic Knowledge** (Moments of the $\chi^2$ Distribution)

If $Y\sim\chi^2\left(k\right)$, then $E\left(Y\right)=k$, $D\left(Y\right)=2k$, $E\left(Y^2\right)=k\left(k+2\right)$, $E\left(\frac{1}{Y}\right)=\frac{1}{k-2}\ \left(k> 2\right)$, $E\left(\sqrt Y\right)=\sqrt 2\,\frac{\Gamma\left(\frac{k+1}{2}\right)}{\Gamma\left(\frac{k}{2}\right)}$.

**Definition 3.6.1** (Regular Family of Distributions)

If a one-parameter family of distributions $\mathcal F=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ satisfies: (1) the parameter space $\Theta$ is an open interval on the real line; (2) for any $\theta\in\Theta$, $f\left(x,\theta\right)> 0$, i.e. the support of the distribution does not depend on the parameter; (3) $\frac{\partial f\left(x,\theta\right)}{\partial\theta}$ exists for any $\theta\in\Theta$; (4) the operations of integration and differentiation of $f\left(x,\theta\right)$ can be interchanged; (5) the Fisher information exists and $0< I\left(\theta\right)=E\left[\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right]^2< +\infty$, then this family is called a Cramér–Rao regular family, where

$$
I\left(\theta\right)=E\left[\left(\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right)^2\right]
$$

is the Fisher information of this family.

**Theorem 3.6.1** (One-Parameter Cramér–Rao Inequality)

Let the family $\mathcal F=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ be a Cramér–Rao regular family, let the estimable function $g\left(\theta\right)$ be differentiable on the parameter space, let $X_1,X_2,\dots,X_n$ be a sample drawn from this population, and let $\widehat g\left(X\right)=\widehat g\left(X_1,X_2,\dots,X_n\right)$ be any unbiased estimator of $g\left(\theta\right)$, with differentiation under the integral sign with respect to $\theta$ permissible. Then

$$
D\left[\widehat g\left(X\right)\right]\ge\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)}.
$$

The right-hand side $\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)}$ is called the Cramér–Rao lower bound. If some unbiased estimator attains this lower bound, then it must be the uniformly minimum variance unbiased estimator.

**Definition 3.6.2** (Efficiency)

Let $\widehat g\left(X\right)$ be an unbiased estimator of $g\left(\theta\right)$. Then the ratio

$$
e\left(\theta\right)=\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)D\left[\widehat g\left(X\right)\right]}
$$

is called the efficiency of the unbiased estimator $\widehat g\left(X\right)$, where $0< e\left(\theta\right)\le1$.

**Definition 3.6.3** (Efficient Estimator)

When $e\left(\theta\right)\equiv1$, $\widehat g\left(X\right)$ is called an efficient estimator of $g\left(\theta\right)$. An efficient estimator is always a uniformly minimum variance unbiased estimator.

**Corollary 3.5.1** (Sufficient and Complete Statistic in the Natural Form of an Exponential Family)

Let the sample distribution be the natural form of an exponential family. If the natural parameter space has an interior point, then $T\left(X\right)$ is a sufficient and complete statistic; in this case, if $h\left(T\left(X\right)\right)$ is an unbiased estimator of $g\left(\theta\right)$, then by **Theorem 3.5.1** (Lehmann–Scheffé Theorem), it is the unique uniformly minimum variance unbiased estimator of $g\left(\theta\right)$.

**Sampling Distribution** (Sampling Distribution of a Normal Sample)

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$. Then $\overline X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right)$. In particular, when $\sigma^2=1$, $\overline X\sim N\left(\mu,\frac{1}{n}\right)$.

## Interval Estimation

**Definition 4.1.1** (Interval Estimator)

Let $\mathcal{F}=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ be a parametric family of distributions, where $\Theta$ is the parameter space, $g\left(\theta\right)$ is a known function defined on $\Theta$, and $X_1,X_2,\dots,X_n$ is a sample drawn from some population in the family $\mathcal{F}$. Let $g_1\left(X_1,X_2,\dots,X_n\right)$ and $g_2\left(X_1,X_2,\dots,X_n\right)$ be functions defined on the sample space, satisfying

$$
g_1\left(X_1,X_2,\dots,X_n\right)\le g_2\left(X_1,X_2,\dots,X_n\right),
$$

then the random interval

$$
\left[g_1\left(X_1,X_2,\dots,X_n\right),g_2\left(X_1,X_2,\dots,X_n\right)\right]
$$

is called an interval estimator of $g\left(\theta\right)$.

**Definition 4.1.4** (Confidence Interval)

Let

$$
\left[\theta_1\left(X_1,X_2,\dots,X_n\right),\theta_2\left(X_1,X_2,\dots,X_n\right)\right]
$$

be an interval estimator of the parameter $\theta$. For a given $0< \alpha< 1$, if for every $\theta\in\Theta$ one has

$$
P_\theta\left\{\theta_1\left(X_1,X_2,\dots,X_n\right)\le\theta\le\theta_2\left(X_1,X_2,\dots,X_n\right)\right\}\ge1-\alpha
$$

then $\left[\theta_1,\theta_2\right]$ is called a confidence interval for the parameter $\theta$ with confidence level $1-\alpha$.

**Definition 4.1.5** (Confidence Limits)

Let $\theta_L\left(X_1,X_2,\dots,X_n\right)$ and $\theta_U\left(X_1,X_2,\dots,X_n\right)$ be statistics defined on the sample space taking values in the parameter space. Given $0< \alpha< 1$, if for every $\theta\in\Theta$ one has $P_\theta\left\{\theta\ge\theta_L\right\}\ge1-\alpha$ and $P_\theta\left\{\theta\le\theta_U\right\}\ge1-\alpha$, then $\theta_L$ and $\theta_U$ are called the one-sided lower confidence limit and one-sided upper confidence limit of the parameter $\theta$ with confidence level $1-\alpha$.

**Sampling Distribution** (Sampling Distribution of a Normal Sample)

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$. Then $\overline X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right)$, and hence $\frac{\sqrt n\left(\overline X-\mu\right)}{\sigma}\sim N\left(0,1\right)$. When $\sigma^2$ is unknown, $\frac{\sqrt n\left(\overline X-\mu\right)}{S}\sim t\left(n-1\right)$, where $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\overline X\right)^2$ is the sample variance.

**Definition 4.2.1** (Pivotal Quantity)

Let $G\left(X_1,X_2,\dots,X_n,\theta\right)$ be a measurable function of the sample $\left(X_1,X_2,\dots,X_n\right)$ and the parameter $\theta$. $G\left(X_1,X_2,\dots,X_n,\theta\right)$ is called a pivotal quantity if and only if the distribution of $G\left(X_1,X_2,\dots,X_n,\theta\right)$ does not depend on the parameter $\theta$.

**Theorem** (Confidence Interval for the Mean of a Single Normal Population)

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$, with $\overline X=\frac{1}{n}\sum_{i=1}^n X_i$ and $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\overline X\right)^2$. When $\sigma^2$ is known, the confidence interval for $\mu$ with confidence level $1-\alpha$ is

$$
\left[\overline X-\frac{\sigma}{\sqrt n}u_{\alpha/2},\overline X+\frac{\sigma}{\sqrt n}u_{\alpha/2}\right];
$$

When $\sigma^2$ is unknown, the confidence interval for $\mu$ with confidence level $1-\alpha$ is

$$
\left[\overline X-\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right),\overline X+\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right)\right].
$$

**Theorem** (Confidence Interval for the Variance of a Single Normal Population)

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$. When $\mu$ is unknown, the confidence interval for $\sigma^2$ with confidence level $1-\alpha$ is

$$
\left[\frac{\left(n-1\right)S^2}{\chi^2_{\alpha/2}\left(n-1\right)},\frac{\left(n-1\right)S^2}{\chi^2_{1-\alpha/2}\left(n-1\right)}\right],
$$

where $\chi^2_\alpha\left(n-1\right)$ denotes the upper $\alpha$ quantile of the $\chi^2$ distribution with $n-1$ degrees of freedom. Correspondingly, the confidence interval for $\sigma$ with confidence level $1-\alpha$ is the square root of the endpoints of the above interval.

**Theorem** (Confidence Interval for the Difference of Means of Two Normal Populations)

Let $X_1,X_2,\dots,X_m$ be a sample from $N\left(\mu_1,\sigma_1^2\right)$ and $Y_1,Y_2,\dots,Y_n$ be a sample from $N\left(\mu_2,\sigma_2^2\right)$, with the two samples independent, let $\overline X,\overline Y$ be the sample means and $S_1^2,S_2^2$ the sample variances. When $\sigma_1^2,\sigma_2^2$ are both known, the confidence interval for $\mu_2-\mu_1$ is

$$
\left[\overline Y-\overline X-u_{\alpha/2}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}},\overline Y-\overline X+u_{\alpha/2}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}\right];
$$

When $\sigma_1^2=\sigma_2^2=\sigma^2$ is unknown, the confidence interval for $\mu_2-\mu_1$ is

$$
\left[\overline Y-\overline X-S_w t_{\alpha/2}\left(m+n-2\right)\sqrt{\frac{1}{m}+\frac{1}{n}},\overline Y-\overline X+S_w t_{\alpha/2}\left(m+n-2\right)\sqrt{\frac{1}{m}+\frac{1}{n}}\right],
$$

where $S_w^2=\frac{\left(m-1\right)S_1^2+\left(n-1\right)S_2^2}{m+n-2}$; when $\sigma_1^2\ne\sigma_2^2$ is unknown, one may use the Welch approximation:

$$
\left[\overline Y-\overline X-t_{\alpha/2}\left(r\right)\sqrt{\frac{S_1^2}{m}+\frac{S_2^2}{n}},\overline Y-\overline X+t_{\alpha/2}\left(r\right)\sqrt{\frac{S_1^2}{m}+\frac{S_2^2}{n}}\right],
$$

where $r=\frac{\left(S_1^2/m+S_2^2/n\right)^2}{\frac{\left(S_1^2/m\right)^2}{m-1}+\frac{\left(S_2^2/n\right)^2}{n-1}}$.

**Theorem** (Confidence Interval for the Ratio of Variances of Two Normal Populations)

Suppose the means of both populations are unknown. Then the confidence interval for $\frac{\sigma_1^2}{\sigma_2^2}$ with confidence level $1-\alpha$ is

$$
\left[\frac{S_1^2/S_2^2}{F_{\alpha/2}\left(m-1,n-1\right)},\frac{S_1^2/S_2^2}{F_{1-\alpha/2}\left(m-1,n-1\right)}\right],
$$

where $F_{\alpha/2}\left(m-1,n-1\right)$ denotes the upper $\alpha/2$ quantile of the $F$ distribution.

**Pivotal Quantity Method** (Construction of Confidence Intervals)

Let $X_1,X_2,\dots,X_n$ be a sample from a population, with unknown parameter $\theta$. If one can construct a function $G\left(X_1,X_2,\dots,X_n,\theta\right)$ of the sample and $\theta$ whose distribution is completely known and does not depend on $\theta$, then $G$ is called a pivotal quantity. For a given confidence level $1-\alpha$, choose $c_1,c_2$ so that $P\left\{c_1\le G\le c_2\right\}=1-\alpha$, then equivalently transform the inequality $c_1\le G\le c_2$ into $\widehat\theta_1\le\theta\le\widehat\theta_2$, which gives the confidence interval $\left[\widehat\theta_1,\widehat\theta_2\right]$ for $\theta$ with confidence level $1-\alpha$.

**Confidence Interval for the Parameter of an Exponential Distribution**

Let $X_1,X_2,\dots,X_n$ be a sample from an exponential population $E\left(\lambda\right)$, whose density function is $f\left(x\right)=\lambda e^{-\lambda x},\ x> 0$. By the additivity of the $\chi^2$ distribution, the pivotal quantity is

$$
T=2\lambda\sum_{i=1}^n X_i=2n\lambda\overline X\sim\chi^2\left(2n\right).
$$

Hence the confidence interval for the mean $\theta=\frac{1}{\lambda}$ with confidence level $1-\alpha$ is

$$
\left[\frac{2n\overline X}{\chi^2_{\alpha/2}\left(2n\right)},\ \frac{2n\overline X}{\chi^2_{1-\alpha/2}\left(2n\right)}\right],
$$

where $\chi^2_{\alpha/2}\left(2n\right)$ and $\chi^2_{1-\alpha/2}\left(2n\right)$ are respectively the upper $\alpha/2$ and upper $1-\alpha/2$ quantiles of the $\chi^2$ distribution with $2n$ degrees of freedom.

**Large-Sample Method** (Approximate Confidence Interval for the Parameter of a Two-Point Distribution)

Let $X_1,X_2,\dots,X_n$ be a sample from the two-point distribution $B\left(1,p\right)$, and let $\overline X$ be the sample mean. By the central limit theorem, when $n$ is sufficiently large, $\frac{\overline X-p}{\sqrt{p\left(1-p\right)/n}}\overset{\mathrm{d}}{\to}N\left(0,1\right)$. Estimating $p$ by $\overline X$, one obtains the approximate confidence interval for $p$ with confidence level $1-\alpha$

$$
\left[\overline X-u_{\alpha/2}\sqrt{\frac{\overline X\left(1-\overline X\right)}{n}},\ \overline X+u_{\alpha/2}\sqrt{\frac{\overline X\left(1-\overline X\right)}{n}}\right],
$$

where $u_{\alpha/2}$ is the upper $\alpha/2$ quantile of the standard normal distribution.

## Hypothesis Testing

**Definition 5.1.1** (Power Function)

Let $\varphi\left(x\right)$ be a test function for the hypothesis testing problem $H_0:\theta\in\Theta_0$; $H_1:\theta\in\Theta_1$. Then the function

$$
\beta\left(\theta\right)=P_\theta\left\{\text{检验函数拒绝原假设 }H_0\right\}=E_\theta\left[\varphi\left(X\right)\right],\ \theta\in\Theta,
$$

is called the power function of the test. For a non-randomized test, $\beta\left(\theta\right)$ is precisely the probability that the sample falls into the rejection domain when the parameter is $\theta$, i.e. the probability of rejecting the null hypothesis $H_0$.

**Two Types of Errors** (Type I Error and Type II Error)

Rejecting $H_0$ when the null hypothesis $H_0$ is true is called making a **Type I error**, with probability $\beta\left(\theta\right),\ \theta\in\Theta_0$; accepting $H_0$ when $H_0$ is not true is called making a **Type II error**, with probability $1-\beta\left(\theta\right),\ \theta\in\Theta_1$.

**Definition 5.1.2** (Significance Test and Test Level)

If the probability that the test function $\varphi\left(x\right)$ makes a Type I error never exceeds $\alpha$, i.e. $\beta\left(\theta\right)\le\alpha,\ \theta\in\Theta_0$, then $\alpha$ is called a level of the test, and $\varphi$ is called a test of significance level $\alpha$, abbreviated as a level-$\alpha$ test.

**Sampling Distribution** (Distribution of the Mean of a Normal Sample)

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$. Then the sample mean

$$
\overline X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right).
$$

**U-Test** (Test for the Mean of a Single Normal Population When the Variance Is Known)

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$, where $\sigma^2=\sigma_0^2$ is known and $\mu$ is unknown. For a given significance level $\alpha$, take the test statistic

$$
U=\frac{\overline X-\mu_0}{\sigma_0/\sqrt n},
$$

When $H_0:\mu=\mu_0$ holds, $U\sim N\left(0,1\right)$. The rejection regions for the three testing problems are: for the two-sided test $H_0:\mu=\mu_0,\ H_1:\mu\ne\mu_0$, the rejection region is $\left\lvert U\right\rvert\ge u_{\alpha/2}$; for the right-sided test $H_0:\mu\le\mu_0,\ H_1:\mu> \mu_0$, the rejection region is $U\ge u_\alpha$; for the left-sided test $H_0:\mu\ge\mu_0,\ H_1:\mu< \mu_0$, the rejection region is $U\le-u_\alpha$.

**t-Test** (Test for the Mean of a Single Normal Population When the Variance Is Unknown)

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$, where $\sigma^2$ is unknown. For a given significance level $\alpha$, take the test statistic

$$
T=\frac{\overline X-\mu_0}{S/\sqrt n},
$$

When $H_0:\mu=\mu_0$ holds, $T\sim t\left(n-1\right)$. The rejection region for the two-sided test is $\left\lvert T\right\rvert\ge t_{\alpha/2}\left(n-1\right)$; for the right-sided test it is $T\ge t_\alpha\left(n-1\right)$; for the left-sided test it is $T\le-t_\alpha\left(n-1\right)$.

**$\chi^2$-Test** (Test for the Variance of a Single Normal Population)

Let $X_1,X_2,\dots,X_n$ be a sample from a normal population $N\left(\mu,\sigma^2\right)$, where $\mu$ is unknown. For a given significance level $\alpha$, take the test statistic

$$
\chi^2=\frac{\left(n-1\right)S^2}{\sigma_0^2},
$$

When $H_0:\sigma^2=\sigma_0^2$ holds, $\chi^2\sim\chi^2\left(n-1\right)$. For the two-sided test $H_0:\sigma^2=\sigma_0^2,\ H_1:\sigma^2\ne\sigma_0^2$, the rejection region is $\chi^2\le\chi^2_{1-\alpha/2}\left(n-1\right)$ or $\chi^2\ge\chi^2_{\alpha/2}\left(n-1\right)$; for the right-sided test $H_0:\sigma^2\le\sigma_0^2,\ H_1:\sigma^2> \sigma_0^2$, the rejection region is $\chi^2\ge\chi^2_\alpha\left(n-1\right)$; for the left-sided test $H_0:\sigma^2\ge\sigma_0^2,\ H_1:\sigma^2< \sigma_0^2$, the rejection region is $\chi^2\le\chi^2_{1-\alpha}\left(n-1\right)$.

**U-Test for the Difference of Means of Two Normal Populations** (When Both Variances Are Known)

Let $X_1,X_2,\dots,X_m$ be from $N\left(\mu_1,\sigma_1^2\right)$ and $Y_1,Y_2,\dots,Y_n$ be from $N\left(\mu_2,\sigma_2^2\right)$, with the two samples independent and both $\sigma_1^2,\sigma_2^2$ known. Take the test statistic

$$
U=\frac{\overline X-\overline Y}{\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}},
$$

When $H_0:\mu_1=\mu_2$ holds, $U\sim N\left(0,1\right)$. The rejection region for the two-sided test is $\left\lvert U\right\rvert\ge u_{\alpha/2}$; for the right-sided test $H_0:\mu_1\le\mu_2,\ H_1:\mu_1> \mu_2$, the rejection region is $U\ge u_\alpha$.

**Pooled t-Test for the Difference of Means of Two Normal Populations** (When Variances Are Unknown but Equal)

Let $X_1,X_2,\dots,X_m$ be from $N\left(\mu_1,\sigma^2\right)$ and $Y_1,Y_2,\dots,Y_n$ be from $N\left(\mu_2,\sigma^2\right)$, with the two samples independent and $\sigma^2$ unknown. Take the pooled sample variance

$$
S_w^2=\frac{\left(m-1\right)S_1^2+\left(n-1\right)S_2^2}{m+n-2},
$$

the test statistic is

$$
T=\frac{\overline X-\overline Y}{S_w\sqrt{\frac1m+\frac1n}},
$$

When $H_0:\mu_1=\mu_2$ holds, $T\sim t\left(m+n-2\right)$. The rejection region for the two-sided test is $\left\lvert T\right\rvert\ge t_{\alpha/2}\left(m+n-2\right)$; for the right-sided test it is $T\ge t_\alpha\left(m+n-2\right)$.

**F-Test** (Test for the Ratio of Variances of Two Normal Populations)

Let $X_1,X_2,\dots,X_m$ be from $N\left(\mu_1,\sigma_1^2\right)$ and $Y_1,Y_2,\dots,Y_n$ be from $N\left(\mu_2,\sigma_2^2\right)$, with the two samples independent and $\mu_1,\mu_2$ unknown. Take the test statistic

$$
F=\frac{S_1^2}{S_2^2},
$$

When $H_0:\sigma_1^2=\sigma_2^2$ holds, $F\sim F\left(m-1,n-1\right)$. For the two-sided test $H_0:\sigma_1^2=\sigma_2^2,\ H_1:\sigma_1^2\ne\sigma_2^2$, the rejection region is $F\le F_{1-\alpha/2}\left(m-1,n-1\right)$ or $F\ge F_{\alpha/2}\left(m-1,n-1\right)$.

**Hypothesis Testing for the Parameter of an Exponential Distribution** (Small-Sample Method)

Let the population $X\sim E\left(\lambda\right)$, whose density function is $f\left(x\right)=\lambda e^{-\lambda x}\left(x> 0\right)$, with $\lambda> 0$ unknown, and let $X_1,X_2,\dots,X_n$ be a sample from the population $X$. By **Theorem 2.3.8**, one has $2n\lambda\overline X\sim\chi^2\left(2n\right)$. For the testing problem $H_0:\lambda=\lambda_0,\ H_1:\lambda\ne\lambda_0$, the rejection region is

$$
D=\left\{2n\lambda_0\overline X\le\chi^2_{1-\alpha/2}\left(2n\right)\ \text{或}\ 2n\lambda_0\overline X\ge\chi^2_{\alpha/2}\left(2n\right)\right\};
$$

For the testing problem $H_0:\lambda\le\lambda_0,\ H_1:\lambda> \lambda_0$, the rejection region is

$$
D=\left\{2n\lambda_0\overline X\le\chi^2_{1-\alpha}\left(2n\right)\right\};
$$

For the testing problem $H_0:\lambda\ge\lambda_0,\ H_1:\lambda< \lambda_0$, the rejection region is

$$
D=\left\{2n\lambda_0\overline X\ge\chi^2_\alpha\left(2n\right)\right\}.
$$

**Test for the Ratio of Parameters of Two Exponential Distributions**

Let $X_1,X_2,\dots,X_m$ be from $E\left(\lambda_1\right)$ and $Y_1,Y_2,\dots,Y_n$ be from $E\left(\lambda_2\right)$, with the two samples independent. Since $2m\lambda_1\overline X\sim\chi^2\left(2m\right)$ and $2n\lambda_2\overline Y\sim\chi^2\left(2n\right)$ are independent, construct an $F$ statistic. When $H_0:\lambda_1=\lambda_2$ holds, one has

$$
\frac{\overline X}{\overline Y}\sim F\left(2m,2n\right).
$$

For the two-sided test $H_0:\lambda_1=\lambda_2,\ H_1:\lambda_1\ne\lambda_2$, the rejection region is

$$
D=\left\{\frac{\overline X}{\overline Y}\le F_{1-\alpha/2}\left(2m,2n\right)\ \text{或}\ \frac{\overline X}{\overline Y}\ge F_{\alpha/2}\left(2m,2n\right)\right\}.
$$

**Large-Sample Method** (Test for the Parameter $p$ of a Binomial Distribution)

Let $X_1,X_2,\dots,X_n$ be from a two-point population $B\left(1,p\right)$, with $0< p< 1$ unknown. When $n$ is sufficiently large (generally requiring $n\ge30$), by the central limit theorem, when $H_0:p=p_0$ holds, one has

$$
U=\frac{\overline X-p_0}{\sqrt{\frac{p_0\left(1-p_0\right)}{n}}}\overset{\text{近似}}{\sim}N\left(0,1\right).
$$

For the two-sided test $H_0:p=p_0,\ H_1:p\ne p_0$, the rejection region is $\left\lvert U\right\rvert\ge u_{\alpha/2}$; for the right-sided test $H_0:p\le p_0,\ H_1:p> p_0$, the rejection region is $U\ge u_\alpha$; for the left-sided test $H_0:p\ge p_0,\ H_1:p< p_0$, the rejection region is $U\le-u_\alpha$.

**Large-Sample Method** (Test for the Parameter $\lambda$ of a Poisson Distribution)

Let $X_1,X_2,\dots,X_n$ be from a Poisson population $P\left(\lambda\right)$, with $\lambda> 0$ unknown. Since $S=\sum_{i=1}^nX_i\sim P\left(n\lambda\right)$, $E\left(S\right)=n\lambda$, $D\left(S\right)=n\lambda$. When $H_0:\lambda=\lambda_0$ holds, by the central limit theorem, one has

$$
U=\frac{S-n\lambda_0}{\sqrt{n\lambda_0}}\overset{\text{近似}}{\sim}N\left(0,1\right),
$$

i.e. $U=\frac{\overline X-\lambda_0}{\sqrt{\lambda_0/n}}\overset{\text{近似}}{\sim}N\left(0,1\right)$. For the two-sided test $H_0:\lambda=\lambda_0,\ H_1:\lambda\ne\lambda_0$, the rejection region is $\left\lvert U\right\rvert\ge u_{\alpha/2}$.

