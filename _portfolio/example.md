---
caption: #what displays in the portfolio grid:
  title: Homework 1
  subtitle: Statistic's 1st homework
  thumbnail: https://place-hold.it/400x300
  
#what displays when the item is clicked:
title: Homework n°1
subtitle: Homework based on Statistical Units and Distributions.
image: https://place-hold.it/400x300 #main image, can be a link or a file in assets/img/portfolio
alt: image alt text

---
# **Base Notions in Statistics: Population, Statistical Units, and Distribution**
Statistics is the study of data and the techniques used to gather, analyze, interpret, and present it. At its core, it involves three fundamental concepts: population, statistical units, and distribution.

### **Population**
In statistics, the term population refers to the complete set of entities or observations that are of interest in a particular study. These entities could be individuals, objects, events, or data points. For example, in a medical study about diabetes, the population could be all individuals diagnosed with diabetes in a particular country.

**Finite Population**: A population with a limited number of observations. For example, all students in a university.

**Infinite Population**: A population that theoretically contains an infinite number of elements. An example would be measuring the height of all humans that will ever exist.
The population is what we aim to draw conclusions about, but often it's too large to observe entirely, so we use a sample, which is a subset of the population, to infer results about the whole.

### **Statistical Units**
A statistical unit is the individual entity on which data is collected. These could be people, companies, products, or measurements. For example, if you're conducting a survey on household income, a statistical unit would be each household surveyed.

Each statistical unit must be:

Well-defined, meaning that there should be no ambiguity in what constitutes a unit.
Comparable, so that the same kind of data can be gathered for every unit.
### **Distribution**
A distribution describes how values of a variable are spread or dispersed within a population or sample. It indicates the frequency with which different outcomes or measurements occur. Distributions help statisticians understand patterns in data and are crucial in probability theory.

**Probability Distribution**: Shows the probability of different outcomes. For example, a normal distribution (also called a Gaussian distribution) is one of the most common in statistics and represents many real-world variables like test scores or heights of people.

**Empirical Distribution**: Based on observed data rather than a theoretical model. The histogram of observed values in a sample is an example of an empirical distribution.
Distributions can also be described by characteristics such as:

 Mean (average)  
 Variance (spread)  
 Skewness (asymmetry)  
 Kurtosis (peakedness)  

## **The Notion of Average: Arithmetic Mean and Its Computational Problems**
### **The Notion of Average**
The average is a central tendency measure that summarizes a set of data by providing a single value representative of the dataset. The most common form is the arithmetic mean (often simply called the mean).

The arithmetic mean is calculated as:  

<!--![Mean](/gabrielepapalino.github.io/assets/img/formulas/mean.jpg)-->

Mean = $$\frac{x_{1} + x_{2} + \cdots + x_{n}}{n}$$

​where $$x_1, x_2, \dots, x_n$$ are the data points, and $$n$$ is the number of observations.

Though averages are widely used, the computation of averages in practice can lead to problems, especially when floating-point numbers are involved.

### **Computational Problems with Floating-Point Representation**
Computers store and process numbers using a floating-point representation, which is an approximation of real numbers. While floating-point arithmetic allows efficient computation with very large or very small numbers, it introduces errors due to the finite precision with which numbers can be stored.

**Floating-Point Error**
Floating-point numbers have limited precision, which means that some numbers cannot be represented exactly. For example, the number 1/3 cannot be precisely represented in decimal form, and similarly, many numbers in binary floating-point representation lose precision.

**Catastrophic Cancellation**
Catastrophic cancellation occurs when subtracting two nearly equal numbers results in a significant loss of precision. This happens because the significant digits in the two numbers cancel out, leaving behind less significant digits that can be heavily affected by floating-point inaccuracies.

For example, if you calculate:

$$x=1.00000001 − 1.00000000$$  
in a system with limited precision, you might end up with a result that is inaccurate or even zero.

This issue becomes problematic when summing large numbers of values or when averaging very large and very small numbers in the same dataset, as errors accumulate.

### **Recursive Formula and the Knuth Algorithm**
The straightforward summation of values to compute an average, especially when dealing with floating-point numbers, can lead to substantial rounding errors. To mitigate this, better algorithms have been developed, such as Donald Knuth's method for calculating running averages.

Recursive Formula for Mean
The recursive formula allows for updating the mean as new data points arrive. Given a new data point 
𝑥
𝑛
+
1
x 
n+1
​
 , and an existing mean 
𝜇
𝑛
μ 
n
​
  of 
𝑛
n data points, the new mean 
𝜇
𝑛
+
1
μ 
n+1
​
  can be computed as:

𝜇
𝑛
+
1
=
𝜇
𝑛
+
𝑥
𝑛
+
1
−
𝜇
𝑛
𝑛
+
1
μ 
n+1
​
 =μ 
n
​
 + 
n+1
x 
n+1
​
 −μ 
n
​
 
​
 
This formula avoids recalculating the mean from scratch each time a new data point is added and is useful for large datasets.

**Knuth’s Algorithm (Kahan Summation)**
Knuth and others developed improved algorithms to minimize the errors that arise from floating-point operations. The Kahan summation algorithm (also known as compensated summation) is one such technique. It keeps track of a small error term that adjusts for floating-point errors accumulated during the summation process.

The Kahan summation algorithm proceeds as follows:

Initialize the sum and a compensation variable, which starts at 0.
For each number in the dataset, add it to the sum, but adjust it by the compensation term to minimize error.
Update the compensation to reflect the lost precision in the previous step.
This method ensures that the final sum is more accurate by accounting for rounding errors incrementally, especially in large datasets where such errors can accumulate significantly.


{:.list-inline} 
- Date: 9th of October 2024


