---
layout: post
mathjax: true
title: "Exploring non-parametric tests"
---


## Assumptions
What do various non-parametric tests assume?

| Test                                        | Type of test  | Assumptions                                                                                                                                                                           |
| :------------------------------------------ | :------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Sign test                                   | Single sample | - The underlying data are continuous.<br>- The data are independent.                                                                                                                  |
| Wilcoxon signed-rank test                   | Single sample | - The underlying data are symmetric.<br>- The underlying data are continuous.<br>- The data are independent.                                                                          |
| Paired sign test                            | Two sample    | - The data are in matched pairs.<br>- The differences between matched pairs are continous.<br>- The data are independent.                                                             | <!--more-->
| Wilcoxon matched-pairs <br>signed-rank test | Two sample    | - The data are in matched pairs.<br>- The differences between matched pairs are symmetrical.<br>- The differences between matched pairs are continous.<br>- The data are independent. |
| Wilcoxon rank-sum test                      | Two sample    | - The two samples are independent.<br>- The underlying data are symmetric.<br>- The underlying data are continuous.                                                                   |

## Single-sample sign test

- To perform the single-sample sign test, 
  (i) mark the values that are greater than the stated median with a $+$ sign, and 
  (ii) mark those that are less than the stated median with a $-$ sign.
<br>
- If the data are well distributed about the median, we would expect an equal number of $+$ and $-$ signs. Hence, there should be 
  (i) a probability of $\frac{1}{2}$ that any data point is above the median; 
  (ii) a probability of $\frac{1}{2}$ that any data point is below the median.
<br>
- Given $n$ data points, a single-sample sign test is created using $X \sim \mathrm{Bin}(n, 0.5)$. The test statistic can be the number $+$ signs, that is the number of data points greater than the median.
  
  We can calculate the probability that $X$ is 
  (i) above this test statistic, 
  (ii) below this test statistic, or
  (iii) either (in the case of a two-tailed test)
  which is $\mathbb{P}(X \le T | X \sim \mathrm{Bin}(n,0.5))$, where $T$ is the test statistic.
<br>
- In a situation where we have $0$ instead of $+$ or $-$, the data point is discounted.
<br>
- It is possible to approximate the sign test to a normal distribution for large $n$ ($n > 10$ can be considered large).
  
  Let $T = \min(S^+, S^-)$, then $E(T) = np = n/2$, and $\mathrm{Var}(T) = npq = n/4.$
  For large $n$, $$X \sim N\left(\frac{n}{2},\frac{n}{4}\right),$$we can use the normal approximation of the binomial with $p = 0.5$. We must also make sure that we use a continuity correction. 
<br>
- In general, at a significance level $\alpha$, where $0< \alpha < 1$,
  (i) for $H_1: m < m_0$, if $P(X \le S^+) \le \alpha \implies$  reject $H_0$
  (ii) for $H_1: m > m_0$, if $P(X \ge S^+) \le \alpha \implies$  reject $H_0$
  (iii) for $H_1: m \neq m_0$, if $P(X \le T) \le \alpha/2 \implies$  reject $H_0$




