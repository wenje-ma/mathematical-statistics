# 作业 18

> **指数分布参数的假设检验**（小样本方法）<br>设总体 $X\sim E\left(\lambda\right)$，其密度函数为 $f\left(x\right)=\lambda e^{-\lambda x}\left(x>0\right)$，其中 $\lambda>0$ 未知，$X_1,X_2,\dots,X_n$ 是来自总体 $X$ 的样本. 由**定理 2.3.8**，有 $2n\lambda\bar X\sim\chi^2\left(2n\right)$. 对检验问题 $H_0:\lambda=\lambda_0,\ H_1:\lambda\ne\lambda_0$，拒绝域为 $$D=\left\{2n\lambda_0\bar X\le\chi^2_{1-\alpha/2}\left(2n\right)\ \text{或}\ 2n\lambda_0\bar X\ge\chi^2_{\alpha/2}\left(2n\right)\right\};$$ 对检验问题 $H_0:\lambda\le\lambda_0,\ H_1:\lambda>\lambda_0$，拒绝域为 $$D=\left\{2n\lambda_0\bar X\le\chi^2_{1-\alpha}\left(2n\right)\right\};$$ 对检验问题 $H_0:\lambda\ge\lambda_0,\ H_1:\lambda<\lambda_0$，拒绝域为 $$D=\left\{2n\lambda_0\bar X\ge\chi^2_\alpha\left(2n\right)\right\}.$$

> **两指数分布参数比的检验**<br>设 $X_1,X_2,\dots,X_m$ 来自 $E\left(\lambda_1\right)$，$Y_1,Y_2,\dots,Y_n$ 来自 $E\left(\lambda_2\right)$，两样本独立. 由 $2m\lambda_1\bar X\sim\chi^2\left(2m\right)$ 与 $2n\lambda_2\bar Y\sim\chi^2\left(2n\right)$ 相互独立，构造 $F$ 统计量. 当 $H_0:\lambda_1=\lambda_2$ 成立时，有 $$\frac{\bar X}{\bar Y}\sim F\left(2m,2n\right).$$ 双边检验 $H_0:\lambda_1=\lambda_2,\ H_1:\lambda_1\ne\lambda_2$ 的拒绝域为 $$D=\left\{\frac{\bar X}{\bar Y}\le F_{1-\alpha/2}\left(2m,2n\right)\ \text{或}\ \frac{\bar X}{\bar Y}\ge F_{\alpha/2}\left(2m,2n\right)\right\}.$$

> **大样本方法**（二项分布参数 $p$ 的检验）<br>设 $X_1,X_2,\dots,X_n$ 来自两点分布总体 $B\left(1,p\right)$，$0<p<1$ 未知. 当 $n$ 充分大（一般要求 $n\ge30$）时，由中心极限定理，在 $H_0:p=p_0$ 成立时，有 $$U=\frac{\bar X-p_0}{\sqrt{\frac{p_0\left(1-p_0\right)}{n}}}\overset{\text{近似}}{\sim}N\left(0,1\right).$$ 双边检验 $H_0:p=p_0,\ H_1:p\ne p_0$ 的拒绝域为 $\left\lvert U\right\rvert\ge u_{\alpha/2}$；右边检验 $H_0:p\le p_0,\ H_1:p>p_0$ 的拒绝域为 $U\ge u_\alpha$；左边检验 $H_0:p\ge p_0,\ H_1:p<p_0$ 的拒绝域为 $U\le-u_\alpha$.

> **大样本方法**（泊松分布参数 $\lambda$ 的检验）<br>设 $X_1,X_2,\dots,X_n$ 来自泊松分布总体 $P\left(\lambda\right)$，$\lambda>0$ 未知. 由 $S=\sum_{i=1}^nX_i\sim P\left(n\lambda\right)$，$E\left(S\right)=n\lambda$，$D\left(S\right)=n\lambda$. 当 $H_0:\lambda=\lambda_0$ 成立时，由中心极限定理，有 $$U=\frac{S-n\lambda_0}{\sqrt{n\lambda_0}}\overset{\text{近似}}{\sim}N\left(0,1\right),$$ 即 $U=\frac{\bar X-\lambda_0}{\sqrt{\lambda_0/n}}\overset{\text{近似}}{\sim}N\left(0,1\right)$. 双边检验 $H_0:\lambda=\lambda_0,\ H_1:\lambda\ne\lambda_0$ 的拒绝域为 $\left\lvert U\right\rvert\ge u_{\alpha/2}$.

