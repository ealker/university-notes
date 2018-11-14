# CS26520 Lecture 22
## Data Mining - Classification 
__Thursday, March 22nd 2018__  
Lecture: rkj@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Richard Jensen](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=rkj).

## Classification 

Decide which class a particular pattern belongs to on the basis of a set of measurements. 

> The data tells use something about the patterns for each class. 

We need to construct a classifier from the training data that will tell us about a previously unseen pattern. 

> Uses a distance measurement, a Euclidean distance measurements is common. 

### Applications of Classification 

- Disease diagnosis
    - $x$ - Properties of patients. 
    - $f$ - Disease (or recommended therapy).
- Face Regognition 
    - $x$ - Picture of person's face. 
    - $f$ - Name/identity of person.

A dataset of Iris plant images is commonly used in AI/ML research. 

## Instance Based Learning 

A method of solving tasks by approximating discrete/real-valued target functions. 

You start with training data points (instances/objects):

$(X_n, f(X_n)), n=1...N$

## Nearest Neighbour Algorithm (K Nearest Neighbour Classifier)

1-NN: Given a test instance, $X_m$:

- Locate the nearest training instance $X_n$.
- Then assign $f(X_m):=f(X_n)$. 

K-NN: Given a test instance, $X_m$:

- First locate the $k$ nearest training instances.
- If the target function is discrete then take a vote among its $k$ nearest neighbours (classifiction).
- Else take the mean of the $f$ values of the $k$  neighbours (prediction).

For this to work we need a measurement between two points.
- For each column take the difference of the two values across the instances, square it and then add it to the next column in the data set. 
- Take the square root of the sum. 
- If the values are the same, the distance is 0. 

Neighbourhood size is centered on the parameter, $k$, the system is currently evaluating:

Parameter $k$ is set with a degree of caution. 
- If param, $k$, is small, say 1, the classification is augmented by the class $k$ is closest too, even if there are the same amount of different classes (1 square, 1 triangle).
- If param, $k$, is too large, you're averaging over the whole dataset, not deriving any classificaiton (only using the classes that are best represented).

### Theoretical Considerations 

### When should we consider using the $k$ - NN Classifier? 
Do you have: 

- No more than 20 features. 
    - Euclidean distance performance is the constraint. 
    - Distance measurements become less effective beyond this number of features. 
- Have lots of train data available to you? 

#### The advantage of the $k$ - NN Classifier: 

- Training is fast. 
- Complex target functions can be learnt. 
- Information is not lost. 
- Outliers can be handled sufficinetly well (if $K$ is sufficiently high). 

#### Disadvantages

- Have to calculate the distance from the test instance to every instance in the set, therefore there is a large computational overhead.

### Distance-weighted $k$ - NN
We can weight nearest neighbours more heavily. 

### Real Value Classes 

- There are many situations where we don't want a "Yes/No" answer, rather a real number value. 

