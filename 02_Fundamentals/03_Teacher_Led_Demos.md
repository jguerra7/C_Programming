# Programming Examples

Program to Find the Size of a variable
```C
#include <stdio.h>
int main()
{
    int integerType;
    float floatType;
    double doubleType;
    char charType;
    // Sizeof operator is used to evaluate the size of a variable
    printf("Size of int: %ld bytes\n",sizeof(integerType));
    printf("Size of float: %ld bytes\n",sizeof(floatType));
    printf("Size of double: %ld bytes\n",sizeof(doubleType));
    printf("Size of char: %ld byte\n",sizeof(charType));
    return 0;
}
```
Output
```
Size of int: 4 bytes
Size of float: 4 bytes
Size of double: 8 bytes
Size of char: 1 byte
```
In this program, 4 variables integerType, floatType, doubleType and charType are declared having int, float, double and char type respectively.

Then, the size of each variable is ascertained using sizeof operator. 

Program to Print an Integer
```c
#include <stdio.h>
int main()
{
    int number;
    // printf() dislpays the formatted output 
    printf("Enter an integer: ");  
    
    // scanf() reads the formatted input and stores them
    scanf("%d", &number);  
    
    // printf() displays the formatted output
    printf("You entered: %d", number);
    return 0;
}
```
Output
```
Enter a integer: 25
You entered: 25
```
In this program, an integer variable number is declared.

The printf() function displays Enter an integer: on the screen. Then, the scanf() function reads an integer data from the user and stores in variable number.

Finally, the value stored in the variable number is displayed on the screen using printf() function.

Program to Add Two Integers
```c
#include <stdio.h>
int main()
{
    int firstNumber, secondNumber, sumOfTwoNumbers;
    
    printf("Enter two integers: ");
    // Two integers entered by user is stored using scanf() function
    scanf("%d %d", &firstNumber, &secondNumber);
    // sum of two numbers in stored in variable sumOfTwoNumbers
    sumOfTwoNumbers = firstNumber + secondNumber;
    // Displays sum      
    printf("%d + %d = %d", firstNumber, secondNumber, sumOfTwoNumbers);
    return 0;
}
```
Output
```
Enter two integers: 12
11
12 + 11 = 23
```
In this program, user is asked to enter two integers. Two integers entered by the user is stored in variables firstNumber and secondNumber respectively. This is done using scanf() function.

Then, variables firstNumber and secondNumber are added using + operator and the result is stored in sumOfTwoNumbers.
Finally, the sumofTwoNumbers is displayed on the screen using printf() function.

Program to Multiply Two Numbers
```c
#include <stdio.h>
int main()
{
    double firstNumber, secondNumber, product;
    printf("Enter two numbers: ");
    // Stores two floating point numbers in variable firstNumber and secondNumber respectively
    scanf("%lf %lf", &firstNumber, &secondNumber);  
 
    // Performs multiplication and stores the result in variable productOfTwoNumbers
    product = firstNumber * secondNumber;  
    // Result up to 2 decimal point is displayed using %.2lf
    printf("Product = %.2lf", product);
    
    return 0;
}
```
Output
```
Enter two numbers: 2.4
1.12
Product = 2.69
```
In this program, user is asked to enter two numbers. These two numbers entered by the user is stored in variable firstNumber and secondNumber respectively. This is done using scanf() function.

Then, the product of firstNumber and secondNumber is evaluated and the result is stored in variable productOfTwoNumbers.

Finally, the productOfTwoNumbers is displayed on the screen using printf() function.

Notice that, the result is round to second decimal place using %.2lf conversion character.

A character variable holds ASCII value (an integer number between 0 and 127) rather than that character itself in C programming. That value is known as ASCII value.

For example, ASCII value of 'A' is 65.

What this means is that, if you assign 'A' to a character variable, 65 is stored in that variable rather than 'A' itself.

Program to Print ASCII Value
```c
#include <stdio.h>
int main()
{
    char c;
    printf("Enter a character: ");
    // Reads character input from the user
    scanf("%c", &c);  
    
    // %d displays the integer value of a character
    // %c displays the actual character
    printf("ASCII value of %c = %d", c, c);
    return 0;
}
```
Output
```
Enter a character: G
ASCII value of G = 71
```
In this program, user is asked to enter a character which is stored in variable c. The ASCII value of that character is stored in variable c rather than that variable itself.

When %d format string is used, 71 (ASCII value of 'G') is displayed.

When %c format string is used, 'G' itself is displayed.

Program to Compute Quotient and Remainder
```c
#include <stdio.h>
int main(){
    int dividend, divisor, quotient, remainder;
    printf("Enter dividend: ");
    scanf("%d", &dividend);
    printf("Enter divisor: ");
    scanf("%d", &divisor);
    // Computes quotient
    quotient = dividend / divisor;
    // Computes remainder
    remainder = dividend % divisor;
    printf("Quotient = %d\n", quotient);
    printf("Remainder = %d", remainder);
    return 0;
}
```
Output
```
Enter dividend: 25
Enter divisor: 4
Quotient = 6
Remainder = 1
```
In this program, user is asked to enter two integers (dividend and divisor) which is stored in variable dividend and divisor respectively.

