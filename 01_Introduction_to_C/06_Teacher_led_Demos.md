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
 
 ## State whether each of the following is true or false. If false, explain why.

Function printf always begins printing at the beginning of a new line.

Comments cause the computer to display the text after // on the screen when the program is executed.

The escape sequence \n when used in a printf format control string causes the cursor to position to the beginning of the next line on the screen.

All variables must be defined before they’re used.

All variables must be given a type when they’re defined.

C considers the variables number and NuMbEr to be identical.

Definitions can appear anywhere in the body of a function.

All arguments following the format control string in a printf function must be preceded by an ampersand (&).

The remainder operator (%) can be used only with integer operands.

The arithmetic operators *, /, %, + and − all have the same level of precedence.

A program that prints three lines of output must contain three printf statements.

## Write a single C statement to accomplish each of the following:

Define the variables c, thisVariable, q76354 and number to be of type int.

Prompt the user to enter an integer. End your prompting message with a colon (:) followed by a space and leave the cursor positioned after the space.

Read an integer from the keyboard and store the value entered in integer variable a.

If number is not equal to 7, print “The variable number is not equal to 7.”

Print the message “This is a C program.” on one line.

Print the message “This is a C program.” on two lines so that the first line ends with C.

Print the message “This is a C program.” with each word on a separate line.

Print the message “This is a C program.” with the words separated by tabs.

## Write a statement (or comment) to accomplish each of the following:

State that a program will calculate the product of three integers.

Define the variables x, y, z and result to be of type int.

Prompt the user to enter three integers.

Read three integers from the keyboard and store them in the variables x, y and z.

Compute the product of the three integers contained in variables x, y and z, and assign the result to the variable result.

Print “The product is” followed by the value of the integer variable result.

## Using the statements you wrote in the previous exercise, write a complete program that calculates the product of three integers.

## Identify and correct the errors in each of the following statements:
```
a. printf( "The value is %d\n", &number );

b. scanf( "%d%d", &number1, number2 );


C. if ( c < 7 ) ; {
   printf( "C is less than 7\n" ) ;
}


D. if ( c => 7 ) {
   printf( "C is greater than or equal to 7\n" );
}
```

## Identify and correct the errors in each of the following statements. (Note: There may be more than one error per statement.)
```
scanf( “d”, value );

printf( “The product of %d and %d is %d”\n, x, y );

firstNumber + secondNumber = sumOfNumbers

if ( number => largest)
   largest == number;

*/ Program to determine the largest of three integers /*

Scanf( “%d”, anInteger );

printf( “Remainder of %d divided by %d is\n”, x, y, x % y );

if ( x = y );
   printf( %d is equal to %d\n", x, y );

print( “The sum is %d\n,” x + y );

Printf( "The value you entered is: %d\n, &value );

```

## Fill in the blanks in each of the following:

_________are used to document a program and improve its readability.

The function used to display information on the screen is_____________--.

A C statement that makes a decision is_______________.

Calculations are normally performed by________________-statements.

The______________function inputs values from the keyboard.


## Write a single C statement or line that accomplishes each of the following:

Print the message “Enter two numbers.”

Assign the product of variables b and c to variable a.

State that a program performs a sample payroll calculation (i.e., use text that helps to document a program).

Input three integer values from the keyboard and place them in integer variables a, b and c.


## State which of the following are true and which are false. If false, explain your answer.

C operators are evaluated from left to right.

The following are all valid variable names: _under_bar_, m928134, t5, j7, her_sales, his_account_total, a, b, c, z, z2.

The statement printf( “a = 5;” ); is a typical example of an assignment statement.

A valid arithmetic expression containing no parentheses is evaluated from left to right.

The following are all invalid variable names: 3g, 87, 67h2, h22, 2h.

## Fill in the blanks in each of the following:

What arithmetic operations are on the same level of precedence as multiplication?____________.

When parentheses are nested, which set of parentheses is evaluated first in an arithmetic expression?___________.

A location in the computer’s memory that may contain different values at various times throughout the execution of a program is called a_______________________.


## What, if anything, prints when each of the following statements is performed? If nothing prints, then answer “Nothing.” Assume x = 2 and y = 3.
```
printf( "%d", x );

printf( "%d", x + x );

printf( "x=" );

printf( "x=%d", x );

printf( "%d = %d", x + y, y + x );

z = x + y;

scanf( "%d%d", &x, &y );

// printf( "x + y = %d", x + y );

printf( "\n" );
```
## Which, if any, of the following C statements contain variables whose values are replaced?
```
scanf( "%d%d%d%d%d", &b, &c, &d, &e, &f );

p = i + j + k + 7;

printf( "Values are replaced" );

printf( "a = 5" );
```
## Given the equation y = ax3 + 7, which of the following, if any, are correct C statements for this equation?
```
y = a * x * x * x + 7;

y = a * x * x * ( x + 7 );

y = ( a * x ) * x * ( x + 7 );

y = ( a * x ) * x * x + 7;

y = a * ( x * x * x ) + 7;

y = a * x * ( x * x + 7 );

```
## State the order of evaluation of the operators in each of the following C statements and show the value of x after each statement is performed.
```
x = 7 + 3 * 6 / 2 - 1;

x = 2 % 2 + 2 * 2 - 2 / 2;

x = ( 3 * 9 * ( 3 + ( 9 * 3 / ( 3 ) ) ) );

```



