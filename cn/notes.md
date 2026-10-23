# 数理统计

## 绪论与基本概念

**定义 1.2.1** (总体)

数理统计中, 把所研究问题涉及的研究对象的全体称为总体. 组成总体的每个元素称为个体. 总体中所包含个体的个数称为总体容量. 实际问题中, 总体可用一个随机变量 $X$ 及其分布来描述, 对总体的研究转化为对表示总体的随机变量 $X$ 的统计规律性的研究, 因此今后不区分总体与相应的随机变量, 统称为总体 $X$.

**定义 1.3.1** (样本空间)

样本 $X_1,X_2,\dots,X_n$ 可能取值的全体的集合, 称为样本空间.

**定义 1.3.2** (简单随机样本)

设有一总体 $X$, 具有分布 $F$, $X_1,X_2,\dots,X_n$ 是从总体 $X$ 中抽取的容量为 $n$ 的样本. 若

(1) $X_1,X_2,\dots,X_n$ 相互独立;

(2) $X_1,X_2,\dots,X_n$ 与总体 $X$ 有相同的分布 $F$,

则称 $X_1,X_2,\dots,X_n$ 是从总体 $X$ 中抽取的容量为 $n$ 的简单随机样本, 简称样本.

**样本分布** (联合分布函数, 联合分布列与联合密度函数)

设总体 $X$ 的分布函数为 $F\left(x\right)$, $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本, 则样本的联合分布函数为

$$
F^{*}\left(x_1,x_2,\dots,x_n\right)=\prod_{i=1}^n F\left(x_i\right).
$$

若总体 $X$ 是离散型随机变量, 分布列为 $P\left\{X=a_i\right\}=p_i$, 则样本 $X_1,X_2,\dots,X_n$ 的联合分布列为

$$
P\left\{X_1=x_1,\dots,X_n=x_n\right\}=\prod_{i=1}^n p_{x_i}.
$$

若总体 $X$ 是连续型随机变量, 密度函数为 $f\left(x\right)$, 则样本 $X_1,X_2,\dots,X_n$ 的联合密度函数为

$$
f^{*}\left(x_1,x_2,\dots,x_n\right)=\prod_{i=1}^n f\left(x_i\right).
$$

**定义 1.3.3** (参数空间)

数理统计中, 称出现在总体分布或样本分布中的未知常数为参数. 参数 $\theta$ 所有可能取值的全体构成的集合, 称为参数空间, 记为 $\Theta$.

**总体分布族与样本分布族**

由于不同的参数值一般对应于不同的总体分布, 参数空间中所有可能的参数值对应于一族总体分布, 称该分布族为总体分布族, 记为 $\left\{f\left(x;\theta\right):\theta\in\Theta\right\}$. 不同的参数值也一般对应于不同的样本分布, 参数空间中所有可能的参数值对应于一族样本分布, 称该分布族为样本分布族, 记为

$$
\left\{\prod_{i=1}^n f\left(x_i;\theta\right):\theta\in\Theta\right\}.
$$

**定义 1.4.1** (统计量)

设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本, $g\left(X_1,X_2,\dots,X_n\right)$ 是样本 $X_1,X_2,\dots,X_n$ 的函数, 且除依赖于样本外, 不依赖于任何其他的未知量, 则称 $g\left(X_1,X_2,\dots,X_n\right)$ 为统计量. 若 $x_1,x_2,\dots,x_n$ 为样本 $X_1,X_2,\dots,X_n$ 的观察值, 称 $g\left(x_1,x_2,\dots,x_n\right)$ 为统计量 $g\left(X_1,X_2,\dots,X_n\right)$ 的一个观察值. 统计量只与样本有关, 不依赖任何未知参数.

**定义 1.5.1** (经验分布函数)

设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本, $X_{\left(1\right)}\le X_{\left(2\right)}\le\dots\le X_{\left(n\right)}$ 为其顺序统计量, 对任意实数 $x$, 称

$$
F_n\left(x\right)=\begin{cases}0,&x< X_{\left(1\right)},\\\frac{r}{n},&X_{\left(r\right)}\le x< X_{\left(r+1\right)},\ r=1,2,\dots,n-1,\\1,&x\ge X_{\left(n\right)}\end{cases}
$$

为样本 $X_1,X_2,\dots,X_n$ 的经验分布函数.

## 抽样分布: 顺序统计量与常用抽样分布

**抽样分布** (定义)

统计量是样本 $X_1,X_2,\dots,X_n$ 的函数, 而样本 $X_1,X_2,\dots,X_n$ 是随机变量. 因此, 统计量也是随机变量, 统计量的分布称为抽样分布.

**定理** (顺序统计量的分布)

设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本, 且 $X$ 的分布函数为 $F\left(x\right)$, $\left(X_{\left(1\right)},X_{\left(2\right)},\dots,X_{\left(n\right)}\right)$ 是其顺序统计量, 则对 $1\le r\le n$, $X_{\left(r\right)}$ 的分布函数为

$$
F_{\left(r\right)}\left(x\right)=P\left\{X_{\left(r\right)}\le x\right\}=\sum_{k=r}^n\binom{n}{k}\left[F\left(x\right)\right]^k\left[1-F\left(x\right)\right]^{n-k}=r\binom{n}{r}\int_0^{F\left(x\right)}t^{r-1}\left(1-t\right)^{n-r}\,\mathrm{d}t.
$$

若总体 $X$ 为连续型且有密度函数 $f\left(x\right)$, 则 $X_{\left(r\right)}$ 的密度函数为

$$
f_{\left(r\right)}\left(x\right)=F_{\left(r\right)}'\left(x\right)=r\binom{n}{r}\left[F\left(x\right)\right]^{r-1}\left[1-F\left(x\right)\right]^{n-r}f\left(x\right).
$$

特别地, 当 $r=1$ 时, 最小顺序统计量 $X_{\left(1\right)}$ 的分布函数和密度函数分别为

$$
F_{\left(1\right)}\left(x\right)=1-\left[1-F\left(x\right)\right]^n,\quad f_{\left(1\right)}\left(x\right)=n\left[1-F\left(x\right)\right]^{n-1}f\left(x\right);
$$

当 $r=n$ 时, 最大顺序统计量 $X_{\left(n\right)}$ 的分布函数和密度函数分别为

$$
F_{\left(n\right)}\left(x\right)=\left[F\left(x\right)\right]^n,\quad f_{\left(n\right)}\left(x\right)=n\left[F\left(x\right)\right]^{n-1}f\left(x\right).
$$

**基础知识** (泊松分布的可加性)

设 $X_1,X_2,\dots,X_n$ 相互独立, 且 $X_i\sim P\left(\lambda_i\right)$, 则 $\sum_{i=1}^n X_i\sim P\left(\sum_{i=1}^n\lambda_i\right)$.

**基础知识** (正态分布的可加性)

