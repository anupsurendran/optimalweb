--- 
layout: post
title: Introduction to Decision Trees
tags: 
- machine learning
- decisiontree
- data
---
A decision tree is a classic and natural model of learning. It can be applied to many machine learning problems. The best way to introduce this would be with an example using binary classiﬁcation.

Suppose that your goal is to predict whether some unknown passenger in  will enjoy some unknown future flight he/she is going to take. You have to simply predict with an answer of  “yes”or “no.”
In order to make a guess, your’re allowed to ask binary questions about the passenger under consideration.

For example:
{% highlight ruby %}
Machine: Are you going on vacation?
You: Yes
Machine: Is the flight early morning?
You: Yes
Machine: Is the flight more than 2 hours?
You: Yes
Machine: I predict this passenger will not enjoy the flight.
{% endhighlight%}

The goal in learning is to ﬁgure out what questions to ask, in whatorder to ask them, and what answer to predict once you have askedenough questions.
The decision tree is so-called because we can write our set of questions and guesses in a tree format. Usually the answers would decide how to navigate the tree.
Diagramatically, the questions are usually written in the internal nodes (rectangles) and the guesses are written in the leaves (ovals). Each non-terminal node has two children: the left child speciﬁes what to do if the answer to the question is “no” and the right child speciﬁes what to do ifit is “yes.”

More learning at  [Optimal.io](http://www.optimal.io) 
