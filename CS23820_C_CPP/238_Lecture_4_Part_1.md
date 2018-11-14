# CS23820 Lecture 4, Part 1
__Thursday, October 12th 2017__  
Lecture: dap@aber.ac.uk   
Notes: ela12@aber.ac.uk

## Arrays, Pointers and Structures

> Reading: Prinz and Crawford, Chapter 8


-

```c
type name [size];
```
**"The name of an array is a pointer to its first element."**

&therefore;   

```c 
int s[10];
```
wrrting `s` is equivalent to `&(s[0])` `&s[0]`.

#### Address (Pointer) Arithmetic

> Address arithmetic is about taking the address and adding enough to the address to make it relevant. In C you can have arrays of any type. For example, you can have an array of structures. 

`&s[i]` is the address of the ith element starting from 0. 

Arithetic works in terms of the size of the elements: 

`int * x;` as a definition. the in an expression `*x` means what `x` points at and if we have `int s[10];` then `*s` is the contents of `s[0]`. 

##### More examples of different notation that achieves the same goal:

`& s[6] - 3` is equivalent to asking for the value at `&s[3]`. 

&therefore; below are all equivalent when asking for the pointer to the address `s[5]`:

```c
s[5] = 47;
* (s + 5) = 47;
* &s[5] = 47;
* (&s[8] - 3);  
```

##### Examples where address arithmetic might be useful: 

###### Passing arrays as parameters (arguments) to functions:

```c
int a[50];
...
myFunction(a); /* Function Declaration */ 

void myFunction(int *p){ /* Function Definition, passing in the pointer to the array. */ 

	p[0] = 47;
	
	/* Or use pointer syntax insead */ 
	
	*(p + 2) = 53;
	
}
	
```

Another way of writing this, which might make more sense: 

```c
void myFunction(int p[]){...}
```

or the K&R way:

```c
int myFunction(ptr)
int * ptr; /*Parameters (arguments) placed on separate line.*/
{...}
```

or the K&R way using sqaure bracket notation:

```c
int myFuntion(ptr)
int ptr[]; /*Parameters (arguments) placed on separate line.*/
{...}
```

#### Pointers

`int * p;`  P can be used to point to an `int`. This allocates space for the pointer, but _not_ for what it might point at. 

```c
main(){
	int *p;
		*p = 'A'; //'A' is stored as it's ASCII int representation.  
}
```
is wrong as P points to nowhere.

```c
main(){
	int *p, ch; //Declare a pointer called p. Declare an int called ch.
	p = &ch; // Pointer p then points to the address of ch.
	*p = 'A'; //the pointer is then assigned the value of 'A' in ASCII. 
}
```

is correct.

#### Pointer Types 

All pointers are not the same - pointers need to be assigned types. 

```c 
int i;
char * p_char; // p_char is pointing to a char. 
p_char = &i; // WRONG as p_char is of type char and it wants to be assigned to the pointer of type int (i). 
p_char = (char *)&i; //This is okay. 
``` 

##### Generic Pointer Type 

```c
void * p_void;
``` 

is a generic pointer. It's not very useful as a keyword because void usually means noting. However, in this context `void` means that the pointer can point to _anything_. 

- With generic pointers, there is no support for address arithmetic. (As the pointer does not know the type of the the _thing_ it's pointing to). 
- You can assign a value which is a pointer to any type into a variable define as `void *`. 
	
#### Strings
Strings are stored as character arrays as there are no string types in C.
For example, if 
"ABC" is a string stored somewhere in memory:

- *"ABC" is eqivalent to &rightarrow; 'A'
- "ABC"[0] is eqivalent to &rightarrow; 'A'
- "ABC"[2] is eqivalent to &&rightarrow; 'C'

##### String Processing Functions 
> Reading: Prinz and Crawford Chapter 17

`strcpy`, `strncpy`, `strlen`, `strcat`, `strncat`, `strcmp`, `strncmp`

et. al. 

#### Dynamic Arrays and C89 and C99

- C89 does _not_ permit the use of "dynamic arrays".
- C99 _does_ permit the use of "dynamic arrays". 

We first see C89 reject such arrays and then we look at how we can still effectively get an equivalent to dynamic arrays in C89:

##### C89 - Dynamic Array Rejection 

```c
void create_array(int n){
	int new_array[n];
	new-array[0] = 54;
	return; 
```

Warning message: "ISOC90 forbids variable length array `'new_array'` [-Werror=vla] `int new_array[n];`



