--- 
layout: post
title: Matrix responses - Process of design
tags: 
- matrix question survey data
---
This post is help the readers get an idea of how we approach some of the visualization problems.
For a matrix type question in a survey, like the one below, the visualization elements to understand the aggregated responses gets quite complicated.



 
What are we trying to get here - What questions do we need answered to deal with responses from the matrix question above ?
For example, we are looking at the following :
1. How many people ‘Liked’  HBO for example ?
2. How can I compare - How many people ‘Liked’ HBO vs How many ‘Liked’  Star Movies ?
3. How can I compare - How many people ‘Liked’ HBO vs How many people ‘Disliked’ SONY PIX ?
I am not going through an exhaustive list of questions based on different answer types (between 1 - Dislike and 5 - Like) and the movie channels ( SONY PIX, AXN etct) because you can substitute that within the question above.
But I think we have covered the most important questions around matrix responses above.
Let’s see if we can answer them by asking more questions :)
What is our smallest dataset we can deal with when dealing with these questions ?
The smallest one would be  the following : [Option , Scale , Response Count], for e.g. [“HBO”, Dislike, 5]. If we have had this dataset, then we could answer question 1 above.
What is the best way to present that dataset ?
Maybe we can use 3 axis’s, because there are three datapoints; 3D ?


 
The blue dot above is the datapoint we are trying to visualize.  Doesn’t this look a teeny bit intimidating and we have only our smallest meaningful dataset for a survey response.
3D is cool. But in the diagram above, without the lines connecting the blue dot to the axis’s this would be hard to understand.
What if we removed an axis?  Since the Response count is very chartable because its a number, we are left with the other two axises. But the Dislike to Like is a scale, which means there is already a number assigned to it where 1 is Dislike and 5 is Like. So we are really left with the Option axis.
What if we color coded these options - lets use Blue for HBO.



Doesn’t this look much more easier to read ? . What is missing here ? . A legend which says HBO = blue.
Now let’s add couple more responses to this -  [“HBO”, Like, 4], [“Star Movies”, Like, 5],[“SONY PIX”, Dislike, 4]
Before adding these responses, we need to come up with a color code, let’s say Star Movies is green and SONY PIX is Orange.  So this is what the visualization will look like :

So the color coding for the chart above is  - HBO=Blue, Star Movies=Green, SONY PIX=Orange. 
Now, trying answering the questions we had at the beginning of the post, Easy to visualize and easy to answer right?
