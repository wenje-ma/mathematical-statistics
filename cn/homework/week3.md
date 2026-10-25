# 作业 3

> **定义 2.2.1**（$\chi^2$ 分布）<br>设 $X_1,X_2,\dots,X_n$ 相互独立且都服从 $N\left(0,1\right)$，则称 $$\chi^2=X_1^2+X_2^2+\dots+X_n^2$$ 为自由度为 $n$ 的 $\chi^2$ 变量，其分布称为自由度为 $n$ 的 $\chi^2$ 分布，记作 $\chi^2\sim\chi^2\left(n\right)$.

> **定理 2.2.1**（$\chi^2$ 分布的密度函数）<br>设 $\chi^2\sim\chi^2\left(n\right)$，则其密度函数为 $$f\left(x\right)=\begin{cases}\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2},&x> 0,\\0,&x\le0.\end{cases}$$

> **$\chi^2$ 分布的性质**<br>设 $\chi^2\sim\chi^2\left(n\right)$，则 $E\left(\chi^2\right)=n$，$D\left(\chi^2\right)=2n$. 若 $X_1\sim\chi^2\left(n_1\right)$，$X_2\sim\chi^2\left(n_2\right)$，且 $X_1$ 与 $X_2$ 相互独立，则 $X_1+X_2\sim\chi^2\left(n_1+n_2\right)$，该性质称为 $\chi^2$ 分布的可加性.

> **定义 2.2.2**（$t$ 分布）<br>设随机变量 $X\sim N\left(0,1\right)$，$Y\sim\chi^2\left(n\right)$，且 $X$ 与 $Y$ 相互独立，则称随机变量 $$T=\frac{X}{\sqrt{Y/n}}$$ 为自由度为 $n$ 的 $t$ 变量，其分布称为自由度为 $n$ 的 $t$ 分布，记作 $T\sim t\left(n\right)$.

> **定理 2.2.2**（$t$ 分布的密度函数）<br>设 $T\sim t\left(n\right)$，则其密度函数为 $$f\left(t\right)=\frac{\Gamma\left(\left(n+1\right)/2\right)}{\Gamma\left(n/2\right)\sqrt{n\pi}}\left(1+\frac{t^2}{n}\right)^{-\left(n+1\right)/2},\quad-\infty< t< +\infty.$$

> **定义 2.2.3**（$F$ 分布）<br>设随机变量 $X\sim\chi^2\left(m\right)$，$Y\sim\chi^2\left(n\right)$，且 $X$ 与 $Y$ 相互独立，则称随机变量 $$F=\frac{X/m}{Y/n}$$ 为自由度为 $m$ 和 $n$ 的 $F$ 变量，其所服从的分布称为 $F$ 分布，记作 $F\sim F\left(m,n\right)$.

> **推论 2.2.1**（$X/Y$ 与 $X+Y$ 的独立性）<br>设随机变量 $X\sim\chi^2\left(m\right)$，$Y\sim\chi^2\left(n\right)$，且 $X$ 与 $Y$ 相互独立，则 $U=X/Y$ 与 $V=X+Y$ 相互独立.

> **伽马分布**<br>若随机变量 $X$ 的密度函数为 $$f\left(x\right)=\begin{cases}\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}x^{\alpha-1}e^{-\lambda x},&x> 0,\\0,&x\le0,\end{cases}$$ 其中 $\alpha> 0$ 为形状参数，$\lambda> 0$ 为尺度参数，则称 $X$ 服从参数为 $\left(\alpha,\lambda\right)$ 的伽马分布，记作 $X\sim Ga\left(\alpha,\lambda\right)$. 当 $\alpha=1$ 时，$Ga\left(1,\lambda\right)$ 为指数分布；当 $\alpha=n/2$，$\lambda=1/2$ 时，$Ga\left(n/2,1/2\right)$ 即 $\chi^2\left(n\right)$ 分布.

### 习题一

（习题 2.2-1）设 $X_1,X_2,X_3,X_4,X_5$ 是来自总体 $X$ 的样本，且 $X\sim N\left(0,1\right)$.

