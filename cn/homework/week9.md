# week9

> **定义 3.3.2 (极大似然估计)**
> 
> $L\left(\hat\theta\right)=\sup L\left(\theta\right)$.
---

## 习题 3.3-3

求五种分布的 MLE.

### 解答 习题 3.3-3

(1) $-1-n/\sum\ln X_i$; (2) $1/\bar X$; (3) $\frac1n\sum\left|X_i\right|$; (4) $\left[X_{\left(n\right)}-0.5,X_{\left(1\right)}+0.5\right]$; (5) $\hat\mu=\overline{\ln X}$, $\hat\sigma^2$ 对数样本方差. $\blacksquare$

---

## 习题 3.3-4

正态分布 MLE.

### 解答 习题 3.3-4

(1) $\hat\mu=\bar X$; (2) $\hat\sigma^2=\frac1n\sum\left(X_i-\mu\right)^2$. $\blacksquare$

---

## 习题 3.3-6

双参数指数分布 MLE.

### 解答 习题 3.3-6

$\hat\mu=X_{\left(1\right)}$, $\hat\lambda=1/\left(\bar X-X_{\left(1\right)}\right)$, $\hat\alpha=\exp\left\{-\left(t-X_{\left(1\right)}\right)/\left(\bar X-X_{\left(1\right)}\right)\right\}$. $\blacksquare$
