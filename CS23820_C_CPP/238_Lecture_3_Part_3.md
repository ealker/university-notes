# CS23820 Lecture 3, Part 3  
Tuesday, October 10th 2017  
Lecture: dap@aber.ac.uk    
Notes: ela12@aber.ac.uk

### Structures 
These are like records in other languages. These allow us to group variables together as part of a similar structure: 

```c
struct myStruct{
int c;
float y;
};

struct myStruct z;
```

The type is defined by the structure tag you place after "struct". On Line 1 in this example, the structure tag is `myStruct`. 

Type is `struct myStruct` and `z` is a var of this type. 

You can combine declaration of a struct type and definition of a var of that type by: 

```c
struct myStruct{
int c;
float y;
} z;
```
Member acess (accessing an element in the struct):  

 ```c
 z.c = 7;
 ```
 > In this case the variable we want to write to is the var 'c'.
 
### Pointers to Structures and -> operator 

```c
struct myStruct new_struct;
struct myStruct * struct_ptr;
struct_ptr = & new_struct;
```

then we can write to a var in the struct: 

```c
new_struct.c = 23;
//or 
(*struct_prt).c = 23;
//or 

```

We can use pointers and structures together to build abstract data types. 
> You cannot put functions inside structs. A struct gives us the ability to collect the "data" together. The fundamental difference to OOP is that a class in OOP contains both the data structures and the functions.  

## Program Organisation:
A program is a collection of:   

+ Functions
+ Global Vars
+ _No_ nested functions. 

### Function Declarations, Definitions, and Calls 

  __Defintions:__ 
  
  + Declaration - state that the function exists and state its signature.
  + Definition - you write the functional code that executes. 
  + Call - where you run the function. 


__There are two types of declarations (both can be global _or_ local):__ 

1. Old K&R approach, with no parameter checking. (still can be used)
1. New ANSI function prototypes. (the modern, better aproach)

#### K&R Method for declaring, defining and calling functions: 

```c
#include <stdio.h>
main(){
	float p;
	float triple(); //K&R style function declaration 
	p = triple(2.7);
	printf("p=%f\n",p);
}

float triple(x)		//Function 'triple' taking x as parameter.
float x; // K&R function parameters (with types) defined here (seperate second line)
{ return 3.0 * x;
}
```
In this example, if line 4 was omitted, the compiler will asssume the code for the body of the function will be written later and that the return type of the undefined function will be an integer. 

#### New ANSI method for declaring, defining and calling functions: 

In the ANSI standard, you declare, define and call functions by 'functioning prototyping'. 

From [Microsoft C Reference:](https://docs.microsoft.com/en-gb/cpp/c-language/function-prototypes)

> A function declaration precedes the function definition and specifies the name, return type, storage class, and other attributes of a function. To be a prototype, the function declaration must also establish types and identifiers for the function's arguments.

```c
#include <stdio.h>

main(){
	float p;
	float triple(float x); //ANSI style function declaration: type, funcName, parameters with types and identifiers.
	p = triple(2.7);
	printf("p=%f\n",p);
}

float triple(float x){  // ANSI function parameters defined here
	return 3.0 * x;
}
```

>Sometimes the complier will throw a 'warning' to the developer - think of these as errors and that the complier is too nice to tell you in future that your code won't work.
  
### Function Local Vars 

1. vars defined in a function are local variables.
2. Parameters (the args passed to the function) - these are initialised as the function is called. These are called/passed by value - the value passed in the function, if changed by the function, will not be altered outside the scope of the function. 

#### Argument Types 

In K&R, declare and the programmer must get it right.
In ANSI, you prototype the declarations and then automatic type conversions are performed (if possible.) 
