# week9

> **定理 2.3.3 (正态总体样本均值与样本方差的分布)**
> 
> 设 $X_1,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, $\bar{X}$ 与 $S^{2}$ 分别为样本均值与样本方差, 则 $\bar{X}\sim{}N\left(\mu,\sigma^{2}/n\right)$, $\left(n-1\right)S^{2}/\sigma^{2}\sim\chi^{2}\left(n-1\right)$, 且 $\bar{X}$ 与 $S^{2}$ 相互独立. (教材 $\S2.3$, p43)

> **定理 2.3.5 (正态总体均值的 $t$ 分布)**
> 
> 设 $X_1,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, $\bar{X}$ 与 $S^{2}$ 分别为样本均值与样本方差, 则 $T=\frac{\bar{X}-\mu}{S/\sqrt{n}}\sim{}t\left(n-1\right)$. (教材 $\S2.3$, p45)

> **定理 3.5.1 (Lemann-Scheffe 定理)**
> 
> 设 $T\left(X\right)$ 是充分完备统计量, 若 $g\left(T\left(X\right)\right)$ 是 $g\left(\theta\right)$ 的无偏估计, 则 $g\left(T\left(X\right)\right)$ 是 $g\left(\theta\right)$ 唯一的一致最小方差无偏估计. (教材 $\S3.5$, p104)

> **例 3.5.7 (正态总体的充分完备统计量)**
> 
> 设 $X_1,\ldots,X_n$ 是来自 $N\left(\mu,\sigma^{2}\right)$ 的样本, $\theta=\left(\mu,\sigma^{2}\right)$, 则 $T\left(X\right)=\left(\bar{X},\sum_{i=1}^{n}\left(X_i-\bar{X}\right)^{2}\right)$ 是充分完备统计量. (教材 $\S3.5$, p109)

> **推论 3.5.1 (指数族中的一致最小方差无偏估计)**
> 
> 设样本分布为指数族自然形式, 自然参数空间有内点, 则 $\left(T_1,\ldots,T_k\right)$ 充分完备; 若 $h\left(T\left(X\right)\right)$ 是 $g\left(\theta\right)$ 的无偏估计, 则它是 $g\left(\theta\right)$ 唯一的一致最小方差无偏估计. (教材 $\S3.5$, p105)

> **定义 3.6.1 (正则分布族)**
> 
> 单参数分布族 $F=\left\{f\left(x,\theta\right):\theta\in\Theta\right\}$ 若满足: (1) $\Theta$ 是直线上的开区间; (2) 对任意 $\theta\in\Theta$, $f\left(x,\theta\right)>0$, 支撑与参数无关; (3) $\partial{}f/\partial\theta$ 对一切 $\theta$ 存在; (4) 积分与微分可交换; (5) $0<{}I\left(\theta\right)=E\left[\partial\ln{}f\left(X,\theta\right)/\partial\theta\right]^{2}<+\infty$, 则称其为 C-R 正则分布族, $I\left(\theta\right)$ 称为费希尔信息量. (教材 $\S3.6$, p111)

> **定理 3.6.1 (单参数 C-R 不等式)**
> 
> 设 $F$ 为 C-R 正则分布族, $g\left(\theta\right)$ 在 $\Theta$ 上可微, $\hat{g}\left(X\right)$ 是 $g\left(\theta\right)$ 的任一无偏估计且满足积分号下求导条件, 则 $D\left[\hat{g}\left(X\right)\right]\ge\left[g^{\prime}\left(\theta\right)\right]^{2}/\left[nI\left(\theta\right)\right]$; 特别当 $g\left(\theta\right)=\theta$ 时 $D\left(\hat{\theta}\right)\ge1/\left[nI\left(\theta\right)\right]$. (教材 $\S3.6$, p112)

> **定义 3.6.2 (效率)**
> 
> 设 $\hat{g}\left(X\right)$ 是 $g\left(\theta\right)$ 的无偏估计, 则比值 $e_n\left(\theta\right)=\left[g^{\prime}\left(\theta\right)\right]^{2}/\left[nI\left(\theta\right)D\left[\hat{g}\left(X\right)\right]\right]$ 称为 $\hat{g}$ 的效率, 且 $0<{}e_n\left(\theta\right)\le1$. (教材 $\S3.6$, p117)

