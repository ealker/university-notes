# CS21120 Lecture 14
__Friday, November 3rd 2017__  
Lecture: c.zarges@aber.ac.uk   
Notes: ela12@aber.ac.uk

## "Applications of the Map ADT" 

### Maps 

Comparing Hashing and Balanced Binary Search Trees 

- BBST  &rightarrow; _better worst case_.
- Hashing &rightarrow; _better expected case_.
- If worst-time complexity is _not_ important, use hashing. Otherwise, search trees may be more appropriate. 
- Hasing distribures data randomly across the hash table so the access pattern may cause caache misses. 
- Performance of hashing depends on the _hash function_ used and designing a good hash function may be difficult. 
- Evaluating a good hash function may be slower than a simple comparison used by AVL trees.

### Applications of Search Trees 

Applications not related to priority queues and maps: 

- File System Representation 
- Storing Arithmetic Expressions 
- Decision Trees (in AI)

There are different types of search trees for different types of applictions: 

- B Trees 
- Tries - dictionary - storing a letter per node and forming words out of them. 

### Applications of Maps 

Problem: System that maintains info. about events with unique **time stamps**, e.g. a financial transaction. 

Task: Get a list of all events ordered by the time at which they occour. 
Solution: `inOrder()` traversal of a search tree. 

Task: Search for an event that occurred closest to a particular time, often called an "inexact search". 
Solution: `inOrder()` traversal, gather all entries - expesnive in a computational time complexity context. 

### The Sorted Map Abstract Data Type 

`firstEntry()`: Returns an entry with the smallest key value (or `NULL` if map is entry). 
`lastEntry()`: Returns entry with the largest key value (or `NULL` if map is entry).   
.  
.  
.  
Some more stuff.

Problem: Spell Checker.  

Task: For a word input decide if it is written correctly, if it is contained in a provided dictionary. 
Model this as a key-value entry. 

### Summary: Abstract Data Types

Four reasons why compscis should know about ADTs and their implementations: 

- 

