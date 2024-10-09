---
caption: #what displays in the portfolio grid:
  title: Homework 1
  subtitle: Statistic's 1st homework
  thumbnail: /assets/img/portfolio/risultato.jpg
  
#what displays when the item is clicked:
title: Homework n°1
subtitle: Homework based on Statistical Units and Distributions.
image: /assets/img/portfolio/risultato.jpg #main image, can be a link or a file in assets/img/portfolio
alt: Form

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

$$\bar{x}\frac{x_{1} + x_{2} + \cdots + x_{n}}{n}$$

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
The recursive formula allows for updating the mean as new data points arrive. Given a new data point $$x_{n+1}$$, and an existing mean $$	\mu_n$$ of $$n$$ data points, the new mean $$	\mu_{n+1}$$ can be computed as:
​

$$	\mu_{n+1}= \mu_n + \frac{x_{n+1}-\mu_n}{n + 1}$$
 
This formula avoids recalculating the mean from scratch each time a new data point is added and is useful for large datasets.

**Knuth’s Algorithm (Kahan Summation)**
Knuth and others developed improved algorithms to minimize the errors that arise from floating-point operations. The Kahan summation algorithm (also known as compensated summation) is one such technique. It keeps track of a small error term that adjusts for floating-point errors accumulated during the summation process.

The Kahan summation algorithm proceeds as follows:

Initialize the sum and a compensation variable, which starts at 0.  
For each number in the dataset, add it to the sum, but adjust it by the compensation term to minimize error.  
Update the compensation to reflect the lost precision in the previous step.  

This method ensures that the final sum is more accurate by accounting for rounding errors incrementally, especially in large datasets where such errors can accumulate significantly.

# **Practical Part**

![simulationStructure](/assets/img/portfolio/simulation.jpg)

**Graph Setup:**

It initializes a Graphics object called graph for drawing on the *pictureGraph* control and clears it with a white background. A black pen (*pen*) is created for drawing the graph.

**Graph Partitioning:**

The code retrieves values from text fields (*textAttackers*, *textServers*, and *textProbability*) and parses them into integers (*attackers*, *servers*) and a float (*probability*).
It calculates horizontal and vertical scaling factors based on the size of the graph area (*pictureGraph.Width* and *Height*) and the number of servers, which determine how the graph is partitioned.

**Histogram Setup:**

A Graphics object called histogram is created for the *pictureHistogram* control, which is also cleared with a white background, likely to represent the histogram.

**Functions Call:**

A function *DrawGraph* is called with the *graph*, *attackers*, *servers*, *probability*, and the calculated horizontal and vertical factors. This function likely draws a representation of the attack simulation.
Afterward, the function *DrawHistogram* is invoked, likely to visualize a histogram using the scoreboard data.

![drawGraph](/assets/img/portfolio/graph.jpg)

**Array for Vulnerabilities:**

An integer array vulnerabilities is created to track which servers have been attacked, with each element representing a server.

**Random Initialization:**

A Random object is initialized to randomize the attackers’ behavior.

**Attackers Iteration (Outer Loop):**

The outer for loop runs through all attackers (attackers variable), differentiating them by setting a random pen color (pen.Color). A Point object (point) is initialized at the bottom of the graph to represent where each attacker starts. The variable score is initialized to track which server the attacker reaches.

**Servers Iteration (Inner Loop):**

The inner loop iterates through all the servers (servers variable), representing the attacker's path across the servers.

**Direction of Movement:**

For each server, a random decision determines if the attacker will "move up" or "move right."
If the randomly generated number is less than the probability, the attacker moves upward (up point) vertically by subtracting vertical from the current Y position. A line is drawn from the current position to this new upward point.
Otherwise, the attacker moves horizontally (right point) by adding horizontal to the X position. A line is drawn to the new rightward position.

**Marking Vulnerabilities:**

Whenever an attacker reaches a new server (based on the score), the corresponding element in the vulnerabilities array is incremented by 1, signifying an attack on that server.

**Return Value:**

The method returns the vulnerabilities array, which contains information on how many times each server was attacked.

![drawGraph](/assets/img/portfolio/histogram.jpg)

**Draw Rectangle for Each Server:**

For each server (*i*), if it has been attacked at least once (i.e., *scoreboard[i] != 0*), a rectangle is drawn to represent the number of attacks on that server.
The height of the rectangle is calculated by subtracting a proportion of the server's attack score from the total height of the *pictureHistogram* control. The more attacks a server has, the higher the rectangle extends from the bottom of the histogram.
The width of the rectangle is determined by dividing the total width of the histogram by the number of servers and multiplying it by the score of the server. This ensures that the width of the bar is proportional to the attack count relative to the total number of attackers.

**Histogram Visualization:**

The function *histogram.DrawRectangle* is called to draw each rectangle at its appropriate position and size within the histogram area. The height of each rectangle reflects the number of attacks on the respective server.

{:.list-inline} 
- Date: 9th of October 2024


