# CS23820 Lecture 5, Part 2
__Wednesday, October 18th 2017__  
Lecture: dap@aber.ac.uk   
Notes: ela12@aber.ac.uk

## "C Programming - Batch 5" 

### Functions with Variable Paramters Lists

Can we overload a function (other lang: method overloading) - that is can we create two functions with the same name but with different arguemnts? No. 

It often proves useful to define a function that may take different numbers of parameters of different types on each call - this is helpful when the program is run in different contexts. 

`printf()` is a very common example:

> Reading: Prinz and Crawford pages 108, 453 .

#### Example

In **ANSI**: 

```c
#include<stdarg.h>
int myFunction(int p, float x, ...) {
	va_list my_arg_ptr;
	int i;
	va_start(my_arg_ptr, x);
	i = va_arg(my_arg_ptr, int);
	va_end(my_arg_ptr);
	return i;
}
```

