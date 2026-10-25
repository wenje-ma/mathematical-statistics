# Assignment 3

> **Definition 2.2.1** ($\chi^2$ Distribution)<br>Let $X_1,X_2,\dots,X_n$ be mutually independent and all follow $N\left(0,1\right)$. Then $$\chi^2=X_1^2+X_2^2+\dots+X_n^2$$ is called a $\chi^2$ variable with $n$ degrees of freedom, its distribution is called the $\chi^2$ distribution with $n$ degrees of freedom, denoted by $\chi^2\sim\chi^2\left(n\right)$.

> **Theorem 2.2.1** (Density Function of the $\chi^2$ Distribution)<br>Let $\chi^2\sim\chi^2\left(n\right)$. Then its density function is $$f\left(x\right)=\begin{cases}\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2},&x> 0,\\0,&x\le0.\end{cases}$$

> **Properties of the $\chi^2$ Distribution**<br>Let $\chi^2\sim\chi^2\left(n\right)$. Then $E\left(\chi^2\right)=n$ and $D\left(\chi^2\right)=2n$. If $X_1\sim\chi^2\left(n_1\right)$, $X_2\sim\chi^2\left(n_2\right)$, and $X_1$ and $X_2$ are mutually independent, then $X_1+X_2\sim\chi^2\left(n_1+n_2\right)$; this property is called the additivity of the $\chi^2$ distribution.

> **Definition 2.2.2** ($t$ Distribution)<br>Let the random variables $X\sim N\left(0,1\right)$ and $Y\sim\chi^2\left(n\right)$, with $X$ and $Y$ mutually independent. Then the random variable $$T=\frac{X}{\sqrt{Y/n}}$$ is called a $t$ variable with $n$ degrees of freedom, its distribution is called the $t$ distribution with $n$ degrees of freedom, denoted by $T\sim t\left(n\right)$.

> **Theorem 2.2.2** (Density Function of the $t$ Distribution)<br>Let $T\sim t\left(n\right)$. Then its density function is $$f\left(t\right)=\frac{\Gamma\left(\left(n+1\right)/2\right)}{\Gamma\left(n/2\right)\sqrt{n\pi}}\left(1+\frac{t^2}{n}\right)^{-\left(n+1\right)/2},\quad-\infty< t< +\infty.$$

> **Definition 2.2.3** ($F$ Distribution)<br>Let the random variables $X\sim\chi^2\left(m\right)$ and $Y\sim\chi^2\left(n\right)$, with $X$ and $Y$ mutually independent. Then the random variable $$F=\frac{X/m}{Y/n}$$ is called an $F$ variable with degrees of freedom $m$ and $n$, and the distribution it follows is called the $F$ distribution, denoted by $F\sim F\left(m,n\right)$.

> **Corollary 2.2.1** (Independence of $X/Y$ and $X+Y$)<br>Let the random variables $X\sim\chi^2\left(m\right)$ and $Y\sim\chi^2\left(n\right)$, with $X$ and $Y$ mutually independent. Then $U=X/Y$ and $V=X+Y$ are mutually independent.

> **Gamma Distribution**<br>If the density function of the random variable $X$ is $$f\left(x\right)=\begin{cases}\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}x^{\alpha-1}e^{-\lambda x},&x> 0,\\0,&x\le0,\end{cases}$$ where $\alpha> 0$ is the shape parameter and $\lambda> 0$ is the scale parameter, then $X$ is said to follow the Gamma distribution with parameters $\left(\alpha,\lambda\right)$, denoted by $X\sim Ga\left(\alpha,\lambda\right)$. When $\alpha=1$, $Ga\left(1,\lambda\right)$ is the exponential distribution; when $\alpha=n/2$ and $\lambda=1/2$, $Ga\left(n/2,1/2\right)$ is the $\chi^2\left(n\right)$ distribution.

### Problem 1

(Problem 2.2-1) Let $X_1,X_2,X_3,X_4,X_5$ be a sample from the population $X$, with $X\sim N\left(0,1\right)$.

