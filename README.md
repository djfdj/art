<<<<<<< HEAD
# masterpiece
=======
# SCE212 Computer Organization and Architecture (Fall 2019)

## Project #0: Implementing a Command Parser

### Due on 11:59:59pm, September 20 (Friday)


### Introduction

The purpose of this project is to bootstrap the term project to implement MIPS simulator, and to get familiar with our project assignment submission system.


### Problem Specification

We will implement a MIPS instruction simulator throughout the class. To that end, you should firstly make the simulator to understand user inputs and commands.

In this project, the framework passes input strings, and your task is to **split the input strings into command tokens**. A string is defined as a sequence of characters which is terminated with `\0`.  A command token is defined as a sequence of characters without whitespaces, where the whitespaces include spaces(' ') and tab characters('`\t`').

For example, if the input string is " Hello   world ", the command tokes are "Hello" and "world". **Note that the tokens do not include any space characters**. Another example is for an input string "add   t0   t1   t2"; it should be broken into "add", "t0", "t1", and "t2".

This feature should be implemented in `parse_command()` function. The user input is passed through `command`. After parsing `command` into tokens, the tokens should be assigned to `tokens[]` in order, which is passed as the argument of the `parse_command()` function. Also, the number of tokens should be assigined to `*nr_tokens` which will be used by the framework.

Below diagram illustrates a correct result for an input string "  add t0  t1  t2  ". Note that each token is also a string which is terminated with `\0`.

```c
char *command   --> "  add t0  t1  t2  "
 
*nr_tokens = 4
tokens[0]  -->  "add"
tokens[1]  -->  "t0"
tokens[2]  -->  "t1"
tokens[3]  -->  "t2"
tokens[4]... = NULL
```


### Skeleton Code

You can start this program assignment by cloning this repository at https://github.com/sslab-ajou/sce212-pa0-2019f. Everything is in `pa0.c`. Please do not modify the `main()` function, but implement your code in `parse_command()` function.

All submission and grading are done automatically through https://sslab.ajou.ac.kr/pasubmit. Please follow the instruction explained in the class. Note that `input` file in the provided code contains the input sequence for the grading.


### Restrictions

- You **should not use any string manipulation functions from any libraries**. The banned functions include `strtok, strtok_r, strlen, fscanf` and/or similars. This implies that you should implement your own string manipulation functions if it is needed. **You will get 0 point if you use any of them**. Note that `malloc()` and `free()` are not string manipulation functions and OK to use.
- Do not `fprintf(stderr ...)` otherwise the grading system cannot grade your submission properly.


### Logistics

- This is an individual project; you work on the assignement alone.
- You can use **up to 4 slip tokens throughout this semester**.
- This is an OS/architecture-independent project; you may use Visual Studio on Windows or vim/gcc on Linux. However, the grading will be done on a Linux machine. So, write code as neutral as possible to compilers.
- Submit only the pa0.c file to the submission server at https://sslab.ajou.ac.kr/pasubmit.


### Tips and Notes

- Briefly speaking, the implementation might look like; start scanning from the beginning of `command` skipping all whitespaces until meet a non-whitespace character. That will be the beginning of the token. Then, resume scanning until meet any whitespace character (' ' or '`\t`'). That will be the end of the token. Repeat this until entire `command` is scanned. Assign the starting position of each token into `tokens[]` and count `nr_tokens` accordingly.
- Read comments in the skeleton code carefully.
- Make sure every string is terminated with '\0'.
- Post freely on QnA board on AjouBb to question about the project.



Good luck and have fun!
>>>>>>> 99e0b711d8a10e1ff71c15f385a621fdf8e3e543
# art
