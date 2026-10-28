# week12

> **定义 3.6.1 (正则分布族)**<br>C-R 正则条件.

> **定理 3.6.1 (单参数 C-R 不等式)**<br>$D(\hat g)\ge [g']^2/[nI(\theta)]$.

> **定义 3.6.2 (效率)**<br>C-R 下界与方差之比.

> **定义 3.6.3 (有效估计)**<br>效率为 1.
---

## 习题 3.6-1

证明 $I(\theta)=-E[\partial^2\ln f/\partial\theta^2]$.

### 解答 习题 3.6-1

对 $\int f=1$ 两次求导. $\blacksquare$

---

## 习题 3.6-2

求负二项分布的费希尔信息量.

### 解答 习题 3.6-2

$I(\theta)=2/[\theta^2(1-\theta)]$. $\blacksquare$

---

## 习题 3.6-4

证明 $\bar X$ 是有效估计.

### 解答 习题 3.6-4

$D(\bar X)=\theta^2/n$ 等于 C-R 下界. $\blacksquare$

---

## 习题 3.6-6

证明 $\bar X^2-1/n$ 是 UMVUE 但非有效.

### 解答 习题 3.6-6

方差 $4\mu^2/n+2/n^2>4\mu^2/n$. $\blacksquare$
