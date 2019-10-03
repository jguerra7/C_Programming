# C Language: #define Directive (macro definition)
## This C section explains how to use the #define preprocessor directive in the C language.

### Description
In the C Programming Language, the #define directive allows the definition of macros within your source code. These macro definitions allow constant values to be declared for use throughout your code.

Macro definitions are not variables and cannot be changed by your program code like variables. You generally use this syntax when creating constants that represent numbers, strings or expressions.

Syntax
The syntax for creating a constant using #define in the C language is:
```c
#define CNAME value
```
OR
```c
#define CNAME (expression)
```
### CNAME
The name of the constant. Most C programmers define their constant names in uppercase, but it is not a requirement of the C Language.
### value
The value of the constant.
### expression
Expression whose value is assigned to the constant. The expression must be enclosed in parentheses if it contains operators.
## Note
Do NOT put a semicolon character at the end of #define statements. This is a common mistake.
### Example
Let's look at how to use #define directives with numbers, strings, and expressions.

### Number
The following is an example of how you use the #define directive to define a numeric constant:
```c
#define AGE 10
```
In this example, the constant named AGE would contain the value of 10.

### String
You can use the #define directive to define a string constant.

For example:
```c
#define NAME "90cos.com"
```
In this example, the constant called NAME would contain the value of "TechOnTheNet.com".

Below is an example C program where we define these two constants:
```c
#include <stdio.h>

#define NAME "90cos.com"
#define AGE 10

int main()
{
   printf("%s is over %d years old.\n", NAME, AGE);
   return 0;
}
```
This C program would print the following:
```
90cos.com is over 10 years old.
```
### Expression
You can use the #define directive to define a constant using an expression.

For example:
```c
#define AGE (20 / 2)
```
In this example, the constant named AGE would also contain the value of 10.

Below is an example C program where we use an expression to define the constant:
```c
#include <stdio.h>

#define AGE (20 / 2)

int main()
{
   printf("90cos.com is over %d years old.\n", AGE);
   return 0;
}
```
This C program would also print the following:
```
90cos.com is over 10 years old.
```
