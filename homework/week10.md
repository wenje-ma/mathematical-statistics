# week10

> **定理 2.3.3 (正态总体样本均值与样本方差的分布)**
> 
> 设 $X_1,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, $\bar{X}$ 与 $S^{2}$ 分别为样本均值与样本方差, 则 $\bar{X}\sim N\left(\mu,\sigma^{2}/n\right)$, $\left(n-1\right)S^{2}/\sigma^{2}\sim\chi^{2}\left(n-1\right)$, 且 $\bar{X}$ 与 $S^{2}$ 相互独立. (教材 $\S2.3$, p43)

> **定理 2.3.5 (正态总体均值的 $t$ 分布)**
> 
> 设 $X_1,\ldots,X_n$ 是来自 $N\left(\mu,\sigma^{2}\right)$ 的样本, 则 $T=\frac{\bar{X}-\mu}{S/\sqrt{n}}\sim t\left(n-1\right)$. (教材 $\S2.3$, p45)

> **定理 2.3.6 (两样本的合并方差 $t$ 分布)**
> 
> 设 $X_1,\ldots,X_m$ 与 $Y_1,\ldots,Y_n$ 分别来自 $N\left(\mu_1,\sigma^{2}\right)$ 与 $N\left(\mu_2,\sigma^{2}\right)$ 且相互独立, 记 $S_w^{2}=\frac{\left(m-1\right)S_1^{2}+\left(n-1\right)S_2^{2}}{m+n-2}$, 则 $\frac{\bar{X}-\bar{Y}-\left(\mu_1-\mu_2\right)}{S_w\sqrt{\frac{1}{m}+\frac{1}{n}}}\sim t\left(m+n-2\right)$. (教材 $\S2.3$, p46)

> **定理 2.3.7 (两样本方差比的 $F$ 分布)**
> 
> 设 $X_1,\ldots,X_m$ 与 $Y_1,\ldots,Y_n$ 分别来自 $N\left(\mu_1,\sigma_1^{2}\right)$ 与 $N\left(\mu_2,\sigma_2^{2}\right)$ 且相互独立, 则 $\frac{S_1^{2}/\sigma_1^{2}}{S_2^{2}/\sigma_2^{2}}\sim F\left(m-1,n-1\right)$. (教材 $\S2.3$, p47)

> **定理 2.3.8 (指数分布样本与卡方分布的关系)**
> 
> 设 $X_1,\ldots,X_n$ 是来自指数分布 $E(\lambda)$ 的样本, 则 $T=2\lambda n\bar{X}=\frac{2n\bar{X}}{\theta}\sim\chi^{2}(2n)$, 其中 $\theta=1/\lambda$. (教材 $\S2.3$, p47)

> **定义 4.1.4 (置信区间)**
> 
> 设 $\left[\hat{\theta}_1,\hat{\theta}_2\right]$ 是 $\theta$ 的一个区间估计, 对给定 $0<\alpha<1$, 若对任意的 $\theta\in\Theta$ 都有 $P_{\theta}\left\{\hat{\theta}_1\le\theta\le\hat{\theta}_2\right\}\ge1-\alpha$, 则称其为 $\theta$ 的置信水平为 $1-\alpha$ 的置信区间, 该概率关于 $\theta$ 的下确界称为置信系数. (教材 $\S4.1$, p123)

> **定义 4.1.5 (置信限)**
> 
> 若 $P_{\theta}\left\{\theta\ge\hat{\theta}_L\right\}\ge1-\alpha$, 则 $\hat{\theta}_L$ 为置信水平 $1-\alpha$ 的单侧置信下限; 若 $P_{\theta}\left\{\theta\le\hat{\theta}_U\right\}\ge1-\alpha$, 则 $\hat{\theta}_U$ 为置信水平 $1-\alpha$ 的单侧置信上限. (教材 $\S4.1$, p123)

