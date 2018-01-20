#CS21120 Lecture 8 - The Priority Queue ADT: An Implementation

Thursday, October 19th 2017  
Lecture: c.zarges@aber.ac.uk  
Notes: ela12@aber.ac.uk

## Array based implementation

### Unsorted array implementation 

- `insert`: efficient - place the element to the end of the array. &theta; (1). 
- `removeMin`: You have to do a linear search and then remove the entry. O(_n_).
- `min`: You have to do a linear search. 0(n).

### Sorted array implementation (circular array, increasing orer) 

- `insert`: binary search O(log _n_ ), then move everything to the right, &therefore; O(_n_).
- `removeMin`: remove the first entry &theta;(1)
- `min`: return the first entry &theta;(1).

## List Based Implementation 

### Unsorted list implementation 

Using a doubly linked list. 

- `insert`: add to the end of the list.&theta;(1)
- `removeMin`: linear search O(_n_)
- `min`: Linear search O(_n_)

### Sorted
There are no index numbers in a list, so you cannot use binary search.

-`insert`: linear search. O(_n_).   
-`removeMin`: remove the first entry &theta;(1).   
- `min`: return the first entry &theta;(1).

These are not very efficient methods of implementing a priorty queue abstract data type. 

## Towards and efficient implementation 

Idea: Use the structure of a binary tree to find a compromise between entires being entierly unsorted and perfectly sorted. 

We can use **heaps**, with a `min variant`. 

This will allow us to perform insertions and removals in logarithmic time (better than linear time, not as good as constant time). 

### Revision: Max Heap 

A binary tree satisfying two constraints: 

- It is a full binary tree. 
- Each child hasa key smaller than or equal to its parents. 

Full in this context: _every level is fully occupied above the lowest level and the nodes on the lowest level are all to the left._

### Min Heaps 

A binary tree satisfying two constraints: 

- It is a complete tree.
- Each child has a value greater than or equal to its parent. 

The minimal key is at the root of the heap. Keys on a path from the root to a leaf are nondecreasing. 