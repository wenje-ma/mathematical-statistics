# week2

> **定义 2.2.1 ($\chi^2$ 分布)**
> 
> $\sum N\left(0,1\right)^2$.

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

## 习题 2.1-1

求 $\sum X_i$ 的分布, $X_i\sim P\left(\lambda\right)$.

### 解答 习题 2.1-1

由泊松分布的可加性, $T\sim P\left(n\lambda\right)$. $\blacksquare$

## 习题 2.1-2

求 $\sum X_i$ 的分布, $X_i\sim N\left(\mu,\sigma^2\right)$.

### 解答 习题 2.1-2

由正态分布的可加性, $T\sim N\left(n\mu,n\sigma^2\right)$. $\blacksquare$

## 习题 2.1-3

证明二项分布尾概率的积分表示.

### 解答 习题 2.1-3

对 $p$ 求导后逐项相消. $\blacksquare$

## 习题 2.1-5

求指数分布最小顺序统计量的密度与矩.

### 解答 习题 2.1-5

$X_{\left(1\right)}\sim E\left(n\lambda\right)$. $\blacksquare$

## 习题 2.1-6

求正态总体最小/最大顺序统计量概率.

### 解答 习题 2.1-6

$\left[1-\Phi\left(1\right)\right]^9$ 与 $\left[\Phi\left(1\right)\right]^9$. $\blacksquare$

## 习题 2.1-7

求均匀分布顺序统计量密度.

### 解答 习题 2.1-7

$f_{\left(1\right)}=n\left(\theta_2-x\right)^{n-1}/\left(\theta_2-\theta_1\right)^n$. $\blacksquare$

## 习题 2.2-1

确定常数使统计量服从 $\chi^2$, $t$, $F$ 分布.

### 解答 习题 2.2-1

$a=1/14$, $b=1/41$; $c=\sqrt{2/3}$; $d=2/3$. $\blacksquare$
