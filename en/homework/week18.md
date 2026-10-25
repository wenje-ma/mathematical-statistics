# Assignment 18

> **Hypothesis Testing for the Parameter of an Exponential Distribution** (Small-sample Method)<br>Let the population $X\sim E\left(\lambda\right)$, whose density function is $f\left(x\right)=\lambda e^{-\lambda x}\left(x> 0\right)$, where $\lambda> 0$ is unknown, and let $X_1,X_2,\dots,X_n$ be a sample from the population $X$. By **Theorem 2.3.8**, we have $2n\lambda\bar X\sim\chi^2\left(2n\right)$. For the testing problem $H_0:\lambda=\lambda_0,\ H_1:\lambda\ne\lambda_0$, the rejection region is $$D=\left\{2n\lambda_0\bar X\le\chi^2_{1-\alpha/2}\left(2n\right)\ \text{或}\ 2n\lambda_0\bar X\ge\chi^2_{\alpha/2}\left(2n\right)\right\};$$ for the testing problem $H_0:\lambda\le\lambda_0,\ H_1:\lambda> \lambda_0$, the rejection region is $$D=\left\{2n\lambda_0\bar X\le\chi^2_{1-\alpha}\left(2n\right)\right\};$$ for the testing problem $H_0:\lambda\ge\lambda_0,\ H_1:\lambda< \lambda_0$, the rejection region is $$D=\left\{2n\lambda_0\bar X\ge\chi^2_\alpha\left(2n\right)\right\}.$$

> **Test for the Ratio of Parameters of Two Exponential Distributions**<br>Let $X_1,X_2,\dots,X_m$ be from $E\left(\lambda_1\right)$ and $Y_1,Y_2,\dots,Y_n$ from $E\left(\lambda_2\right)$, with the two samples independent. Since $2m\lambda_1\bar X\sim\chi^2\left(2m\right)$ and $2n\lambda_2\bar Y\sim\chi^2\left(2n\right)$ are independent, construct an $F$ statistic. When $H_0:\lambda_1=\lambda_2$ holds, we have $$\frac{\bar X}{\bar Y}\sim F\left(2m,2n\right).$$ For the two-sided test $H_0:\lambda_1=\lambda_2,\ H_1:\lambda_1\ne\lambda_2$, the rejection region is $$D=\left\{\frac{\bar X}{\bar Y}\le F_{1-\alpha/2}\left(2m,2n\right)\ \text{或}\ \frac{\bar X}{\bar Y}\ge F_{\alpha/2}\left(2m,2n\right)\right\}.$$

> **Large-sample Method** (Test for the Binomial Distribution Parameter $p$)<br>Let $X_1,X_2,\dots,X_n$ be from the two-point-distribution population $B\left(1,p\right)$, with $0< p< 1$ unknown. When $n$ is sufficiently large (generally requiring $n\ge30$), by the central limit theorem, when $H_0:p=p_0$ holds, we have $$U=\frac{\bar X-p_0}{\sqrt{\frac{p_0\left(1-p_0\right)}{n}}}\overset{\text{近似}}{\sim}N\left(0,1\right).$$ For the two-sided test $H_0:p=p_0,\ H_1:p\ne p_0$, the rejection region is $\left\lvert U\right\rvert\ge u_{\alpha/2}$; for the right-tailed test $H_0:p\le p_0,\ H_1:p> p_0$, the rejection region is $U\ge u_\alpha$; for the left-tailed test $H_0:p\ge p_0,\ H_1:p< p_0$, the rejection region is $U\le-u_\alpha$.

> **Large-sample Method** (Test for the Poisson Distribution Parameter $\lambda$)<br>Let $X_1,X_2,\dots,X_n$ be from the Poisson-distribution population $P\left(\lambda\right)$, with $\lambda> 0$ unknown. Since $S=\sum_{i=1}^nX_i\sim P\left(n\lambda\right)$, $E\left(S\right)=n\lambda$, $D\left(S\right)=n\lambda$. When $H_0:\lambda=\lambda_0$ holds, by the central limit theorem, we have $$U=\frac{S-n\lambda_0}{\sqrt{n\lambda_0}}\overset{\text{近似}}{\sim}N\left(0,1\right),$$ i.e. $U=\frac{\bar X-\lambda_0}{\sqrt{\lambda_0/n}}\overset{\text{近似}}{\sim}N\left(0,1\right)$. For the two-sided test $H_0:\lambda=\lambda_0,\ H_1:\lambda\ne\lambda_0$, the rejection region is $\left\lvert U\right\rvert\ge u_{\alpha/2}$.

