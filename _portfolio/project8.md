---
title: Homework n°9
subtitle: The Law of Large Numbers and Distribution of variance
image: /assets/img/portfolio/meanofvariance.jpg
alt: SDE

caption:
  title: Homework 9
  subtitle: The Law of Large Numbers
  thumbnail: /assets/img/portfolio/meanofvariance.jpg
---

# Sampling Mean and Variance

## The Sampling Mean

Perhaps the most important concept in statistics when using a sample to make inferences about a population is the sampling mean. Some of its key properties are as follows:

### Unbiasedness

The sampling mean is an unbiased estimator, meaning the average of all possible sample means equals the true population mean. This ensures that, on average, there is no systematic overestimation or underestimation of the population mean.

### Consistency

The sample mean approaches the true mean of the population as the sample size increases. This property is crucial because it ensures that larger samples yield more accurate representations of the population.

### Normality (with Large Samples)

The Central Limit Theorem (CLT) states that for large enough sample sizes, the distribution of the sampling mean approximates a normal distribution, regardless of the shape of the population distribution. This property is particularly useful in hypothesis testing and confidence interval construction.

## The Sampling Variance

Sampling variance measures the spread of the sampling distribution of the sample mean. Its properties include:

### Inverse Relationship with Sample Size

As the sample size increases, the sampling variance decreases. This implies that estimates of the mean vary less with larger samples.

### Formula

The sampling variance is defined mathematically as:

$$
\text{Var}(\bar{X}) = \frac{\sigma^2}{n}
$$

Here, $$\sigma^2$$ is the population variance, and $$n$$ is the sample size. This formula demonstrates why increasing the sample size results in more accurate estimates.


# The Law of Large Numbers (LLN)

The **Law of Large Numbers (LLN)** is a foundational result in probability theory. It explains why the averages of random samples stabilize as the sample size grows. In other words, the LLN is the theoretical basis for statistical inference, ensuring that large-sample averages approximate the corresponding population parameters.

## Types of LLN

### Weak LLN

The sample mean converges in probability to the population mean. As the sample size increases, the probability of significant deviations from the population mean becomes arbitrarily small.

### Strong LLN

The sample mean almost surely (with probability 1) converges to the population mean. This is a stronger guarantee of convergence but follows the same principle.

## Illustration of LLN

Suppose a fair coin is flipped. The expected proportion of heads is 50%. However, with a small number of flips, the observed proportion may deviate significantly from this value. As the number of flips increases, the observed proportion converges to the true value of 50%.

The LLN does not eliminate randomness but ensures that its influence diminishes as samples grow larger.

# Applications of LLN in Cybersecurity

The LLN has broad applications in cybersecurity, where stable averages and predictable patterns are essential for identifying anomalies, assessing risks, and making informed decisions. Examples include:

## Anomaly Detection

Network traffic and user behavior often follow predictable patterns when systems are functioning normally. Large datasets collected over time establish baselines for "normal" behavior.

### Example:

In monitoring network traffic, LLN ensures that averages for metrics like packet sizes, request frequencies, and access times stabilize. A sudden deviation from these averages may signal anomalies such as:

A DDoS attack, where traffic spikes beyond normal ranges.  
Unusual user activity, potentially indicating compromised credentials.

## Risk Assessment

Organizations rely on quantitative models to analyze vulnerabilities and risks. The LLN ensures that as more systems, devices, or incidents are analyzed, the calculated average risk score becomes a reliable measure of cybersecurity posture.

### Example:

Repeated Monte Carlo simulations of the financial impact of a ransomware attack refine the expected average loss, providing a robust estimate for risk management and budgetary decisions.

## Behavioral Profiling

Profiling user behavior is a common method for detecting insider threats or account takeovers in cybersecurity.

### Example:

A user may access, on average, a specific number of files per day. Over time, the LLN ensures that this average stabilizes. If a user suddenly accesses hundreds of files, it could indicate malicious activity.

## Metrics for Security Tools

Security solutions, such as antivirus software or intrusion detection systems, depend on performance metrics like detection and false-positive rates. The LLN ensures that these metrics stabilize when tested on large datasets, enabling fair comparisons and informed decisions.

### Example:

Evaluating the detection rate of an intrusion detection system over thousands of simulated attacks ensures the average detection rate is reliable, aiding in determining its effectiveness.

## Predictive Analytics and Threat Intelligence

Predictive models in cybersecurity often leverage historical data to forecast future risks. The LLN ensures that as more data is collected, the averages and trends become robust predictors.

### Example:

A model predicting phishing email volumes uses historical data. The LLN ensures that the average number of phishing emails detected each month stabilizes, making forecasts more reliable.

## Conclusions

The LLN underscores the importance of collecting and analyzing large datasets in cybersecurity. Whether it's monitoring system logs, analyzing threat intelligence feeds, or profiling user behavior, larger datasets lead to more reliable insights.

# Practical Part


![Variance distribution](/assets/img/portfolio/meanofvariance7.jpg)

## Analysis of the Simulation of Sample Variances and Theoretical Distribution

### Parent (Theoretical) Distribution

The theoretical distribution has:

**Mean**: 6.15  
**Variance**: 18.17  

These characteristics represent the expected properties of the parent population from which samples are drawn.

### Distribution of Sample Variances

The top histogram (in **purple**) illustrates the distribution of sample variances.  
These sample variances are computed from repeated experiments of drawing $$ n $$ samples from the parent distribution.

### Relationship Observed

The **mean of the sample variances** is **7.28**, which is smaller than the theoretical variance of **18.17**.  

This discrepancy may be caused by:

Insufficient sample size
Sampling bias
Other factors affecting estimation accuracy

The **variance of the sample variances** is **0.07**, indicating that the sample variances exhibit limited spread around their mean.

### Theoretical and Empirical Alignment

Although the variability of the sample variances (small spread) aligns closely with expectations, the mean of the sample variances does **not** fully match the theoretical variance.

**Convergence Expectation**: As the sample size and number of simulations increase:

The mean of the sample variances should converge toward the theoretical variance of the parent distribution.

### Key Facts

The relatively small mean of the sample variances (compared to the theoretical variance) indicates that:

The sampling process or sample size may not adequately capture the full variability of the population.

**Recommendations**:
Increase the number of samples drawn.
Perform more simulations to reduce bias and achieve closer alignment between the sample and theoretical properties.


[Homework9.rar](https://github.com/GabrielePapalino/statistics/raw/refs/heads/main/Homework%209.rar)

{:.list-inline}

- Date: 4 December 2024