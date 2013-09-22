--- 
layout: post
title: What is a Theta Join ?
tags: 
- theta join
- data scientist
- database joins
---
The most general join operation is Theta Join (or q join). The Theta Join is defined as the result of performing a selection operation using comparison operator Theta (q), on the product. In other words, a join operation with a general join condition using Theta (q) operator is called a Theta Join.
For example, if you want only those tuples of the product of two relations ‘Student1’ and ‘Student2’ whose value is ‘L’ in the attribute ‘City’, Theta joinoperation is written as:

 
Student1 TIMES student2 WHERE City =’L’This is equivalent to: 
Student1 TIMES student2 GIVING temp
 SELECT temp WHERE City =’L’
