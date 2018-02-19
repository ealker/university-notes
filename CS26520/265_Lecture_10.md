# CS26520 Lecture 10
## Fuzzy Logic
__Monday, February 19th 2018__  
Lecture: rkj@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Richard Jensen](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=rkj).

Question: How many grains of sand make a pile? You could guess a million grains, and then remove a grain one by one until you reach a threshold where 
the grains don't make a pile anymore, although this could be an atrbitrary number.

Learning outcomes: 

- Explain the function and use of fuzzy logic. 
    - Learn about fuzzy sets and memberships.
    - Learn about fuzzy rules.
    - Learn about fuzzy rule-based systems.
    - Learn how to apply these to new problems. 

### Towards Fuzzy Logic

Fuzzy logic applications: 

- Home appliances - washing machines, dishwashers, rice cookers. 
- Vehicle subsystems - ABS, transmissions.
- Data Mining 
- Video game AI 

Traditional logic: 

- True vs False. 
    - A ^ B = C 
    - A, B, and C are only ever true (1) or false (0).
    
- Since the foundation of logic (greeks) there has been the thought that the world isn't black and white. 
- Reality is "fuzzy". For example, language isn't precise.
    - How "hot" is hot? 30 degrees? 40 degrees? 
    - When we burn our hands, we don't say "Ow! That was 80.56 Centigrade" 
- There is a lot of uncertainty: 
    - Quantum level, everything is uncertain : Schrodingers cat. 
    - Atoms aren't unique. 

#### Definitions 

- **Crisp Variables**
    - Represent precise quantities. 
    - x = 2.89
    - The set A contains elements {0,1,2}. 

- A proposition in logic is either True or False. 
    - A ^ B = C
    - Richard is either greedy or not greedy. 

What happens in the case that Richard is not either totally greedy or not at all greedy? What if Richard is somewhat greedy? 

- Fuzzy sets can represent the degree to which a quality is possessed. 
    - Sets have values in the range of [0,1]
    - Greedy(Richard) = 0.7


### What is fuzzy logic? 

A type of logic that recognises more than sumple true and false values. Propositions can be represented with degrees of truthfulness and falsehood. 

#### More Definitions 

- **Universe of discourse:**
    - A universe - the range of values a variable can take. 
    - It varies upon the context of the problem, and the values used are whatever is appropriate for the application. 

- **Membership Functions, &mu; :**
    - For any fuzzy set A accossiates each element, x, with a membership value in [0,1]

- Fuzzy Variables: 
    - Fuzzy lingustic variables are used to represent concepts spanning a particular spectrum/range. 

N.B. Elements can belong to more than one set at a time. 

### Member Functions 

#### Trapezoidal Membership Functions

- LH Trapezoid
    - Case
    - Case

- Regular Trapezoid 
    - Case
    - Case 
    - Case

- RH Trapezoid 
    - Case
    - Case
    - Case


### Alternative Representation 

- Fuzzy sets can also be represented in a vector notation. 
- Useful for discrete rather than real-valued universes. 