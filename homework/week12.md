# 作业 12

> **定义 3.6.1**（正则分布族）<br>若单参数分布族 $\mathcal F=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ 满足：(1) 参数空间 $\Theta$ 是直线上的开区间；(2) 对任意 $\theta\in\Theta$，$f\left(x,\theta\right)>0$，即分布的支撑与参数无关；(3) $\frac{\partial f\left(x,\theta\right)}{\partial\theta}$ 对任意 $\theta\in\Theta$ 存在；(4) $f\left(x,\theta\right)$ 的积分与微分运算可以交换；(5) 费希尔信息量存在且 $0<I\left(\theta\right)=E\left[\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right]^2<+\infty$，则称该分布族为 C-R 正则分布族，其中 $$I\left(\theta\right)=E\left[\left(\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right)^2\right]$$ 为该分布族的费希尔信息量.

> **定理 3.6.1**（单参数 C-R 不等式）<br>设分布族 $\mathcal F=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ 是 C-R 正则分布族，可估函数 $g\left(\theta\right)$ 在参数空间上可微，$X_1,X_2,\dots,X_n$ 是从该总体抽取的样本，$\hat g\left(X\right)=\hat g\left(X_1,X_2,\dots,X_n\right)$ 是 $g\left(\theta\right)$ 的任一无偏估计，且积分可在积分号下对 $\theta$ 求导，则有 $$D\left[\hat g\left(X\right)\right]\ge\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)}.$$ 右端 $\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)}$ 称为 C-R 下界. 若某一无偏估计达到该下界，则它必为一致最小方差无偏估计.

> **定义 3.6.2**（效率）<br>设 $\hat g\left(X\right)$ 为 $g\left(\theta\right)$ 的无偏估计，则比值 $$e\left(\theta\right)=\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)D\left[\hat g\left(X\right)\right]}$$ 称为无偏估计 $\hat g\left(X\right)$ 的效率，其中 $0<e\left(\theta\right)\le1$.

> **定义 3.6.3**（有效估计）<br>当 $e\left(\theta\right)\equiv1$ 时，称 $\hat g\left(X\right)$ 为 $g\left(\theta\right)$ 的有效估计. 有效估计一定是一致最小方差无偏估计.

> **推论 3.5.1**（指数族自然形式下的充分完备统计量）<br>设样本的分布为指数族的自然形式，若自然参数空间有内点，则 $T\left(X\right)$ 为充分完备统计量；此时若 $h\left(T\left(X\right)\right)$ 是 $g\left(\theta\right)$ 的无偏估计，则由**定理 3.5.1**（L-S 定理），它是 $g\left(\theta\right)$ 唯一的一致最小方差无偏估计.

> **抽样分布**（正态样本的抽样分布）<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，则 $\bar X=\frac{1}{n}\sum_{i=1}^n X_i\sim N\left(\mu,\frac{\sigma^2}{n}\right)$. 特别地，当 $\sigma^2=1$ 时，$\bar X\sim N\left(\mu,\frac{1}{n}\right)$.

### 习题一

（习题 3.6-1）设总体 $X$ 的密度函数或分布列为 $f\left(x,\theta\right)$，且费希尔信息量 $I\left(\theta\right)$ 存在，如果二阶导数 $\frac{\partial^2 f\left(x,\theta\right)}{\partial\theta^2}$ 对一切 $\theta\in\Theta$ 存在，证明费希尔信息量为

$$
I\left(\theta\right)=-E\left[\frac{\partial^2\ln f\left(X,\theta\right)}{\partial\theta^2}\right].
$$

### 解答 习题一

由**定义 3.6.1**（正则分布族），$f\left(x,\theta\right)$ 为密度函数（离散情形同理），且积分与微分可交换. 由于 $\int f\left(x,\theta\right)\,\mathrm dx=1$，对 $\theta$ 求导并利用正则条件 (4)，得

