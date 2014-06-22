---
layout: post
title: What are the different type of questions a Data Scientist would ask ?
tags:
- datascience
- questions
---

These are the different classifications of questions a Data Scientist can ask :

1. **Exploratory**

2. **Descriptive**

3. **Inferential**
Often, you do not have access to the whole data (better called population) you are interested in investigating, but only a limited number of data instead. For example, you might be interested in the exam marks of all students in Canada. It is not feasible to measure all exam marks of all students in the whole of Canada, so you have to measure a smaller sample of students (e.g., 100 students), which are used to represent the larger population of all Canada students. Properties of samples, such as the mean or standard deviation, are not called parameters, but statistics. Inferential statistics are techniques that allow us to use these samples to make generalizations about the populations from which the samples were drawn.

Usually almost every statistics driven company uses this to publish results. For example, Nielson ratings gather information from a small sample of homes and are used to infer the television-viewing patterns of an entire country.

4. **Predictive**

5. **Causal**
Causal question are usually asked to find out what happens to one variable when you change another.

	- Implementation usually requires randomized studies
	- There are approaches to inferring causation in non-randomized studies
	- Causal models are said to be the “gold standard” for data analysis
	- Type of data set applied to: Randomized Trial Data Set – data from a randomized study

	Causal analysis aims to explain the causal relations between variables. If you want to indicate explicit causality, your study must include an experiment. You compare the control and treatment groups, for example, with variance analysis.  i

	You may also use regression analysis, which measures causality in a weaker way. Regression analysis enables you to explore the influence of several variables on a single variable at the same time. Regression analysis may also focus on exploring the intensity of the influence of a single variable.

6. **Mechanistic**

Mechanistic type of modelling requires the most amount of effort. It requires you to understand the exact changes in variables that lead to changes in other variables for individual objects.

"All other things being equal, mechanistic models are more powerful since they tell you about the underlying processes driving patterns. They are more likely to work correctly when extrapolating beyond the observed conditions."
-Bolker (2008) Ecological models and Data in R, p7.


	- Incredibly hard to infer, except in simple situations
	- Usually modeled by a deterministic set of equations (physical/engineering science)
	- Generally the random component of the data is measurement error
	- If the equations are known but the parameters are not, they may be inferred with data analysis
	- Type of data set applied to: Randomized Trial Data Set – data about all components of the system


