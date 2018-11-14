# CS26520 Lecture 3
## Knowledge Representation & Logic 
__Friday, February 2nd 2018__  
Lecture: mxw@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Myra Wilson](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=mxw).

## Knowledge Based Systems
Choosing a suitable method for knowledge representations is the foundation of the larger goal of building a knowledge based system. This system shold: 

- Accept new tasks in the form of explicitly described goals.
- Achieve competence quickly by being told or learning new knowledge about the environment.
- Adapt to changes by updating relevant knowledge.

Now that the motivation for knowledge representation is clear, we should look to develop a language for knowledge representation.

## Towards a Language for Knowledge Representation

There are two key aspects in developing a language for KR:

 - Semantics: The facts in the world to which sentences in the language refer.
 - Syntax: The intricate legalities of the language. 

 Reasoning in a KBS involves the generation and manipulation of symbols. 

## Knowledge Representation Schemes 

### Declarative Schemes 

- Logic
    - Propositional Logic (Boolean Logic)
        - Built from propositions.
        - Each proposition is either true or false.
        - Compositionality: truth value is dependent on consituent parts and operators. 
    - First Order Logic (First Order Predicate Calculus)
        - More flexible than propositional logic.
        - Built up from objections and their relationships.
        - Has functions - relations which accept inputs and give a singular output.

- Semantic Networks 
    - Nodes that denotes concepts or objects.
    - Links between the nodes that denote object relations.
    - Link labels that denote specific relations.
    - Consists of an object and semantic associations between objects.

### Imperative Schemes

- Procedural Languages 
    - Describe a series of events which will bring about a desired state of affairs. 
    - They describe _how_ something is to be done, rather than truth of the action to be performed. 
    - Procedural languages are effective at representing temporal information. 
    - It is difficult to separate factual data from the code of the program. 
- Recipes 
    - The same semantics that procedural languages implement, but in a natural language like English or Welsh.   

Example:

1) Place butter in a saucepan.  
2) Wait until the butter has melted.  
3) Add flour to pan.  
4) Remove from heat.  
5) Stir until a smooth paste is formed.
 
### Mixed Schemes

- Frames
    - A frame is a collection of declarative and procedural knowledge relating to a particular entity.
    - Slots can be filled by default, calculated, or inherited.
    - Contains procedural knowledge.

- Production Systems
    - Also called rule-based systems.
    - Experts supply the knowledge for a particular problem.
    - Knowledge is represented in the form of rules.
    - Temporary data and variables are stored in working memory.
    - Follows the process: 
        - IF condition THEN action.
    - Conditions can be simple or complex statements. 
    - Actions can do one of the following four processes:
        - Assert data into working memory.
        - Remove data from working memory.
        - Alter values in working memory.
        - Send messages to user/external system.
    
#### A Note on Production Systems and Rule Firing

- When a rule with matching conditions is found, the action part of the rule is executed.
- Called firing the rule.
- Forward chaining.
- Some conflict resolution may be involved.
- Control flow is not sequential, unlike procedural languages.

## Pros & Cons of Knowledge Representation Schemes

- Logic
    - Pros
        - Well established theoretical foundations, with simple, economical notation based on mathematical logic. 
        - Well suited to describing passive, declarative knowledge.
        - Inference mechanisms allow information retrieval and problem solving.
        - Inference mechanisms are well understood and simple to implement.
    - Cons 
        - Difficult to represent temporal, heuristic, and uncertain knowledge using logic.
        - Large knowledge bases must be well organised to be efficient, as every item in the knowledge base may be examined.
        - It is difficult to represent procedural knowledge using logic.
        - Difficult to represent heuristics or time knowledge.
        - As with all symbolic schemes, programs can seem more intelligent than they really are.

- Semantic Networks
    - Pros 
        - The formal theory makes semantic networks easy to understand. 
        - This is made easier still with graphic visualisations.
        - Elements that are related will appear next to teach other in the knowledge base which makes partitioning and contextual reasoning easier. 
        - Properties can be inherited from parent nodes - child classes can inherit from base class. 
    - Cons
        - Foundations and theory are not as well understood as those of logic.
        - Inheritance can cause problems - the [diamond problem](https://en.wikipedia.org/wiki/Multiple_inheritance#The_diamond_problem). 
        - Very difficult to represent temporal or procedural knowledge.
        - A special kind of representation would be needed to reproduce the rich semantics of logic. 

- Frames
    - Pros
        - Allows inheritance of properties. 
        - Allow the combination of procedural and declarative knowledge.
        - Inference can be guided by local links. 
    - Cons 
        - No formal theory unlike propositional logic and first order predicate calculus.
        - No history of changes to system.
        - No standards. 

- Production Systems 
    - Pros
        - Simple rule structure and inference engine.
        - Rules can be read backward to “explain” reasoning.
        - Allows declarative and imperative knowledge to be combined.
        - Data can be separated from control code.
    - Cons 
        - Forward chaining means predicting execution flow is very difficult (has implications for testing and reliability).
        - Constructing rule sets can be difficult.  


## Logic Terms 

The following terms are described in more detail in Chapter 7 of Russel & Norvig's _Artificial Intelligence: A Modern Approach_.

### Entailment 
- The relationship between a sentence and another sentence that follows from it. 
- &alpha; entails &beta; if and only if every model in which &alpha; is true, &beta; is also true. 
### Inference 
- An inference engine derives &alpha; from a knowledge base.
### Soundness 
- "An inference algorithm that derives only entailed sentences is called sound or truth preserving."
- It ensures that propositions that are false are only ever false, that is, that they cannot be proved to be true. 
- Inferences that are said to be "unsound" makes things up as it goes along. 
### Completeness 
- An inference algorithm is said to be complete if "it can derive any sentecne that is entailed." 
- There is a need for enough rules so that any true derivation can be proved.
### Grounding 
- "The connection between logical reasoning processes and the real environment in whih the agent exists."
- A reasonable question to ask is _"How do we know that the knowledge base is true in the real world?"_
    - Knowledge Base is just syntax inside the agent's mind. 
    - The agent's sensors connect the real world to the knowledge base.

