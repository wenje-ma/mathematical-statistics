# Assignment 16

> **Definition 5.1.1** (Power Function)<br>Let $\varphi\left(x\right)$ be a test function for the hypothesis-testing problem $H_0:\theta\in\Theta_0$; $H_1:\theta\in\Theta_1$. Then the function $$\beta\left(\theta\right)=P_\theta\left\{\text{检验函数拒绝原假设 }H_0\right\}=E_\theta\left[\varphi\left(X\right)\right],\ \theta\in\Theta,$$ is called the power function of the test (also called the efficiency function or power curve). For a non-randomized test, $\beta\left(\theta\right)$ is the probability that the sample falls into the rejection region when the parameter is $\theta$, i.e. the probability of rejecting the null hypothesis $H_0$.

> **Two Types of Error** (Type I Error and Type II Error)<br>Rejecting $H_0$ when the null hypothesis $H_0$ is true is called committing a **Type I error** (error of rejecting a true null hypothesis), whose probability is $\beta\left(\theta\right),\ \theta\in\Theta_0$; accepting $H_0$ when $H_0$ is false is called committing a **Type II error** (error of accepting a false null hypothesis), whose probability is $1-\beta\left(\theta\right),\ \theta\in\Theta_1$.

> **Definition 5.1.2** (Significance Test and Level of the Test)<br>If the probability that the test function $\varphi\left(x\right)$ commits a Type I error never exceeds $\alpha$, i.e. $\beta\left(\theta\right)\le\alpha,\ \theta\in\Theta_0$, then $\alpha$ is called a level of the test, and $\varphi$ is called a test with significance level $\alpha$, abbreviated as a test of level $\alpha$.

> **Sampling Distribution** (Distribution of the Mean of a Normal Sample)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$. Then the sample mean $$\bar X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right).$$

### Problem 1

(Problem 5.1-5) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,1\right)$, where $\mu\in\mathbb R$ is an unknown parameter. Let the rejection region of the testing problem $H_0:\mu=0$; $H_1:\mu=1$ be $D=\left\{\bar X\ge0.98\right\}$.

(1) If $n=4$, find the probability that the test commits a Type I error and the probability that it commits a Type II error;

(2) If the probability that the test commits a Type I error is to be no greater than $0.01$, what is the minimum sample size $n$ to take?

### Solution to Problem 1

By **Sampling Distribution** (Distribution of the Mean of a Normal Sample), under $H_0:\mu=0$, $\bar X\sim N\left(0,\frac{1}{n}\right)$, and under $H_1:\mu=1$, $\bar X\sim N\left(1,\frac{1}{n}\right)$. By **Definition 5.1.1** (Power Function), $\beta\left(\mu\right)=P_\mu\left\{\bar X\ge0.98\right\}$.

(1) When $n=4$, under $H_0$, $\bar X\sim N\left(0,\frac{1}{4}\right)$. By **Two Types of Error** (Type I Error and Type II Error), the probability of committing a Type I error is

$$
\alpha=\beta\left(0\right)=P_0\left\{\bar X\ge0.98\right\}=P\left\{Z\ge\frac{0.98}{1/2}\right\}=P\left\{Z\ge1.96\right\}=0.025,
$$

where $Z\sim N\left(0,1\right)$.

The probability of committing a Type II error is

$$
\beta_2=1-\beta\left(1\right)=P_1\left\{\bar X< 0.98\right\}=P\left\{Z< \frac{0.98-1}{1/2}\right\}=P\left\{Z< -0.04\right\}=\Phi\left(-0.04\right)=0.484.
$$

(2) By **Definition 5.1.2** (Significance Test and Level of the Test), requiring the probability of a Type I error to be no greater than $0.01$, i.e.

$$
\beta\left(0\right)=P_0\left\{\bar X\ge0.98\right\}=P\left\{Z\ge0.98\sqrt n\right\}\le0.01.
$$

