--- 
layout: post
title: How to remove inspect element in Chrome ?
tags: 
- statistics
- spss
- analysis
- crosstabs
---

###Step 1 - Get the SPSS file and understand which variables you will be using for your crosstabs.

I had the following source file and wanted to find out differences between shopping behaviour of Males and Females for a specific event.

![SPSS Source file for cross tabs]({{ site.baseurl }}/assets/img/spss-input-file-for-analysis.png "SPSS file")

My independent variables  are therefore - Gender ( Male, Female)  and my dependent varable is the question  - 'Do you shop on Black Friday?'

###Step 2 - Add the variables on SPSS under Analyze > Descriptives > Crosstabs

Check the screenshot below

![SPSS Menu for Crosstabs]({{ site.baseurl }}/assets/img/spss-crosstab-menu-option.png "SPSS Menu for Crosstab")

Choose the variables you want to see in the crosstab

![SPSS Variables for Crosstabs]({{ site.baseurl }}/assets/img/spss-cross-tab-variables.png "Select variables for SPSS Crosstab")


###Step 3 - Create Crosstab with percentage values


Then choose the Statistics option > Chi-square

![SPSS Chi-square]({{ site.baseurl }}/assets/img/spss-chi-square.png "SPSS Chi-square")

And under option Cells, ensure you have clicked on Percentage > Columns

![SPSS Column percentage]({{ site.baseurl }}/assets/img/spss-crosstab-column-percentage.png "SPSS column percentage")

And once you have this setup you can generate the report which looks like this for my example:

![SPSS Crosstab report]({{ site.baseurl }}/assets/img/crosstab-report-generated-from-spss.png "SPSS Crosstab report") 
