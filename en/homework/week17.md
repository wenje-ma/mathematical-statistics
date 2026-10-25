# Assignment 17

> **U-test** (Test for the Mean of a Single Normal Population with Known Variance)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, where $\sigma^2=\sigma_0^2$ is known and $\mu$ is unknown. For a given significance level $\alpha$, take the test statistic $$U=\frac{\bar X-\mu_0}{\sigma_0/\sqrt n},$$ and when $H_0:\mu=\mu_0$ holds, $U\sim N\left(0,1\right)$. The rejection regions for the three testing problems are respectively: for the two-sided test $H_0:\mu=\mu_0,\ H_1:\mu\ne\mu_0$, the rejection region is $\left\lvert U\right\rvert\ge u_{\alpha/2}$; for the right-tailed test $H_0:\mu\le\mu_0,\ H_1:\mu> \mu_0$, the rejection region is $U\ge u_\alpha$; for the left-tailed test $H_0:\mu\ge\mu_0,\ H_1:\mu< \mu_0$, the rejection region is $U\le-u_\alpha$.

> **t-test** (Test for the Mean of a Single Normal Population with Unknown Variance)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, where $\sigma^2$ is unknown. For a given significance level $\alpha$, take the test statistic $$T=\frac{\bar X-\mu_0}{S/\sqrt n},$$ and when $H_0:\mu=\mu_0$ holds, $T\sim t\left(n-1\right)$. The rejection region for the two-sided test is $\left\lvert T\right\rvert\ge t_{\alpha/2}\left(n-1\right)$; for the right-tailed test it is $T\ge t_\alpha\left(n-1\right)$; for the left-tailed test it is $T\le-t_\alpha\left(n-1\right)$.

> **$\chi^2$-test** (Test for the Variance of a Single Normal Population)<br>Let $X_1,X_2,\dots,X_n$ be a sample from the normal population $N\left(\mu,\sigma^2\right)$, where $\mu$ is unknown. For a given significance level $\alpha$, take the test statistic $$\chi^2=\frac{\left(n-1\right)S^2}{\sigma_0^2},$$ and when $H_0:\sigma^2=\sigma_0^2$ holds, $\chi^2\sim\chi^2\left(n-1\right)$. For the two-sided test $H_0:\sigma^2=\sigma_0^2,\ H_1:\sigma^2\ne\sigma_0^2$, the rejection region is $\chi^2\le\chi^2_{1-\alpha/2}\left(n-1\right)$ or $\chi^2\ge\chi^2_{\alpha/2}\left(n-1\right)$; for the right-tailed test $H_0:\sigma^2\le\sigma_0^2,\ H_1:\sigma^2> \sigma_0^2$, the rejection region is $\chi^2\ge\chi^2_\alpha\left(n-1\right)$; for the left-tailed test $H_0:\sigma^2\ge\sigma_0^2,\ H_1:\sigma^2< \sigma_0^2$, the rejection region is $\chi^2\le\chi^2_{1-\alpha}\left(n-1\right)$.

> **U-test for the Difference of Means of Two Normal Populations** (Both Variances Known)<br>Let $X_1,X_2,\dots,X_m$ be from $N\left(\mu_1,\sigma_1^2\right)$ and $Y_1,Y_2,\dots,Y_n$ from $N\left(\mu_2,\sigma_2^2\right)$, with the two samples independent, where $\sigma_1^2,\sigma_2^2$ are both known. Take the test statistic $$U=\frac{\bar X-\bar Y}{\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}},$$ and when $H_0:\mu_1=\mu_2$ holds, $U\sim N\left(0,1\right)$. The rejection region for the two-sided test is $\left\lvert U\right\rvert\ge u_{\alpha/2}$; for the right-tailed test $H_0:\mu_1\le\mu_2,\ H_1:\mu_1> \mu_2$, the rejection region is $U\ge u_\alpha$.

> **Pooled t-test for the Difference of Means of Two Normal Populations** (Variances Unknown but Equal)<br>Let $X_1,X_2,\dots,X_m$ be from $N\left(\mu_1,\sigma^2\right)$ and $Y_1,Y_2,\dots,Y_n$ from $N\left(\mu_2,\sigma^2\right)$, with the two samples independent, where $\sigma^2$ is unknown. Take the pooled sample variance $$S_w^2=\frac{\left(m-1\right)S_1^2+\left(n-1\right)S_2^2}{m+n-2},$$ and the test statistic is $$T=\frac{\bar X-\bar Y}{S_w\sqrt{\frac1m+\frac1n}},$$ and when $H_0:\mu_1=\mu_2$ holds, $T\sim t\left(m+n-2\right)$. The rejection region for the two-sided test is $\left\lvert T\right\rvert\ge t_{\alpha/2}\left(m+n-2\right)$; for the right-tailed test it is $T\ge t_\alpha\left(m+n-2\right)$.

