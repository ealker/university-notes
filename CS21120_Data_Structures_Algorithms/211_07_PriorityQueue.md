#CS21120 Lecture 7 - The Priority Queue ADT

Thursday, October 19th 2017  
Lecture: c.zarges@aber.ac.uk  
Notes: ela12@aber.ac.uk

## Priority Queue Abstract Data Type 

The queue is a nice theoretical abstract data type, however in the real world implementing queues as first in, first out is rather difficult. 

The priority queue ADT is a collection of _prioritised_ objects that allows arbitrary insertion of new objects and the removal of the objects that has first priority. 

We model an object and its priority as a key-value pair known as an entry. 

Any object that allos a meaningful omparison between any two instances can be used as the key. 

As a convention, an object with the minimal key will be removed next. 

You can have items with the same priority - in this case we can remove the object that was added first, or remove a random object. 

### Examples 

**Scheduling** - Jobs waiting for CPU time.

In this case - the value is the job information and the key is the priority assigned by the user. 

**Waiting List** - Standby passengers waiting for a flight. 

In this case - the value is the passenger information and the key is the priority which is determined by a list of criteria: e.g waiting time of the passenger, class of ticket, frequent flyer status. 

**Competition** - Participants waiting for their turn.

In this case - the value is the participant information and the key is their name. 

## The Entry Composite 

Define a class that allows us to pair a key _k_ and a value _v_ as a single object: 

```java
public interface Entry <K,V> {
	K getKey();
	V getValue();
}
```

## Comparing Keys 

We need to allow arbitrary objects that can be compared in a meaningful way. The results of the comparison must not be contradictory. 

### Total Order Relation 


