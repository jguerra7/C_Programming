##  Escape Sequences
Sometimes, it is necessary to use characters that cannot be typed or has special meaning in C programming. For example: newline(enter), tab, question mark etc.

In order to use these characters, escape sequences are used.

> Escape Sequences
**Escape Sequences**	**Character**
```
\b	Backspace
\f	Form feed
\n	Newline
\r	Return
\t	Horizontal tab
\v	Vertical tab
\\	Backslash
\'	Single quotation mark
\"	Double quotation mark
\?	Question mark
\0	Null character
```
For example: \n is used for a newline. The backslash \ causes escape from the normal way the characters are handled by the compiler.

## String Literals
A string literal is a sequence of characters enclosed in double-quote marks. For example:
```
"good"                  //string constant
""                     //null string constant
"      "               //string constant of six white space
"x"                    //string constant having a single character.
"Earth is round\n"         //prints string with a newline
```
## Constants
If you want to define a variable whose value cannot be changed, you can use the const keyword. This will create a constant. For example,
```c
const double PI = 3.14;
```
Notice, we have added keyword const.

Here, PI is a symbolic constant; its value cannot be changed.
```c
const double PI = 3.14;
PI = 2.9; //Error
```
You can also define a constant using the #define preprocessor directive. 
