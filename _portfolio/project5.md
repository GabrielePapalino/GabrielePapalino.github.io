---
title: Homework n°6
subtitle: Fundamental Theorem of Calculus (FTC) and probability distributions with their CDFs
image: /assets/img/portfolio/home.jpg
alt: SDE

caption:
  title: Homework 6
  subtitle: Fundamental Theorem of Calculus (FTC)
  thumbnail: /assets/img/portfolio/home.jpg
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







{:.list-inline}

- Date: 13 November 2024