---
title: Homework n°2
subtitle: Recursive calculation of the Mean and Variance of the attackers vs server simulation with absoloute and relative frequencies.
image: /assets/img/portfolio/euler-maru.jpg
alt: Euler-Maruyama

caption:
  title: Homework 2
  subtitle: Euler–Maruyama simulator
  thumbnail: /assets/img/portfolio/timestep.jpg
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

This stocastic process using the Euler-Maruyama method simulates multiple attackers trying to exploit vulnerabilities in a set of servers, using a probabilistic approach. It visualizes the outcomes of each attacker's attempts through three different types of graphs:

**Random Walk**

![timestep](/assets/img/portfolio/timestep2.jpg)

Shows the overall attack progression for each attacker as they succeed or fail in exploiting vulnerabilities. This is done by emulating a random walk with parameters +1 in case of success and -1 otherwise. Furthermore, in order to understand the performance of the simulation for a given intermediate time t, the distribution at that time is calculated with its mean and variance.

![Code for t interval](/assets/img/portfolio/codedelta.jpg)

Similar to the one on previous homework this method is used to draw the histogram for a given input delta t used to select the partial time on the x-axis. 

**Absoloute Frequency**

![Absoloute Frequency](/assets/img/portfolio/absoloute.jpg)

 Absolute trajectories in this context refer to the path or progression of an attacker’s success in exploiting servers over time, represented on the absolute graph. Each trajectory illustrates how the total number of successful attacks changes with each step or server interaction.


**Relative Frequency**

![Relative Frequency](/assets/img/portfolio/relative.jpg)

Relative trajectories in this context represent the success rate of attackers over time, visualized on the relative graph. Unlike absolute trajectories, which track the total number of successful attacks, relative trajectories focus on the ratio of successes to attempts, providing a measure of how efficiently an attacker is performing as they continue to interact with servers.
By examining relative trajectories, you can understand not just how many successes an attacker achieved, but how effectively they achieved them throughout the simulation.

**Personal considerations**

**Mean:**

The absolute mean is approximately 0.8197, which suggests the average outcome of the simulated process when considering all samples. This value reflects the central tendency of the data.
The relative mean, which is also 0.8197, implies that the mean value normalized to the relative context (e.g., proportion of success or frequency in comparison to a total) is the same as the absolute mean. This might be due to the nature of the simulation, where the absolute measure directly translates into a proportion.

**Variance:**

The absolute variance is 3.1314, indicating the spread or dispersion of the values around the mean. A higher variance suggests that the data points are more spread out from the mean.
The relative variance, 40.3118, is much higher than the absolute variance. This could mean that when adjusting for the relative context (e.g., the variance of a proportion or frequency), the spread becomes more significant. This is often seen when probabilities or proportions are translated into relative measures, which can exaggerate variability.

**T Mean and T Variance:**

The T Mean (0.4167) and T Variance (2.8888) might be derived from a transformed or secondary variable within the simulation. These values are lower than the absolute measures, suggesting that the transformed data have a lower central tendency and slightly less variability.

**Conclusions**

Overall, the mean and variance values suggest a simulation with some spread, and the difference between absolute and relative variance hints at a model where proportions introduce additional variability.

[Homework2.rar](https://github.com/GabrielePapalino/statistics/raw/refs/heads/main/Homework%202.rar)

{:.list-inline}

- Date: 16 October 2024

