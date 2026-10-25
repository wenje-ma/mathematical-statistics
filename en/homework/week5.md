# Assignment 5

> **Definition 2.4.1** (Exponential Family)<br>Let $\mathcal{F}=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ be a family of distributions defined on the sample space $\mathcal{X}$, where $\Theta$ is the parameter space. If $f\left(x,\theta\right)$ can be expressed as $$f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k Q_i\left(\theta\right)T_i\left(x\right)\right\}h\left(x\right),$$ then this family of distributions is called an exponential family of distributions, abbreviated as an exponential family. Here $C\left(\theta\right)> 0$ and $Q_i\left(\theta\right)$ are defined on the parameter space $\Theta$, $h\left(x\right)> 0$ and $T_i\left(x\right)$ are defined on the sample space $\mathcal{X}$, and the support set $\left\{x:f\left(x,\theta\right)> 0\right\}$ does not depend on $\theta$.

> **Definition 2.4.2** (Natural Form of the Exponential Family)<br>If an exponential family has the form $$f\left(x,\varphi\right)=C\left(\varphi\right)\exp\left\{\sum_{i=1}^k\varphi_i T_i\left(x\right)\right\}h\left(x\right),$$ then it is called the natural form of the exponential family, also called the standard form. The set $$\Theta^{*}=\left\{\varphi=\left(\varphi_1,\dots,\varphi_k\right):\int\exp\left\{\sum_{i=1}^k\varphi_i T_i\left(x\right)\right\}h\left(x\right)\,\mathrm{d}x< +\infty\right\}$$ is called the natural parameter space.

### Problem 1

(Problem 2.4-3) Let $X_1,X_2,\dots,X_n$ be a sample from the population $X$, and the density function of $X$ is

$$
f\left(x\right)=\begin{cases}\theta x^{\theta-1},&0< x< 1,\\0,&\text{其他},\end{cases}
$$

where $\theta> 0$. Prove that the sample distribution family is an exponential family, express it in the natural form of the exponential family, and find the natural parameter space.

### Solution to Problem 1

By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are mutually independent and identically distributed with the population $X$, so the joint density function of the sample is

$$
f\left(x_1,x_2,\dots,x_n,\theta\right)=\prod_{i=1}^n\theta x_i^{\theta-1}=\theta^n\left(\prod_{i=1}^n x_i\right)^{\theta-1}=\theta^n\exp\left\{\left(\theta-1\right)\sum_{i=1}^n\ln x_i\right\}.
$$

Rewriting it as

$$
f\left(x_1,\dots,x_n,\theta\right)=\theta^n\exp\left\{\theta\sum_{i=1}^n\ln x_i\right\}\cdot\frac{1}{\prod_{i=1}^n x_i},\quad 0< x_i< 1.
$$

Take $C\left(\theta\right)=\theta^n$, $Q\left(\theta\right)=\theta$, $T\left(x_1,\dots,x_n\right)=\sum_{i=1}^n\ln x_i$, and $h\left(x_1,\dots,x_n\right)=\frac{1}{\prod_{i=1}^n x_i}$. Its support set $\left\{x:f\left(x,\theta\right)> 0\right\}=\left(0,1\right)$ does not depend on $\theta$, so by **Definition 2.4.1** (Exponential Family), this sample distribution family is an exponential family.

Letting the natural parameter be $\varphi=\theta$, by **Definition 2.4.2** (Natural Form of the Exponential Family), the natural form is

