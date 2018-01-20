#CS2720 Lecture 5 - Recap on the Relational Data Model 

Wednesday, October 11th 2017  
Lecture: hmd1@aber.ac.uk  
Notes: ela12@aber.ac.uk

## Database Theory Overview 

### History 

Normally, when we think about DBs, we think about rows, columns and tables in a database. In DB theory, we use the following terms:

+ Row &rightarrow; Tuples
+ Columns &rightarrow; Attributes
+ Tables &rightarrow; Relations

#### Specifying Relations

A database is a collection of relations, with tuples contraining attribute values that conform to the set domain. A relation has two parts: a schema and a body. The chema defines what can be put in the relation, and the body is the data itself. 

Key properties of relations (why relations are not tables):   

+ Tuples and attributes are unordered
+ there are no duplicate tuples (think set theory)
+ All attribute values are atomic - cannot be broken into smaller parts. 

### Keys 

We uniquely identify the data using keys. 

Super keys &rightarrow; Candidate Keys &rightarrow; Primary Key.

+ Super keys: the list of attirbutes that don't uniquely identify a tuple, but that you need to identify tuples.
+ Candidate keys: a subset of the super keys that are minimal.    
+ Primary key: an element selected within this set.

Relational keys allow us to specify __uniqueness__ within the RDM. Uniqueness is a property of the real-world that needs modelling. We need keys to reference/identify/query specific tuples (as mentioned before). Allows us to efnorce integrity constraints. 

### Data Integrity 

Two rules that apply to all instances of the DB: 

+ Entity Integrity: Ensure each tuple can be uniquely identified. 
+ Referential Integrity: Ensure data of one relation does not contradict the data of another relation. 

These integrity rules ensure that we can always identify a single tuple and do not refer to non-existent tuples. 

#### Entity Integrity 

+ Uniqueness - the primary key of a tuple is unique for that relation. 
+ No attribute of a primary key can be __null__. 

> In a DB, a null means that there is an _absence of data_. Useful for modelling uncertainity in DB theory. 

###### Foreign Keys 

These are ways of letting you reference data from one relation to another relation. 

#### Referential Integrity 

Referential integrityy ensures the DB does not hold any unmatched foreign keys. It should not be possible to create a record reffering to `personID 'G100'` unless there is already a record for `personID 'G100'`. 

When integrity is threatened: 

+ Restrict users from creating conflicts
+ Cascade deletes - things which refer to defunct tuple are also deleted.
+ Set references to NULL.

### Data Manipulation

The following are set theoretic operations.

#### Union 

#### Difference

#### Projection

#### Selection

#### Division


### Joins: A Recap

Joins are a way of making the Cartesian product useful.

#### Natural Join

The natural join is the joining of R1 and R2 over all common attributes. 

> Do a join on all columns which have the same name. You're doing a join ON something, but the contents of the ON clause are _implicit_.

#### Theta Join 

The Θ join defines a relation... etc...

> Θ join - there is a function, Θ, which specifies the criteria that you're joining on. You can join on a value being equal, or a value being less than, or a value being more than, etc. 

#### Directional Join 

