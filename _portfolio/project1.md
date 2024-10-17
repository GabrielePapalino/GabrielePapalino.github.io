---
title: Homework n°2
subtitle: Recursive calculation of the Mean and Variance of the attackers vs server simulation with absoloute and relative frequencies.
image: /assets/img/portfolio/euler-maru.jpg
alt: Euler-Maruyama

caption:
  title: Homework 2
  subtitle: Euler–Maruyama simulator
  thumbnail: /assets/img/portfolio/euler-maru.jpg
---

# **Welford Recursion**

Mathematically, sample variance can be computed as follows:

$$\sigma^2 = \frac{1}{n(n-1)} (n \sum_{i=1}^{n}{x_i}^2 - (\sum_{i=1}^{n}x_k)^2)$$

It can be derived by looking at the differences between the sums of squared differences for $$N$$ and $$N-1$$ samples.

So the difference turns out to be:

$$(N-1){s_N}^2 -(N-2){s_{N-1}}^2$$

$$= \sum_{i=1}^{N}(x_i-\bar{x}_N)^2 - \sum_{i=1}^{N-1}(x_i-\bar{x}_{N-1})^2$$

$$= (x_N-\bar{x}_N)^2 + \sum_{i=1}^{N-1} ((x_i-\bar{x}_N)^2 - (x_i-\bar{x}_{N-1})^2)$$

$$= (x_N-\bar{x}_N)^2 + \sum_{i=1}^{N-1} (x_i-\bar{x}_N + x_i - \bar{x}_{N-1} ) (\bar{x}_{N-1}-\bar{x}_N)$$

$$= (x_N-\bar{x}_N)^2 + (\bar{x}_N-x_N)(\bar{x}_{N-1}-\bar{x}_N)$$

$$= (x_N-\bar{x}_N)(x_N - \bar{x}_N - \bar{x}_{N-1} + \bar{x}_N)$$

$$= (x_N-\bar{x}_N)(x_N - \bar{x}_{N-1})$$

# **Practical Part**






{:.list-inline}

- Date: 16 October 2024

