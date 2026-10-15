# 作业 1

> **定义 1.2.1**（总体）<br>数理统计中，把所研究问题涉及的研究对象的全体称为总体. 组成总体的每个元素称为个体. 总体中所包含个体的个数称为总体容量. 实际问题中，总体可用一个随机变量 $X$ 及其分布来描述，对总体的研究转化为对表示总体的随机变量 $X$ 的统计规律性的研究，因此今后不区分总体与相应的随机变量，统称为总体 $X$.

> **定义 1.3.1**（样本空间）<br>样本 $X_1,X_2,\dots,X_n$ 可能取值的全体的集合，称为样本空间.

> **定义 1.3.2**（简单随机样本）<br>设有一总体 $X$，具有分布 $F$，$X_1,X_2,\dots,X_n$ 是从总体 $X$ 中抽取的容量为 $n$ 的样本. 若<br>(1) $X_1,X_2,\dots,X_n$ 相互独立;<br>(2) $X_1,X_2,\dots,X_n$ 与总体 $X$ 有相同的分布 $F$，<br>则称 $X_1,X_2,\dots,X_n$ 是从总体 $X$ 中抽取的容量为 $n$ 的简单随机样本，简称样本.

> **样本分布**（联合分布函数、联合分布列与联合密度函数）<br>设总体 $X$ 的分布函数为 $F\left(x\right)$，$X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，则样本的联合分布函数为 $$F^{*}\left(x_1,x_2,\dots,x_n\right)=\prod_{i=1}^n F\left(x_i\right).$$ 若总体 $X$ 是离散型随机变量，分布列为 $P\left\{X=a_i\right\}=p_i$，则样本 $X_1,X_2,\dots,X_n$ 的联合分布列为 $$P\left\{X_1=x_1,\dots,X_n=x_n\right\}=\prod_{i=1}^n p_{x_i}.$$ 若总体 $X$ 是连续型随机变量，密度函数为 $f\left(x\right)$，则样本 $X_1,X_2,\dots,X_n$ 的联合密度函数为 $$f^{*}\left(x_1,x_2,\dots,x_n\right)=\prod_{i=1}^n f\left(x_i\right).$$

> **定义 1.3.3**（参数空间）<br>数理统计中，称出现在总体分布或样本分布中的未知常数为参数. 参数 $\theta$ 所有可能取值的全体构成的集合，称为参数空间，记为 $\Theta$.

> **总体分布族与样本分布族**<br>由于不同的参数值一般对应于不同的总体分布，参数空间中所有可能的参数值对应于一族总体分布，称该分布族为总体分布族，记为 $\left\{f\left(x;\theta\right):\theta\in\Theta\right\}$. 不同的参数值也一般对应于不同的样本分布，参数空间中所有可能的参数值对应于一族样本分布，称该分布族为样本分布族，记为 $$\left\{\prod_{i=1}^n f\left(x_i;\theta\right):\theta\in\Theta\right\}.$$

> **定义 1.4.1**（统计量）<br>设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，$g\left(X_1,X_2,\dots,X_n\right)$ 是样本 $X_1,X_2,\dots,X_n$ 的函数，且除依赖于样本外，不依赖于任何其他的未知量，则称 $g\left(X_1,X_2,\dots,X_n\right)$ 为统计量. 若 $x_1,x_2,\dots,x_n$ 为样本 $X_1,X_2,\dots,X_n$ 的观察值，称 $g\left(x_1,x_2,\dots,x_n\right)$ 为统计量 $g\left(X_1,X_2,\dots,X_n\right)$ 的一个观察值. 统计量只与样本有关，不依赖任何未知参数.

> **定义 1.5.1**（经验分布函数）<br>设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，$X_{\left(1\right)}\le X_{\left(2\right)}\le\dots\le X_{\left(n\right)}$ 为其顺序统计量，对任意实数 $x$，称 $$F_n\left(x\right)=\begin{cases}0,&x<X_{\left(1\right)},\\\frac{r}{n},&X_{\left(r\right)}\le x<X_{\left(r+1\right)},\ r=1,2,\dots,n-1,\\1,&x\ge X_{\left(n\right)}\end{cases}$$ 为样本 $X_1,X_2,\dots,X_n$ 的经验分布函数.

### 习题一

（习题 1-1）什么是总体？什么是样本？

### 解答 习题一

由**定义 1.2.1**（总体），数理统计中，把所研究问题涉及的研究对象的全体称为总体，组成总体的每个元素称为个体. 由第 1 章绪论，从总体中随机抽取一部分个体进行观测的过程称为抽样，抽取的部分个体称为样本. 具体地，设 $X_1,X_2,\dots,X_n$ 是从总体 $X$ 中抽取的样本，由**定义 1.3.2**（简单随机样本），这些个体应与总体 $X$ 同分布且相互独立. $\blacksquare$