设 $X_1,X_2,\dots,X_n$ 相互独立, 且 $X_i\sim N\left(\mu_i,\sigma_i^2\right)$, 则 $\sum_{i=1}^n X_i\sim N\left(\sum_{i=1}^n\mu_i,\sum_{i=1}^n\sigma_i^2\right)$.

**定义 2.2.1** ($\chi^2$ 分布)

设 $X_1,X_2,\dots,X_n$ 相互独立且都服从 $N\left(0,1\right)$, 则称

$$
\chi^2=X_1^2+X_2^2+\dots+X_n^2
$$

为自由度为 $n$ 的 $\chi^2$ 变量, 其分布称为自由度为 $n$ 的 $\chi^2$ 分布, 记作 $\chi^2\sim\chi^2\left(n\right)$.

**定理 2.2.1** ($\chi^2$ 分布的密度函数)

设 $\chi^2\sim\chi^2\left(n\right)$, 则其密度函数为

$$
f\left(x\right)=\begin{cases}\frac{1}{2^{n/2}\Gamma\left(n/2\right)}x^{n/2-1}e^{-x/2},&x> 0,\\0,&x\le0.\end{cases}
$$

**$\chi^2$ 分布的性质**

设 $\chi^2\sim\chi^2\left(n\right)$, 则 $E\left(\chi^2\right)=n$, $D\left(\chi^2\right)=2n$. 若 $X_1\sim\chi^2\left(n_1\right)$, $X_2\sim\chi^2\left(n_2\right)$, 且 $X_1$ 与 $X_2$ 相互独立, 则 $X_1+X_2\sim\chi^2\left(n_1+n_2\right)$, 该性质称为 $\chi^2$ 分布的可加性.

**定义 2.2.2** ($t$ 分布)

设随机变量 $X\sim N\left(0,1\right)$, $Y\sim\chi^2\left(n\right)$, 且 $X$ 与 $Y$ 相互独立, 则称随机变量

$$
T=\frac{X}{\sqrt{Y/n}}
$$

为自由度为 $n$ 的 $t$ 变量, 其分布称为自由度为 $n$ 的 $t$ 分布, 记作 $T\sim t\left(n\right)$.

**定理 2.2.2** ($t$ 分布的密度函数)

设 $T\sim t\left(n\right)$, 则其密度函数为

$$
f\left(t\right)=\frac{\Gamma\left(\left(n+1\right)/2\right)}{\Gamma\left(n/2\right)\sqrt{n\pi}}\left(1+\frac{t^2}{n}\right)^{-\left(n+1\right)/2},\quad-\infty< t< +\infty.
$$

**定义 2.2.3** ($F$ 分布)

设随机变量 $X\sim\chi^2\left(m\right)$, $Y\sim\chi^2\left(n\right)$, 且 $X$ 与 $Y$ 相互独立, 则称随机变量

$$
F=\frac{X/m}{Y/n}
$$

为自由度为 $m$ 和 $n$ 的 $F$ 变量, 其所服从的分布称为 $F$ 分布, 记作 $F\sim F\left(m,n\right)$.

**推论 2.2.1** ($X/Y$ 与 $X+Y$ 的独立性)

设随机变量 $X\sim\chi^2\left(m\right)$, $Y\sim\chi^2\left(n\right)$, 且 $X$ 与 $Y$ 相互独立, 则 $U=X/Y$ 与 $V=X+Y$ 相互独立.

**伽马分布**

若随机变量 $X$ 的密度函数为

$$
f\left(x\right)=\begin{cases}\frac{\lambda^\alpha}{\Gamma\left(\alpha\right)}x^{\alpha-1}e^{-\lambda x},&x> 0,\\0,&x\le0,\end{cases}
$$

其中 $\alpha> 0$ 为形状参数, $\lambda> 0$ 为尺度参数, 则称 $X$ 服从参数为 $\left(\alpha,\lambda\right)$ 的伽马分布, 记作 $X\sim Ga\left(\alpha,\lambda\right)$. 当 $\alpha=1$ 时, $Ga\left(1,\lambda\right)$ 为指数分布; 当 $\alpha=n/2$, $\lambda=1/2$ 时, $Ga\left(n/2,1/2\right)$ 即 $\chi^2\left(n\right)$ 分布.

**引理 2.3.1** (样本均值与样本方差的期望)

设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的一个样本, 且 $E\left(X\right)=\mu$, $D\left(X\right)=\sigma^2$, $\overline X=\frac{1}{n}\sum_{i=1}^n X_i$ 和 $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\overline X\right)^2$ 分别为样本均值和样本方差, 则

$$
E\left(\overline X\right)=\mu,\quad D\left(\overline X\right)=\frac{\sigma^2}{n},\quad E\left(S^2\right)=\sigma^2.
$$

**定理 2.3.3** (正态总体样本均值与样本方差的分布)

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本, $\overline X$ 和 $S^2$ 分别为样本均值和样本方差, 则有:

(1) $\overline X\sim N\left(\mu,\sigma^2/n\right)$, 即 $\frac{\overline X-\mu}{\sigma/\sqrt n}\sim N\left(0,1\right)$;

(2) $\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$;

(3) $\overline X$ 和 $S^2$ 相互独立.

**定理 2.3.4**

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本, 则

$$
\frac{1}{\sigma^2}\sum_{i=1}^n\left(X_i-\mu\right)^2\sim\chi^2\left(n\right).
$$

**定义 2.2.2** ($t$ 分布)

设随机变量 $X\sim N\left(0,1\right)$, $Y\sim\chi^2\left(n\right)$, 且 $X$ 与 $Y$ 相互独立, 则称 $T=\frac{X}{\sqrt{Y/n}}$ 为自由度为 $n$ 的 $t$ 变量, 记作 $T\sim t\left(n\right)$.

**定义 2.2.3** ($F$ 分布)

设随机变量 $X\sim\chi^2\left(m\right)$, $Y\sim\chi^2\left(n\right)$, 且 $X$ 与 $Y$ 相互独立, 则称 $F=\frac{X/m}{Y/n}$ 为自由度为 $m$ 和 $n$ 的 $F$ 变量, 记作 $F\sim F\left(m,n\right)$.

**$\chi^2$ 分布的性质** (可加性)

设 $X_1\sim\chi^2\left(n_1\right)$, $X_2\sim\chi^2\left(n_2\right)$, 且 $X_1$ 与 $X_2$ 相互独立, 则 $X_1+X_2\sim\chi^2\left(n_1+n_2\right)$.

**基础知识** (中心极限定理)

设 $X_1,X_2,\dots,X_n$ 独立同分布, 且 $E\left(X_i\right)=\mu$, $D\left(X_i\right)=\sigma^2> 0$, 则

$$
\frac{\overline X-\mu}{\sigma/\sqrt n}\xrightarrow{L}N\left(0,1\right).
$$

