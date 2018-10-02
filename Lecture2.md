# Lecture 2: Oct 2, 2018
## Chapter 3: LL Parsing
* Regular expressions are used to classify, grammars are used to count
* Parse = derivation; ie. `<expression> -> <num> <op> <num> -> 1 + 1`
### Precedence
* To add precedence, add additional levels to grammar:
  ```
  <expr> :== <expr> + <term>
           | <expr> - <term>
           | <term>
  <term> :== <term> / <factor>
           | <term> * factor
           | <factor>
  ```