(1) 确定 $a$，$b$ 使得 $a\left(X_1-2X_2+3X_3\right)^2+b\left(4X_4-5X_5\right)^2$ 服从 $\chi^2$ 分布，并指出自由度；

(2) 确定 $c$ 使得 $c\frac{\sum_{i=1}^3 X_i}{\sqrt{\sum_{i=4}^5 X_i^2}}$ 服从 $t$ 分布，并指出自由度；

(3) 确定 $d$ 使得 $d\frac{\sum_{i=1}^3 X_i^2}{\sum_{i=4}^5 X_i^2}$ 服从 $F$ 分布，并指出自由度.

### 解答 习题一

由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_5$ 相互独立且均服从 $N\left(0,1\right)$.

(1) 由**基础知识**（正态分布的可加性），$X_1-2X_2+3X_3$ 为独立正态变量的线性组合，故

$$
X_1-2X_2+3X_3\sim N\left(0,1+4+9\right)=N\left(0,14\right),
$$

标准化得 $\left(X_1-2X_2+3X_3\right)/\sqrt{14}\sim N\left(0,1\right)$，由**定义 2.2.1**（$\chi^2$ 分布），

$$
\frac{\left(X_1-2X_2+3X_3\right)^2}{14}\sim\chi^2\left(1\right).
$$

同理，$4X_4-5X_5\sim N\left(0,16+25\right)=N\left(0,41\right)$，故

$$
\frac{\left(4X_4-5X_5\right)^2}{41}\sim\chi^2\left(1\right).
$$

两项所依赖的样本 $X_1,X_2,X_3$ 与 $X_4,X_5$ 互不重叠，故二者相互独立. 由**$\chi^2$ 分布的性质**（可加性），

$$
\frac{\left(X_1-2X_2+3X_3\right)^2}{14}+\frac{\left(4X_4-5X_5\right)^2}{41}\sim\chi^2\left(2\right).
$$

因此 $a=\frac{1}{14}$，$b=\frac{1}{41}$，自由度为 $2$.

(2) 由正态分布的可加性，$\sum_{i=1}^3 X_i\sim N\left(0,3\right)$，故 $\left(\sum_{i=1}^3 X_i\right)/\sqrt{3}\sim N\left(0,1\right)$. 由**定义 2.2.1**，$\sum_{i=4}^5 X_i^2\sim\chi^2\left(2\right)$，且二者相互独立. 由**定义 2.2.2**（$t$ 分布），

$$
T=\frac{\left(\sum_{i=1}^3 X_i\right)/\sqrt{3}}{\sqrt{\left(\sum_{i=4}^5 X_i^2\right)/2}}=\sqrt{\frac{2}{3}}\cdot\frac{\sum_{i=1}^3 X_i}{\sqrt{\sum_{i=4}^5 X_i^2}}\sim t\left(2\right).
$$

因此 $c=\sqrt{\frac{2}{3}}$，自由度为 $2$.

(3) 由**定义 2.2.1**，$\sum_{i=1}^3 X_i^2\sim\chi^2\left(3\right)$，$\sum_{i=4}^5 X_i^2\sim\chi^2\left(2\right)$，且二者相互独立. 由**定义 2.2.3**（$F$ 分布），

$$
F=\frac{\left(\sum_{i=1}^3 X_i^2\right)/3}{\left(\sum_{i=4}^5 X_i^2\right)/2}=\frac{2}{3}\cdot\frac{\sum_{i=1}^3 X_i^2}{\sum_{i=4}^5 X_i^2}\sim F\left(3,2\right).
$$

因此 $d=\frac{2}{3}$，自由度为 $\left(3,2\right)$. $\blacksquare$

### 习题二

（习题 2.2-2）设随机变量 $X$ 服从自由度为 $n$ 的 $\chi^2$ 分布，证明：

$$
E\left(X^k\right)=\frac{2^k\Gamma\left(n/2+k\right)}{\Gamma\left(n/2\right)},\quad k=1,2,\dots
$$

