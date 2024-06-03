
A predicate is a function that produces a population.

Example
$H(x):\text{X is wearing a hat}$
H(x) is not a proposition since there is no value for x.
H(Max) would be a proposition

Universal Quantifier
$\forall xP(x)$ "For all x in domain, P(x) is true."

Example

Let S(x): x is a student

$\forall x S(x)$ is true for all the students sitting in this classroom

Existential Quantifier
$\exists xP(x)$ "There is at least one x such that P(x) is true"

Examples:
* $\exists x(x+1>x)$: True
* $\exists x(x+x=x\cdot x)$: True
* $\exists x(x>x+1)$: False

Uniqueness

$\exists!xP(x)$ "exactly one x causes P(x) to be true"

*NOTE*
$\forall,\exists$ have higher precedence thatn the other logical operators.

Example Translation
"All politicians are liars"

P(x): x is a poltiican
L(x): x is a liar

$\forall x(P(x)\implies L(x))$

Example Translation

F(x): x is a fish
S(x): x can swim
domain of x is animals

For every animal, if that animal is a fish, then it can swim
$\forall x(F(x)\implies S(x))$

Only fish can swim
$\forall x(S(x)\implies F(x))$

Example Translation
x is people in the room
S(x): x is a superhero
P(x): x is a puppet

"Someone in the room is a superhero puppet"
$\exists x(S(x)\land P(x))$


Typically $\forall$ goes with $\implies$

Typically $\exists$ goes with $\land$

Demorgan's rule for quantifiers

$\neg \forall xP(x)\equiv \exists x\neg P(x)$
$\neg \exists xP(x)\equiv \forall x\neg P(x)$


Example:

"You board the plane unless you bring two suitcases and don't annoy the pilot"

p: You board the plane
q: You don't bring two suitcases or annoy the pilot

The statement is q unless not p or in other words p implies q