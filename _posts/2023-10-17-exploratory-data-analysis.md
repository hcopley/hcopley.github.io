---
title: "Exploring Exploratory Data Analysis"
author: "Heather Copley"
date: "2023-10-17"
output: 
    html_document:
        keep_md: yes
---

## What is Exploratory Data Analysis?

Exploratory Data Analysis (EDA) is an indispensable step in any data analysis or modeling process. While it might sometimes feel like wading through the weeds, it's an important tool in any data scientist's or statistician's toolkit.

The overall goal is to better gain a deeper understanding of the data's characteristics, shape, and structure before diving into more advanced analytical methods. This understanding paves the way for more appropriate subsequent analyses, and allows for informed data transformations that better support the intended analysis.

## Strategy

The strategy for EDA often involves addressing the following questions. The process can be linear or cyclical, with certain steps revisited as new insights are discovered.

### What is the objective? 

At the heart of an effective EDA strategy is clarity about the ultimate goal. Before even looking at the data it's important to understand what questions you might be trying to answer or problems you want to solve and their context. Are you aiming to predict an outcome, discern natural groupings, answer specific questions, or understand certain relationships? Establishing clear objectives upfront is crucial. Keeping this objective in mind throughout the process of EDA is also important.

### What is the overall structure?

It's important to know the overall dimension of your data. How many observations (typically rows) and how many columns do you have. Are the observations unique or repeated? What data types are your dealing with (numeric, categorical, temporal, free-text, etc.) 

### What is the meaning?

Each variable carries some meaning which may or may not be self-explanatory and its important to do your research to understand that meaning. Is there a data glossary available? Are there subject matter experts or stakeholders you can talk to? Don't make assumptions based solely on column names. Sometimes the way that the data was intended to be collected and the way it was actually collected can differ greatly. 

### How should the data be cleaned?

* Are there missing values in any of the columns. If so what is the meaning of the missingness? You may want to simply remove the missing observations, replace them with another value (impute) like the mean, median, mode, or using predictive methods. This decision should be driven by the meaning.

* Are there duplicate values that need to either be removed, or reshaped. You may have truly duplicate values where all column values are identical. These you will likely want to remove. You may have repeated observations on different dates or under different circumstances in which you may require reshaping. 

* Are all of the variables coded as the expected data type? Are numeric values coded as numeric rather than text and do they have the appropriate precision? Are categorical variables coded as such (either character or factor) and do they have appropriate levels. You may find that there are some levels in your categories that are actually the same, are inconsistent due to misspelling, case sensitivity, etc.

### What is the nature of each variable?

This step involves both visualizing and summarization. 

* For numeric and continuous variables you can explore the distribution using boxplots, histograms, quantiles, and measures of central tendency and spread. Do the data follow a particular distribution or shape?

* For categorical variables you will typically want to use barcharts and frequency tables.

### Are there relationships among the variables?

Cross tabs, scatterplots, correlation matrices can help us both visualize and measure the strength or lack of relationships between the variables.

* Pairs plots can also help you identify relationships between numeric variables. 
* Stacked bar charts and chi-squared tests can help to determine if there are relationships among categorical variables. 

### Are there outliers?

* For numeric variables you may use thresholds to identify outliers such as 1.5 x the IQR or 2 standard deviations from the mean. You can also use box plots or scatter plots.

* For categorical variables you may want to identify categories that occur too frequently or infrequently in comparison to the other categories. 

### Are your assumptions appropriate?

Does the data align with your intended method? If you know at the outset the type of analysis you will be conducting, or the method you will be using now is a good time to see if the assumptions of that method hold. If not is there another similar method you could use that is more flexible or appropriate to the data. 

## Final Thoughts

Exploratory Data Analysis helps us to bridge the gap between raw data and meaningful insights. It ensures that our subsequent methods are well informed and appropriate to both the data and the questions we want to answer or problems we want to solve. 
