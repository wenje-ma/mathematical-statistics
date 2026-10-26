# 作业 17

> **U检验法**（方差已知时单个正态总体均值的检验）<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，其中 $\sigma^2=\sigma_0^2$ 已知，$\mu$ 未知. 对给定显著性水平 $\alpha$，取检验统计量 $$U=\frac{\overline X-\mu_0}{\sigma_0/\sqrt n},$$ 当 $H_0:\mu=\mu_0$ 成立时 $U\sim N\left(0,1\right)$. 三种检验问题的拒绝域分别为：双边检验 $H_0:\mu=\mu_0,\ H_1:\mu\ne\mu_0$ 的拒绝域为 $\left\lvert U\right\rvert\ge u_{\alpha/2}$；右边检验 $H_0:\mu\le\mu_0,\ H_1:\mu> \mu_0$ 的拒绝域为 $U\ge u_\alpha$；左边检验 $H_0:\mu\ge\mu_0,\ H_1:\mu< \mu_0$ 的拒绝域为 $U\le-u_\alpha$.

> **t检验法**（方差未知时单个正态总体均值的检验）<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，其中 $\sigma^2$ 未知. 对给定显著性水平 $\alpha$，取检验统计量 $$T=\frac{\overline X-\mu_0}{S/\sqrt n},$$ 当 $H_0:\mu=\mu_0$ 成立时 $T\sim t\left(n-1\right)$. 双边检验的拒绝域为 $\left\lvert T\right\rvert\ge t_{\alpha/2}\left(n-1\right)$；右边检验的拒绝域为 $T\ge t_\alpha\left(n-1\right)$；左边检验的拒绝域为 $T\le-t_\alpha\left(n-1\right)$.

> **$\chi^2$检验法**（单个正态总体方差的检验）<br>设 $X_1,X_2,\dots,X_n$ 是来自正态总体 $N\left(\mu,\sigma^2\right)$ 的样本，其中 $\mu$ 未知. 对给定显著性水平 $\alpha$，取检验统计量 $$\chi^2=\frac{\left(n-1\right)S^2}{\sigma_0^2},$$ 当 $H_0:\sigma^2=\sigma_0^2$ 成立时 $\chi^2\sim\chi^2\left(n-1\right)$. 双边检验 $H_0:\sigma^2=\sigma_0^2,\ H_1:\sigma^2\ne\sigma_0^2$ 的拒绝域为 $\chi^2\le\chi^2_{1-\alpha/2}\left(n-1\right)$ 或 $\chi^2\ge\chi^2_{\alpha/2}\left(n-1\right)$；右边检验 $H_0:\sigma^2\le\sigma_0^2,\ H_1:\sigma^2> \sigma_0^2$ 的拒绝域为 $\chi^2\ge\chi^2_\alpha\left(n-1\right)$；左边检验 $H_0:\sigma^2\ge\sigma_0^2,\ H_1:\sigma^2< \sigma_0^2$ 的拒绝域为 $\chi^2\le\chi^2_{1-\alpha}\left(n-1\right)$.

> **两正态总体均值差的U检验**（方差均已知）<br>设 $X_1,X_2,\dots,X_m$ 来自 $N\left(\mu_1,\sigma_1^2\right)$，$Y_1,Y_2,\dots,Y_n$ 来自 $N\left(\mu_2,\sigma_2^2\right)$，两样本独立，其中 $\sigma_1^2,\sigma_2^2$ 均已知. 取检验统计量 $$U=\frac{\overline X-\overline Y}{\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}},$$ 当 $H_0:\mu_1=\mu_2$ 成立时 $U\sim N\left(0,1\right)$. 双边检验拒绝域为 $\left\lvert U\right\rvert\ge u_{\alpha/2}$；右边检验 $H_0:\mu_1\le\mu_2,\ H_1:\mu_1> \mu_2$ 的拒绝域为 $U\ge u_\alpha$.

> **两正态总体均值差的合并t检验**（方差未知但相等）<br>设 $X_1,X_2,\dots,X_m$ 来自 $N\left(\mu_1,\sigma^2\right)$，$Y_1,Y_2,\dots,Y_n$ 来自 $N\left(\mu_2,\sigma^2\right)$，两样本独立，其中 $\sigma^2$ 未知. 取合并样本方差 $$S_w^2=\frac{\left(m-1\right)S_1^2+\left(n-1\right)S_2^2}{m+n-2},$$ 检验统计量为 $$T=\frac{\overline X-\overline Y}{S_w\sqrt{\frac1m+\frac1n}},$$ 当 $H_0:\mu_1=\mu_2$ 成立时 $T\sim t\left(m+n-2\right)$. 双边检验拒绝域为 $\left\lvert T\right\rvert\ge t_{\alpha/2}\left(m+n-2\right)$；右边检验拒绝域为 $T\ge t_\alpha\left(m+n-2\right)$.

