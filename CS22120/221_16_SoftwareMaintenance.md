# CS22120 Lecture 16
## Software Maintenance

"The process of changing a software system after it has been accepted and in use."

__Friday, March 23rd 2018__  
Lecture: cjp@aber.ac.uk   
Notes: ela12@aber.ac.uk  

These notes are based off the course notes provided by [Prof. Chris Price](https://www.aber.ac.uk/en/cs/staff-list/staff_profiles/?staff_id=cjp).

# 

It is estimated that maintenance accounts for 50% to 70% of the effort involved in the software lifcyle of a commerical system. The type of maintenance a project requires can be categorised as follows: 

- Adaptive: Modifying software due to environmental changes. 
- Corrective: Diagnosis and error correction.
- Perfective: Addition of new features & improvement of system functionality.
- Preventative: Defensive rewriting & refactoring of code. 

## Cost 

It is expensive to add functionality to a system once that system has shipped. The cost of perfective maintenance is uually much greater than providing similar functionality when the product is first developed. Factors that contribute to this are: 

- Expense of brining in experiences staff and training them up to a working knowledge of the system. 
- Legacy systems were developed before modern software engineering techniques were developed or put into practice. 
- Often additions to code introduce new faults to a previously working system.
- As new code is written, the strucutre of the codebase may degrade. 
- Links (physical or otherwise) are lost between the system and its associated documentaiton. 

## Cost Reduction Methods 

It is essential to keep the initial system design simple and efficient. The best way to reduce the possibility of expensive future maintenance is to consider maintainence in the system's inital design. 
