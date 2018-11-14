# CS22120 Lecture 16
## Software Maintenance

"The process of changing a software system after it has been accepted and in use."

**Friday, March 23rd 2018**  
Lecture: cjp@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off the course notes provided by [Prof. Chris Price](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=cjp).

# 

### Introduction

It is estimated that maintenance accounts for 50% to 70% of the effort involved in the software lifcyle of a commerical system. The type of maintenance a project requires can be categorised as follows: 

- **Adaptive:** Modifying software due to environmental changes. 
- **Corrective:** Diagnosis and error correction.
- **Perfective:** Addition of new features & improvement of system functionality.
- **Preventative:** Defensive rewriting & refactoring of code. 

### Cost 

It is expensive to add functionality to a system once that system has shipped. The cost of perfective maintenance is uually much greater than providing similar functionality when the product is first developed. Factors that contribute to this are: 

- Expense of brining in experiences staff and training them up to a working knowledge of the system. 
- Legacy systems were developed before modern software engineering techniques were developed or put into practice. 
- Often additions to code introduce new faults to a previously working system.
- As new code is written, the strucutre of the codebase may degrade. 
- Links (physical or otherwise) are lost between the system and its associated documentaiton. 

### Cost Reduction Methods 

It is essential to keep the initial system design simple and efficient. The best way to reduce the possibility of expensive future maintenance is to consider maintainence in the system's inital design. 

Maintaining system documentation is also important. Ideally a maintenance guide would contain the following:

- Rebuilding information - code, test and makefile locations.
- Examplesofchanges that might be needed.
- Evolution thoughts.
- Error codes and their explanations.

Ideally, the system would also have a robust requirement specification, design overview and test reports. 
Furthermore, [regression tests](https://en.wikipedia.org/wiki/Regression_testing) during maintenance ensure that no system functionality is lost as the code is improved. 

### Handling Maintenance 

Change Requests &rightarrow; Recording/Evaluation &rightarrow; Action

- Change Requrest: issues are raised by developers in a problem report form. 
- Recording & Evaluation: the issue is logged, and is assigned a priorty:
    - not a problem  
    - not our problem  
    - our problem (no action to be taken)  
    - our problem (no action until future release)  
    - our problem (action now)  
- Action: a change request form is raised, resources are allocated to fixing the problem. The fix is tested, documentation is then updated, and the patch is released. 

### Change Control Process 
#### Paper Based

![Change Control Process](./221_img/changecontrol.png)
Image from Chris Price. 

#### Modern Approach 

The paper based system previously described is an outdated approach to change control. A modern approach favours collaborative tools such as Git, an interface for Git like GitLab or Github, and bugtrackers like MantisDB.  

### Refactoring 

Refactoring is often about making small changes to code, such as renaming methods, moving fields from one class to another, and combining small classes into a superclass with multiple methods. 

- Reduces the short term need to design the system. 
- Makes software easier to maintain. 
- Import not to update functionality at the same time. Functions, methods, subroutines could break. 

Refactoring is best completed when you can’t figure out how the code works, and should be completed in short, test driven steps. It is also crucial if your code smells bad. 

### Code Smells   

A "code smell" is an example of "bad code" within a system that can be emblematic of a larger problem. Often, "bad" code is technically correct and will compile/run, however it demonstrates a weakness in the design and architecure of a software system. 

There are many types of "code smells": 

- Long Methods: Robert C. Martin says that "Functions should hardly ever be 20 lines long." 
- Code Duplication: if code is duplicated, the developer(s) may not have [factored](https://en.wikipedia.org/wiki/Decomposition_(computer_science)) the problem correctly. 
- Large classes: in [SOLID](https://en.wikipedia.org/wiki/SOLID) design thinking, the [Single Responsibility Principle](https://en.wikipedia.org/wiki/Single_responsibility_principle) states that classes should only encapsulate a single part of the system's functionality. Large classes with lots of conditional code are prime examples of bad Object Oriented Programming practice.
- Comments: bad comments that describe "what" instead of "why" demonstrate a fundamental lack of understanding on the developer's part. 

More examples of bad code smells can be found on [Coding Horror](https://blog.codinghorror.com/code-smells/) and at [Mika Mantyla's site](http://mikamantyla.eu/BadCodeSmellsTaxonomy.html).