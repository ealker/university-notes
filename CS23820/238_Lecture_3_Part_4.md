# CS23820 Lecture 3, Part 4
__Wednesday, October 11th 2017__  
Lecture: dap@aber.ac.uk   
Notes: ela12@aber.ac.uk

### More on Argument Types 

#### Passing by Reference
If you want to alter variables outside of functions, using a function, you need to pass and address (reference) (using a pointer) to the var location to be altered. You need to use `&` symbol. 

Example:  

```c
int fun(iptr, jptr)
int * iptr, *jptr;
{...}
```

Example of function call: 

```c
int a,b,c;
c = fun(&a,&b);
```

### Default Function Type

`int` is the default return type of all functions if a return type is not otherwise specified. Function return values are discarded if they are not used in the program. 

In ANSI C, a keyword `void` was added. This has the advantages of: 

+ To say that functions have no return value. 
+ Can be used in function prototypes if no parameters are given. 

Function declaration example: 

```c
void newFunction(void); //Function declaration of type void, called newFunction, taking a parameter of type void. 
```  
### Separate Compilation with Multiple Files / Modules
Functions by default are external, which means that they are visible to the linker. 
You can declare (not define) external variables by:

```c 
extern int x;
```
