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
## What does the following program print?
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
## Write a single pseudocode statement that indicates each of the following:
```
Display the message "Enter two numbers".

Assign the sum of variables x, y, and z to variable p.

The following condition is to be tested in an if…else selection statement: 
The current value of variable m is greater than twice the current value of variable v.

Obtain values for variables s, r, and t from the keyboard.
```
## Formulate a pseudocode algorithm for each of the following:
```
Obtain two numbers from the keyboard, compute their sum and display the result.

Obtain two numbers from the keyboard, and determine and display which (if either) is the
larger of the two numbers.

Obtain a series of positive numbers from the keyboard, and determine and display their sum. 
Assume that the user types the sentinel value -1 to indicate “end of data entry.”
```
## For These next three Exercises, perform each of these steps:
```
Read the problem statement.

Formulate the algorithm using pseudocode and top-down, stepwise refinement.

Write a C program.

Test, debug and execute the C program.
```
(Gas Mileage)Drivers are concerned with the mileage obtained by their automobiles. One driver has kept 
track of several tankfuls of gasoline by recording miles driven and gallons used for each tankful.
Develop a program that will input the miles driven and gallons used for each tankful. 
The program should calculate and display the miles per gallon obtained for each tankful. 
After processing all input information, the program should calculate and print the combined 
miles per gallon obtained for all tankfuls. Here is a sample input/output dialog:

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
(Credit Limit Calculator) Develop a C program that will determine if a department store customer
has exceeded the credit limit on a charge account. For each customer, the following facts are available:
```
Account number

Balance at the beginning of the month

Total of all items charged by this customer this month

Total of all credits applied to this customer’s account this month

Allowed credit limit
```
The program should input each fact, calculate the new balance (= beginning balance + charges – credits), 
and determine whether the new balance exceeds the customer’s credit limit. For those customers whose 
credit limit is exceeded, the program should display the customer’s account number, credit limit, 
new balance and the message “Credit limit exceeded.” Here is a sample input/output dialog:

```

Enter account number (-1 to end): 100
Enter beginning balance: 5394.78
Enter total charges: 1000.00
Enter total credits: 500.00
Enter credit limit: 5500.00
Account:      100
Credit limit: 5500.00
Balance:      5894.78
Credit Limit Exceeded.

Enter account number (-1 to end): 200
Enter beginning balance: 1000.00
Enter total charges: 123.45
Enter total credits: 321.00
Enter credit limit: 1500.00

Enter account number (-1 to end): 300
Enter beginning balance: 500.00
Enter total charges: 274.73
Enter total credits: 100.00
Enter credit limit: 800.00

Enter account number (-1 to end): -1
```
 (Sales Commission Calculator) One large chemical company pays its salespeople on a commission basis. 
 The salespeople receive $200 per week plus 9% of their gross sales for that week. For example,
 a salesperson who sells $5000 worth of chemicals in a week receives $200 plus 9% of $5000, or a total of $650. 
 Develop a program that will input each salesperson’s gross sales for last week and will 
 calculate and display that salesperson’s earnings. Process one salesperson’s figures at a time. 
 Here is a sample input/output dialog:

```

Enter sales in dollars (-1 to end): 5000.00
Salary is: $650.00

Enter sales in dollars (-1 to end): 1234.56
Salary is: $311.11

Enter sales in dollars (-1 to end): -1
```




