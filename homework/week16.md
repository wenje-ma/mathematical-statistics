# 作业 16

> **定义 5.1.1**（功效函数）<br>设 $\varphi\left(x\right)$ 是假设检验问题 $H_0:\theta\in\Theta_0$；$H_1:\theta\in\Theta_1$ 的一个检验函数，则函数 $$\beta\left(\theta\right)=P_\theta\left\{\text{检验函数拒绝原假设 }H_0\right\}=E_\theta\left[\varphi\left(X\right)\right],\ \theta\in\Theta,$$ 称为该检验的功效函数（效函数或势函数）. 对非随机化检验，$\beta\left(\theta\right)$ 即参数为 $\theta$ 时样本落入拒绝域的概率，亦即拒绝原假设 $H_0$ 的概率.

> **两类错误**（第一类错误与第二类错误）<br>当原假设 $H_0$ 为真时却拒绝 $H_0$，称为犯**第一类错误**（弃真错误），其概率为 $\beta\left(\theta\right),\ \theta\in\Theta_0$；当 $H_0$ 不真时却接受 $H_0$，称为犯**第二类错误**（取伪错误），其概率为 $1-\beta\left(\theta\right),\ \theta\in\Theta_1$.

> **定义 5.1.2**（显著性检验与检验水平）<br>若检验函数 $\varphi\left(x\right)$ 犯第一类错误的概率总不超过 $\alpha$，即 $\beta\left(\theta\right)\le\alpha,\ \theta\in\Theta_0$，则称 $\alpha$ 为该检验的一个水平，称 $\varphi$ 为显著性水平为 $\alpha$ 的检验，简称水平为 $\alpha$ 的检验.

> **抽样分布**（正态样本均值的分布）<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，则样本均值 $$\bar X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right).$$

### 习题一

（习题 5.1-5）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,1\right)$ 的样本，其中 $\mu\in\mathbb R$ 为未知参数，设检验问题 $H_0:\mu=0$；$H_1:\mu=1$ 的拒绝域为 $D=\left\{\bar X\ge0.98\right\}$.

(1) 若 $n=4$，求该检验犯第一类错误的概率和犯第二类错误的概率；

(2) 若要使该检验犯第一类错误的概率不超过 $0.01$，样本容量 $n$ 最少取多少？

### 解答 习题一

由**抽样分布**（正态样本均值的分布），在 $H_0:\mu=0$ 下 $\bar X\sim N\left(0,\frac{1}{n}\right)$，在 $H_1:\mu=1$ 下 $\bar X\sim N\left(1,\frac{1}{n}\right)$. 由**定义 5.1.1**（功效函数），$\beta\left(\mu\right)=P_\mu\left\{\bar X\ge0.98\right\}$.

(1) 当 $n=4$ 时，在 $H_0$ 下 $\bar X\sim N\left(0,\frac{1}{4}\right)$. 由**两类错误**（第一类错误与第二类错误），犯第一类错误的概率为

$$
\alpha=\beta\left(0\right)=P_0\left\{\bar X\ge0.98\right\}=P\left\{Z\ge\frac{0.98}{1/2}\right\}=P\left\{Z\ge1.96\right\}=0.025,
$$

其中 $Z\sim N\left(0,1\right)$.

犯第二类错误的概率为

$$
\beta_2=1-\beta\left(1\right)=P_1\left\{\bar X<0.98\right\}=P\left\{Z<\frac{0.98-1}{1/2}\right\}=P\left\{Z<-0.04\right\}=\Phi\left(-0.04\right)=0.484.
$$

(2) 由**定义 5.1.2**（显著性检验与检验水平），要求犯第一类错误的概率不超过 $0.01$，即

$$
\beta\left(0\right)=P_0\left\{\bar X\ge0.98\right\}=P\left\{Z\ge0.98\sqrt n\right\}\le0.01.
$$

