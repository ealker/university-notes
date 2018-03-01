# CS26520 Lecture 2
## Introduction to Knowledge Representation
__Monday, January 29th 2018__  
Lecture: rkj@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Myra Wilson](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=mxw).

"Yu, shall I teach you what knowledge is? When you know a thing, to recognize that you know it and when you do not know a thing, to recognize that you do not know it. That is knowledge.”
-- Confucius

## What is knowledge? 

Knowledge is built up from the following parts. 

- Symbols &rightarrow; Data
- Structure &rightarrow; Information 
- Inference &rightarrow; Knowledge

### Data 

Data can be described as "sets of symbols". These symbols have no inherent meaning assigned to them, rather meaning is assigned to the symbols by the agent using it. Data can be stored and represented in ASCII in computer systems, but once you move the abstractions you realise that each word is made of a character, and each character is just a collection of pixels displayed on a screen. 

Example: 

Singapore London 12.35 QF32. 

### Information 

Information can be described as structured data. It is structured in a way so that it is meaningful to the agent using it. 

Example: 

Flight QF32 leaves London for Singapore at 12.35. 

### Knowledge 

Knowledge builds on the ideas of data and information - knowledge allows the agent to make inferences from information that are not explicitely stated in the information. 

Example: 

The knowledge base: 
Flight QF32 leaves for Singapore at 12.00 GMT.
The flight takes 8 hours.

The inference: 
Therefore flight QF32 will arrive in Singapore at 20.00 GM 


Whilst individual data (facts) have some meaning to the agent, a set of facts contain truths about the world. An agent can represent these facts as either: 

- Internal descriptions
- Models of states and events 

## Types of Knowledge 

- Performance knowledge:
    - Skills, control
    - Unconscious, non-verbal, dynamic
        - talking, walking etc

- Declarative knowledge:
    - Facts, static, conscious
        - The capital of  France is Paris
        - Grass is green (except when it's brown...?)

## What is Knowledge Representation?

The model for representing information about real problems in a way such that: 

- Sufficient information about the problem is captured. 
- Information is captured in such a way that we can manipulate it using a computer system. 

A basic system would have a large knowledge base, and would apply this knowledge to form a solution dependent on a particular problem. 

## Type of Knowledge Representation 

[Definitions](http://www.ai.rug.nl/~lambert/projects/miami/taxonomy/node99.html) for the types of knowledge representation.

- Symbolic: "Classic AI" - representation system in which atomic constituents of representations are reputations themselves. This system has a compositional syntax and semantics. 

    - Input symbols &rightarrow; symbolic processor &rightarrow; output symbols.
    - The symbolic processor transforms information by using logical rules. 

- Sub-Symbolic: Follows the metaphor of the human brain, drawing on knowledge of neuroscience. Consituent entities are not representations.

    - Input pulses (strings) &rightarrow; neurons &rightarrow; neutrons (output pulses as strings).

## Knowlesge Representation Questions

The task of computer scientists is to therefore find representations which are appropriate for a given problem. 

Questions to ask when trying to solve a problem:
- What precisely is the problem I want to solve? 
- What information is pertinent?
- What level of representation will be useful? 
- What are the symbols likely to be?
- What operations on those symbols are needed?

We therefore need syntax and semantics with which to tackle the problem we are trying to solve.

## Modelling Knowledge Representation (Characteristics)

Our method of knowledge representation therfore needs to be both **expressive** and **efficient**. 

Expressive, in that our sentences are sufficiently precise, clear, and complete.
Efficient, in that the way we model the problem is suitable for computation. 

So what languages/methods can we use when modelling our problems? What follows are possible contenders. Our solution will be a trade-off between expressivness and efficiency. 

### Natural Language 

- Languages such as English, Welsh, Chinese, etc.
- Could we use natural language for knowledge representation? 

- Advantages:
    - Extremely expressive.
    - Most humans use them to represent knowledge (text books etc).
- Disadvantages:    
    - Syntax and semantics are very complex.
    - Little uniformity in sentence structure.
    - Ambiguous.

### Databases

- Database solutions are great at storing & retrieving data, however it is represented (ASCII for example). 
- They're easy to use, but they're not very flexible. 
- They follow a model to store data - usually the relational data model but other solutions like NoSQL exist and are useful for different applications. 
- Links in between data produce information (structured data useful to the agent). 
- Representing data is easy, representing knowledge is hard.

- Could we use databases for knowledge representation? 

- Advantages:
    - Efficiently represent and process large amounts of data
    - Can build on traditional database systems
- Disadvantages:
    - Only simple aspects of the problem domain can be accommodated
    - Can represent entities and relationships, but not much more
    - Reasoning is very simplified – need something more sophisticated

## Final Thoughts 

Think about some computer program you know well:  
 - When the computer is running, what does the system “know”
 - What knowledge about the application is contained in the program?
 - How much does the computer/program appear to “understand” when it is operating?
 - Think about how you could represent a computer chess game?

- Knowledge Representation affects the time and space required to get an answer to a given problem
- All programs languages can encapsulate knowledge:
    - Java
    - Prolog (later)