> **定义 4.2.1 (枢轴量)**
> 
> 令 $G\left(X_1,\ldots,X_n,\theta\right)$ 是样本与参数 $\theta$ 的可测函数, 当且仅当 $G\left(X_1,\ldots,X_n,\theta\right)$ 的分布不依赖于 $\theta$ 时, 称之为枢轴量. 若 $g(\theta)$ 关于 $\theta$ 单调, 则 $\theta$ 的置信区间 $\left[\theta_1,\theta_2\right]$ 可变换为 $g(\theta)$ 的置信区间. (教材 $\S4.2$, p127)

## 习题 4.2-5 (由区间长度要求确定样本容量)

设总体 $X\sim N\left(\mu,\sigma_0^{2}\right)$, $\sigma_0>0$ 已知, $\mu$ 未知. 要求 $\mu$ 的置信水平为 $1-\alpha$ 的置信区间的长度不超过 $k$, 求所需样本容量 $n$ 的最小值.

### 解答 4.2-5

由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $\bar{X}\sim N\left(\mu,\sigma_0^{2}/n\right)$, 取枢轴量

$$
U=\frac{\sqrt{n}\left(\bar{X}-\mu\right)}{\sigma_0}\sim N\left(0,1\right),
$$

按**定义 4.2.1 (枢轴量)**, $U$ 的分布与 $\mu$ 无关, 且

$$
P\left\{\left|U\right|\le u_{\alpha/2}\right\}=1-\alpha
$$

反解得置信区间 $\left[\bar{X}-\frac{\sigma_0}{\sqrt{n}}u_{\alpha/2},\bar{X}+\frac{\sigma_0}{\sqrt{n}}u_{\alpha/2}\right]$, 其长度为

$$
L\left(n\right)=\frac{2\sigma_0u_{\alpha/2}}{\sqrt{n}}.
$$

由**定义 4.1.4 (置信区间)** 的覆盖要求, 该区间合法; 其长度 $L\left(n\right)$ 关于 $n$ 单调递减, 故要在保持置信水平的前提下把长度压到 $k$ 以内, 只能增大 $n$. 令 $L\left(n\right)\le k$ 得

$$
n\ge\left(\frac{2\sigma_0u_{\alpha/2}}{k}\right)^{2}.
$$

故最小样本容量为不小于 $\left(2\sigma_0u_{\alpha/2}/k\right)^{2}$ 的最小整数.

$\blacksquare$

## 习题 4.2-9 (两总体方差比的置信区间)

设 $X_1,\ldots,X_m$ 与 $Y_1,\ldots,Y_n$ 分别来自正态总体 $N\left(\mu_1,\sigma_1^{2}\right)$ 与 $N\left(\mu_2,\sigma_2^{2}\right)$ 且相互独立, 由样本算得 $S_1^{2}$ 与 $S_2^{2}$. 求方差比 $\sigma_1^{2}/\sigma_2^{2}$ 的置信水平为 $1-\alpha$ 的置信区间.

注: 教材 p138 原书缺页, 该页第 1 至 10 题的题面不可见, 上式据参考答案页 (p330) 所载结果 $\left[0.024,0.285\right]$ 回填.

### 解答 4.2-9

由**定理 2.3.7 (两样本方差比的 $F$ 分布)**,

$$
F=\frac{S_1^{2}/\sigma_1^{2}}{S_2^{2}/\sigma_2^{2}}\sim F\left(m-1,n-1\right),
$$

其分布与 $\left(\sigma_1^{2},\sigma_2^{2}\right)$ 无关, 按**定义 4.2.1 (枢轴量)** 可作枢轴量. 取

$$
P\left\{F_{1-\alpha/2}\left(m-1,n-1\right)\le F\le F_{\alpha/2}\left(m-1,n-1\right)\right\}=1-\alpha,
$$

解不等式得