**基础知识** (斯卢茨基引理)

设随机变量序列 $X_n\xrightarrow{L}X$, $Y_n\xrightarrow{P}c$ ($c$ 为常数) , 则 $X_n/Y_n\xrightarrow{L}X/c$ ($c\ne0$) .

## 指数族与充分完备统计量

**定义 2.4.1** (指数族)

设 $\mathcal{F}=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ 是定义在样本空间 $\mathcal{X}$ 上的分布族, 其中 $\Theta$ 为参数空间. 若 $f\left(x,\theta\right)$ 可以表示为

$$
f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k Q_i\left(\theta\right)T_i\left(x\right)\right\}h\left(x\right),
$$

则称此分布族为指数型分布族, 简称指数族. 其中 $C\left(\theta\right)> 0$ 和 $Q_i\left(\theta\right)$ 定义在参数空间 $\Theta$ 上, $h\left(x\right)> 0$ 和 $T_i\left(x\right)$ 定义在样本空间 $\mathcal{X}$ 上, 且支撑集 $\left\{x:f\left(x,\theta\right)> 0\right\}$ 与 $\theta$ 无关.

**定义 2.4.2** (指数族的自然形式)

如果指数族有下列形式

$$
f\left(x,\varphi\right)=C\left(\varphi\right)\exp\left\{\sum_{i=1}^k\varphi_i T_i\left(x\right)\right\}h\left(x\right),
$$

则称其为指数族的自然形式, 也称为标准形式. 集合

$$
\Theta^{*}=\left\{\varphi=\left(\varphi_1,\dots,\varphi_k\right):\int\exp\left\{\sum_{i=1}^k\varphi_i T_i\left(x\right)\right\}h\left(x\right)\,\mathrm{d}x< +\infty\right\}
$$

称为自然参数空间.

**定义 2.5.1** (充分统计量)

设样本 $X_1,X_2,\dots,X_n$ 的分布族为 $f\left(x_1,x_2,\dots,x_n,\theta\right)$, $\theta\in\Theta$, $\Theta$ 是参数空间. 设 $T=T\left(X_1,X_2,\dots,X_n\right)$ 为一统计量, 若在给定 $T$ 的条件下, 样本 $X_1,X_2,\dots,X_n$ 的条件分布与参数 $\theta$ 无关, 则称统计量 $T\left(X_1,X_2,\dots,X_n\right)$ 为参数 $\theta$ 的充分统计量.

**定理 2.5.1** (因子分解定理)

设样本 $X_1,X_2,\dots,X_n$ 的联合密度函数 (或联合分布列) 为 $f\left(x_1,x_2,\dots,x_n,\theta\right)$, 依赖于参数 $\theta$, $T=T\left(X_1,X_2,\dots,X_n\right)$ 是一个统计量, 则 $T$ 是充分统计量的充要条件是 $f\left(x_1,x_2,\dots,x_n,\theta\right)$ 可以分解为

$$
f\left(x_1,x_2,\dots,x_n,\theta\right)=g\left(T\left(x_1,x_2,\dots,x_n\right),\theta\right)h\left(x_1,\dots,x_n\right),
$$

其中 $h\left(x_1,\dots,x_n\right)$ 不依赖于参数 $\theta$.

**推论 2.5.1**

设 $T=T\left(X_1,X_2,\dots,X_n\right)$ 为 $\theta$ 的充分统计量, $S\left(T\right)$ 是单值可逆函数, 则 $S\left(T\right)$ 也是 $\theta$ 的充分统计量.

**定义 2.6.1** (完备统计量)

设 $\mathcal{F}=\left\{f\left(x;\theta\right),\theta\in\Theta\right\}$ 为一分布族, 其中 $\Theta$ 为参数空间. 设 $T=T\left(X_1,X_2,\dots,X_n\right)$ 为一统计量, 若对任何满足 $E\left[\Phi\left(T\left(X_1,X_2,\dots,X_n\right)\right)\right]=0$ 对一切 $\theta\in\Theta$ 的 $\Phi\left(\cdot\right)$, 都有 $P_\theta\left\{\Phi\left(T\left(X_1,X_2,\dots,X_n\right)\right)=0\right\}=1$ 对一切 $\theta\in\Theta$, 则称 $T\left(X_1,X_2,\dots,X_n\right)$ 为完备统计量, 或完全统计量. 若 $T$ 为完备统计量, 则它的任一可测函数 $g\left(T\right)$ 也是完备统计量.

**定理 2.6.1** (指数族中统计量的完备性)

设 $X_1,X_2,\dots,X_n$ 是从如下指数族 (自然形式) 中抽取的样本:

$$
f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k\theta_i T_i\left(x\right)\right\}h\left(x\right),\quad \theta=\left(\theta_1,\theta_2,\dots,\theta_k\right)\in\Theta^*\subseteq\mathbb R^k,
$$

若其自然参数空间 $\Theta^*$ 有内点, 则 $T\left(X_1,X_2,\dots,X_n\right)=\left(T_1\left(X_1,\dots,X_n\right),\dots,T_k\left(X_1,\dots,X_n\right)\right)$ 为完备统计量.

**定理 2.5.1** (因子分解定理)

设样本 $X_1,X_2,\dots,X_n$ 的联合密度函数 (或联合分布列) 为 $f\left(x_1,x_2,\dots,x_n;\theta\right)$, $T=T\left(X_1,X_2,\dots,X_n\right)$ 是一个统计量, 则 $T$ 为充分统计量的充要条件是 $f\left(x_1,x_2,\dots,x_n;\theta\right)$ 可以分解为

$$
f\left(x_1,x_2,\dots,x_n;\theta\right)=g\left(T\left(x_1,x_2,\dots,x_n\right),\theta\right)h\left(x_1,x_2,\dots,x_n\right),
$$

其中 $h\left(x_1,x_2,\dots,x_n\right)$ 不依赖于参数 $\theta$.

## 点估计: 矩估计与极大似然估计

**定义 3.2.1** (矩估计)

设 $\mathcal{F}=\left\{f\left(x;\theta\right):\theta\in\Theta\right\}$ 是一个参数分布族, 其中 $\theta=\left(\theta_1,\theta_2,\dots,\theta_m\right)$, $\Theta$ 为参数空间, $X_1,X_2,\dots,X_n$ 是从该分布族中抽取的样本. 假设总体的 $k$ 阶原点矩 $\alpha_k=E\left(X^k\right)$ 存在, 其作为 $\theta$ 的函数记为 $\alpha_k=\alpha_k\left(\theta_1,\theta_2,\dots,\theta_m\right)$. 令样本的 $k$ 阶原点矩为 $A_k=\frac{1}{n}\sum_{i=1}^n X_i^k$, 取 $k=1,2,\dots,m$, 令总体矩等于样本矩, 建立方程组

