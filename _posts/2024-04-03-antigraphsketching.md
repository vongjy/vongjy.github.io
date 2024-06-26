---
layout: post
mathjax: true
title: "Antigraphsketching"
---


In this article, we will solve an inequality using pure algebra instead of the conventional graph sketching method.

> Given $\displaystyle f(x) = \frac{x^2 + 1}{(x+1)(x-7)}$, find the set of values of $x$ that satisfy $f(x) > \dfrac{1}{f(x)}$.

We first note that $f(x) > 0 \iff x<-1 \vee x> 7$ and $f(x) < 0 \iff -1 < x < 7$ by sign test.

<br>

**Case #1:** $f(x) > 0$

$$\begin{aligned} 
& f(x) > \frac{1}{f(x)} \\ 
\implies & (f(x))^2 - 1 > 0 \\ 
\iff & (f(x)-1)(f(x)+1) > 0 \\ 
\end{aligned} $$

<br>

From the inequality above, $f(x) < -1$ (reject since $f(x) > 0$) and $f(x) > 1$.

<br>

When $f(x) > 1$, 

$$\begin{aligned} 
& \frac{x^2 + 1}{(x+1)(x-7)} > 1 \\ 
\iff & \frac{6x + 8}{(x+1)(x-7)} > 0 \\ 
\iff & \frac{x + \frac{4}{3}}{(x+1)(x-7)} > 0 \\ 
\end{aligned}$$

By sign test, $-\dfrac{4}{3} < x < -1$ and $x > 7$.

<br>

**Case #2:** $f(x) < 0$

$$\begin{aligned} 
& f(x) > \frac{1}{f(x)} \\ 
\implies & (f(x))^2 - 1 < 0 \\ 
\iff & (f(x)-1)(f(x)+1) < 0 \\ 
\end{aligned} $$

From the inequality above, $-1 < f(x)< 0$ .

This gives 

$$-1 < \frac{x^2 + 1}{(x+1)(x-7)} < 0 $$
This case works for $-1 < x < 7$, so $(x+1)(x-7) < 0$. 

We split the inequality into two parts again.

$$\begin{aligned} 
& \frac{x^2 + 1}{(x+1)(x-7)} < 0 \\
\iff & x^2 + 1 > 0 \\
\iff & x^2 > -1 \\
\implies & x \in \mathbb{R} \\
\end{aligned} $$

$$\begin{aligned} 
& \frac{x^2 + 1}{(x+1)(x-7)} > -1 \\ 
\implies & x^2 + 1 < 6x +7 -x^2 \\ 
\iff & x^2 -3x -3 < 0 \\
\implies & \frac{3-\sqrt{21}}{2} < x < \frac{3+\sqrt{21}}{2} \\
\end{aligned}$$

From case #2, we conclude $\dfrac{3-\sqrt{21}}{2} < x < \dfrac{3+\sqrt{21}}{2}$.

Thus, $$x \in \boxed{\left(-\frac{4}{3},1\right) \cup \left(\frac{3-\sqrt{21}}{2},\frac{3+\sqrt{21}}{2}\right) \cup (7,\infty)}.$$

[Link to graph](https://www.desmos.com/calculator/qzr3miloeu)