### 习题一

（习题 5.3-1）某公司生产一种 $40\mathrm{W}$ 灯泡，并声称灯泡的平均寿命为 $1000\mathrm{h}$. 消费者随机地抽取了 $4$ 个灯泡做试验，得到它们的寿命分别是 $980\mathrm{h}$，$1005\mathrm{h}$，$992\mathrm{h}$，$973\mathrm{h}$，计算得平均寿命为 $987.5\mathrm{h}$. 若假定灯泡的寿命服从指数分布，问在显著性水平 $0.05$ 下，有无充分证据认为平均寿命小于 $1000\mathrm{h}$？

### 解答 习题一

灯泡寿命服从指数分布 $E\left(\lambda\right)$，平均寿命为 $1/\lambda$. 公司声称平均寿命为 $1000\mathrm{h}$，即 $1/\lambda=1000$，亦即 $\lambda=1/1000$. 消费者怀疑平均寿命小于 $1000\mathrm{h}$，即 $1/\lambda<1000$，亦即 $\lambda>1/1000$. 由**指数分布参数的假设检验**（小样本方法），这是右边检验问题，提出假设

$$
H_0:\lambda\le\lambda_0=\frac{1}{1000},\qquad H_1:\lambda>\lambda_0.
$$

由**指数分布参数的假设检验**，检验统计量为 $2n\lambda_0\bar X$，其拒绝域为

$$
D=\left\{2n\lambda_0\bar X\le\chi^2_{1-\alpha}\left(2n\right)\right\}.
$$

代入 $n=4$，$\bar x=987.5$，$\lambda_0=1/1000$，$\alpha=0.05$，得

$$
2n\lambda_0\bar x=2\times4\times\frac{1}{1000}\times987.5=7.9.
$$

查 $\chi^2$ 分布表，$\chi^2_{0.95}\left(8\right)=2.733$（即自由度 $8$、下侧分位数 $0.05$ 对应的上侧分位数 $\chi^2_{1-\alpha}\left(2n\right)=\chi^2_{0.95}\left(8\right)$）. 由于 $7.9>2.733$，样本未落入拒绝域，故在显著性水平 $\alpha=0.05$ 下不拒绝原假设，即没有充分证据认为灯泡的平均寿命小于 $1000\mathrm{h}$. $\blacksquare$

### 习题二

（习题 5.3-3）设 $X_1,X_2,\dots,X_m$ 是来自指数分布总体 $E\left(\lambda_1\right)$ 的样本，其中 $\lambda_1>0$ 为未知参数，$Y_1,Y_2,\dots,Y_n$ 是来自指数分布总体 $E\left(\lambda_2\right)$ 的样本，其中 $\lambda_2>0$ 为未知参数，且两样本相互独立. 在显著性水平 $\alpha$ 下，检验假设 $\lambda_1=\lambda_2$，$\lambda_1\ne\lambda_2$.

### 解答 习题二

由**指数分布参数的假设检验**（小样本方法）中的 $2n\lambda\bar X\sim\chi^2\left(2n\right)$ 结论，有

$$
2m\lambda_1\bar X\sim\chi^2\left(2m\right),\qquad 2n\lambda_2\bar Y\sim\chi^2\left(2n\right),
$$

且由两样本相互独立知上述两个 $\chi^2$ 变量相互独立. 由**两指数分布参数比的检验**，构造 $F$ 统计量

$$
F=\frac{\frac{2m\lambda_1\bar X}{2m}}{\frac{2n\lambda_2\bar Y}{2n}}=\frac{\lambda_1\bar X}{\lambda_2\bar Y}.
$$

当 $H_0:\lambda_1=\lambda_2=\lambda$ 成立时，$\lambda$ 约去，得

$$
F=\frac{\bar X}{\bar Y}\sim F\left(2m,2n\right).
$$

由**两指数分布参数比的检验**，双边检验的拒绝域为