Then the quotient is evaluated using division / operator and stored in variable quotient.

Similarly, the remainder is evaluated using modulus % operator and stored in remainder variable.

Finally, the quotient and remainder are displayed using printf() function.

# SWAPPING NUMBERS
## Example 1: Program to Swap Numbers Using Temporary Variable
```c
#include <stdio.h>
int main()
{
      double firstNumber, secondNumber, temporaryVariable;
      printf("Enter first number: ");
      scanf("%lf", &firstNumber);
      printf("Enter second number: ");
      scanf("%lf",&secondNumber);
      // Value of firstNumber is assigned to temporaryVariable
      temporaryVariable = firstNumber;
      // Value of secondNumber is assigned to firstNumber
      firstNumber = secondNumber;
      // Value of temporaryVariable (which contains the initial value of firstNumber) is assigned to secondNumber
      secondNumber = temporaryVariable;
      printf("\nAfter swapping, firstNumber = %.2lf\n", firstNumber);
      printf("After swapping, secondNumber = %.2lf", secondNumber);
      return 0;
}
```
 
Output
```
Enter first number: 1.20
Enter second number: 2.45

After swapping, firstNumber = 2.45
After swapping, secondNumber = 1.20
```
In the above program, the temporaryVariable is assigned the value of firstNumber.
Then, the value of firstNumber is assigned to secondNumber.
Finally, the temporaryVariable (which holds the initial value of firstNumber) is assigned to secondNumber which completes the swapping process.

Here, temporaryVariable is used to hold the value of firstNumber and doesn't have any other use except that. You can also write the swapping program without using temporaryVariable.

## Example 2: Program to Swap Number Without Using Temporary Variables
```c
#include <stdio.h>
int main()
{
    double firstNumber, secondNumber;
    printf("Enter first number: ");
    scanf("%lf", &firstNumber);
    printf("Enter second number: ");
    scanf("%lf",&secondNumber);
    // Swapping process
    firstNumber = firstNumber - secondNumber;
    secondNumber = firstNumber + secondNumber;
    firstNumber = secondNumber - firstNumber;
    printf("\nAfter swapping, firstNumber = %.2lf\n", firstNumber);
    printf("After swapping, secondNumber = %.2lf", secondNumber);
    return 0;
}
```
Output
```
Enter first number: 10.25
Enter second number: -12.5

After swapping, firstNumber = -12.50
After swapping, secondNumber = 10.25
```
# Practice Exercises

Write a C program to compute the perimeter and area of a rectangle with a height of 7 inches. and width of 5 inches. 
Expected Output:
```
Perimeter of the rectangle = 24 inches
Area of the rectangle = 35 square inches
```
Write a C program to display multiple variables. 
Sample Variables :
a+ c, x + c,dx + x, ((int) dx) + ax, a + x, s + b, ax + b, s + c, ax + c, ax + ux
Declaration :
int a = 125, b = 12345;
long ax = 1234567890;
short s = 4043;
float x = 2.13459;
double dx = 1.1415927;
char c = 'W';
unsigned long ux = 2541567890;

Expected output
```
a + c =  212                                                           
x + c = 89.134590                                                      
dx + x = 3.276183                                                      
((int) dx) + ax =  1234567891                                          
a + x = 127.134590                                                     
s + b =  16388                                                         
ax + b = 1234580235                                                    
s + c =  4130                                                          
ax + c = 1234567977                                                    
ax + ux = 3776135780
```
 Write a C program to convert specified days into years, weeks and days. 
Note: Ignore leap year.
```
Test Data :
Number of days : 1329
Expected Output :
Years: 3
Weeks: 33
Days: 3
```
Expected Output
```
Years: 3                                                               
Weeks: 33                                                              
Days: 3
```
Write a C program that accepts two integers from the user and calculate the sum of the two integers. 
	Test Data :
	Input the first integer: 25
	Input the second integer: 38
	Expected Output:
```
Sum of the above two integers = 63
```
Write a program that asks the user to enter two numbers, obtains them from the user and prints their sum, product, difference, quotient and remainder.

 Write a program that asks the user to enter two integers, obtains the numbers from the user, then prints the larger number followed by the words “is larger.” If the numbers are equal, print the message “These numbers are equal.” Using only a single-selection form of the if statement. (Challenge)

Write a program that reads in the radius of a circle and prints the circle’s diameter, circumference and area. Use the constant value 3.14159 for π. Perform each of these calculations inside the printf statement(s) and use the conversion specifier %f.

Write a program that reads an integer and determines and prints whether it’s odd or even. [Hint: Use the remainder operator. An even number is a multiple of two. Any multiple of two leaves a remainder of zero when divided by 2.]