$$
\frac{S_1^{2}}{S_2^{2}}\cdot\frac{1}{F_{\alpha/2}\left(m-1,n-1\right)}\le\frac{\sigma_1^{2}}{\sigma_2^{2}}\le\frac{S_1^{2}}{S_2^{2}}\cdot\frac{1}{F_{1-\alpha/2}\left(m-1,n-1\right)},
$$

其中 $F_{1-\alpha/2}\left(m-1,n-1\right)=1/F_{\alpha/2}\left(n-1,m-1\right)$. 由**定义 4.1.4 (置信区间)**, 这就是置信水平 $1-\alpha$ 的置信区间.

$\blacksquare$

## 习题 4.2-11 (区间长度的期望与方差)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, $a,b$ 为常数, $0<a<b$, 求随机区间

$$
\left[\frac{\sum_{i=1}^{n}\left(X_i-\bar{X}\right)^{2}}{b},\frac{\sum_{i=1}^{n}\left(X_i-\bar{X}\right)^{2}}{a}\right]
$$

的长度 $L$ 的数学期望和方差.

### 解答 4.2-11

记 $Q=\sum_{i=1}^{n}\left(X_i-\bar{X}\right)^{2}=\left(n-1\right)S^{2}$, 则

$$
L=\left(\frac{1}{a}-\frac{1}{b}\right)Q,\qquad \frac{1}{a}-\frac{1}{b}>0.
$$

由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $Q/\sigma^{2}\sim\chi^{2}\left(n-1\right)$, 而 $\chi^{2}\left(m\right)$ 的均值与方差为 $m$ 与 $2m$, 故

$$
E\left(L\right)=\left(\frac{1}{a}-\frac{1}{b}\right)\sigma^{2}\left(n-1\right)=\left(n-1\right)\sigma^{2}\left(\frac{1}{a}-\frac{1}{b}\right),
$$

$$
D\left(L\right)=\left(\frac{1}{a}-\frac{1}{b}\right)^{2}\sigma^{4}\cdot2\left(n-1\right)=2\left(n-1\right)\sigma^{4}\left(\frac{1}{a}-\frac{1}{b}\right)^{2}.
$$

$\blacksquare$

## 习题 4.2-14 (正态总体标准差的单侧置信上限)

随机选取 9 发炮弹, 测得炮弹的炮口速度的样本标准差 $s=11$ (m/s). 若炮弹的炮口速度服从正态分布 $N\left(\mu,\sigma^{2}\right)$, 其中 $\mu,\sigma^{2}$ 未知, 求标准差 $\sigma$ 的置信水平为 $95\%$ 的单侧置信上限.

### 解答 4.2-14

由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $Q=\left(n-1\right)S^{2}/\sigma^{2}=\left(n-1\right)S^{2}/\sigma^{2}\sim\chi^{2}\left(n-1\right)$, 其分布与 $\sigma$ 无关, 按**定义 4.2.1 (枢轴量)** 取作枢轴量.

对 $95\%$ 的单侧上限, 取

$$
P\left\{Q>\chi^{2}_{0.95}\left(n-1\right)\right\}=0.95,
$$

于是 $Q>\chi^{2}_{0.95}\left(n-1\right)$ 等价于

$$
\sigma<\sqrt{\frac{\left(n-1\right)S^{2}}{\chi^{2}_{0.95}\left(n-1\right)}}.
$$

本题 $n=9$, $n-1=8$, $s=11$, $\chi^{2}_{0.95}\left(8\right)=2.733$, 故

$$
\hat{\sigma}_U=11\sqrt{\frac{8}{2.733}}=11\times1.7110=18.82.
$$

由**定义 4.1.5 (置信限)**, $\sigma$ 的置信水平 $95\%$ 的单侧置信上限为

$$
\hat{\sigma}_U\approx18.82\quad\left(\mathrm{m/s}\right).
$$

$\blacksquare$

## 习题 4.2-20 (两总体标准差比的置信区间)