> **F检验法**（两正态总体方差比的检验）<br>设 $X_1,X_2,\dots,X_m$ 来自 $N\left(\mu_1,\sigma_1^2\right)$，$Y_1,Y_2,\dots,Y_n$ 来自 $N\left(\mu_2,\sigma_2^2\right)$，两样本独立，其中 $\mu_1,\mu_2$ 未知. 取检验统计量 $$F=\frac{S_1^2}{S_2^2},$$ 当 $H_0:\sigma_1^2=\sigma_2^2$ 成立时 $F\sim F\left(m-1,n-1\right)$. 双边检验 $H_0:\sigma_1^2=\sigma_2^2,\ H_1:\sigma_1^2\ne\sigma_2^2$ 的拒绝域为 $F\le F_{1-\alpha/2}\left(m-1,n-1\right)$ 或 $F\ge F_{\alpha/2}\left(m-1,n-1\right)$.

### 习题一

（习题 5.2-5）从标准差为 $\sigma=5.2$ 的正态总体 $N\left(\mu,\sigma^2\right)$ 中随机抽取容量为 $16$ 的样本，计算得样本均值为 $\overline x=27.56$，在显著性水平 $\alpha=0.05$ 下，能否认为总体均值 $\mu=26$？

### 解答 习题一

本题中总体方差 $\sigma^2=5.2^2$ 已知，由**U检验法**（方差已知时单个正态总体均值的检验），提出假设

$$
H_0:\mu=26,\quad H_1:\mu\ne26.
$$

检验统计量为 $U=\frac{\overline X-\mu_0}{\sigma_0/\sqrt n}$，代入数据 $\overline x=27.56$，$\mu_0=26$，$\sigma_0=5.2$，$n=16$，得

$$
u=\frac{27.56-26}{5.2/\sqrt{16}}=\frac{1.56}{1.3}=1.2.
$$

显著性水平 $\alpha=0.05$，双边检验拒绝域为 $\left\lvert U\right\rvert\ge u_{0.025}=1.96$. 由于 $\left\lvert u\right\rvert=1.2< 1.96$，样本未落入拒绝域，故在显著性水平 $\alpha=0.05$ 下不拒绝原假设，即可以认为总体均值 $\mu=26$. $\blacksquare$

### 习题二

（习题 5.2-7）要求一种元件的平均使用寿命不得低于 $1000\mathrm{h}$，生产者从这种元件中随机抽取 $25$ 件，测得其寿命的平均值为 $950\mathrm{h}$. 已知该种元件寿命服从标准差为 $\sigma=100\mathrm{h}$ 的正态分布，在显著性水平 $\alpha=0.05$ 下，判断这批元件是否合格？

### 解答 习题二

题目要求平均寿命不得低于 $1000\mathrm{h}$，生产者希望通过样本数据检验产品是否合格. 由**U检验法**（方差已知时单个正态总体均值的检验），这是左边检验问题，提出假设

$$
H_0:\mu\ge1000,\quad H_1:\mu< 1000.
$$

检验统计量为 $U=\frac{\overline X-\mu_0}{\sigma_0/\sqrt n}$，代入数据 $\overline x=950$，$\mu_0=1000$，$\sigma_0=100$，$n=25$，得

$$
u=\frac{950-1000}{100/\sqrt{25}}=\frac{-50}{20}=-2.5.
$$

左边检验在显著性水平 $\alpha=0.05$ 下的拒绝域为 $U\le-u_{0.05}=-1.645$. 由于 $u=-2.5< -1.645$，样本落入拒绝域，故在显著性水平 $\alpha=0.05$ 下拒绝原假设，即认为这批元件的平均寿命低于 $1000\mathrm{h}$，这批元件不合格. $\blacksquare$

### 习题三

（习题 5.2-9）设 $X_1,X_2,\dots,X_{25}$ 是来自正态总体 $N\left(\mu,3^2\right)$ 的一个样本，其中 $\mu\in\mathbb R$ 为未知参数. 设检验问题 $H_0:\mu=\mu_0$；$H_1:\mu\ne\mu_0$（$\mu_0$ 已知）的拒绝域为 $D=\left\{\left\lvert\overline X-\mu_0\right\rvert\ge c\right\}$.