Hence $0.98\sqrt n\ge u_{0.01}=2.326$, i.e. $\sqrt n\ge2.373$, $n\ge5.64$. Therefore the minimum sample size $n$ is $6$.

$\blacksquare$

### Problem 2

(Problem 5.1-7) Let the sample $X$ (of size $1$) be drawn from a population with density function $f\left(\cdot\right)$, with the following two hypotheses about the population:

$$
H_0:f\left(x\right)=\begin{cases}1,&0< x< 1,\\0,&\text{其他};\end{cases}\ \ H_1:f\left(x\right)=\begin{cases}2x,&0< x< 1,\\0,&\text{其他}.\end{cases}
$$

Let the rejection region of this test be $D=\left\{X> \frac{2}{3}\right\}$. Find the probability that the test commits a Type I error and the probability that it commits a Type II error.

### Solution to Problem 2

By **Two Types of Error** (Type I Error and Type II Error), the probability of committing a Type I error is the probability that the sample falls into the rejection region when $H_0$ is true, i.e.

$$
\alpha=P_{H_0}\left\{X> \frac{2}{3}\right\}=\int_{2/3}^1 1\,\mathrm dx=\frac{1}{3}.
$$

The probability of committing a Type II error is the probability that the sample falls into the acceptance region when $H_1$ is true, i.e.

$$
\beta_2=P_{H_1}\left\{X\le\frac{2}{3}\right\}=\int_0^{2/3}2x\,\mathrm dx=\left[x^2\right]_0^{2/3}=\frac{4}{9}.
$$

$\blacksquare$

### Problem 3

(Problem 5.1-8) Let $X_1,X_2,\dots,X_{10}$ be a sample from the uniform-distribution population $U\left[0,\theta\right]$, where $\theta> 0$ is an unknown parameter. Let the rejection region of the testing problem $H_0:\theta=1$; $H_1:\theta> 1$ be $D=\left\{\left(X_1,\dots,X_{10}\right):X_{\left(10\right)}\ge0.95\right\}$, where $X_{\left(10\right)}=\max\left\{X_1,\dots,X_{10}\right\}$.

(1) Find the significance level of this test;

(2) Find the power function of this test.

### Solution to Problem 3

For the uniform-distribution population $U\left[0,\theta\right]$, its distribution function is $F_\theta\left(x\right)=\frac{x}{\theta},\ 0\le x\le\theta$. By the distribution of order statistics, for $0\le t\le\theta$,

$$
P_\theta\left\{X_{\left(10\right)}< t\right\}=\prod_{i=1}^{10}P_\theta\left\{X_i< t\right\}=\left(\frac{t}{\theta}\right)^{10}.
$$

By **Definition 5.1.1** (Power Function), the power function is $\beta\left(\theta\right)=P_\theta\left\{X_{\left(10\right)}\ge0.95\right\}$.

(1) The null hypothesis $H_0:\theta=1$ is a simple hypothesis. By **Definition 5.1.2** (Significance Test and Level of the Test), the level of the test is

$$
\beta\left(1\right)=P_1\left\{X_{\left(10\right)}\ge0.95\right\}=1-P_1\left\{X_{\left(10\right)}< 0.95\right\}=1-0.95^{10}=0.4013.
$$

(2) Discuss the power function in two cases. When $0< \theta\le0.95$, all $X_i\le\theta\le0.95$, so $X_{\left(10\right)}\le0.95$ always holds, and $\beta\left(\theta\right)=0$; when $\theta> 0.95$,

$$
\beta\left(\theta\right)=1-P_\theta\left\{X_{\left(10\right)}< 0.95\right\}=1-\left(\frac{0.95}{\theta}\right)^{10}.
$$

In summary,

$$
\beta\left(\theta\right)=\begin{cases}0,&0< \theta\le0.95,\\1-\left(\frac{0.95}{\theta}\right)^{10},&\theta> 0.95.\end{cases}
$$

$\blacksquare$
