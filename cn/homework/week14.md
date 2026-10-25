# 作业 14

> **定义 4.2.1**（枢轴量）<br>令 $G\left(X_1,X_2,\dots,X_n,\theta\right)$ 是样本 $\left(X_1,X_2,\dots,X_n\right)$ 和参数 $\theta$ 的一个可测函数，当且仅当 $G\left(X_1,X_2,\dots,X_n,\theta\right)$ 的分布不依赖于参数 $\theta$ 时，$G\left(X_1,X_2,\dots,X_n,\theta\right)$ 被称为枢轴量.

> **定理**（单个正态总体均值的置信区间）<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，$\bar X=\frac{1}{n}\sum_{i=1}^n X_i$，$S^2=\frac{1}{n-1}\sum_{i=1}^n\left(X_i-\bar X\right)^2$. 当 $\sigma^2$ 已知时，$\mu$ 的置信水平为 $1-\alpha$ 的置信区间为 $\left[\bar X-\frac{\sigma}{\sqrt n}u_{\alpha/2},\bar X+\frac{\sigma}{\sqrt n}u_{\alpha/2}\right]$；当 $\sigma^2$ 未知时，$\mu$ 的置信水平为 $1-\alpha$ 的置信区间为 $\left[\bar X-\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right),\bar X+\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right)\right]$.

> **定理**（单个正态总体方差的置信区间）<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，当 $\mu$ 未知时，$\sigma^2$ 的置信水平为 $1-\alpha$ 的置信区间为 $$\left[\frac{\left(n-1\right)S^2}{\chi^2_{\alpha/2}\left(n-1\right)},\frac{\left(n-1\right)S^2}{\chi^2_{1-\alpha/2}\left(n-1\right)}\right],$$ 其中 $\chi^2_\alpha\left(n-1\right)$ 表示自由度为 $n-1$ 的 $\chi^2$ 分布的上 $\alpha$ 分位数. 相应地，$\sigma$ 的置信水平为 $1-\alpha$ 的置信区间为上述区间端点的平方根.

> **定理**（两个正态总体均值差的置信区间）<br>设 $X_1,X_2,\dots,X_m$ 是来自 $N\left(\mu_1,\sigma_1^2\right)$ 的样本，$Y_1,Y_2,\dots,Y_n$ 是来自 $N\left(\mu_2,\sigma_2^2\right)$ 的样本，两样本独立，$\bar X,\bar Y$ 为样本均值，$S_1^2,S_2^2$ 为样本方差. 当 $\sigma_1^2,\sigma_2^2$ 均已知时，$\mu_2-\mu_1$ 的置信区间为 $\left[\bar Y-\bar X-u_{\alpha/2}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}},\bar Y-\bar X+u_{\alpha/2}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}\right]$；当 $\sigma_1^2=\sigma_2^2=\sigma^2$ 未知时，$\mu_2-\mu_1$ 的置信区间为 $\left[\bar Y-\bar X-S_w t_{\alpha/2}\left(m+n-2\right)\sqrt{\frac{1}{m}+\frac{1}{n}},\bar Y-\bar X+S_w t_{\alpha/2}\left(m+n-2\right)\sqrt{\frac{1}{m}+\frac{1}{n}}\right]$，其中 $S_w^2=\frac{\left(m-1\right)S_1^2+\left(n-1\right)S_2^2}{m+n-2}$；当 $\sigma_1^2\ne\sigma_2^2$ 未知时，可用 Welch 近似：$\left[\bar Y-\bar X-t_{\alpha/2}\left(r\right)\sqrt{\frac{S_1^2}{m}+\frac{S_2^2}{n}},\bar Y-\bar X+t_{\alpha/2}\left(r\right)\sqrt{\frac{S_1^2}{m}+\frac{S_2^2}{n}}\right]$，其中 $r=\frac{\left(S_1^2/m+S_2^2/n\right)^2}{\frac{\left(S_1^2/m\right)^2}{m-1}+\frac{\left(S_2^2/n\right)^2}{n-1}}$.

