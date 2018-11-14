# CS26520 Lecture 16
## Evolutionary Algorithms
__Thuraday, March 15th 2018__  
Lecture: mxw@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Myra Wilson](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=mxw).

## Introduction 
"EAs are the next step from the previous heuristics, $h(n)$, that we were looking at."

Definition: **"An EA is an iterative procedure which evolves a population of individuals."** 

- Each individual is a candidate solution to a given problem
- Each individual is evaluated by a fitness function, which measures the quality of its candidate solution.

> Reading: [Vrije University, Amsterdam](http://www.cs.vu.nl/~gusz/ecbook/Eiben-Smith-Intro2EC-Ch2.pdf)

At each generation (iteration): 

- It folows a survival of the fittest patttern - the best individuals are selected. 
- Genetric operators are aplpied to selected individuals in order to produce offspring. 
- Offspring are evaluated by a fitness function. 

## Genetic Algorithms

Evolutionary Algorithm &rightarrow; Gentic Algorithm (popular EA)

Definition: **"Directed search algorithms based on the mechanics of biological evolution."**

- Provide efficient, effective techniques for optimisation and machine learning applications. 
- Artificial systems software that retains the robustness of natural systems. 

### Applications 

Loads of applications. 

### GA Terminology 

- Chromosome 
    - Potential solutions to the problem.
    - Could be any of the following: 
        - Bit patterns.
        - Strings. 
- Population 
    - Colletion of poltential solutions.
- Parents and Children 
    - Chromosomes. Child chromosomes are generated through recombination/crossover. 
- Gnerations 
    - The number of iterations.cycles through the GA process. Can we done a set number of times or until specified size of population is reached. 

### Simple Genetic Algorithm Stages:

Problem   
&downarrow;    
Encoding Technique  
&downarrow;  
Initialization Procedure   
&downarrow;  
Evaluation Function   
&downarrow;  
Parent Selection   
&downarrow;  
Genetic Operators   
&downarrow;  
Parameter Settings 

### Simple Genetic Algorithm Example:

```java
init population;
eval population;

while (terminationCriteriaNotSatisfied){
    select parents;
    perform mutation;
    eval population;
} 
```

## Discrete Representation

## Process 

### Representation 
### Selection 


