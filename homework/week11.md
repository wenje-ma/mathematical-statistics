# week11

> **定理 2.3.3 (正态总体样本均值与样本方差的分布)**
> 
> 设 $X_1,\ldots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^{2}\right)$ 的样本, $\bar{X}$ 与 $S^{2}$ 分别为样本均值与样本方差, 则 $\bar{X}\sim{}N\left(\mu,\sigma^{2}/n\right)$, $\left(n-1\right)S^{2}/\sigma^{2}\sim\chi^{2}\left(n-1\right)$, 且 $\bar{X}$ 与 $S^{2}$ 相互独立. (教材 $\S2.3$, p43)

> **定理 2.3.8 (指数分布样本与卡方分布的关系)**
> 
> 设 $X_1,\ldots,X_n$ 是来自指数分布 $E\left(\lambda\right)$ 的样本, 则 $2\lambda{}n\bar{X}\sim\chi^{2}\left(2n\right)$. (教材 $\S2.3$, p47)

> **定义 4.1.4 (置信区间)**
> 
> 设 $\left[\hat{\theta}_1,\hat{\theta}_2\right]$ 是 $\theta$ 的区间估计, 对给定 $0<\alpha<1$, 若对任意 $\theta\in\Theta$ 都有 $P_{\theta}\left\{\hat{\theta}_1\le\theta\le\hat{\theta}_2\right\}\ge1-\alpha$, 则称其为 $\theta$ 的置信水平为 $1-\alpha$ 的置信区间. (教材 $\S4.1$, p123)

> **定义 4.2.1 (枢轴量)**
> 
> 令 $G\left(X_1,\ldots,X_n,\theta\right)$ 是样本与参数 $\theta$ 的可测函数, 当且仅当 $G$ 的分布不依赖于 $\theta$ 时称之为枢轴量; 若 $g\left(\theta\right)$ 关于 $\theta$ 单调, 则 $\theta$ 的置信区间可逐端变换为 $g\left(\theta\right)$ 的置信区间. (教材 $\S4.2$, p127)

> **定义 5.1.1 (功效函数)**
> 
> 设 $\varphi\left(x\right)$ 是检验问题 $H_0:\theta\in\Theta_0$; $H_1:\theta\in\Theta_1$ 的一个检验函数, 则 $\gamma_{\varphi}\left(\theta\right)=P_{\theta}\left\{\varphi\text{~拒绝~}H_0\right\}=E_{\theta}\left[\varphi\left(X\right)\right]$, $\theta\in\Theta$ 称为 $\varphi$ 的功效函数 (势函数). 当 $\theta\in\Theta_0$ 时 $\gamma_{\varphi}\left(\theta\right)$ 是犯第一类错误的概率, 当 $\theta\in\Theta_1$ 时 $1-\gamma_{\varphi}\left(\theta\right)$ 是犯第二类错误的概率. (教材 $\S5.1$, p151)

> **定义 5.1.2 (显著性检验)**
> 
> 设 $\varphi\left(x\right)$ 是检验问题 $H_0:\theta\in\Theta_0$; $H_1:\theta\in\Theta_1$ 的检验函数, $0\le\alpha\le1$. 若对一切 $\theta\in\Theta_0$ 都有 $\gamma_{\varphi}\left(\theta\right)\le\alpha$, 则称 $\alpha$ 是 $\varphi$ 的一个水平, $\varphi$ 为水平为 $\alpha$ 的显著性检验. (教材 $\S5.1$, p151)

## 习题 4.3-4 (瑞利型总体的参数置信区间)

设 $X_1,X_2,\ldots,X_n$ 是来自总体 $X$ 的样本, 且 $X$ 的密度函数为 $f\left(x\right)=2\lambda{}x\mathrm{e}^{-\lambda{}x^{2}}$ ($x>0$), $f=0$ ($x\le0$), 求参数 $\lambda$ 的置信水平为 $1-\alpha$ 的置信区间.

### 解答 4.3-4

作变换 $Y=X^{2}$, 则 $Y$ 的密度为 $\lambda\mathrm{e}^{-\lambda{}y}$ ($y>0$), 即 $Y_1,\ldots,Y_n$ 是来自 $E\left(\lambda\right)$ 的样本, $Y_i=X_i^{2}$.

由**定理 2.3.8 (指数分布样本与卡方分布的关系)**,

