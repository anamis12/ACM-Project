# ACM
ACM Programming Language
This is a programming language inspired by Lisp, implemented using the C programming language. It provides a simplified Lisp-like syntax and semantics, aiming to make it easier for C programmers to incorporate Lisp-like features into their projects. This README serves as a guide to understanding and using the Language.

## Features
- Lisp-like Syntax: MPC Lisp adopts many syntax elements from Lisp, including prefix notation and parentheses for function calls.
- S-Expressions: The language is based on S-expressions, which are used for both code and data representation.
- Basic Lisp Functions: Provides a set of basic Lisp-like functions for arithmetic, list manipulation, and control flow.
- Extensibility: Users can extend the language by defining new functions and macros in C.

## Installation
 ### Prerequisites
    - C Compiler (e.g., GCC)

- You have to copy the files mpc.c and mpc.h from the [MPC GITHUB REPO](https://github.com/orangeduck/mpc) 
- Clone the github repository of the Programing Language.
- Save the files mpc.c and mpc.h in the same directory as the source file.

## Usage
  -compile the code using the command:
    -cc -std=c99 -Wall parsing.c mpc.c -ledit -lm -o parsing   
    for  Linux and Mac
    - cc -std=c99 -Wall parsing.c mpc.c -o parsing
     for Windows

  -Then run the code by using
   -./parsing
