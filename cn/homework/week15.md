# 作业 15

> **枢轴量法**（置信区间的构造）<br>设 $X_1,X_2,\dots,X_n$ 是来自总体的样本，未知参数为 $\theta$. 若能构造出一个样本与 $\theta$ 的函数 $G\left(X_1,X_2,\dots,X_n,\theta\right)$，其分布完全已知且与 $\theta$ 无关，则称 $G$ 为枢轴量. 对给定置信水平 $1-\alpha$，选取 $c_1,c_2$ 使 $P\left\{c_1\le G\le c_2\right\}=1-\alpha$，再将不等式 $c_1\le G\le c_2$ 等价变形为 $\hat\theta_1\le\theta\le\hat\theta_2$，即得 $\theta$ 的置信水平为 $1-\alpha$ 的置信区间 $\left[\hat\theta_1,\hat\theta_2\right]$.

> **指数分布参数的置信区间**<br>设 $X_1,X_2,\dots,X_n$ 是来自指数分布总体 $E\left(\lambda\right)$ 的样本，其密度函数为 $f\left(x\right)=\lambda e^{-\lambda x},\ x> 0$. 由 $\chi^2$ 分布的可加性，枢轴量为 $$T=2\lambda\sum_{i=1}^n X_i=2n\lambda\bar X\sim\chi^2\left(2n\right).$$ 由此均值 $\theta=\frac{1}{\lambda}$ 的置信水平为 $1-\alpha$ 的置信区间为 $$\left[\frac{2n\bar X}{\chi^2_{\alpha/2}\left(2n\right)},\ \frac{2n\bar X}{\chi^2_{1-\alpha/2}\left(2n\right)}\right],$$ 其中 $\chi^2_{\alpha/2}\left(2n\right)$ 与 $\chi^2_{1-\alpha/2}\left(2n\right)$ 分别为自由度 $2n$ 的 $\chi^2$ 分布的上 $\alpha/2$ 与上 $1-\alpha/2$ 分位数.

> **大样本方法**（两点分布参数的近似置信区间）<br>设 $X_1,X_2,\dots,X_n$ 是来自两点分布 $B\left(1,p\right)$ 的样本，$\bar X$ 为样本均值. 由中心极限定理，当 $n$ 充分大时 $\frac{\bar X-p}{\sqrt{p\left(1-p\right)/n}}\overset{\mathrm{d}}{\to}N\left(0,1\right)$. 用 $\bar X$ 估计 $p$，得参数 $p$ 的置信水平近似为 $1-\alpha$ 的置信区间 $$\left[\bar X-u_{\alpha/2}\sqrt{\frac{\bar X\left(1-\bar X\right)}{n}},\ \bar X+u_{\alpha/2}\sqrt{\frac{\bar X\left(1-\bar X\right)}{n}}\right],$$ 其中 $u_{\alpha/2}$ 为标准正态分布的上 $\alpha/2$ 分位数.

### 习题一

（习题 4.3-1）设某电子产品的寿命服从指数分布 $E\left(\lambda\right)$，其密度函数为 $f\left(x\right)=\lambda e^{-\lambda x},\ x> 0$，其中 $\lambda> 0$. 现从该分布的一批产品中抽取容量为 $9$ 的样本，测得寿命为（单位：kh）$15,45,50,53,60,65,70,83,90$. 求平均寿命 $\frac{1}{\lambda}$ 的置信水平为 $90\%$ 的置信区间和置信上、下限.

### 解答 习题一

由**指数分布参数的置信区间**，枢轴量 $T=2n\lambda\bar X\sim\chi^2\left(2n\right)$. 样本均值为

$$
\bar X=\frac{15+45+50+53+60+65+70+83+90}{9}=\frac{531}{9}=59,
$$

故 $2n\bar X=18\times59=1062$，自由度为 $2n=18$.

由**枢轴量法**（置信区间的构造），对置信水平 $1-\alpha=0.90$，即 $\alpha=0.10$，有

$$
P\left\{\chi^2_{0.05}\left(18\right)\le 2n\lambda\bar X\le\chi^2_{0.95}\left(18\right)\right\}=0.90.
$$

查表得 $\chi^2_{0.05}\left(18\right)=9.390$，$\chi^2_{0.95}\left(18\right)=28.869$. 解不等式即得平均寿命 $\theta=\frac{1}{\lambda}$ 的置信水平为 $90\%$ 的置信区间为

$$
\left[\frac{1062}{28.869},\ \frac{1062}{9.390}\right]=\left[36.79,\ 113.09\right]\ \text{kh}.
$$

单侧置信上限 $\theta_U$ 满足 $P\left\{\theta\le\theta_U\right\}=0.90$，即 $P\left\{2n\lambda\bar X\ge\chi^2_{0.10}\left(18\right)\right\}=0.90$，故

$$
\theta_U=\frac{2n\bar X}{\chi^2_{0.10}\left(18\right)}=\frac{1062}{10.865}=97.75.
$$

单侧置信下限 $\theta_L$ 满足 $P\left\{\theta\ge\theta_L\right\}=0.90$，即 $P\left\{2n\lambda\bar X\le\chi^2_{0.90}\left(18\right)\right\}=0.90$，故

$$
\theta_L=\frac{2n\bar X}{\chi^2_{0.90}\left(18\right)}=\frac{1062}{25.989}=40.86.
$$

$\blacksquare$

### 习题二

（习题 4.3-3）设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，且 $X$ 的密度函数为 $f\left(x,\theta\right)=\begin{cases}\frac{\theta}{x^2},&x> \theta,\\0,&\text{其他},\end{cases}$ 其中 $\theta> 0$. 求参数 $\theta$ 的置信水平为 $1-\alpha$ 的置信区间.

