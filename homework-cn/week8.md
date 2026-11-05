# week8

> **定义 3.3.2 (极大似然估计)**
> 
> $L\left(\widehat\theta\right)=\sup{L}\left(\theta\right)$.

> **定义 3.4.1 (无偏估计)**
> 
> $E\left(\widehat\theta\right)=\theta$.

> **定义 3.4.2 (有效性)**
> 
> 方差小者有效.

> **定义 3.4.3 (相合估计)**
> 
> 依概率收敛于 $\theta$.

> **引理 3.5.1 (改进无偏估计的方法)**
> 
> 对充分统计量取条件期望.

> **定理 3.5.1 (Lehmann-Scheffe 定理)**
> 
> 充分完备统计量的无偏函数为 UMVUE.

> **推论 3.5.1 (指数族自然形式下的充分完备统计量)**
> 
> 自然参数空间有内点.

> **例 3.5.3 (两点分布的充分完备统计量)**
> 
> $\sum{X}_i\sim{B}\left(n,p\right)$.

> **例 3.5.7 (正态总体的充分完备统计量)**
> 
> $\left(\overline{X},\sum\left(X_i-\overline{X}\right)^2\right)$.

## 习题 3.3-6

双参数指数分布 MLE.

### 解答 习题 3.3-6

$\widehat\mu=X_{\left(1\right)}$, $\widehat\lambda=1/\left(\overline{X}-X_{\left(1\right)}\right)$, $\widehat\alpha=\exp\left\{-\left(t-X_{\left(1\right)}\right)/\left(\overline{X}-X_{\left(1\right)}\right)\right\}$. $\blacksquare$

## 习题 3.4-1

求 $c$ 使相邻差平方和无偏.

### 解答 习题 3.4-1

$c=1/\left[2\left(n-1\right)\right]$. $\blacksquare$

## 习题 3.4-5

平移指数分布的矩估计与 MLE 无偏性.

### 解答 习题 3.4-5

$\widehat\theta_1=\overline{X}-1$ 无偏; $\widehat\theta_2=X_{\left(1\right)}$ 有偏. $\blacksquare$

## 习题 3.4-7

比较两个无偏估计的有效性.

### 解答 习题 3.4-7

$T_2$ 更有效. $\blacksquare$

## 习题 3.4-10

均方收敛蕴含相合.

### 解答 习题 3.4-10

切比雪夫不等式. $\blacksquare$

## 习题 3.4-12

几何均值是 $\theta/e$ 的相合估计.

### 解答 习题 3.4-12

大数定律. $\blacksquare$

## 习题 3.5-4

求 $p^m$ 与 $p\left(1-p\right)$ 的 UMVUE.

### 解答 习题 3.5-4

$\widehat{g}_1$ 组合数比; $\widehat{g}_2=T\left(n-T\right)/\left[n\left(n-1\right)\right]$. $\blacksquare$