$$
\frac{\partial}{\partial\theta}\int f\left(x,\theta\right)\,\mathrm dx=\int\frac{\partial f\left(x,\theta\right)}{\partial\theta}\,\mathrm dx=0.
$$

将 $\frac{\partial f}{\partial\theta}=f\cdot\frac{\partial\ln f}{\partial\theta}$ 代入上式，得

$$
\int\frac{\partial\ln f\left(x,\theta\right)}{\partial\theta}f\left(x,\theta\right)\,\mathrm dx=E\left[\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right]=0.
$$

上式再对 $\theta$ 求导，利用正则条件 (4) 交换积分与微分次序，得

$$
\frac{\partial}{\partial\theta}E\left[\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right]=\int\frac{\partial}{\partial\theta}\left[\frac{\partial\ln f\left(x,\theta\right)}{\partial\theta}f\left(x,\theta\right)\right]\,\mathrm dx=0.
$$

展开被积函数，

$$
\frac{\partial}{\partial\theta}\left[\frac{\partial\ln f}{\partial\theta}f\right]=\frac{\partial^2\ln f}{\partial\theta^2}f+\frac{\partial\ln f}{\partial\theta}\cdot\frac{\partial f}{\partial\theta}=\frac{\partial^2\ln f}{\partial\theta^2}f+\left(\frac{\partial\ln f}{\partial\theta}\right)^2f.
$$

两边积分，注意第一项积分为 $E\left[\frac{\partial^2\ln f\left(X,\theta\right)}{\partial\theta^2}\right]$，第二项积分为 $E\left[\left(\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right)^2\right]=I\left(\theta\right)$，故

$$
E\left[\frac{\partial^2\ln f\left(X,\theta\right)}{\partial\theta^2}\right]+I\left(\theta\right)=0.
$$

移项即得

$$
I\left(\theta\right)=-E\left[\frac{\partial^2\ln f\left(X,\theta\right)}{\partial\theta^2}\right].
$$

$\blacksquare$

### 习题二

（习题 3.6-2）设总体 $X$ 的分布列为

$$
P\left\{X=x\right\}=\left(x-1\right)\theta^2\left(1-\theta\right)^{x-2},\quad x=2,3,\dots
$$

其中 $0<\theta<1$，求费希尔信息量 $I\left(\theta\right)$.

### 解答 习题二

由**定义 3.6.1**（正则分布族），费希尔信息量为 $I\left(\theta\right)=E\left[\left(\frac{\partial\ln f\left(X,\theta\right)}{\partial\theta}\right)^2\right]$. 对分布列取对数，

$$
\ln P\left\{X=x\right\}=\ln\left(x-1\right)+2\ln\theta+\left(x-2\right)\ln\left(1-\theta\right).
$$

对 $\theta$ 求导，

$$
\frac{\partial\ln P\left\{X=x\right\}}{\partial\theta}=\frac{2}{\theta}-\frac{x-2}{1-\theta}.
$$

由**习题一**的结论，$I\left(\theta\right)=-E\left[\frac{\partial^2\ln f}{\partial\theta^2}\right]$，再求一次导数，

$$
\frac{\partial^2\ln P\left\{X=x\right\}}{\partial\theta^2}=-\frac{2}{\theta^2}-\frac{x-2}{\left(1-\theta\right)^2}.
$$

该分布为负二项分布 $NB\left(r=2,\theta\right)$，其均值为 $E\left(X\right)=\frac{2}{\theta}$，故 $E\left(X-2\right)=\frac{2}{\theta}-2=\frac{2\left(1-\theta\right)}{\theta}$. 于是

$$
I\left(\theta\right)=-E\left[-\frac{2}{\theta^2}-\frac{X-2}{\left(1-\theta\right)^2}\right]=\frac{2}{\theta^2}+\frac{E\left(X-2\right)}{\left(1-\theta\right)^2}=\frac{2}{\theta^2}+\frac{2\left(1-\theta\right)}{\theta\left(1-\theta\right)^2}=\frac{2}{\theta^2}+\frac{2}{\theta\left(1-\theta\right)}.
$$

