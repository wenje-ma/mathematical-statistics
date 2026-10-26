# Assignment 1

> **Definition 1.2.1** (Population)<br>In mathematical statistics, the entire collection of the objects under study involved in the problem being investigated is called the population. Each element making up the population is called an individual. The number of individuals contained in the population is called the population size. In practice, a population can be described by a random variable $X$ and its distribution; the study of the population is then transformed into the study of the statistical regularity of the random variable $X$ representing the population. Henceforth we shall not distinguish between the population and the corresponding random variable, and both are collectively referred to as the population $X$.

> **Definition 1.3.1** (Sample Space)<br>The set of all possible values of the sample $X_1,X_2,\dots,X_n$ is called the sample space.

> **Definition 1.3.2** (Simple Random Sample)<br>Let there be a population $X$ with distribution $F$, and let $X_1,X_2,\dots,X_n$ be a sample of size $n$ drawn from the population $X$. If<br>(1) $X_1,X_2,\dots,X_n$ are mutually independent;<br>(2) $X_1,X_2,\dots,X_n$ have the same distribution $F$ as the population $X$,<br>then $X_1,X_2,\dots,X_n$ is called a simple random sample of size $n$ drawn from the population $X$, abbreviated as a sample.

> **Sample Distribution** (Joint Distribution Function, Joint Probability Mass Function and Joint Density Function)<br>Let the distribution function of the population $X$ be $F\left(x\right)$, and let $X_1,X_2,\dots,X_n$ be a sample from the population $X$. Then the joint distribution function of the sample is $$F^{*}\left(x_1,x_2,\dots,x_n\right)=\prod_{i=1}^n F\left(x_i\right).$$ If the population $X$ is a discrete random variable with probability mass function $P\left\{X=a_i\right\}=p_i$, then the joint probability mass function of the sample $X_1,X_2,\dots,X_n$ is $$P\left\{X_1=x_1,\dots,X_n=x_n\right\}=\prod_{i=1}^n p_{x_i}.$$ If the population $X$ is a continuous random variable with density function $f\left(x\right)$, then the joint density function of the sample $X_1,X_2,\dots,X_n$ is $$f^{*}\left(x_1,x_2,\dots,x_n\right)=\prod_{i=1}^n f\left(x_i\right).$$

> **Definition 1.3.3** (Parameter Space)<br>In mathematical statistics, the unknown constants appearing in the population distribution or the sample distribution are called parameters. The set of all possible values of the parameter $\theta$ is called the parameter space, denoted by $\Theta$.

> **Population Distribution Family and Sample Distribution Family**<br>Since different parameter values generally correspond to different population distributions, all possible parameter values in the parameter space correspond to a family of population distributions, called the population distribution family, denoted by $\left\{f\left(x;\theta\right):\theta\in\Theta\right\}$. Different parameter values also generally correspond to different sample distributions; all possible parameter values in the parameter space correspond to a family of sample distributions, called the sample distribution family, denoted by $$\left\{\prod_{i=1}^n f\left(x_i;\theta\right):\theta\in\Theta\right\}.$$

> **Definition 1.4.1** (Statistic)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and let $g\left(X_1,X_2,\dots,X_n\right)$ be a function of the sample $X_1,X_2,\dots,X_n$ that, besides depending on the sample, does not depend on any other unknown quantity; then $g\left(X_1,X_2,\dots,X_n\right)$ is called a statistic. If $x_1,x_2,\dots,x_n$ are the observed values of the sample $X_1,X_2,\dots,X_n$, then $g\left(x_1,x_2,\dots,x_n\right)$ is called an observed value of the statistic $g\left(X_1,X_2,\dots,X_n\right)$. A statistic depends only on the sample and does not depend on any unknown parameter.

> **Definition 1.5.1** (Empirical Distribution Function)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and let $X_{\left(1\right)}\le X_{\left(2\right)}\le\dots\le X_{\left(n\right)}$ be its order statistics. For any real number $x$, $$F_n\left(x\right)=\begin{cases}0,&x< X_{\left(1\right)},\\\frac{r}{n},&X_{\left(r\right)}\le x< X_{\left(r+1\right)},\ r=1,2,\dots,n-1,\\1,&x\ge X_{\left(n\right)}\end{cases}$$ is called the empirical distribution function of the sample $X_1,X_2,\dots,X_n$.

### Problem 1

(Problem 1-1) What is a population? What is a sample?

### Solution to Problem 1

By **Definition 1.2.1** (Population), the entire collection of the objects under study involved in the problem being investigated is the population, and each element making up the population is an individual. From the introduction in Chapter 1, the process of randomly drawing a part of the individuals from the population for observation is called sampling, and the part of the individuals drawn is called the sample. Specifically, let $X_1,X_2,\dots,X_n$ be a sample drawn from the population $X$; by **Definition 1.3.2** (Simple Random Sample), these individuals should be identically distributed with the population $X$ and mutually independent. $\blacksquare$