(1) Determine $a$ and $b$ such that $a\left(X_1-2X_2+3X_3\right)^2+b\left(4X_4-5X_5\right)^2$ follows a $\chi^2$ distribution, and state the degrees of freedom;

(2) Determine $c$ such that $c\frac{\sum_{i=1}^3 X_i}{\sqrt{\sum_{i=4}^5 X_i^2}}$ follows a $t$ distribution, and state the degrees of freedom;

(3) Determine $d$ such that $d\frac{\sum_{i=1}^3 X_i^2}{\sum_{i=4}^5 X_i^2}$ follows an $F$ distribution, and state the degrees of freedom.

### Solution to Problem 1

By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_5$ are mutually independent and all follow $N\left(0,1\right)$.

(1) By **Basic Knowledge** (Additivity of the Normal Distribution), $X_1-2X_2+3X_3$ is a linear combination of independent normal variables, so

$$
X_1-2X_2+3X_3\sim N\left(0,1+4+9\right)=N\left(0,14\right),
$$

standardizing gives $\left(X_1-2X_2+3X_3\right)/\sqrt{14}\sim N\left(0,1\right)$, and by **Definition 2.2.1** ($\chi^2$ Distribution),

$$
\frac{\left(X_1-2X_2+3X_3\right)^2}{14}\sim\chi^2\left(1\right).
$$

Similarly, $4X_4-5X_5\sim N\left(0,16+25\right)=N\left(0,41\right)$, so

$$
\frac{\left(4X_4-5X_5\right)^2}{41}\sim\chi^2\left(1\right).
$$

The samples $X_1,X_2,X_3$ and $X_4,X_5$ on which the two terms depend do not overlap, so the two are mutually independent. By **Properties of the $\chi^2$ Distribution** (Additivity),

$$
\frac{\left(X_1-2X_2+3X_3\right)^2}{14}+\frac{\left(4X_4-5X_5\right)^2}{41}\sim\chi^2\left(2\right).
$$

Therefore $a=\frac{1}{14}$ and $b=\frac{1}{41}$, with $2$ degrees of freedom.

(2) By the additivity of the normal distribution, $\sum_{i=1}^3 X_i\sim N\left(0,3\right)$, so $\left(\sum_{i=1}^3 X_i\right)/\sqrt{3}\sim N\left(0,1\right)$. By **Definition 2.2.1**, $\sum_{i=4}^5 X_i^2\sim\chi^2\left(2\right)$, and the two are mutually independent. By **Definition 2.2.2** ($t$ Distribution),

$$
T=\frac{\left(\sum_{i=1}^3 X_i\right)/\sqrt{3}}{\sqrt{\left(\sum_{i=4}^5 X_i^2\right)/2}}=\sqrt{\frac{2}{3}}\cdot\frac{\sum_{i=1}^3 X_i}{\sqrt{\sum_{i=4}^5 X_i^2}}\sim t\left(2\right).
$$

Therefore $c=\sqrt{\frac{2}{3}}$, with $2$ degrees of freedom.

(3) By **Definition 2.2.1**, $\sum_{i=1}^3 X_i^2\sim\chi^2\left(3\right)$ and $\sum_{i=4}^5 X_i^2\sim\chi^2\left(2\right)$, and the two are mutually independent. By **Definition 2.2.3** ($F$ Distribution),

$$
F=\frac{\left(\sum_{i=1}^3 X_i^2\right)/3}{\left(\sum_{i=4}^5 X_i^2\right)/2}=\frac{2}{3}\cdot\frac{\sum_{i=1}^3 X_i^2}{\sum_{i=4}^5 X_i^2}\sim F\left(3,2\right).
$$

Therefore $d=\frac{2}{3}$, with $\left(3,2\right)$ degrees of freedom. $\blacksquare$

### Problem 2

(Problem 2.2-2) Let the random variable $X$ follow the $\chi^2$ distribution with $n$ degrees of freedom. Prove:

$$
E\left(X^k\right)=\frac{2^k\Gamma\left(n/2+k\right)}{\Gamma\left(n/2\right)},\quad k=1,2,\dots
$$

