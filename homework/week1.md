# week1

> **定义 1.2.1 (总体)**
> 
> 数理统计中, 把所研究问题涉及的研究对象的全体称为总体. (教材 $\S1.2$, p4)

> **定义 1.2.2 (个体)**
> 
> 组成总体的每个元素称为个体. (教材 $\S1.2$, p4)

> **定义 1.3.1 (样本空间)**
> 
> 样本 $X_1,X_2,\ldots,X_n$ 可能取值的全体的集合, 称为样本空间, 记为 $\mathcal{X}$. (教材 $\S1.3$, p6)

> **定义 1.3.2 (简单随机样本)**
> 
> 设总体 $X$ 的分布为 $F$, $X_1,X_2,\ldots,X_n$ 是从 $X$ 中抽取的容量为 $n$ 的样本. 若 $X_1,X_2,\ldots,X_n$ 相互独立, 且都与总体 $X$ 同分布, 则称它们是简单随机样本, 简称样本. (教材 $\S1.3$, p7)

> **定义 1.3.3 (参数空间)**
> 
> 参数 $\theta$ 所有可能取值的全体构成的集合, 称为参数空间, 记为 $\Theta$. (教材 $\S1.3$, p10)

> **定义 1.4.1 (统计量)**
> 
> 设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, $g\left(X_1,X_2,\ldots,X_n\right)$ 是样本的函数, 且除依赖于样本外不依赖于任何其他的未知量, 则称 $g\left(X_1,X_2,\ldots,X_n\right)$ 为统计量. (教材 $\S1.4$, p12)

> **定义 1.4.2 (顺序统计量)**
> 
> 把 $X_1,X_2,\ldots,X_n$ 按从小到大的顺序排列为 $X_{\left(1\right)}\le{}X_{\left(2\right)}\le\cdots\le{}X_{\left(n\right)}$, 称 $\left(X_{\left(1\right)},X_{\left(2\right)},\ldots,X_{\left(n\right)}\right)$ 为顺序统计量. (教材 $\S1.4$, p14)

> **定义 1.5.1 (经验分布函数)**
> 
> 设 $X_{\left(1\right)}\le\cdots\le{}X_{\left(n\right)}$ 是样本的顺序统计量, 对任意实数 $x$, 当 $x<{}X_{\left(1\right)}$ 时取 $F_n\left(x\right)=0$, 当 $X_{\left(r\right)}\le{}x<{}X_{\left(r+1\right)}$, $r=1,2,\ldots,n-1$ 时取 $F_n\left(x\right)=r/n$, 当 $x\ge{}X_{\left(n\right)}$ 时取 $F_n\left(x\right)=1$, 称 $F_n\left(x\right)$ 为经验分布函数. (教材 $\S1.5$, p15)

## 习题 1-1 (总体与样本)

什么是总体? 什么是样本?

### 解答 1-1

由**定义 1.2.1 (总体)**, 总体是所研究问题涉及的研究对象的全体; 由**定义 1.2.2 (个体)**, 组成总体的每个元素是个体. 实际研究中关心的并非个体本身, 而是个体的某项数量指标 $X$. 每件个体的指标值随机, 于是总体与随机变量 $X$ 对应, 总体分布即 $X$ 的分布, 总体均值, 总体方差即 $X$ 的数字特征. 个体为有限个时称有限总体, 否则称无限总体.

$\blacksquare$

样本是从总体中随机抽取的部分个体. 由**定义 1.3.2 (简单随机样本)**, 若抽得的 $X_1,X_2,\ldots,X_n$ 相互独立且每个都与总体 $X$ 同分布, 则称它们为容量 $n$ 的样本. 由**定义 1.3.1 (样本空间)**, 样本可能取值的全体构成样本空间. 样本有两重性: 抽样前是随机向量 $\left(X_1,\ldots,X_n\right)$, 抽样后是数组 $\left(x_1,\ldots,x_n\right)$.

$\blacksquare$

## 习题 1-2 (简单随机样本的条件)

简单随机样本应满足什么条件?

### 解答 1-2

由**定义 1.3.2 (简单随机样本)**, 条件有两条.

代表性: 每个 $X_i$ 与总体 $X$ 同分布, 即总体中任一个体被抽到的机会均等, 抽到的个体能代表总体.

