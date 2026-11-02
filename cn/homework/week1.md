# week1

> **基础知识: 样本分布**
> 
> 联合分布为 $\prod F\left(x_i\right)$.

> **基础知识: 总体分布族与样本分布族**
> 
> $\left\{\prod f\left(x_i;\theta\right):\theta\in\Theta\right\}$.

> **定义 1.2.1 (总体)**
> 
> 研究对象的全体.

> **定义 1.3.1 (样本空间)**
> 
> 样本可能取值的全体.

> **定义 1.3.2 (简单随机样本)**
> 
> 独立同分布.

> **定义 1.3.3 (参数空间)**
> 
> 参数所有可能取值的集合.

> **定义 1.4.1 (统计量)**
> 
> 样本的函数, 不含未知参数.

> **定义 1.5.1 (经验分布函数)**
> 
> $F_n\left(x\right)=\frac1n\sum I\left\{X_i\le x\right\}$.
---

## 习题 1-1

什么是总体? 什么是样本?

### 解答 习题 1-1

由**定义 1.2.1 (总体)**, 总体是研究对象的全体. 样本是从总体中随机抽取的部分个体. $\blacksquare$

---

## 习题 1-2

简单随机样本应满足什么条件?

### 解答 习题 1-2

由**定义 1.3.2 (简单随机样本)**, 独立性与代表性 (同分布). $\blacksquare$

---

## 习题 1-4

写出三种总体的样本联合分布.

### 解答 习题 1-4

由**基础知识: 样本分布**, 几何分布 $p^n\left(1-p\right)^{\sum x_i-n}$, 指数分布 $\lambda^n e^{-\lambda\sum x_i}$, 拉普拉斯分布 $\left(\lambda/2\right)^n e^{-\lambda\sum\left|x_i\right|}$. $\blacksquare$

---

## 习题 1-6

写出七种分布的样本分布族.

### 解答 习题 1-6

由**基础知识: 总体分布族与样本分布族**, 分别写出 $\left\{\prod f\left(x_i;\theta\right)\right\}$. $\blacksquare$

---

## 习题 1-7

写出正态总体的统计模型.

### 解答 习题 1-7

$\Theta=\left\{\left(\mu,\sigma^2\right):\mu\in\mathbb R,\sigma^2> 0\right\}$. $\blacksquare$

---

## 习题 1-8

判断哪些是统计量.

### 解答 习题 1-8

含 $\sigma^2$ 的不是统计量, 其余是. $\blacksquare$

---

## 习题 1-9

求经验分布函数.

### 解答 习题 1-9

排序后每点跳跃 $1/10$. $\blacksquare$

---

## 习题 1-10

证明 $E\left(F_n\left(x\right)\right)=F\left(x\right)$, $D\left(F_n\left(x\right)\right)=F\left(x\right)\left(1-F\left(x\right)\right)/n$.

### 解答 习题 1-10

示性函数分解. $\blacksquare$
