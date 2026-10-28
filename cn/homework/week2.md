# week2

> **基础知识: 泊松分布的可加性**<br>$\sum P(\lambda_i)\sim P(\sum\lambda_i)$.

> **基础知识: 正态分布的可加性**<br>$\sum N(\mu_i,\sigma_i^2)\sim N(\sum\mu_i,\sum\sigma_i^2)$.

> **基础知识: 抽样分布**<br>统计量的分布.

> **基础知识: 顺序统计量的分布**<br>$f_{(r)}(x)=rC_n^r F^{r-1}(x)(1-F)^{n-r}f(x)$.

---

## 习题 2.1-1

求 $\sum X_i$ 的分布, $X_i\sim P(\lambda)$.

### 解答 习题 2.1-1

由**基础知识: 泊松分布的可加性**, $T\sim P(n\lambda)$. $\blacksquare$

---

## 习题 2.1-2

求 $\sum X_i$ 的分布, $X_i\sim N(\mu,\sigma^2)$.

### 解答 习题 2.1-2

由**基础知识: 正态分布的可加性**, $T\sim N(n\mu,n\sigma^2)$. $\blacksquare$

---

## 习题 2.1-3

证明二项分布尾概率的积分表示.

### 解答 习题 2.1-3

对 $p$ 求导后逐项相消. $\blacksquare$

---

## 习题 2.1-5

求指数分布最小顺序统计量的密度与矩.

### 解答 习题 2.1-5

$X_{(1)}\sim E(n\lambda)$. $\blacksquare$

---

## 习题 2.1-6

求正态总体最小/最大顺序统计量概率.

### 解答 习题 2.1-6

$[1-\Phi(1)]^9$ 与 $[\Phi(1)]^9$. $\blacksquare$

---

## 习题 2.1-7

求均匀分布顺序统计量密度.

### 解答 习题 2.1-7

$f_{(1)}=n(\theta_2-x)^{n-1}/(\theta_2-\theta_1)^n$. $\blacksquare$