独立性: $X_1,\ldots,X_n$ 相互独立, 即某一个体取什么值不影响其他个体的取值.

两条合起来即 $X_1,\ldots,X_n$ 独立同分布. 若只保证代表性而不保证独立性, 则样本的联合分布不能写成各边缘分布的乘积, 样本分布族也就不能由总体分布族逐点决定, 推断失去依据. 对有限总体, 独立抽取要求有放回抽样; 总体容量很大而样本容量很小时, 无放回抽样可近似看作独立抽样.

$\blacksquare$

## 习题 1-4 (三种总体的样本分布)

设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, 在下列三种情况下, 分别写出样本 $X_1,X_2,\ldots,X_n$ 的联合分布列或联合密度函数.

(1) 总体 $X$ 服从几何分布, 其分布列为 $P\left\{X=x\right\}=\left(1-p\right)^{x-1}p$, $0<{}p<1$, $x=1,2,\ldots$;

(2) 总体 $X$ 服从指数分布, 其密度函数为 $f\left(x\right)=\lambda\mathrm{e}^{-\lambda{}x}$ ($x>0$), $f\left(x\right)=0$ (其他), 其中 $\lambda>0$;

(3) 总体 $X$ 的密度函数为 $f\left(x\right)=\frac{\lambda}{2}\mathrm{e}^{-\lambda\left|x\right|}$, $-\infty<{}x<+\infty$, 其中 $\lambda>0$.

### 解答 1-4

三种情况都是离散或连续的一维总体, 由**定义 1.3.2 (简单随机样本)**, $X_1,\ldots,X_n$ 独立同分布, 故联合分布列等于各边缘分布列之积, 联合密度函数等于各边缘密度之积.

(1) 各 $x_i$ 取正整数,

$$
P\left\{X_1=x_1,\ldots,X_n=x_n\right\}=\prod_{i=1}^{n}\left(1-p\right)^{x_i-1}p=p^{n}\left(1-p\right)^{\sum_{i=1}^{n}x_i-n}.
$$

$\blacksquare$

(2) 各 $x_i>0$,

$$
f\left(x_1,\ldots,x_n\right)=\prod_{i=1}^{n}\lambda\mathrm{e}^{-\lambda{}x_i}=\lambda^{n}\mathrm{e}^{-\lambda\sum_{i=1}^{n}x_i}.
$$

$\blacksquare$

(3) 各 $x_i$ 取遍实数,

$$
f\left(x_1,\ldots,x_n\right)=\prod_{i=1}^{n}\frac{\lambda}{2}\mathrm{e}^{-\lambda\left|x_i\right|}=\left(\frac{\lambda}{2}\right)^{n}\mathrm{e}^{-\lambda\sum_{i=1}^{n}\left|x_i\right|}.
$$

$\blacksquare$

## 习题 1-6 (七个总体的样本分布族)

设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, 写出两点分布, 二项分布, 泊松分布, 几何分布, 均匀分布, 指数分布, 正态分布的样本分布族.

### 解答 1-6

样本分布族是参数空间中每个参数值所对应的样本分布之全体, 其中样本分布是 $X_1,\ldots,X_n$ 的联合分布. 由**定义 1.3.2 (简单随机样本)**, 联合分布是各边缘分布之积, 故只需把边缘分布逐项相乘. 各族的参数空间按**定义 1.3.3 (参数空间)** 写出.

两点分布 $B\left(1,p\right)$: $\Theta=\left\{p:0<{}p<1\right\}$,

$$
\left\{\prod_{i=1}^{n}p^{x_i}\left(1-p\right)^{1-x_i}=p^{\sum_{i=1}^{n}x_i}\left(1-p\right)^{n-\sum_{i=1}^{n}x_i}:x_i\in\left\{0,1\right\},0<{}p<1\right\}.
$$

$\blacksquare$

二项分布 $B\left(m,p\right)$, $m$ 为正整数: $\Theta=\left\{p:0<{}p<1\right\}$,

$$
\left\{\prod_{i=1}^{n}\binom{m}{x_i}p^{x_i}\left(1-p\right)^{m-x_i}:x_i\in\left\{0,1,\ldots,m\right\},0<{}p<1\right\}.
$$

$\blacksquare$

