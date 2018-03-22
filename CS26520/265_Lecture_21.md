# CS26520 Lecture 21
## Data Mining
__Monday, March 19th 2018__  
Lecture: rkj@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Richard Jensen](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=rkj).

## Overview of Data Mining 

"A difficult process of trying to find "golden nuggets" of information in a large data set." 

Data Set &rightarrow; Filtering Technique &rightarrow; Result 

Definition 1: Extraction of interesting information (non-trivial, implicit, uknown and potentially useful) or patterns from data in large databases.   

Definition 2: The process of discovering meaningful new correlations, patterns and trends by sifting through large amounts of data stored in repositories using AI as well as using statistical and mathematical techniques.

**Remember: Correlation is _not_ causation.**

### Why mine data? 

From a commercial viewpoint, it's a goldmine: 

- Lots of data is collected.
    - Web data, e-commerce trends.
    - Transactions.
- Computers have become powerful and cheap. 
- Competative pressure is strong. 

From a scientific viewpoint:

- Data is collected and stored at enormous speeds.
    - Remote sensors (satellites).
    - Telescopes scanning the skies.
    - Scientific simulations. 
- Traditional statistical techniques are redundant for analysing large data sets. 

We have lots of data - a lack of data is not the problem. A lack of _knowledge_ is the problem. 

## Introduction to Data Mining Techniques 

### What does data look like? 

- Collection of information about a particular domain. 
- Stored in a tabular form.
    - Each row being an _instance_.
    - Each column is a _measurement_.  
    - Final column is the decision. 

Data mining is not a set of tools. It should be thought of as process. 

### Data Preparation 

- Dealing with missing values. 
- Removing or reducing noise from the data that could cause the data to be misleading. 
    - Sometimes there might be redundant data (lots of idential data points).

- Feature selection - finding the data that doesn't have any bearing on the problem. 

### Data Understanding and

### Data Reduction 

## Classification 

**Given a collection of records/instances (a training set), we want to find a model for the class feature as a function of the values of the other features.**

**Goal: previously unseen instances should be assigned a class as accurately as possible.** 

Example: Fish packaging plant automating process of packaging Salmon and Seabass.

Preprocessing &rightarrow; Feature Extraction &rightarrow; Classification 

Errors in the example: 

- Insufficient training data. 
- Too few features. 
- Too many irrelevant features. 
- Overfitting (too much training). 

### Applications of Classification 

- Direct Marketing 
    - Goal: Reduce cost of mailing by targeting a set of consumers likely to buy a new product. 
    - Approach: Use data for a similar product introduced previously. 
        - {buy, don't buy} is the class feature. 
        - Collection various demographic, lifestyle, company-interaction information.
        - Use this data as input features. 
- Customer Attrition (Churn)
    - Goal: Predict if a customer is likely to be lost to a competitor. 
    - Approach: Use detailed record of transactions with each of the past and present customers. 

## Clustering 

**Given a set of data points (instances), find clusters using a similarity measure such that data points in one cluster are more similar to one another, and data points in separate clusters are less similar to one another.**

Similarity Measures: 

- Market Segmentation
    - Goal:
    - Approach:
        - Something.
        - Something 2. 

- Document Clustering 
    - Goal:
    - Approach:
        - Something 1. 
        - Something 2. 

### Applications of Clustering 

## Association Rule Mining 

