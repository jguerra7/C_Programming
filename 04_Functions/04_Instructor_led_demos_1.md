# Guided Walk-throughs of Programs 

##  A program that illustrates the use of user-defined functions
 
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
## Output window

 

Enter the values 43

-------------------------

Result of addition is 7

Result of subtraction is 1


## Remarks

• println, add and sub are user-defined functions

• In line numbers 4, 5 and 6, user-defined functions are declared

• In line numbers 23 to 34, they are defined

• In line numbers 15, 16 and 17, they are called

• Line numbers 23, 27 and 31 consist of headers of the functions println, add and sub

• The variables declared in the function headers or function declarations are known as parameters

• In line numbers 6, x and y are the parameter names

• In line numbers 27 and 31, a and b are the parameter names

• The parameters declared inside the function headers are similar to the variables declared inside the body of the function

• main is also a user-defined function

 ## Write a program to show how user-defined function is called.

 
```c
  int add(int,int); /* function prototype */
void main()
{
   int x=1,y=2,z;
   z=add(x,y); /*     FUNCTION call/
   printf(“z=%d”,z);
}

/* FUNCTION DEFINITION */
int add(int a, int b);
{
   return(a+b);
}
```
OUTPUT:
```
z=3
```
## Explanation:

In the above program, values of ‘x’ and ‘y’ are passed to function add(). 
Formal arguments ‘a’ and ‘b’ receive the values. The function add() calculates 
the addition of both the variables and returns result. The result is collected by the
variable ‘z’ of the main() function which is printed through the printf() statement.

## Write a program to define a user-defined function. Call them at different places.
```c
  void y();
void y()
{
   printf(“Y”);
}

void main()
{
   void a(),b(),c(),d();
   clrscr();
   y();
   a();
   b();
   c();
   d();
}

void a()
{
   printf(“A”);
   y();
}
void b()
{
   printf(“B”);
   a();
}

void c()
{
   a();
   b();
   printf(“C”);
}

void d()
{
   printf(“D”);
   c();
   b();
   a();
}
```
OUTPUT:
```
Y A Y B A Y A Y B A Y C D A Y B A Y C B A Y A Y
```
## Explanation:

From the above program we can conclude that.

The main() function can call any other function defined before or after the main() function.
 

Any other user-defined function can call the main() function.
 

The user-defined function can call only those user-defined functions which are defined before 
it, i.e. the function a() can call only y() and not b(), c() and d(). The function b() cannot 
call functions c() and d(). The function d() can call all the functions because it is the last function.
(f) Local and global variables: There are two kinds of variables: (i) local and (ii) global.

Local variable: The local variables are defined within the body of the function or block. 
The variable defined is local to that function or block only. Other functions cannot access 
these variables. The compiler shows errors in case other functions try to access the variables.


## Write a program to show how similar variable names can be used in different functions.

 ```c

  void fun(void);
void main()
{
   int b=10,c=5;
   clrscr();
   printf(“\n In main() B=%d C=%d”,b,c);
   fun();
}

void fun()
{
   int b=20,c=10;
   printf(“\nIn fun() B=%d C=%d”,b,c);
}
```
OUTPUT:
```
In main() B=10 C=5
In fun() B=20 C=10
```

## Explanation:

In the above program, two functions are used. One is main() and the other user-defined function is fun(). 
The variables ‘b’ and ‘c’ are defined in both the functions. Their effect is only within the 
function in which they are defined. Both the functions print local values of ‘b’ and ‘c’ assigned in their functions.

We can also declare the same variable names for actual and formal arguments. The compiler 
will not get confused due to same variable names. The scope of every auto variable is local to
the block in which they are defined.

Global variables: Global variables are defined outside the main() function. Multiple functions 
can use them. The example is illustrated below for understanding.

## Write a program to show the effect of global variables on different functions.

