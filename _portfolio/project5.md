---
title: Homework n°6
subtitle: Fundamental Theorem of Calculus (FTC) and probability distributions with their CDFs
image: /assets/img/portfolio/distribution.jpg
alt: SDE

caption:
  title: Homework 6
  subtitle: Fundamental Theorem of Calculus (FTC)
  thumbnail: /assets/img/portfolio/distribution.jpg
---

# **Fundamental Theorem of Calculus (FTC) and probability distributions with their CDFs**

The key relationships between the Fundamental Theorem of Calculus and probability distributions are:

Fundamental Theorem of Calculus:

First Part: $$F'(x) = f(x)$$ for continuous functions  
Second Part: $$\int_{a}^{b} f(x)\,dx\ = F(b) - F(a)$$


Application to Probability:

PDF ($$f(x)$$) is analogous to the derivative function  
CDF ($$F(x)$$) is analogous to the antiderivative

Their relationship is exactly what FTC describes:

$$F(x) = \int_{\infty}^{x} f(t)\,dt$$ (CDF as integral of PDF)  
$$f(x) = \frac{d}{dx} F(x)$$ (PDF as derivative of CDF)


**Key Properties:**

The cumulative distribution function (cdf) gives the probability that the random variable $$X$$ is less than or equal to $$x$$ and is usually denoted $$F(x)$$. The cumulative distribution function of a random variable $$X$$ is the function given by

$$F(x) = P[X \leq x]$$

CDF Properties:

$$\lim_{x\to\infty} F(x)  = 0$$  
$$\lim_{x\to\infty} F(x)  = 1$$

Monotonically increasing  
Right-continuous


The PDF is the density of probability rather than the probability mass. The concept is very similar to mass density in physics: its unit is probability per unit length. To get a feeling for PDF, consider a continuous random variable $$X$$ and define the function $$f_X(x)$$ as follows (wherever the limit exists):

$$f_X(x) = \lim_{\Delta \to 0^+} \frac{P(x < X \leq x + \Delta)}{\Delta}.$$


PDF Properties:

$$f(x) \ge 0$$  
$$\int_{-\infty}^{\infty} f(x)\,dx = 1$$

Represents probability density

Probabilistic Interpretation:

$$P(a < X \leq b)= F(b) - F(a) = \int_{a}^{b} f(x)\,dx$$  

This is exactly what FTC tells us about the relationship between a function and its integral

The relationship between PDFs and CDFs through FTC allows us to:

Move between probability calculations flexibly  
Understand the geometric interpretation of probability  
Derive properties of distributions  
Compute probabilities efficiently  


**Applications:**

Finding probabilities of intervals  
Computing expected values: $$\mathbb{E} = \int_{-\infty}^{\infty} x f(x)\,dx$$  
Generating random variables through inverse CDF 
Computing quantiles and percentiles  

**Conclusions**

This relationship allows us to move between cumulative probabilities and probability densities, making the FTC an essential tool in probability and statistics.

# **Practical Part**

![Distributions](/assets/img/portfolio/distributions.jpg)


To analyze the results displayed in this simulation, let's compare the empirical distribution statistics with the theoretical distribution:

**Theoretical Distribution:**

Mean: 4.90
Variance: 4.13
This distribution represents the expected (ideal) outcome based on a known probability distribution, likely reflecting a uniform or normal distribution used as a reference model for the simulation.

**Empirical Distribution:**

Mean: 5.52
Variance: 7.08
This distribution is derived from the simulated draws (20 in this case), which creates a sample approximation of the theoretical distribution.

**Comparison and Interpretation**

**Mean Comparison:**

The empirical mean (5.52) is slightly higher than the theoretical mean (4.90). This difference suggests that, in this particular sample of 20 draws, the observed values are somewhat skewed to higher values relative to the theoretical expectation.
Since the empirical mean is based on a relatively small sample (20 draws), this difference is expected to decrease with a larger sample size due to the law of large numbers. In larger samples, empirical means typically converge more closely to theoretical means.  

**Variance Comparison:**

The empirical variance (7.08) is noticeably higher than the theoretical variance (4.13). A higher variance in the empirical distribution suggests that the observed values in this sample are more spread out around the mean than the theoretical model predicts.
With a small sample size, it’s common to see a larger empirical variance due to increased sensitivity to outliers or clusters of values. In simulations, smaller samples can exhibit high variance simply because each draw can significantly impact the overall spread.

**Relationship and Implications:**

The differences between empirical and theoretical mean/variance suggest that this particular sample does not perfectly represent the theoretical model, which is expected with only 20 draws.
For more accurate empirical values, increasing the number of draws would typically bring the empirical mean and variance closer to the theoretical values, as random fluctuations would average out across a larger dataset.
This example highlights the importance of sample size in achieving results that are representative of the underlying theoretical distribution, demonstrating how empirical distributions approximate theoretical ones with sufficient data.
In summary, the observed empirical values deviate from the theoretical values, with a higher mean and variance. This deviation can largely be attributed to the small sample size.


[Homework6.rar](https://github.com/GabrielePapalino/statistics/raw/refs/heads/main/Homework%206.rar)


{:.list-inline}

- Date: 13 November 2024