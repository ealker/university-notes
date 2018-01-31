# CS26520 Lecture 1
## Introduction to Artificial Intelligence
__Monday, January 29th 2018__  
Lecture: rkj@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off of the course notes provided by [Dr. Richard Jensen](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=rkj).

### General Module Information 

#### Composition: 

200 hours of work is required to do well on this module.

 - 1 hour lecture x 28 = 28 hours. 
 - Remaining 172 hours:
	- Fleshing out notes.
	- Working at home on Blackboard exercises.
	- Background reading.
        
#### Lecture Content: 

- Introduction (1hr) – Richard
- Knowledge representation and logic (6hrs) – Myra
- Fuzzy logic (4hrs) – Richard
- Current research in AI (1hr) – experts in the department 
- Search (6hrs) – Myra
- Evolutionary algorithms and swarms (3hrs) – Myra
- Data mining (5hrs) – Richard
- Revision lecture – Richard, Myra

#### Assessment: 

- 40% Practicals 
- 60% Written Examination - 2 hours.

#### Tips: 

- Attending lectures and practicals is not enough to do well on the module. Similarly, just looking at slides is not enough to get to grips with the content - they provide a base for discussion in lectures. 
- Read the textbooks. 

#### [Reading List](http://aspire.aber.ac.uk/lists/2112AB1F-49E1-2046-471A-2A1A12B94B5F.html)

- "Artificial Intelligence: A Modern Approach" - Russell, S. & Norvig, P. ISBN 9781292024202
- "Prolog programming for artificial intelligence" - Bratko, I. ISBN 0201403757

### What is Artificial Intelligence? 

- “Artificial Intelligence (AI) is the part of CS concerned with **designing intelligent computer systems**, that is, systems that exhibit characteristics we associate with intelligence in **human** behaviour – understanding language, learning, reasoning, solving problems, and so on” (Barr & Feigenbaum, 1981)

- “The branch of computer science that is concerned with the **automation of intelligent behaviour”** (Luger and Stubblefield, 1993)

- “The **study of the computations** that make it possible to perceive, reason, and act” (Winston, 1992)

It's difficult to reach a universal definition of AI. It's more practical to consider the following research/design/manufacturing disciplines that AI research uses:

- Studying intelligent entities by learning more aobut ourselves as humans as well as animals. 

- Building such intelligent entities - creating 'things' that exhibit 'intelligence'.

- Studying constructed intelligent entities - AI creations are interesting in their own right, independent from studying intelligent entities. 

The goals of AI research can be split into two broad categories: 

- Scientific: To determine which ideas about knowlesge representation, learning, rule systems, searching techniques, etc., explain various sorts of 'real' intelligence.

- Engineering: Applying AI to solve 'real world' problems. This involves the application of knowledge representation, learning, rule systems, searching techniques, etc. 


### Problems in AI 

Problems that we want to solve using artificial intelligence can be split into the following categories: 

- Formal Tasks: games (board/card), puzzles, mathematical and logic problems. 
- Expert Tasks: medical diagnosis, engineering, scheduling, computer hardware design. 
- Mundane Tasks: speech, writing, perception, walking, handling. 

We want AI systems to do various things; to plan and reason about the world in which they exist, to understand natural language, to perform optimisations, to control machines (self-driving cars), etc.

#### History of AI and Games

AI systems have a track record of performing well when playing "classic" games such Chess, Noughts and Crosses, Backgammon, Scrabble, Bridge. 

Due to the rapid advancement of AI in the 1950s, Newell and Simon predicted that a computer would be the world chess champion wihin 10 years. This goal was actually accomplished more than 30 years later than predicted in 1997 by the Deep Blue system. Simon reflected on his early prediction in his memoirs and stated that "there was no way to do it with machines that were as slow as the ones way back then."

Recently, it has become increasingly apparent that AI can have advantageous applications in a wide variety of computer games, for example in strategy/tactical/combat games (Forza, F.E.A.R). AI can be used for procedural content generation (Minecraft, Left4Dead, Far Cry 2) and artificial life generation (Creatures, Spore).

AI in games use various techniques: 
- Pathfinding/Search - for AI bots to move throughout the map.
- Genetic Algorithms 
- Fuzzy Logic - where AI bots try to emulate human decision making.
- Agents/Logic
- Data Mining - for games companies to optimise game play and maximise user playing time. 

### Applications of AI Techniques

