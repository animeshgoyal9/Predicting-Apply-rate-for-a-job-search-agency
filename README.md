# Predict Click through rate (CTR) for a website

# Introduction

The problem of interest is the prediction of apply rate. Imagine a user visiting a website, and performing a job search. From the set of displayed results, user clicks on certain ones that she is interested in, and after checking job descriptions, she further clicks on apply button therein to land in to an application page. The apply rate is defined as the fraction of applies (after visiting job description pages), and the goal is to predict this metric using the dataset described in the following section.

# Dataset

Each row in the dataset corresponds to a user’s view of a job listing. It has 10 columns as described below.
1) title proximity tfidf: Measures the closeness of query and job title.
2) description proximity tfidf: Measures the closeness of query and job description.
3) main query tfidf: A score related to user query closeness to job title and job description. 
4) query jl score: Measures the popularity of query and job listing pair.
5) query title score: Measures the popularity of query and job title pair.
6) city match: Indicates if the job listing matches to user (or, user-specified) location.
7) job age days: Indicates the age of job listing posted.
8) apply: Indicates if the user has applied for this job listing.
9) search date pacific: Date of the activity.
10) class id: Class ID of the job title clicked.

# Analysis

Please use the “search date pacific” column (9-th column) to split the dataset into training and test dataset. Train your model(s) using the data between 01/21/2018-01/26/2018, and test your model on 01/27/2018.
Split the analysis into two parts:

1) Focus on the first 7 columns. Use these as features to predict the 8-th column, “apply”. Discuss the
model you choose. Primarily focus on AUC as the metric of interest for your binary classifier. You
can also investigate/discuss other metrics.

2) Consider now adding the last column to your feature set. Is it possible to segment data based on
(“class id”), and achieve a better classification performance? How would you generate a better model using this feature?