### Problem 1

(Problem 5.3-1) A company produces $40\mathrm{W}$ light bulbs and claims that the mean service life of the bulbs is $1000\mathrm{h}$. A consumer randomly samples $4$ bulbs for a test, obtaining their service lives as $980\mathrm{h}$, $1005\mathrm{h}$, $992\mathrm{h}$, $973\mathrm{h}$, and computes the mean service life as $987.5\mathrm{h}$. If the service life of the bulbs is assumed to follow an exponential distribution, ask whether, at significance level $0.05$, there is sufficient evidence to believe that the mean service life is less than $1000\mathrm{h}$.

### Solution to Problem 1

The bulb service life follows an exponential distribution $E\left(\lambda\right)$, with mean life $1/\lambda$. The company claims the mean life is $1000\mathrm{h}$, i.e. $1/\lambda=1000$, equivalently $\lambda=1/1000$. The consumer suspects the mean life is less than $1000\mathrm{h}$, i.e. $1/\lambda< 1000$, equivalently $\lambda> 1/1000$. By **Hypothesis Testing for the Parameter of an Exponential Distribution** (Small-sample Method), this is a right-tailed testing problem. Set up the hypotheses

$$
H_0:\lambda\le\lambda_0=\frac{1}{1000},\quad H_1:\lambda> \lambda_0.
$$

By **Hypothesis Testing for the Parameter of an Exponential Distribution**, the test statistic is $2n\lambda_0\bar X$, whose rejection region is

$$
D=\left\{2n\lambda_0\bar X\le\chi^2_{1-\alpha}\left(2n\right)\right\}.
$$

Substituting $n=4$, $\bar x=987.5$, $\lambda_0=1/1000$, $\alpha=0.05$, we get

$$
2n\lambda_0\bar x=2\times4\times\frac{1}{1000}\times987.5=7.9.
$$

From the $\chi^2$-distribution table, $\chi^2_{0.95}\left(8\right)=2.733$ (i.e. the upper quantile corresponding to $8$ degrees of freedom and lower-tail probability $0.05$, namely $\chi^2_{1-\alpha}\left(2n\right)=\chi^2_{0.95}\left(8\right)$). Since $7.9> 2.733$, the sample does not fall into the rejection region, so the null hypothesis is not rejected at significance level $\alpha=0.05$, i.e. there is no sufficient evidence to believe that the mean service life of the bulbs is less than $1000\mathrm{h}$. $\blacksquare$

### Problem 2

(Problem 5.3-3) Let $X_1,X_2,\dots,X_m$ be a sample from the exponential-distribution population $E\left(\lambda_1\right)$, where $\lambda_1> 0$ is an unknown parameter, and $Y_1,Y_2,\dots,Y_n$ a sample from the exponential-distribution population $E\left(\lambda_2\right)$, where $\lambda_2> 0$ is an unknown parameter, with the two samples mutually independent. At significance level $\alpha$, test the hypotheses $\lambda_1=\lambda_2$ against $\lambda_1\ne\lambda_2$.

### Solution to Problem 2

From the conclusion $2n\lambda\bar X\sim\chi^2\left(2n\right)$ in **Hypothesis Testing for the Parameter of an Exponential Distribution** (Small-sample Method), we have

$$
2m\lambda_1\bar X\sim\chi^2\left(2m\right),\quad 2n\lambda_2\bar Y\sim\chi^2\left(2n\right),
$$

and since the two samples are independent, the above two $\chi^2$ variables are mutually independent. By **Test for the Ratio of Parameters of Two Exponential Distributions**, construct the $F$ statistic

$$
F=\frac{\frac{2m\lambda_1\bar X}{2m}}{\frac{2n\lambda_2\bar Y}{2n}}=\frac{\lambda_1\bar X}{\lambda_2\bar Y}.
$$

When $H_0:\lambda_1=\lambda_2=\lambda$ holds, $\lambda$ cancels out, giving

$$
F=\frac{\bar X}{\bar Y}\sim F\left(2m,2n\right).
$$

By **Test for the Ratio of Parameters of Two Exponential Distributions**, the rejection region for the two-sided test is