特别地，有 $E\left(X\right)=n$，$D\left(X\right)=2n$.

### 解答 习题二

由**定理 2.2.1**（$\chi^2$ 分布的密度函数），$X\sim\chi^2\left(n\right)$ 的密度函数为

$$
f\left(x\right)=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2},\quad x> 0.
$$

于是

$$
E\left(X^k\right)=\int_0^{+\infty}x^k\cdot\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2}\,\mathrm{d}x.
$$

令 $u=x/2$，则 $x=2u$，$\mathrm{d}x=2\,\mathrm{d}u$，代入得

$$
E\left(X^k\right)=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}\int_0^{+\infty}\left(2u\right)^{n/2+k-1}e^{-u}\cdot2\,\mathrm{d}u=\frac{2^k}{\Gamma\left(n/2\right)}\int_0^{+\infty}u^{n/2+k-1}e^{-u}\,\mathrm{d}u.
$$

由伽马函数的定义 $\Gamma\left(s\right)=\int_0^{+\infty}u^{s-1}e^{-u}\,\mathrm{d}u$，即得

$$
E\left(X^k\right)=\frac{2^k\Gamma\left(n/2+k\right)}{\Gamma\left(n/2\right)}.
$$

特别地，当 $k=1$ 时，利用 $\Gamma\left(s+1\right)=s\Gamma\left(s\right)$，

$$
E\left(X\right)=\frac{2\Gamma\left(n/2+1\right)}{\Gamma\left(n/2\right)}=\frac{2\cdot\frac{n}{2}\Gamma\left(n/2\right)}{\Gamma\left(n/2\right)}=n.
$$

当 $k=2$ 时，

$$
E\left(X^2\right)=\frac{4\Gamma\left(n/2+2\right)}{\Gamma\left(n/2\right)}=\frac{4\cdot\frac{n}{2}\cdot\left(\frac{n}{2}+1\right)\Gamma\left(n/2\right)}{\Gamma\left(n/2\right)}=n\left(n+2\right).
$$

因此

$$
D\left(X\right)=E\left(X^2\right)-\left[E\left(X\right)\right]^2=n\left(n+2\right)-n^2=2n.
$$

$\blacksquare$

### 习题三

（习题 2.2-3）设某连续型总体 $X$ 的分布函数 $F\left(x\right)$ 是连续的严格单调递增函数，$X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，证明：

(1) $Y=F\left(X\right)\sim U\left(0,1\right)$；

(2) $U=-2\sum_{i=1}^n\ln Y_i\sim\chi^2\left(2n\right)$.

### 解答 习题三

(1) 由 $F\left(x\right)$ 连续且严格单调递增，其反函数 $F^{-1}$ 存在. 对任意 $0\le y\le1$，

$$
P\left\{Y\le y\right\}=P\left\{F\left(X\right)\le y\right\}=P\left\{X\le F^{-1}\left(y\right)\right\}=F\left(F^{-1}\left(y\right)\right)=y.
$$

当 $y< 0$ 时 $P\left\{Y\le y\right\}=0$；当 $y> 1$ 时 $P\left\{Y\le y\right\}=1$. 故 $Y=F\left(X\right)\sim U\left(0,1\right)$.

(2) 由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 相互独立且与总体 $X$ 同分布，故由 (1)，$Y_i=F\left(X_i\right)\sim U\left(0,1\right)$，且 $Y_1,Y_2,\dots,Y_n$ 相互独立.

令 $Z_i=-2\ln Y_i$. 对 $z> 0$，

$$
P\left\{Z_i\le z\right\}=P\left\{-2\ln Y_i\le z\right\}=P\left\{\ln Y_i\ge-\frac{z}{2}\right\}=P\left\{Y_i\ge e^{-z/2}\right\}=1-e^{-z/2}.
$$

该式即自由度为 $2$ 的 $\chi^2$ 分布的分布函数（由**伽马分布**，$\chi^2\left(2\right)=Ga\left(1,1/2\right)$ 为参数 $1/2$ 的指数分布），故 $Z_i\sim\chi^2\left(2\right)$. 由 $Y_i$ 相互独立知 $Z_i$ 相互独立，再由**$\chi^2$ 分布的性质**（可加性），

