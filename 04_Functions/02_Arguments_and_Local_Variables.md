## ARGUMENTS AND LOCAL VARIABLES
When the printf() function is called, you always supply one or more values to the function, 
the first value being the format string and the remaining values being the specific program 
results to be displayed. These values, called arguments, greatly increase the usefulness and 
flexibility of a function. Unlike your printMessage() routine, which displays the same message
each time it is called, the printf() function displays whatever you tell it to display.

You can define a function that accepts arguments. In Chapter 4, “Program Looping,” you 
developed an assortment of programs for calculating triangular numbers. Here, you define
a function to generate a triangular number, called appropriately enough, calculateTriangularNumber().
As an argument to the function, you specify which triangular number to calculate. The function then
calculates the desired number and displays the results at the terminal. Program below shows the 
function to accomplish this task and a main() routine to try it out.

## Program  Calculating the nth Triangular Number

```c
// Function to calculate the nth triangular number

#include <stdio.h>

void calculateTriangularNumber (int n)
{
    int  i, triangularNumber = 0;

    for ( i = 1;  i <= n;  ++i )
        triangularNumber += i;

    printf ("Triangular number %i is %i\n", n, triangularNumber);
}

int main (void)
{
    calculateTriangularNumber (10);
    calculateTriangularNumber (20);
    calculateTriangularNumber (50);

    return 0;
}
```
Program Output
```
Triangular number 10 is 55
Triangular number 20 is 210
Triangular number 50 is 1275
```
## Function Prototype Declaration
The function calculateTriangularNumber() requires a bit of explanation. The first line of the function:

```
void calculateTriangularNumber (int n)
```
is called the function prototype declaration. It tells the compiler that calculateTriangularNumber() 
is a function that returns no value (the keyword void) and that takes a single argument, called n, 
which is an int. The name that is chosen for an argument, called its formal parameter name, as well
as the name of the function itself, can be any valid name formed by observing the naming rules 
outlined in earlier sections, for forming variable names. For obvious reasons, you should choose meaningful names.

After the formal parameter name has been defined, it can be used to refer to the argument anywhere inside the body of the function.

The beginning of the function’s definition is indicated by the opening curly brace.
Because you want to calculate the nth triangular number, you have to set up a variable 
to store the value of the triangular number as it is being calculated. You also need a
variable to act as your loop index. The variables triangularNumber and i are defined 
for these purposes and are declared to be of type int. These variables are defined and 
initialized in the same manner that you defined and initialized your variables inside 
the main routine in previous programs.

## Automatic Local Variables
Variables defined inside a function are known as automatic local variables
because they are automatically “created” each time the function is called, 
and because their values are local to the function. The value of a local 
variable can only be accessed by the function in which the variable is defined. 
Its value cannot be accessed by any other function. If an initial value is given 
to a variable inside a function, that initial value is assigned to the variable 
each time the function is called.

When defining a local variable inside a function, it is more precise in
C to use the keyword auto before the definition of the variable.
An example of this is as follows:

```
auto int  i, triangularNumber = 0;
```
Because the C compiler assumes by default that any variable defined inside a 
function is an automatic local variable, the keyword auto is seldom used, and for 
this reason it is not used in this book.

Returning to the program example, after the local variables have been defined, 
the function calculates the triangular number and displays the results. 
The closing brace then defines the end of the function.

Inside the main() routine, the value 10 is passed as the argument in the first 
call to calculateTriangularNumber(). Execution is then transferred directly to 
the function where the value 10 becomes the value of the formal parameter n 
inside the function. The function then proceeds to calculate the value of 
the 10th triangular number and display the result.

The next time that calculateTriangularNumber() is called, the argument 20 is passed. 
In a similar process, as described earlier, this value becomes the value of n inside 
the function. The function then proceeds to calculate the value of the 20th triangular
number and display the answer at the terminal.

For an example of a function that takes more than one argument, rewrite the 
greatest common divisor program (Program 4.7) in function form. The two arguments 
to the function are the two numbers whose greatest common divisor (gcd) you want to calculate. See Program below.

Program Revising the Program to Find the Greatest Common Divisor
```c


/* Function to find the greatest common divisor
        of two nonnegative integer values             */

#include <stdio.h>

void gcd (int u, int v)
{
    int  temp;

    printf ("The gcd of %i and %i is ", u, v);

    while ( v != 0 ) {
        temp = u % v;
        u = v;
        v = temp;
    }

    printf ("%i\n", u);
}


int main (void)
{
    gcd (150, 35);
    gcd (1026, 405);
    gcd (83, 240);

    return 0;
}
```
Program Output
```
The gcd of 150 and 35 is 5
The gcd of 1026 and 405 is 27
The gcd of 83 and 240 is 1
```
The function gcd() is defined to take two integer arguments. The function refers to these 
arguments through their formal parameter names u and v. After declaring the variable temp 
to be of type int, the program displays the values of the arguments u and v, together with
an appropriate message. The function then calculates and displays the greatest common
divisor of the two integers.

You might be wondering why there are two printf() statements inside the function gcd. 
You must display the values of u and v before you enter the while loop because their 
values are changed inside the loop. If you wait until after the loop has finished, the 
values displayed for u and v do not at all resemble the original values that were passed
to the routine. Another solution to this problem is to assign the values of u and v to
two variables before entering the while loop. The values of these two variables can then
be displayed together with the value of u (the greatest common divisor) using a single 
printf() statement after the while loop has completed.
