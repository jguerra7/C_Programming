# C for Loop
In this section, you will learn to create for loop in C programming with the help of examples.

In programming, loops are used to repeat a block of code until a specified condition is met.

C programming has three types of loops:
```
for loop
while loop
do...while loop
```
We will learn about for loop in this tutorial. In the next tutorial, we will learn about while and do...while loop.

## for Loop
The syntax of the for loop is:
```c
for (initializationStatement; testExpression; updateStatement)
{
    // statements inside the body of loop
}
```
## How for loop works?
```
The initialization statement is executed only once.
Then, the test expression is evaluated. If the test expression is evaluated to false, the for loop is terminated.
However, if the test expression is evaluated to true, statements inside the body of for loop are executed, and the update expression is updated.
Again the test expression is evaluated.
```
This process goes on until the test expression is false. When the test expression is false, the loop terminates.



## for loop Flowchart
![image](https://user-images.githubusercontent.com/47218880/66161380-c6668f80-e5f1-11e9-8691-2c228a04b146.png)

## Example 1: for loop
```c
 # Print numbers from 1 to 10
#include <stdio.h>
int main() {
  int i;
  for (i = 1; i < 11; ++i)
  {
    printf("%d ", i);
  }
  return 0;
}
```
Output
```
1 2 3 4 5 6 7 8 9 10
```
```
i is initialized to 1.
The test expression i < 11 is evaluated. Since 1 less than 11 is true, the body of for loop is executed. This will print the 1 (value of i) on the screen.
The update statement ++i is executed. Now, the value of i will be 2. Again, the test expression is evaluated to true, and the body of for loop is executed. This will print 2 (value of i) on the screen.
Again, the update statement ++i is executed and the test expression i < 11 is evaluated. This process goes on until i becomes 11.
When i becomes 11, i < 11 will be false, and the for loop terminates.
```
## Example 2: for loop
```c
// Program to calculate the sum of first n natural numbers
// Positive integers 1,2,3...n are known as natural numbers
#include <stdio.h>
int main()
{
    int num, count, sum = 0;
    printf("Enter a positive integer: ");
    scanf("%d", &num);
    // for loop terminates when num is less than count
    for(count = 1; count <= num; ++count)
    {
        sum += count;
    }
    printf("Sum = %d", sum);
    return 0;
}
```
Output
```
Enter a positive integer: 10
Sum = 55
```
```
The value entered by the user is stored in the variable num. Suppose, the user entered 10.

The count is initialized to 1 and the test expression is evaluated. Since the test expression count<=num (1 less than or equal to 10) is true, the body of for loop is executed and the value of sum will equal to 1.

Then, the update statement ++count is executed and the count will equal to 2. Again, the test expression is evaluated. Since 2 is also less than 10, the test expression is evaluated to true and the body of for loop is executed. Now, the sum will equal 3.

This process goes on and the sum is calculated until the count reaches 11.

When the count is 11, the test expression is evaluated to 0 (false), and the loop terminates.

Then, the value of sum is printed on the screen.
```
## C while and do...while Loop
In this section, you will learn to create while and do...while loop in C programming with the help of examples.

In programming, loops are used to repeat a block of code until a specified condition is met.


In the previous section, we learned about for loop. In this tutorial, we will learn about while and do..while loop.

## while loop
The syntax of the while loop is:
```c
while (testExpression) 
{
    // statements inside the body of the loop 
}
```
##  How while loop works?
```
The while loop evaluates the test expression inside the parenthesis ().
If the test expression is true, statements inside the body of while loop are executed. Then, the test expression is evaluated again.
The process goes on until the test expression is evaluated to false.
If the test expression is false, the loop terminates (ends).

```
## Flowchart of while loop
![image](https://user-images.githubusercontent.com/47218880/66161397-d2eae800-e5f1-11e9-9f08-174f56b204a8.png)

Example 1: while loop
```c
// Print numbers from 1 to 5
#include <stdio.h>
int main()
{
    int i = 1;
    
    while (i <= 5)
    {
        printf("%d\n", i);
        ++i;
    }
    return 0;
}
```
Output
```
1
2
3
4
5
```
Here, we have initialized i to 1.
```
When i is 1, the test expression i <= 5 is true. Hence, the body of the while loop is executed. This prints 1 on the screen and the value of i is increased to 2.
Now, i is 2, the test expression i <= 5 is again true. The body of the while loop is executed again. This prints 2 on the screen and the value of i is increased to 3.
This process goes on until i becomes 6. When i is 6, the test expression i <= 5 will be false and the loop terminates.
```
## do...while loop
The do..while loop is similar to the while loop with one important difference. The body of do...while loop is executed at least once. Only then, the test expression is evaluated.

The syntax of the do...while loop is:
```c
do
{
   // statements inside the body of the loop
}
while (testExpression);
```
## How do...while loop works?
```
The body of do...while loop is executed once. Only then, the test expression is evaluated.
If the test expression is true, the body of the loop is executed again and the test expression is evaluated.
This process goes on until the test expression becomes false.
If the test expression is false, the loop ends.
```
## Flowchart of do...while Loop
![image](https://user-images.githubusercontent.com/47218880/66161365-be0e5480-e5f1-11e9-9ddf-98459bc02bef.png)
Example 2: do...while loop
```c
// Program to add numbers until the user enters zero
#include <stdio.h>
int main()
{
    double number, sum = 0;
    // the body of the loop is executed at least once
    do
    {
        printf("Enter a number: ");
        scanf("%lf", &number);
        sum += number;
    }
    while(number != 0.0);
    printf("Sum = %.2lf",sum);
    return 0;
}
```
Output
```
Enter a number: 1.5
Enter a number: 2.4
Enter a number: -3.4
Enter a number: 4.2
Enter a number: 0
Sum = 4.70
```








