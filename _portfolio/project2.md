---
title: Homework n°3
subtitle: Median,Location or Central Tendecy and Continuous time process simulator
image: /assets/img/portfolio/continuous.jpg
alt: Euler-Maruyama

caption:
  title: Homework 3
  subtitle: Continuous time process simulator
  thumbnail: /assets/img/portfolio/continuous.jpg
---

# **Why the median minimizes the sum of absoloute deviations**

To illustrate why the median is the value of $$c$$ that minimizes the sum of absolute deviations, we can use a formal, simple argument using properties of the absolute value function.

Given a set of $$n$$ ordered data points $$x_1 \leq x_2 \leq \ldots \leq x_n$$ we want to find a value $$c$$ that minimizes the function:

$$S(c) = \sum_{i=1}^{n} |x_i - c|$$

**Proof**

The function $$S(c)$$ is defined as the sum of the absolute deviations of the points $$x_i$$ from a central point $$c$$ :

$$S(c) = |x_1 - c| + |x_2 - c| + \ldots + |x_n - c|$$

Since the absolute value function measures the distance between $$x_i$$ and $$c$$, $$S(c)$$ represents the total distance between $$c$$ and each of the $$x_i$$'s
The absoloute value function $$|x - c|$$ is a piecewise linear function with a "V" shape. It changes its slope at $$x = c$$:  
For $$c < x_i, |x_i - c| = x_i - c$$ (positive slope).  
For $$c > x_i, |x_i - c| = c - x_i$$ (negative slope).

As $$c$$ moves from left to right, the value of each term $$|x_i - c|$$ changes its slope when $$c$$ crosses $$x_i$$.  
To minimize $$S(c)$$, we need to understand how the total slope changes as $$c$$ increases:  
For $$c < x_1$$ (left of all $$x_i$$'s), the slope of each $$|x_i -c|$$ is negative.  
Thus, the overall slope of $$S(c)$$ is negative.   
As $$c$$ passes through each $$x_i$$, the slope of $$|x_i - c|$$ switches from negative to positive, thus increasing the overall slope of $$S(c)$$.  
At each $$x_i$$, a term $$|x_i - c|$$ changes from decreasing to increasing as $$c$$ moves past $$x_i$$.  

For $$S(c)$$ to reach a minimum, its slope must change from negative to positive. This change happens when $$c$$ is such that there are as many data points $$x_i$$ smaller than $$c$$ as there are larger than $$c$$.

This balance occurs at the median:

If $$n$$ is odd, the median is $$x_\frac{(n+1)}{2}$$.
If $$n$$ is even, any value between $$x_\frac{n}{2}$$ and $$x_\frac{n}{2+1}$$ can serve as the median.

Thus, $$S(c)$$ achieves its minimum value when $$c$$ is the median of the data points.  
In conclusion the median is the value of $$c$$ that balances the number of points on either side, thus minimizing the sum of absolute deviations $$\sum_{i=1}^{n} |x_i - c|$$. This balance ensures that the total distance from $$c$$ to all the points is minimized. Hence, the median is the optimal solution.

# **Location (also known as "Center" or "Central Tendecy")**  

In statistics, a "location" measure (also known as "center" or "central tendency") aims to capture a single value that is representative of a distribution of data points. There are multiple ways to define a location, each emphasizing different characteristics of the data or with varying sensitivity to outliers, skewness, or the overall shape of the distribution.

We already seen some of these measures like the Arithmetic Mean and  Median but there are many more, for example:

**Mode**

Definition: The value that appears most frequently in the data.  
Properties: Useful for categorical data, or to identify the most common value in unimodal distributions.

**Geometric Mean**

Definition: The nth root of the product of all data points.  
Properties: Useful for data with exponential growth or multiplicative processes.

**Harmonic Mean**

Definition: The reciprocal of the arithmetic mean of reciprocals.  
Properties: Places greater weight on smaller values, making it useful for rates or ratios.

**Trimmed Mean**

Definition: The mean after removing a fixed proportion of the smallest and largest values.  
Properties: Reduces sensitivity to outliers, especially when distributions are heavy-tailed.

**Winsorized Mean**

Definition: Similar to a trimmed mean, but instead of removing extreme values, they are replaced by the nearest remaining values.  
Properties: Moderates the influence of outliers while retaining all data points.

**Midrange**

Definition: The average of the minimum and maximum values in the dataset.  
Properties: Simple but highly sensitive to outliers.

**Barycenter in a Metric Space**

Definition: The point that minimizes the sum of distances (e.g., Euclidean distances) to all points in a space.  
Properties: This concept generalizes the mean to any metric space.

**Entropy-based Centers**

Definition: Concepts like the maximum entropy estimate aim to find a central point that reflects the most uncertainty or randomness around it.  
Example: Entropy minimization or maximization methods to find a balance between data points.

**L-p Norm-based Centers**

Definition: Location as defined by the point that minimizes the sum of $$p$$-norms of residuals:

$$\sum_{i=1}^{n} |x_i - m|^p$$

Example: For $$p = 2$$, we get the mean; for $$p = 1$$, the median.

This flexibility suggests that, given different ways of defining "distance," "centrality," and "balance," there are theoretically infinite ways to determine what constitutes the "location" of a set of data.

# **Practical part**

**Continuous-Time Attack Simulation**

I refine the SDE simulator to simulate a continuous time process using a parameter *lambda* where this parameter suggests a probability of an event occurring (e.g., an attack succeeding or making a "jump"). 
This aligns with concepts in continuous-time models like Poisson processes, where *lambda* represents the rate of events over time.

![Lambda](/assets/img/portfolio/lambda.jpg)

This kind of simulation is often used in various fields like cybersecurity, risk analysis, queuing theory, and reliability engineering.  

![Continuous Path](/assets/img/portfolio/continuous.jpg)

In real-world scenarios, events like cyberattacks, system failures, or breaches don’t occur at regular intervals but rather happen randomly over time. A continuous-time simulation using jumps allows for the modeling of these occurrences more accurately to give a deeper understanding of the timing and frequency of unpredictable events that significantly affect system performance and security.

[Homework3.rar](https://github.com/GabrielePapalino/statistics/raw/refs/heads/main/Homework%202.rar)

{:.list-inline}

- Date: 23 October 2024