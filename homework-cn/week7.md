# week7

> **定义 3.2.1 (矩估计)**
> 
> 总体矩等于样本矩.

> **例 3.2.1 结论 (总体均值与方差的矩估计)**
> 
> $\widehat\mu=\overline X$, $\widehat\sigma^2=S_n^2$.

> **定义 3.3.2 (极大似然估计)**
> 
> $L\left(\widehat\theta\right)=\sup L\left(\theta\right)$.

## 习题 3.2-3

求六种分布的矩估计.

### 解答 习题 3.2-3

(1) $\left(2\overline X-1\right)/\left(1-\overline X\right)$; (2) $1/\overline X$; (3) $\frac1n\sum\left|X_i\right|$; (4) $\overline X$; (5) $\widehat\mu=\overline{\ln X}$, $\widehat\sigma^2$ 为对数样本方差; (6) $\widehat\lambda=1/S_n$, $\widehat\mu=\overline X-S_n$. $\blacksquare$

## 习题 3.2-5

求 $P\left(X> 1\right)$ 的矩估计.

### 解答 习题 3.2-5

$1-\Phi\left(\left(1-\overline X\right)/S_n\right)$. $\blacksquare$

## 习题 3.2-7

求帕累托分布矩估计.

### 解答 习题 3.2-7

$\widehat\theta=\overline X/\left(\overline X-1\right)$. $\blacksquare$

## 习题 3.3-3

求五种分布的 MLE.

### 解答 习题 3.3-3

(1) $-1-n/\sum\ln X_i$; (2) $1/\overline X$; (3) $\frac1n\sum\left|X_i\right|$; (4) $\left[X_{\left(n\right)}-0.5,X_{\left(1\right)}+0.5\right]$; (5) $\widehat\mu=\overline{\ln X}$, $\widehat\sigma^2$ 对数样本方差. $\blacksquare$

## 习题 3.3-4

正态分布 MLE.

### 解答 习题 3.3-4

(1) $\widehat\mu=\overline X$; (2) $\widehat\sigma^2=\frac1n\sum\left(X_i-\mu\right)^2$. $\blacksquare$
