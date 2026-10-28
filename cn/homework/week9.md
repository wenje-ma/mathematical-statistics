# week9

> **基础知识: 似然函数与对数似然函数**<br>$L=\prod f(x_i;\theta)$.

> **基础知识: 极大似然估计的求法**<br>对数似然方程.

> **基础知识: 极大似然估计的不变性**<br>$g(\hat\theta)$ 为 $g(\theta)$ 的 MLE.

> **定义 3.3.2 (极大似然估计)**<br>$L(\hat\theta)=\sup L(\theta)$.
---

## 习题 3.3-3

求五种分布的 MLE.

### 解答 习题 3.3-3

(1) $-1-n/\sum\ln X_i$; (2) $1/\bar X$; (3) $\frac1n\sum|X_i|$; (4) $[X_{(n)}-0.5,X_{(1)}+0.5]$; (5) $\hat\mu=\overline{\ln X}$, $\hat\sigma^2$ 对数样本方差. $\blacksquare$

---

## 习题 3.3-4

正态分布 MLE.

### 解答 习题 3.3-4

(1) $\hat\mu=\bar X$; (2) $\hat\sigma^2=\frac1n\sum(X_i-\mu)^2$. $\blacksquare$

---

## 习题 3.3-6

双参数指数分布 MLE.

### 解答 习题 3.3-6

$\hat\mu=X_{(1)}$, $\hat\lambda=1/(\bar X-X_{(1)})$, $\hat\alpha=\exp\{-(t-X_{(1)})/(\bar X-X_{(1)})\}$. $\blacksquare$
