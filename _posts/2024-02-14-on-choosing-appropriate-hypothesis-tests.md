---
layout: post
mathjax: true
title: "On choosing appropriate hypothesis tests"
---

1. **Variances**
	- Population variance: The variance of the entire population, denoted by $\sigma^2$
	- (Biased) Sample variance: The variance of a particular sample from a population, denoted by $S^2$
	- Unbiased estimator for population variance: An estimate of population variance when it is unknown, denoted by $s^2$ or $\hat{\sigma^2}$.
	- **Bessel's correction** - The variances obey the following relationship: $$s^2 = \frac{n}{n-1}S^2$$
	- Standard error refers to $\dfrac{s}{\sqrt{n}}$.
<br>

2. **Means**
	- Population mean: denoted by $\mu$.
	- Sample mean: usually denoted by $\overline{x}$.
	- $\overline{x}$ is an unbiased estimator for $\mu$.
<br>

3. **Parameters and tests for confidence intervals**
	- Population mean with known population variance: $z$-test
	- Population mean using a large sample (unknown $\sigma^2$): $z$-test, use unbiased estimator of population variance, $s^2$. 
	- Population mean using small sample (unknown $\sigma^2$): $t$-test ($\nu = n-1$ degrees of freedom)
	- Population proportion, $\hat{p}$: $z$-test
	- Difference in population means: 
		- Small samples: $t$-test
		- Large sample: $z$-test
		- Matched pairs: $t$-test
<br>

4. **Hypothesis testing** <br>
	1. Difference in means (two-sample $t$-test)
		- Assumptions: 
			- Underlying distributions are normal
			- Populations are independent
			- Population variance of the two populations is the same (but may be unknown).
		- If $n_1$ and $n_2$ are large ($\ge 30$), then the distribution of $(\overline{X}-\overline{Y})$ is given by $$(\overline{X}-\overline{Y}) \sim N\left(\mu_x-\mu_y, \frac{s_1^2}{n_1}+\frac{s_2^2}{n_2}\right)$$ and test statistic is $$z = \dfrac{\overline{X}-\overline{Y}-(\mu_x-\mu_y)}{\sqrt{\frac{s_1^2}{n_1}+\frac{s_2^2}{n_2}}}$$
		- If $n_1$ and $n_2$ are small ($<30$), and the two populations are normally distributed with an **unknown common variance**, then the test statistic $t$ has the distribution $$(\overline{X}-\overline{Y}) \sim t_{n_1+n_2-2}\left(\mu_x-\mu_y, s_p^2\left(\frac{1}{n_1}+\frac{1}{n_2}\right)\right)$$ and $$t = \dfrac{(\overline{X}-\overline{Y})-(\mu_x-\mu_y)}{s_p^2\left(\frac{1}{n_1}+\frac{1}{n_2}\right)}.$$
		- If the sample sizes are too small to allow us to use $s_x^2$ and $s_y^2$ are estimators, we need to pool these variances (combine them).
		- The pooled estimate of the population variance is
$$\begin{aligned} s_p^2 &= \frac{\sum(x-\overline{x})^2+\sum(y-\overline{y})^2}{n_x+n_y+2} \\ &= \frac{(n_x-1)s_x^2+(n_y-1)s_y^2}{n_x+n_y+2}.\end{aligned}$$
  
	2. Difference in means: Paired sample $t$-tests
		- Assumptions:
			- Differences are normally distributed
			- Population variance of the two populations is the same (but may be unknown).
			- Data are matched pairs (repeated measures design).
		- The test statistic $t$ has the distribution  $D \sim N\left(\mu_d, \dfrac{s_d^2}{n}\right)$ and $$t = \frac{\overline{d}-k}{\frac{s_d}{\sqrt{n}}}.$$ <br>
	3. Difference in means: Normal distribution 
		- Assumptions:
			- Underlying distributions are normal
			- Large sample sizes
			- Populations are independent
			- Population variance of the two populations is the same (but may be unknown)
		- The test statistic is $$Z = \frac{(\overline{X}-\overline{Y})-(\mu_x - \mu_y)}{\sqrt{\frac{\sigma_x^2}{n_x}+\frac{\sigma_y^2}{n_y}}} \sim N(0,1).$$
