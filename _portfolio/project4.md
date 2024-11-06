---
title: Homework n°5
subtitle: Cauchy-Schwarz inequality, concepts of independence and uncorrelation and E-M simulator enhancement
image: /assets/img/portfolio/home.jpg
alt: SDE

caption:
  title: Homework 5
  subtitle: Cauchy-Schwarz inequality
  thumbnail: /assets/img/portfolio/home.jpg
---

# **Cauchy-Schwarz inequality**

Define the random variable $$W=(X−\alpha Y)^2$$. Clearly, $$W$$ is a nonnegative random variable for any value of $$\alpha \in R$$
. Thus, we obtain:

$$0 \leq E[W]  = E[(X - \alpha Y)^2]$$  

$$= E[X^2 - 2\alpha XY + \alpha^2 Y^2]$$ 

$$= E[X^2] - 2\alpha E[XY] + \alpha^2 E[Y^2].$$

So, if we let $$f(\alpha)=E[X^2]−2\alpha E[XY]+\alpha^2 E[Y^2]$$, then we know that $$f(\alpha) \geq 0$$, for all $$\alpha \in R$$. Moreover, if $$f(\alpha)=0$$ for some $$\alpha$$, then we have $$EW=E(X−\alpha Y)^2=0$$, which essentially means $$X=\alpha Y$$ with probability one. To prove the Cauchy-Schwarz inequality, choose $$\alpha=\frac{EXY}{EY^2}$$. We obtain:


$$0\leq E[X^2]−2\alpha E[XY]+\alpha^2 E[Y^2]$$

$$=E[X^2]−2\frac{EXY}{EY^2} E[XY]+\frac{(EXY)^2}{(EY^2)^2}E[Y^2]$$

$$=E[X^2]−\frac{(E[XY])^2}{EY^2}$$

Thus, we conclude

$$(E[XY])^2 \leq E[X^2] E[Y^2]$$

which implies

$$|EXY| \leq \sqrt{E[X^2] E[Y^2]}$$  

Also, if 

$$|EXY|=\sqrt{E[X^2] E[Y^2]}$$

we conclude that $$f(\frac{EXY}{EY^2})=0$$, which implies $$X=\frac{EXY}{EY^2}Y$$ with probability one.

# **Concepts of Independence and Uncorrelation**

### **Independence**

Two random variables $$X$$ and $$Y$$ are said to be independent if the joint probability distribution can be expressed as the product of their marginal distributions:

$$P(X \cap Y) = P(X) P(Y)$$

Independence implies that knowing the value of one variable does not provide any information about the other.

### **Uncorrelation**

Two random variables $$X$$ and $$Y$$ are uncorrelated if their covariance is zero:

$$\operatorname{Cov}(X, Y) = E[(X - E[X])(Y - E[Y])] = 0$$

This means that there is no linear relationship between $$X$$ and $$Y$$.

**More in deep**

Covariance is a measure of the linear relationship between two variables. It is zero for uncorrelated variables.

Correlation Coefficient $$r$$ is a normalized version of covariance defined as:

$$r(X, Y) = \frac{\operatorname{Cov}(X, Y)}{\sigma_X \sigma_Y}$$
 
where $$\sigma_X$$ and  $$\sigma_Y$$ are the standard deviations of $$X$$ and $$Y$$.

**Independence vs Uncorrelation:**


Independence is stronger than uncorrelation:

Independence implies uncorrelation  
Uncorrelation does not imply independence

In conclusion, while uncorrelation only measures the absence of linear dependence, independence indicates a complete lack of any form of dependence, including non-linear

# **Extra Exercise : Deriving Regression Coefficients and R^2**

Consider a set of $$n$$ data points $$(x_i, y_i)$$, where $$i = 1, 2, \dots, n$$. We want to find the coefficients $$a$$ and $$b$$ for the two regression lines:


Regression of $$y$$ on $$x$$: $$y = a + bx$$  
Regression of $$x$$ on $$y$$: $$x = a' + b'y$$


Using the principle of least squares, we can derive the coefficients as follows:

**Regression of $$y$$ on $$x$$**

The goal is to minimize the sum of squared vertical distances between the data points and the regression line:

$$\sum_{i=1}^n (y_i - (a + bx_i))^2$$


Taking the partial derivatives with respect to $$a$$ and $$b$$ and setting them equal to 0, we get:

$$\frac{\partial}{\partial a} \sum_{i=1}^n (y_i - (a + bx_i))^2 = 0$$  
$$\frac{\partial}{\partial b} \sum_{i=1}^n (y_i - (a + bx_i))^2 = 0$$


Solving these equations, we obtain the coefficients:

$$a = \bar{y} - b\bar{x}$$  
$$b = \frac{\sum_{i=1}^n (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^n (x_i - \bar{x})^2}$$

**Regression of $$x$$ on $$y$$**

Similarly, we can find the coefficients for the regression of $$x$$ on $$y$$:

$$a' = \bar{x} - b'\bar{y}$$  
$$b' = \frac{\sum_{i=1}^n (y_i - \bar{y})(x_i - \bar{x})}{\sum_{i=1}^n (y_i - \bar{y})^2}$$

**Relationship with $$R^2$$**

The coefficient of determination, $$R^2$$, is defined as the proportion of the variance in the dependent variable that is predictable from the independent variable. It can be calculated as:

$$R^2 = \frac{\sum_{i=1}^n (\hat{y}_i - \bar{y})^2}{\sum_{i=1}^n (y_i - \bar{y})^2} = \frac{b^2 \sum_{i=1}^n (x_i - \bar{x})^2}{\sum_{i=1}^n (y_i - \bar{y})^2}$$


where $$\hat{y}_i = a + bx_i$$ is the predicted value of $$y_i$$.

The relationship between the regression coefficients and $$R^2$$ is:

$$R^2 = \left(\frac{b\sigma_x}{\sigma_y}\right)^2 = \left(\frac{b'}{\sigma_y/\sigma_x}\right)^2$$


where $$\sigma_x$$ and $$\sigma_y$$ are the standard deviations of $$x$$ and $$y$$, respectively.


# **Practice**

### **E-M simulator Enhancement**

![Interface](/assets/img/portfolio/home.jpg)

This window represent an interface to access different functionalities or tasks, with each button leading to a different stochastic differential equation developed step by step during the course

![Multi Simulation](/assets/img/portfolio/multisimulation.jpg)

Projecting the interface in this way allows us to compare different stochastic equations by providing a clear visual of multiple simulation parameters and outcomes side-by-side

**Visual Comparison of Results**

Each form has a graphical area where simulation results are plotted. In both forms:

The colored lines represent individual stochastic trajectories, showing the progression of the simulation over time.  
The histogram on the right shows the distribution of outcomes, allowing for an immediate visual comparison of how variable or stable the results are for each simulation.

By allowing both forms to run independently and simultaneously, the interface enables the user to view and compare multiple scenarios in real-time without needing to switch between screens. This setup is useful when comparing outcomes under different stochastic equations, as it makes differences and similarities readily apparent.


{:.list-inline}

- Date: 6 November 2024