$$
T=2\lambda\sum_{i=1}^{n}Y_i=2\lambda\sum_{i=1}^{n}X_i^{2}\sim\chi^{2}\left(2n\right),
$$

其分布与 $\lambda$ 无关, 按**定义 4.2.1 (枢轴量)** 可作枢轴量. 由

$$
P\left\{\chi^{2}_{1-\alpha/2}\left(2n\right)\le{}T\le\chi^{2}_{\alpha/2}\left(2n\right)\right\}=1-\alpha
$$

解出 $\lambda$ 的区间:

$$
\frac{\chi^{2}_{1-\alpha/2}\left(2n\right)}{2\sum_{i=1}^{n}X_i^{2}}\le\lambda\le\frac{\chi^{2}_{\alpha/2}\left(2n\right)}{2\sum_{i=1}^{n}X_i^{2}}.
$$

由**定义 4.1.4 (置信区间)**, 这就是 $\lambda$ 的置信水平为 $1-\alpha$ 的置信区间.

$\blacksquare$

## 习题 4.3-10 (不合格品率的大样本置信区间)

在一批货物中随机抽取 $100$ 件, 发现有 $16$ 件不合格品, 求这批货物的不合格品率的置信水平近似为 $95\%$ 的置信区间.

### 解答 4.3-10

记不合格品率为 $p$, 样本不合格品率 $\hat{p}=16/100=0.16$. 由中心极限定理, $\hat{p}$ 近似服从

$$
N\left(p,\frac{p\left(1-p\right)}{n}\right),
$$

故枢轴量 $\frac{\hat{p}-p}{\sqrt{\hat{p}\left(1-\hat{p}\right)/n}}$ 近似服从 $N\left(0,1\right)$. 按**定义 4.2.1 (枢轴量)** 取近似 $1-\alpha$ 区间, 再把 $\hat{p}$ 代入得

$$
\left[\hat{p}-u_{\alpha/2}\sqrt{\frac{\hat{p}\left(1-\hat{p}\right)}{n}},\hat{p}+u_{\alpha/2}\sqrt{\frac{\hat{p}\left(1-\hat{p}\right)}{n}}\right].
$$

本题 $\hat{p}=0.16$, $n=100$, $u_{0.025}=1.96$, 标准差 $\sqrt{0.16\times0.84/100}=\sqrt{0.001344}=0.03666$, 故

$$
p\in0.16\pm1.96\times0.03666=\left[0.088,0.232\right].
$$

由**定义 4.1.4 (置信区间)**, 这就是不合格品率置信水平近似 $95\%$ 的置信区间.

$\blacksquare$

## 习题 5.1-5 (正态均值的简单检验的两类错误与样本容量)

设 $X_1,X_2,\ldots,X_n$ 是来自正态总体 $N\left(\mu,1\right)$ 的样本, $\mu\in\mathbb{R}$ 未知, 检验问题 $H_0:\mu=0$; $H_1:\mu=1$ 的拒绝域为

$$
D=\left\{\bar{X}\ge0.98\right\}.
$$

(1) 若 $n=4$, 求该检验犯第一类错误的概率和犯第二类错误的概率;

(2) 若要使该检验犯第一类错误的概率不超过 $0.01$, 样本容量 $n$ 最少取多少?

### 解答 5.1-5

记 $\gamma\left(\mu\right)=P_{\mu}\left\{\bar{X}\ge0.98\right\}$, 它为**定义 5.1.1 (功效函数)** 中的功效函数; 由**定义 5.1.2 (显著性检验)**, $\gamma\left(0\right)$ 即水平, $1-\gamma\left(1\right)$ 即第二类错误概率.

(1) 由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $\bar{X}\sim{}N\left(\mu,1/n\right)$. 当 $n=4$ 时 $\bar{X}\sim{}N\left(\mu,1/4\right)$,

$$
\alpha=\gamma\left(0\right)=1-\Phi\left(\frac{0.98-0}{1/2}\right)=1-\Phi\left(1.96\right)=0.025,
$$

$$
\beta=1-\gamma\left(1\right)=P_{1}\left\{\bar{X}<0.98\right\}=\Phi\left(\frac{0.98-1}{1/2}\right)=\Phi\left(-0.04\right)=0.484.
$$

$\blacksquare$

(2) 一般地

$$
\alpha\left(n\right)=1-\Phi\left(0.98\sqrt{n}\right).
$$