泊松分布 $P\left(\lambda\right)$: $\Theta=\left\{\lambda:\lambda>0\right\}$,

$$
\left\{\prod_{i=1}^{n}\frac{\lambda^{x_i}}{x_i!}\mathrm{e}^{-\lambda}=\frac{\lambda^{\sum_{i=1}^{n}x_i}}{\prod_{i=1}^{n}x_i!}\mathrm{e}^{-n\lambda}:x_i\in\left\{0,1,2,\ldots\right\},\lambda>0\right\}.
$$

$\blacksquare$

几何分布 $G\left(p\right)$: $\Theta=\left\{p:0<{}p<1\right\}$,

$$
\left\{p^{n}\left(1-p\right)^{\sum_{i=1}^{n}x_i-n}:x_i\in\left\{1,2,\ldots\right\},0<{}p<1\right\}.
$$

$\blacksquare$

均匀分布 $U\left[a,b\right]$: $\Theta=\left\{\left(a,b\right):-\infty<{}a<{}b<+\infty\right\}$,

$$
\left\{\left(b-a\right)^{-n}:\,a\le{}x_i\le{}b,i=1,2,\ldots,n,-\infty<{}a<{}b<+\infty\right\}.
$$

$\blacksquare$

指数分布 $E\left(\lambda\right)$: $\Theta=\left\{\lambda:\lambda>0\right\}$,

$$
\left\{\lambda^{n}\mathrm{e}^{-\lambda\sum_{i=1}^{n}x_i}:x_i>0,i=1,2,\ldots,n,\lambda>0\right\}.
$$

$\blacksquare$

正态分布 $N\left(\mu,\sigma^{2}\right)$: $\Theta=\left\{\left(\mu,\sigma^{2}\right):\mu\in\mathbb{R},\sigma>0\right\}$,

$$
\left\{\left(2\pi\sigma^{2}\right)^{-\frac{n}{2}}\exp\left\{-\frac{1}{2\sigma^{2}}\sum_{i=1}^{n}\left(x_i-\mu\right)^{2}\right\}:x_i\in\mathbb{R},i=1,2,\ldots,n,\mu\in\mathbb{R},\sigma>0\right\}.
$$

$\blacksquare$

## 习题 1-7 (零件的统计模型)

某机床加工出的零件的直径服从正态分布 $N\left(\mu,\sigma^{2}\right)$, 其中 $\mu,\sigma^{2}$ 均未知. 为对 $\mu,\sigma^{2}$ 做出估计, 随机选取加工出来的 $n$ 个零件进行测量, 得到 $n$ 个数据 $x_1,x_2,\ldots,x_n$. 试写出该问题的统计模型 (即参数空间和样本分布族).

### 解答 1-7

$n$ 次测量独立进行, 每次的量具与加工条件相同, 故 $X_1,\ldots,X_n$ 是来自同一条正态总体的简单随机样本, 即满足**定义 1.3.2 (简单随机样本)**. 未知量为 $\mu$ 与 $\sigma^{2}$, 故参数向量为 $\theta=\left(\mu,\sigma^{2}\right)$, 按**定义 1.3.3 (参数空间)**,

$$
\Theta=\left\{\left(\mu,\sigma^{2}\right):\mu\in\mathbb{R},\sigma>0\right\}.
$$

单个正态总体的密度为 $\frac{1}{\sqrt{2\pi}\sigma}\exp\left\{-\frac{\left(x-\mu\right)^{2}}{2\sigma^{2}}\right\}$, 把 $n$ 个边缘密度相乘, 得样本分布族

$$
\mathcal{F}=\left\{\left(\frac{1}{\sqrt{2\pi}\sigma}\right)^{n}\exp\left\{-\frac{1}{2\sigma^{2}}\sum_{i=1}^{n}\left(x_i-\mu\right)^{2}\right\}:\left(\mu,\sigma^{2}\right)\in\Theta,x_i\in\mathbb{R}\right\}.
$$

统计模型即样本分布族 $\mathcal{F}$ 与参数空间 $\Theta$ 这一对. $\mu$ 与 $\sigma^{2}$ 都未知, 故 $\Theta$ 中每个点给出一条样本分布, $\mathcal{F}$ 含不止一条分布.

$\blacksquare$