### Problem 2

(Problem 1-2) What conditions should a simple random sample satisfy?

### Solution to Problem 2

By **Definition 1.3.2** (Simple Random Sample), let there be a population $X$ with distribution $F$, and let $X_1,X_2,\dots,X_n$ be a sample of size $n$ drawn from the population $X$. If $X_1,X_2,\dots,X_n$ satisfies:

(1) $X_1,X_2,\dots,X_n$ are mutually independent;

(2) $X_1,X_2,\dots,X_n$ have the same distribution $F$ as the population $X$,

then it is called a simple random sample. That is, a simple random sample should satisfy the two conditions of **independence** and **representativeness** (identical distribution). $\blacksquare$

### Problem 3

(Problem 1-4) Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$. In each of the following three cases, write down the joint probability mass function or joint density function of the sample $X_1,X_2,\dots,X_n$:

(1) the population $X$ follows the geometric distribution with probability mass function $P\left\{X=x\right\}=\left(1-p\right)^{x-1}p,\ 0< p< 1,\ x=1,2,\dots$;

(2) the population $X$ follows the exponential distribution with density function $f\left(x\right)=\lambda e^{-\lambda x},\ x> 0$ (which is $0$ when $x\le0$), where $\lambda> 0$;

(3) the population $X$ has density function $f\left(x\right)=\frac{\lambda}{2}e^{-\lambda\left|x\right|},\ -\infty< x< +\infty$, where $\lambda> 0$.

### Solution to Problem 3

By **Sample Distribution** (Joint Probability Mass Function and Joint Density Function), if the population $X$ has probability mass function $P\left\{X=x\right\}$, then the joint probability mass function of the sample is $\prod_{i=1}^n P\left\{X=x_i\right\}$; if the population $X$ has density function $f\left(x\right)$, then the joint density function of the sample is $\prod_{i=1}^n f\left(x_i\right)$.

(1) The population $X$ follows the geometric distribution $P\left\{X=x\right\}=\left(1-p\right)^{x-1}p$, so the joint probability mass function of the sample is
$$
P\left\{X_1=x_1,\dots,X_n=x_n\right\}=\prod_{i=1}^n\left(1-p\right)^{x_i-1}p=p^n\left(1-p\right)^{\sum_{i=1}^n x_i-n},\quad x_i=1,2,\dots
$$

(2) The population $X$ follows the exponential distribution $f\left(x\right)=\lambda e^{-\lambda x}$, so the joint density function of the sample is
$$
f\left(x_1,\dots,x_n\right)=\prod_{i=1}^n\lambda e^{-\lambda x_i}=\lambda^n e^{-\lambda\sum_{i=1}^n x_i},\quad x_i> 0.
$$

(3) The population $X$ has density function $f\left(x\right)=\frac{\lambda}{2}e^{-\lambda\left|x\right|}$, so the joint density function of the sample is
$$
f\left(x_1,\dots,x_n\right)=\prod_{i=1}^n\frac{\lambda}{2}e^{-\lambda\left|x_i\right|}=\left(\frac{\lambda}{2}\right)^n e^{-\lambda\sum_{i=1}^n\left|x_i\right|},\quad x_i\in\mathbb R.
$$

$\blacksquare$

### Problem 4

(Problem 1-6) Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$. Write down the sample distribution families for the two-point distribution, binomial distribution, Poisson distribution, geometric distribution, uniform distribution, exponential distribution, and normal distribution.

### Solution to Problem 4

By **Population Distribution Family and Sample Distribution Family**, the sample distribution family is $\left\{\prod_{i=1}^n f\left(x_i;\theta\right):\theta\in\Theta\right\}$, where $f\left(x;\theta\right)$ is the population's probability mass function (or density function), and $\Theta$ is the parameter space (**Definition 1.3.3**).

(1) Two-point distribution $B\left(1,p\right)$, parameter space $\Theta=\left\{p:0< p< 1\right\}$: the sample distribution family is
$$
\left\{\prod_{i=1}^n p^{x_i}\left(1-p\right)^{1-x_i}:0< p< 1\right\},\quad x_i\in\left\{0,1\right\}.
$$

(2) Binomial distribution $B\left(m,p\right)$, parameter space $\Theta=\left\{p:0< p< 1\right\}$: the sample distribution family is
$$
\left\{\prod_{i=1}^n\binom{m}{x_i}p^{x_i}\left(1-p\right)^{m-x_i}:0< p< 1\right\},\quad x_i=0,1,\dots,m.
$$