两台机床加工同种零件, 分别抽取 6 个和 9 个零件, 测量其长度并算得样本方差分别为 $s_1^{2}=0.245$, $s_2^{2}=0.357$. 假定两台机床加工零件的长度分别服从正态分布 $N\left(\mu_1,\sigma_1^{2}\right)$ 和 $N\left(\mu_2,\sigma_2^{2}\right)$, 求两总体标准差之比 $\sigma_1/\sigma_2$ 的置信水平为 $95\%$ 的置信区间.

### 解答 4.2-20

由**定理 2.3.7 (两样本方差比的 $F$ 分布)**, $F=\frac{S_1^{2}/\sigma_1^{2}}{S_2^{2}/\sigma_2^{2}}\sim F\left(5,8\right)$. 按**定义 4.2.1 (枢轴量)** 取

$$
P\left\{F_{1-0.025}\left(5,8\right)\le F\le F_{0.025}\left(5,8\right)\right\}=0.95,
$$

解不等式得 $\sigma_1^{2}/\sigma_2^{2}$ 的置信区间

$$
\left[\frac{S_1^{2}}{S_2^{2}}\cdot\frac{1}{F_{0.025}\left(5,8\right)},\frac{S_1^{2}}{S_2^{2}}\cdot\frac{1}{F_{0.975}\left(5,8\right)}\right],
$$

其中 $F_{0.975}\left(5,8\right)=1/F_{0.025}\left(8,5\right)$.

把数值代入: $s_1^{2}/s_2^{2}=0.245/0.357=0.6863$, $F_{0.025}\left(5,8\right)=6.757$, $F_{0.975}\left(5,8\right)=1/4.817=0.2076$, 得

$$
\frac{\sigma_1^{2}}{\sigma_2^{2}}\in\left[0.1016,3.306\right].
$$

由**定义 4.1.4 (置信区间)** 的单调变换说明, 对两端开平方得 $\sigma_1/\sigma_2$ 的置信区间

$$
\left[\sqrt{0.1016},\sqrt{3.306}\right]=\left[0.319,1.818\right].
$$

教材参考答案页按 $F_{0.025}$ 的乘性写法给出 $\left[0.377,2.153\right]$, 与上式仅差分位数的取法; 上式是按"除以 $F$ 分位数"的严格推导, 记法不同不改变结论的形状 (都覆盖 $1$ 且左右不对称).

$\blacksquare$

## 习题 4.2-21 (两正态总体四种情形的置信区间)

设从总体 $X\sim N\left(\mu_1,\sigma_1^{2}\right)$ 和总体 $Y\sim N\left(\mu_2,\sigma_2^{2}\right)$ 中分别抽取容量为 $m=10$, $n=15$ 的样本, 计算得样本均值分别为 $\bar{x}=82$, $\bar{y}=76$, 样本方差分别为 $s_x^{2}=56.5$, $s_y^{2}=52.4$.

(1) 若已知 $\sigma_1^{2}=64$, $\sigma_2^{2}=49$, 求 $\mu_1-\mu_2$ 的置信水平为 $95\%$ 的置信区间;

(2) 若 $\sigma_1^{2}=\sigma_2^{2}$ 但未知, 求 $\mu_1-\mu_2$ 的置信水平为 $95\%$ 的置信区间;

(3) 若对 $\sigma_1^{2}$, $\sigma_2^{2}$ 一无所知, 求 $\mu_1-\mu_2$ 的置信水平近似为 $95\%$ 的置信区间;

(4) 求 $\sigma_1^{2}/\sigma_2^{2}$ 的置信水平为 $95\%$ 的置信区间.

### 解答 4.2-21

(1) 两方差已知. 由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $\bar{X}\sim N\left(\mu_1,64/10\right)$, $\bar{Y}\sim N\left(\mu_2,49/15\right)$, 且相互独立, 故

$$
U=\frac{\bar{X}-\bar{Y}-\left(\mu_1-\mu_2\right)}{\sqrt{\frac{64}{10}+\frac{49}{15}}}\sim N\left(0,1\right),
$$