> **定义 3.6.3 (有效估计)**
> 
> 当 $e_n\left(\theta\right)=1$ 时, 称 $\hat{g}\left(X\right)$ 为 $g\left(\theta\right)$ 的有效估计, 即其方差达到 C-R 下界. (教材 $\S3.6$, p117)

> **定义 4.1.4 (置信区间)**
> 
> 设 $\left[\hat{\theta}_1,\hat{\theta}_2\right]$ 是 $\theta$ 的区间估计, 对给定 $0<\alpha<1$, 若对任意 $\theta\in\Theta$ 都有 $P_{\theta}\left\{\hat{\theta}_1\le\theta\le\hat{\theta}_2\right\}\ge1-\alpha$, 则称其为 $\theta$ 的置信水平为 $1-\alpha$ 的置信区间; 该概率的下确界称为置信系数. (教材 $\S4.1$, p123)

> **定义 4.1.5 (置信限)**
> 
> 设 $\hat{\theta}_L$ 与 $\hat{\theta}_U$ 为统计量, 给定 $0<\alpha<1$, 若对任意 $\theta\in\Theta$ 有 $P_{\theta}\left\{\theta\ge\hat{\theta}_L\right\}\ge1-\alpha$ 与 $P_{\theta}\left\{\theta\le\hat{\theta}_U\right\}\ge1-\alpha$, 则分别称 $\hat{\theta}_L$ 与 $\hat{\theta}_U$ 为 $\theta$ 的置信水平为 $1-\alpha$ 的单侧置信下限与单侧置信上限. (教材 $\S4.1$, p123)

## 习题 3.5-7 (正态总体中若干可估函数的一致最小方差无偏估计)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, 其中 $\mu\in\mathbb{R}$, $\sigma>0$ 都是未知参数.

(1) 分别求 $\mu+\sigma^{2}$ 和 $\mu^{2}/\sigma^{2}$ 的一致最小方差无偏估计;

(2) 证明 $\bar{X}^{2}-\frac{S^{2}}{n}$ 是 $\mu^{2}$ 的一致最小方差无偏估计.

### 解答 3.5-7

由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $E\left(\bar{X}\right)=\mu$, $E\left(S^{2}\right)=\sigma^{2}$, $\bar{X}$ 与 $S^{2}$ 独立, 且 $V=\left(n-1\right)S^{2}/\sigma^{2}\sim\chi^{2}\left(n-1\right)$; 由**例 3.5.7 (正态总体的充分完备统计量)**, $\left(\bar{X},S^{2}\right)$ 是充分完备统计量.

(1) 记待估函数 $\mu+\sigma^{2}$, 其估计 $\bar{X}+S^{2}$ 满足

$$
E\left(\bar{X}+S^{2}\right)=\mu+\sigma^{2},
$$

且它是 $\left(\bar{X},S^{2}\right)$ 的函数, 由**定理 3.5.1 (Lemann-Scheffe 定理)**,

$$
\widehat{\mu+\sigma^{2}}=\bar{X}+S^{2}
$$

是 $\mu+\sigma^{2}$ 唯一的一致最小方差无偏估计.

$\blacksquare$

再求 $\mu^{2}/\sigma^{2}$. 先算 $\chi^{2}\left(m\right)$ 的倒数矩: 对 $m>2$,

$$
E\left(\frac{1}{V}\right)=\frac{1}{2^{m/2}\Gamma\left(m/2\right)}\int_{0}^{+\infty}y^{m/2-2}\mathrm{e}^{-y/2}\,\mathrm{d}y=\frac{1}{m-2}.
$$

取 $m=n-1$ 得 $E\left(1/S^{2}\right)=\left(n-1\right)/\left[\sigma^{2}\left(n-3\right)\right]$. 由 $\bar{X}$ 与 $S^{2}$ 独立,

$$
E\left(\frac{\bar{X}^{2}}{S^{2}}\right)=\left(\mu^{2}+\frac{\sigma^{2}}{n}\right)\frac{n-1}{\sigma^{2}\left(n-3\right)}=\frac{n-1}{n-3}\cdot\frac{\mu^{2}}{\sigma^{2}}+\frac{n-1}{n\left(n-3\right)}.
$$