通分合并，

$$
I\left(\theta\right)=\frac{2\left(1-\theta\right)+2\theta}{\theta^2\left(1-\theta\right)}=\frac{2}{\theta^2\left(1-\theta\right)}.
$$

$\blacksquare$

### 习题三

（习题 3.6-4）设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，且 $X$ 的密度函数为

$$
f\left(x,\theta\right)=
\begin{cases}
\frac{1}{\theta}e^{-\frac{x}{\theta}},& x>0,\\[6pt\right]
0,& x\le0,
\end{cases}
$$

其中 $\theta>0$ 为未知参数，求 $\theta$ 的一致最小方差无偏估计，并证明其方差等于 C-R 下界，即它是有效估计.

### 解答 习题三

由**推论 3.5.1**（指数族自然形式下的充分完备统计量），该密度函数可写为

$$
f\left(x,\theta\right)=\frac{1}{\theta}\exp\left\{-\frac{x}{\theta}\right\}=\theta^{-1}\exp\left\{-\frac{1}{\theta}x\right\},\quad x>0,
$$

为单参数指数族，自然参数空间 $\left\{-\frac{1}{\theta}:\theta>0\right\}=\left(-\infty,0\right)$ 有内点，故 $T=\sum_{i=1}^n X_i$ 为充分完备统计量. 该总体为指数分布 $E\left(\frac{1}{\theta}\right)$，其均值 $E\left(X\right)=\theta$. 由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 独立同分布，故

$$
E\left(\bar X\right)=\frac{1}{n}\sum_{i=1}^n E\left(X_i\right)=\theta.
$$

$\bar X=\frac{T}{n}$ 是充分完备统计量 $T$ 的函数且无偏，由**定理 3.5.1**（L-S 定理），$\bar X$ 为 $\theta$ 的唯一一致最小方差无偏估计.

下面证明 $\bar X$ 达到 C-R 下界. 由**定义 3.6.1**（正则分布族），对数密度为

$$
\ln f\left(x,\theta\right)=-\ln\theta-\frac{x}{\theta},\quad x>0.
$$

对 $\theta$ 求导，

$$
\frac{\partial\ln f}{\partial\theta}=-\frac{1}{\theta}+\frac{x}{\theta^2}=\frac{x-\theta}{\theta^2}.
$$

由 $E\left(X\right)=\theta$，$D\left(X\right)=\theta^2$，故

$$
I\left(\theta\right)=E\left[\left(\frac{X-\theta}{\theta^2}\right)^2\right]=\frac{D\left(X\right)}{\theta^4}=\frac{\theta^2}{\theta^4}=\frac{1}{\theta^2}.
$$

由**定理 3.6.1**（单参数 C-R 不等式），对 $g\left(\theta\right)=\theta$，$g'\left(\theta\right)=1$，C-R 下界为