> **F-test** (Test for the Variance Ratio of Two Normal Populations)<br>Let $X_1,X_2,\dots,X_m$ be from $N\left(\mu_1,\sigma_1^2\right)$ and $Y_1,Y_2,\dots,Y_n$ from $N\left(\mu_2,\sigma_2^2\right)$, with the two samples independent, where $\mu_1,\mu_2$ are unknown. Take the test statistic $$F=\frac{S_1^2}{S_2^2},$$ and when $H_0:\sigma_1^2=\sigma_2^2$ holds, $F\sim F\left(m-1,n-1\right)$. For the two-sided test $H_0:\sigma_1^2=\sigma_2^2,\ H_1:\sigma_1^2\ne\sigma_2^2$, the rejection region is $F\le F_{1-\alpha/2}\left(m-1,n-1\right)$ or $F\ge F_{\alpha/2}\left(m-1,n-1\right)$.

### Problem 1

(Problem 5.2-5) A sample of size $16$ is randomly drawn from the normal population $N\left(\mu,\sigma^2\right)$ with standard deviation $\sigma=5.2$, and computation gives the sample mean $\bar x=27.56$. At significance level $\alpha=0.05$, can the population mean be regarded as $\mu=26$?

### Solution to Problem 1

In this problem the population variance $\sigma^2=5.2^2$ is known. By **U-test** (Test for the Mean of a Single Normal Population with Known Variance), set up the hypotheses

$$
H_0:\mu=26,\quad H_1:\mu\ne26.
$$

The test statistic is $U=\frac{\bar X-\mu_0}{\sigma_0/\sqrt n}$. Substituting the data $\bar x=27.56$, $\mu_0=26$, $\sigma_0=5.2$, $n=16$, we get

$$
u=\frac{27.56-26}{5.2/\sqrt{16}}=\frac{1.56}{1.3}=1.2.
$$

At significance level $\alpha=0.05$, the rejection region for the two-sided test is $\left\lvert U\right\rvert\ge u_{0.025}=1.96$. Since $\left\lvert u\right\rvert=1.2< 1.96$, the sample does not fall into the rejection region, so the null hypothesis is not rejected at significance level $\alpha=0.05$, i.e. the population mean can be regarded as $\mu=26$. $\blacksquare$

### Problem 2

(Problem 5.2-7) The average service life of a component is required to be no less than $1000\mathrm{h}$. The producer randomly samples $25$ such components and measures their mean service life to be $950\mathrm{h}$. It is known that the service life of this kind of component follows a normal distribution with standard deviation $\sigma=100\mathrm{h}$. At significance level $\alpha=0.05$, determine whether this batch of components is qualified.

### Solution to Problem 2

The problem requires the average service life to be no less than $1000\mathrm{h}$, and the producer wishes to use the sample data to test whether the product is qualified. By **U-test** (Test for the Mean of a Single Normal Population with Known Variance), this is a left-tailed testing problem. Set up the hypotheses

$$
H_0:\mu\ge1000,\quad H_1:\mu< 1000.
$$

The test statistic is $U=\frac{\bar X-\mu_0}{\sigma_0/\sqrt n}$. Substituting the data $\bar x=950$, $\mu_0=1000$, $\sigma_0=100$, $n=25$, we get

$$
u=\frac{950-1000}{100/\sqrt{25}}=\frac{-50}{20}=-2.5.
$$

The rejection region for the left-tailed test at significance level $\alpha=0.05$ is $U\le-u_{0.05}=-1.645$. Since $u=-2.5< -1.645$, the sample falls into the rejection region, so the null hypothesis is rejected at significance level $\alpha=0.05$, i.e. the average service life of this batch is regarded as below $1000\mathrm{h}$, and this batch of components is not qualified. $\blacksquare$

### Problem 3

(Problem 5.2-9) Let $X_1,X_2,\dots,X_{25}$ be a sample from the normal population $N\left(\mu,3^2\right)$, where $\mu\in\mathbb R$ is an unknown parameter. Let the rejection region of the testing problem $H_0:\mu=\mu_0$; $H_1:\mu\ne\mu_0$ ($\mu_0$ known) be $D=\left\{\left\lvert\bar X-\mu_0\right\rvert\ge c\right\}$.

(1) At significance level $\alpha=0.05$, find the constant $c$;