### 习题二

（习题 1-2）简单随机样本应满足什么条件？

### 解答 习题二

由**定义 1.3.2**（简单随机样本），设有一总体 $X$，具有分布 $F$，$X_1,X_2,\dots,X_n$ 是从总体 $X$ 中抽取的容量为 $n$ 的样本. 若 $X_1,X_2,\dots,X_n$ 满足：

(1) $X_1,X_2,\dots,X_n$ 相互独立;

(2) $X_1,X_2,\dots,X_n$ 与总体 $X$ 有相同的分布 $F$，

则称其为简单随机样本. 即简单随机样本应满足**独立性**与**代表性**（同分布）两个条件. $\blacksquare$

### 习题三

（习题 1-4）设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，在下列三种情况下，分别写出样本 $X_1,X_2,\dots,X_n$ 的联合分布列或联合密度函数：

(1) 总体 $X$ 服从几何分布，其分布列为 $P\left\{X=x\right\}=\left(1-p\right)^{x-1}p,\ 0<p<1,\ x=1,2,\dots$;

(2) 总体 $X$ 服从指数分布，其密度函数为 $f\left(x\right)=\lambda e^{-\lambda x},\ x>0$（$x\le0$ 时为 $0$），其中 $\lambda>0$;

(3) 总体 $X$ 的密度函数为 $f\left(x\right)=\frac{\lambda}{2}e^{-\lambda\left|x\right|},\ -\infty<x<+\infty$，其中 $\lambda>0$.

### 解答 习题三

由**样本分布**（联合分布列与联合密度函数），若总体 $X$ 的分布列为 $P\left\{X=x\right\}$，则样本的联合分布列为 $\prod_{i=1}^n P\left\{X=x_i\right\}$；若总体 $X$ 的密度函数为 $f\left(x\right)$，则样本的联合密度函数为 $\prod_{i=1}^n f\left(x_i\right)$.

(1) 总体 $X$ 服从几何分布 $P\left\{X=x\right\}=\left(1-p\right)^{x-1}p$，故样本的联合分布列为
$$
P\left\{X_1=x_1,\dots,X_n=x_n\right\}=\prod_{i=1}^n\left(1-p\right)^{x_i-1}p=p^n\left(1-p\right)^{\sum_{i=1}^n x_i-n},\quad x_i=1,2,\dots
$$

(2) 总体 $X$ 服从指数分布 $f\left(x\right)=\lambda e^{-\lambda x}$，故样本的联合密度函数为
$$
f\left(x_1,\dots,x_n\right)=\prod_{i=1}^n\lambda e^{-\lambda x_i}=\lambda^n e^{-\lambda\sum_{i=1}^n x_i},\quad x_i>0.
$$

(3) 总体 $X$ 的密度函数为 $f\left(x\right)=\frac{\lambda}{2}e^{-\lambda\left|x\right|}$，故样本的联合密度函数为
$$
f\left(x_1,\dots,x_n\right)=\prod_{i=1}^n\frac{\lambda}{2}e^{-\lambda\left|x_i\right|}=\left(\frac{\lambda}{2}\right)^n e^{-\lambda\sum_{i=1}^n\left|x_i\right|},\quad x_i\in\mathbb R.
$$

$\blacksquare$

### 习题四

（习题 1-6）设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，写出两点分布、二项分布、泊松分布、几何分布、均匀分布、指数分布、正态分布的样本分布族.

### 解答 习题四

由**总体分布族与样本分布族**，样本分布族为 $\left\{\prod_{i=1}^n f\left(x_i;\theta\right):\theta\in\Theta\right\}$，其中 $f\left(x;\theta\right)$ 为总体的分布列（或密度函数），$\Theta$ 为参数空间（**定义 1.3.3**）.

(1) 两点分布 $B\left(1,p\right)$，参数空间 $\Theta=\left\{p:0<p<1\right\}$：样本分布族为
$$
\left\{\prod_{i=1}^n p^{x_i}\left(1-p\right)^{1-x_i}:0<p<1\right\},\quad x_i\in\left\{0,1\right\}.
$$

(2) 二项分布 $B\left(m,p\right)$，参数空间 $\Theta=\left\{p:0<p<1\right\}$：样本分布族为
$$
\left\{\prod_{i=1}^n\binom{m}{x_i}p^{x_i}\left(1-p\right)^{m-x_i}:0<p<1\right\},\quad x_i=0,1,\dots,m.
$$