- Knowledge Representation: Representing the world and reasoning in that context.
- Search: Generating possibilities, finding best solutions.
- Evolutionary Search & Optimisation: Solving **very* difficult (usually) industrial problems.
- Data Mining: Discovering knowledge/insights from raw data sets.  


### Approaches to AI 

AI is **not** the emulation of conscious beings. There are various approaches to creating AI systems:

- 'Thinking' or Acting (Behaviour)
- Human or Rationality (Doing the **'right'** thing)

This creates a matrix to examine when approaching the design of an AI system:  
|                                                    |                                       |     |
| -------------------------------------------------- | ------------------------------------- | --- |
| Systems that **think** like humans (cognitive science) | Systems that **think** rationally (logic) |     |
| Systems that **act** like humans (c.f. Turing test)    | Systems that **act** rationally (agents)  |     |
|                                                    |                                       |     |                                                               


#### Strong vs Weak AI

There is an ongoing debate about whether AI can truly reason and solve problems. 
Proponents of the argument that AI is "strong" believe that machines can actually **think** intelligently. Proponents of the converse belive AI to be "weak"; machines can **act** intelligently.

Variations of the debate discuss whether something can be truly intelligent without sentience or a form of a "soul". Again, the goal of AI is not to create sentient beings, rather it is to create an artificial intelligence. 

John Searle:
- “...according to strong AI, the computer is not merely a tool in the study of
the mind; rather, the appropriately programmed computer really is a mind”  

- “...according to strong AI, the correct simulation really is a mind.
According to weak AI, the correct simulation is a model of the mind”

As we can see, it is difficult to define what "intelligence" actually is, therefore it is difficult to determine if a program/system truly is "intelligent". There are, however, tests, the most famous of which is the turing test.

##### Turing Test 
The turing test is explained [here](http://www.psych.toronto.edu/users/reingold/courses/ai/turing.html). 

A turing test requires the system to implement:

- Natural Language Processing: to enable successful communication with the interogator. 
- Knowledge Representaiton: to have a base of knowlesge and to store information provided during the interrogation. 
- Automated Reasoning: to use stored information to answer questions and to draw conclusions from the information. 
- Machine Learning: to adapt to new, unforseen circumstances and to detect and extrapolate patterns of conversation. 

The turing test is not without its flaws - it focuses on duplicating intelligence, rahter than studying the principles of intelligence. The latter is of more importance to most AI researches. 

A rather compelling analogy can be used to explain why most AI researchers devote such little time to passing the turing test: 

When humans sought to create aeroplanes, scientists and engineers worked to immitate the flight behaviour of birds. This proved unsuccessful. They discovered the principles of aerodynamics, and created machines capable of flight. The lesson is that once people stopped imitating what they already saw in nature and learnt the priciples behind how the natural entity worked, they were successful in creating a machine that generate the same outcome, the ability to fly. 

Aeronautical engineering does not define its goal as making "machines that fly so exactly like pigeons that they can fool even other pigeons" - this is the equivalent to what the turing test measures. 

##### Chinese Room

The Consortium of Cognitive Science Instruction has a good [page](http://www.mind.ilstu.edu/curriculum/searle_chinese_room/searle_chinese_room.php) about Searle's 'Chinese Room' test. 

Stanford also has a good [page](https://plato.stanford.edu/entries/chinese-room/#3) on the Chinese Room test.

Even though the "person" inside the box doesn't speak chinese and can only translate  characters to others to form an output, this could be symolic of what humans do in their brains - run consecutive calculations on inputs to create outputs, much like a CPU. 

#### Ethics and AI 
We can develop AI, should we? The problems that AI poses:
- People might lose jobs to automation
- People might have too much/little leisure time
- Loss of accountability – who’s to blame if things go wrong? 
- Success of AI might mean end of human race!
	- Almost any technology has the potential to cause harm in the wrong hands.

Donald Trump's choice for Labor Secretary (Andrew Puzder) is a big fan of automation:

- "They're always polite, they always upsell, they never take a vacation, they never show up late, there's never a slip-and-fall, or an age-, sex-, or race-discrimination case.” 

What does this mean for the US job market, and indeed the world market? 
In Wales, by 2030, it is predicted that 112,000 people will have lost their jobs to AI. 2030 to 2018 is the same time as 2006 to 2018 - have sufficient safeguards/will sufficient safeguards be put in place? 
  