(3) Poisson distribution $P\left(\lambda\right)$, parameter space $\Theta=\left\{\lambda:\lambda> 0\right\}$: the sample distribution family is
$$
\left\{\prod_{i=1}^n\frac{e^{-\lambda}\lambda^{x_i}}{x_i!}:\lambda> 0\right\},\quad x_i=0,1,2,\dots
$$

(4) Geometric distribution $G\left(p\right)$, parameter space $\Theta=\left\{p:0< p< 1\right\}$: the sample distribution family is
$$
\left\{\prod_{i=1}^n\left(1-p\right)^{x_i-1}p:0< p< 1\right\},\quad x_i=1,2,\dots
$$

(5) Uniform distribution $U\left[a,b\right]$, parameter space $\Theta=\left\{\left(a,b\right):-\infty< a< b< +\infty\right\}$: the sample distribution family is
$$
\left\{\prod_{i=1}^n\frac{1}{b-a}:-\infty< a< b< +\infty\right\},\quad x_i\in\left[a,b\right].
$$

(6) Exponential distribution $E\left(\lambda\right)$, parameter space $\Theta=\left\{\lambda:\lambda> 0\right\}$: the sample distribution family is
$$
\left\{\prod_{i=1}^n\lambda e^{-\lambda x_i}:\lambda> 0\right\},\quad x_i> 0.
$$

(7) Normal distribution $N\left(\mu,\sigma^2\right)$, parameter space $\Theta=\left\{\left(\mu,\sigma^2\right):\mu\in\mathbb R,\ \sigma> 0\right\}$: the sample distribution family is
$$
\left\{\prod_{i=1}^n\frac{1}{\sqrt{2\pi}\sigma}\exp\left\{-\frac{\left(x_i-\mu\right)^2}{2\sigma^2}\right\}:\mu\in\mathbb R,\ \sigma> 0\right\},\quad x_i\in\mathbb R.
$$

$\blacksquare$

### Problem 5

(Problem 1-7) The diameters of parts machined by a certain machine tool follow the normal distribution $N\left(\mu,\sigma^2\right)$, where $\mu,\sigma^2$ are both unknown. In order to estimate $\mu,\sigma^2$, $n$ machined parts are randomly selected and measured, yielding the $n$ data $x_1,x_2,\dots,x_n$. Write down the statistical model of this problem (namely the parameter space and the sample distribution family).

### Solution to Problem 5

By **Definition 1.3.3** (Parameter Space), the parameter is $\theta=\left(\mu,\sigma^2\right)$, and its range of values, i.e. the parameter space, is
$$
\Theta=\left\{\left(\mu,\sigma^2\right):\mu\in\mathbb R,\ \sigma^2> 0\right\}.
$$

By **Population Distribution Family and Sample Distribution Family**, the density function of the normal population $N\left(\mu,\sigma^2\right)$ is $f\left(x;\mu,\sigma^2\right)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{\left(x-\mu\right)^2}{2\sigma^2}}$, so the sample distribution family is
$$
\left\{\prod_{i=1}^n\frac{1}{\sqrt{2\pi}\sigma}\exp\left\{-\frac{\left(x_i-\mu\right)^2}{2\sigma^2}\right\}:\left(\mu,\sigma^2\right)\in\Theta\right\},\quad x_i\in\mathbb R.
$$

$\blacksquare$

### Problem 6

(Problem 1-8) Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, where $\mu$ is known and $\sigma^2$ is unknown. Determine which of the following quantities are statistics and which are not statistics, and why?
$$
\frac{1}{n}\sum_{i=1}^n X_i,\quad\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\overline X\right)^2,\quad\frac{1}{\sigma^2}\sum_{i=1}^n X_i^2,\quad\frac{1}{n}\sum_{i=1}^n\left(X_i-\mu\right)^2,
$$
$$
\frac{1}{\sigma^2}\sum_{i=1}^n\left(X_i-\mu\right)^2,\quad X_1+2\mu,\quad\max\left\{X_1,\dots,X_n\right\},\quad\min\left\{X_1,\dots,X_n\right\}.
$$

### Solution to Problem 6

By **Definition 1.4.1** (Statistic), a statistic is a function of the sample and, apart from the sample, does not depend on any unknown quantity. In this problem $\mu$ is known and $\sigma^2$ is unknown, so any quantity containing the unknown parameter $\sigma^2$ is not a statistic; the others are statistics.