```c
  void fun(void);
int b=10,c=5;
void main()
{
   clrscr();
   printf(“\nIn main() B=%d C=%d”,b,c);
   fun();
   b++;
   c--;
   printf(“\n Again In main() B=%d C=%d”,b,c);
}

void fun()
{
   b++;
   c--;
   printf(“\nIn fun() B=%d C=%d”,b,c);
}
```
OUTPUT:
```
In main()       B=10 C=5
In fun()        B=11 C=4
Again In main() B=12 C=3
```
Explanation:

In the above program variables ‘b’ and ‘c’ are defined outside the main(), hence they are global. 
They can be called by any other function. The same variables ‘b’ and ‘c’ are used throughout the 
program. In main(), values of ‘b’ and ‘c’ are printed.

The function fun() is called; 'b’ is incremented and ‘c’ is decremented. The values of ‘b’ and
‘c’ are printed. The control then returns to the function main().

Again ‘b’ is incremented and ‘c’ is decremented. The values of ‘b’ and ‘c’ are printed. Here, 
both the functions use the same variables.

(g) Return value: It is the outcome of the function. The result obtained by the function is sent
back to the calling function through the return statement. The return statement returns one 
value per call. The value returned is collected by the variable of the calling function.

## Write a program to show the effect of global variables on different functions.

```c 

  void fun(void);
int b=10,c=5;
void main()
{
   clrscr();
   printf(“\nIn main() B=%d C=%d”,b,c);
   fun();
   b++;
   c--;
   printf(“\n Again In main() B=%d C=%d”,b,c);
}

void fun()
{
   b++;
   c--;
   printf(“\nIn fun() B=%d C=%d”,b,c);
}
```
OUTPUT:
```
In main()       B=10 C=5
In fun()        B=11 C=4
Again In main() B=12 C=3
```
## Explanation:

In the above program variables ‘b’ and ‘c’ are defined outside the main(), 
hence they are global. They can be called by any other function. The same variables ‘b’ and ‘c’ 
are used throughout the program. In main(), values of ‘b’ and ‘c’ are printed.

The function fun() is called; 'b’ is incremented and ‘c’ is decremented. The values of ‘b’ and
‘c’ are printed. The control then returns to the function main().

Again ‘b’ is incremented and ‘c’ is decremented. The values of ‘b’ and ‘c’ are printed. 
Here, both the functions use the same variables.

(g) Return value: It is the outcome of the function. The result obtained by the 
function is sent back to the calling function through the return statement. 
The return statement returns one value per call. The value returned is collected by the variable of the calling function.

## Write a program to pass values to user-defined function. Collect and display the values returned by the called function.

 
```c
  int main()
{
   int dat(int, int, int);
   int d,m,y,t;
   clrscr();
   printf(“Enter Date dd/mm/yy :”);
   scanf(“%d %d %d”,&d,&m,&y);
   t=dat(d,m,y);
   printf(“\nTomorrow = %d/%d/%d”,t,m,y);
   return 0;
}

dat (int x, int y, int z)
{
   printf(“\nToday = %d/%d/%d”,x,y,z);
   return(++x);
}
```
OUTPUT:
```
Enter Date dd/mm/yy : 12 12 2001
Today = 12/12/2001
Tomorrow = 13/12/2001
```
## Explanation:

In the above program, three values date, month and year are passed to the function dat(). 
The function displays date. The function dat() returns the next date. 
The next date is printed in function main(). Here, function dat() receives arguments and return values.

## Write a program to send values to user-defined function and receive and display the return value.
```c
  int main()
{
   int sum(int,int,int), a,b,c,s;
   clrscr();
   printf(“Enter Three Numbers :”);
   scanf(“%d %d %d”, &a,&b,&c);
   s=sum(a,b,c);
   printf(“Sum = %d”,s);
   return 0;
}
int sum(int x, int y, int z)
{
   return(x+y+z);
}
```
OUTPUT:
```
Enter Three Numbers : 7 5 4
Sum = 16
```
## Explanation:

In the above program, the function sum() receives three values from the function main().
The sum() calculates the sum of three numbers and returns them to main().