要求 $\alpha\left(n\right)\le0.01$, 即 $\Phi\left(0.98\sqrt{n}\right)\ge0.99$, 故 $0.98\sqrt{n}\ge{}u_{0.01}=2.326$, $\sqrt{n}\ge2.3734$, $n\ge5.633$. 最小样本容量为

$$
n=6.
$$

$\blacksquare$

## 习题 5.1-7 (容量为一的样本的两类错误)

设样本 $X$ (容量为 $1$) 取自具有密度函数 $f\left(x\right)$ 的总体, 关于总体的两个假设为

$$
H_0:\,f\left(x\right)=1\,\left(0<{}x<1\right);\quad{}H_1:\,f\left(x\right)=2x\,\left(0<{}x<1\right),
$$

该检验的拒绝域为 $D=\left\{X>2/3\right\}$, 求该检验犯第一类错误的概率和犯第二类错误的概率.

### 解答 5.1-7

由**定义 5.1.1 (功效函数)**,

$$
\alpha=P_{H_0}\left\{X>\frac{2}{3}\right\}=\int_{2/3}^{1}1\,\mathrm{d}x=\frac{1}{3},
$$

$$
\beta=P_{H_1}\left\{X\le\frac{2}{3}\right\}=\int_{0}^{2/3}2x\,\mathrm{d}x=\left(\frac{2}{3}\right)^{2}=\frac{4}{9}.
$$

$\blacksquare$

## 习题 5.1-8 (均匀总体最大值检验的水平与功效函数)

设 $X_1,X_2,\ldots,X_{10}$ 是来自均匀分布总体 $U\left[0,\theta\right]$ 的样本, $\theta>0$ 未知, 检验问题 $H_0:\theta=1$; $H_1:\theta>1$ 的拒绝域为

$$
D=\left\{X_{\left(10\right)}\ge0.95\right\},\quad{}X_{\left(10\right)}=\max\left\{X_1,\ldots,X_{10}\right\}.
$$

(1) 求该检验的显著性水平;

(2) 求该检验的功效函数.

### 解答 5.1-8

$U\left[0,\theta\right]$ 的分布函数为 $F\left(x\right)=x/\theta$ ($0\le{}x\le\theta$), 故

$$
P_{\theta}\left\{X_{\left(10\right)}<{}y\right\}=\left(\frac{y}{\theta}\right)^{10},\quad0<{}y\le\theta.
$$

(1) 由**定义 5.1.1 (功效函数)**,

$$
\alpha=P_{1}\left\{X_{\left(10\right)}\ge0.95\right\}=1-0.95^{10}=1-0.5987=0.4013.
$$

$\blacksquare$

(2) 对 $\theta>1$ (即 $\theta\in\Theta_1$), 功效函数为

$$
\gamma\left(\theta\right)=P_{\theta}\left\{X_{\left(10\right)}\ge0.95\right\}=1-\left(\frac{0.95}{\theta}\right)^{10},\quad\theta>0.95,
$$

在 $\Theta_1=\left(1,+\infty\right)$ 上取值于 $\left(\gamma\left(1\right),1\right)$, 且

$$
1-\gamma\left(\theta\right)=P_{\theta}\left\{X_{\left(10\right)}<0.95\right\}
$$

即犯第二类错误的概率. 由**定义 5.1.2 (显著性检验)**, 该检验在 $\Theta_1$ 上的功效严格大于其水平.

$\blacksquare$

## 习题 5.2-5 (方差已知时正态均值的 $u$ 检验)

从标准差为 $\sigma=5.2$ 的正态总体 $N\left(\mu,\sigma^{2}\right)$ 中随机抽取容量为 $16$ 的样本, 计算得样本均值 $\bar{x}=27.56$, 在显著性水平 $\alpha=0.05$ 下, 能否认为总体均值 $\mu=26$?

### 解答 5.2-5

检验问题 $H_0:\mu=26$; $H_1:\mu\ne26$, 方差已知, 取 $u$ 检验. 由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $H_0$ 成立时

$$
U=\frac{\bar{X}-26}{\sigma/\sqrt{n}}\sim{}N\left(0,1\right).
$$

代入 $\bar{X}=27.56$, $\sigma=5.2$, $n=16$:

$$
u=\frac{27.56-26}{5.2/4}=\frac{1.56}{1.30}=1.200.
$$

