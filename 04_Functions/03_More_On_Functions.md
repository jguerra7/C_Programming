#  What is a Function?
A function is combined of a block of code that can be called or used anywhere in the program by calling the name. Body of a function starts with { and ends with } . This is similar to the main function. Example below shows how we can write a simple function.
```c
#include<stdio.h> 

/*Function prototypes*/ 
myfunc();
 
main() 
{ 
    myfunc();  
}

/*Function Defination*/ 
myfunc() 
{ 
    printf("Hello, this is a test\n"); 
} 
```
In above example we have put a section of program in a separate function. 
Function body can be very complex though. 
After creating a function we can call it using its name. 
Functions can also call each other. A function can even call itself.

By the way pay attention to function prototypes section. 
In some C compilers we are needed to introduce the functions
we are creating in a program above the program. 
Introducing a function is being called function prototype.

Note:
```
Any C program contains at least one function.

If a program contains only one function, it must be main().

If a C program contains more than one function, then one (and only one) of these functions must be main(), 
because program execution always begins with main().

There is no limit on the number of functions that might be present in a C program.

Each function in a program is called in the sequence specified by the function calls in main().

After each function has done its thing, control returns to main(). When main() 
runs out of function calls, the program ends.
```
##  Why Use Functions
Why write separate functions at all? Why not squeeze the entire
logic into one function, main()? Two reasons:

Writing functions avoids rewriting the same code over and over.
Using functions it becomes easier to write programs and keep track of what 
they are doing. If the operation of a program can be divided into separate activities,
and each activity placed in a different function, then each could be written and checked 
more or less independently. Separating the code into modular functions also 
makes the program easier to design and understand.

What is the moral of the story? Don’t try to cram the entire logic in one function. 
It is a very bad style of programming. Instead, break a program into small units and 
write functions for each of these isolated subdivisions. Don’t hesitate to write 
functions that are called only once. What is important is that these functions perform some logically isolated task.

## Function arguments
Functions are able to accept input parameters in the form of variables. 
These input parameter variables
can then be used in function body.
```c
#include<stdio.h> 
/* use function prototypes */ 
sayhello(int count);
main()
{ 
    sayhello(4);  
} 

sayhello(int count) 
{ 
    int c; 
    for(c=0;c<count;c++) 
        printf("Hello\n"); 
} 
```
In above example we have called sayhello() function with the parameter 4. 
This function receives an input value and assigns it to count variable before 
starting execution of function body. sayhello() function will then print a hello message count times on the screen.

## Function return values
In mathematics we generally expect a function to return a value. 
It may or may not accept arguments but it always returns a value.

This return value has a type as other values in C. It can be int,
float, char or anything else. Type of this return value determines type of your function.

Default type of function is int or integer. If you do not indicate type of function that you use, it will be of type int. As we told earlier every function must return a value. We do this with return command.
```c
int sum() 
{ 
    int a,b,c; 
    a=1; 
    b=4; 
    c=a+b; 
    reurn c; 
}
```
Above function returns the value of variable c as the return value of function. 
We can also use expressions in return command. For example we can replace two last 
lines of function with return a+b; If you forget to return a value in a function 
you will get a warning message in most of C compilers. This message will warn you 
that your function must return a value. Warnings do not stop program execution but errors stop it.

In our previous examples we did not return any value in our functions.
For example you must return a value in main() function.
```c
main() 
{ 
    . 
    . 
    . 
    return 0; 
} 
```
Default return value for an int type function is 0. If you do not insert return 0 
or any other value in your main() function a 0 value will be returned automatically. 
If you are planning to return an int value in your function, it is seriously preferred
to mention the return value in your function header and make.

## void return value
There is another void type of function in C language. Void type function is
a function that does not return a value. You can define a function that does not need a return value as void.
```c
void test () 
{ 
    /* fuction code comes here but no return value */ 
}
```
void functions cannot be assigned to a variable because it does not return value. So you cannot write:
```
a=test(); 
```
Using above command will generate an error.

## Recursive Function
In C, it is possible for the functions to call themselves. 
A function is called recursive if a statement within the body of a function calls the same function.