(2) Find the probability of committing a Type II error when $\mu=\mu_1$ ($\ne\mu_0$) (expressed in terms of the standard normal distribution function $\Phi\left(\cdot\right)$).

### Solution to Problem 3

By **U-test** (Test for the Mean of a Single Normal Population with Known Variance), when $H_0:\mu=\mu_0$ holds, $\bar X\sim N\left(\mu_0,\frac{3^2}{25}\right)$, so

$$
\frac{\bar X-\mu_0}{3/5}\sim N\left(0,1\right).
$$

(1) From the significance level $\alpha=0.05$, we have

$$
\alpha=P\left(\left\lvert\bar X-\mu_0\right\rvert\ge c\,\middle|\,H_0\right)=P\left(\left\lvert\frac{\bar X-\mu_0}{3/5}\right\rvert\ge\frac{5c}{3}\right)=2\left[1-\Phi\left(\frac{5c}{3}\right)\right].
$$

Hence $\Phi\left(\frac{5c}{3}\right)=1-\frac{\alpha}{2}=0.975$. From the table, $\frac{5c}{3}=u_{0.025}=1.96$, so

$$
c=\frac{3}{5}\times1.96=1.176.
$$

(2) When $\mu=\mu_1$ ($\mu_1\ne\mu_0$), $\bar X\sim N\left(\mu_1,\frac{3^2}{25}\right)$. The Type II error, i.e. the probability of accepting a false null, is

$$
\beta\left(\mu_1\right)=P\left(\left\lvert\bar X-\mu_0\right\rvert< c\,\middle|\,\mu=\mu_1\right)=P\left(-c< \bar X-\mu_0< c\right).
$$

Let $\delta=\mu_1-\mu_0$. Then $\bar X-\mu_1\sim N\left(0,\frac{3^2}{25}\right)$, i.e. $\frac{\bar X-\mu_1}{3/5}\sim N\left(0,1\right)$, so

$$
\beta\left(\mu_1\right)=P\left(-c-\delta< \bar X-\mu_1< c-\delta\right)=\Phi\left(\frac{c-\delta}{3/5}\right)-\Phi\left(\frac{-c-\delta}{3/5}\right).
$$

Substituting $c=1.176$ and simplifying,

$$
\beta\left(\mu_1\right)=\Phi\left(\frac{5\left(c-\mu_1+\mu_0\right)}{3}\right)+\Phi\left(\frac{5\left(c+\mu_1-\mu_0\right)}{3}\right)-1.
$$

In particular, when $\delta=\mu_1-\mu_0$ takes $0.5,1.0,1.5$ respectively, $\beta$ is approximately $0.867,0.615,0.295$, showing that the larger $\left\lvert\mu_1-\mu_0\right\rvert$, the smaller the probability of committing a Type II error. $\blacksquare$

### Problem 4

(Problem 5.2-12) It is known that, under normal conditions, the fiber fineness of vinylon follows a normal distribution $N\left(\mu,\sigma^2\right)$ with $\sigma=0.048$. From one day's production, $5$ fibers are randomly taken, and their fineness is measured as $1.32,1.55,1.36,1.40,1.44$. At significance level $\alpha=0.05$, ask whether the standard deviation on this day is normal.

### Solution to Problem 4

In this problem the variance $\sigma^2$ is unknown, and we need to test whether the standard deviation is still $0.048$, i.e. whether the variance equals $0.048^2$. By **$\chi^2$-test** (Test for the Variance of a Single Normal Population), set up the hypotheses

$$
H_0:\sigma^2=0.048^2,\quad H_1:\sigma^2\ne0.048^2.
$$

From the sample data, compute the sample mean and sample variance:

$$
\bar x=\frac{1.32+1.55+1.36+1.40+1.44}{5}=1.414,
$$
$$
s^2=\frac{1}{5-1}\sum_{i=1}^5\left(x_i-\bar x\right)^2=0.00778.
$$

The test statistic is $\chi^2=\frac{\left(n-1\right)S^2}{\sigma_0^2}$. Substituting $n=5$, $\sigma_0=0.048$, we get

$$
\chi^2=\frac{4\times0.00778}{0.048^2}=13.507.
$$

The rejection region for the two-sided test at significance level $\alpha=0.05$ is $\chi^2\le\chi^2_{0.975}\left(4\right)=0.484$ or $\chi^2\ge\chi^2_{0.025}\left(4\right)=11.143$. Since $\chi^2=13.507> 11.143$, the sample falls into the rejection region, so the null hypothesis is rejected at significance level $\alpha=0.05$, i.e. the standard deviation on this day is regarded as abnormal. $\blacksquare$