## 习题 1-8 (统计量的判定)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, 其中 $\mu$ 已知, $\sigma^{2}$ 未知, 判断下列量哪些是统计量哪些不是统计量, 为什么?

$$
\frac{1}{n}\sum_{i=1}^{n}X_i,\quad\frac{1}{n-1}\sum_{i=1}^{n}\left(X_i-\bar{X}\right)^{2},\quad\frac{1}{\sigma^{2}}\sum_{i=1}^{n}X_i^{2},\quad\frac{1}{n}\sum_{i=1}^{n}\left(X_i-\mu\right)^{2},
$$

$$
\frac{1}{\sigma^{2}}\sum_{i=1}^{n}\left(X_i-\mu\right)^{2},\quad{}X_1+2\mu,\quad\max\left\{X_1,\ldots,X_n\right\},\quad\min\left\{X_1,\ldots,X_n\right\}.
$$

### 解答 1-8

判据只用**定义 1.4.1 (统计量)**: 量必须是样本的函数, 且不含任何未知量. 本题 $\mu$ 已知, 可当作常数参与运算; $\sigma^{2}$ 未知, 凡出现 $\sigma^{2}$ 的量都不是统计量.

$\frac{1}{n}\sum_{i=1}^{n}X_i$ 只是 $X_1,\ldots,X_n$ 的函数, 是统计量.

$\blacksquare$

$\frac{1}{n-1}\sum_{i=1}^{n}\left(X_i-\bar{X}\right)^{2}$ 只用到样本, 是统计量.

$\blacksquare$

$\frac{1}{\sigma^{2}}\sum_{i=1}^{n}X_i^{2}$ 含未知的 $\sigma^{2}$, 不是统计量.

$\blacksquare$

$\frac{1}{n}\sum_{i=1}^{n}\left(X_i-\mu\right)^{2}$ 中 $\mu$ 已知, 是统计量.

$\blacksquare$

$\frac{1}{\sigma^{2}}\sum_{i=1}^{n}\left(X_i-\mu\right)^{2}$ 含未知的 $\sigma^{2}$, 不是统计量.

$\blacksquare$

$X_1+2\mu$ 中 $\mu$ 已知, 是统计量.

$\blacksquare$

$\max\left\{X_1,\ldots,X_n\right\}$ 与 $\min\left\{X_1,\ldots,X_n\right\}$ 都只是样本的函数, 都是统计量.

$\blacksquare$

## 习题 1-9 (经验分布函数)

对三年级的 $10$ 个孩子做阅读能力测试, 分数如下: $95,86,78,90,62,73,89,92,84,76$. 求相应的经验分布函数, 并绘出经验分布函数的图形.

### 解答 1-9

记样本为 $X_1,\ldots,X_{10}$, 观察值为 $95,86,78,90,62,73,89,92,84,76$. 按**定义 1.4.2 (顺序统计量)**, 把它们从小到大排列为

$$
x_{\left(1\right)}=62,x_{\left(2\right)}=73,x_{\left(3\right)}=76,x_{\left(4\right)}=78,x_{\left(5\right)}=84,x_{\left(6\right)}=86,x_{\left(7\right)}=89,x_{\left(8\right)}=90,x_{\left(9\right)}=92,x_{\left(10\right)}=95.
$$

按**定义 1.5.1 (经验分布函数)**, 取 $n=10$, 得

$$
F_{10}\left(x\right)=
\begin{cases}
0,&x<62,\\
0.1,&62\le{}x<73,\\
0.2,&73\le{}x<76,\\
0.3,&76\le{}x<78,\\
0.4,&78\le{}x<84,\\
0.5,&84\le{}x<86,\\
0.6,&86\le{}x<89,\\
0.7,&89\le{}x<90,\\
0.8,&90\le{}x<92,\\
0.9,&92\le{}x<95,\\
1,&x\ge95.
\end{cases}
$$

十个观察值互不相同, 故 $F_{10}$ 是右连续的阶梯函数, 在每个观察值处跃升 $0.1$, 两相邻观察值之间取常值: 它的图形是自左向右逐级升高的台阶, 在 $x=62$ 处由 $0$ 跳到 $0.1$, 在 $x=95$ 处跳到 $1$ 并向右保持水平.

$\blacksquare$