In particular, $E\left(X\right)=n$ and $D\left(X\right)=2n$.

### Solution to Problem 2

By **Theorem 2.2.1** (Density Function of the $\chi^2$ Distribution), the density function of $X\sim\chi^2\left(n\right)$ is

$$
f\left(x\right)=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2},\quad x> 0.
$$

Hence

$$
E\left(X^k\right)=\int_0^{+\infty}x^k\cdot\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2}\,\mathrm{d}x.
$$

Letting $u=x/2$, then $x=2u$ and $\mathrm{d}x=2\,\mathrm{d}u$, substituting gives

$$
E\left(X^k\right)=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}\int_0^{+\infty}\left(2u\right)^{n/2+k-1}e^{-u}\cdot2\,\mathrm{d}u=\frac{2^k}{\Gamma\left(n/2\right)}\int_0^{+\infty}u^{n/2+k-1}e^{-u}\,\mathrm{d}u.
$$

By the definition of the Gamma function $\Gamma\left(s\right)=\int_0^{+\infty}u^{s-1}e^{-u}\,\mathrm{d}u$, we obtain

$$
E\left(X^k\right)=\frac{2^k\Gamma\left(n/2+k\right)}{\Gamma\left(n/2\right)}.
$$

In particular, when $k=1$, using $\Gamma\left(s+1\right)=s\Gamma\left(s\right)$,

$$
E\left(X\right)=\frac{2\Gamma\left(n/2+1\right)}{\Gamma\left(n/2\right)}=\frac{2\cdot\frac{n}{2}\Gamma\left(n/2\right)}{\Gamma\left(n/2\right)}=n.
$$

When $k=2$,

$$
E\left(X^2\right)=\frac{4\Gamma\left(n/2+2\right)}{\Gamma\left(n/2\right)}=\frac{4\cdot\frac{n}{2}\cdot\left(\frac{n}{2}+1\right)\Gamma\left(n/2\right)}{\Gamma\left(n/2\right)}=n\left(n+2\right).
$$

Therefore

$$
D\left(X\right)=E\left(X^2\right)-\left[E\left(X\right)\right]^2=n\left(n+2\right)-n^2=2n.
$$

$\blacksquare$

### Problem 3

(Problem 2.2-3) Let the distribution function $F\left(x\right)$ of a certain continuous population $X$ be a continuous, strictly increasing function, and let $X_1,X_2,\dots,X_n$ be a sample from the population $X$. Prove:

(1) $Y=F\left(X\right)\sim U\left(0,1\right)$;

(2) $U=-2\sum_{i=1}^n\ln Y_i\sim\chi^2\left(2n\right)$.

### Solution to Problem 3

(1) Since $F\left(x\right)$ is continuous and strictly increasing, its inverse function $F^{-1}$ exists. For any $0\le y\le1$,

$$
P\left\{Y\le y\right\}=P\left\{F\left(X\right)\le y\right\}=P\left\{X\le F^{-1}\left(y\right)\right\}=F\left(F^{-1}\left(y\right)\right)=y.
$$

When $y< 0$, $P\left\{Y\le y\right\}=0$; when $y> 1$, $P\left\{Y\le y\right\}=1$. Hence $Y=F\left(X\right)\sim U\left(0,1\right)$.

(2) By **Definition 1.3.2** (Simple Random Sample), $X_1,X_2,\dots,X_n$ are mutually independent and identically distributed with the population $X$, so by (1), $Y_i=F\left(X_i\right)\sim U\left(0,1\right)$, and $Y_1,Y_2,\dots,Y_n$ are mutually independent.

Let $Z_i=-2\ln Y_i$. For $z> 0$,

$$
P\left\{Z_i\le z\right\}=P\left\{-2\ln Y_i\le z\right\}=P\left\{\ln Y_i\ge-\frac{z}{2}\right\}=P\left\{Y_i\ge e^{-z/2}\right\}=1-e^{-z/2}.
$$