### Problem 5

(Problem 5.2-15) The weight of an object is measured $10$ times, giving a sample mean $\bar x=10.05$ and a sample variance $s^2=0.0576$. Assume the weight of this object follows a normal distribution $N\left(\mu,\sigma^2\right)$.

(1) If $\sigma^2=0.2^2$, at significance level $\alpha=0.05$, test $H_0:\mu=10$; $H_1:\mu> 10$;

(2) If $\sigma^2$ is unknown, at significance level $\alpha=0.05$, test $H_0:\mu=10$; $H_1:\mu> 10$;

(3) At significance level $\alpha=0.05$, test $H_0:\sigma^2\ge0.25^2$; $H_1:\sigma^2< 0.25^2$.

### Solution to Problem 5

(1) Since $\sigma^2=0.2^2$ is known, by **U-test** (Test for the Mean of a Single Normal Population with Known Variance), this is a right-tailed test. The test statistic is

$$
U=\frac{\bar X-\mu_0}{\sigma_0/\sqrt n},
$$

Substituting $\bar x=10.05$, $\mu_0=10$, $\sigma_0=0.2$, $n=10$, we get

$$
u=\frac{10.05-10}{0.2/\sqrt{10}}=0.791.
$$

The rejection region for the right-tailed test at $\alpha=0.05$ is $U\ge u_{0.05}=1.645$. Since $u=0.791< 1.645$, the null hypothesis is not rejected.

(2) $\sigma^2$ is unknown; by **t-test** (Test for the Mean of a Single Normal Population with Unknown Variance), this is still a right-tailed test. The test statistic is

$$
T=\frac{\bar X-\mu_0}{S/\sqrt n},
$$

Substituting $s=\sqrt{0.0576}=0.24$, we get

$$
t=\frac{10.05-10}{0.24/\sqrt{10}}=0.659.
$$

The rejection region for the right-tailed test at $\alpha=0.05$ is $T\ge t_{0.05}\left(9\right)=1.833$. Since $t=0.659< 1.833$, the null hypothesis is not rejected.

(3) By **$\chi^2$-test** (Test for the Variance of a Single Normal Population), this is a left-tailed test. The test statistic is

$$
\chi^2=\frac{\left(n-1\right)S^2}{\sigma_0^2},
$$

where $\sigma_0^2=0.25^2=0.0625$. Substituting $n=10$, $s^2=0.0576$, we get

$$
\chi^2=\frac{9\times0.0576}{0.25^2}=8.294.
$$

The rejection region for the left-tailed test at $\alpha=0.05$ is $\chi^2\le\chi^2_{0.95}\left(9\right)=3.325$. Since $\chi^2=8.294> 3.325$, the null hypothesis is not rejected, i.e. the assertion that the variance is no less than $0.25^2$ cannot be rejected. $\blacksquare$

### Problem 6

(Problem 5.2-17) To compare the quality of two cotton varieties, A and B, assume the strengths of the cotton yarn spun from them follow normal distributions $N\left(\mu_1,\sigma_1^2\right)$ and $N\left(\mu_2,\sigma_2^2\right)$ respectively. The experimenter draws samples $X_1,X_2,\dots,X_{100}$ and $Y_1,Y_2,\dots,Y_{50}$ from these two yarns, obtaining sample means and sample variances $\bar x=5.6$, $\bar y=5.2$, $s_1^2=4$, $s_2^2=2.56$.

(1) If $\sigma_1^2=2.2^2$, $\sigma_2^2=1.8^2$, at significance level $\alpha=0.05$, test $H_0:\mu_1\le\mu_2$; $H_1:\mu_1> \mu_2$;

(2) If $\sigma_1^2=\sigma_2^2$ is unknown, at significance level $\alpha=0.05$, test $H_0:\mu_1\le\mu_2$; $H_1:\mu_1> \mu_2$.

### Solution to Problem 6

(1) Since $\sigma_1^2=2.2^2=4.84$, $\sigma_2^2=1.8^2=3.24$ are known, by **U-test for the Difference of Means of Two Normal Populations** (Both Variances Known), the test statistic is

$$
U=\frac{\bar X-\bar Y}{\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}},
$$

Substituting $\bar x=5.6$, $\bar y=5.2$, $m=100$, $n=50$, we get

$$
u=\frac{5.6-5.2}{\sqrt{\frac{4.84}{100}+\frac{3.24}{50}}}=\frac{0.4}{\sqrt{0.1132}}=1.189.
$$