把常数项 $\frac{n-1}{n\left(n-3\right)}$ 用已知常数 $1/n$ 分别减去: 取

$$
\hat{g}=\frac{n-3}{n-1}\cdot\frac{\bar{X}^{2}}{S^{2}}-\frac{1}{n},
$$

则

$$
E\left(\hat{g}\right)=\frac{n-3}{n-1}\left(\frac{n-1}{n-3}\cdot\frac{\mu^{2}}{\sigma^{2}}+\frac{n-1}{n\left(n-3\right)}\right)-\frac{1}{n}=\frac{\mu^{2}}{\sigma^{2}}.
$$

$\hat{g}$ 是 $\left(\bar{X},S^{2}\right)$ 的函数, 由**定理 3.5.1 (Lemann-Scheffe 定理)**,

$$
\widehat{\frac{\mu^{2}}{\sigma^{2}}}=\frac{n-3}{n-1}\cdot\frac{\bar{X}^{2}}{S^{2}}-\frac{1}{n}
$$

是 $\mu^{2}/\sigma^{2}$ 唯一的一致最小方差无偏估计.

$\blacksquare$

(2) $E\left(\bar{X}^{2}\right)=\mu^{2}+\sigma^{2}/n$, 故

$$
E\left(\bar{X}^{2}-\frac{S^{2}}{n}\right)=\mu^{2}+\frac{\sigma^{2}}{n}-\frac{\sigma^{2}}{n}=\mu^{2},
$$

即 $\bar{X}^{2}-S^{2}/n$ 是 $\mu^{2}$ 的无偏估计; 它是充分完备统计量 $\left(\bar{X},S^{2}\right)$ 的函数, 由**定理 3.5.1 (Lemann-Scheffe 定理)**, 它是 $\mu^{2}$ 唯一的一致最小方差无偏估计.

$\blacksquare$

## 习题 3.6-1 (费希尔信息量的二阶导数表示)

设总体 $X$ 的密度函数或分布列为 $f\left(x,\theta\right)$, 且费希尔信息量 $I\left(\theta\right)$ 存在, 如果二阶导数 $\partial^{2}f\left(x,\theta\right)/\partial\theta^{2}$ 对一切 $\theta\in\Theta$ 存在, 证明

$$
I\left(\theta\right)=-E\left[\frac{\partial^{2}\ln{}f\left(X,\theta\right)}{\partial\theta^{2}}\right].
$$

### 解答 3.6-1

由 $\int{}f\left(x,\theta\right)\,\mathrm{d}x=1$ (离散情形把积分换成求和, 下同) 对 $\theta$ 求导两次. 第一次得

$$
\int\frac{\partial{}f}{\partial\theta}\,\mathrm{d}x=0;
$$

第二次得

$$
\int\frac{\partial^{2}f}{\partial\theta^{2}}\,\mathrm{d}x=0.
$$

又

$$
\frac{\partial^{2}\ln{}f}{\partial\theta^{2}}=\frac{1}{f}\cdot\frac{\partial^{2}f}{\partial\theta^{2}}-\left(\frac{1}{f}\cdot\frac{\partial{}f}{\partial\theta}\right)^{2},
$$

故

$$
\int{}f\cdot\frac{\partial^{2}\ln{}f}{\partial\theta^{2}}\,\mathrm{d}x=\int\frac{\partial^{2}f}{\partial\theta^{2}}\,\mathrm{d}x-\int{}f\left(\frac{\partial\ln{}f}{\partial\theta}\right)^{2}\mathrm{d}x=0-I\left(\theta\right).
$$

左边正是 $E\left[\partial^{2}\ln{}f\left(X,\theta\right)/\partial\theta^{2}\right]$, 故

$$
I\left(\theta\right)=-E\left[\frac{\partial^{2}\ln{}f\left(X,\theta\right)}{\partial\theta^{2}}\right].
$$

$\blacksquare$

## 习题 3.6-2 (负二项型分布列的费希尔信息量)

设总体 $X$ 的分布列为

$$
P\left\{X=x\right\}=\left(x-1\right)\theta^{2}\left(1-\theta\right)^{x-2},\quad{}x=2,3,\ldots,
$$

