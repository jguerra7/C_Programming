# Teacher Led Demos

1. Create the Famous "Hello World!" program:
```C
#include <stdio.h>

int main(void)
{
	printf("hello, world\n");
 }
```
Sometimes you may get a warning message from the compiler? If so, what did you get and what is needed to make it go away?

2.  Consider the following program:
 ```C
  #include <stdio.h>

int main (void)
{
	printf("Parkinson's Law:\nWork expands so as to ");
	printf("fill the time\n");
	printf("available for its completion.\n");
	return 0;
}
 ```

(a) Identify the directives and statements in this program.
(b) What Output does the program produce?

3. Condense the dweight.c program by (1) replacing the assignments to height,length, and width with 
  initializers and (2) removing the weight variable, instead calculating (volume+ 165)/166 within the last printf.
  
4. Write a program that declares several int and float variables-without initializing them- and then prints their values. Is there any pattern to the values? (Usually there isn't.)

5.  Which of the following are not legal C identifiers?
  (a) 100_bottles
  (b)_100_bottles
  (c) one_hundred_bottles
  (d) bottles_by_the_hundred_
  
 6. Why is it not a good idea for an identifier to contain more than one adjacent underscore(as in current__balance, for example)?
 7. Which of the following are keywords in C?
    (a) for
    (b) If
    (c) main
    (d) printf
    (e) while
 8. How many tokens are there in the following statement?
    ```
    answer=(3*1-p*p)/3;
    ```
9. Insert spaces between the tokens in Exercise 8 to make the statement easier to read.
10. In the dweight.c program, which spaces are essential?

## Fill in the blanks in each of the following.

Every C program begins execution at the function ___________.

Every function’s body begins with ____________and ends with__________.

Every statement ends with a(n)___________.

The______________standard library function displays information on the screen.

The escape sequence \n represents the____________character, which causes the cursor to position to the beginning of the next line on the screen.

The_________Standard Library function is used to obtain data from the keyboard.

The conversion specifier______________is used in a scanf format control string to indicate that an integer will be input and in a printf format control string to indicate that an integer will be output.

Whenever a new value is placed in a memory location, that value overrides the previous value in that location. This process is said to be_____________.

When a value is read from a memory location, the value in that location is preserved; this process is said to be______________.

The_______________statement is used to make decisions.
 