The rejection region for the right-tailed test at $\alpha=0.05$ is $U\ge u_{0.05}=1.645$. Since $u=1.189< 1.645$, the null hypothesis is not rejected, i.e. the strength of variety A yarn cannot be regarded as significantly higher than that of variety B.

(2) $\sigma_1^2=\sigma_2^2$ is unknown but equal; by **Pooled t-test for the Difference of Means of Two Normal Populations** (Variances Unknown but Equal), first compute the pooled sample variance

$$
s_w^2=\frac{\left(m-1\right)s_1^2+\left(n-1\right)s_2^2}{m+n-2}=\frac{99\times4+49\times2.56}{148}=3.523,
$$

$s_w=\sqrt{3.523}=1.877$. The test statistic is

$$
T=\frac{\bar X-\bar Y}{S_w\sqrt{\frac1m+\frac1n}},
$$

Substituting the data,

$$
t=\frac{5.6-5.2}{1.877\times\sqrt{\frac1{100}+\frac1{50}}}=\frac{0.4}{1.877\times0.1732}=1.230.
$$

The rejection region for the right-tailed test at $\alpha=0.05$ is $T\ge t_{0.05}\left(148\right)\approx1.655$. Since $t=1.230< 1.655$, the null hypothesis is not rejected, i.e. the strength of variety A yarn cannot be regarded as significantly higher than that of variety B. $\blacksquare$

### Problem 7

(Problem 5.2-21) The resistance (in $\Omega$) of two batches of similar electronic components is tested, with $6$ items sampled from each batch, giving the following results:

First batch: $0.140,0.138,0.143,0.142,0.144,0.137$;

Second batch: $0.135,0.140,0.142,0.136,0.138,0.140$.

It is known that the resistances of the two batches follow normal distributions $N\left(\mu_1,\sigma_1^2\right)$ and $N\left(\mu_2,\sigma_2^2\right)$ respectively. At significance level $\alpha=0.05$, test respectively:

(1) whether the variances of the resistances of the two batches are equal;

(2) whether there is a significant difference in the mean resistance of the two batches.

### Solution to Problem 7

(1) First use **F-test** (Test for the Variance Ratio of Two Normal Populations) to test whether the variances are equal. Set up the hypotheses

$$
H_0:\sigma_1^2=\sigma_2^2,\quad H_1:\sigma_1^2\ne\sigma_2^2.
$$

From the sample data, compute the sample means and sample variances of the two batches:

$$
\bar x_1=\frac{1}{6}\sum_{i=1}^6x_{1i}=0.14067,\quad s_1^2=7.867\times10^{-6},
$$
$$
\bar x_2=\frac{1}{6}\sum_{i=1}^6x_{2i}=0.13850,\quad s_2^2=7.100\times10^{-6}.
$$

The test statistic is $F=\frac{S_1^2}{S_2^2}$. Substituting,

$$
f=\frac{7.867\times10^{-6}}{7.100\times10^{-6}}=1.108.
$$

The rejection region for the two-sided test at $\alpha=0.05$ is $F\le F_{0.975}\left(5,5\right)=0.140$ or $F\ge F_{0.025}\left(5,5\right)=7.146$. Since $0.140< f=1.108< 7.146$, the sample does not fall into the rejection region, so the null hypothesis is not rejected, i.e. the variances of the resistances of the two batches can be regarded as equal.

(2) From the conclusion of (1), the two population variances are equal but unknown; by **Pooled t-test for the Difference of Means of Two Normal Populations** (Variances Unknown but Equal), set up the hypotheses

$$
H_0:\mu_1=\mu_2,\quad H_1:\mu_1\ne\mu_2.
$$

The pooled sample variance is

$$
s_w^2=\frac{\left(6-1\right)s_1^2+\left(6-1\right)s_2^2}{6+6-2}=\frac{5\times7.867\times10^{-6}+5\times7.100\times10^{-6}}{10}=7.483\times10^{-6},
$$

$s_w=\sqrt{7.483\times10^{-6}}=0.002736$. The test statistic is

$$
T=\frac{\bar X_1-\bar X_2}{S_w\sqrt{\frac1m+\frac1n}},
$$

Substituting $m=n=6$, we get

$$
t=\frac{0.14067-0.13850}{0.002736\times\sqrt{\frac16+\frac16}}=\frac{0.00217}{0.00158}=1.372.
$$

The rejection region for the two-sided test at $\alpha=0.05$ is $\left\lvert T\right\rvert\ge t_{0.025}\left(10\right)=2.228$. Since $\left\lvert t\right\rvert=1.372< 2.228$, the null hypothesis is not rejected, i.e. there is no significant difference in the mean resistance of the two batches. $\blacksquare$