(1) 在显著性水平 $\alpha=0.05$ 下，求常数 $c$；

(2) 求 $\mu=\mu_1$（$\ne\mu_0$）时犯第二类错误的概率（用标准正态分布函数 $\Phi\left(\cdot\right)$ 表示）.

### 解答 习题三

由**U检验法**（方差已知时单个正态总体均值的检验），当 $H_0:\mu=\mu_0$ 成立时，$\overline X\sim N\left(\mu_0,\frac{3^2}{25}\right)$，故

$$
\frac{\overline X-\mu_0}{3/5}\sim N\left(0,1\right).
$$

(1) 由显著性水平 $\alpha=0.05$，有

$$
\alpha=P\left(\left\lvert\overline X-\mu_0\right\rvert\ge c\,\middle|\,H_0\right)=P\left(\left\lvert\frac{\overline X-\mu_0}{3/5}\right\rvert\ge\frac{5c}{3}\right)=2\left[1-\Phi\left(\frac{5c}{3}\right)\right].
$$

于是 $\Phi\left(\frac{5c}{3}\right)=1-\frac{\alpha}{2}=0.975$，查表得 $\frac{5c}{3}=u_{0.025}=1.96$，故

$$
c=\frac{3}{5}\times1.96=1.176.
$$

(2) 当 $\mu=\mu_1$（$\mu_1\ne\mu_0$）时，$\overline X\sim N\left(\mu_1,\frac{3^2}{25}\right)$，犯第二类错误即取伪概率为

$$
\beta\left(\mu_1\right)=P\left(\left\lvert\overline X-\mu_0\right\rvert< c\,\middle|\,\mu=\mu_1\right)=P\left(-c< \overline X-\mu_0< c\right).
$$

令 $\delta=\mu_1-\mu_0$，则 $\overline X-\mu_1\sim N\left(0,\frac{3^2}{25}\right)$，即 $\frac{\overline X-\mu_1}{3/5}\sim N\left(0,1\right)$，于是

$$
\beta\left(\mu_1\right)=P\left(-c-\delta< \overline X-\mu_1< c-\delta\right)=\Phi\left(\frac{c-\delta}{3/5}\right)-\Phi\left(\frac{-c-\delta}{3/5}\right).
$$

代入 $c=1.176$，化简得

$$
\beta\left(\mu_1\right)=\Phi\left(\frac{5\left(c-\mu_1+\mu_0\right)}{3}\right)+\Phi\left(\frac{5\left(c+\mu_1-\mu_0\right)}{3}\right)-1.
$$

特别地，当 $\delta=\mu_1-\mu_0$ 分别取 $0.5,1.0,1.5$ 时，$\beta$ 约为 $0.867,0.615,0.295$，可见 $\left\lvert\mu_1-\mu_0\right\rvert$ 越大，犯第二类错误的概率越小. $\blacksquare$

### 习题四

（习题 5.2-12）已知维尼纶纤度在正常情况下服从正态分布 $N\left(\mu,\sigma^2\right)$，且 $\sigma=0.048$. 从某天的产品中任取 $5$ 根纤维，测得其纤度为 $1.32,1.55,1.36,1.40,1.44$，在显著性水平 $\alpha=0.05$ 下，问这天的标准差是否正常？

### 解答 习题四

本题中方差 $\sigma^2$ 未知，需检验标准差是否仍为 $0.048$，即检验方差是否等于 $0.048^2$. 由**$\chi^2$检验法**（单个正态总体方差的检验），提出假设

$$
H_0:\sigma^2=0.048^2,\quad H_1:\sigma^2\ne0.048^2.
$$

由样本数据计算样本均值与样本方差：

$$
\overline x=\frac{1.32+1.55+1.36+1.40+1.44}{5}=1.414,
$$
$$
s^2=\frac{1}{5-1}\sum_{i=1}^5\left(x_i-\overline x\right)^2=0.00778.
$$

检验统计量为 $\chi^2=\frac{\left(n-1\right)S^2}{\sigma_0^2}$，代入 $n=5$，$\sigma_0=0.048$，得

$$
\chi^2=\frac{4\times0.00778}{0.048^2}=13.507.
$$

双边检验在显著性水平 $\alpha=0.05$ 下的拒绝域为 $\chi^2\le\chi^2_{0.975}\left(4\right)=0.484$ 或 $\chi^2\ge\chi^2_{0.025}\left(4\right)=11.143$. 由于 $\chi^2=13.507> 11.143$，样本落入拒绝域，故在显著性水平 $\alpha=0.05$ 下拒绝原假设，即认为这天的标准差不正常. $\blacksquare$