> **定理**（两个正态总体方差比的置信区间）<br>设两总体均值均未知，则 $\frac{\sigma_1^2}{\sigma_2^2}$ 的置信水平为 $1-\alpha$ 的置信区间为 $$\left[\frac{S_1^2/S_2^2}{F_{\alpha/2}\left(m-1,n-1\right)},\frac{S_1^2/S_2^2}{F_{1-\alpha/2}\left(m-1,n-1\right)}\right],$$ 其中 $F_{\alpha/2}\left(m-1,n-1\right)$ 表示 $F$ 分布的上 $\alpha/2$ 分位数.

### 习题一

（习题 4.2-3）设 $X_1,X_2,\dots,X_{21}$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，计算得样本均值 $\bar{x}=32.295$，样本标准差 $s=0.343$.

(1) 若 $\sigma$ 未知，求 $\mu$ 的置信水平为 $95\%$ 的置信区间；

(2) 若 $\sigma$ 未知，求 $\mu$ 的置信水平为 $99\%$ 的置信区间.

### 解答 习题一

由**定理**（单个正态总体均值的置信区间），当 $\sigma^2$ 未知时，$\mu$ 的置信水平为 $1-\alpha$ 的置信区间为 $\left[\bar X-\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right),\bar X+\frac{S}{\sqrt n}t_{\alpha/2}\left(n-1\right)\right]$.

本题中 $n=21$，$\bar{x}=32.295$，$s=0.343$，自由度 $n-1=20$.

(1) 置信水平为 $95\%$，即 $\alpha=0.05$，查 $t$ 分布表得 $t_{0.025}\left(20\right)=2.086$. 计算得

$$
\frac{s}{\sqrt n}t_{0.025}\left(20\right)=\frac{0.343}{\sqrt{21}}\times2.086=0.156.
$$

故 $\mu$ 的 $95\%$ 置信区间为

$$
\left[32.295-0.156,\ 32.295+0.156\right]=\left[32.139,\ 32.451\right].
$$

(2) 置信水平为 $99\%$，即 $\alpha=0.01$，查 $t$ 分布表得 $t_{0.005}\left(20\right)=2.845$. 计算得

$$
\frac{s}{\sqrt n}t_{0.005}\left(20\right)=\frac{0.343}{\sqrt{21}}\times2.845=0.213.
$$

故 $\mu$ 的 $99\%$ 置信区间为

$$
\left[32.295-0.213,\ 32.295+0.213\right]=\left[32.082,\ 32.508\right].
$$

$\blacksquare$

### 习题二

（习题 4.2-5）设总体 $X\sim N\left(\mu,\sigma_0^2\right)$，其中 $\sigma_0$ 已知. 为使 $\mu$ 的置信水平为 $1-\alpha$ 的置信区间长度不超过给定值 $k$，求样本容量 $n$ 至少应取多少.

### 解答 习题二

由**定义 4.2.1**（枢轴量），当 $\sigma^2$ 已知时，枢轴量为 $U=\frac{\sqrt n\left(\bar X-\mu\right)}{\sigma_0}\sim N\left(0,1\right)$. 由**定理**（单个正态总体均值的置信区间），$\mu$ 的置信水平为 $1-\alpha$ 的置信区间为

$$
\left[\bar X-\frac{\sigma_0}{\sqrt n}u_{\alpha/2},\ \bar X+\frac{\sigma_0}{\sqrt n}u_{\alpha/2}\right].
$$

该区间的长度为

$$
l=\frac{2\sigma_0}{\sqrt n}u_{\alpha/2}.
$$

要求 $l\le k$，即

$$
\frac{2\sigma_0}{\sqrt n}u_{\alpha/2}\le k.
$$

解此不等式得

$$
\sqrt n\ge\frac{2\sigma_0}{k}u_{\alpha/2},\quad n\ge\left(\frac{2\sigma_0}{k}u_{\alpha/2}\right)^2.
$$

由于样本容量 $n$ 必须为正整数，故