$$
U=\sum_{i=1}^n Z_i=-2\sum_{i=1}^n\ln Y_i\sim\chi^2\left(2n\right).
$$

$\blacksquare$

### 习题四

（习题 2.2-6）设随机变量 $X$ 服从参数为 $\alpha$，$\lambda$ 的伽马分布 $Ga\left(\alpha,\lambda\right)$，$\alpha> 0$，$\lambda> 0$. 证明：

(1) $X$ 的特征函数为 $\varphi\left(t\right)=\left(1-\frac{it}{\lambda}\right)^{-\alpha}$；

(2) $E\left(X^k\right)=\frac{\Gamma\left(\alpha+k\right)}{\Gamma\left(\alpha\right)\lambda^k}$，特别地，$E\left(X\right)=\frac{\alpha}{\lambda}$，$D\left(X\right)=\frac{\alpha}{\lambda^2}$；

(3) 如果 $X_i\sim Ga\left(\alpha_i,\lambda\right)$，$i=1,2,\dots,n$ 且 $X_1,X_2,\dots,X_n$ 相互独立，则 $\sum_{i=1}^n X_i\sim Ga\left(\alpha_1+\alpha_2+\dots+\alpha_n,\lambda\right)$；

(4) 若取 $\alpha=n/2$，$\lambda=1/2$，则 $Ga\left(n/2,1/2\right)$ 是 $\chi^2\left(n\right)$ 分布；

(5) 若取 $\alpha=1$，则 $Ga\left(1,\lambda\right)$ 是指数分布.

### 解答 习题四

由**伽马分布**，$X\sim Ga\left(\alpha,\lambda\right)$ 的密度函数为

$$
f\left(x\right)=\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}x^{\alpha-1}e^{-\lambda x},\quad x> 0.
$$

(1) 特征函数为

$$
\varphi\left(t\right)=E\left(e^{itX}\right)=\int_0^{+\infty}e^{itx}\cdot\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}x^{\alpha-1}e^{-\lambda x}\,\mathrm{d}x=\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}\int_0^{+\infty}x^{\alpha-1}e^{-\left(\lambda-it\right)x}\,\mathrm{d}x.
$$

由伽马函数定义，$\int_0^{+\infty}x^{\alpha-1}e^{-sx}\,\mathrm{d}x=\Gamma\left(\alpha\right)/s^\alpha$（$\mathrm{Re}\left(s\right)> 0$），故

$$
\varphi\left(t\right)=\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}\cdot\frac{\Gamma\left(\alpha\right)}{\left(\lambda-it\right)^\alpha}=\left(\frac{\lambda}{\lambda-it}\right)^\alpha=\left(1-\frac{it}{\lambda}\right)^{-\alpha}.
$$

(2) $k$ 阶原点矩为

$$
E\left(X^k\right)=\int_0^{+\infty}x^k\cdot\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}x^{\alpha-1}e^{-\lambda x}\,\mathrm{d}x=\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}\int_0^{+\infty}x^{\alpha+k-1}e^{-\lambda x}\,\mathrm{d}x=\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}\cdot\frac{\Gamma\left(\alpha+k\right)}{\lambda^{\alpha+k}}=\frac{\Gamma\left(\alpha+k\right)}{\Gamma\left(\alpha\right)\lambda^k}.
$$

特别地，$E\left(X\right)=\frac{\Gamma\left(\alpha+1\right)}{\Gamma\left(\alpha\right)\lambda}=\frac{\alpha}{\lambda}$，$E\left(X^2\right)=\frac{\Gamma\left(\alpha+2\right)}{\Gamma\left(\alpha\right)\lambda^2}=\frac{\alpha\left(\alpha+1\right)}{\lambda^2}$，故

$$
D\left(X\right)=E\left(X^2\right)-\left[E\left(X\right)\right]^2=\frac{\alpha\left(\alpha+1\right)}{\lambda^2}-\frac{\alpha^2}{\lambda^2}=\frac{\alpha}{\lambda^2}.
$$