(3) 泊松分布 $P\left(\lambda\right)$，参数空间 $\Theta=\left\{\lambda:\lambda>0\right\}$：样本分布族为
$$
\left\{\prod_{i=1}^n\frac{e^{-\lambda}\lambda^{x_i}}{x_i!}:\lambda>0\right\},\quad x_i=0,1,2,\dots
$$

(4) 几何分布 $G\left(p\right)$，参数空间 $\Theta=\left\{p:0<p<1\right\}$：样本分布族为
$$
\left\{\prod_{i=1}^n\left(1-p\right)^{x_i-1}p:0<p<1\right\},\quad x_i=1,2,\dots
$$

(5) 均匀分布 $U\left[a,b\right]$，参数空间 $\Theta=\left\{\left(a,b\right):-\infty<a<b<+\infty\right\}$：样本分布族为
$$
\left\{\prod_{i=1}^n\frac{1}{b-a}:-\infty<a<b<+\infty\right\},\quad x_i\in\left[a,b\right].
$$

(6) 指数分布 $E\left(\lambda\right)$，参数空间 $\Theta=\left\{\lambda:\lambda>0\right\}$：样本分布族为
$$
\left\{\prod_{i=1}^n\lambda e^{-\lambda x_i}:\lambda>0\right\},\quad x_i>0.
$$

(7) 正态分布 $N\left(\mu,\sigma^2\right)$，参数空间 $\Theta=\left\{\left(\mu,\sigma^2\right):\mu\in\mathbb R,\ \sigma>0\right\}$：样本分布族为
$$
\left\{\prod_{i=1}^n\frac{1}{\sqrt{2\pi}\sigma}\exp\left\{-\frac{\left(x_i-\mu\right)^2}{2\sigma^2}\right\}:\mu\in\mathbb R,\ \sigma>0\right\},\quad x_i\in\mathbb R.
$$

$\blacksquare$

### 习题五

（习题 1-7）某机床加工出的零件的直径服从正态分布 $N\left(\mu,\sigma^2\right)$，其中 $\mu,\sigma^2$ 均未知. 为对 $\mu,\sigma^2$ 做出估计，随机选取加工出来的 $n$ 个零件进行测量，得到 $n$ 个数据 $x_1,x_2,\dots,x_n$. 试写出该问题的统计模型（即参数空间和样本分布族）.

### 解答 习题五

由**定义 1.3.3**（参数空间），参数为 $\theta=\left(\mu,\sigma^2\right)$，其取值范围即参数空间为
$$
\Theta=\left\{\left(\mu,\sigma^2\right):\mu\in\mathbb R,\ \sigma^2>0\right\}.
$$

由**总体分布族与样本分布族**，正态总体 $N\left(\mu,\sigma^2\right)$ 的密度函数为 $f\left(x;\mu,\sigma^2\right)=\frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{\left(x-\mu\right)^2}{2\sigma^2}}$，故样本分布族为
$$
\left\{\prod_{i=1}^n\frac{1}{\sqrt{2\pi}\sigma}\exp\left\{-\frac{\left(x_i-\mu\right)^2}{2\sigma^2}\right\}:\left(\mu,\sigma^2\right)\in\Theta\right\},\quad x_i\in\mathbb R.
$$

$\blacksquare$

### 习题六

（习题 1-8）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，其中 $\mu$ 已知，$\sigma^2$ 未知，判断下列量哪些是统计量哪些不是统计量，为什么？
$$
\frac{1}{n}\sum_{i=1}^n X_i,\quad\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2,\quad\frac{1}{\sigma^2}\sum_{i=1}^n X_i^2,\quad\frac{1}{n}\sum_{i=1}^n\left(X_i-\mu\right)^2,
$$
$$
\frac{1}{\sigma^2}\sum_{i=1}^n\left(X_i-\mu\right)^2,\quad X_1+2\mu,\quad\max\left\{X_1,\dots,X_n\right\},\quad\min\left\{X_1,\dots,X_n\right\}.
$$

### 解答 习题六

由**定义 1.4.1**（统计量），统计量是样本的函数，且除样本外不依赖于任何未知量. 本题中 $\mu$ 已知，$\sigma^2$ 未知，故凡含未知参数 $\sigma^2$ 的量不是统计量，其余为统计量.

