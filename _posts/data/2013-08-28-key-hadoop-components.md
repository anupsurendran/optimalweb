--- 
layout: post
title: "Key Hadoop Components "
tags: 
- hadoop 101
- data scientist
- Hadoop architecture
---




The three major categories of components in a Hadoop deployment are Client machines, Masters nodes, and Slave nodes.  
The Master nodes oversees the two key functional pieces that make up Hadoop: storing lots of data (HDFS), and running parallel computations on all that data (Map Reduce).  
The Name Node oversees and coordinates the data storage function (HDFS), while the Job Tracker oversees and coordinates the parallel processing of data using Map Reduce.  
Slave Nodes make up the vast majority of machines and do all the dirty work of storing the data and running the computations.  Each slave runs both a Data Node and Task Tracker daemon that communicate with and receive instructions from their master nodes.  
The Task Tracker daemon is a slave to the Job Tracker, the Data Node daemon a slave to the Name Node.
