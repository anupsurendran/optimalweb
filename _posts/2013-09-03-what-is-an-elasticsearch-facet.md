--- 
layout: post
title: What is an ElasticSearch Facet ?
tags: 
- elasticsearch
- facets
- geodistancefacet
---


LinkedIn uses facets to refine their search query.
In ElasticSearch, Facets are additional data which you can attach to a query. This helps with returning aggregate statistics alongside regular query results. The aggregate statistics are a core part of elasticsearch, and are exposed through the Search API.
An example would be to consider searching for your ex-colleagues who worked with you. The best example from the above screenshot is when you want to find colleagues whose “Past Company” was “ABC Company”.
Facets are highly configurable. In addition to counting distinct field values, facets can count by more complex groupings, such as spans of time, nest filters, and even include full, nested, elasticsearch queries.
Here is an example of a Geo Distance Facet which is included as part of an ElasticSearch Query.


Image courtesy of Karmi.