This is precisely the distribution function of the $\chi^2$ distribution with $2$ degrees of freedom (by **Gamma Distribution**, $\chi^2\left(2\right)=Ga\left(1,1/2\right)$ is the exponential distribution with parameter $1/2$), so $Z_i\sim\chi^2\left(2\right)$. Since $Y_i$ are mutually independent, $Z_i$ are mutually independent, and by **Properties of the $\chi^2$ Distribution** (Additivity),

$$
U=\sum_{i=1}^n Z_i=-2\sum_{i=1}^n\ln Y_i\sim\chi^2\left(2n\right).
$$

$\blacksquare$

### Problem 4

(Problem 2.2-6) Let the random variable $X$ follow the Gamma distribution $Ga\left(\alpha,\lambda\right)$ with parameters $\alpha$ and $\lambda$, $\alpha> 0$, $\lambda> 0$. Prove:

(1) the characteristic function of $X$ is $\varphi\left(t\right)=\left(1-\frac{it}{\lambda}\right)^{-\alpha}$;

(2) $E\left(X^k\right)=\frac{\Gamma\left(\alpha+k\right)}{\Gamma\left(\alpha\right)\lambda^k}$; in particular, $E\left(X\right)=\frac{\alpha}{\lambda}$ and $D\left(X\right)=\frac{\alpha}{\lambda^2}$;

(3) if $X_i\sim Ga\left(\alpha_i,\lambda\right)$, $i=1,2,\dots,n$, and $X_1,X_2,\dots,X_n$ are mutually independent, then $\sum_{i=1}^n X_i\sim Ga\left(\alpha_1+\alpha_2+\dots+\alpha_n,\lambda\right)$;

(4) if we take $\alpha=n/2$ and $\lambda=1/2$, then $Ga\left(n/2,1/2\right)$ is the $\chi^2\left(n\right)$ distribution;

(5) if we take $\alpha=1$, then $Ga\left(1,\lambda\right)$ is the exponential distribution.

### Solution to Problem 4

By **Gamma Distribution**, the density function of $X\sim Ga\left(\alpha,\lambda\right)$ is

$$
f\left(x\right)=\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}x^{\alpha-1}e^{-\lambda x},\quad x> 0.
$$

(1) The characteristic function is

$$
\varphi\left(t\right)=E\left(e^{itX}\right)=\int_0^{+\infty}e^{itx}\cdot\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}x^{\alpha-1}e^{-\lambda x}\,\mathrm{d}x=\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}\int_0^{+\infty}x^{\alpha-1}e^{-\left(\lambda-it\right)x}\,\mathrm{d}x.
$$

By the definition of the Gamma function, $\int_0^{+\infty}x^{\alpha-1}e^{-sx}\,\mathrm{d}x=\Gamma\left(\alpha\right)/s^\alpha$ ($\mathrm{Re}\left(s\right)> 0$), so

$$
\varphi\left(t\right)=\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}\cdot\frac{\Gamma\left(\alpha\right)}{\left(\lambda-it\right)^\alpha}=\left(\frac{\lambda}{\lambda-it}\right)^\alpha=\left(1-\frac{it}{\lambda}\right)^{-\alpha}.
$$

(2) The $k$-th raw moment is

$$
E\left(X^k\right)=\int_0^{+\infty}x^k\cdot\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}x^{\alpha-1}e^{-\lambda x}\,\mathrm{d}x=\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}\int_0^{+\infty}x^{\alpha+k-1}e^{-\lambda x}\,\mathrm{d}x=\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}\cdot\frac{\Gamma\left(\alpha+k\right)}{\lambda^{\alpha+k}}=\frac{\Gamma\left(\alpha+k\right)}{\Gamma\left(\alpha\right)\lambda^k}.
$$

In particular, $E\left(X\right)=\frac{\Gamma\left(\alpha+1\right)}{\Gamma\left(\alpha\right)\lambda}=\frac{\alpha}{\lambda}$ and $E\left(X^2\right)=\frac{\Gamma\left(\alpha+2\right)}{\Gamma\left(\alpha\right)\lambda^2}=\frac{\alpha\left(\alpha+1\right)}{\lambda^2}$, so