$$
D=\left\{\frac{\bar X}{\bar Y}\le F_{1-\alpha/2}\left(2m,2n\right)\ \text{或}\ \frac{\bar X}{\bar Y}\ge F_{\alpha/2}\left(2m,2n\right)\right\}.
$$

That is, if the sample observations satisfy $\frac{\bar x}{\bar y}\le F_{1-\alpha/2}\left(2m,2n\right)$ or $\frac{\bar x}{\bar y}\ge F_{\alpha/2}\left(2m,2n\right)$, then the null hypothesis $H_0$ is rejected at significance level $\alpha$, and $\lambda_1\ne\lambda_2$ is believed; otherwise $H_0$ is not rejected. $\blacksquare$

### Problem 3

(Problem 5.3-4) Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, where $X\sim P\left(\lambda\right)$, and $\lambda> 0$ is an unknown parameter. At significance level $\alpha$, use the large-sample method to find the rejection region for testing $H_0:\lambda=\lambda_0$; $H_1:\lambda\ne\lambda_0$.

### Solution to Problem 3

By **Large-sample Method** (Test for the Poisson Distribution Parameter $\lambda$), let $S=\sum_{i=1}^nX_i$. By the additivity of the Poisson distribution, $S\sim P\left(n\lambda\right)$, so $E\left(S\right)=n\lambda$ and $D\left(S\right)=n\lambda$.

When $H_0:\lambda=\lambda_0$ holds, $S\sim P\left(n\lambda_0\right)$. By the central limit theorem, as $n\to+\infty$,

$$
\frac{S-n\lambda_0}{\sqrt{n\lambda_0}}\overset{\text{近似}}{\sim}N\left(0,1\right).
$$

Take the test statistic

$$
U=\frac{S-n\lambda_0}{\sqrt{n\lambda_0}}=\frac{\bar X-\lambda_0}{\sqrt{\lambda_0/n}}.
$$

For a given significance level $\alpha$, from the form of the rejection region for the two-sided test in **Large-sample Method** (Test for the Poisson Distribution Parameter $\lambda$), we get

$$
\alpha=P\left(\left\lvert U\right\rvert\ge u_{\alpha/2}\,\middle|\,H_0\right),
$$

so the rejection region for the testing problem $H_0:\lambda=\lambda_0,\ H_1:\lambda\ne\lambda_0$ is

$$
D=\left\{\left(x_1,x_2,\dots,x_n\right):\left\lvert\frac{\sum_{i=1}^nx_i-n\lambda_0}{\sqrt{n\lambda_0}}\right\rvert\ge u_{\alpha/2}\right\}.
$$

That is, if the sample observations satisfy $\left\lvert\frac{\bar x-\lambda_0}{\sqrt{\lambda_0/n}}\right\rvert\ge u_{\alpha/2}$, then $H_0$ is rejected at significance level $\alpha$; otherwise $H_0$ is not rejected. $\blacksquare$

### Problem 4

(Problem 5.3-6) A city randomly samples $1000$ households, and a survey finds that $450$ of them own a computer. Let $p$ denote the proportion of households in this city that own a computer. At significance level $\alpha=0.05$, test the hypotheses $H_0:p=0.5$; $H_1:p\ne0.5$.

### Solution to Problem 4

The sample size $n=1000$ is a large-sample case. By **Large-sample Method** (Test for the Binomial Distribution Parameter $p$), take the test statistic

$$
U=\frac{\bar X-p_0}{\sqrt{\frac{p_0\left(1-p_0\right)}{n}}}.
$$

From the problem, $\bar x=\frac{450}{1000}=0.45$, $p_0=0.5$. Substituting,

$$
u=\frac{0.45-0.5}{\sqrt{\frac{0.5\times0.5}{1000}}}=\frac{-0.05}{\sqrt{0.00025}}=\frac{-0.05}{0.01581}=-3.162.
$$

The rejection region for the two-sided test at $\alpha=0.05$ is $\left\lvert U\right\rvert\ge u_{0.025}=1.96$. Since $\left\lvert u\right\rvert=3.162> 1.96$, the sample falls into the rejection region, so the null hypothesis $H_0$ is rejected at significance level $\alpha=0.05$, i.e. the proportion $p$ of households owning a computer in this city is believed not to equal $0.5$. $\blacksquare$
