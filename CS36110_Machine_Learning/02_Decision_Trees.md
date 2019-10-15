# Decision Trees 

Machine Learning with bits of Information Theory 

Michaelmas Term 2019 

These notes are based off of lectures given at Aberystwyth University by [Neil Mac Parthalain](https://www.aber.ac.uk/en/cs/staff-profiles/listing/profile/ncm/).

> Reading: Chapter 3 of [_Machine Learning_ by Mitchell](http://profsite.um.ac.ir/~monsefi/machine-learning/pdf/Machine-Learning-Tom-Mitchell.pdf)

## Introduction

### What are decision trees? 

A decision tree is used to model decisions and their possible consequences using a tree-like graph. In essence, it maps observations to conclusions about a target value (crisp or discrete). 
Decision trees can be re-represented as if-then rules as a decision support tool. 

> It is a method for approximating discrete-valued functions that
is robust to noisy data and capable of learning disjunctive expressions.

### When should we use decision trees? 

Instances (data objects) should be described by feature-value pairs. 
Decision trees are useful for "problematic" data, either noisy data or data which contains missing feature values.  
 
### Why shouldn't we use decision trees? 

Real valued decisions are 
Problems which are not easy to express are XOR; 

## Decision Tree Representation 

### How do we build decision trees? 

### Top Down Induction

### Choosing the root feature? 

### Choosing the feature to split upon 

## Entropy & Information Gain  

### Entropy 

Entropy measures the order (uncertainty) of a given data set by examining the homogenity of the items in the set. 

Entropy (S) = 

Where S is an arbitrary collection of examples of a test set.

The binary entropy function is a special case of the the entropy function. 

### Information Gain 

Information gain is the heurisitic that's used by the algorithm building the tree which determine the feature which it will split upon. The algorithm is looking for the attribute which returns the greatest information gain (and thus most homogenous branches.)

Information gain is based on the decrease in entropy. 

## ID3 Algorithm

The pseudocode algorithm 

### Example Usage 



