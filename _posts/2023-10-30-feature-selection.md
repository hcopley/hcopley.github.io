---
title: "Feature Selection for Linear Models"
author: "Heather Copley"
date: "2023-10-30"
output: 
    html_document:
        keep_md: yes
---

Selecting the right variables for any predictive model can be a daunting task, particularly if there are a very large number of variables to choose from or you don't have domain expertise in the subject area. There are several different approaches one can take including manually selecting variables and algorithmically choosing variables that have the most "importance". Selecting variables for a linear model may also require some special considerations due to the assumptions of linear methods. In this post I will attempt to discuss some of the techniques that can be used when selecting variables for a linear model.

## Start with Domain Expertise

Whenever possible it is best to discuss the goal in mind and the data itself with the experts. This collaboration can often lead to a more focused and relevant selection of predictors, guiding you toward essential variables and potentially identifying others that are not initially present in your dataset but need to be collected or constructed. A conversation with knowledgeable subject matter experts in the field can also help you ensure your variable choices are well-aligned with the topic and identify any variables that may be misleading or inappropriate. Sometimes your dataset may contain variables that are correlated with your target variable, but are more a consequence or characteristic of the target itself rather than serving as reliable predictors. Engaging in these expert conversations can help you navigate such nuances. 

## Consult the Research

If you are lucky, there may already be research related to the variable you are trying to predict. It is important to look to existing research to see what has been tried in the past as well as what factors are known to be related to your target variable. There may be known predictors that will help you get the most out of your model. 

## Use your Exploratory Data Analysis

A good EDA can also help you understand which features are related to the target you are interested in, and which are less than helpful. With linear models in particular you are going to want to assess variables that will violate assumptions. You will want to check for multicollinearity between predictors. During this stage you can decide to either leave some variables out, combine variables that are correlated, or use an algorithmic approach to address the correlation such as PCA (described below).  

## Algorithmic Approaches

Once an initial set of potential predictors are selected using some or all of the methods above, an algorithmic approach may be considered. Keep in mind that algorithmic approaches to feature selection can be a very powerful tool, but typically have different goals and there may be a loss of interpretability depending on the method chosen. [This paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5969114/) also recommends not using algorithmic approaches on variables known to be strong predictors by prior research or expertise. The examples noted are age in cardiovascular risk models, and tumor stage in cancer modeling. It is also helpful to use Cross-Validation and/or Stability Selection in combination with the methods described below. 

### Stepwise Methods

Forward Selection, Backward Elimination, and Stepwise Selection are widely used in practice, however their application should be approached with caution due to a lack of robust theoretical foundation. Despite this, they are easy to use and they can still serve as valuable tools in simplifying a complex model to a more manageable form.
    
### Criterion Based Methods

These methods involve fitting models with all possible subsets of predictors and choosing the model that have "better" acceptance criteria such as AIC, BIC, adjusted $R^2$, etc. While also a useful tool, this may not be possible or efficient if the set of potential variables if large. 

### Dimension Reduction Methods

Dimension reduction techniques such as PCA are useful in reducing the ultimate number of predictors that are used in the input of a model. The resulting principal components will be by nature, not correlated with one another and the first few components will explain the largest variability in the dataset. This has some obvious advantages particularly in linear modeling but it is important to keep in mind that some interpretability of the model is lost. Biplots and correlating the principal components with the original variables can help, but are ultimately more difficult to explain than the original variables themselves. If interpretability and meaning of the predictors are important, PCA may not be the tool you want to use. 

### Regularization Methods

Lasso, Ridge Regression, and Elastic Net methods decrease model complexity by performing both regularization and variable selection. These are helpful methods particularly if the number of predictors is larger than the number of observations. 


