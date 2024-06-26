---
layout: post
title: "lcm[k,m,n] * gcd(km,mn,nk)= kmn"
mathjax: true
categories:
  - github
  - website
---

### Problem
> Prove that $\text{lcm}[k,m,n] \cdot \text{gcd}(km,mn,nk)= kmn$ where $k,m,n$ are natural numbers.

### Solution
We can first express $k, m, n$ using their prime factorization.
<!--more-->

$$\begin{align*}
k &= p_1^{a_1}p_2^{a_2}p_3^{a_3} \cdots \\
m &= p_1^{b_1}p_2^{b_2}p_3^{b_3} \cdots \\
n &= p_1^{c_1}p_2^{c_2}p_3^{c_3} \cdots \\
\end{align*}$$

where $a_i, b_i, c_i$ are nonnegative integers.

WLOG we assume $a_i \le b_i \le c_i \forall i \in \mathbb{Z^+}$, then

$$\begin{align*}
\text{lcm}[k,m,n] \cdot \text{gcd}(km,mn,nk) &= \left(\prod^{\infty}_{i = 1}p_i^{\max(a_i, b_i, c_i)}\right)\left(\prod^{\infty}_{i = 1}p_i^{\min(a_i+b_i, b_i+c_i, c_i+a_i)}\right) \\
&= \left(\prod^{\infty}_{i = 1}p_i^{c_i}\right) \left(\prod^{\infty}_{i = 1}p_i^{a_i + b_i}\right) \\
&= \left(\prod^{\infty}_{i = 1}p_i^{a_i}\right) \left(\prod^{\infty}_{i = 1}p_i^{b_i}\right) \left(\prod^{\infty}_{i = 1}p_i^{c_i}\right)\\
&= kmn \\
\end{align*}$$

$\blacksquare$