$$
\alpha_k\left(\theta_1,\theta_2,\dots,\theta_m\right)=A_k,\quad k=1,2,\dots,m,
$$

其解 $\hat\theta_i=\hat\theta_i\left(X_1,X_2,\dots,X_n\right)$ 即称为 $\theta_i$ 的矩估计. 也可用样本 $k$ 阶中心矩去估计总体 $k$ 阶中心矩而建立相应方程. 若要估计参数的函数 $g\left(\theta_1,\dots,\theta_m\right)$, 则以 $g\left(\hat\theta_1,\dots,\hat\theta_m\right)$ 作为其矩估计.

**例 3.2.1 结论** (总体均值与方差的矩估计)

设总体 $X$ 的均值 $\mu$ 与方差 $\sigma^2$ 都存在且未知, $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本, 则总体均值的矩估计为 $\hat\mu=\overline X=\frac{1}{n}\sum_{i=1}^n X_i$, 总体方差的矩估计为

$$
\hat\sigma^2=S_n^2=\frac{1}{n}\sum_{i=1}^n\left(X_i-\overline X\right)^2.
$$

**定义 3.3.2** (极大似然估计)

设总体的密度函数 (或分布列) 为 $f\left(x;\theta\right)$, $X_1,X_2,\dots,X_n$ 为来自该总体的样本, 其观察值为 $x_1,x_2,\dots,x_n$. 若似然函数 $L\left(\theta\right)=L\left(\theta;x_1,x_2,\dots,x_n\right)$ 在 $\hat\theta=\hat\theta\left(x_1,x_2,\dots,x_n\right)$ 处达到极大值, 即

$$
L\left(\hat\theta\right)=\sup_{\theta\in\Theta}L\left(\theta\right),
$$

则称 $\hat\theta\left(x_1,x_2,\dots,x_n\right)$ 为 $\theta$ 的极大似然估计值, 称 $\hat\theta\left(X_1,X_2,\dots,X_n\right)$ 为极大似然估计量, 简称 极大似然估计.

**似然函数与对数似然函数**

对连续型总体, 似然函数为 $L\left(\theta\right)=\prod_{i=1}^n f\left(x_i;\theta\right)$; 对离散型总体, 似然函数为 $L\left(\theta\right)=\prod_{i=1}^n P\left(X=x_i;\theta\right)$. 称

$$
\ln L\left(\theta\right)=\sum_{i=1}^n\ln f\left(x_i;\theta\right)
$$

为对数似然函数, $L\left(\theta\right)$ 与 $\ln L\left(\theta\right)$ 在同一参数处取得极值.

**极大似然估计的求法**

若似然函数关于 $\theta$ 可微, 则 $\hat\theta$ 由对数似然方程 $\frac{\mathrm{d}\ln L}{\mathrm{d}\theta}=0$ (多参数时为方程组) 求得, 当驻点唯一且为极大值点时即为 极大似然估计; 若似然函数不可微, 则按**定义 3.3.2** (极大似然估计) 直接比较似然函数在参数空间上的极大值点.

**极大似然估计的不变性**

若 $\hat\theta$ 为 $\theta$ 的 极大似然估计, $g\left(\theta\right)$ 为具有单值反函数的已知函数, 则 $g\left(\hat\theta\right)$ 为 $g\left(\theta\right)$ 的 极大似然估计.

## 估计量的评价标准

**定义 3.4.1** (无偏估计)

设 $\hat\theta=\hat\theta\left(X_1,X_2,\dots,X_n\right)$ 为未知参数 $\theta$ 的估计量, 若对任意 $\theta\in\Theta$ 都有

$$
E\left[\hat\theta\left(X_1,X_2,\dots,X_n\right)\right]=\theta,
$$

则称 $\hat\theta$ 为 $\theta$ 的无偏估计. 对 $g\left(\theta\right)$ 的估计量 $\hat g$, 若 $E\left[\hat g\right]=g\left(\theta\right)$, 则称 $\hat g$ 为 $g\left(\theta\right)$ 的无偏估计.

**定义 3.4.2** (有效性)

设 $\hat\theta_1$ 与 $\hat\theta_2$ 都是 $\theta$ 的无偏估计, 若对一切 $\theta\in\Theta$ 都有 $D\left(\hat\theta_1\right)\le D\left(\hat\theta_2\right)$, 且不等号至少对某个 $\theta$ 成立, 则称 $\hat\theta_1$ 比 $\hat\theta_2$ 有效.

**定义 3.4.3** (相合估计)

设对每个自然数 $n$, $\hat\theta_n=\hat\theta_n\left(X_1,X_2,\dots,X_n\right)$ 为 $\theta$ 的估计量, 若对任意 $\theta\in\Theta$ 及任意 $\varepsilon> 0$, 都有

$$
\lim_{n\to\infty}P\left\{\left|\hat\theta_n-\theta\right|\ge\varepsilon\right\}=0,
$$

则称 $\hat\theta_n$ 为 $\theta$ 的 (弱) 相合估计.

**基础知识** (切比雪夫不等式与大数定律)

对任意随机变量 $Y$ 及 $\varepsilon> 0$, 有 $P\left\{\left|Y-EY\right|\ge\varepsilon\right\}\le\frac{D\left(Y\right)}{\varepsilon^2}$; 独立同分布且期望存在时, 由大数定律 $\overline X_n\xrightarrow{P}E\left(X\right)$; 依概率收敛经连续函数映射保持不变.

## 一致最小方差无偏估计与克拉默-拉奥不等式

**引理 3.5.1** (改进无偏估计的方法)

设 $T=T\left(X_1,X_2,\dots,X_n\right)$ 是一个充分统计量, 而 $\hat g\left(X_1,X_2,\dots,X_n\right)$ 是 $g\left(\theta\right)$ 的一个无偏估计, 则 $h\left(T\right)=E\left[\hat g\left(X_1,X_2,\dots,X_n\right)\mid T\right]$ 是 $g\left(\theta\right)$ 的无偏估计, 且对任意 $\theta$, 有 $D\left[h\left(T\right)\right]\le D\left[\hat g\left(X_1,X_2,\dots,X_n\right)\right]$, 等号当且仅当 $\hat g\left(X_1,X_2,\dots,X_n\right)=h\left(T\right)$ 几乎处处成立.

**定理 3.5.1** (莱曼-谢弗定理)

设 $T\left(X\right)=T\left(X_1,X_2,\dots,X_n\right)$ 是充分完备统计量, 若 $g\left(T\left(X\right)\right)$ 是 $g\left(\theta\right)$ 的一个无偏估计, 则 $g\left(T\left(X\right)\right)$ 是 $g\left(\theta\right)$ 唯一的一致最小方差无偏估计.

**推论 3.5.1** (指数族自然形式下的充分完备统计量)