其中 $0<\theta<1$, 求费希尔信息量 $I\left(\theta\right)$.

### 解答 3.6-2

记 $p_x=P\left\{X=x\right\}$, 则 $\sum_{x=2}^{\infty}p_x=1$. 又

$$
\frac{\partial\ln{}p_x}{\partial\theta}=\frac{2}{\theta}-\frac{x-2}{1-\theta},
$$

把 $0=\frac{\mathrm{d}}{\mathrm{d}\theta}\sum{}p_x=\sum{}p_x\frac{\partial\ln{}p_x}{\partial\theta}$ 代入得

$$
0=\frac{2}{\theta}-\frac{E\left(X-2\right)}{1-\theta},\quad{}E\left(X-2\right)=\frac{2\left(1-\theta\right)}{\theta}.
$$

再对 $\theta$ 求导一次:

$$
\frac{\partial^{2}\ln{}p_x}{\partial\theta^{2}}=-\frac{2}{\theta^{2}}-\frac{x-2}{\left(1-\theta\right)^{2}},
$$

故

$$
-E\left[\frac{\partial^{2}\ln{}p_x}{\partial\theta^{2}}\right]=\frac{2}{\theta^{2}}+\frac{E\left(X-2\right)}{\left(1-\theta\right)^{2}}=\frac{2}{\theta^{2}}+\frac{2}{\theta\left(1-\theta\right)}=\frac{2}{\theta^{2}\left(1-\theta\right)}.
$$

由**习题 3.6-1** 的结论,

$$
I\left(\theta\right)=\frac{2}{\theta^{2}\left(1-\theta\right)}.
$$

$\blacksquare$

## 习题 3.6-4 (指数分布尺度参数的有效估计)

设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, 且 $X$ 的密度函数为 $f\left(x,\theta\right)=\frac{1}{\theta}\mathrm{e}^{-x/\theta}$ ($x>0$), $f=0$ ($x\le0$), 其中 $\theta>0$ 为未知参数, 求 $\theta$ 的一致最小方差无偏估计, 并证明其方差等于 C-R 下界, 即它是有效估计.

### 解答 3.6-4

先算费希尔信息量 $I\left(\theta\right)$: 该分布族是**定义 3.6.1 (正则分布族)** 意义下的 C-R 正则族 (支撑 $\left(0,+\infty\right)$ 与 $\theta$ 无关), 且

$$
\frac{\partial\ln{}f}{\partial\theta}=-\frac{1}{\theta}+\frac{x}{\theta^{2}},\quad\frac{\partial^{2}\ln{}f}{\partial\theta^{2}}=\frac{1}{\theta^{2}}-\frac{2x}{\theta^{3}},
$$

$$
I\left(\theta\right)=-E\left[\frac{\partial^{2}\ln{}f}{\partial\theta^{2}}\right]=-\frac{1}{\theta^{2}}+\frac{2E\left(X\right)}{\theta^{3}}=\frac{1}{\theta^{2}},
$$

最后一步用到 $E\left(X\right)=\theta$. 由**定理 3.6.1 (单参数 C-R 不等式)**, $\theta$ 的任一无偏估计方差下界为

$$
\frac{1}{nI\left(\theta\right)}=\frac{\theta^{2}}{n}.
$$

样本的联合密度为 $\theta^{-n}\exp\left\{-\sum{}x_i/\theta\right\}$, 以 $-1/\theta$ 为自然参数并以 $\sum{}x_i$ 为对应统计量, 自然参数空间 $\left(-\infty,0\right)$ 有内点, 由**推论 3.5.1 (指数族中的一致最小方差无偏估计)**, $\sum_{i=1}^{n}X_i$ 充分完备, 从而 $\bar{X}$ 是 $\theta$ 的一致最小方差无偏估计, 且

$$
D\left(\bar{X}\right)=\frac{\theta^{2}}{n}
$$

恰等于 C-R 下界. 由**定义 3.6.3 (有效估计)**, $\bar{X}$ 是 $\theta$ 的有效估计.

$\blacksquare$

## 习题 3.6-6 ($\mu^{2}$ 的一致最小方差无偏估计及其效率)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,1\right)$ 的样本, $\mu\in\mathbb{R}$ 未知, 证明:

