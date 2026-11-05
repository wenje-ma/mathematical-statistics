# week4

> **引理 2.3.1 (样本均值与样本方差的期望)**
> 
> $E\left(\overline{X}\right)=\mu$, $D\left(\overline{X}\right)=\sigma^2/n$, $E\left(S^2\right)=\sigma^2$.

> **定理 2.3.3 (正态总体样本均值与样本方差的分布)**
> 
> $\overline{X}\sim{N}\left(\mu,\sigma^2/n\right)$, $\left(n-1\right)S^2/\sigma^2\sim\chi^2\left(n-1\right)$, 二者独立.

## 习题 2.3-5

求 $c$ 使 $c\left(X_{n+1}-\overline{X}\right)/S_n\sim{t}$.

### 解答 习题 2.3-5

$c=\sqrt{\left(n-1\right)/\left(n+1\right)}$, $t\left(n-1\right)$. $\blacksquare$

## 习题 2.3-7

求 $c$ 使 $c\sum_{1}^nX_i^2/\sum_{n+1}^{n+m}X_i^2\sim{F}$.

### 解答 习题 2.3-7

$c=m/n$, $F\left(n,m\right)$. $\blacksquare$

## 习题 2.3-8

求 $a,b$ 使 $a\left(\overline{X}-\mu\right)^2+bS^2\sim\chi^2\left(n\right)$.

### 解答 习题 2.3-8

$a=n/\sigma^2$, $b=\left(n-1\right)/\sigma^2$. $\blacksquare$

## 习题 2.3-9

求 $Y=\left(\left(X_1+X_2\right)/\left(X_1-X_2\right)\right)^2$ 的分布.

### 解答 习题 2.3-9

$F\left(1,1\right)$. $\blacksquare$

## 习题 2.3-12

求 $c$ 使 $cX_1/\sqrt{X_2^2+X_3^2+X_4^2}\sim{t}$.

### 解答 习题 2.3-12

$c=\sqrt3$, $t\left(3\right)$, $E=0$, $D=3$. $\blacksquare$

## 习题 2.3-19

均匀样本均值的极限分布.

### 解答 习题 2.3-19

由中心极限定理, $N\left(0,1\right)$. $\blacksquare$

## 习题 2.3-20

泊松样本均值的极限分布.

### 解答 习题 2.3-20

由斯卢茨基引理, $N\left(0,1\right)$. $\blacksquare$
