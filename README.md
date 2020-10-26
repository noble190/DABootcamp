# Kickstarting with Excel

## Overview of Project

This project utilizes Kickstarter crowdsourcing data across a range of years and project categories / subcategories together with the analytic capabilities of MS Excel: namely, formulae, pivot tables, and charts.

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




### Analysis of Outcomes Based on Goals

### Challenges and Difficulties Encountered

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?

- What can you conclude about the Outcomes based on Goals?

- What are some limitations of this dataset?

- What are some other possible tables and/or graphs that we could create?
