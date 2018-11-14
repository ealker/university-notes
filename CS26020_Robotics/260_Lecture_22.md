# CS26020 Lecture 22
## Hybrid Systems
__Friday, March 22nd 2018__  
Lecture: mxw@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Myra Wilson](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=mxw).


Hybrid Architectures 

- Goal oriented deliberative systems. 
- Reactive systems that can deal with an ever changing world. 
- Usually implemented as a deliberative system with an interface to a reactive system. 
- It creates a plan based on knowledge, but then can use reactive side to be reponsive to the changing environment. 

Hybird Interfaces 

- A framework mediates between the reactive and deliberative system's control over the actuators. 
- Each systems can use knowledge from the other, but a supervisor controls both. 
- Deliveratie system provides information which directs the behaviour of the reactive system.

Example

AuRA - R. Arkin 

Two components, reactive and deliberative. 

Each behaviour represented as a schema, essentially a equation. 
Work together to produce the emergent behaviour. 
Each behaviour has a vector (calculated from sensor information) which represents the magnitude and 
the direction of each behaviour.

