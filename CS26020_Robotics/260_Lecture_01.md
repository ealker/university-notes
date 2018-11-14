# CS26020 Lecture 1
## Introduction to Robotics and Embedded Systems
__Monday, January 29th 2018__  
Lecture: mxw@aber.ac.uk   
Notes: ela12@aber.ac.uk

### General Module Information 

Lecturers:

- Myra Wilson 
- Fred Labrosse 	 
- Laurence Tyler 

Composition: 

 - 2 hour practical x 10 = 20 hours. 
 - 1 hour lecture x 24 = 24 hours. 
 - Remaining 156 hours:
	- Working in ISL (Intelligent Systems Lab).
	- Working at home.
	- Background reading.
        
Lecture Content: 

 - Introduction - 2 (mxw)
 - Practicals Introduction – l (lgt)
 - Mobiles and Arms - 2 (mxw)
 - Embedded Systems – 6 (ffl)
 	- Microcontrollers, Embedded system components, Power, energy & batteries, Usage patterns, energy budgets, component selection
 - Practical FSM's – 1 (lgt)
 - Sensors and Perception - 4 (ffl)
 	– Sensors, properties, data, problems, Environment modelling, Sensor fusion,
 	Kalman filters, SLAM
 - Robot Control Architectures – 8 (mxw)
 	- Reactive, Deliberative, Hybrid

Assessment: 

- 50% Practicals 
- 50% Written Examination

Tips: 

- Attending lectures and practicals is not enough to do well on the module. Similarly, just looking at slides is not enough to get to grips with the content - they provide a base for discussion in lectures. 
- Do the practical worksheets and loads of independent research/play in your own time. 
- Read the textbooks. 

### [Reading List](http://aspire.aber.ac.uk/lists/DF6EABA1-E37C-6B63-CA0F-D47F19B0B12F.html)

Essential reading is "Introduction to AI Robotics" by Robin Murphy. ISBN 0-262-13383-0.

### Definitions 

From OED:   

 - Robot: “noun: a machine capable of carrying out a
	complex series of actions automatically, especially
	one programmable by a computer.”
	
This is quite a limited definition in that a modern toaster or washing machine could be considered a robot. As technology advances and evolves, the line between the classical image of a "robot" and now-common household technology has been blurred. 

McKerrow instead considers "robotics" as a discipline that encompasses the following: 

 - The design, manufacturing, and programming of robots. 
 - The use of robots to solve problems. 
 - The study of control processes, sensors, and algorithms found in human, animals and machines.
 	- Animals are particularly useful to study, as they have seemingly "simple" behaviours/actions that have evolved over thousands of years, and require dexterity and inherent knowledge to complete. 
 - The application of such processes and algorithms in the design of robots. 

 Etymology of "Robot"
 
 - From Czech "Robota", meaning labour or work. 
 - The term "Robot" was first used in K. Chapek's 1920 play Rossum's Universal Robots.
 - The term "Robotics" was used by the science fiction author Issac Asimov in his novels. He defined a series of laws known as Asimov's Laws for determining the behaviour of robots:
 	- 1st law: A robot may not injure a human being or, through
inaction, allow a human to be harmed.
	- 2nd law: A robot must obey orders given by humans
except when that conflicts with the First Law.
	- 3rd law: A robot must protect its own existence unless that
conflicts with the First or Second Laws.

### The State of Robotics (2018)

- We think of "robots" in classical terms - a humanoid machine that performs the actions that humans would normally perform, in a human-like way. For example, such a robot would hoover the carpets like a human would human carpets, holding the hoover in one hand and moving around with it. 

This is as much a design thought as it is a philosophical one: when designing robotic systems, we need to consider that the world is optimised for humans. Doors are human height, seats are human sized, roads fit human cars, etc. 

Companies that make robots have changed their priorities: 

Robot that hoovers a carpet using a vaccum cleaner &rightarrow; Robot that **is** the vaccum cleaner.

We've moved from wanting single autonomous robots that use a range of human tools, to creating robots that **are** the tools (although work to create humanoid robots persists). Consider a roomba for example - it performs a single, automated function (hoovering carpets). 

Robots in 2018 are generally **really** good at operating in consistent, specific environments. The challenge is to design and manufacture robots that perform well in a general environment. 


  

