# Discussion 1: September 28, 2018
* Office: W 11am - 1pm @ Engineering IV 32565-B
```
S := {L}
   | system.out.println(E);
   | if (E) s else s
   | while (E) s
L := S L | ε
E := true | false | 
```
## Deterministic Finite Automaton
* M = (Q, Σ, δ, q<sub>0</sub>, F) where:
  * Q = finite set (states)
  * Σ = finite set (alphabet)
  * q<sub>0</sub> ∈ Q = initial state
  * F ⊆ Q = the accepting state(s)
  * δ: Qx Σ → Q
