---
layout: post
mathjax: true
title: "Approximating Probability Distributions Done Right"
---
_Disclaimer: This post is written based on the syllabus for Cambridge International AS and A Levels, and may not be applicable for higher level studies._

## Approximation
1. Binomial to Normal:
	- Conditions*: $np > 5$ and $nq > 5$ ($n$ is sufficiently large).
	- Apply continuity correction.

2. Binomial to Poisson:
	- A Poisson distribution can be used to model a discrete probability distribution in which the events
		- occur singly, 
		- at random and independently, 
		- in a given interval of space or time.
	- The mean and variance of a Poisson distribution are equal.
	- Conditions*: $n > 50$ and $np < 5$ ($n$ is large, $p$ is small/rare event).

3. Poisson to Normal:
	- Conditions*: $\lambda > 15$
	- Apply continuity correction.

## Central Limit Theorem
> The central limit theorem (CLT) states that, provided $n$ is large, the distribution of **sample means** of size $n$ is: 
$$\overline{X}(n) \sim N\left(\mu, \frac{\sigma^2}{n}\right),$$where the original population has mean $\mu$ and variance $\sigma^2$.

- CLT can be used for sample size $n > 50$* (or $n > 30$**).

*Rule of thumb <br>
**For Further Statistics

References:
1. Chalmers, Dean. Cambridge International AS & A Level Mathematics: Probability & Statistics 1 - Coursebook. Cambridge University Press, 2018.
2. Kranat, Jayne. Cambridge International AS & A Level Mathematics: Probability & Statistics 2 - Coursebook. Cambridge University Press, 2018.
3. McKevley, Lee, and Crozier, Martin. Cambridge International AS & A Level Further Mathematics - Coursebook. Cambridge University Press, 2018.
