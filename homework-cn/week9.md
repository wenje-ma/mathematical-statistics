# week9

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

> **定义 3.6.1 (正则分布族)**
> 
> C-R 正则条件.

> **定理 3.6.1 (单参数 C-R 不等式)**
> 
> $D\left(\widehat{g}\right)\ge\left[g'\right]^2/\left[nI\left(\theta\right)\right]$.

> **定义 3.6.2 (效率)**
> 
> C-R 下界与方差之比.

> **定义 3.6.3 (有效估计)**
> 
> 效率为 1.

> **定义 4.1.1 (区间估计)**
> 
> 随机区间估计参数.

> **定义 4.1.4 (置信区间)**
> 
> 覆盖概率 $\ge1-\alpha$.

> **定义 4.1.5 (置信限)**
> 
> 单侧置信上下限.

## 习题 3.5-6

求 $\sigma$ 与 $\sigma^4$ 的 UMVUE.

### 解答 习题 3.5-6

$\widehat\sigma=\Gamma\left(n/2\right)/\left[\sqrt2\Gamma\left(\left(n+1\right)/2\right)\right]\sqrt{T}$; $\widehat\sigma^4=T^2/\left[n\left(n+2\right)\right]$. $\blacksquare$

## 习题 3.5-7

求 $\mu+\sigma^2$, $\mu^2/\sigma^2$ 的 UMVUE.

### 解答 习题 3.5-7

$\overline{X}+S^2$; $\left[\left(n-3\right)\overline{X}^2\right]/\left[\left(n-1\right)S^2\right]-1/n$. $\blacksquare$

## 习题 3.6-1

证明 $I\left(\theta\right)=-E\left[\partial^2\ln{f}/\partial\theta^2\right]$.

### 解答 习题 3.6-1

对 $\int{f}=1$ 两次求导. $\blacksquare$

## 习题 3.6-2

求负二项分布的费希尔信息量.

### 解答 习题 3.6-2

$I\left(\theta\right)=2/\left[\theta^2\left(1-\theta\right)\right]$. $\blacksquare$

## 习题 3.6-4

证明 $\overline{X}$ 是有效估计.

### 解答 习题 3.6-4

$D\left(\overline{X}\right)=\theta^2/n$ 等于 C-R 下界. $\blacksquare$

## 习题 3.6-6

证明 $\overline{X}^2-1/n$ 是 UMVUE 但非有效.

### 解答 习题 3.6-6

方差 $4\mu^2/n+2/n^2>4\mu^2/n$. $\blacksquare$

## 习题 4.1-4

求置信水平.

### 解答 习题 4.1-4

$0.90$. $\blacksquare$
