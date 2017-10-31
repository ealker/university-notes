# CS23820 Lecture 4, Part 2
__Thursday, October 12th 2017__  
Lecture: dap@aber.ac.uk   
Notes: ela12@aber.ac.uk

#### Implicit Function Declarations 

From [Stack Overflow:](https://stackoverflow.com/questions/9182763/implicit-function-declarations-in-c)
> When C doesn't find a declaration, it assumes this implicit declaration: int f();, which means the function can receive whatever you give it, and returns an integer. If this happens to be close enough (and in case of printf, it is), then things can work. In some cases (e.g. the function actually returns a pointer, and pointers are larger than ints), it may cause real trouble.

#### C89 - Equivalent to Dynamic Arrays 

Dynamic Memory allocation in C89: 

This is illegal in C89 where n is a `var`. 

```c
char s[n]; 
```

```c
char *s; //Pointer s of type char.
s = malloc (n); // Request an area of n bytes and sets s to point at it.
float *f; //Pointer f of type float.
f = malloc(100 * sizeof(float));
```
`malloc` returns `NULL = 0` if a failure occurs. 

An array that needs to be used by more than one function should be created used `malloc()` and `calloc()`. These arrays can only be 'destroyed' by using `free`. A program must release space allocated by `calloc` or `malloc` by calling this function: 

```c
void free(void * ptr);
for instance like 
	free (f);
```

A common pitfall is calling `free` twice on the same pointer. 

#### C99 - Dynamic Arrays 

```c
char s[n]; //Is legal in C99 where n is a var.
```

Arrays are allowed in C99 as local `var` inside functions in C99.

Structures and unions may _not_ include such arrays as elements. 
These arrays are created as the function is entered and any spaced used is released as the function exists. 

For dynamic arryays with lifetimes longer than a single function call then you need to use `malloc()` and `calloc()` as described in previous slides. 

> Reading: Pages 112/113, Chapter 8, Prinz and Crawford.

### I/O Strings 

```c
put(s)
gets(s) /Gets text into s[0] ... s[...]
```
`gets()` can be fairly dangerous. There is no subscript overflow checking, therefore if the array `s` is written to have 10 elements, and previous code has assigned the array to have 11 elements, using `get` can cause memory issues. 
 
`gets()` is removed in C11.

### 2D Arrays 

```c
int X[5][7]; //Stored, first row all clumns, second row all column.
```

```c
int X[5][4] = {{0,3,7,9}, {7,4,2,1}}; //If not all the rows are declared, the rest are set to 0. 
```

You can also create multi-dimensional arrays.

### Preprocessor 

The generic syntax: 

```c
#define symbol value
```

You can parameterise the substitions (called Macros in a lot of languages). 

```c
#define symbol(x,y) (x+x)*y

z =symbol(2,3); //This is NOT a function call - you're calling the preprocessing substitution.
```

is eqivalent to:

```c
z = (2+2) * 3;
```

Problems can araise if the actual `x` and `y` vals in the preprocessing statement are expressions. 	

You can embed the hash symbol in substitutions: 

```c
#define myMac(x) #x
myMac(fred) //causes "fred" with return val in quotes.
```

#### Conditional Compliation 

Two variants of the code in one file, perhaps they compile for different operating systems. 

`# if constant_expression` ... `#else` ... `endif` 

Sometimes, we can comment old code while testing: 

```c 
#if 0 
... old code ...
#endif
```

This helps us from accidentally commenting out code we want to test with the normal `/**/` comment operator.  