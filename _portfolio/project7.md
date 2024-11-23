---
title: Homework n°8
subtitle: Shannon Entropy,other diversity measures of distributions,primitive root and Caesar cypher
image: /assets/img/portfolio/Caesarcypher.jpg
alt: SDE

caption:
  title: Homework 8
  subtitle: Caesar cypher and Shannon Entropy
  thumbnail: /assets/img/portfolio/Caesarcypher.jpg
---

# Shannon Entropy and Other Diversity Measures

## **Shannon Entropy**

Shannon entropy is a measure of uncertainty or diversity in a probability distribution. For a discrete random variable $$ X $$ with $$ n $$ possible outcomes $$ x_1, x_2, \ldots, x_n $$, each having probabilities $$ p(x_1), p(x_2), \ldots, p(x_n) $$, the entropy $$ H(X) $$ is defined as:

$$
H(X) = -\sum_{i=1}^n p(x_i) \log_b p(x_i)
$$

**Base $$ b $$:** The logarithm's base $$ b $$ determines the unit of measurement (e.g., base 2 for bits, base $$ e $$ for nats).  
**Interpretation:** Higher entropy indicates greater uncertainty or diversity in the distribution.

### Other Diversity Measures

**Simpson's Index**:

 Measures the probability that two randomly selected items belong to the same category.
   $$
   D = \sum_{i=1}^n p(x_i)^2
   $$
   - Often used in ecological studies to measure species dominance.

**Gini-Simpson Index (Complement of Simpson's)**:

   $$
   1 - D = 1 - \sum_{i=1}^n p(x_i)^2
   $$

Interpreted as the probability that two randomly selected items belong to different categories.

**Rényi Entropy**: Generalization of Shannon entropy, defined as:

   $$
   H_\alpha(X) = \frac{1}{1 - \alpha} \log \left( \sum_{i=1}^n p(x_i)^\alpha \right)
   $$

where $$ \alpha > 0 $$ and $$ \alpha \neq 1 $$.
Reduces to Shannon entropy as $$ \alpha \to 1 $$.

# Primitive Root

### Definition

A **primitive root modulo $$ p $$**, where $$ p $$ is a prime number, is an integer $$ g $$ such that its powers generate all the integers $$ 1, 2, \ldots, p-1 $$ modulo $$ p $$. Formally:

Given a prime $$ p $$, $$ g $$ is a primitive root modulo $$ p $$ if for every integer $$ a $$ coprime to $$ p $$ ($$ \gcd(a, p) = 1 $$), there exists an integer $$ k $$ such that:

$$
g^k \equiv a \pmod{p}
$$

Equivalently, $$ g $$ is a generator of the **multiplicative group** of integers modulo $$ p $$, denoted $$ (\mathbb{Z}/p\mathbb{Z})^* $$.

### Properties

The order of $$ g $$ modulo $$ p $$ (the smallest $$ k > 0 $$ such that $$ g^k \equiv 1 \pmod{p} $$) is $$ p-1 $$.

If $$ g $$ is a primitive root modulo $$ p $$, then the sequence $$ g^1, g^2, \ldots, g^{p-1} \mod p $$ is a permutation of $$ 1, 2, \ldots, p-1 $$.

### Finding Primitive Roots

To find a primitive root $$ g $$ modulo $$ p $$:

Verify $$ g^{(p-1)/q} \not\equiv 1 \pmod{p} $$ for all prime divisors $$ q $$ of $$ p-1 $$. If true, $$ g $$ is a primitive root.

### Example

For $$ p = 7 $$, the numbers coprime to $$ 7 $$ are $$ 1, 2, 3, 4, 5, 6 $$. Testing, $$ g = 3 $$ is a primitive root since:

$$
3^1 \equiv 3, \; 3^2 \equiv 9 \equiv 2, \; 3^3 \equiv 27 \equiv 6, \; 3^4 \equiv 18 \equiv 4, \; 3^5 \equiv 12 \equiv 5, \; 3^6 \equiv 1 \pmod{7}.
$$

# Practical Part

![Caesar cypher](/assets/img/portfolio/Caesarcypher7.jpg)

## Findings from the Exercise

###  Letter Frequency Distribution (Input Text)

The **blue histogram** represents the frequency distribution of letters in the plaintext.  
It aligns with typical English letter frequency:

**E** is the most frequent letter (approximately 12.7%), followed by **T**, **A**, and **O**.  
Rare letters include **Z**, **X**, and **Q**.  
This demonstrates the predictable nature of letter usage in English.  

### Letter Frequency Distribution (Encrypted Text)

The **red histogram** represents the letter frequency in the encrypted (ciphertext) text.  
The ciphertext preserves the same statistical patterns but shifts the peaks due to the Caesar cipher's rotation.  
This observation highlights that the Caesar cipher does not obscure frequency characteristics, making it vulnerable to **frequency analysis**.

## How Statistical Analysis Enhances Understanding of Cryptography

### Revealing Weaknesses in Ciphers

Statistical tools such as histograms expose the weaknesses of simple substitution ciphers like Caesar.  
For example:

The frequency of letters in the ciphertext correlates with the plaintext.  
This allows cryptanalysts to deduce the shift by mapping common letters (e.g., **E** in English).

### Decoding Encrypted Messages

Frequency analysis and entropy calculations make breaking weak encryption methods possible.  
As demonstrated, even a basic understanding of letter patterns enables the deciphering of messages encrypted with the Caesar cipher.


This exercise highlights the power of statistical analysis in uncovering patterns in encrypted messages, showcasing why modern cryptography relies on randomness and complexity to ensure security. Developing these analytical skills is vital for anyone in the field of cybersecurity in order to:

**Detecting Weak Cryptography**

Statistical analysis helps identify insecure systems using weak encryption schemes, like substitution ciphers.

**Designing Secure Algorithms**

Understanding how patterns compromise encryption motivates the adoption of modern, secure cryptographic algorithms (e.g., AES, RSA).  
Modern algorithms avoid patterns and use randomness for security.

**Incident Response**

During a breach, analysts may need to break weak encryption to assess the attacker’s intentions or reverse-engineer malicious code.

**Strengthening Security Practices**

Cryptographic analysis informs secure implementations by discouraging outdated and predictable methods.




[Homework8.rar](https://github.com/GabrielePapalino/statistics/raw/refs/heads/main/Homework%208.rar)


{:.list-inline}

- Date: 27 November 2024