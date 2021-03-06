--- 
layout: post
title: Introduction to Bayesian analysis
tags: 
- bayesian analysis
- machine learning
- statistics
- bigdata
---
The key ingredients to a Bayesian analysis are the likelihood function, which reﬂects information about the parameters contained in the data, and the prior distribution, which quantiﬁes what is known about the parameters before observing data.
The prior distribution and likelihood can be easily combined to form the posterior distribution, which represents total knowledge about the parameters after the data have been observed.

###Fundamentals of a Bayesian Analysis

A typical Bayesian analysis can be outlined in the following steps :

1. Formulate a probability model for the data.
2. Decide on a prior distribution, which quantiﬁes the uncertainty in the values of the unknown model parameters before the data are observed.
3. Observe the data, and construct the likelihood function ) based on the data and the probability model formulated in step 1. The likelihood is then combined with the prior distribution from step 2 to determine the posterior distribution, which quantiﬁes the uncertainty in the values of the unknown model parameters after the data are observed.
4. Summarize important features of the posterior distribution, or calculate quantities of interest based on the posterior distribution. These quantities constitute statistical outputs, such as point estimates and intervals.
