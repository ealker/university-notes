# CS23820 Lecture 1 - C Programming
October 3rd 2017   
Lecture: dap@aber.ac.uk.  
Notes: ela12@aber.ac.uk

## Introduction
It's easy to write powerful programs that are syntactically correct in C, but that don't behave the way that you (the programmer) expect them to behave. 
C was designed to be a portable, efficient language that works closesly with the machine's architecture - there is a central philosophy that runs throughout C that promotes compatability - for example a C program written in the early '70s should compile and run on a modern system running C11. Due to this philosophy, almost no features have been removed/ syntax dramatically changed from the first version of C to C11. 

### C Programs:

* Are a collection of _functions_ and _global variables_ at a high level. 
* Contain **no** nested functions. 
* Are saved in C Source files and header files that describe shared features and function signatures. 

### Compiltation Process: 

Preprocessing &rightarrow; Compilation &rightarrow; Linking. During compliation, a single "compliation unit" is compiled at a time in isolation of other files, in the order in which the compiler finds and reads in the source files. So, for example, a 'main.c' file is read in, compiled, object code is produced and then the other c files are complied independently of when 'main.c' was compiled. 
During linking, the otuput from the code is combined (linked) with objecrs produced by the compilation user's programs compilation units, functions from libraries and standard program startup code. 

>Note: "Comments shouldn't describe the syntactical rules of the language, rather they should provide the reason for 'why' you are writing your code a certain way/describe what it does."

#### Command Line Commands 
Compile and link C source code:
`
elliot$ gcc nameOfFile.c
` 

Create executable:
`
elliot$ gcc nameOfFile.c -O exefile
`
