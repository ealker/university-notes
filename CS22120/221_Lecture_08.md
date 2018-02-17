# CS22120 Lecture 8 - Documenting Your Design 

Friday February 17th 2018   
Lecturer: Chris Price     
Notes: Elliot Alker 

What makes a good design?  
How do we express a good design so that others can understand it? 

## Why do we produce a design document? 

- A design document allows the group to make firm decisions about what we are going to build. 

- Allows us to be able to agree that we are happy on the decisions we have made. 

- Show that we have a suitable mechanism for acheieving the requirements. 

- Allows the group to develop the product in parallel. 

- To enable testers to get on with plannign the testing - testing can and usually does inform design. 

## What is good design? 

[Good Desing - Dieter Rams](https://www.vitsoe.com/gb/about/good-design)  
[Simplicity - Jonathan Ive](https://www.youtube.com/watch?v=1jdPKi5i030)

The design of a piece of software should only be as complex as it needs to be.   
N.B - You need to be twice as clever to debug something as to build it. 

It needs to have high coherence (cohesion) within components and low coupling between its components (especially in OOP). In relation to high coherence, it needs to be able to perform frequent operations easily. 

A design should use what we as software engineers already know about good process - it should use the appropriate design patterns. 

## What does a good design document look like? 

"It should..." 

- Provide the "why" - why the system is implemented the way it is and provides a context and understanding of the design to the reader. 

- Breaks the design into its parts - the components (classes and objects). 

- Clearly show the interactions between different system components - where the interactions are and why they are nescessary. 

- Reflect the design decisions that had to be made - shows the though processes behind the difficult/risky parts of the implementation. 

The document should provide details on the overall architecture of the system as well as the detailed design of the components. The architectural section should be easy for a non-technical customer to interpret, provide and overall structure to the system's design and show how the system "fits together". 

The detailed design should show the classes, methods and algorithms used. It should provide the detail needed for independent development of system components and should generally not be an overview of the "big picture", rather an explination of the individual "pieces" of the system that need to work together. 

It should contain UML diagrams, more specifically: 

- Structual UML diagrams: 
    - Class Diagram 
    - Object Diagram 
    - Component Diagram 

- Behvaioural UML diagrams: 
    - Sequence Diagram 
    - Statechart Diagram

## General Design Questions 

- What are the Use Cases/Scenarios for your project?

- What are the ‘objects’ for your project?

- What is the information (data) held in each class?

- How do the classes relate to each other?

- What operations happen on each class?
    - Does the design cover all of the system? 
    - Does it meet requirements?
    - Does it support all features and functions?
    - Does it meet all the constraints. 

- Does the design have high cohesion / low coupling

- Is the design understandable /maintainable?