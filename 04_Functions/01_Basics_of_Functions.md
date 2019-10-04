
# Basics of Functions
## Working with Functions
Behind all well-written programs in the C programming language lies the same fundamental
element—the function. You’ve used functions in every program that you’ve encountered so far. 
The printf() and scanf() routines are examples of functions. Indeed, each and every program 
also uses a function called main(). You may be wondering, “What’s the big deal about functions?”
When you start breaking down the your programming task into functions, your code will be easier to write,
read, understand, debug, modify, and maintain. Obviously, anything that can accomplish all of these 
things is worthy of a bit of fanfare. As a result this is a chapter packed with important information, including

 * Understanding the basics of functions.

 * Explaining local, global, automatic, and static variables.

 * Using single-dimensional and multi-dimensional arrays with functions.

 * Returning data from functions

 * Using functions to execute top-down programming

 * Calling functions from within other functions, as well as recursive functions.

## DEFINING A FUNCTION
First, you must understand what a function is, and then you can proceed
to find out how it can be most effectively used in the development of programs. 
Lets look at this program, which displays the phrase “Programming is fun.”:

```c
#include <stdio.h>

int main (void)
{
    printf ("Programming is fun.\n");

    return 0;
}
```
Here is a function called printMessage() that does the same thing:

```c
void printMessage (void)
{
    printf ("Programming is fun.\n");
}
```
The differences between printMessage() and the function main() from the first program 
is in the first and last line. The first line of a function definition tells the compiler 
(in order from left to right) four things about the function:
```
1. Who can call it (discussed in Chapter 14, “Working with Larger Programs”)

2. The type of value it returns

3. Its name

4. The arguments it takes
```
The first line of the printMessage() function definition tells the
compiler that the function returns no value (the first use of the keyword void),
its name is printMessage, and that it takes no arguments (the second use of the keyword void). 
You learn more details about the void keyword shortly, if we haven't covered it yet. 

Obviously, choosing meaningful function names is just as important as choosing meaningful 
variable names—the choice of names greatly affects the program’s readability.

Recall from discussions of the first program that main() is a specially recognized 
name in the C system that always indicates where the program is to begin execution. 
You must always have a main(). You can add a main() function to the preceding code 
to end up with a complete program, as shown in Program.

Program:  Writing a Function in C

```c
#include <stdio.h>

void printMessage (void)
{
    printf ("Programming is fun.\n");
}

int main (void)
{
    printMessage ();

    return 0;
}
```
Program Output
```
Programming is fun.
```
Program consists of two functions: printMessage() and main(). Program execution always begins with main(). 
Inside that function, the statement
```
printMessage ();
```
appears. This statement indicates that the function printMessage() is to be executed. 
The open and close parentheses are used to tell the compiler that printMessage() is a 
function and that no arguments or values are to be passed to this function (which is 
consistent with the way the function is defined in the program). When a function call is 
executed, program execution is transferred directly to the indicated function. 
Inside the printMessage() function, the printf() statement is executed to display 
the message “Programming is fun.”. After the message has been displayed, the printMessage() 
routine is finished (as signaled by the closing brace) and the program returns to 
the main() routine, where program execution continues at the point where the function 
call was executed. By this time you may have noted that the terms function and routine 
are used interchangeably—the two terms basically mean the same thing.

Note that it is acceptable to insert a return statement at the end of printMessage() like this:
```
return;
```
Because printMessage() does not return a value, no value is specified for 
the return. This statement is optional because reaching the end of a function 
without executing a return has the effect of exiting the function anyway without 
returning a value. In other words, either with or without the return statement, 
the behavior on exit from printMessage() is identical.

As mentioned previously, the idea of calling a function is not new. The printf() and scanf() 
routines are both program functions. The main distinction here is that these routines did not 
have to be written by you because they are a part of the standard C library. When you use the 
printf() function to display a message or program results, execution is transferred to the 
printf() function, which performs the required tasks and then returns back to the program. 
In each case, execution is returned to the program statement that immediately follows the call to the function.

Now try to predict the output from this Program

Program Calling Functions

```c
#include <stdio.h>

void printMessage (void)
{
     printf ("Programming is fun.\n");
}

int main (void)
{
    printMessage ();
    printMessage ();

    return 0;
}
```
Program Output
```
Programming is fun.
Programming is fun.
```
Execution of the preceding program starts at main(), which contains two calls
to the printMessage() function. When the first call to the function is executed, 
control is sent directly to the printMessage() function, which displays the message 
“Programming is fun.” and then returns to the main() routine. Upon return, another
call to the printMessage() routine is encountered, which results in the execution 
of the same function a second time. After the return is made from the printMessage() 
function, execution is terminated.

As a final example of the printMessage() function, try to predict the output from the follwoing program

Program More on Calling Functions

```c
#include <stdio.h>

void printMessage (void)
{
    printf ("Programming is fun.\n");
}

int main (void)
{
    int  i;

    for ( i = 1;  i <= 5;  ++i )
        printMessage ();

    return 0;
}
```
Program Output
```
Programming is fun.
Programming is fun.
Programming is fun.
Programming is fun.
Programming is fun.
```
