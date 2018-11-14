# CS26020 Lecture 20
## Reactive Systems, Part B
__Thursday, March 15th 2018__  
Lecture: mxw@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Myra Wilson](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=mxw).

## Braitenberg 

### Summary of Theory 

- Observered complxity in behavioural systems comes from environmental interaction rather than complexity of the brain. 
- Law of uphill analysis and downhill invention. 
    - We tend to overestimate a system's complexity. 
    - Neuroscience & cognitive science can combine the analysis of living brains with the construction of ebodied behavioural circuits. 

## Behaviour Based Architectures 

- Tight coupling of sensing and action. 
- Avoid representational symbolic knowledge - we don't need to reason and rationalise everything. 
- Decompose situations into contextually meaningul units - each agent should have a high level of competnence in a small area of the task to be completed. 

### Models and their Problems 

- Why bother with a model of the real world? 
    - The rel world is a complete model of itself anyway. 

### Individual Behaviours 

Each behaviour is built from augmented finite state machines. Both AFSMs and FSMs have inputs, outputs and are wired together with a ficed topology over low bandwidth communication lines (an advantage over high bandwidth deliberative systems). 

Augmented finite state machines have aded facilities including timing mechanisms (state changes can be delayed), as well as the ability  to hold internal data structures. 

### Types of BBAs 

#### Subsumption Architectures   

- [Prof. Rod Brooks](http://people.csail.mit.edu/brooks/index.html), MIT (1980 - )

- Tenants of Subsumption Architectures  
    - The world is its own best model.   
    - Against building world models/explicit symbolic representation reasoning.
    - Robots should be cheap/simple. 
    - Robustness is a design goal.
    - Onboard computation is vital. 
    - Systems are built incrementally.  


#### Action-Selection Architecture 
- Pattie Maes (1989)

#### Voting Architecture
- D. W. Payton (1986)

