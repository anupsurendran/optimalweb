--- 
layout: post
title: What is a Join Operation ?
tags: 
- data scientist
- database join
- database fundamentals
---
The join operation is used to combine related tuples from two relations. This operation is very important in relational databases because it allows to process relationship among relations.
The join operation is the combination of the product, selection and projection operations. The join operation on two relations is performed as follows:
Product operation is performed on two relations.
Selection (SELECT) operation is performed to eliminate duplicate tuples by the join criteria or condition.
Projection (PROJECT) operation is performed to remove some attributes.
The PROJECT operation is another unary operation. This operation returns a set of tuples containing a subset of the attributes in the original relation. Thus, as we state that the SELECT operation selects some rows and discards the others. The PROJECT operation, on the other hand, selects some columns of the relation and discards the other column. The PROJECT operation can be viewed as the vertical filter of the relation.
Here is a wikipedia article on the Join Operation .