设样本的分布为指数族的自然形式 $f\left(x,\theta\right)=C\left(\theta\right)\exp\left\{\sum_{i=1}^k\theta_iT_i\left(x\right)\right\}h\left(x\right)$, 若自然参数空间作为 $\mathbb R^k$ 的子集有内点, 则 $T\left(X\right)=\left(T_1\left(X\right),\dots,T_k\left(X\right)\right)$ 为充分完备统计量; 此时若 $h\left(T\left(X\right)\right)$ 是 $g\left(\theta\right)$ 的无偏估计, 则它是 $g\left(\theta\right)$ 唯一的一致最小方差无偏估计.

**例 3.5.3** (两点分布的充分完备统计量)

设 $X_1,X_2,\dots,X_n$ 是来自两点分布 $B\left(1,p\right)$, $0< p< 1$ 的样本, 则 $T\left(X_1,X_2,\dots,X_n\right)=\sum_{i=1}^n X_i\sim B\left(n,p\right)$ 是 $p$ 的充分完备统计量, 且 $\overline X=\frac{1}{n}\sum_{i=1}^n X_i$ 为 $p$ 的唯一一致最小方差无偏估计.

**例 3.5.7** (正态总体的充分完备统计量)

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$, $\mu\in\mathbb R,\ \sigma^2> 0$ 的样本, 则 $T\left(X\right)=\left(\overline X,\sum_{i=1}^n\left(X_i-\overline X\right)^2\right)$ 是 $\left(\mu,\sigma^2\right)$ 的充分完备统计量, 其中 $\overline X=\frac{1}{n}\sum_{i=1}^n X_i$.

**抽样分布** (正态样本的抽样分布)

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本, 记 $\overline X=\frac{1}{n}\sum_{i=1}^n X_i$, $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\overline X\right)^2$, 则 $\overline X\sim N\left(\mu,\frac{\sigma^2}{n}\right)$, $\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$, 且 $\overline X$ 与 $S^2$ 相互独立. 特别地, 当 $\mu=0$ 时, $T=\sum_{i=1}^n X_i^2=\sigma^2\cdot\frac{\sum_{i=1}^n X_i^2}{\sigma^2}\sim\sigma^2\chi^2\left(n\right)$.

**基础知识** ($\chi^2$ 分布的矩)

若 $Y\sim\chi^2\left(k\right)$, 则 $E\left(Y\right)=k$, $D\left(Y\right)=2k$, $E\left(Y^2\right)=k\left(k+2\right)$, $E\left(\frac{1}{Y}\right)=\frac{1}{k-2}\ \left(k> 2\right)$, $E\left(\sqrt Y\right)=\sqrt 2\,\frac{\Gamma\left(\frac{k+1}{2}\right)}{\Gamma\left(\frac{k}{2}\right)}$.

**定义 3.6.1** (正则分布族)

若单参数分布族 $\mathcal F=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ 满足: (1) 参数空间 $\Theta$ 是直线上的开区间; (2) 对任意 $\theta\in\Theta$, $f\left(x,\theta\right)> 0$, 即分布的支撑与参数无关; (3) $\frac{\partial f\left(x,\theta\right)}{\partial\theta}$ 对任意 $\theta\in\Theta$ 存在; (4) $f\left(x,\theta\right)$ 的积分与微分运算可以交换; (5) 费希尔信息量存在且 $0< I\left(\theta\right)=E\left[\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right]^2< +\infty$, 则称该分布族为 克拉默-拉奥正则分布族, 其中

$$
I\left(\theta\right)=E\left[\left(\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right)^2\right]
$$

为该分布族的费希尔信息量.

**定理 3.6.1** (单参数克拉默-拉奥不等式)

设分布族 $\mathcal F=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ 是 克拉默-拉奥正则分布族, 可估函数 $g\left(\theta\right)$ 在参数空间上可微, $X_1,X_2,\dots,X_n$ 是从该总体抽取的样本, $\hat g\left(X\right)=\hat g\left(X_1,X_2,\dots,X_n\right)$ 是 $g\left(\theta\right)$ 的任一无偏估计, 且积分可在积分号下对 $\theta$ 求导, 则有

$$
D\left[\hat g\left(X\right)\right]\ge\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)}.
$$

右端 $\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)}$ 称为 克拉默-拉奥下界. 若某一无偏估计达到该下界, 则它必为一致最小方差无偏估计.

**定义 3.6.2** (效率)

设 $\hat g\left(X\right)$ 为 $g\left(\theta\right)$ 的无偏估计, 则比值

$$
e\left(\theta\right)=\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)D\left[\hat g\left(X\right)\right]}
$$

称为无偏估计 $\hat g\left(X\right)$ 的效率, 其中 $0< e\left(\theta\right)\le1$.

**定义 3.6.3** (有效估计)

当 $e\left(\theta\right)\equiv1$ 时, 称 $\hat g\left(X\right)$ 为 $g\left(\theta\right)$ 的有效估计. 有效估计一定是一致最小方差无偏估计.

**推论 3.5.1** (指数族自然形式下的充分完备统计量)

设样本的分布为指数族的自然形式, 若自然参数空间有内点, 则 $T\left(X\right)$ 为充分完备统计量; 此时若 $h\left(T\left(X\right)\right)$ 是 $g\left(\theta\right)$ 的无偏估计, 则由**定理 3.5.1** (莱曼-谢弗定理) , 它是 $g\left(\theta\right)$ 唯一的一致最小方差无偏估计.

**抽样分布** (正态样本的抽样分布)

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本, 则 $\overline X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right)$. 特别地, 当 $\sigma^2=1$ 时, $\overline X\sim N\left(\mu,\frac{1}{n}\right)$.

## 区间估计

**定义 4.1.1** (区间估计)

设 $\mathcal{F}=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ 是一个参数分布族, 其中 $\Theta$ 为参数空间, $g\left(\theta\right)$ 是定义在 $\Theta$ 上的一个已知函数, $X_1,X_2,\dots,X_n$ 是从分布族 $\mathcal{F}$ 中的某总体抽取的样本. 令 $g_1\left(X_1,X_2,\dots,X_n\right)$ 和 $g_2\left(X_1,X_2,\dots,X_n\right)$ 是定义在样本空间上的函数, 并且满足

$$
g_1\left(X_1,X_2,\dots,X_n\right)\le g_2\left(X_1,X_2,\dots,X_n\right),
$$

则称随机区间

$$
\left[g_1\left(X_1,X_2,\dots,X_n\right),g_2\left(X_1,X_2,\dots,X_n\right)\right]
$$

是 $g\left(\theta\right)$ 的一个区间估计.

**定义 4.1.4** (置信区间)

设

$$
\left[\theta_1\left(X_1,X_2,\dots,X_n\right),\theta_2\left(X_1,X_2,\dots,X_n\right)\right]
$$

是参数 $\theta$ 的一个区间估计. 对给定 $0< \alpha< 1$, 如果对于任意的 $\theta\in\Theta$, 都有

