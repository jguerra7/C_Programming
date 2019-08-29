#  Basics of C Language 

This will cover some fundamental concepts of C Language namely Variables, Tokens, Operators in C language.

## Variables
They are temporary memory locations allocated during execution of the program. As the name suggests it is an entity whose value may change during program execution.

### Rules for variable name

* It does not have a space between characters.
* Collection of alphabets, digits, and underscore (_).
* The first character should be either alphabet or underscore (_).
* No other special symbol except underscore (_).
* Keywords cannot be used as variable name.

### Declaration of variable

### Syntax:

```c datatype variable_name;```
### Example:
```c
int a;
```
It tells the user what is the data type of a declared variable or what type of values it can hold.

#### Initialization of a variable

The process of assigning any value to any variable.

### Example:
```c
int a = 5;
```
## Token
The basic and smallest unit of C program is token.

### Token includes :

* Keywords
* Identifier
* Constants
* String Constant
* Operators
* Special Symbols e.g: _ , @ , *

## Keywords or Reserve words

These are those words whose meaning is already explained to the compiler.

They can’t be used as a variable name because if we do so that means we are defining the new meaning to the compiler which the compiler does not allow.

## Identifier

They are the name given to programming elements such as array, function, variable. Same rules as of variable name.

## Constant

Entities whose value does not during the execution of a program.

## String constant

Collection of character enclosed by a double inverted comma. e.g.: "abc"

## Operators

They are used to perform arithmetic and logical operations by ALU.

## Example:

 a+b

Here, a and b are operands and + is an operator.

C language has very rich operators. Many different types of operators are available in C language for different mathematical computations.

### They are mainly of three types:
Operators itself is a separate topic which needs to be covered in detail.

So, here we get started.

### Unary operators

They require only one operand for execution, it includes :

* Unary minus
* Bitwise compliment
* Logical Not
* Increment / Decrement
* sizeof() operator
* sizeof() Operator

It is used to return the size of an operand. It can be applied on variable, constant, datatype.

## Syntax:
```c
sizeof(operand);
```
### Example:
```c
    int a=2, b;
    b = sizeof(a);
    //or
    b = sizeof(int);
    //or
    b = sizeof(5);
    printf("%d\n",b);
    
    //All of the 3 three statements will give same output.
```
### Ternary operators

They are also called conditional operator. For these operators, we require 3 operands for execution. There is only and one ternary operator in C language.

### Syntax:
```c
 expression_1  ? expression_2 : expression_3 ;
```
If expression_1 is true expression_2 gets executed, if false then expression_3.

## Example:
```c
    int a=4 , b=7 , c;
    
    c = ( a<7 ? a:b );
    
    printf("%d\n", c );
```
### Output

>  4

Since, a = 4, exp_1 is true and therefore exp_2 gets executed. So, c = a gets executed.

## Binary operators

### Arithmetic operators
```
Operator name	            Operator
Addition	                  +
Subtraction               	-
Multiplication	            *
Division                  	/
Modulus	                    %
```
Modulus operator gives remainder and division operator gives quotient. All arithmetic operators can be used for integer and float values except modulus which is used for integers only.

## Relational operators

They are used for comparison between two values. They return result as true or false.
```
Operator name                       	Operator
Less than                             	<
Less than or equal to                 	<=
Greater than	                          >
Greater than or equal to              	>=
Equal to                              	==
Not equal to	                          !=
```
## Logical operators

Used to combine two relational expression and they returns result as true or false.
```
A	   B	      A && B	      A || B	         !A
0		 0    		    0              0            1
0	   1          0              1            1
1	   0          0              1            0
1	   1          1              1            0
```
## Bitwise operators

They are used to perform operation on individual bits. They can be applied on char and int.
```
Operators	        Symbol name	             Meaning
&	                 Ampersand	             Bitwise AND
|	                  Pipe	                  Bitwise OR
^	                  Caret	                   Bitwise X OR
~	                  Tilde	                   Bitwise compliment
<<                	Double less than	      Left shift operator
>>	              Double greater than	      Right shift operator
```






