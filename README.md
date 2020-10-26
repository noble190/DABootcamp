# Kickstarting with Excel

## Overview of Project

This project utilizes Kickstarter crowdsourcing data across a range of years and project categories / subcategories together with the analytic capabilities of MS Excel: namely, formulae, pivot tables, and charts.

The following excel spreadsheet was used for all analytics for this project (File was not compressed as the resulting space savings were negligible):

[Data Spreadsheet](https://github.com/noble190/DABootcamp/blob/main/Kickstarter_Challenge.xlsx)

### Purpose

My purpose is to analyze the relationships between launch dates / funding goals and Kickstarter project outcomes in order to be able to make productive recommendations to maximuze the likelyhood of a successful Kickstarter project.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

An Excel pivot table / chart combination was used in order to analyze the impact of launch date (month) on project outcomes.

In order to implement the required filters on the pivot table, the initial dataset had to be modified with a few additional columns. Firstly, the 'Category and Subcategory' column was split into 'Parent Category' and 'Subcategory' columns using the Excel Text to Columns functionality in order to facilitate filtering by the 'Theater' parent category. Finally, a 'Years' column was created with values populated by the Year() formula and data from the previously created 'Date Created Conversion' column in order to facilitate filtering by year.

The pivot table fields were set up as follows:

![Pivot Table Fields](https://github.com/noble190/DABootcamp/blob/main/resources/pivotTableFields.png)

Afterwards, the Date values were grouped by month, and the outcome values were sorted. The 'Parent Category' chart filter was set to 'theater'.

The resulting pivot table looks just like the example in the assignment:

![Pivot Table](https://github.com/noble190/DABootcamp/blob/main/resources/pivotTable.png)

A Line Chart with Markers was used to plot the data. Afterwards, line colours were adjusted to match the palette in the assignment example:

![Chart 1](https://github.com/noble190/DABootcamp/blob/main/resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals

A variety of excel formulas was used in order to analyze the impact of funding goals on project outcomes.

My starting point were the 8 columns and 12 value ranges provided in the assignment description. Afterwards, I have used the 'COUNTIFS' formula for each permutation of value range and outcome for the 'plays' category. I have structured my formula as follows:

![CountIfs Formula Breakdown](https://github.com/noble190/DABootcamp/blob/main/resources/countIfsExplained.png)

The remaining formulas were relatively straightforward. The 'Total Projects' column was populated using the Sum formula on the 'Number' columns for each respective row. The 'Percentage' columns were populated by simple division and formatted as percentages with 0 decimal points.

A simple Line Chart was used to plot the data. Specific columns were selected just prior to inserting the chart:

![Chart 2](https://github.com/noble190/DABootcamp/blob/main/resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered

I have not encountered significant challenges with this assignment. One potential difficulty that could be encountered would be the conversion of value ranges for the Outcomes vs Goals analysis to COUNTIFS criteria. I have simply used multiple criteria where the range was between two concrete numbers, but this may not be immediately apparent. I'm not sure if it's possible to have composite conditions as COUNTIFS criteria (for example, something like ">=1000 && <5000").

## Results

### Conclusion - Outcomes based on Launch Date

Upon analyzing the data for funding outcomes based on the launch month of kickstarter campaign for the 'theatre category', two conclusions are evident:

1. The majority of campaigns are launched during the period of late spring to summer. 

2. Campaigns are most likely to succeed in the months of May and June, and are least likely to succeed in the month of December.

### Conclusion - Outcomes based on Funding Goals

Upon analyzing the data for funding outcomes based on funding goals, it is evident that projects with funding goals between $1000 and $4999 are most likely to be funded, with a 73% percent likelyhood of success. The likelyhood of funding success for theatre projects appears to decrease as funding goal increases.

### Limitations of Dataset

A major limitation of this dataset is the # of records. It may be usable to generate a high-level summary across all countries, categories, and years, but is not sufficiently large for more detailed analysis. One example is the above analysis of outcomes based on funding goals - once filtered by the 'theatre' category, there is insufficient data to reliably predict outcomes for the higher funding goal ranges. If an additional set of filters is applied (for example, targetting a single country), there may be insufficient data for any sort of analysis.


### Recommendations for additional analysis

This dataset may be used to analyze the likelyhood of success of kickstarter projects per category, per country, using a combination of a pivot table (outcomes on Columns & Values, country on Rows) and a pivot chart (stacked bar chart would be appropriate). This may help make recommendations as to whether a particular project category is viable in a target country.

<hr>
<hr>
<hr>

