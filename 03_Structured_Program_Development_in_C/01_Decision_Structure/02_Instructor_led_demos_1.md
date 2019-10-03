# if...else Statement
In this section, you will learn about if statement (including if...else and nested if..else) in C programming with the help of examples.

## C if Statement
The syntax of the if statement in C programming is:
```c
if (test expression) 
{
   // statements to be executed if the test expression is true
}
```
##  How if statement works?
The if statement evaluates the test expression inside the parenthesis ().
```
If the test expression is evaluated to true, statements inside the body of if are executed.
If the test expression is evaluated to false, statements inside the body of if are not executed.
```
![image](https://user-images.githubusercontent.com/47218880/66153795-c199df80-e5e1-11e9-9c05-391d3ba80597.png)

## How if statement works in C programming?

## Example 1: if statement
```c
// Program to display a number if it is negative
#include <stdio.h>
int main()
{
    int number;
    printf("Enter an integer: ");
    scanf("%d", &number);
    // true if number is less than 0
    if (number < 0)
    {
        printf("You entered %d.\n", number);
    }
    printf("The if statement is easy.");
    return 0;
}
```
Output 1
```
Enter an integer: -2
You entered -2.
The if statement is easy.
```
When the user enters -2, the test expression number<0 is evaluated to true. Hence, You entered -2 is displayed on the screen.

Output 2
```
Enter an integer: 5
The if statement is easy.
```
When the user enters 5, the test expression number<0 is evaluated to false and the statement inside the body of if is not executed

## C if...else Statement
The if statement may have an optional else block. The syntax of the if..else statement is:
```c
if (test expression) {
    // statements to be executed if the test expression is true
}
else {
    // statements to be executed if the test expression is false
}
```
## How if...else statement works?
If the test expression is evaluated to true,
```
statements inside the body of if are executed.
statements inside the body of else are skipped from execution.
```
If the test expression is evaluated to false,
```
statements inside the body of else are executed
statements inside the body of if are skipped from execution.
```
![image](https://user-images.githubusercontent.com/47218880/66153818-cbbbde00-e5e1-11e9-91de-81a6034cc055.png)

## Example 2: if...else statement
```c
// Check whether an integer is odd or even
#include <stdio.h>
int main()
{
    int number;
    printf("Enter an integer: ");
    scanf("%d", &number);
    // True if the remainder is 0
    if  (number%2 == 0) 
    {
        printf("%d is an even integer.",number);
    }
    else
    {
        printf("%d is an odd integer.",number);
    }
    return 0;
}
```
Output
```
Enter an integer: 7
7 is an odd integer.
```
When the user enters 7, the test expression number%2==0 is evaluated to false. Hence, the statement inside the body of else is executed.

## C if...else Ladder
The if...else statement executes two different codes depending upon whether the test expression is true or false. Sometimes, a choice has to be made from more than 2 possibilities.

The if...else ladder allows you to check between multiple test expressions and execute different statements.

## Syntax of nested if...else statement.
```c
if (test expression1) 
{
   // statement(s)
}
else if(test expression2) 
{
   // statement(s)
}
else if (test expression3) 
{
   // statement(s)
}
.
.
else 
{
   // statement(s)
}
```
## Example 3: C if...else Ladder
```c
// Program to relate two integers using =, > or < symbol
#include <stdio.h>
int main()
{
    int number1, number2;
    printf("Enter two integers: ");
    scanf("%d %d", &number1, &number2);
    //checks if the two integers are equal.
    if(number1 == number2)
    {
        printf("Result: %d = %d",number1,number2);
    }
    //checks if number1 is greater than number2.
    else if (number1 > number2)
    {
        printf("Result: %d > %d", number1, number2);
    }
    //checks if both test expressions are false
    else
    {
        printf("Result: %d < %d",number1, number2);
    }
    return 0;
}
```
Output
```
Enter two integers: 12
23
Result: 12 < 23
```
## Nested if...else
It is possible to include an if...else statement inside the body of another if...else statement.

## Example 4: Nested if...else
This program given below relates two integers using either <, > and = similar to the if...else ladder's example. However, we will use a nested if...else statement to solve this problem.
```c
#include <stdio.h>
int main()
{
    int number1, number2;
    printf("Enter two integers: ");
    scanf("%d %d", &number1, &number2);
    if (number1 >= number2)
    {
      if (number1 == number2) 
      {
        printf("Result: %d = %d",number1,number2);
      }
      else 
      {
        printf("Result: %d > %d", number1, number2);
      }
    }
    else
    {
        printf("Result: %d < %d",number1, number2);
    }
    return 0;
}
```
If the body of an if...else statement has only one statement, you do not need to use brackets {}.

For example, this code
```c
if (a > b) {
    print("Hello");
}
print("Hi");
```
is equivalent to
```c
if (a > b)
    print("Hello");
print("Hi");
```
# C switch Statement
In this section, you will learn to create the switch statement in C programming with the help of an example.

The switch statement allows us to execute one code block among many alternatives.

You can do the same thing with the if...else..if ladder. However, the syntax of the switch statement is much easier to read and write.

## Syntax of switch...case
```c
switch (expression)
​{
    case constant1:
      // statements
      break;
    case constant2:
      // statements
      break;
    .
    .
    .
    default:
      // default statements
}
```
How does the switch statement work?
```
The expression is evaluated once and compared with the values of each case label.

If there is a match, the corresponding statements after the matching label are executed. For example, if the value of the expression is equal to constant2, statements after case constant2: are executed until break is encountered.
If there is no match, the default statements are executed.
```
If we do not use break, all statements after the matching label are executed.

The default clause inside the switch statement is optional.

switch Statement Flowchart
![image](https://user-images.githubusercontent.com/47218880/66153940-0f164c80-e5e2-11e9-87da-80e475ebd340.png)

## Example: Simple Calculator
```c
// Program to create a simple calculator
#include <stdio.h>
int main() {
    char operator;
    double n1, n2;
    printf("Enter an operator (+, -, *, /): ");
    scanf("%c", &operator);
    printf("Enter two operands: ");
    scanf("%lf %lf",&n1, &n2);
    switch(operator)
    {
        case '+':
            printf("%.1lf + %.1lf = %.1lf",n1, n2, n1+n2);
            break;
        case '-':
            printf("%.1lf - %.1lf = %.1lf",n1, n2, n1-n2);
            break;
        case '*':
            printf("%.1lf * %.1lf = %.1lf",n1, n2, n1*n2);
            break;
        case '/':
            printf("%.1lf / %.1lf = %.1lf",n1, n2, n1/n2);
            break;
        // operator doesn't match any case constant +, -, *, /
        default:
            printf("Error! operator is not correct");
    }
    return 0;
}
```
Output
```
Enter an operator (+, -, *,): -
Enter two operands: 32.5
12.4
32.5 - 12.4 = 20.1
```
The - operator entered by the user is stored in the operator variable. And, two operands 32.5 and 12.4 are stored in variables n1 and n2 respectively.

Since the operator is -, the control of the program jumps to
```
printf("%.1lf / %.1lf = %.1lf", n1, n2, n1/n2);
```
Finally, the break statement terminates the switch statement.