- $\frac{1}{n}\sum_{i=1}^n X_i$: contains only the sample; it is a statistic.
- $\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\overline X\right)^2$: contains only the sample ($\overline X$ is the sample mean); it is a statistic.
- $\frac{1}{\sigma^2}\sum_{i=1}^n X_i^2$: contains the unknown parameter $\sigma^2$; it is not a statistic.
- $\frac{1}{n}\sum_{i=1}^n\left(X_i-\mu\right)^2$: $\mu$ is known and it contains only the sample and known constants; it is a statistic.
- $\frac{1}{\sigma^2}\sum_{i=1}^n\left(X_i-\mu\right)^2$: contains the unknown parameter $\sigma^2$; it is not a statistic.
- $X_1+2\mu$: $\mu$ is known; it is a statistic.
- $\max\left\{X_1,\dots,X_n\right\}$: contains only the sample; it is a statistic.
- $\min\left\{X_1,\dots,X_n\right\}$: contains only the sample; it is a statistic.

$\blacksquare$

### Problem 7

(Problem 1-9) A reading-ability test is given to 10 third-grade children, with the following scores: $95,86,78,90,62,73,89,92,84,76$. Find the corresponding empirical distribution function and plot its graph.

### Solution to Problem 7

By **Definition 1.5.1** (Empirical Distribution Function), first sort the sample observed values in increasing order as
$$
x_{\left(1\right)}=62,\ x_{\left(2\right)}=73,\ x_{\left(3\right)}=76,\ x_{\left(4\right)}=78,\ x_{\left(5\right)}=84,\ x_{\left(6\right)}=86,\ x_{\left(7\right)}=89,\ x_{\left(8\right)}=90,\ x_{\left(9\right)}=92,\ x_{\left(10\right)}=95.
$$

Then the empirical distribution function $F_{10}\left(x\right)$ is a right-continuous step function that jumps by $\frac{1}{10}$ at each order statistic:
$$
F_{10}\left(x\right)=\begin{cases}0,&x< 62,\\\frac{1}{10},&62\le x< 73,\\\frac{2}{10},&73\le x< 76,\\\frac{3}{10},&76\le x< 78,\\\frac{4}{10},&78\le x< 84,\\\frac{5}{10},&84\le x< 86,\\\frac{6}{10},&86\le x< 89,\\\frac{7}{10},&89\le x< 90,\\\frac{8}{10},&90\le x< 92,\\\frac{9}{10},&92\le x< 95,\\1,&x\ge95.\end{cases}
$$

Its graph is a right-continuous step function starting at $62$ and ending at $95$, jumping by $\frac{1}{10}$ at each of the points $62,73,76,78,84,86,89,90,92,95$, taking the values $\frac{1}{10},\frac{2}{10},\dots,1$ in turn. $\blacksquare$

### Problem 8

(Problem 1-10) Let $F\left(x\right)$ be the distribution function of the population $X$, let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and let $F_n\left(x\right)$ be its empirical distribution function. Prove that for any given real number $x$,

(1) $E\left(F_n\left(x\right)\right)=F\left(x\right)$;

(2) $D\left(F_n\left(x\right)\right)=\frac{1}{n}F\left(x\right)\left(1-F\left(x\right)\right)$.

### Solution to Problem 8

Write the indicator function as $I\left\{X_i\le x\right\}=\begin{cases}1,&X_i\le x,\\0,&X_i> x.\end{cases}$ Then by **Definition 1.5.1** (Empirical Distribution Function), $F_n\left(x\right)=\frac{1}{n}\sum_{i=1}^n I\left\{X_i\le x\right\}$.

(1) By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are identically distributed with the population $X$, so for each $i$,
$$
E\left[I\left\{X_i\le x\right\}\right]=P\left(X_i\le x\right)=F\left(x\right).
$$
Hence, by the linearity of expectation,
$$
E\left[F_n\left(x\right)\right]=\frac{1}{n}\sum_{i=1}^n E\left[I\left\{X_i\le x\right\}\right]=\frac{1}{n}\cdot nF\left(x\right)=F\left(x\right).
$$

(2) For the indicator variable $I\left\{X_i\le x\right\}$, it is a two-point variable taking the value $1$ with probability $F\left(x\right)$, so by (1) its variance is
$$
D\left[I\left\{X_i\le x\right\}\right]=F\left(x\right)\left(1-F\left(x\right)\right).
$$
Also, by **Definition 1.3.2**, $X_1,X_2,\dots,X_n$ are mutually independent, so $I\left\{X_i\le x\right\}$ are mutually independent. Hence
$$
D\left[F_n\left(x\right)\right]=\frac{1}{n^2}\sum_{i=1}^n D\left[I\left\{X_i\le x\right\}\right]=\frac{1}{n^2}\cdot nF\left(x\right)\left(1-F\left(x\right)\right)=\frac{1}{n}F\left(x\right)\left(1-F\left(x\right)\right).
$$

$\blacksquare$
