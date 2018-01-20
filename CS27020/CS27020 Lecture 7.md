# CS27020 Lecture 7 - Normalisation
__Monday, October 16th 2017__  
Lecture: ara11@aber.ac.uk   
Notes: ela12@aber.ac.uk

## Normalisation of Data

But first, a short recap on keys... 

### Recap on Keys 

- A key is a determinant that univocally identifies a record. 
- A key can be composite that can be defined by more than one attribute. 
- To decide if it's a key we need to know the context of the problem. 
	- There can be determinants that aren't keys - they determine other attributes but no a 		single tuple. 

Super Key &rightarrow; Candidate Key &rightarrow; Primary Key

- Super Key: One or more attributes that uniquey determines/identifies a row (record/tuple) in a table. A superkey are the most general types of keys. 
- Candidate Key: A key that cannot be reduced - the minimal superkeys. Minimal in this context _does not_ mean smallest in size. Minimaal means that you can't lose any attribute without losing uniqueness. 
- Primary Key: A candidate key selected by the database designer: it cannot be NULL. If it is a composite primary key, no single attribute can be NULL. On a list of DB attributes, the primary key will usually be underlined. 
> Sometimes, the primary key is abbreviated to 'key' - this is incredibly sloppy. 

- Surrogate Key: a ket with no meaning to the DB entity - it could be an automatically generated sequence key. Keys that pertain to the data of the DB entity are called Natural Keys. 
	- Use a SK instead of a NK when you don't want the key to have meaning. 

- Foreign Key: a primary key on another 'table' (relation). It refers to another tuple in another relation. It represents a relationship - it can be part of a composite key. 

### Normalisation

Just like ER modelling, Normalisation is a database design technique.

Normalisation is a procedure to derive the optimal set of relations through the use of a series of tests (normal forms). It removes unwanted redundancy of data. It splits a relation into smaller relations if violations of the normal form are found. 

Edgar Codd devloped the normal forms around 50 years ago:

- UNF: Unnormalised form.
- 1NF: Third Normal Form
- 2NF: Second Normal Form
- 3NF: Third Normal Form
- BCNF: Boyce-Codd Normal Form
- 4NF: Fourth Normal Form
- 5NF: Fifth Normal Form
 
Each normal form builds upon the previous normal form &therefore; the third normal form is in the second normal form, which in turn is in the first normal form. 

#### Getting to Normalisation

Analysis of requirements: 

- Interview the client 
- Collecting existing reports 

Design the DB: 
- The preferable phase for normalisation. 

##### An Example Problem

Spec: AU wants to record the piece of every equipment assigned to staff. Each piece of equipment has a serial number. 

#### First Normal Form 

- Break the non-atomic field (or repeating groups) into a separate table. 
- The new table takes a copy of the original table's primary key. 

 