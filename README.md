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
    C Compiler (e.g., GCC)

- You have to copy the files mpc.c and mpc.h from the [MPC GITHUB REPO](https://github.com/orangeduck/mpc) 
- Clone the github repository of the Programing Language.
- Save the files mpc.c and mpc.h in the same directory as the source file.

## Usage
  
  compile the code using the command:for  Linux and Mac
   ```ok
    cc -std=c99 -Wall parsing.c mpc.c -ledit -lm -o parsing
   ```

 for Windows

    
   
    cc -std=c99 -Wall parsing.c mpc.c -o parsing
  
    
    

  Then run the code by using

   ```ok1
   ./parsing

   ```

## Format
### S-expressions
- S-expressions are enclosed within parentheses.()
- The first element in an S-expression is typically a function or operator, followed by its arguments.
    example-
   ```s
   (+ 10 (* 5 3))
  ````

 ### Q-expressions
- Q-expressions are enclosed within parentheses.{}
- The first element in an Q-expression is typically a macro or operator, followed by its arguments.
    example-
   ```q
    eval {head (list 1 2 3 4)}
  ````
  Tail and Join macros are also available.

 ### Variables
- Variables are defined using the def keyword,aruguments placed in {} and values beside them.
example-
   ```v
      def {a b} 2 3 
  ````
- A list can also be declared as follows
    
   ```vl
   def {arglist} {a b x y}
   def arglist 1 2 3 4
   list a b x y
  ```
   ### Functions
   - We can call the function by putting it as the first argument in a normal S-Expression.
  Example-
   ```f
      (\ {x y} {+ x y}) 10 20
  ```

  - If we want to name this function we can pass it to our existing builtin def , Then we can call it by refering to it by name.
  Example-
   ```f1
     def {add-together} (\ {x y} {+ x y})
    add-together 10 20
   ```
  - This Language also supports partial evaluation.Example-
   ```f2
      def {add-mul} (\ {x y} {+ x (* x y)})
      add-mul 10 20
      def {add-mul-ten} (add-mul 10)
      add-mul-ten 50
   ```
     ### Conditionals
     - We check conditions using operators such as < = ,== etc.
       Example:
        ```c
         == 5 6
        ```
   - Ternary operator can also be implemented
   
   ```c1
   def {x y} 100 200
   if (== x y) {+ x y} {- x y}
   ```

   - using functions and conditionals , recursive functions can also be written.
  Example
   ```fc
   (fun {len l} {
   if (== l {})
    {0}
    {+ 1 (len (tail l))}
    })
   ```
     ### Strings
     - Our programming language can also handle strings.
       Example:
        ```st
         eval (head {"hello" "world"})
        ```
     Output:"hello"

    -With strings we can implement 3 new Builtins- print , load and error.
     Example:
  ```st1
  print "Hello World!"
  ```

   Output:"Hello World!"

  ```st2
  error "This is an error"
  ```
   
  Output:Error: This is an error

    ```st3
    load hello.lspy
    ```
   load-prints out the information in a file
  ### Comments
     -comments start with ; and end at the end of the line.

## Conclusion
Lisp is a powerful and versatile programming language known for its unique syntax, powerful macro system, and support for functional programming paradigms. Its simplicity and elegance make it a favorite among many programmers for tasks ranging from artificial intelligence to web development.

We welcome feedback, bug reports, and contributions from the community to further enhance the language's capabilities. Together, we can continue improving the language and making it even more valuable for libraries and their patrons.

Thank you for using the Acm Programming Language. If you have any questions or need assistance, please don't hesitate to reach out.
 
