# CS23820 Lecture 5, Part 1
__Tuesday, October 17th 2017__  
Lecture: dap@aber.ac.uk   
Notes: ela12@aber.ac.uk

## "C Programming - Batch 5" 

### Reminder - Structures 

These are like `records` in other languages. 

```c
struct myStruct {
	int c;
	float y;
}

z;
```

The type is `struct myStruct` and `z` is a `var` of this type. 

For element (member) access: 

```c
z.c = 7;
```

### Typedef 

New names for `types`:

>Reading Prinz and Crawford Chapter 10 

```c
typedef struct myStruct myNew;

myNew r;
```

rather than:

```c
struct myStruct r;
```

You can often combine `typedef` and the `struct` definition:

```c
typedef struct s_tag{
	int c;
	flaot x;
	struct s_tag * s_ptr;
}

newstruct; 
```

Then we can just used `newstrcut`.

### Structure and Arguments 

Both **K&R** and **ANSI**: permit pointers to structures as arguments and return values for functions. 

**ANSI**: permits structurs themselves as argumentss and return values. 

**Dynamic data strcutures**: `structs` are often used to build linked lists, trees, networks, etc.

#### Potential Problems with Pointers 

```c
int * myFunc(){
	int i; // A local var created automatically as the function is called.
	...
	return &i; //Function returns a pointer to an int which has now been destroyed.
}
```
#### Union 

A single area of memory that can be used in one of a choice of ways: 

```c
union myUn{
	int x;
	float y;
	char x;
}; 

union myUn p,q; //Two vars. 
```
> At any time, `p` and `q` can each only contain an `int` or a `float` or a `char`. 

#### Bit Fields 

A means to use one location and split its bits into separate accessible items. 

```c
struct myS{
	unsigned p1:3,p2:4,p3:1;
	int x;
} z;
```

`z` is a structure of type `struct myS`. It has four members, `p1` `p2` `p3` (bit fields) and `x` (an integer). You cannot ask for the address of bit fields (for example `&Z.p2` is not a legal statement in C. 

#### Files 

`stdio.h` contains a definition of a structure `FILE`. 

```c
typedef struct{...} FILE;
```

Files are often accessed via `FILE *` functions:

- `fopen`
- `fprintf`
- `fscanf`
- `fclose`
- `feod`
- `fgets`
- `fputs`
- `fseeks`
- `fread`
- `fwrite`

This works with the 'standard' `FILE *` streams - `stdin`, `stdout`, `stderr`.

> Reading: Prinz and Crawford Chapter 13.

#### Program Parameters 

```c
main(int argc, char * argv[]){...}
```

where: 

- `argc` - number of arguments.
- `argv[0]` - a pointer to the first argument (string in the case abov).

> Reading: Prinz and Crawford pg 101, 102. 

#### Pointers to Functions 

**ANSI**:

```c
float (*p)(int i, int j);
```

**K&R**:

```c
float (*p)();
```

`p` is a pointer to a function that takes two `ints` as parameters and returns a `float`. With the ANSI syntax, it shows the two paramters of type `int`. The R&R syntax doesn't show the parameter types. 

Below is a call to the function (you call the function by supplying the pointer to the function and its parameters):

```c
(*p)(x,y)
```
In the ANSI standard, you can write the line below: 

```c
p(x,y)
```

>Reading: Prinz and Crawford pg 136-138

##### Extended Example 

```c
#include <stdio.h> 

int fred(int x){
	printf("Hello for Fred \n");
	return x * x;
}

int bert(int x) {
	printf("Hello for Burt \n");
	return x * 100;
}

main(){
	int r;
	r = doAsYouAreTold(&fred); //A call to doAsYouAreTold, passing in a pointer to fred();.
	printf("r was set equal to %d\n",r); 
	r = doAsYouAreTold(&bert);
	printf("r was set equal to %d\n",r);
}

int doAsYouAreTold(int (*f)(int)){ //This function takes a pointer to another function as its parameter. 
	reutrn (*f)(6);
}
```