### 习题五

（习题 5.2-15）测量某物体的重量 $10$ 次，得样本均值为 $\overline x=10.05$，样本方差为 $s^2=0.0576$. 假定该物体的重量服从正态分布 $N\left(\mu,\sigma^2\right)$.

(1) 若 $\sigma^2=0.2^2$，在显著性水平 $\alpha=0.05$ 下，检验 $H_0:\mu=10$；$H_1:\mu> 10$；

(2) 若 $\sigma^2$ 未知，在显著性水平 $\alpha=0.05$ 下，检验 $H_0:\mu=10$；$H_1:\mu> 10$；

(3) 在显著性水平 $\alpha=0.05$ 下，检验 $H_0:\sigma^2\ge0.25^2$；$H_1:\sigma^2< 0.25^2$.

### 解答 习题五

(1) 已知 $\sigma^2=0.2^2$，由**U检验法**（方差已知时单个正态总体均值的检验），这是右边检验. 检验统计量为

$$
U=\frac{\overline X-\mu_0}{\sigma_0/\sqrt n},
$$

代入 $\overline x=10.05$，$\mu_0=10$，$\sigma_0=0.2$，$n=10$，得

$$
u=\frac{10.05-10}{0.2/\sqrt{10}}=0.791.
$$

右边检验在 $\alpha=0.05$ 下的拒绝域为 $U\ge u_{0.05}=1.645$. 由于 $u=0.791< 1.645$，不拒绝原假设.

(2) $\sigma^2$ 未知，由**t检验法**（方差未知时单个正态总体均值的检验），仍为右边检验. 检验统计量为

$$
T=\frac{\overline X-\mu_0}{S/\sqrt n},
$$

代入 $s=\sqrt{0.0576}=0.24$，得

$$
t=\frac{10.05-10}{0.24/\sqrt{10}}=0.659.
$$

右边检验在 $\alpha=0.05$ 下的拒绝域为 $T\ge t_{0.05}\left(9\right)=1.833$. 由于 $t=0.659< 1.833$，不拒绝原假设.

(3) 由**$\chi^2$检验法**（单个正态总体方差的检验），这是左边检验. 检验统计量为

$$
\chi^2=\frac{\left(n-1\right)S^2}{\sigma_0^2},
$$

其中 $\sigma_0^2=0.25^2=0.0625$，代入 $n=10$，$s^2=0.0576$，得

$$
\chi^2=\frac{9\times0.0576}{0.25^2}=8.294.
$$

左边检验在 $\alpha=0.05$ 下的拒绝域为 $\chi^2\le\chi^2_{0.95}\left(9\right)=3.325$. 由于 $\chi^2=8.294> 3.325$，不拒绝原假设，即不能否定方差不小于 $0.25^2$ 的断言. $\blacksquare$

### 习题六

（习题 5.2-17）比较甲、乙两种棉花品种的优劣，假设用它们纺出的棉纱强度分别服从正态分布 $N\left(\mu_1,\sigma_1^2\right)$，$N\left(\mu_2,\sigma_2^2\right)$，试验者分别从这两种棉纱中抽取样本 $X_1,X_2,\dots,X_{100}$，$Y_1,Y_2,\dots,Y_{50}$，得样本均值和样本方差分别为 $\overline x=5.6$，$\overline y=5.2$，$s_1^2=4$，$s_2^2=2.56$.

(1) 若 $\sigma_1^2=2.2^2$，$\sigma_2^2=1.8^2$，在显著性水平 $\alpha=0.05$ 下，检验 $H_0:\mu_1\le\mu_2$；$H_1:\mu_1> \mu_2$；

(2) 若 $\sigma_1^2=\sigma_2^2$ 未知，在显著性水平 $\alpha=0.05$ 下，检验 $H_0:\mu_1\le\mu_2$；$H_1:\mu_1> \mu_2$.

### 解答 习题六

(1) 已知 $\sigma_1^2=2.2^2=4.84$，$\sigma_2^2=1.8^2=3.24$，由**两正态总体均值差的U检验**（方差均已知），检验统计量为

$$
U=\frac{\overline X-\overline Y}{\sqrt{\frac{\sigma_1^2}{m}+\frac{\sigma_2^2}{n}}},
$$

代入 $\overline x=5.6$，$\overline y=5.2$，$m=100$，$n=50$，得

$$
u=\frac{5.6-5.2}{\sqrt{\frac{4.84}{100}+\frac{3.24}{50}}}=\frac{0.4}{\sqrt{0.1132}}=1.189.
$$

