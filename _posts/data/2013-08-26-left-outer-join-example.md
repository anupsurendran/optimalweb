--- 
layout: post
title: Left Outer Join Example
tags: 
- left outer join
- data scientist
- sql joins
---
So I have a products table :


And I have a Sales table:


If I want to find the sales for ALL products including the ones which are not present in the sales table, I can do this ( SQLITE syntax) :
select p.productname, 
case when sum(amount) is null then 0 else sum(s.amount) end as totalsales 
from product p left outer join sale s on p.productcode = s.productcode 
where s.productcode is null or s.productcode is not null group by p.productname 


One of the best examples I have seen for Outer and Inner joins is at CodingHorror