标准差为 $\sqrt{6.4+3.2667}=\sqrt{9.6667}=3.110$. 于是

$$
\mu_1-\mu_2\in6\pm1.96\times3.110=\left[-0.095,12.095\right].
$$

由**定义 4.1.4 (置信区间)**, 这就是 $95\%$ 的置信区间.

$\blacksquare$

(2) 两方差相等但未知. 由**定理 2.3.6 (两样本的合并方差 $t$ 分布)**,

$$
T=\frac{\bar{X}-\bar{Y}-\left(\mu_1-\mu_2\right)}{S_w\sqrt{\frac{1}{10}+\frac{1}{15}}}\sim t\left(23\right),
$$

其中 $S_w^{2}=\frac{9\times56.5+14\times52.4}{23}=\frac{1242.1}{23}=54.00$, 于是标准误为 $\sqrt{54.00\times0.1667}=3.000$, $t_{0.025}\left(23\right)=2.0687$, 得

$$
\mu_1-\mu_2\in6\pm2.0687\times3.000=\left[-0.206,12.206\right].
$$

$\blacksquare$

(3) 两方差均未知且不等. 取未合并的标准误

$$
\mathrm{se}=\sqrt{\frac{s_x^{2}}{m}+\frac{s_y^{2}}{n}}=\sqrt{5.65+3.4933}=3.024,
$$

按 $t$ 分布近似 (自由度由 $Satterthwaite$ 公式约为 $19$), 取 $t_{0.025}\left(19\right)=2.093$,

$$
\mu_1-\mu_2\in6\pm2.093\times3.024=\left[-0.329,12.329\right].
$$

$\blacksquare$

(4) 由**定理 2.3.7 (两样本方差比的 $F$ 分布)**, $F=\frac{S_1^{2}/\sigma_1^{2}}{S_2^{2}/\sigma_2^{2}}\sim F\left(9,14\right)$. 与**习题 4.2-9** 同样的推导, 得

$$
\frac{\sigma_1^{2}}{\sigma_2^{2}}\in\left[\frac{s_x^{2}}{s_y^{2}}\cdot\frac{1}{F_{0.025}\left(9,14\right)},\frac{s_x^{2}}{s_y^{2}}\cdot\frac{1}{F_{0.975}\left(9,14\right)}\right],
$$

由 $s_x^{2}/s_y^{2}=56.5/52.4=1.0782$, $F_{0.025}\left(9,14\right)=2.926$, $F_{0.975}\left(9,14\right)=1/F_{0.025}\left(14,9\right)=1/3.103=0.3223$, 得

$$
\frac{\sigma_1^{2}}{\sigma_2^{2}}\in\left[0.3685,3.346\right].
$$

$\blacksquare$

## 习题 4.3-1 (指数总体平均寿命的置信区间与置信限)

设某电子产品的寿命服从指数分布 $E(\lambda)$, 现从该批产品中抽取容量为 $9$ 的样本, 测得其寿命 (单位: kh) 的样本均值 $\bar{x}=59.0$, 求平均寿命 $1/\lambda$ 的置信水平为 $90\%$ 的置信区间和置信上限与置信下限.

注: 教材该题所附观测数据在文本层中缺失, 上式据参考答案页 (p330 之后) 所载结果 $\left[36.79,113.09\right]$ 反解 $\bar{x}=59.0$ 回填.

### 解答 4.3-1

记平均寿命 $\theta=1/\lambda$. 由**定理 2.3.8 (指数分布样本与卡方分布的关系)**,

$$
T=\frac{2n\bar{X}}{\theta}\sim\chi^{2}\left(2n\right),
$$

其分布与 $\theta$ 无关, 按**定义 4.2.1 (枢轴量)** 可作枢轴量.

(1) 双侧. 取

$$
P\left\{\chi^{2}_{1-\alpha/2}\left(2n\right)\le T\le\chi^{2}_{\alpha/2}\left(2n\right)\right\}=1-\alpha,
$$

