---
layout: post
title: How we are building Alexa for the mobile industry.
tags:
- alexa
- mobile statistics
- alexa for mobile
- find top apps running on mobile
---

*Where is the Univeral Mobile Statistics Site ?

It's a mobile world - everybody knows that. It's been like this for almost a decade now. The funniest thing is that we still don't have an [Alexa](http://www.Alexa.com) for the mobile industry. There is no publicly available source currently which I can take a look at to see where my / my company's mobile application ranks amongst other apps of the sametype. There are challenges to get statistics from mobile applications - distribute processing, offline/online support, hybrid applications all lead to 

In my opinion there are three ways to do this.  

1.Google could ask their Google Analytics mobile users to publish their mobile statistics publicly. 
I know that this is a completely different model which will conflict with their existing service model where the end customers will not agree to because its their 'private' metrics. 

Even if Google goes down with this model, there is a challenge of proving that the metrics is correct. What I mean by that is that the Analytics code ( UA-*** ) could have been used in one of an existing mobile application which was already popular and therefore prevents an easy verifiable method to prove the identity of the mobile application.

2. Users call an api to publish their user statistics.
Again this proves to be a non-verifiable way of ensuring the statistics is accurate.

3. A 3rd Party runs device level statistics and collects it centrally. 
A mobile phone is a personal device.  Running a process there to collect information requires permissions from users and has an intrinsic resistance built up. But if you think through this problem, and if use inferential statistics, you could identify a sample which represents your population you want to get data from. You could incentivize them to get the data you need (ie. sending only app related data back to your servers).   

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

		"All other things being equal, mechanistic models are more powerful since they tell you 
		about the underlying processes driving patterns. They are more likely to work 
		correctly when extrapolating beyond the observed conditions."
		-Bolker (2008) Ecological models and Data in R, p7.

	- Incredibly hard to infer, except in simple situations
	- Usually modeled by a deterministic set of equations (physical/engineering science)
	- Generally the random component of the data is measurement error
	- If the equations are known but the parameters are not, they may be inferred with data analysis
	- Type of data set applied to: Randomized Trial Data Set – data about all components of the system


