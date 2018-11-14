# CS23820 Lecture 5, Part 3
__Wednesday, October 18th 2017__ and __Thursday, October 19th 2017__
 
**Lecture:** Dave Price and Richard Shipman, based on slides developed by Fred Long and Peter Hoskins.  
**Notes:** ela12@aber.ac.uk

## Indian Hill C Style and Coding standards 

> Reading: Indian Hill style guide. 

- C Programs written in an idiosyncratic style can be difficult for others to read.
- A standard should be adpoted by organisations to reduce this difficulty. 
- The main cose of software dev is typically maintaining code.
- Code which is complicated or difficult to read is _bad code_. 
- The ojective should always be to create maintainable code. 

### Files 

- Approx 1000 lines (probalby closer to 100-200) lines to be considedered max length to avoid possible buffer confestions with editors and line printers. 
- Line length should probably not exceed 79 characters. 
- Suffix conventions: 
	- .c
	- .o
	- .h
	- .s

- Case Conventions: 
	- Makefile README

### Header Files 

- Files that are included in other files by the C preprocessor before compilation. 
- Avoid private header filenames that are the same as library header filenames.
- Avoid defining vars in a header file.
- Header files should not be nested. 
- Header files are included using the <> symbols if the header file belongs to the standard library, or the "" symbols if they are written by the programmer. 

#### Stopping Double Includes 

In a heade file called `example.h` it is quite common to have lines such as :

```c
#ifndef EXAMPLE_H //If not defined EXAMPLE_H
#define EXAMPLE_H //Define it EXAMPLE_H here.

...

#endif
```
### README

It is very conventional to have a file called README that contains valuable information concerining the program, its compliation and use, etc.

### Comments 

All comments should add real value. 
The comments should describe what is happening, how it is being done, waht parameters mean, which globals are used and which are modified, and any restrictions or bugs. 

#### Examples 

```c
/* 
* Here is a block comment.
* The comment text should be tabed
* orspaced uniformly.
* The opening slash-star and closing star-slash are alone on a 
* line.
* */
```

or

```c
/*
** Alternative format for block comments.
*/
```

In more recent versions of C, you can comment like this: 

```c
// This is a legal comment in newer versions of C.
```

Older single line comments look like this: 

```c
/* Old style single line comment */
```

### Declarations 

- Global declarations should begin in column 1. 
- All external data declaration should be preceeded by the `extern` keyword.
- The `pointer` qualifier `*` should be with the `var` name rather than with the type. 

```c
char *s,*t,*u; //Three pointers declared.
char* s,t,u // One pointer declared.
```
Unrelated declarations, even of the same type, should be on separate lines.

```c
struct boat { 
	int wllength; //Waterline length in meter.
	int type; //See below.
	long sailarea; //Sail area in square meters.
```
Any variable whose initial value is important should be explicitly initizalized, or at the very least should be commented to indicate that C's default initialization to zero (which only happens for `globals` and `statics`) is being relied upon. 

This is especially important if your program depends on some specific initialized `var`.

Each function should be preceeded by a block comment. 

### Whitespace

- Use vertical and horizontal whitespace generously.
- Indentation and spacing shold reflect the block structure of the code; there should be at least 2 blank lines between the end of one function and the comments for the next. 

#### Simple Statements

There should only be one statement per line unless the statements are very closely related. 

#### Careful

The `NULL` body of a `for` or `while` loop should be alone on a line and commented so that it's clear that the `NULL` body is intentional and not missing code.

```c
while (*dest++ = *src++)
	; // Void
```

#### Compound Statements 

A compound statement is a list of statements enclosed by braces. 
There are many common ways of formatting the braces.
Be consistent with your local standard, if you have one, or pick one and use it consistently. 
When editing someone else's code, always use the style used in that code. 

##### Examples

**K&R style** is the conventional prferred method: 

```c
control {
	statement;
	statement;
	...
}
```

#### Case Statements

```c
switch (expr) {
case ABC:
case DEF: 
	statement;
	break;
case UWV:
	statement;
	//Fallthrough to XYZ.
case XYZ:
	statment;
	break;
}	
```

### Operators 

- Unary operators should not be separated from their single operand.
- Generally, all binary operators except `.` and `->` should be separated from their operands by blanks. 

### Naming Conventions 

- Individual projects will have their own naming conventions
- General Rules
	- #define constants should be in CAPS
	- Enumerated constants are Capitalized or in CAPS.
	- Most other things should be in lower case. 
	- In C, camel case shouldn't be used, rather an `_` should be used in names with `multiple_parts`.

### Portability

- Aim to write code that will run on different machines with the minimum amount of re-writing. 
- Obstacles
	- Hardware
	- OS 
	- Compliers 

#### Operand Evaluation 

#### Word Sizes 

- Objects may be non-intuitive sizes, pointers are not always the same size as ints, the same size as each other, or freely interconvertible. 
 