$$
n=\begin{cases}
\left(\frac{2\sigma_0}{k}u_{\alpha/2}\right)^2,&\text{若 }\left(\frac{2\sigma_0}{k}u_{\alpha/2}\right)^2\text{ 为整数},\\[6pt\right]
\left\lfloor\left(\frac{2\sigma_0}{k}u_{\alpha/2}\right)^2\right\rfloor+1,&\text{若 }\left(\frac{2\sigma_0}{k}u_{\alpha/2}\right)^2\text{ 不是整数}.
\end{cases}
$$

$\blacksquare$

### 习题三

（习题 4.2-9）设 $X_1,X_2,\dots,X_{10}$ 是来自正态总体 $N\left(\mu_1,\sigma_1^2\right)$ 的样本，$Y_1,Y_2,\dots,Y_{13}$ 是来自正态总体 $N\left(\mu_2,\sigma_2^2\right)$ 的样本，两样本独立. 计算得样本方差之比 $\frac{s_1^2}{s_2^2}=0.083$. 求 $\frac{\sigma_1^2}{\sigma_2^2}$ 的置信水平为 $95\%$ 的置信区间.

### 解答 习题三

由**定理**（两个正态总体方差比的置信区间），当两总体均值均未知时，$\frac{\sigma_1^2}{\sigma_2^2}$ 的置信水平为 $1-\alpha$ 的置信区间为

$$
\left[\frac{S_1^2/S_2^2}{F_{\alpha/2}\left(m-1,n-1\right)},\ \frac{S_1^2/S_2^2}{F_{1-\alpha/2}\left(m-1,n-1\right)}\right].
$$

本题中 $m=10$，$n=13$，$\frac{s_1^2}{s_2^2}=0.083$，$\alpha=0.05$，查 $F$ 分布表得

$$
F_{0.025}\left(9,12\right)=3.436,\quad F_{0.975}\left(9,12\right)=\frac{1}{F_{0.025}\left(12,9\right)}=0.291.
$$

代入公式得置信下限为

$$
\frac{0.083}{3.436}=0.024,
$$

置信上限为

$$
\frac{0.083}{0.291}=0.285.
$$

故 $\frac{\sigma_1^2}{\sigma_2^2}$ 的 $95\%$ 置信区间为 $\left[0.024,\ 0.283\right]$. $\blacksquare$

### 习题四

（习题 4.2-11）设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，$a,b$ 为常数，且 $0< a< b$，求随机区间 $\left[\frac{\left(n-1\right)S^2}{b\sigma^2},\frac{\left(n-1\right)S^2}{a\sigma^2}\right]$ 的长度 $L$ 的数学期望和方差.

### 解答 习题四

该随机区间为 $\left[\frac{\left(n-1\right)S^2}{b\sigma^2},\frac{\left(n-1\right)S^2}{a\sigma^2}\right]$，其长度为

$$
L=\frac{\left(n-1\right)S^2}{a\sigma^2}-\frac{\left(n-1\right)S^2}{b\sigma^2}=\frac{n-1}{\sigma^2}\left(\frac{1}{a}-\frac{1}{b}\right)S^2.
$$

由**定理**（单个正态总体方差的置信区间）的推导，$\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$. 设 $Y=\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$，则

$$
L=\left(\frac{1}{a}-\frac{1}{b}\right)Y.
$$

由 $\chi^2$ 分布的性质，$E\left(Y\right)=n-1$，$D\left(Y\right)=2\left(n-1\right)$. 因此

$$
E\left(L\right)=\left(\frac{1}{a}-\frac{1}{b}\right)E\left(Y\right)=\left(n-1\right)\left(\frac{1}{a}-\frac{1}{b}\right),
$$

$$
D\left(L\right)=\left(\frac{1}{a}-\frac{1}{b}\right)^2D\left(Y\right)=2\left(n-1\right)\left(\frac{1}{a}-\frac{1}{b}\right)^2.
$$

$\blacksquare$

### 习题五

（习题 4.2-14）随机选取 9 发炮弹，测得炮弹的炮口速度的样本标准差 $s=11\ \text{m/s}$. 若炮弹的炮口速度服从正态分布 $N\left(\mu,\sigma^2\right)$，其中 $\mu,\sigma$ 未知，求标准差 $\sigma$ 的置信水平为 $95\%$ 的单侧置信上限.