故 $0.98\sqrt n\ge u_{0.01}=2.326$，即 $\sqrt n\ge2.373$，$n\ge5.64$. 因此样本容量 $n$ 最少取 $6$.

$\blacksquare$

### 习题二

（习题 5.1-7）设样本 $X$（容量为 $1$）取自具有密度函数 $f\left(\cdot\right)$ 的总体，关于总体的两个假设如下：

$$
H_0:f\left(x\right)=\begin{cases}1,&0<x<1,\\0,&\text{其他};\end{cases}\ \ H_1:f\left(x\right)=\begin{cases}2x,&0<x<1,\\0,&\text{其他}.\end{cases}
$$

设该检验的拒绝域为 $D=\left\{X>\frac{2}{3}\right\}$. 求该检验犯第一类错误的概率和犯第二类错误的概率.

### 解答 习题二

由**两类错误**（第一类错误与第二类错误），犯第一类错误的概率为 $H_0$ 为真时样本落入拒绝域的概率，即

$$
\alpha=P_{H_0}\left\{X>\frac{2}{3}\right\}=\int_{2/3}^1 1\,\mathrm dx=\frac{1}{3}.
$$

犯第二类错误的概率为 $H_1$ 为真时样本落入接受域的概率，即

$$
\beta_2=P_{H_1}\left\{X\le\frac{2}{3}\right\}=\int_0^{2/3}2x\,\mathrm dx=\left[x^2\right]_0^{2/3}=\frac{4}{9}.
$$

$\blacksquare$

### 习题三

（习题 5.1-8）设 $X_1,X_2,\dots,X_{10}$ 是来自均匀分布总体 $U\left[0,\theta\right]$ 的样本，其中 $\theta>0$ 为未知参数，设检验问题 $H_0:\theta=1$；$H_1:\theta>1$ 的拒绝域为 $D=\left\{\left(X_1,\dots,X_{10}\right):X_{\left(10\right)}\ge0.95\right\}$，其中 $X_{\left(10\right)}=\max\left\{X_1,\dots,X_{10}\right\}$.

(1) 求该检验的显著性水平；

(2) 求该检验的功效函数.

### 解答 习题三

对均匀分布总体 $U\left[0,\theta\right]$，其分布函数为 $F_\theta\left(x\right)=\frac{x}{\theta},\ 0\le x\le\theta$. 由顺序统计量的分布，对 $0\le t\le\theta$，

$$
P_\theta\left\{X_{\left(10\right)}<t\right\}=\prod_{i=1}^{10}P_\theta\left\{X_i<t\right\}=\left(\frac{t}{\theta}\right)^{10}.
$$

由**定义 5.1.1**（功效函数），功效函数为 $\beta\left(\theta\right)=P_\theta\left\{X_{\left(10\right)}\ge0.95\right\}$.

(1) 原假设 $H_0:\theta=1$ 为简单假设，由**定义 5.1.2**（显著性检验与检验水平），检验水平为

$$
\beta\left(1\right)=P_1\left\{X_{\left(10\right)}\ge0.95\right\}=1-P_1\left\{X_{\left(10\right)}<0.95\right\}=1-0.95^{10}=0.4013.
$$

(2) 分两种情况讨论功效函数. 当 $0<\theta\le0.95$ 时，所有 $X_i\le\theta\le0.95$，故 $X_{\left(10\right)}\le0.95$ 恒成立，$\beta\left(\theta\right)=0$；当 $\theta>0.95$ 时，

$$
\beta\left(\theta\right)=1-P_\theta\left\{X_{\left(10\right)}<0.95\right\}=1-\left(\frac{0.95}{\theta}\right)^{10}.
$$

综上，

$$
\beta\left(\theta\right)=\begin{cases}0,&0<\theta\le0.95,\\1-\left(\dfrac{0.95}{\theta}\right)^{10},&\theta>0.95.\end{cases}
$$

$\blacksquare$