- $\frac{1}{n}\sum_{i=1}^n X_i$：只含样本，是统计量.
- $\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$：只含样本（$\bar X$ 为样本均值），是统计量.
- $\frac{1}{\sigma^2}\sum_{i=1}^n X_i^2$：含未知参数 $\sigma^2$，不是统计量.
- $\frac{1}{n}\sum_{i=1}^n\left(X_i-\mu\right)^2$：$\mu$ 已知，只含样本与已知常数，是统计量.
- $\frac{1}{\sigma^2}\sum_{i=1}^n\left(X_i-\mu\right)^2$：含未知参数 $\sigma^2$，不是统计量.
- $X_1+2\mu$：$\mu$ 已知，是统计量.
- $\max\left\{X_1,\dots,X_n\right\}$：只含样本，是统计量.
- $\min\left\{X_1,\dots,X_n\right\}$：只含样本，是统计量.

$\blacksquare$

### 习题七

（习题 1-9）对三年级的 10 个孩子做阅读能力测试，分数如下：$95,86,78,90,62,73,89,92,84,76$. 求相应的经验分布函数，并绘出经验分布函数的图形.

### 解答 习题七

由**定义 1.5.1**（经验分布函数），先将样本观察值按从小到大排序为
$$
x_{\left(1\right)}=62,\ x_{\left(2\right)}=73,\ x_{\left(3\right)}=76,\ x_{\left(4\right)}=78,\ x_{\left(5\right)}=84,\ x_{\left(6\right)}=86,\ x_{\left(7\right)}=89,\ x_{\left(8\right)}=90,\ x_{\left(9\right)}=92,\ x_{\left(10\right)}=95.
$$

则经验分布函数 $F_{10}\left(x\right)$ 为在每处顺序统计量上跳跃 $\frac{1}{10}$ 的右连续阶梯函数：
$$
F_{10}\left(x\right)=\begin{cases}0,&x<62,\\\frac{1}{10},&62\le x<73,\\\frac{2}{10},&73\le x<76,\\\frac{3}{10},&76\le x<78,\\\frac{4}{10},&78\le x<84,\\\frac{5}{10},&84\le x<86,\\\frac{6}{10},&86\le x<89,\\\frac{7}{10},&89\le x<90,\\\frac{8}{10},&90\le x<92,\\\frac{9}{10},&92\le x<95,\\1,&x\ge95.\end{cases}
$$

其图形是以 $62$ 为起点、$95$ 为终点的右连续阶梯函数，在 $62,73,76,78,84,86,89,90,92,95$ 各点处分别跳跃 $\frac{1}{10}$，取值依次为 $\frac{1}{10},\frac{2}{10},\dots,1$.

![empirical_cdf.svg](../figures/empirical_cdf.svg){width=100%}

$\blacksquare$

### 习题八

（习题 1-10）设 $F\left(x\right)$ 为总体 $X$ 的分布函数，$X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，$F_n\left(x\right)$ 为其经验分布函数，证明对任意给定实数 $x$，有：

(1) $E\left(F_n\left(x\right)\right)=F\left(x\right)$;

(2) $D\left(F_n\left(x\right)\right)=\frac{1}{n}F\left(x\right)\left(1-F\left(x\right)\right)$.

### 解答 习题八

记示性函数 $I\left\{X_i\le x\right\}=\begin{cases}1,&X_i\le x,\\0,&X_i>x.\end{cases}$ 则由**定义 1.5.1**（经验分布函数），$F_n\left(x\right)=\frac{1}{n}\sum_{i=1}^n I\left\{X_i\le x\right\}$.

(1) 由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 与总体 $X$ 同分布，故对每个 $i$，
$$
E\left[I\left\{X_i\le x\right\}\right]=P\left(X_i\le x\right)=F\left(x\right).
$$
于是由期望的线性性，
$$
E\left[F_n\left(x\right)\right]=\frac{1}{n}\sum_{i=1}^n E\left[I\left\{X_i\le x\right\}\right]=\frac{1}{n}\cdot nF\left(x\right)=F\left(x\right).
$$

(2) 对示性变量 $I\left\{X_i\le x\right\}$，它是两点变量，取值 $1$ 的概率为 $F\left(x\right)$，故由 (1) 其方差为
$$
D\left[I\left\{X_i\le x\right\}\right]=F\left(x\right)\left(1-F\left(x\right)\right).
$$
又由**定义 1.3.2**，$X_1,X_2,\dots,X_n$ 相互独立，故 $I\left\{X_i\le x\right\}$ 相互独立，于是
$$
D\left[F_n\left(x\right)\right]=\frac{1}{n^2}\sum_{i=1}^n D\left[I\left\{X_i\le x\right\}\right]=\frac{1}{n^2}\cdot nF\left(x\right)\left(1-F\left(x\right)\right)=\frac{1}{n}F\left(x\right)\left(1-F\left(x\right)\right).
$$

$\blacksquare$
