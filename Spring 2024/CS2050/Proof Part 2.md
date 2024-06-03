Direct Proof of $p\implies q$
Assume p, then through some steps, you get q

x`xpositive proof of $p\implies q$
Prove $\neg q\implies \neg p$
Assume $\neg q$, through some steps, you get $\neg p$

Example:
Prove that, for positive ints n,a,b

if n=ab, then $a\leq \sqrt{ n }$ or $b\leq \sqrt{ n }$

Direct proof is hard

Contrapositive Proof
![[Pasted image 20240126100509.png]]

Proof by contradiction

Prove R. Assume that you are wrong. Show not r is false, so r is true.

Example:
Prove $\sqrt{ 2 }$ is irrational
![[Pasted image 20240126100906.png]]

![[Pasted image 20240126100923.png]]


Trivial Proof

Ignore p, show that q is true

P(n): $a\leq b\implies a^n\leq b^n$
Prove P(0):

$a^0\leq b^0$

Which is clearly always true, so P(0) is proven


Vacuous Proof
Ignore q, show that p is false

Prove that every perfect square between 10 and 15 is a perfect cube.

(x is a perfect square between 10 and 15) -> (x is a perfect cube)

x is a perfect square between 10 and 15 is false

so the statement is proven


![[Pasted image 20240126101259.png]]


![[Pasted image 20240126101427.png]] 

Prove $\forall xP(x)$

Prove using induction.

Exhaustive proof: show P(x) individually for each x. Must be a finite domain.


Example:

Show that $x! \leq 2^x$ for $x\in \mathbb{Z},0\leq x\leq 3$

Go through each case x=0,1,2,3



Example:
Disprove $\forall xP(x)$
"Disprove" by counter example

Prove/Disprove that every positive integer can be written as a sum of 3 digits.

Proof by counterexample:
Consider 7. The only squares less than 7 are 0,1, and 4. Without 4 the best we can do is 1+1+1. With two fours, we are too large. So we can have exactly one 4. But 4+1+1 is the largest we can do with one 4. So 7 cannot be written as the sum of 3 squares.