# Lecture 2: Oct 2, 2018
## Chapter 3: LL Parsing
* Regular expressions are used to classify, grammars are used to count
* Parse = derivation; ie. `<expression> -> <num> <op> <num> -> 1 + 1`
* LL: leftmost derivation
  * Build tree top-down
* LR: rightmost derivation
  * Build tree bottom-up
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
### Ambiguity
* If a grammar has more than one derivation for a single sentential form, then it is ambiguous