$$
P_\theta\left\{\theta_1\left(X_1,X_2,\dots,X_n\right)\le\theta\le\theta_2\left(X_1,X_2,\dots,X_n\right)\right\}\ge1-\alpha
$$

成立, 则称 $\left[\theta_1,\theta_2\right]$ 是参数 $\theta$ 的置信水平为 $1-\alpha$ 的置信区间.

**定义 4.1.5** (置信限)

设 $\theta_L\left(X_1,X_2,\dots,X_n\right)$ 和 $\theta_U\left(X_1,X_2,\dots,X_n\right)$ 是定义在样本空间上取值在参数空间的统计量, 给定 $0< \alpha< 1$, 对任意的 $\theta\in\Theta$ 都有 $P_\theta\left\{\theta\ge\theta_L\right\}\ge1-\alpha$ 和 $P_\theta\left\{\theta\le\theta_U\right\}\ge1-\alpha$ 成立, 则称 $\theta_L$ 和 $\theta_U$ 是参数 $\theta$ 的置信水平为 $1-\alpha$ 的单侧置信下限和单侧置信上限.

**抽样分布** (正态样本的抽样分布)

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本, 则 $\overline X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right)$, 从而 $\frac{\sqrt n\left(\overline X-\mu\right)}{\sigma}\sim N\left(0,1\right)$. 当 $\sigma^2$ 未知时, $\frac{\sqrt n\left(\overline X-\mu\right)}{S}\sim t\left(n-1\right)$, 其中 $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\overline X\right)^2$ 为样本方差.

**定义 4.2.1** (枢轴量)

令 $G\left(X_1,X_2,\dots,X_n,\theta\right)$ 是样本 $\left(X_1,X_2,\dots,X_n\right)$ 和参数 $\theta$ 的一个可测函数, 当且仅当 $G\left(X_1,X_2,\dots,X_n,\theta\right)$ 的分布不依赖于参数 $\theta$ 时, $G\left(X_1,X_2,\dots,X_n,\theta\right)$ 被称为枢轴量.

**定理** (单个正态总体均值的置信区间)

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本, $\overline X=\frac{1}{n}\sum_{i=1}^n X_i$, $S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\overline X\right)^2$. 当 $\sigma^2$ 已知时, $\mu$ 的置信水平为 $1-\alpha$ 的置信区间为

$$
\left[\overline X-\frac{\sigma}{\sqrt n}u_{\alpha/2},\overline X+\frac{\sigma}{\sqrt n}u_{\alpha/2}\right];
$$

当 $\sigma^2$ 未知时, $\mu$ 的置信水平为 $1-\alpha$ 的置信区间为

$$
\left[\overline X-\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right),\overline X+\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right)\right].
$$

**定理** (单个正态总体方差的置信区间)

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本, 当 $\mu$ 未知时, $\sigma^2$ 的置信水平为 $1-\alpha$ 的置信区间为

$$
\left[\frac{\left(n-1\right)S^2}{\chi^2_{\alpha/2}\left(n-1\right)},\frac{\left(n-1\right)S^2}{\chi^2_{1-\alpha/2}\left(n-1\right)}\right],
$$

其中 $\chi^2_\alpha\left(n-1\right)$ 表示自由度为 $n-1$ 的 $\chi^2$ 分布的上 $\alpha$ 分位数. 相应地, $\sigma$ 的置信水平为 $1-\alpha$ 的置信区间为上述区间端点的平方根.

**定理** (两个正态总体均值差的置信区间)

设 $X_1,X_2,\dots,X_m$ 是来自 $N\left(\mu_1,\sigma_1^2\right)$ 的样本, $Y_1,Y_2,\dots,Y_n$ 是来自 $N\left(\mu_2,\sigma_2^2\right)$ 的样本, 两样本独立, $\overline X,\overline Y$ 为样本均值, $S_1^2,S_2^2$ 为样本方差. 当 $\sigma_1^2,\sigma_2^2$ 均已知时, $\mu_2-\mu_1$ 的置信区间为

$$
\left[\overline Y-\overline X-u_{\alpha/2}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}},\overline Y-\overline X+u_{\alpha/2}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}\right];
$$

当 $\sigma_1^2=\sigma_2^2=\sigma^2$ 未知时, $\mu_2-\mu_1$ 的置信区间为

$$
\left[\overline Y-\overline X-S_w t_{\alpha/2}\left(m+n-2\right)\sqrt{\frac{1}{m}+\frac{1}{n}},\overline Y-\overline X+S_w t_{\alpha/2}\left(m+n-2\right)\sqrt{\frac{1}{m}+\frac{1}{n}}\right],
$$

其中 $S_w^2=\frac{\left(m-1\right)S_1^2+\left(n-1\right)S_2^2}{m+n-2}$; 当 $\sigma_1^2\ne\sigma_2^2$ 未知时, 可用 韦尔奇近似:

$$
\left[\overline Y-\overline X-t_{\alpha/2}\left(r\right)\sqrt{\frac{S_1^2}{m}+\frac{S_2^2}{n}},\overline Y-\overline X+t_{\alpha/2}\left(r\right)\sqrt{\frac{S_1^2}{m}+\frac{S_2^2}{n}}\right],
$$

其中 $r=\frac{\left(S_1^2/m+S_2^2/n\right)^2}{\frac{\left(S_1^2/m\right)^2}{m-1}+\frac{\left(S_2^2/n\right)^2}{n-1}}$.

**定理** (两个正态总体方差比的置信区间)

设两总体均值均未知, 则 $\frac{\sigma_1^2}{\sigma_2^2}$ 的置信水平为 $1-\alpha$ 的置信区间为

$$
\left[\frac{S_1^2/S_2^2}{F_{\alpha/2}\left(m-1,n-1\right)},\frac{S_1^2/S_2^2}{F_{1-\alpha/2}\left(m-1,n-1\right)}\right],
$$

其中 $F_{\alpha/2}\left(m-1,n-1\right)$ 表示 $F$ 分布的上 $\alpha/2$ 分位数.

**枢轴量法** (置信区间的构造)

设 $X_1,X_2,\dots,X_n$ 是来自总体的样本, 未知参数为 $\theta$. 若能构造出一个样本与 $\theta$ 的函数 $G\left(X_1,X_2,\dots,X_n,\theta\right)$, 其分布完全已知且与 $\theta$ 无关, 则称 $G$ 为枢轴量. 对给定置信水平 $1-\alpha$, 选取 $c_1,c_2$ 使 $P\left\{c_1\le G\le c_2\right\}=1-\alpha$, 再将不等式 $c_1\le G\le c_2$ 等价变形为 $\hat\theta_1\le\theta\le\hat\theta_2$, 即得 $\theta$ 的置信水平为 $1-\alpha$ 的置信区间 $\left[\hat\theta_1,\hat\theta_2\right]$.