Following is the recursive function to calculate the factorial value.
```c
#include<stdio.h>
int rec(int);
main() 
{ 
    int a, fact ; 
    printf("\nEnter any number "); 
    scanf ("%d", &a); 
    fact = rec(a); 
    printf ("Factorial value = %d", fact); 
} 
int rec (int x) 
{ 
    int f; 
    if (x == 1) 
        return (1); 
    else 
        f = x * rec (x - 1) ; 
    return (f) ; 
}
```
Output-
```
Enter any number 5 
Factorial value = 120
```
Let us understand this recursive factorial function.

what happens is,
```c
rec(5) returns(5 * rec(4), 
 which returns (4 * rec(3), 
  which returns (3 * rec(2), 
   which returns (2 * rec(1), 
    which returns (1)))))
```
Foxed? Well, that is recursion for you in its simplest garbs. I hope you agree that it’s difficult to visualize how the control flows from one function call to another. Possibly Following figure would make things a bit clearer.

![image](https://user-images.githubusercontent.com/47218880/66239267-0d6e8680-e6bf-11e9-8da1-fdb8bcca4f4a.png)


## Multiple Parameters
In fact you can use more than one argument in a function. Following example will show you how you can do this.
```c
#include<stdio.h> 
int min(int a,int b); 
main() 
{ 
    int m; 
    m=min(3,6); 
    printf("Minimum is %d",m);  
    return 0; 
} 
int min(int a,int b) 
{ 
    if(a<b) 
        return a; 
    else 
        return b; 
} 
```
As you see you can add your variables to arguments list easily.

## Call by value
C programming language function calls, use call by value method. Let’s see an example to understand this subject better.
```c
#include<stdio.h> 
void test(int a); 
main() 
{ 
    int m; 
    m=2; 
    printf("\nM is %d",m); 
    test(m); 
    printf("\nM is %d\n",m); 
    return 0; 
} 
void test(int a) 
{ 
    a=5; 
} 
```
In main() function, we have declared a variable m. We have assigned value 2 to m. 
We want to see if function call is able to change value of m as we have modified 
value of incoming parameter inside test() function.

Program output result is:
```
M is 2 
M is 2
```
So you see function call has not changed the value of argument. This s is because 
function-calling method only sends value of variable m to the function and it does 
not send variable itself. Actuallyit places value of variable m in a memory location 
called stack and then function retrieves the value without having access to main 
variable itself. This is why we call this method of calling "call by value".

## Call by reference
There is another method of sending variables being called "Call by reference". 
This second method enables function to modify value of argument variables used in function call.

We will first see an example and then we will describe it.
```c
#include<stdio.h> 
void test(int *ptr); 
main() 
{ 
    int m; 
    m=2; 
    printf("\nM is %d",m); 
    test(&m); 
    printf("\nM is %d\n",m); 
    return 0; 
} 
void test(int *ptr) 
{ 
    printf("\nModifying the value inside memory address%ld",&m); 
    *ptr=5; 
} 
```
To be able to modify the value of a variable used as an argument in a function,
function needs to know memory address of the variable (where exactly the variable is situated in memory).

In C programming language & operator gives the address at which the variable is stored.
For example if m is a variable of type int then &m will give us the starting memory 
address of our variable.We call this resulting address a pointer.
```
ptr=&m;
```
In above command ptr variable will contain memory address of variable m. 
This method is used in some of standard functions in C. For example scanf 
function uses this method to be able to receive values from console keyboard 
and put it in a variable. In fact it places received value in memory location 
of the variable used in function. Now we understand the reason why we add &
sign before variable names in scanf variables.
```
scanf(“%d”,&a);
```
Now that we have memory address of variable we must use an operator
that enables us to assign a value or access to value stored in that address.

As we told, we can find address of variable a using & operator.
```
ptr=&a; 
```
Now we can find value stored in variable a using * operator:
```
val=*ptr; /* finding the value ptr points to */
```
We can even modify the value inside the address:
```
*ptr=5; 
```
Let’s look at our example again. We have passed pointer (memory address) to function.
Now function is able to modify value stored inside variable. If yourun the program, you will get these results:
```
M is 2 
Modifying the value inside memory address 2293620
M is 5
```
So you see this time we have changed value of an argument variable inside the called
function (by modifying the value inside the memory location of our main variable).
