The "Hello, World!" Program
Tradition dictates that we begin with a very simple program, which simply displays the characters "Hello, World!" on the screen and immediately exits. Type the following source code in your preferred text editor/IDE and save this in a file named **hello.c.**
```c
#include <stdio.h>

int main(void)
{
    printf("Hello, World!\n");
    return 0;
}
```
Source code analysis
Below are described the parts the program is composed of. The various details will be introduced and explained in later chapters.

#include <stdio.h>
This is a preprocessor directive. Preprocessor directives instruct a part of the compiler - the preprocessor - to modify the code we've written before it is compiled. In this case, the #include directive retrieves C code from the stdio.h file found in the standard library. Files used in this way are called header files and are saved with the .h extension. The stdio.h file contains many functions defined according to the C standard. For this program, the only function we need from stdio.h is the printf function.

int main(void)
The function named main is the starting point of all C programs. In computer science, the term function tends to be used a bit more loosely than in mathematics, since functions often express imperative ideas (as in the case of C) - that is, how-to process, instead of declarations. For now, suffice it to say, functions let us define a complex process that we want to reference frequently.

    printf("Hello World!\n");
This line is of particular interest because it produces the actual output on the console (also known as the terminal in the context of Unix-like operating systems), a traditional text-based interface to system utilities and programs.

    return 0;
When terminating our program, it is useful to be able to let the operating system know whether or not the program succeeded. We do this with an exit status, which is sent to the operating system with a return statement in the main function. In this case, we provide an exit status of 0 to indicate that execution succeeded without error. As our programs grow in complexity, we can use other integers as codes to indicate various types of errors. This style of providing exit status is a long standing convention[1].

Compiling
Unix-like
If you are using a Unix(-like) system, such as GNU/Linux, Mac OS X, or Solaris, it will probably have GCC installed, otherwise on Linux you can install it using yum or apt-get commands depending on your distribution. Open the virtual console or a terminal emulator and enter the following (be certain your current working directory is the one containing your source code):

gcc hello.c
By default gcc will generate our executable binary with the name a.out. To run your new generated program type:

./a.out
You should see Hello, World! printed after the last prompt.

To see the exit status of the last program you ran, type on your shell command:

echo $?
This shows the value the main function has returned, which is 0 in the above example.

There are a lot of options you can use with the gcc compiler. For example, if you want the output to have a name other than a.out, you can use the -o option. The following shows a few examples:

-o
indicates that the next parameter is the name of the resulting program (or library). If this option is not specified, the compiled program will, for historic reasons, end up in a file called "a.out" or "a.exe" (for cygwin users).
-Wall
indicates that gcc should warn about many types of suspicious code that are likely to be incorrect.
You can use these options to create a program called "helloworld" instead of "a.out" by typing:

gcc -o helloworld hello.c -Wall
Now you can run it by typing:

./helloworld
All the options are well documented in the manual[2] for GCC.

On IDEs
If you are using an IDE you may have to select console project, and to compile you just select build from the menu or the toolbar. The executable will appear inside the project folder, but you should have a menu button so you can just run the executable from the IDE. The process is roughly the same on all IDEs.
