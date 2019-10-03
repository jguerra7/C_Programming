
# Group Discussion Questions

1. Run Listing 4.1 again, but this time give your first and last name when it asks you for your first name. What happens? Why?

2. Assuming that each of the following examples is part of a complete program, what will each one print?

a.
```c
printf("He sold the painting for $%2.2f.\n", 2.345e2);
```
b.
```c
printf("%c%c%c\n", 'H', 105, '\41');
```
c.
```c
#define Q "His Hamlet was funny without being vulgar."

   printf("%s\nhas %d characters.\n", Q, strlen(Q));
```
d.
```c
printf("Is %2.2e the same as %2.2f?\n", 1201.0, 1201.0);
```
3. In Question 2c, what changes could you make so that string Q is printed out enclosed in double quotation marks?

4. It’s find the error time!

```c

define B booboo
define X 10
main(int)
{
   int age;
   char name;

   printf("Please enter your first name.");
   scanf("%s", name);
   printf("All right, %c, what's your age?\n", name);
   scanf("%f", age);
   xp = age + X;
   printf("That's a %s! You must be at least %d.\n", B, xp);
   rerun 0;
}
```
5. Suppose a program starts as follows:
```c
#define BOOK "War and Peace"
int main(void)
{
   float cost =12.99;
   float percent = 80.0;
```
Construct a printf() statement that uses BOOK, cost, and percent to print the following:
```c
This copy of "War and Peace" sells for $12.99.
That is 80% of list.
```
6. What conversion specification would you use to print each of the following?

a. A decimal integer with a field width equal to the number of digits

b. A hexadecimal integer in the form 8A in a field width of 4

c. A floating-point number in the form 232.346 with a field width of 10

d. A floating-point number in the form 2.33e+002 with a field width of 12

e. A string left-justified in a field of width 30

7. Which conversion specification would you use to print each of the following?

a. An unsigned long integer in a field width of 15

b. A hexadecimal integer in the form 0x8a in a field width of 4

c. A floating-point number in the form 2.33E+02 that is left-justified in a field width of 12

d. A floating-point number in the form +232.346 in a field width of 10

e. The first eight characters of a string in a field eight characters wide

8. What conversion specification would you use to print each of the following?

a. A decimal integer having a minimum of four digits in a field width of 6

b. An octal integer in a field whose width will be given in the argument list

c. A character in a field width of 2

d. A floating-point number in the form +3.13 in a field width equal to the number of characters in the number

e. The first five characters in a string left-justified in a field of width 7

9. For each of the following input lines, provide a scanf() statement to read it. Also declare any variables or arrays used in the statement.

a. 101

b. 22.32 8.34E−09

c. linguini

d. catch 22

e. catch 22 (but skip over catch)

10. What is whitespace?

11. What’s wrong with the following statement and how can you fix it?
```c

printf("The double type is %z bytes..\n", sizeof (double));
```
12. Suppose that you would rather use parentheses than braces in your programs. How well would the following work?
```c
#define ( {
#define ) }
```
