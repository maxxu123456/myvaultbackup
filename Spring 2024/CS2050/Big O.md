Big O is a comparison between two functiosn

f(n) is O(g(n)) if 
$f(n)\leq C\cdot g(n),\forall n>k$

C,k are witnesses that f(n) is big O of g(n)

Compare $7n^2$ vs. $n^3$

Claim: $7n^2$ is $O(n^3)$

$7n^2\leq 7n^3$

for $n\geq 1$

We have proven that $7n^2$ is $O(n^3)$ with witnessnes C=7, and k=1

![[Pasted image 20240214101922.png]]


f(x) is O(g(x)) mean "g(x) grows more quickly or roughly equal to f(x)"

Math:

$\exists C\exists k [f(x)\leq C\cdot g(x) \forall x\geq k]$

Example: Show $5x^2+6x$ is $O(x^2)$

![[Pasted image 20240216111619.png]]

![[Pasted image 20240216111805.png]]


Theorem: A polynomial is bounded by its highest power term

$a_{n}x^n$ is $O(x^n)$

Example: $x^7+506x^6+223$ is $O(x^7)$



