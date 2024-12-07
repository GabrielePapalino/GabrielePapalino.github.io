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

# Optional

# Analysis of Modular Exponentiation Distributions and Entropy

![Optional](/assets/img/portfolio/7opt7.jpg)

### Case A: Modular Exponentiation for $$ n = 19 $$

### Observations

 **Uniformity of Distributions**:

For $$ g = 2, 3, 10, $$ and $$ 17 $$, the distributions appear nearly uniform.  
Each residue mod $$ n $$ is approximately equally likely, with probabilities between 4% and 7%.

**Entropy**:

Entropy values are consistently high ($$ \approx 4.15 $$–$$ 4.16 $$).  
High entropy reflects a greater level of randomness and unpredictability in the outputs.

### Cryptographic Implications

**Uniformity and Randomness**:

Uniform distributions ensure all residues mod $$ n $$ are equally probable. This prevents patterns that could be exploited by attackers.  
Randomness in modular exponentiation makes solving cryptographic problems (like the discrete logarithm problem) computationally infeasible.

**Higher Entropy**:

High entropy indicates more diverse outputs, making predictions significantly harder for attackers.  
Entropy is a key measure of security: greater entropy translates to stronger cryptographic properties.

**Applications**:

These properties make Case A suitable for:

**Diffie-Hellman Key Exchange**: Randomness ensures secure key agreement.  
**ElGamal Encryption**: Uniformity protects message confidentiality.

### Why $$ g = $$ 2, 3, 10, 17 $$ $$ Was Chosen

These values likely correspond to generators of cyclic groups or produce high-entropy distributions.  
The choice of $$ g $$ maximizes uniformity across residue distributions, minimizing bias and ensuring robustness against attacks.


## Case B: Modular Exponentiation for $$ n = 15 $$

### Observations

**Non-Uniform Distributions**:

For $$ g = 3, 6, 9, $$ and $$ 12 $$, the distributions show significant bias:

$$ g = 6 $$: All outputs collapse into a single residue (100%), resulting in zero entropy.  
$$ g = 3 $$ and $$ g = 12 $$: Residues have unequal probabilities, with some more frequent than others.

**Entropy**:

Entropy values are much lower ($$ 0.00 $$–$$ 2.00 $$), reflecting reduced diversity and predictability.

### Cryptographic Implications

**Predictability**:

Low entropy makes it easier for attackers to predict outcomes of modular exponentiation.  
For example, with $$ g = 6 $$, the result is entirely deterministic, eliminating any randomness.

 **Bias in Results**:

For $$ g = 3 $$ and $$ g = 12 $$, certain residues occur more frequently than others. This bias could lead to cryptographic vulnerabilities by exposing patterns.

**Unsuitability for Cryptography**:

Case B’s low entropy and biased distributions make it unsuitable for cryptographic protocols:

Weak randomness compromises the security of key exchanges.  
Biased outputs make attacks like brute force easier.


## Key Differences Between Case A and Case B

| **Property**          | **Case A ($$ n = 19 $$)**               | **Case B ($$ n = 15 $$)**          |
|-----------------------|-----------------------------------------|------------------------------------|
| **Uniformity**        | High uniformity across residues         | Biased or deterministic outputs   |
| **Entropy**           | High ($$ \approx 4.16 $$)               | Low ($$ 0.00 $$–$$ 2.00 $$)       |
| **Cryptographic Suitability** | Strong cryptographic properties         | Weak, vulnerable to attacks       |
| **Predictability**    | Low (high randomness)                   | High (patterns and biases)        |
| **Example Generators**| $$ g = 2, 3, 10, 17 $$                  | $$ g = 3, 6, 9, 12 $$             |



## Errors and Observations in the Exercise

**Choice of $$ g $$ in Case B**:

The values $$ g = 6 $$ and $$ g = 9 $$ produce deterministic or highly biased distributions.  
These choices are poorly suited for cryptographic applications, as they fail to ensure randomness and uniformity.

**Entropy Calculations**:

The entropy value for $$ g = 3 $$ in Case B is reported as $$ 2.00 $$. However, the visual distribution suggests that this may be an overestimate, given the observed bias.

**Missing Context**:

The exercise does not specify the intended cryptographic application (e.g., Diffie-Hellman, ElGamal). This information would clarify the significance of uniformity and entropy in the analysis.

**Generator Selection for Case A**:

The selection of $$ g = $$ 2, 3, 10, 17 $$ $$ seems aimed at maximizing entropy. However, the reasoning (e.g., their role as primitive roots or cyclic group generators) could be better explained.

## Conclusion

**Case A** demonstrates strong cryptographic properties, such as high entropy and uniform distributions. These characteristics make it well-suited for secure applications.  
**Case B**, on the other hand, highlights vulnerabilities caused by low entropy and biased distributions, making it unsuitable for cryptographic use.  

**Key Implications**:

High entropy and uniformity are essential for ensuring the security of cryptographic protocols.
Poor parameter choices (as seen in Case B) can introduce vulnerabilities, such as predictability and bias, which attackers can exploit.

**Recommendations**:

Carefully select parameters ($$ g $$ and $$ n $$) to maximize entropy and randomness.  
Verify the suitability of modular exponentiation properties for the intended cryptographic application.




[Homework7.rar](https://github.com/GabrielePapalino/statistics/raw/refs/heads/main/Homework%207.rar)


{:.list-inline}

- Date: 20 November 2024