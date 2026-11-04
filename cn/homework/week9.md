# week9

> **定义 3.3.2 (极大似然估计)**
> 
> $L\left(\widehat\theta\right)=\sup L\left(\theta\right)$.
---

## 习题 3.3-3

求五种分布的 MLE.

### 解答 习题 3.3-3

(1) $-1-n/\sum\ln X_i$; (2) $1/\overline X$; (3) $\frac1n\sum\left|X_i\right|$; (4) $\left[X_{\left(n\right)}-0.5,X_{\left(1\right)}+0.5\right]$; (5) $\widehat\mu=\overline{\ln X}$, $\widehat\sigma^2$ 对数样本方差. $\blacksquare$

---

## 习题 3.3-4

正态分布 MLE.

### 解答 习题 3.3-4

(1) $\widehat\mu=\overline X$; (2) $\widehat\sigma^2=\frac1n\sum\left(X_i-\mu\right)^2$. $\blacksquare$

---

## 习题 3.3-6

双参数指数分布 MLE.

### 解答 习题 3.3-6

$\widehat\mu=X_{\left(1\right)}$, $\widehat\lambda=1/\left(\overline X-X_{\left(1\right)}\right)$, $\widehat\alpha=\exp\left\{-\left(t-X_{\left(1\right)}\right)/\left(\overline X-X_{\left(1\right)}\right)\right\}$. $\blacksquare$
