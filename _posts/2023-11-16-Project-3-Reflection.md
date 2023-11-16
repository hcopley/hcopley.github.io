---
title: "Project 3 Reflection"
author: "Heather Copley"
date: "2023-11-16"
output: 
    html_document:
        keep_md: yes
---

## Project 3 Reflection

### Project Objective

This was a collaborative project with the aim of automating the production of R Markdown reports for developing predictive models for distinct subsets of diabetes data. The data was segmented into levels of highest education reached by the respondents and reports were automated through an Rmarkdown document with parameters. Multiple models were attempted on each data segment and the optimal model among them was ultimately chosen. 

### Project Links

* [Project 3 ](https://hcopley.github.io/ST558_Project_3/)
* [Prject 3 Github repo](https://github.com/hcopley/ST558_Project_3)


### What I would do differently

With more time to delve into this project, there are a few things I'd really like to tackle. First I would have liked to automate the descriptive part of our exploratory data analysis. It would be great to have automatically generated detailed descriptions tailored to each of the plots.

I would also like to experiment with some new modeling methods that I'm even less familiar with such as neural networks. I would also like to spend more time understanding the models we did use and their output. For example, I learned the hard way with the random forest model. Adjusting the 'mtry' parameter and the number of trees made a huge difference in the amount of time it took to process – wish I'd realized that sooner!

Another thing on my list would be to examine the results from each educational level more closely. I'm curious about why certain models performed better for some groups than others and I wonder if it had more to do with the size of the data sets vs. the characteristics of the members. Understanding these nuances could be really helpful for future projects


### The most challenging part for me

The most significant challenge I encountered in this project was managing GitHub Pages. I had difficulty ensuring the pages displayed as intended after rendering our Markdown documents and uploading them to GitHub. We found it necessary to delete all old files before re-rendering and updating the remote repository. If not done meticulously, graphs and titles would be placed out of order from the text. I felt like I had little control over the HTML rendering of the documents from the Markdown files, but I am sure this is something that takes time to learn. Another aspect I would approach differently is the use of LaTeX for equations, as I later realized that GitHub Pages does not natively support LaTeX. While equations appeared correctly within GitHub's repository view, they did not render on the actual webpages. Despite our efforts to address this issue, we ultimately could not find a working solution. 


### My take-aways from this project

I found it surprising how the varying education levels in our datasets led to such different outcomes in terms to the optimal model chosen. I found it interesting to that in some instances, ensemble methods, which are generally considered more flexible and powerful, didn't outperform a simple logistic regression. This really highlighted for me the nuanced nature of predictive modeling and the importance of considering the specific characteristics of each data segment and trying many model types when choosing a modeling approach. I also found it interesting coding for different scenarios that arise when automating tasks. As an example there was one particular classification tree that completed with no branches. We had planned to graph all of our trees and this made a unique challenge for only one subset of the data. I realized how important it is to plan for contingencies when coding for automation because unforseen scenarios can happen especially if we were to include new data. I also have never worked collaboratively with another person on the same project in the same github repository. I expected that to be extremely difficult, but I found that part of the process to be easy and seamless.