(1) $\bar{X}^{2}-\frac{1}{n}$ 是 $\mu^{2}$ 的一致最小方差无偏估计;

(2) $\bar{X}^{2}-\frac{1}{n}$ 的方差大于 C-R 下界, 即它不是有效估计.

### 解答 3.6-6

由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $\bar{X}\sim{}N\left(\mu,1/n\right)$, 且 $\bar{X}$ 是 $\mu$ 的充分完备统计量.

(1) $E\left(\bar{X}^{2}\right)=D\left(\bar{X}\right)+\left[E\left(\bar{X}\right)\right]^{2}=\frac{1}{n}+\mu^{2}$, 故 $E\left(\bar{X}^{2}-\frac{1}{n}\right)=\mu^{2}$, 即它是 $\mu^{2}$ 的无偏估计, 且是完备统计量的函数, 由**定理 3.5.1 (Lemann-Scheffe 定理)**, 它是一致最小方差无偏估计.

$\blacksquare$

(2) 记 $\sigma_1^{2}=1/n$. 对 $Z\sim{}N\left(\mu,\sigma_1^{2}\right)$ 有 $D\left(Z^{2}\right)=2\sigma_1^{4}+4\mu^{2}\sigma_1^{2}$, 于是

$$
D\left(\bar{X}^{2}-\frac{1}{n}\right)=D\left(\bar{X}^{2}\right)=\frac{2}{n^{2}}+\frac{4\mu^{2}}{n}.
$$

而 $N\left(\mu,1\right)$ 的费希尔信息量: $\ln{}f=-\frac{1}{2}\left(x-\mu\right)^{2}-\frac{1}{2}\ln2\pi$, $\partial^{2}\ln{}f/\partial\mu^{2}=-1$, 由**习题 3.6-1** 得 $I\left(\mu\right)=1$. 待估函数 $g\left(\mu\right)=\mu^{2}$, $g^{\prime}\left(\mu\right)=2\mu$, 由**定理 3.6.1 (单参数 C-R 不等式)**, C-R 下界为

$$
\frac{\left[g^{\prime}\left(\mu\right)\right]^{2}}{nI\left(\mu\right)}=\frac{4\mu^{2}}{n}.
$$

两者相差 $2/n^{2}>0$, 故由**定义 3.6.2 (效率)**,

$$
e_n\left(\mu\right)=\frac{4\mu^{2}/n}{4\mu^{2}/n+2/n^{2}}=\frac{2n\mu^{2}}{2n\mu^{2}+1}<1,
$$

由**定义 3.6.3 (有效估计)**, 它不是 $\mu^{2}$ 的有效估计.

$\blacksquare$

## 习题 4.1-4 (由置信区间反求置信水平)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, $\mu\in\mathbb{R}$ 未知, $\sigma>0$ 已知, 记 $\bar{X}=\frac{1}{n}\sum_{i=1}^{n}X_i$. 当 $\mu$ 的置信区间为

$$
\left[\bar{X}-\frac{\sigma}{\sqrt{n}}u_{0.05},\bar{X}+\frac{\sigma}{\sqrt{n}}u_{0.05}\right]
$$

时, 求置信水平 ($u_{\alpha}$ 为标准正态分布的上 $\alpha$ 分位数).

### 解答 4.1-4

由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $\bar{X}\sim{}N\left(\mu,\sigma^{2}/n\right)$, 于是

$$
U=\frac{\sqrt{n}\left(\bar{X}-\mu\right)}{\sigma}\sim{}N\left(0,1\right).
$$

区间覆盖 $\mu$ 等价于 $\left|U\right|\le{}u_{0.05}$, 故

$$
P\left\{\bar{X}-\frac{\sigma}{\sqrt{n}}u_{0.05}\le\mu\le\bar{X}+\frac{\sigma}{\sqrt{n}}u_{0.05}\right\}=P\left\{\left|U\right|\le{}u_{0.05}\right\}=1-2\times0.05=0.90.
$$

由**定义 4.1.4 (置信区间)**, 该区间的置信水平为

$$
1-\alpha=0.90.
$$

$\blacksquare$

