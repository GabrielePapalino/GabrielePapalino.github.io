---
title: Homework n°10
subtitle: Lebesgue–Stieltjes integration and applications to Probability theory
image: /assets/img/portfolio/integralesquare.jpg
alt: SDE

caption:
  title: Homework 10
  subtitle: Lebesgue–Stieltjes integration
  thumbnail: /assets/img/portfolio/integralesquare.jpg
---

# Lebesgue–Stieltjes Integration

## General Idea

Lebesgue–Stieltjes integration generalizes both **Riemann–Stieltjes integration** and **Lebesgue integration**, allowing integration with respect to functions that may have discontinuities or non-uniform behavior. This makes it ideal for modeling phenomena with irregular distributions or jumps.

### Core Concept

The **Lebesgue–Stieltjes integral** of a function $$ f $$ with respect to a function $$ g $$ on an interval $$ [a, b] $$ is expressed as:

$$
\int_a^b f(x) \, dg(x).
$$

Where:

$$ f(x) $$: The integrand, typically a measurable function.  
$$ g(x) $$: The integrator, a function of bounded variation.

Instead of integrating $$ f(x) $$ directly with respect to $$ x $$, the integration is performed relative to the changes in $$ g(x) $$, making $$ g $$ a "weighting" function.

## Relation to Measure Theory

In measure-theoretic terms, the function $$ g(x) $$ induces a measure $$ \mu_g $$, defined as:

$$
\mu_g([a, b)) = g(b) - g(a).
$$

The Lebesgue–Stieltjes integral is then equivalent to the Lebesgue integral of $$ f $$ with respect to the measure $$ \mu_g $$:

$$
\int_a^b f(x) \, dg(x) = \int_a^b f(x) \, d\mu_g(x).
$$

This connects classical integration methods with modern measure theory and forms the basis for applications in probability and analysis.


## Applications to Probability Theory

### Cumulative Distribution Functions (CDFs)
The **CDF** of a random variable $$ X $$, $$ F_X(x) = P(X \leq x) $$, is a monotonically non-decreasing function. The Lebesgue–Stieltjes integral is used to compute expectations with respect to $$ F_X $$:

$$
\mathbb{E}[h(X)] = \int_{-\infty}^\infty h(x) \, dF_X(x).
$$

Here, $$ F_X $$ acts as the integrator, and $$ h(x) $$ is the function being averaged.

### Discrete and Continuous Distributions
The Lebesgue–Stieltjes framework accommodates both discrete and continuous distributions:

For continuous distributions, $$ F_X $$ is absolutely continuous, and $$ dF_X(x) = f_X(x)dx $$, where $$ f_X $$ is the probability density function (PDF).

For discrete distributions, $$ F_X $$ has jumps at points of the support, and $$ dF_X(x) $$ corresponds to the probability masses.

### Expected Value of a Random Variable
For a random variable $$ X $$ with a given CDF $$ F_X $$, the expectation can be expressed as:

$$
\mathbb{E}[X] = \int_{-\infty}^\infty x \, dF_X(x).
$$

### Probability Measures

The function $$ g(x) = F_X(x) $$ defines a probability measure $$ \mu $$, turning the integral into an expectation. This is foundational in stochastic processes and statistical analysis.

## Applications to Measure Theory

### Induced Measures
Any function of bounded variation $$ g(x) $$ induces a measure $$ \mu_g $$, allowing the use of Lebesgue integration in cases where $$ g(x) $$ may have discontinuities.

### Generalization of Riemann–Stieltjes
The Lebesgue–Stieltjes integral generalizes classical Riemann–Stieltjes integration by allowing integration with respect to measures that may include singular components, such as Dirac measures.

### Decomposition of Measures

The **Lebesgue decomposition theorem** states that any measure $$ \mu $$ can be decomposed into three parts:

An **absolutely continuous** part with respect to the Lebesgue measure.  
A **discrete** part, associated with point masses.  
A **singular** part, such as singularly continuous measures (e.g., Cantor's function).

Lebesgue–Stieltjes integration handles all these cases seamlessly.

### Functional Analysis

In spectral theory, Lebesgue–Stieltjes integration is used to represent measures associated with spectral distributions of self-adjoint operators in Hilbert spaces.

# Practical Part

# Comparison of the Results in the Image

![x^2](/assets/img/portfolio/integralesquare7.jpg)

**Riemann Integral Result:**

41.66666

**Lebesgue Integral Result:**

 41.60419

## Why Are the Results Close but Different?

The function $$ f(x) = x^2 $$ is continuous and smooth over the interval $$[0, 5]$$. For such functions:

**Both integrals converge** to nearly the same value as the number of subdivisions ($$n$$) increases.  
The **slight difference** arises from the numerical approximation methods used in the implementation.   
The Lebesgue integral relies on sorting and grouping values, which may introduce small errors when approximated numerically.  
These differences become **negligible as the precision** of the calculation increases (e.g., using more subintervals or more accurate computational methods).

## Strengths and Use Cases

### Riemann Integral

#### Strengths:

Straightforward and **intuitive** for simple, continuous functions.   
Easy to visualize as the **sum of rectangles**.

#### Weaknesses:

**Fails for functions** with many discontinuities (e.g., functions with a dense set of jumps).  
Cannot handle functions defined on **complex sets**, such as subsets of the real line with nontrivial structures.

### Lebesgue Integral

#### Strengths:

Handles a **broader class of functions**, including those that are discontinuous almost everywhere (e.g., characteristic functions, Dirichlet functions).  
Provides a **more general framework** for integration in measure theory.  
Better suited for **convergence theorems**, such as the Dominated Convergence Theorem.

#### Weaknesses:

More **abstract** and harder to compute numerically.  
Visualization is **less intuitive** than Riemann sums.

## Conclusion

For the function $$f(x) = x^2$$, which is simple and well-behaved, the **Riemann** and **Lebesgue integrals** yield nearly identical results, differing slightly due to numerical methods. 

However, the **Lebesgue integral's versatility** makes it the preferred approach in advanced mathematical analysis and for functions with more complex behaviors. For example:

The characteristic function of rationals in $$[0, 1]$$ (1 for rational $$x$$, 0 otherwise) has no Riemann integral but a Lebesgue integral of 0 because the rationals have zero measure.



[Homework10.rar](https://github.com/GabrielePapalino/statistics/raw/refs/heads/main/Homework%2010.rar)

{:.list-inline}

- Date:  December 2024