$$
D\left(X\right)=E\left(X^2\right)-\left[E\left(X\right)\right]^2=\frac{\alpha\left(\alpha+1\right)}{\lambda^2}-\frac{\alpha^2}{\lambda^2}=\frac{\alpha}{\lambda^2}.
$$

(3) Since $X_i$ are mutually independent, the characteristic function of $\sum_{i=1}^n X_i$ is the product of the individual characteristic functions:

$$
\varphi_{\sum X_i}\left(t\right)=\prod_{i=1}^n\left(1-\frac{it}{\lambda}\right)^{-\alpha_i}=\left(1-\frac{it}{\lambda}\right)^{-\sum_{i=1}^n\alpha_i}.
$$

Since the characteristic function and the distribution uniquely determine each other, $\sum_{i=1}^n X_i\sim Ga\left(\alpha_1+\alpha_2+\dots+\alpha_n,\lambda\right)$.

(4) When $\alpha=n/2$ and $\lambda=1/2$, the density function is

$$
f\left(x\right)=\frac{\left(1/2\right)^{n/2}}{\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2}=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2},
$$

which agrees with **Theorem 2.2.1** (Density Function of the $\chi^2$ Distribution), so $Ga\left(n/2,1/2\right)$ is the $\chi^2\left(n\right)$ distribution.

(5) When $\alpha=1$, $\Gamma\left(1\right)=1$, and the density function is

$$
f\left(x\right)=\lambda e^{-\lambda x},\quad x> 0,
$$

namely the exponential distribution with parameter $\lambda$. $\blacksquare$

### Problem 5

(Problem 2.2-7) Let the random variables $X\sim\chi^2\left(m\right)$ and $Y\sim\chi^2\left(n\right)$, with $X$ and $Y$ mutually independent. Prove that $U=X/Y$ and $V=X+Y$ are mutually independent.

### Solution to Problem 5

By **Theorem 2.2.1** (Density Function of the $\chi^2$ Distribution) and the mutual independence of $X$ and $Y$, the joint density function of $\left(X,Y\right)$ is

$$
f\left(x,y\right)=\frac{1}{2^{\left(m+n\right)/2}\Gamma\left(m/2\right)\Gamma\left(n/2\right)}x^{m/2-1}y^{n/2-1}e^{-\left(x+y\right)/2},\quad x> 0,\ y> 0.
$$

Make the transformation $u=x/y$, $v=x+y$, namely $x=\frac{uv}{1+u}$ and $y=\frac{v}{1+u}$. The Jacobian determinant of this transformation is

$$
J=\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}=\begin{vmatrix}\frac{v}{\left(1+u\right)^2}&\frac{u}{1+u}\\-\frac{v}{\left(1+u\right)^2}&\frac{1}{1+u}\end{vmatrix}=\frac{v}{\left(1+u\right)^2}.
$$

Hence the joint density function of $\left(U,V\right)$ is

$$
g\left(u,v\right)=f\left(\frac{uv}{1+u},\frac{v}{1+u}\right)\left|J\right|.
$$

Substituting gives

$$
g\left(u,v\right)=\frac{1}{2^{\left(m+n\right)/2}\Gamma\left(m/2\right)\Gamma\left(n/2\right)}\left(\frac{uv}{1+u}\right)^{m/2-1}\left(\frac{v}{1+u}\right)^{n/2-1}e^{-v/2}\cdot\frac{v}{\left(1+u\right)^2}.
$$

After rearrangement, the variables $u$ and $v$ separate as

$$
g\left(u,v\right)=\underbrace{\frac{\Gamma\left(\left(m+n\right)/2\right)}{\Gamma\left(m/2\right)\Gamma\left(n/2\right)}u^{m/2-1}\left(1+u\right)^{-\left(m+n\right)/2}}_{g_U\left(u\right)}\cdot\underbrace{\frac{1}{2^{\left(m+n\right)/2}\Gamma\left(\left(m+n\right)/2\right)}v^{\left(m+n\right)/2-1}e^{-v/2}}_{g_V\left(v\right)}.
$$

