# Lecture 1: September 27, 2018
* HW1 due Sunday, Oct 7
## Chapter 1: Intro to Compilers
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
#### Scanner
* Maps characters into tokens; `x = x + y` becomes <id, `x`> = <id, `x`> + <id, `y`>
* Character string value for a token is a *lexeme*
* Typical tokens: number, id, +. -, *, /, do, end
* Eliminates white space 
* A key issue is speed
  * Use specialized recognizer as opposed to lex
#### Parser
* Recognize context-free syntax
* Guide context-sensitive analysis
* Construct IRs
* Produce error messages
* Attempt error correction
### Back End
* IR -> instruction selection -> register allocation -> machine code
* Responsibilities:
  * Translate IR into target machine code
  * Choose instructions for each IR operation
  * Decide what to keep in registers at each point
  * Ensure conformance with system interfaces
#### Instuction Selection
* Produce compact, fast code
* Use available addressing modes
* Pattern matching problem
  * Ad hoc techniques
  * Tree pattern matching
  * String pattern matching
  * Dynamic programming
### Optimizer (Middle End)
* Analyzes and changes IR
* Goal is to reduce runtime
* Built as a set of passes
  * Constant propagation and folding
  * Code motion
  * Reduction of operator strength
  * Common subexpression elimination
  * Redundant store elimination
  * Dead code elimination
## Chapter 2: Lexical Analysis
### Scanner
* Maps characters into tokens; `x = x + y` becomes <id, `x`> = <id, `x`> + <id, `y`>
* Character string value for a token is a *lexeme*
* Typical tokens: number, id, +. -, *, /, do, end
* Eliminates white space 
* A key issue is speed
  * Use specialized recognizer as opposed to lex
* A scanner must recognize various parts of the language's syntax
  * Some parts are easy, like white space:
    ```
    <ws> ::= <ws> ' '
           | <ws> 't'
           | ' '
           | '\t'
    ```
  * Other parts are harder:
    * Identifiers (alphabetic followed by k alphanumerics
    * Numbers (integers, decimals, reals, complex)
    * We use regular expressions to specify these patterns
### CS 181 Refresh
* Regular expressions -> NFA -> DFA -> code for scanner