右边检验在 $\alpha=0.05$ 下的拒绝域为 $U\ge u_{0.05}=1.645$. 由于 $u=1.189< 1.645$，不拒绝原假设，即不能认为甲品种棉纱强度显著高于乙品种.

(2) $\sigma_1^2=\sigma_2^2$ 未知但相等，由**两正态总体均值差的合并t检验**（方差未知但相等），先计算合并样本方差

$$
s_w^2=\frac{\left(m-1\right)s_1^2+\left(n-1\right)s_2^2}{m+n-2}=\frac{99\times4+49\times2.56}{148}=3.523,
$$

$s_w=\sqrt{3.523}=1.877$. 检验统计量为

$$
T=\frac{\overline X-\overline Y}{S_w\sqrt{\frac1m+\frac1n}},
$$

代入数据得

$$
t=\frac{5.6-5.2}{1.877\times\sqrt{\frac1{100}+\frac1{50}}}=\frac{0.4}{1.877\times0.1732}=1.230.
$$

右边检验在 $\alpha=0.05$ 下的拒绝域为 $T\ge t_{0.05}\left(148\right)\approx1.655$. 由于 $t=1.230< 1.655$，不拒绝原假设，即不能认为甲品种棉纱强度显著高于乙品种. $\blacksquare$

### 习题七

（习题 5.2-21）对两批同类电子元件的电阻（单位：$\Omega$）进行测试，各抽取 $6$ 件测得结果如下：

第一批：$0.140,0.138,0.143,0.142,0.144,0.137$；

第二批：$0.135,0.140,0.142,0.136,0.138,0.140$.

已知两批元件的电阻分别服从正态分布 $N\left(\mu_1,\sigma_1^2\right)$ 和 $N\left(\mu_2,\sigma_2^2\right)$，在显著性水平 $\alpha=0.05$ 下，分别检验：

(1) 两批元件电阻的方差是否相等；

(2) 两批元件的平均电阻有无显著差异.

### 解答 习题七

(1) 先由**F检验法**（两正态总体方差比的检验）检验方差是否相等. 提出假设

$$
H_0:\sigma_1^2=\sigma_2^2,\quad H_1:\sigma_1^2\ne\sigma_2^2.
$$

由样本数据计算两批的样本均值与样本方差：

$$
\overline x_1=\frac{1}{6}\sum_{i=1}^6x_{1i}=0.14067,\quad s_1^2=7.867\times10^{-6},
$$
$$
\overline x_2=\frac{1}{6}\sum_{i=1}^6x_{2i}=0.13850,\quad s_2^2=7.100\times10^{-6}.
$$

检验统计量为 $F=\frac{S_1^2}{S_2^2}$，代入得

$$
f=\frac{7.867\times10^{-6}}{7.100\times10^{-6}}=1.108.
$$

双边检验在 $\alpha=0.05$ 下的拒绝域为 $F\le F_{0.975}\left(5,5\right)=0.140$ 或 $F\ge F_{0.025}\left(5,5\right)=7.146$. 由于 $0.140< f=1.108< 7.146$，样本未落入拒绝域，故不拒绝原假设，即可以认为两批元件电阻的方差相等.

(2) 由 (1) 的结论，两总体方差相等但未知，由**两正态总体均值差的合并t检验**（方差未知但相等），提出假设

$$
H_0:\mu_1=\mu_2,\quad H_1:\mu_1\ne\mu_2.
$$

合并样本方差为

$$
s_w^2=\frac{\left(6-1\right)s_1^2+\left(6-1\right)s_2^2}{6+6-2}=\frac{5\times7.867\times10^{-6}+5\times7.100\times10^{-6}}{10}=7.483\times10^{-6},
$$

$s_w=\sqrt{7.483\times10^{-6}}=0.002736$. 检验统计量为

$$
T=\frac{\overline X_1-\overline X_2}{S_w\sqrt{\frac1m+\frac1n}},
$$

代入 $m=n=6$，得

$$
t=\frac{0.14067-0.13850}{0.002736\times\sqrt{\frac16+\frac16}}=\frac{0.00217}{0.00158}=1.372.
$$

双边检验在 $\alpha=0.05$ 下的拒绝域为 $\left\lvert T\right\rvert\ge t_{0.025}\left(10\right)=2.228$. 由于 $\left\lvert t\right\rvert=1.372< 2.228$，不拒绝原假设，即认为两批元件的平均电阻无显著差异. $\blacksquare$
