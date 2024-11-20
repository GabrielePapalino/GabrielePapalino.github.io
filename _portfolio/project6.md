---
title: Homework n°7
subtitle: Distribution of the sampling average
image: /assets/img/portfolio/meanofmean.jpg
alt: SDE

caption:
  title: Homework 7
  subtitle: Distribution of the sampling average
  thumbnail: /assets/img/portfolio/meanofmean.jpg
---

# **The average of the distribution of the averages of the samples**

**Observed Relationship Between Parent and Sample Mean Distributions**

This simulation demonstrates the **Central Limit Theorem (CLT)** by comparing the theoretical distribution (parent distribution) with the sampling distribution of the sample means.

### **Observed Relationships**

**Mean Comparison**

**Theoretical Distribution (Parent)**: The mean of the theoretical distribution is shown as 7.26.  
**Sample Means Distribution**: The mean of the sample means is approximately 1.74, which seems significantly different. This could arise because the theoretical and sample means may represent different measures, or the scale used in sampling could differ.

**Variance Comparison**

**Theoretical Distribution (Parent)**: The variance is relatively high (32.45), indicating a wide spread of the parent population.  
**Sample Means Distribution**: The variance is much smaller (0.02), demonstrating that the distribution of sample means is less spread out than the parent distribution. This aligns with the CLT, which states that as sample size increases, the variance of the sample means decreases according to:

$$\text{Variance of sample means} = \frac{\sigma^2}{n}$$

where $$\sigma^2$$ is the parent variance and $$n$$ is the sample size.

**Key Insights**

The **distribution of sample means** is narrower (less variance) than the **theoretical distribution**, showcasing how averaging reduces variability.  
While the parent distribution could be non-normal (as seen in the blue histogram), the distribution of sample means (green histogram) tends toward a normal shape, which is a hallmark of the Central Limit Theorem.  
These results emphasize how repeated sampling from a population yields sample means that are more stable and closer to the true population mean, despite variability in the parent population.



[Homework7.rar](https://github.com/GabrielePapalino/statistics/raw/refs/heads/main/Homework%207.rar)


{:.list-inline}

- Date: 20 November 2024