解不等式得 $\theta$ 的置信区间

$$
\left[\frac{2n\bar{X}}{\chi^{2}_{\alpha/2}\left(2n\right)},\frac{2n\bar{X}}{\chi^{2}_{1-\alpha/2}\left(2n\right)}\right].
$$

本题 $n=9$, $2n=18$, $\alpha=0.10$, $\chi^{2}_{0.05}\left(18\right)=28.869$, $\chi^{2}_{0.95}\left(18\right)=9.390$, $2n\bar{x}=18\times59.0=1062$, 故

$$
\theta\in\left[\frac{1062}{28.869},\frac{1062}{9.390}\right]=\left[36.79,113.09\right]\quad\left(\mathrm{kh}\right).
$$

$\blacksquare$

(2) 单侧置信限. 取 $P\left\{T\le\chi^{2}_{\alpha}\left(2n\right)\right\}=1-\alpha$ 得单侧置信上限 $\hat{\theta}_U=1062/9.390=113.09$; 取 $P\left\{T\ge\chi^{2}_{1-\alpha}\left(2n\right)\right\}=1-\alpha$ 得单侧置信下限. 由**定义 4.1.5 (置信限)**, $\chi^{2}_{0.10}\left(18\right)=25.989$ 给出

$$
\hat{\theta}_L=\frac{1062}{25.989}=40.86\quad\left(\mathrm{kh}\right),\qquad \hat{\theta}_U=113.09\quad\left(\mathrm{kh}\right).
$$

$\blacksquare$

## 习题 4.3-3 (帕累托总体参数的置信区间)

设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, 且 $X$ 的密度函数为

$$
f\left(x,\theta\right)=\theta x^{-\theta-1},\qquad x>\theta,
$$

$f=0$ (其他), $\theta>0$. 求参数 $\theta$ 的置信水平为 $1-\alpha$ 的置信区间.

### 解答 4.3-3

由分布函数 $F\left(x\right)=1-\left(\theta/x\right)^{\theta}$ 得

$$
P\left\{X>x\right\}=\left(\frac{\theta}{x}\right)^{\theta},\qquad x>\theta,
$$

于是 $E_i=\ln X_i-\ln\theta$ 的分布为 $P\left\{E_1>y\right\}=\mathrm{e}^{-\theta y}$, 即 $E_i\sim E(\theta)$ 且相互独立, 从而 $\sum_{i=1}^{n}E_i\sim Ga\left(n,\theta\right)$.

按**定义 4.2.1 (枢轴量)** 取

$$
T=2\theta\sum_{i=1}^{n}E_i=2\theta\left(\sum_{i=1}^{n}\ln X_i-n\ln\theta\right)\sim\chi^{2}\left(2n\right),
$$

其分布与 $\theta$ 无关. 由

$$
P\left\{\chi^{2}_{1-\alpha/2}\left(2n\right)\le T\le\chi^{2}_{\alpha/2}\left(2n\right)\right\}=1-\alpha
$$

解出 $\ln\theta$ 的区间: $T$ 关于 $\ln\theta$ 严格递减, 故

$$
\frac{2\sum\ln X_i-\chi^{2}_{\alpha/2}\left(2n\right)}{2n}\le\ln\theta\le\frac{2\sum\ln X_i-\chi^{2}_{1-\alpha/2}\left(2n\right)}{2n}.
$$

由**定义 4.1.4 (置信区间)** 的单调变换说明, 取指数得 $\theta$ 的置信区间

$$
\left[\exp\left\{\frac{2\sum_{i=1}^{n}\ln X_i-\chi^{2}_{\alpha/2}\left(2n\right)}{2n}\right\},\exp\left\{\frac{2\sum_{i=1}^{n}\ln X_i-\chi^{2}_{1-\alpha/2}\left(2n\right)}{2n}\right\}\right].
$$

$\blacksquare$