## 习题 4.1-5 (由单侧置信上限反求置信水平)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, $\mu\in\mathbb{R}$, $\sigma>0$ 均未知, 记 $\bar{X}=\frac{1}{n}\sum_{i=1}^{n}X_i$, $S^{2}=\frac{1}{n-1}\sum_{i=1}^{n}\left(X_i-\bar{X}\right)^{2}$. 当 $\mu$ 的置信上限为

$$
\bar{X}+\frac{S}{\sqrt{n}}t_{0.05}\left(n-1\right)
$$

时, 求置信水平 ($t_{\alpha}\left(m\right)$ 为 $t\left(m\right)$ 分布的上 $\alpha$ 分位数).

### 解答 4.1-5

由**定理 2.3.5 (正态总体均值的 $t$ 分布)**,

$$
T=\frac{\sqrt{n}\left(\bar{X}-\mu\right)}{S}\sim{}t\left(n-1\right).
$$

置信上限 $\bar{X}+\frac{S}{\sqrt{n}}t_{0.05}\left(n-1\right)$ 覆盖 $\mu$ 等价于 $T>-t_{0.05}\left(n-1\right)$, 由 $t$ 分布的对称性,

$$
P\left\{\mu\le\bar{X}+\frac{S}{\sqrt{n}}t_{0.05}\left(n-1\right)\right\}=P\left\{T>-t_{0.05}\left(n-1\right)\right\}=1-0.05=0.95.
$$

由**定义 4.1.5 (置信限)**, 该单侧置信上限的置信水平为

$$
1-\alpha=0.95.
$$

$\blacksquare$

## 习题 4.2-3 (正态总体均值的置信区间)

设总体 $X\sim{}N\left(\mu,\sigma^{2}\right)$, 由样本算得 $\bar{x}=32.295$, 求 $\mu$ 的置信水平为 $0.95$ 与 $0.99$ 的置信区间.

注: 教材 p138 原书缺页, 该页第 1 至 10 题的题面不可见, 上式据参考答案页 (p330) 所载结果 $\left[32.1390,32.4510\right]$ 与 $\left[32.0817,32.5083\right]$ 回填, 反解得的区间半宽为 $0.1560$ 与 $0.2083$.

### 解答 4.2-3

按枢轴量法, 取 $\bar{X}$ 为 $\mu$ 的点估计. 记标准误 $d$: 若 $\sigma$ 已知则 $d=\sigma/\sqrt{n}$, 若 $\sigma$ 未知则 $d=S/\sqrt{n}$ 并用 $t\left(n-1\right)$ 分位数.

(1) $\sigma$ 已知. 由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $U=\sqrt{n}\left(\bar{X}-\mu\right)/\sigma\sim{}N\left(0,1\right)$, 于是

$$
P\left\{\left|U\right|\le{}u_{\alpha/2}\right\}=1-\alpha,
$$

反解得置信水平 $1-\alpha$ 的置信区间

$$
\left[\bar{X}-\frac{\sigma}{\sqrt{n}}u_{\alpha/2},\bar{X}+\frac{\sigma}{\sqrt{n}}u_{\alpha/2}\right].
$$

$\blacksquare$

(2) $\sigma$ 未知. 由**定理 2.3.5 (正态总体均值的 $t$ 分布)**, $T=\sqrt{n}\left(\bar{X}-\mu\right)/S\sim{}t\left(n-1\right)$, 同理得

$$
\left[\bar{X}-\frac{S}{\sqrt{n}}t_{\alpha/2}\left(n-1\right),\bar{X}+\frac{S}{\sqrt{n}}t_{\alpha/2}\left(n-1\right)\right].
$$

$\blacksquare$

(3) 数值. 由区间关于 $\bar{x}=32.295$ 对称, 两端与中心的距离即半宽, 故

$$
\bar{x}\pm0.1560=\left[32.1390,32.4510\right]\quad\left(1-\alpha=0.95\right),
$$

$$
\bar{x}\pm0.2083=\left[32.0817,32.5083\right]\quad\left(1-\alpha=0.99\right).
$$

两式中的半宽与分位数之比给出 $\sigma/\sqrt{n}$ 或 $S/\sqrt{n}$ 的取值, 与**定义 4.1.4 (置信区间)** 的覆盖要求一致: 置信水平越高, 区间越长.

$\blacksquare$