### 解答 习题五

由**定理**（单个正态总体方差的置信区间），当 $\mu$ 未知时，$\frac{\left(n-1\right)S^2}{\sigma^2}\sim\chi^2\left(n-1\right)$.

单侧置信上限 $\sigma_U$ 满足 $P\left(\sigma\le\sigma_U\right)=1-\alpha$. 由

$$
P\left(\frac{\left(n-1\right)S^2}{\sigma^2}\ge\chi^2_{1-\alpha}\left(n-1\right)\right)=1-\alpha,
$$

反解 $\sigma$ 得单侧置信上限为

$$
\sigma_U=\sqrt{\frac{\left(n-1\right)S^2}{\chi^2_{1-\alpha}\left(n-1\right)}}.
$$

本题中 $n=9$，$s=11$，$\alpha=0.05$，查 $\chi^2$ 分布表得 $\chi^2_{0.95}\left(8\right)=2.733$（即上 $95\%$ 分位数，亦即下 $5\%$ 分位数）. 代入得

$$
\sigma_U=\sqrt{\frac{8\times11^2}{2.733}}=\sqrt{\frac{968}{2.733}}=\sqrt{354.2}=18.82.
$$

故标准差 $\sigma$ 的置信水平为 $95\%$ 的单侧置信上限为 $18.82\ \text{m/s}$. $\blacksquare$

### 习题六

（习题 4.2-20）两台机床加工同一种零件，分别抽取 6 个和 9 个零件，测量其长度并算得样本方差分别为 $s_1^2=0.245$，$s_2^2=0.357$. 假定两台机床加工零件的长度分别服从正态分布 $N\left(\mu_1,\sigma_1^2\right)$ 和 $N\left(\mu_2,\sigma_2^2\right)$. 求两总体标准差之比 $\frac{\sigma_1}{\sigma_2}$ 的置信水平为 $95\%$ 的置信区间.

### 解答 习题六

由**定理**（两个正态总体方差比的置信区间），$\frac{\sigma_1^2}{\sigma_2^2}$ 的置信水平为 $1-\alpha$ 的置信区间为

$$
\left[\frac{S_1^2/S_2^2}{F_{\alpha/2}\left(m-1,n-1\right)},\ \frac{S_1^2/S_2^2}{F_{1-\alpha/2}\left(m-1,n-1\right)}\right].
$$

本题中 $m=6$，$n=9$，$s_1^2=0.245$，$s_2^2=0.357$，$\alpha=0.05$. 计算得

$$
\frac{s_1^2}{s_2^2}=\frac{0.245}{0.357}=0.686.
$$

查 $F$ 分布表得

$$
F_{0.025}\left(5,8\right)=4.817,\quad F_{0.975}\left(5,8\right)=\frac{1}{F_{0.025}\left(8,5\right)}=0.148.
$$

故 $\frac{\sigma_1^2}{\sigma_2^2}$ 的 $95\%$ 置信区间为

$$
\left[\frac{0.686}{4.817},\ \frac{0.686}{0.148}\right]=\left[0.142,\ 4.637\right].
$$

对上式两端开平方，得 $\frac{\sigma_1}{\sigma_2}$ 的 $95\%$ 置信区间为

$$
\left[\sqrt{0.142},\ \sqrt{4.637}\right]=\left[0.377,\ 2.153\right].
$$

$\blacksquare$

### 习题七

（习题 4.2-21）设从总体 $X\sim N\left(\mu_1,\sigma_1^2\right)$ 和总体 $Y\sim N\left(\mu_2,\sigma_2^2\right)$ 中分别抽取容量为 $m=10$，$n=15$ 的样本，计算得样本均值分别为 $\bar{x}=82$，$\bar{y}=76$，样本方差分别为 $s_x^2=56.5$，$s_y^2=52.4$.

(1) 若已知 $\sigma_1^2=64$，$\sigma_2^2=49$，求 $\mu_1-\mu_2$ 的置信水平为 $95\%$ 的置信区间；