**指数分布参数的置信区间**

设 $X_1,X_2,\dots,X_n$ 是来自指数分布总体 $E\left(\lambda\right)$ 的样本, 其密度函数为 $f\left(x\right)=\lambda e^{-\lambda x},\ x> 0$. 由 $\chi^2$ 分布的可加性, 枢轴量为

$$
T=2\lambda\sum_{i=1}^n X_i=2n\lambda\overline X\sim\chi^2\left(2n\right).
$$

由此均值 $\theta=\frac{1}{\lambda}$ 的置信水平为 $1-\alpha$ 的置信区间为

$$
\left[\frac{2n\overline X}{\chi^2_{\alpha/2}\left(2n\right)},\ \frac{2n\overline X}{\chi^2_{1-\alpha/2}\left(2n\right)}\right],
$$

其中 $\chi^2_{\alpha/2}\left(2n\right)$ 与 $\chi^2_{1-\alpha/2}\left(2n\right)$ 分别为自由度 $2n$ 的 $\chi^2$ 分布的上 $\alpha/2$ 与上 $1-\alpha/2$ 分位数.

**大样本方法** (两点分布参数的近似置信区间)

设 $X_1,X_2,\dots,X_n$ 是来自两点分布 $B\left(1,p\right)$ 的样本, $\overline X$ 为样本均值. 由中心极限定理, 当 $n$ 充分大时 $\frac{\overline X-p}{\sqrt{p\left(1-p\right)/n}}\overset{\mathrm{d}}{\to}N\left(0,1\right)$. 用 $\overline X$ 估计 $p$, 得参数 $p$ 的置信水平近似为 $1-\alpha$ 的置信区间

$$
\left[\overline X-u_{\alpha/2}\sqrt{\frac{\overline X\left(1-\overline X\right)}{n}},\ \overline X+u_{\alpha/2}\sqrt{\frac{\overline X\left(1-\overline X\right)}{n}}\right],
$$

其中 $u_{\alpha/2}$ 为标准正态分布的上 $\alpha/2$ 分位数.

## 假设检验

**定义 5.1.1** (功效函数)

设 $\varphi\left(x\right)$ 是假设检验问题 $H_0:\theta\in\Theta_0$; $H_1:\theta\in\Theta_1$ 的一个检验函数, 则函数

$$
\beta\left(\theta\right)=P_\theta\left\{\text{检验函数拒绝原假设 }H_0\right\}=E_\theta\left[\varphi\left(X\right)\right],\ \theta\in\Theta,
$$

称为该检验的功效函数 (效函数或势函数) . 对非随机化检验, $\beta\left(\theta\right)$ 即参数为 $\theta$ 时样本落入拒绝域的概率, 亦即拒绝原假设 $H_0$ 的概率.

**两类错误** (第一类错误与第二类错误)

当原假设 $H_0$ 为真时却拒绝 $H_0$, 称为犯**第一类错误** (弃真错误) , 其概率为 $\beta\left(\theta\right),\ \theta\in\Theta_0$; 当 $H_0$ 不真时却接受 $H_0$, 称为犯**第二类错误** (取伪错误) , 其概率为 $1-\beta\left(\theta\right),\ \theta\in\Theta_1$.

**定义 5.1.2** (显著性检验与检验水平)

若检验函数 $\varphi\left(x\right)$ 犯第一类错误的概率总不超过 $\alpha$, 即 $\beta\left(\theta\right)\le\alpha,\ \theta\in\Theta_0$, 则称 $\alpha$ 为该检验的一个水平, 称 $\varphi$ 为显著性水平为 $\alpha$ 的检验, 简称水平为 $\alpha$ 的检验.

**抽样分布** (正态样本均值的分布)

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本, 则样本均值

$$
\overline X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right).
$$

**U检验法** (方差已知时单个正态总体均值的检验)

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本, 其中 $\sigma^2=\sigma_0^2$ 已知, $\mu$ 未知. 对给定显著性水平 $\alpha$, 取检验统计量

$$
U=\frac{\overline X-\mu_0}{\sigma_0/\sqrt n},
$$

当 $H_0:\mu=\mu_0$ 成立时 $U\sim N\left(0,1\right)$. 三种检验问题的拒绝域分别为: 双边检验 $H_0:\mu=\mu_0,\ H_1:\mu\ne\mu_0$ 的拒绝域为 $\left\lvert U\right\rvert\ge u_{\alpha/2}$; 右边检验 $H_0:\mu\le\mu_0,\ H_1:\mu> \mu_0$ 的拒绝域为 $U\ge u_\alpha$; 左边检验 $H_0:\mu\ge\mu_0,\ H_1:\mu< \mu_0$ 的拒绝域为 $U\le-u_\alpha$.

**t检验法** (方差未知时单个正态总体均值的检验)

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本, 其中 $\sigma^2$ 未知. 对给定显著性水平 $\alpha$, 取检验统计量

$$
T=\frac{\overline X-\mu_0}{S/\sqrt n},
$$

当 $H_0:\mu=\mu_0$ 成立时 $T\sim t\left(n-1\right)$. 双边检验的拒绝域为 $\left\lvert T\right\rvert\ge t_{\alpha/2}\left(n-1\right)$; 右边检验的拒绝域为 $T\ge t_\alpha\left(n-1\right)$; 左边检验的拒绝域为 $T\le-t_\alpha\left(n-1\right)$.

**$\chi^2$检验法** (单个正态总体方差的检验)

设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本, 其中 $\mu$ 未知. 对给定显著性水平 $\alpha$, 取检验统计量

$$
\chi^2=\frac{\left(n-1\right)S^2}{\sigma_0^2},
$$

当 $H_0:\sigma^2=\sigma_0^2$ 成立时 $\chi^2\sim\chi^2\left(n-1\right)$. 双边检验 $H_0:\sigma^2=\sigma_0^2,\ H_1:\sigma^2\ne\sigma_0^2$ 的拒绝域为 $\chi^2\le\chi^2_{1-\alpha/2}\left(n-1\right)$ 或 $\chi^2\ge\chi^2_{\alpha/2}\left(n-1\right)$; 右边检验 $H_0:\sigma^2\le\sigma_0^2,\ H_1:\sigma^2> \sigma_0^2$ 的拒绝域为 $\chi^2\ge\chi^2_\alpha\left(n-1\right)$; 左边检验 $H_0:\sigma^2\ge\sigma_0^2,\ H_1:\sigma^2< \sigma_0^2$ 的拒绝域为 $\chi^2\le\chi^2_{1-\alpha}\left(n-1\right)$.

**两正态总体均值差的U检验** (方差均已知)

设 $X_1,X_2,\dots,X_m$ 来自 $N\left(\mu_1,\sigma_1^2\right)$, $Y_1,Y_2,\dots,Y_n$ 来自 $N\left(\mu_2,\sigma_2^2\right)$, 两样本独立, 其中 $\sigma_1^2,\sigma_2^2$ 均已知. 取检验统计量

