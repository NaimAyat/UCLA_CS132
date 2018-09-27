# Lecture 1: September 27, 2018
* HW1 due Sunday, Oct 7
## Intro to Compilers
* Compiler translates an exe in one language to an exe in another language
  * We expect the program produced by the compiler to be better than the original
* Interpreter reads an exe and produces the results of running a program
  * Involves executing the source program in some fashion
## Two Pass Compiler
* Source -> front end -> intermediate representation (IR) -> back end -> machine code
  * Front end maps legal code into IR
  * Back end maps IR onto target machine
  * Allows multiple front ends
### Front End
* Source code -> scanner -> tokens -> parser -> IR
* Responsibilities:
  * Recognizes legal procedure
  * Reports errors
  * Produces IR
  * Preliminary storage map
  * Shape the code for back end
* Much of the front end construction can be automated