$$
\frac{\left[g'\left(\theta\right)\right]^2}{nI\left(\theta\right)}=\frac{1}{n\cdot\frac{1}{\theta^2}}=\frac{\theta^2}{n}.
$$

另一方面，$\bar X$ 的方差为

$$
D\left(\bar X\right)=\frac{1}{n}D\left(X\right)=\frac{\theta^2}{n}.
$$

故 $D\left(\bar X\right)=\frac{\theta^2}{n}$ 恰等于 C-R 下界. 由**定义 3.6.3**（有效估计），$\bar X$ 是 $\theta$ 的有效估计，从而也是 $\theta$ 的一致最小方差无偏估计. $\blacksquare$

### 习题四

（习题 3.6-6）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,1\right)$ 的样本，其中 $\mu\in\mathbb R$ 是未知参数，证明：

(1) $\bar X^2-\frac{1}{n}$ 是 $\mu^2$ 的一致最小方差无偏估计；

(2) $\bar X^2-\frac{1}{n}$ 的方差大于 C-R 下界，即它不是有效估计.

### 解答 习题四

由**推论 3.5.1**（指数族自然形式下的充分完备统计量），正态分布族 $N\left(\mu,1\right)$ 为单参数指数族，其密度函数为

$$
f\left(x,\mu\right)=\frac{1}{\sqrt{2\pi}}\exp\left\{-\frac{\left(x-\mu\right)^2}{2}\right\}=\frac{1}{\sqrt{2\pi}}e^{-\frac{x^2}{2}}\exp\left\{\mu x-\frac{\mu^2}{2}\right\},
$$

自然参数空间 $\left\{\mu:\mu\in\mathbb R\right\}$ 有内点，故 $\bar X=\frac{1}{n}\sum_{i=1}^n X_i$ 为 $\mu$ 的充分完备统计量.

(1) 证明 $\bar X^2-\frac{1}{n}$ 是 $\mu^2$ 的一致最小方差无偏估计. 由**抽样分布**（正态样本的抽样分布），$\bar X\sim N\left(\mu,\frac{1}{n}\right)$，故

$$
E\left(\bar X^2\right)=D\left(\bar X\right)+\left[E\left(\bar X\right)\right]^2=\frac{1}{n}+\mu^2.
$$

于是

$$
E\left(\bar X^2-\frac{1}{n}\right)=E\left(\bar X^2\right)-\frac{1}{n}=\mu^2.
$$

故 $\bar X^2-\frac{1}{n}$ 是 $\mu^2$ 的无偏估计，且是充分完备统计量 $\bar X$ 的函数，由**定理 3.5.1**（L-S 定理），$\bar X^2-\frac{1}{n}$ 是 $\mu^2$ 的唯一一致最小方差无偏估计.

(2) 证明其方差大于 C-R 下界. 先计算该估计量的方差. 由 $\bar X\sim N\left(\mu,\frac{1}{n}\right)$，令 $Z=\sqrt n\,\bar X$，则 $Z\sim N\left(\sqrt n\,\mu,1\right)$，即 $Z^2$ 服从自由度为 $1$、非中心参数为 $\lambda=n\mu^2$ 的非中心 $\chi^2$ 分布. 由非中心 $\chi^2$ 分布的方差公式，$D\left(Z^2\right)=2+4\lambda=2+4n\mu^2$. 又 $\bar X^2=\frac{Z^2}{n^2}$，故

$$
D\left(\bar X^2-\frac{1}{n}\right)=D\left(\bar X^2\right)=\frac{D\left(Z^2\right)}{n^2}=\frac{2+4n\mu^2}{n^2}=\frac{4\mu^2}{n}+\frac{2}{n^2}.
$$

再计算 C-R 下界. 由**定义 3.6.1**（正则分布族），对数密度为

$$
\ln f\left(x,\mu\right)=-\frac{1}{2}\ln\left(2\pi\right)-\frac{\left(x-\mu\right)^2}{2}.
$$

对 $\mu$ 求导，

$$
\frac{\partial\ln f}{\partial\mu}=x-\mu.
$$

故费希尔信息量为

$$
I\left(\mu\right)=E\left[\left(X-\mu\right)^2\right]=D\left(X\right)=1.
$$

待估函数 $g\left(\mu\right)=\mu^2$，$g'\left(\mu\right)=2\mu$. 由**定理 3.6.1**（单参数 C-R 不等式），C-R 下界为

$$
\frac{\left[g'\left(\mu\right)\right]^2}{nI\left(\mu\right)}=\frac{\left(2\mu\right)^2}{n\cdot 1}=\frac{4\mu^2}{n}.
$$

比较二者：

$$
D\left(\bar X^2-\frac{1}{n}\right)=\frac{4\mu^2}{n}+\frac{2}{n^2}>\frac{4\mu^2}{n}=\text{C-R 下界}.
$$

二者之差为 $\frac{2}{n^2}>0$，故 $\bar X^2-\frac{1}{n}$ 的方差严格大于 C-R 下界，由**定义 3.6.3**（有效估计），它不是有效估计. $\blacksquare$
