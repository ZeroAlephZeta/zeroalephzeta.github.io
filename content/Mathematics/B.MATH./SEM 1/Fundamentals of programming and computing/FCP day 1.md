---
date: 24-7-25
duration: 1 hr
prev: NONE
next: "[[FCP day 2]]"
---
The main goal of the course is to be able to program (in C) on our own and check if the program does its job.
###### Installations and books and stuff

Most of the teaching and learning will happen directly from the book by K. N. King, so less notes overall. 

So here is the first programme we parse:

```
#include<stdio.h>
int main(void)
{
	printf("To C, or not to C: that is the question.\n");
	return 0;
}
``` 
The `#` tells the *compiler* to not compile this, and it is rather sent to the *preprocessor*. 
The `int main(void)` is the declaration of the *main function*, which does the main execution of the code. Inside, the `void` says that it doesn't take any arguments in this program. The `return 0;` returns the `0` value to the *environment* and tells the operating system that the program has actually been executed properly. The `printf()` is the command to print the 

###### Math problem asked
How simply can a code be written to print the first hundred integers that are not multiples of 2 and not multiples of 3?
The sequence goes `1 5 7 11 13 17 19 ...`