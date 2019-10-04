# Class Practice Exercises
## Structured Development

## Identify and correct the errors in each of the following. [Note: There may be more than one error in each piece of code.]

a. 
```
if ( age >= 65 );
   puts( "Age is greater than or equal to 65" );
else
   puts( "Age is less than 65" );
```
b. 
```
int x = 1, total;

while ( x <= 10 ) {
   total += x;
   ++x;
}
```
c.
```
While ( x <= 100 )
   total += x;
   ++x;
```
d.
```
while ( y > 0 ) {
   printf( "%d\n", y );
   ++y;
}
```
What does the following program print?
```c 

#include <stdio.h>

int main( void )
{
   unsigned int x = 1, total = 0, y;
   
   while ( x <= 10){
      y = x * x;
      printf("%d\n", y );
      total += y;
      ++x;
   }// end while
   
   printf("Total is %d\n", total);
} //end main

```
Write a single pseudocode statement that indicates each of the following:
```
Display the message "Enter two numbers".

Assign the sum of variables x, y, and z to variable p.

The following condition is to be tested in an if…else selection statement: 
The current value of variable m is greater than twice the current value of variable v.

Obtain values for variables s, r, and t from the keyboard.
```
Formulate a pseudocode algorithm for each of the following:
```
Obtain two numbers from the keyboard, compute their sum and display the result.

Obtain two numbers from the keyboard, and determine and display which (if either) is the larger of the two numbers.

Obtain a series of positive numbers from the keyboard, and determine and display their sum. 
Assume that the user types the sentinel value -1 to indicate “end of data entry.”
```
For These next three Exercises, perform each of these steps:

Read the problem statement.

Formulate the algorithm using pseudocode and top-down, stepwise refinement.

Write a C program.

Test, debug and execute the C program.

Drivers are concerned with the mileage obtained by their automobiles. One driver has kept track of several tankfuls of gasoline by recording miles driven and gallons used for each tankful. Develop a program that will input the miles driven and gallons used for each tankful. The program should calculate and display the miles per gallon obtained for each tankful. After processing all input information, the program should calculate and print the combined miles per gallon obtained for all tankfuls. Here is a sample input/output dialog:

```

Enter the gallons used (-1 to end):  12.8
Enter the miles driven: 287
The miles/gallon for this tank was 22.421875

Enter the gallons used (-1 to end):  10.3
Enter the miles driven: 200
The miles/gallon for this tank was 19.417475

Enter the gallons used (-1 to end): 5
Enter the miles driven: 120
The miles/gallon for this tank was 24.000000

Enter the gallons used (-1 to end): -1

The overall average miles/gallon was 21.601423

```