(3) 由 $X_i$ 相互独立，$\sum_{i=1}^n X_i$ 的特征函数为各特征函数之积：

$$
\varphi_{\sum X_i}\left(t\right)=\prod_{i=1}^n\left(1-\frac{it}{\lambda}\right)^{-\alpha_i}=\left(1-\frac{it}{\lambda}\right)^{-\sum_{i=1}^n\alpha_i}.
$$

由特征函数与分布函数相互唯一确定，$\sum_{i=1}^n X_i\sim Ga\left(\alpha_1+\alpha_2+\dots+\alpha_n,\lambda\right)$.

(4) 当 $\alpha=n/2$，$\lambda=1/2$ 时，密度函数为

$$
f\left(x\right)=\frac{\left(1/2\right)^{n/2}}{\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2}=\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2},
$$

与**定理 2.2.1**（$\chi^2$ 分布的密度函数）一致，故 $Ga\left(n/2,1/2\right)$ 即 $\chi^2\left(n\right)$ 分布.

(5) 当 $\alpha=1$ 时，$\Gamma\left(1\right)=1$，密度函数为

$$
f\left(x\right)=\lambda e^{-\lambda x},\quad x> 0,
$$

即参数为 $\lambda$ 的指数分布. $\blacksquare$

### 习题五

（习题 2.2-7）设随机变量 $X\sim\chi^2\left(m\right)$，$Y\sim\chi^2\left(n\right)$，且 $X$ 与 $Y$ 相互独立，证明 $U=X/Y$ 与 $V=X+Y$ 相互独立.

### 解答 习题五

由**定理 2.2.1**（$\chi^2$ 分布的密度函数）及 $X$ 与 $Y$ 相互独立，$\left(X,Y\right)$ 的联合密度函数为

$$
f\left(x,y\right)=\frac{1}{2^{\left(m+n\right)/2}\Gamma\left(m/2\right)\Gamma\left(n/2\right)}x^{m/2-1}y^{n/2-1}e^{-\left(x+y\right)/2},\quad x> 0,\ y> 0.
$$

作变换 $u=x/y$，$v=x+y$，即 $x=\frac{uv}{1+u}$，$y=\frac{v}{1+u}$. 该变换的雅可比行列式为

$$
J=\frac{\partial\left(x,y\right)}{\partial\left(u,v\right)}=\begin{vmatrix}\frac{v}{\left(1+u\right)^2}&\frac{u}{1+u}\\-\frac{v}{\left(1+u\right)^2}&\frac{1}{1+u}\end{vmatrix}=\frac{v}{\left(1+u\right)^2}.
$$

于是 $\left(U,V\right)$ 的联合密度函数为

$$
g\left(u,v\right)=f\left(\frac{uv}{1+u},\frac{v}{1+u}\right)\left|J\right|.
$$

代入得

$$
g\left(u,v\right)=\frac{1}{2^{\left(m+n\right)/2}\Gamma\left(m/2\right)\Gamma\left(n/2\right)}\left(\frac{uv}{1+u}\right)^{m/2-1}\left(\frac{v}{1+u}\right)^{n/2-1}e^{-v/2}\cdot\frac{v}{\left(1+u\right)^2}.
$$

整理后，$u$ 与 $v$ 的变量分离为

$$
g\left(u,v\right)=\underbrace{\frac{\Gamma\left(\left(m+n\right)/2\right)}{\Gamma\left(m/2\right)\Gamma\left(n/2\right)}u^{m/2-1}\left(1+u\right)^{-\left(m+n\right)/2}}_{g_U\left(u\right)}\cdot\underbrace{\frac{1}{2^{\left(m+n\right)/2}\Gamma\left(\left(m+n\right)/2\right)}v^{\left(m+n\right)/2-1}e^{-v/2}}_{g_V\left(v\right)}.
$$