$$
U=\frac{\overline X-\overline Y}{\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}},
$$

当 $H_0:\mu_1=\mu_2$ 成立时 $U\sim N\left(0,1\right)$. 双边检验拒绝域为 $\left\lvert U\right\rvert\ge u_{\alpha/2}$; 右边检验 $H_0:\mu_1\le\mu_2,\ H_1:\mu_1> \mu_2$ 的拒绝域为 $U\ge u_\alpha$.

**两正态总体均值差的合并t检验** (方差未知但相等)

设 $X_1,X_2,\dots,X_m$ 来自 $N\left(\mu_1,\sigma^2\right)$, $Y_1,Y_2,\dots,Y_n$ 来自 $N\left(\mu_2,\sigma^2\right)$, 两样本独立, 其中 $\sigma^2$ 未知. 取合并样本方差

$$
S_w^2=\frac{\left(m-1\right)S_1^2+\left(n-1\right)S_2^2}{m+n-2},
$$

检验统计量为

$$
T=\frac{\overline X-\overline Y}{S_w\sqrt{\frac1m+\frac1n}},
$$

当 $H_0:\mu_1=\mu_2$ 成立时 $T\sim t\left(m+n-2\right)$. 双边检验拒绝域为 $\left\lvert T\right\rvert\ge t_{\alpha/2}\left(m+n-2\right)$; 右边检验拒绝域为 $T\ge t_\alpha\left(m+n-2\right)$.

**F检验法** (两正态总体方差比的检验)

设 $X_1,X_2,\dots,X_m$ 来自 $N\left(\mu_1,\sigma_1^2\right)$, $Y_1,Y_2,\dots,Y_n$ 来自 $N\left(\mu_2,\sigma_2^2\right)$, 两样本独立, 其中 $\mu_1,\mu_2$ 未知. 取检验统计量

$$
F=\frac{S_1^2}{S_2^2},
$$

当 $H_0:\sigma_1^2=\sigma_2^2$ 成立时 $F\sim F\left(m-1,n-1\right)$. 双边检验 $H_0:\sigma_1^2=\sigma_2^2,\ H_1:\sigma_1^2\ne\sigma_2^2$ 的拒绝域为 $F\le F_{1-\alpha/2}\left(m-1,n-1\right)$ 或 $F\ge F_{\alpha/2}\left(m-1,n-1\right)$.

**指数分布参数的假设检验** (小样本方法)

设总体 $X\sim E\left(\lambda\right)$, 其密度函数为 $f\left(x\right)=\lambda e^{-\lambda x}\left(x> 0\right)$, 其中 $\lambda> 0$ 未知, $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本. 由**定理 2.3.8**, 有 $2n\lambda\overline X\sim\chi^2\left(2n\right)$. 对检验问题 $H_0:\lambda=\lambda_0,\ H_1:\lambda\ne\lambda_0$, 拒绝域为

$$
D=\left\{2n\lambda_0\overline X\le\chi^2_{1-\alpha/2}\left(2n\right)\ \text{或}\ 2n\lambda_0\overline X\ge\chi^2_{\alpha/2}\left(2n\right)\right\};
$$

对检验问题 $H_0:\lambda\le\lambda_0,\ H_1:\lambda> \lambda_0$, 拒绝域为

$$
D=\left\{2n\lambda_0\overline X\le\chi^2_{1-\alpha}\left(2n\right)\right\};
$$

对检验问题 $H_0:\lambda\ge\lambda_0,\ H_1:\lambda< \lambda_0$, 拒绝域为

$$
D=\left\{2n\lambda_0\overline X\ge\chi^2_\alpha\left(2n\right)\right\}.
$$

**两指数分布参数比的检验**

设 $X_1,X_2,\dots,X_m$ 来自 $E\left(\lambda_1\right)$, $Y_1,Y_2,\dots,Y_n$ 来自 $E\left(\lambda_2\right)$, 两样本独立. 由 $2m\lambda_1\overline X\sim\chi^2\left(2m\right)$ 与 $2n\lambda_2\overline Y\sim\chi^2\left(2n\right)$ 相互独立, 构造 $F$ 统计量. 当 $H_0:\lambda_1=\lambda_2$ 成立时, 有

$$
\frac{\overline X}{\overline Y}\sim F\left(2m,2n\right).
$$

双边检验 $H_0:\lambda_1=\lambda_2,\ H_1:\lambda_1\ne\lambda_2$ 的拒绝域为

$$
D=\left\{\frac{\overline X}{\overline Y}\le F_{1-\alpha/2}\left(2m,2n\right)\ \text{或}\ \frac{\overline X}{\overline Y}\ge F_{\alpha/2}\left(2m,2n\right)\right\}.
$$

**大样本方法** (二项分布参数 $p$ 的检验)

设 $X_1,X_2,\dots,X_n$ 来自两点分布总体 $B\left(1,p\right)$, $0< p< 1$ 未知. 当 $n$ 充分大 (一般要求 $n\ge30$) 时, 由中心极限定理, 在 $H_0:p=p_0$ 成立时, 有

$$
U=\frac{\overline X-p_0}{\sqrt{\frac{p_0\left(1-p_0\right)}{n}}}\overset{\text{近似}}{\sim}N\left(0,1\right).
$$

双边检验 $H_0:p=p_0,\ H_1:p\ne p_0$ 的拒绝域为 $\left\lvert U\right\rvert\ge u_{\alpha/2}$; 右边检验 $H_0:p\le p_0,\ H_1:p> p_0$ 的拒绝域为 $U\ge u_\alpha$; 左边检验 $H_0:p\ge p_0,\ H_1:p< p_0$ 的拒绝域为 $U\le-u_\alpha$.

**大样本方法** (泊松分布参数 $\lambda$ 的检验)

设 $X_1,X_2,\dots,X_n$ 来自泊松分布总体 $P\left(\lambda\right)$, $\lambda> 0$ 未知. 由 $S=\sum_{i=1}^nX_i\sim P\left(n\lambda\right)$, $E\left(S\right)=n\lambda$, $D\left(S\right)=n\lambda$. 当 $H_0:\lambda=\lambda_0$ 成立时, 由中心极限定理, 有

$$
U=\frac{S-n\lambda_0}{\sqrt{n\lambda_0}}\overset{\text{近似}}{\sim}N\left(0,1\right),
$$

即 $U=\frac{\overline X-\lambda_0}{\sqrt{\lambda_0/n}}\overset{\text{近似}}{\sim}N\left(0,1\right)$. 双边检验 $H_0:\lambda=\lambda_0,\ H_1:\lambda\ne\lambda_0$ 的拒绝域为 $\left\lvert U\right\rvert\ge u_{\alpha/2}$.

