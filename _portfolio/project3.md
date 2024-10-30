---
title: Homework n°4
subtitle: Statistical independence and SDE simulator used to represent the scaling limit of the random Walk
image: /assets/img/portfolio/Wiener.jpg
alt: SDE

caption:
  title: Homework 4
  subtitle: Continuous time process simulator
  thumbnail: /assets/img/portfolio/Wiener.jpg
---

# **Statistical Independence**

Statistical independence is a fundamental concept in probability theory, describing a situation where the occurrence of one event does not affect the occurrence of another. Imagine flipping a coin twice. The outcome of the first flip (heads or tails) doesn't influence the outcome of the second flip. These events are considered independent. 

Imagine flipping a coin twice. The outcome of the first flip (heads or tails) doesn't influence the outcome of the second flip. These events are considered independent. Two events $$A$$ and $$B$$ are said to be independent if the probability of their intersection is equal to the product of their individual probabilities:

$$P(A \cap B) = P(A) \cdot P(B)$$

Key Points About Independence:

Events are independent if knowledge of one event doesn't affect the probability of the other

Independent events may still occur together, but their co-occurrence is purely random

Independence is symmetric: if A is independent of B, then B is independent of A


Another way to express independence is through conditional probability. If $$A$$ and $$B$$ are independent, then:

$$P(A \mid B) = P(A)$$

And similarly:

$$P(B \mid A) = P(B)$$

For dependent events, the conditional probability would differ from the unconditional probability, indicating that the occurrence of one event gives information about the other.

From a distributional perspective, when two random variables are independent, their marginal distributions do not affect each other. This means that to find their joint distribution, you can simply multiply their marginal distributions.

# **Practical Part**

The simulation of a Wiener process shown in the image is significant because it illustrates principles like Donsker’s Invariance Principle (also known as the Functional Central Limit Theorem). This theorem establishes a crucial link between discrete random processes and continuous ones, specifically showing that certain types of discrete processes converge to the Wiener process as the number of steps goes to infinity.


![Wiener Process Code](/assets/img/portfolio/wienercode.jpg)

This code essentially simulates a two-dimensional random walk with vertical movement based on a probability threshold. Each "attacker" has a unique path composed of up and down steps that are scaled by sqrt_dt, and the horizontal movement advances consistently at each time step where:

*dt*: This is the time interval, calculated as 1 / servers. It represents the small increment in time for each step.
*sqrt_dt*: The square root of dt, which is used to scale the vertical step size. This scaling is typical in Wiener processes to ensure variance increases linearly with time.

![Wiener Process](/assets/img/portfolio/Wiener7.jpg)

The image shows a simulation of a Wiener process, also known as Brownian motion, with specific parameters.this type of simulation can be used to study random phenomena, such as the diffusion of particles in a fluid or the random movements of individuals within a network, where the outcome is based on probabilistic interactions.


**More in deep**

Donsker's Invariance Principle states that the rescaled sum of i.i.d. random variables with finite variance converges in distribution to a Wiener process (or standard Brownian motion) as the number of steps grows. In essence, the theorem generalizes the Central Limit Theorem to the level of functions or paths rather than single values.

The theorem allows us to approximate continuous Brownian motion with a large number of discrete random walks. In practical terms, it means that processes like stock prices, particle diffusion, and network dynamics can be studied using discrete models, knowing they will behave like continuous Wiener processes as the sample size becomes large.

[Homework4.rar](https://github.com/GabrielePapalino/statistics/raw/refs/heads/main/Homework%204.rar)

{:.list-inline}

- Date: 30 October 2024