由**定义 5.1.2 (显著性检验)**, $\alpha=0.05$ 的双边 $u$ 检验拒绝域为 $\left|U\right|\ge{}u_{0.025}=1.96$. 因 $\left|1.200\right|<1.96$, 落在接受域内, 故不拒绝 $H_0$, 即在 $\alpha=0.05$ 下可以认为 $\mu=26$.

$\blacksquare$

## 习题 5.2-7 (方差已知时正态均值的单侧 $u$ 检验)

要求一种元件的平均使用寿命不得低于 $1000$ h, 生产者从这种元件中随机抽取 $25$ 件, 测得其寿命的平均值为 $950$ h. 已知该种元件寿命服从标准差为 $\sigma=100$ h 的正态分布, 在显著性水平 $\alpha=0.05$ 下, 判断这批元件是否合格?

### 解答 5.2-7

"不得低于 $1000$ h" 是生产者的承诺, 故取

$$
H_0:\mu\ge1000;\quad{}H_1:\mu<1000,
$$

把"不合格"放在备择假设一侧. 方差已知, 由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $H_0$ 成立时

$$
U=\frac{\bar{X}-1000}{\sigma/\sqrt{n}}\sim{}N\left(0,1\right)\quad\left(\text{当~}\mu=1000\right),
$$

且 $\mu>1000$ 时 $U$ 更小地偏向右侧, 故拒绝域取 $U\le-u_{0.05}$ 即可保证水平 $0.05$ (见**定义 5.1.2 (显著性检验)**). 代入 $\bar{x}=950$, $\sigma=100$, $n=25$:

$$
u=\frac{950-1000}{100/5}=\frac{-50}{20}=-2.50.
$$

因 $-2.50<-u_{0.05}=-1.645$, 拒绝 $H_0$, 即认为这批元件的平均寿命低于 $1000$ h, 不合格.

$\blacksquare$

## 习题 5.2-9 (由临界值求第二类错误概率)

设 $X_1,X_2,\ldots,X_{25}$ 是来自正态总体 $N\left(\mu,3^{2}\right)$ 的一个样本, $\mu\in\mathbb{R}$ 未知. 检验问题 $H_0:\mu=\mu_0$; $H_1:\mu\ne\mu_0$ ($\mu_0$ 已知) 的拒绝域为

$$
D=\left\{\left|\bar{X}-\mu_0\right|\ge{}c\right\}.
$$

(1) 在显著性水平 $\alpha=0.05$ 下, 求常数 $c$;

(2) 求 $\mu=\mu_1$ ($\mu_1\ne\mu_0$) 时犯第二类错误的概率 (用标准正态分布函数 $\Phi$ 表示).

### 解答 5.2-9

(1) $H_0$ 成立时, 由**定理 2.3.3 (正态总体样本均值与样本方差的分布)**, $\bar{X}\sim{}N\left(\mu_0,9/25\right)$, 标准差为 $3/5=0.6$, 故

$$
\alpha=P\left\{\left|\bar{X}-\mu_0\right|\ge{}c\right\}=2\left[1-\Phi\left(\frac{c}{0.6}\right)\right].
$$

要求 $\alpha=0.05$, 即 $\Phi\left(c/0.6\right)=0.975$, $\frac{c}{0.6}=u_{0.025}=1.96$,

$$
c=1.96\times0.6=1.176.
$$

由**定义 5.1.2 (显著性检验)**, 该拒绝域给出水平 $0.05$ 的检验.

$\blacksquare$

(2) 记 $\delta=\mu_1-\mu_0\ne0$. 当 $\mu=\mu_1$ 时 $\bar{X}\sim{}N\left(\mu_1,0.36\right)$, 第二类错误概率

$$
\beta=P_{\mu_1}\left\{\left|\bar{X}-\mu_0\right|<{}c\right\}=P\left\{-c<\bar{X}-\mu_0<{}c\right\}.
$$

把 $\bar{X}-\mu_0=\delta+\left(\bar{X}-\mu_1\right)$ 代入并标准化:

$$
\beta=\Phi\left(\frac{c-\delta}{0.6}\right)-\Phi\left(\frac{-c-\delta}{0.6}\right)=\Phi\left(1.96-\frac{\delta}{0.6}\right)-\Phi\left(-1.96-\frac{\delta}{0.6}\right).
$$

$\blacksquare$
