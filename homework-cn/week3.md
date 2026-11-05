# week3

> **定义 2.2.1 ($\chi^2$ 分布)**
> 
> $\sum{N}\left(0,1\right)^2$.

> **定理 2.2.1 ($\chi^2$ 分布的密度函数)**
> 
> $Ga\left(n/2,1/2\right)$.

> **推论 2.2.1 ($X/Y$ 与 $X+Y$ 的独立性)**
> 
> 独立卡方变量的比值与和独立.

> **定义 2.2.2 ($t$ 分布)**
> 
> $N\left(0,1\right)/\sqrt{\chi^2\left(n\right)/n}$.

> **定理 2.2.2 ($t$ 分布的密度函数)**
> 
> 对称钟形.

> **定义 2.2.3 ($F$ 分布)**
> 
> $\left(\chi^2\left(m\right)/m\right)/\left(\chi^2\left(n\right)/n\right)$.

> **引理 2.3.1 (样本均值与样本方差的期望)**
> 
> $E\left(\overline{X}\right)=\mu$, $D\left(\overline{X}\right)=\sigma^2/n$, $E\left(S^2\right)=\sigma^2$.

> **定理 2.3.3 (正态总体样本均值与样本方差的分布)**
> 
> $\overline{X}\sim{N}\left(\mu,\sigma^2/n\right)$, $\left(n-1\right)S^2/\sigma^2\sim\chi^2\left(n-1\right)$, 二者独立.

## 习题 2.2-2

证明 $E\left(X^k\right)=2^k\Gamma\left(n/2+k\right)/\Gamma\left(n/2\right)$.

### 解答 习题 2.2-2

伽马积分. $\blacksquare$

## 习题 2.2-3

证明概率积分变换与 $-2\sum\ln{Y}_i\sim\chi^2\left(2n\right)$.

### 解答 习题 2.2-3

$F\left(X\right)\sim{U}\left(0,1\right)$, $-2\ln{U}\sim\chi^2\left(2\right)$. $\blacksquare$

## 习题 2.2-6

证明伽马分布性质.

### 解答 习题 2.2-6

特征函数与矩. $\blacksquare$

## 习题 2.2-7

证明 $X/Y$ 与 $X+Y$ 独立.

### 解答 习题 2.2-7

变量分离. $\blacksquare$

## 习题 2.2-8

证明 $t\left(n\right)\to{N}\left(0,1\right)$.

### 解答 习题 2.2-8

斯特林公式. $\blacksquare$

## 习题 2.2-10

求 $P\left(F\left(1,1\right)<1\right)$.

### 解答 习题 2.2-10

$1/2$. $\blacksquare$

## 习题 2.3-2

泊松样本的 $E\left(\overline{X}\right)$, $D\left(\overline{X}\right)$, $E\left(S^2\right)$.

### 解答 习题 2.3-2

由**引理 2.3.1 (样本均值与样本方差的期望)**, 均为 $\lambda$, $\lambda/n$, $\lambda$. $\blacksquare$

## 习题 2.3-4

正态样本的 $D\left(S^2\right)$.

### 解答 习题 2.3-4

$D\left(S^2\right)=2\sigma^4/\left(n-1\right)$. $\blacksquare$
