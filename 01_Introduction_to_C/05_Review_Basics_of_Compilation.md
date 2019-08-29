# Compilation Basics Review

Having covered the basic concepts of C programming, we can now briefly discuss the process of compilation.

Like any programming language, C by itself is completely incomprehensible to a microprocessor. Its purpose is to provide an intuitive way for humans to provide instructions that can be easily converted into machine code that is comprehensible to a microprocessor. The compiler is what translates our human-readable source code into machine code.

To those new to programming, this seems fairly simple. A naive compiler might read in every source file, translate everything into machine code, and write out an executable. That could work, but has two serious problems. First, for a large project, the computer may not have enough memory to read all of the source code at once. Second, if you make a change to a single source file, you would have to recompile the entire application.

To deal with these problems, compilers break the job into steps. For each source file (each .c file), the compiler reads the file, reads the files it references via the #include directive, and translates them to machine code. The result of this is an "object file" (.o). After all the object files are created, a "linker" program collects all of the object files and writes the actual executable program. That way, if you change one source file, only that file needs to be recompiled, after which, the application will need to be re-linked.

Without going into details, it can be beneficial to have a superficial understanding of the compilation process.

## Preprocessor
The preprocessor provides the ability for the inclusion of so called header files, macro expansions, conditional compilation and line control. Many times you will need to give special instructions to your compiler. This can be done by inserting preprocessor directives into your code. When you begin compiling your code, a special program called the preprocessor scans the source code and performs simple substitution of token strings for others according to predefined rules. The C preprocessor is not a part of the C language.

All preprocessor directives begin with the hash character (#). You can see one preprocessor directive in the Hello world program. Example:
```c
 #include <stdio.h>
``` 
This directive causes the stdio header to be included into your program. Other directives such as #pragma control compiler settings and macros. The result of the preprocessing stage is a text string. You can think of the preprocessor as a non-interactive text editor that prepares your code for compilation. The language of preprocessor directives is agnostic to the grammar of C, so the C preprocessor can also be used independently to process other kinds of text files.

## Syntax Checking
This step ensures that the code is valid and will sequence into an executable program. Under most compilers, you may get messages or warnings indicating potential issues with your program (such as a conditional statement always being true or false, etc.)

When an error is detected in the program, the compiler will normally report the file name and line that is preventing compilation.

## Object Code
The compiler produces a machine code equivalent of the source code that can be linked into the final program. At this point the code itself can't be executed, as it requires linking to do so.

It's important to note after discussing the basics that compilation is a "one way street". That is, compiling a C source file into machine code is easy, but "decompiling" (turning machine code into the C source that creates it) is not. Decompilers for C do exist, but the code they create is hard to understand and only useful for reverse engineering.

## Linking
Linking combines the separate object files into one complete program by integrating libraries and the code and producing either an executable program or a library. Linking is performed by a linker program, which is often part of a compiler suite.

Common errors during this stage are either missing or duplicate functions.

## Automation
For large C projects, many programmers choose to automate compilation, both in order to reduce user interaction requirements and to speed up the process by recompiling only modified files.

Most Integrated Development Environments (IDE's) have some kind of project management which makes such automation very easy. However, the project management files are often usable only by users of the same integrated development environment, so anyone desiring to modify the project would need to use the same IDE.

On UNIX-like systems, make and Makefiles are often used to accomplish the same. Make is traditional and flexible and is available as one of the standard developer tools on most Unix and GNU distributions.

Makefiles have been extended by the GNU Autotools, composed of Automake and Autoconf for making software compilable, testable, translatable and configurable on many types of machines. Automake and Autoconf are described in detail in their respective manuals.

The Autotools are often perceived to be complicated and various simpler build systems have been developed. Many components of the GNOME project now use the declarative Meson build system which is less flexible, but instead focuses on providing the features most commonly needed from a build system in a simple way. Other popular build systems for programs written in the C language include CMake and Waf.

Once gcc is installed, it can be called with a list of c source files that have been written but not yet compiled. e.g. if the file main.c includes functions described in myfun.h and implemented in myfun_a.c and myfun_b.c, then it is enough to write
```c
 gcc   main.c myfun_a.c myfun_b.c 
```
myfun.h is included in main.c, but if it is in a separate header file directory, then that directory can be listed after a "-I " switch.

In larger programs, Makefiles and gnu make program can compile c files into intermediate files ending with suffix .o which can be linked by gcc.

How to compile each object file is usually described in the Makefile with the object file as a label ending with a colon followed by two spaces (tabs often cause problems) followed by a list of other files that are dependencies, e.g. .c files and .o files compiled in another section, and on the next line, the invocation of gcc that is required.

Typing man make or info make often gives the information needed to on how to use make, as well as gcc.

Although gcc has a lot of option switches, one often used is -g to generate debugging information for gdb to allow gdb to show source code during a step-through of the machine code program. gdb has an 'h' command that shows what it can do, and is usually started with 'gdb a.out' if a.out is the anonymous executable machine code file that was compiled by gcc.
