--- 
layout: post
title: 3 Differences between a MapReduce Combiner and Reducer ?
tags: 
- hadoop
- combiner
- mapreduce
- bigdata
---
Think of a Combiner as a function of your map output. This you can primarily use for decreasing the amount of data needed to be processed by Reducers. In some cases, because of the nature of the algorithm you implement, this function can be the same as the Reducer. But in some other cases this function can of course be different.
A combiner will still be implementing the Reducer interface. Combiners can only be used in specific cases which are going to be job dependent. 


Difference # 1
One constraint that a Combiner will have, unlike a Reducer, is that the input/output key and value types must match the output types of your Mapper.
Difference  #2
Combiners can only be used on the functions that are commutative(a.b = b.a) and associative {a.(b.c) = (a.b).c} . This also means that combiners may operate only on a subset of your keys and values or may not execute at all, still you want the output of the program to remain same.
Difference  #3
Reducers can get data from multiple Mappers as part of the partitioning process. Combiners can only get its input from one Mapper.
