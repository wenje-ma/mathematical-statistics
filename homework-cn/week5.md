# week5

> **引理 2.3.1 (样本均值与样本方差的期望)**
> 
> $E\left(\overline X\right)=\mu$, $D\left(\overline X\right)=\sigma^2/n$, $E\left(S^2\right)=\sigma^2$.

> **定理 2.3.3 (正态总体样本均值与样本方差的分布)**
> 
> $\overline X\sim N\left(\mu,\sigma^2/n\right)$, $\left(n-1\right)S^2/\sigma^2\sim\chi^2\left(n-1\right)$, 二者独立.

> **定义 2.4.1 (指数族)**
> 
> $f=C\left(\theta\right)\exp\left\{\sum Q_i\left(\theta\right)T_i\left(x\right)\right\}h\left(x\right)$.

> **定义 2.4.2 (指数族的自然形式)**
> 
> $f=C\left(\varphi\right)\exp\left\{\sum\varphi_i T_i\left(x\right)\right\}h\left(x\right)$.

## 习题 2.3-21

均匀样本顺序统计量.

### 解答 习题 2.3-21

$n=299$, $f_{R_n}=n\left(n-1\right)r^{n-2}\left(1-r\right)$, $\chi^2\left(4\right)$. $\blacksquare$

## 习题 2.4-3

证明幂分布族是指数族.

### 解答 习题 2.4-3

$f=\theta^n\exp\left\{\theta\sum\ln x_i\right\}/\prod x_i$. 自然参数空间 $\left(0,\infty\right)$. $\blacksquare$

## 习题 2.4-4

证明拉普拉斯分布族是指数族.

### 解答 习题 2.4-4

$\left(2\theta\right)^{-n}\exp\left\{-\sum\left|x_i\right|/\theta\right\}$. 自然空间 $\left(-\infty,0\right)$. $\blacksquare$

## 习题 2.4-5

证明瑞利分布族是指数族.

### 解答 习题 2.4-5

$\left(2\theta\right)^n\exp\left\{-\theta\sum x_i^2\right\}\prod x_i$. 自然空间 $\left(-\infty,0\right)$. $\blacksquare$

## 习题 2.4-6

证明指数分布族是指数族.

### 解答 习题 2.4-6

$\lambda^n\exp\left\{-\lambda\sum x_i\right\}$. 自然空间 $\left(-\infty,0\right)$. $\blacksquare$

## 习题 2.4-7

证明对数正态分布族是指数族.

### 解答 习题 2.4-7

二维自然参数 $\varphi_1=\mu/\sigma^2$, $\varphi_2=-1/\left(2\sigma^2\right)$. 空间 $\varphi_2< 0$. $\blacksquare$