$$
D=\left\{\frac{\bar X}{\bar Y}\le F_{1-\alpha/2}\left(2m,2n\right)\ \text{或}\ \frac{\bar X}{\bar Y}\ge F_{\alpha/2}\left(2m,2n\right)\right\}.
$$

即若样本观测值满足 $\frac{\bar x}{\bar y}\le F_{1-\alpha/2}\left(2m,2n\right)$ 或 $\frac{\bar x}{\bar y}\ge F_{\alpha/2}\left(2m,2n\right)$，则在显著性水平 $\alpha$ 下拒绝原假设 $H_0$，认为 $\lambda_1\ne\lambda_2$；否则不拒绝 $H_0$. $\blacksquare$

### 习题三

（习题 5.3-4）设 $X_1,X_2,\dots,X_n$ 为来自总体 $X$ 的样本，且 $X\sim P\left(\lambda\right)$，其中 $\lambda>0$ 为未知参数. 在显著性水平 $\alpha$ 下，用大样本方法求检验假设 $H_0:\lambda=\lambda_0$；$H_1:\lambda\ne\lambda_0$ 的拒绝域.

### 解答 习题三

由**大样本方法**（泊松分布参数 $\lambda$ 的检验），令 $S=\sum_{i=1}^nX_i$. 由泊松分布的可加性，$S\sim P\left(n\lambda\right)$，故 $E\left(S\right)=n\lambda$，$D\left(S\right)=n\lambda$.

当 $H_0:\lambda=\lambda_0$ 成立时，$S\sim P\left(n\lambda_0\right)$，由中心极限定理，当 $n\to+\infty$ 时，

$$
\frac{S-n\lambda_0}{\sqrt{n\lambda_0}}\overset{\text{近似}}{\sim}N\left(0,1\right).
$$

取检验统计量

$$
U=\frac{S-n\lambda_0}{\sqrt{n\lambda_0}}=\frac{\bar X-\lambda_0}{\sqrt{\lambda_0/n}}.
$$

对给定显著性水平 $\alpha$，由**大样本方法**（泊松分布参数 $\lambda$ 的检验）中双边检验的拒绝域形式，得

$$
\alpha=P\left(\left\lvert U\right\rvert\ge u_{\alpha/2}\,\middle|\,H_0\right),
$$

故检验问题 $H_0:\lambda=\lambda_0,\ H_1:\lambda\ne\lambda_0$ 的拒绝域为

$$
D=\left\{\left(x_1,x_2,\dots,x_n\right):\left\lvert\frac{\sum_{i=1}^nx_i-n\lambda_0}{\sqrt{n\lambda_0}}\right\rvert\ge u_{\alpha/2}\right\}.
$$

即若样本观测值满足 $\left\lvert\frac{\bar x-\lambda_0}{\sqrt{\lambda_0/n}}\right\rvert\ge u_{\alpha/2}$，则在显著性水平 $\alpha$ 下拒绝 $H_0$；否则不拒绝 $H_0$. $\blacksquare$

### 习题四

（习题 5.3-6）某市随机抽取 $1000$ 个家庭，调查其中有 $450$ 家拥有电脑，$p$ 表示该市拥有电脑家庭的比例. 在显著性水平 $\alpha=0.05$ 下，检验假设 $H_0:p=0.5$；$H_1:p\ne0.5$.

### 解答 习题四

样本容量 $n=1000$，属于大样本情形，由**大样本方法**（二项分布参数 $p$ 的检验），取检验统计量

$$
U=\frac{\bar X-p_0}{\sqrt{\frac{p_0\left(1-p_0\right)}{n}}}.
$$

由题意，$\bar x=\frac{450}{1000}=0.45$，$p_0=0.5$，代入得

$$
u=\frac{0.45-0.5}{\sqrt{\frac{0.5\times0.5}{1000}}}=\frac{-0.05}{\sqrt{0.00025}}=\frac{-0.05}{0.01581}=-3.162.
$$

双边检验在 $\alpha=0.05$ 下的拒绝域为 $\left\lvert U\right\rvert\ge u_{0.025}=1.96$. 由于 $\left\lvert u\right\rvert=3.162>1.96$，样本落入拒绝域，故在显著性水平 $\alpha=0.05$ 下拒绝原假设 $H_0$，即认为该市拥有电脑家庭的比例 $p$ 不等于 $0.5$. $\blacksquare$
