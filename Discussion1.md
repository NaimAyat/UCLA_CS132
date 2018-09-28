# Discussion 1: September 28, 2018
* Office: W 11am - 1pm @ Engineering IV 32565-B
## Deterministic Finite Automaton
* M = (Q, Σ, δ, q<sub>0</sub>, F) where:
  * Q = finite set (states)
  * Σ = finite set (alphabet)
  * q<sub>0</sub> ∈ Q = initial state
  * F ⊆ Q = the accepting state(s)
  * δ: Qx Σ → Q
* A language is regular if there exists a DFA accepts it
## Closure Properties of Finite State Languages
* L<sub>1</sub> • L<sub>2</sub>
* L<sub>1</sub> ∪ L<sub>2</sub>
* L<sub>1</sub>* and L<sub>1</sub><sup>+</sup> (Kleene star and Kleene plus)
* L<sub>1</sub> ∩ L<sub>2</sub>
* L<sub>1</sub><sup>R</sup>
* Homomorphisms: any function h: Σ → Σ*
  * Ex: for the language L = { w | x y; x = a<sup>n</sup>; y = b<sup>n</sup>; n ≥ 0} 
    * h(a) = ε, h(b) = ε
      * h(aaabbb) = εεεεεε = ε
    * h(a) = a, h(b) = a
      * h(L) = {a<sup>2n</sup>}