$$
f\left(x_1,\dots,x_n,\varphi\right)=\varphi^n\exp\left\{\varphi\sum_{i=1}^n\ln x_i\right\}\frac{1}{\prod_{i=1}^n x_i}=C\left(\varphi\right)\exp\left\{\varphi T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

where $C\left(\varphi\right)=\varphi^n$. The natural parameter space satisfies

$$
\Theta^{*}=\left\{\varphi:\int_0^1\exp\left\{\varphi\ln x\right\}\cdot\frac{1}{x}\,\mathrm{d}x< +\infty\right\}=\left\{\varphi:\int_0^1 x^{\varphi-1}\,\mathrm{d}x< +\infty\right\}.
$$

Since $\int_0^1 x^{\varphi-1}\mathrm{d}x=\frac{1}{\varphi}$ converges if and only if $\varphi> 0$, the natural parameter space is

$$
\Theta^{*}=\left(0,+\infty\right).
$$

$\blacksquare$

### Problem 2

(Problem 2.4-4) Let $X_1,X_2,\dots,X_n$ be a sample from the Laplace distribution, whose density function is

$$
f\left(x\right)=\frac{1}{2\theta}e^{-\left|x\right|/\theta},\quad-\infty< x< +\infty,\ \theta> 0.
$$

Prove that the sample distribution family is an exponential family, express it in the natural form of the exponential family, and find the natural parameter space.

### Solution to Problem 2

By **Definition 1.3.2** (Simple Random Sample), the joint density function of the sample is

$$
f\left(x_1,\dots,x_n,\theta\right)=\prod_{i=1}^n\frac{1}{2\theta}e^{-\left|x_i\right|/\theta}=\left(2\theta\right)^{-n}\exp\left\{-\frac{1}{\theta}\sum_{i=1}^n\left|x_i\right|\right\}.
$$

Take $C\left(\theta\right)=\left(2\theta\right)^{-n}$, $Q\left(\theta\right)=-\frac{1}{\theta}$, $T\left(x_1,\dots,x_n\right)=\sum_{i=1}^n\left|x_i\right|$, and $h\left(x_1,\dots,x_n\right)=1$. Its support set is $\left(-\infty,+\infty\right)$, which does not depend on $\theta$, so by **Definition 2.4.1** (Exponential Family), this sample distribution family is an exponential family.

Letting the natural parameter be $\varphi=-\frac{1}{\theta}$, then $\theta=-\frac{1}{\varphi}$, and by **Definition 2.4.2** (Natural Form of the Exponential Family), the natural form is

$$
f\left(x_1,\dots,x_n,\varphi\right)=\left(-\frac{\varphi}{2}\right)^n\exp\left\{\varphi\sum_{i=1}^n\left|x_i\right|\right\}=C\left(\varphi\right)\exp\left\{\varphi T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

where $C\left(\varphi\right)=\left(-\frac{\varphi}{2}\right)^n$. The natural parameter space satisfies

$$
\Theta^{*}=\left\{\varphi:\int_{-\infty}^{+\infty}\exp\left\{\varphi\left|x\right|\right\}\,\mathrm{d}x< +\infty\right\}=\left\{\varphi:2\int_0^{+\infty}e^{\varphi x}\,\mathrm{d}x< +\infty\right\}.
$$

Since $\int_0^{+\infty}e^{\varphi x}\mathrm{d}x=\frac{1}{-\varphi}$ converges if and only if $\varphi< 0$, the natural parameter space is

$$
\Theta^{*}=\left(-\infty,0\right).
$$

$\blacksquare$

### Problem 3

(Problem 2.4-5) Let $X_1,X_2,\dots,X_n$ be a sample from the Rayleigh distribution, whose density function is

$$
f\left(x\right)=\begin{cases}2\theta x e^{-\theta x^2},&x> 0,\\0,&\text{其他},\end{cases}
$$

where $\theta> 0$. Prove that the sample distribution family is an exponential family, express it in the natural form of the exponential family, and find the natural parameter space.

### Solution to Problem 3

By **Definition 1.3.2** (Simple Random Sample), the joint density function of the sample is

$$
f\left(x_1,\dots,x_n,\theta\right)=\prod_{i=1}^n 2\theta x_i e^{-\theta x_i^2}=\left(2\theta\right)^n\left(\prod_{i=1}^n x_i\right)\exp\left\{-\theta\sum_{i=1}^n x_i^2\right\}.
$$

Take $C\left(\theta\right)=\left(2\theta\right)^n$, $Q\left(\theta\right)=-\theta$, $T\left(x_1,\dots,x_n\right)=\sum_{i=1}^n x_i^2$, and $h\left(x_1,\dots,x_n\right)=\prod_{i=1}^n x_i$. Its support set is $\left(0,+\infty\right)$, which does not depend on $\theta$, so by **Definition 2.4.1** (Exponential Family), this sample distribution family is an exponential family.

Letting the natural parameter be $\varphi=-\theta$, then $\theta=-\varphi$, and by **Definition 2.4.2** (Natural Form of the Exponential Family), the natural form is

$$
f\left(x_1,\dots,x_n,\varphi\right)=\left(-2\varphi\right)^n\exp\left\{\varphi\sum_{i=1}^n x_i^2\right\}\prod_{i=1}^n x_i=C\left(\varphi\right)\exp\left\{\varphi T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

where $C\left(\varphi\right)=\left(-2\varphi\right)^n$. The natural parameter space satisfies

$$
\Theta^{*}=\left\{\varphi:\int_0^{+\infty}\exp\left\{\varphi x^2\right\}x\,\mathrm{d}x< +\infty\right\}.
$$

Letting $u=x^2$, then $\mathrm{d}u=2x\,\mathrm{d}x$, and the integral becomes $\frac{1}{2}\int_0^{+\infty}e^{\varphi u}\mathrm{d}u=\frac{1}{2\left(-\varphi\right)}$, which converges if and only if $\varphi< 0$, so the natural parameter space is

$$
\Theta^{*}=\left(-\infty,0\right).
$$

$\blacksquare$

### Problem 4

(Problem 2.4-6) Let $X_1,X_2,\dots,X_n$ be a sample from the exponential distribution $E\left(\lambda\right)$, whose density function is

$$
f\left(x\right)=\begin{cases}\lambda e^{-\lambda x},&x> 0,\\0,&\text{其他},\end{cases}
$$

where $\lambda> 0$. Prove that the sample distribution family is an exponential family, express it in the natural form of the exponential family, and find the natural parameter space.

### Solution to Problem 4

By **Definition 1.3.2** (Simple Random Sample), the joint density function of the sample is

$$
f\left(x_1,\dots,x_n,\lambda\right)=\prod_{i=1}^n\lambda e^{-\lambda x_i}=\lambda^n\exp\left\{-\lambda\sum_{i=1}^n x_i\right\}.
$$

Take $C\left(\lambda\right)=\lambda^n$, $Q\left(\lambda\right)=-\lambda$, $T\left(x_1,\dots,x_n\right)=\sum_{i=1}^n x_i$, and $h\left(x_1,\dots,x_n\right)=1$. Its support set is $\left(0,+\infty\right)$, which does not depend on $\lambda$, so by **Definition 2.4.1** (Exponential Family), this sample distribution family is an exponential family.

Letting the natural parameter be $\varphi=-\lambda$, then $\lambda=-\varphi$, and by **Definition 2.4.2** (Natural Form of the Exponential Family), the natural form is

$$
f\left(x_1,\dots,x_n,\varphi\right)=\left(-\varphi\right)^n\exp\left\{\varphi\sum_{i=1}^n x_i\right\}=C\left(\varphi\right)\exp\left\{\varphi T\left(x_1,\dots,x_n\right)\right\}h\left(x_1,\dots,x_n\right),
$$

where $C\left(\varphi\right)=\left(-\varphi\right)^n$. The natural parameter space satisfies

$$
\Theta^{*}=\left\{\varphi:\int_0^{+\infty}e^{\varphi x}\,\mathrm{d}x< +\infty\right\}.
$$

Since $\int_0^{+\infty}e^{\varphi x}\mathrm{d}x=\frac{1}{-\varphi}$ converges if and only if $\varphi< 0$, the natural parameter space is

$$
\Theta^{*}=\left(-\infty,0\right).
$$

$\blacksquare$

### Problem 5

(Problem 2.4-7) Let $X_1,X_2,\dots,X_n$ be a sample from the lognormal distribution, whose density function is

$$
f\left(x,\mu,\sigma^2\right)=\begin{cases}\frac{1}{\sqrt{2\pi}\sigma x}\exp\left\{-\frac{\left(\ln x-\mu\right)^2}{2\sigma^2}\right\},&x> 0,\\0,&\text{其他},\end{cases}
$$

where $\mu\in\mathbb R,\ \sigma> 0$. Prove that the sample distribution family is an exponential family, express it in the natural form of the exponential family, and find the natural parameter space.

### Solution to Problem 5

By **Definition 1.3.2** (Simple Random Sample), the joint density function of the sample is

$$
f\left(x_1,\dots,x_n,\mu,\sigma^2\right)=\left(2\pi\sigma^2\right)^{-n/2}\left(\prod_{i=1}^n x_i\right)^{-1}\exp\left\{-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(\ln x_i-\mu\right)^2\right\}.
$$

Expanding the squared term: $\sum_{i=1}^n\left(\ln x_i-\mu\right)^2=\sum_{i=1}^n\left(\ln x_i\right)^2-2\mu\sum_{i=1}^n\ln x_i+n\mu^2$, and substituting gives

$$
f=\left(2\pi\sigma^2\right)^{-n/2}\sigma^{-n}\exp\left\{-\frac{n\mu^2}{2\sigma^2}\right\}\exp\left\{\frac{\mu}{\sigma^2}\sum_{i=1}^n\ln x_i-\frac{1}{2\sigma^2}\sum_{i=1}^n\left(\ln x_i\right)^2\right\}\cdot\left(\prod_{i=1}^n x_i\right)^{-1}.
$$

Take $C\left(\mu,\sigma^2\right)=\left(2\pi\right)^{-n/2}\sigma^{-n}\exp\left\{-\frac{n\mu^2}{2\sigma^2}\right\}$, $Q_1\left(\mu,\sigma^2\right)=\frac{\mu}{\sigma^2}$, $T_1=\sum_{i=1}^n\ln x_i$, $Q_2\left(\mu,\sigma^2\right)=-\frac{1}{2\sigma^2}$, $T_2=\sum_{i=1}^n\left(\ln x_i\right)^2$, and $h=\left(\prod_{i=1}^n x_i\right)^{-1}$. Its support set is $\left(0,+\infty\right)$, which does not depend on the parameters, so by **Definition 2.4.1** (Exponential Family), this sample distribution family is an exponential family.

Letting the natural parameters be $\varphi_1=\frac{\mu}{\sigma^2}$ and $\varphi_2=-\frac{1}{2\sigma^2}$, by **Definition 2.4.2** (Natural Form of the Exponential Family), the natural form is

$$
f\left(x_1,\dots,x_n,\varphi_1,\varphi_2\right)=\left(-\frac{\varphi_2}{\pi}\right)^{n/2}\exp\left\{\frac{n\varphi_1^2}{4\varphi_2}\right\}\exp\left\{\varphi_1\sum_{i=1}^n\ln x_i+\varphi_2\sum_{i=1}^n\left(\ln x_i\right)^2\right\}\left(\prod_{i=1}^n x_i\right)^{-1}.
$$

The natural parameter space satisfies

$$
\Theta^{*}=\left\{\left(\varphi_1,\varphi_2\right):\int_0^{+\infty}\exp\left\{\varphi_1\ln x+\varphi_2\left(\ln x\right)^2\right\}\frac{1}{x}\,\mathrm{d}x< +\infty\right\}.
$$

Letting $u=\ln x$, then $\mathrm{d}u=\frac{\mathrm{d}x}{x}$, and the integral becomes

$$
\int_{-\infty}^{+\infty}\exp\left\{\varphi_1 u+\varphi_2 u^2\right\}\,\mathrm{d}u=\sqrt{\frac{\pi}{-\varphi_2}}\exp\left\{-\frac{\varphi_1^2}{4\varphi_2}\right\},
$$

which converges if and only if $\varphi_2< 0$ (in which case it converges for any $\varphi_1$), so the natural parameter space is

$$
\Theta^{*}=\left\{\left(\varphi_1,\varphi_2\right):-\infty< \varphi_1< +\infty,\ \varphi_2< 0\right\}.
$$

$\blacksquare$