(2) 若 $\sigma_1^2=\sigma_2^2$ 未知，求 $\mu_1-\mu_2$ 的置信水平为 $95\%$ 的置信区间；

(3) 若对 $\sigma_1^2,\sigma_2^2$ 一无所知，求 $\mu_1-\mu_2$ 的置信水平为 $95\%$ 的置信区间；

(4) 求 $\frac{\sigma_1^2}{\sigma_2^2}$ 的置信水平为 $95\%$ 的置信区间.

### 解答 习题七

由**定理**（两个正态总体均值差的置信区间）和**定理**（两个正态总体方差比的置信区间），分四种情况讨论.

(1) $\sigma_1^2=64$，$\sigma_2^2=49$ 均已知. 置信区间为

$$
\left[\bar x-\bar y-u_{0.025}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}},\ \bar x-\bar y+u_{0.025}\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}\right].
$$

其中 $\bar x-\bar y=82-76=6$，$u_{0.025}=1.96$，

$$
\sqrt{\frac{64}{10}+\frac{49}{15}}=\sqrt{6.4+3.267}=\sqrt{9.667}=3.109.
$$

边际误差为 $1.96\times3.109=6.094$. 故置信区间为

$$
\left[6-6.094,\ 6+6.094\right]=\left[-0.094,\ 12.094\right].
$$

(2) $\sigma_1^2=\sigma_2^2=\sigma^2$ 未知. 合并方差为

$$
s_w^2=\frac{\left(m-1\right)s_x^2+\left(n-1\right)s_y^2}{m+n-2}=\frac{9\times56.5+14\times52.4}{23}=\frac{508.5+733.6}{23}=\frac{1242.1}{23}=54.00.
$$

$s_w=\sqrt{54.00}=7.349$. 查 $t$ 分布表得 $t_{0.025}\left(23\right)=2.069$. 边际误差为

$$
s_w t_{0.025}\left(23\right)\sqrt{\frac{1}{m}+\frac{1}{n}}=7.349\times2.069\times\sqrt{\frac{1}{10}+\frac{1}{15}}=7.349\times2.069\times0.408=6.206.
$$

故 $\mu_1-\mu_2$ 的 $95\%$ 置信区间为

$$
\left[6-6.206,\ 6+6.206\right]=\left[-0.206,\ 12.206\right].
$$

(3) $\sigma_1^2,\sigma_2^2$ 均未知且不等. 采用 Welch 近似，自由度为

$$
r=\frac{\left(s_x^2/m+s_y^2/n\right)^2}{\frac{\left(s_x^2/m\right)^2}{m-1}+\frac{\left(s_y^2/n\right)^2}{n-1}}=\frac{\left(5.65+3.493\right)^2}{\frac{5.65^2}{9}+\frac{3.493^2}{14}}=\frac{9.143^2}{3.547+0.872}=\frac{83.59}{4.419}=18.92\approx19.
$$

查 $t$ 分布表得 $t_{0.025}\left(19\right)=2.093$. 边际误差为

$$
t_{0.025}\left(19\right)\sqrt{\frac{s_x^2}{m}+\frac{s_y^2}{n}}=2.093\times\sqrt{9.143}=2.093\times3.024=6.329.
$$

故 $\mu_1-\mu_2$ 的 $95\%$ 置信区间为

$$
\left[6-6.329,\ 6+6.329\right]=\left[-0.329,\ 12.329\right].
$$

(4) 求 $\frac{\sigma_1^2}{\sigma_2^2}$ 的置信区间. 查 $F$ 分布表得

$$
F_{0.025}\left(9,14\right)=3.209,\quad F_{0.975}\left(9,14\right)=\frac{1}{F_{0.025}\left(14,9\right)}=0.263.
$$

$\frac{s_x^2}{s_y^2}=\frac{56.5}{52.4}=1.078$. 故置信区间为

$$
\left[\frac{1.078}{3.209},\ \frac{1.078}{0.263}\right]=\left[0.336,\ 4.100\right].
$$

$\blacksquare$