Here $g_V\left(v\right)$ is exactly the density function of the $\chi^2\left(m+n\right)$ distribution (by the additivity in **Properties of the $\chi^2$ Distribution**, $X+Y\sim\chi^2\left(m+n\right)$), while $g_U\left(u\right)$ depends only on $u$. Since $g\left(u,v\right)=g_U\left(u\right)g_V\left(v\right)$, $U=X/Y$ and $V=X+Y$ are mutually independent. This is exactly **Corollary 2.2.1**. $\blacksquare$

### Problem 6

(Problem 2.2-8) Let $f_n\left(x\right)$ denote the density function of a $t$ variable with $n$ degrees of freedom. Prove:

$$
\lim_{n\to+\infty}f_n\left(x\right)=\frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}.
$$

### Solution to Problem 6

By **Theorem 2.2.2** (Density Function of the $t$ Distribution),

$$
f_n\left(x\right)=\frac{\Gamma\left(\left(n+1\right)/2\right)}{\Gamma\left(n/2\right)\sqrt{n\pi}}\left(1+\frac{x^2}{n}\right)^{-\left(n+1\right)/2}.
$$

Using Stirling's formula $\Gamma\left(s+1\right)\sim\sqrt{2\pi s}\left(s/e\right)^s$ gives the asymptotic relation

$$
\frac{\Gamma\left(n/2+1/2\right)}{\Gamma\left(n/2\right)}\sim\left(\frac{n}{2}\right)^{1/2}=\sqrt{\frac{n}{2}},\quad n\to+\infty.
$$

Therefore

$$
\frac{\Gamma\left(\left(n+1\right)/2\right)}{\Gamma\left(n/2\right)\sqrt{n\pi}}\sim\frac{\sqrt{n/2}}{\sqrt{n\pi}}=\frac{1}{\sqrt{2\pi}}.
$$

On the other hand,

$$
\left(1+\frac{x^2}{n}\right)^{-\left(n+1\right)/2}=\left[\left(1+\frac{x^2}{n}\right)^n\right]^{-\frac{n+1}{2n}}\longrightarrow\left(e^{x^2}\right)^{-1/2}=e^{-x^2/2}.
$$

Multiplying the two gives

$$
\lim_{n\to+\infty}f_n\left(x\right)=\frac{1}{\sqrt{2\pi}}e^{-x^2/2}.
$$

That is, as $n\to+\infty$, the density function of the $t\left(n\right)$ distribution converges to the density function of the standard normal distribution $N\left(0,1\right)$.

$\blacksquare$

### Problem 7

(Problem 2.2-10) Let the random variable $X\sim F\left(1,1\right)$. Find $P\left\{X< 1\right\}$.

### Solution to Problem 7

By **Definition 2.2.3** ($F$ Distribution), $X\sim F\left(1,1\right)$ means there exist mutually independent $Y_1\sim\chi^2\left(1\right)$ and $Y_2\sim\chi^2\left(1\right)$ such that

$$
X=\frac{Y_1/1}{Y_2/1}=\frac{Y_1}{Y_2}.
$$

By **Definition 2.2.1** ($\chi^2$ Distribution), $Y_1=Z_1^2$ and $Y_2=Z_2^2$, where $Z_1,Z_2$ are mutually independent and both follow $N\left(0,1\right)$. Hence

$$
X=\frac{Z_1^2}{Z_2^2}=\left(\frac{Z_1}{Z_2}\right)^2.
$$

Since $Z_1,Z_2$ are independent and identically distributed as $N\left(0,1\right)$, they are symmetric about the origin and play completely symmetric roles. By **Properties of the $F$ Distribution**, if $X\sim F\left(1,1\right)$, then $1/X\sim F\left(1,1\right)$, i.e. $X$ and $1/X$ are identically distributed. Therefore

$$
P\left\{X< 1\right\}=P\left\{\frac{1}{X}> 1\right\}=P\left\{X> 1\right\}.
$$

Also, $P\left\{X=1\right\}=0$ (a continuous distribution), so

$$
P\left\{X< 1\right\}+P\left\{X> 1\right\}=1,
$$

and hence $P\left\{X< 1\right\}=\frac{1}{2}$. $\blacksquare$