其中 $g_V\left(v\right)$ 恰为 $\chi^2\left(m+n\right)$ 分布的密度函数（由**$\chi^2$ 分布的性质**之可加性，$X+Y\sim\chi^2\left(m+n\right)$），$g_U\left(u\right)$ 仅含 $u$. 由于 $g\left(u,v\right)=g_U\left(u\right)g_V\left(v\right)$，故 $U=X/Y$ 与 $V=X+Y$ 相互独立. 此即**推论 2.2.1**. $\blacksquare$

### 习题六

（习题 2.2-8）以 $f_n\left(x\right)$ 表示自由度为 $n$ 的 $t$ 变量的密度函数，证明：

$$
\lim_{n\to+\infty}f_n\left(x\right)=\frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}.
$$

### 解答 习题六

由**定理 2.2.2**（$t$ 分布的密度函数），

$$
f_n\left(x\right)=\frac{\Gamma\left(\left(n+1\right)/2\right)}{\Gamma\left(n/2\right)\sqrt{n\pi}}\left(1+\frac{x^2}{n}\right)^{-\left(n+1\right)/2}.
$$

利用斯特林公式 $\Gamma\left(s+1\right)\sim\sqrt{2\pi s}\left(s/e\right)^s$ 可得渐近关系

$$
\frac{\Gamma\left(n/2+1/2\right)}{\Gamma\left(n/2\right)}\sim\left(\frac{n}{2}\right)^{1/2}=\sqrt{\frac{n}{2}},\quad n\to+\infty.
$$

因此

$$
\frac{\Gamma\left(\left(n+1\right)/2\right)}{\Gamma\left(n/2\right)\sqrt{n\pi}}\sim\frac{\sqrt{n/2}}{\sqrt{n\pi}}=\frac{1}{\sqrt{2\pi}}.
$$

另一方面，

$$
\left(1+\frac{x^2}{n}\right)^{-\left(n+1\right)/2}=\left[\left(1+\frac{x^2}{n}\right)^n\right]^{-\frac{n+1}{2n}}\longrightarrow\left(e^{x^2}\right)^{-1/2}=e^{-x^2/2}.
$$

两式相乘即得

$$
\lim_{n\to+\infty}f_n\left(x\right)=\frac{1}{\sqrt{2\pi}}e^{-x^2/2}.
$$

即当 $n\to+\infty$ 时，$t\left(n\right)$ 分布的密度函数收敛于标准正态分布 $N\left(0,1\right)$ 的密度函数.

$\blacksquare$

### 习题七

（习题 2.2-10）设随机变量 $X\sim F\left(1,1\right)$，求 $P\left\{X< 1\right\}$.

### 解答 习题七

由**定义 2.2.3**（$F$ 分布），$X\sim F\left(1,1\right)$ 意味着存在相互独立的 $Y_1\sim\chi^2\left(1\right)$，$Y_2\sim\chi^2\left(1\right)$，使得

$$
X=\frac{Y_1/1}{Y_2/1}=\frac{Y_1}{Y_2}.
$$

由**定义 2.2.1**（$\chi^2$ 分布），$Y_1=Z_1^2$，$Y_2=Z_2^2$，其中 $Z_1,Z_2$ 相互独立且均服从 $N\left(0,1\right)$. 故

$$
X=\frac{Z_1^2}{Z_2^2}=\left(\frac{Z_1}{Z_2}\right)^2.
$$

由 $Z_1,Z_2$ 独立同分布于 $N\left(0,1\right)$，它们关于原点对称且地位完全对等. 由**$F$ 分布的性质**，若 $X\sim F\left(1,1\right)$，则 $1/X\sim F\left(1,1\right)$，即 $X$ 与 $1/X$ 同分布. 因此

$$
P\left\{X< 1\right\}=P\left\{\frac{1}{X}> 1\right\}=P\left\{X> 1\right\}.
$$

又 $P\left\{X=1\right\}=0$（连续型分布），故

$$
P\left\{X< 1\right\}+P\left\{X> 1\right\}=1,
$$

从而 $P\left\{X< 1\right\}=\frac{1}{2}$. $\blacksquare$