### 解答 习题二

先求总体分布函数. 对 $x> \theta$，

$$
F\left(x,\theta\right)=\int_\theta^x\frac{\theta}{t^2}\,\mathrm dt=\theta\left[-\frac{1}{t}\right]_\theta^x=1-\frac{\theta}{x}.
$$

由**定义 1.3.2**（简单随机样本），$X_1,X_2,\dots,X_n$ 相互独立且与总体同分布. 考虑最小顺序统计量 $X_{\left(1\right)}=\min\left\{X_1,\dots,X_n\right\}$，对 $t> \theta$，

$$
P\left\{X_{\left(1\right)}\ge t\right\}=\prod_{i=1}^n P\left\{X_i\ge t\right\}=\left[1-F\left(t,\theta\right)\right]^n=\left(\frac{\theta}{t}\right)^n.
$$

构造枢轴量 $G=\frac{X_{\left(1\right)}}{\theta}$. 由于 $X_i> \theta$ 恒成立，故 $G\ge1$. 对 $t\ge1$，

$$
P\left\{G\ge t\right\}=P\left\{X_{\left(1\right)}\ge\theta t\right\}=\left(\frac{\theta}{\theta t}\right)^n=t^{-n},
$$

其分布与 $\theta$ 无关，故 $G$ 为枢轴量.

由**枢轴量法**（置信区间的构造），注意到 $G\ge1$，取

$$
P\left\{1\le G\le\alpha^{-1/n}\right\}=P\left\{G\le\alpha^{-1/n}\right\}=1-\left(\alpha^{-1/n}\right)^{-n}=1-\alpha.
$$

即

$$
P\left\{1\le\frac{X_{\left(1\right)}}{\theta}\le\alpha^{-1/n}\right\}=1-\alpha.
$$

等价变形为

$$
P\left\{\alpha^{1/n}X_{\left(1\right)}\le\theta\le X_{\left(1\right)}\right\}=1-\alpha.
$$

故参数 $\theta$ 的置信水平为 $1-\alpha$ 的置信区间为

$$
\left[\alpha^{1/n}X_{\left(1\right)},\ X_{\left(1\right)}\right].
$$

$\blacksquare$

### 习题三

（习题 4.3-4）设 $X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本，且 $X$ 的密度函数为 $f\left(x\right)=\begin{cases}2\lambda x e^{-\lambda x^2},&x> 0,\\0,&\text{其他},\end{cases}$ 其中 $\lambda> 0$. 求参数 $\lambda$ 的置信水平为 $1-\alpha$ 的置信区间.

### 解答 习题三

令 $Y=X^2$. 当 $y> 0$ 时，由随机变量函数的密度变换公式，

$$
f_Y\left(y\right)=f\left(\sqrt y\right)\left|\frac{\mathrm d\sqrt y}{\mathrm dy}\right|=2\lambda\sqrt y\,e^{-\lambda y}\cdot\frac{1}{2\sqrt y}=\lambda e^{-\lambda y},
$$

即 $Y\sim E\left(\lambda\right)$. 由**定义 1.3.2**（简单随机样本），$Y_i=X_i^2$ 相互独立且均服从 $E\left(\lambda\right)$.

由**指数分布参数的置信区间**，枢轴量为

$$
2\lambda\sum_{i=1}^n Y_i=2\lambda\sum_{i=1}^n X_i^2\sim\chi^2\left(2n\right).
$$

由**枢轴量法**（置信区间的构造），

$$
P\left\{\chi^2_{1-\alpha/2}\left(2n\right)\le 2\lambda\sum_{i=1}^n X_i^2\le\chi^2_{\alpha/2}\left(2n\right)\right\}=1-\alpha.
$$

解不等式即得参数 $\lambda$ 的置信水平为 $1-\alpha$ 的置信区间为

$$
\left[\frac{\chi^2_{1-\alpha/2}\left(2n\right)}{2\sum_{i=1}^n X_i^2},\ \frac{\chi^2_{\alpha/2}\left(2n\right)}{2\sum_{i=1}^n X_i^2}\right].
$$

$\blacksquare$

### 习题四

（习题 4.3-10）在一批货物中随机抽取 $100$ 件，发现有 $16$ 件不合格品，求这批货物的不合格品率的置信水平近似为 $95\%$ 的置信区间.

### 解答 习题四

设不合格品率为 $p$，则样本均值即频率 $\bar X=\frac{16}{100}=0.16$，样本容量 $n=100$.

由**大样本方法**（两点分布参数的近似置信区间），$p$ 的置信水平近似为 $1-\alpha$ 的置信区间为

$$
\left[\bar X-u_{\alpha/2}\sqrt{\frac{\bar X\left(1-\bar X\right)}{n}},\ \bar X+u_{\alpha/2}\sqrt{\frac{\bar X\left(1-\bar X\right)}{n}}\right].
$$

取 $1-\alpha=0.95$，则 $\alpha=0.05$，$u_{0.025}=1.96$，且

$$
\sqrt{\frac{\bar X\left(1-\bar X\right)}{n}}=\sqrt{\frac{0.16\times0.84}{100}}=\sqrt{0.001344}=0.0367.
$$

故不合格品率 $p$ 的置信水平近似为 $95\%$ 的置信区间为

$$
\left[0.16-1.96\times0.0367,\ 0.16+1.96\times0.0367\right]=\left[0.088,\ 0.232\right].
$$

$\blacksquare$
