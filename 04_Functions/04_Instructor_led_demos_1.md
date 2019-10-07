# Class Review 

 A program that illustrates the use of user-defined functions
 
 User-defined functions are the functions that are defined (i.e. developed) by the user
 at the time of writing a program. The user develops the functionality by writing the body of the function. 
 These functions are sometimes referred to as programmer-defined functions.
 Program below illustrates the use of user-defined functions add, sub and println.
 
 ```c
 //User defined functions

#include<stdio.h>

//Function declarations or function prototypes

println();

int add(int, int);

int sub(int x, int y);

//main function, the master function

main()

{

int a,b,sum, diff;

printf(“Enter the values\t”);

scanf(“%d %d”,&a, &b);

//Function invocations

//Asking the workers to do work

sum=add(a,b);

diff=sub(a,b);

println();

//Master presents the results returned by workers

printf(“Result of addition is %d\n”,sum);

printf(“Result of subtraction is %d\n”,diff);

}

//Function definitions

println()

{

printf(“-------------------------\n”);

}

int add(int a, int b)

{

return a+b;

}

int sub(int a, int b)

{

return a-b;

}
```
