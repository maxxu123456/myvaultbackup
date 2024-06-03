Example:

Statement: Not all clowns are funny
$\neg(\forall x(C(x)\implies F(x)))$
$\exists x\neg(C(x)\implies F(x))$
...
$\exists x[C(x)\land \neg F(x)]$

Example:

F(x,y): x is friends is y: not a proposition
F(x,BoB): x is freinds with bob: it is not a proposition
$\forall xF(x,\text{Bob})$:Everyone is friends with bob: It is a proposition
$\forall xF(x,y): \text{Everyone is friends with y}$: not a proposition
$\exists y[\forall xF(x,y)]$: there is someone who everyone is friends with
$\forall x[\exists yF(x,y)]$: for every person, there is someone who is friends with them

## Quantifiers as loops

$\forall x\forall yP(x,y)$

True for every possible x,y pair.
```
for x in domain:
	for y in domain:
		P(x,y)
```


$\exists x\forall yP(x,y)$

one fixed x has a relationship with all y

```
x=______
for y in domain:
	P(x,y)
```

$\exists x\exists yP(x,y)$

true for at least one x,y pair

```
x=___
y=___
P(x,y)
```

$\forall x\exists yP(x,y)$
```
for x in domain:
	x=_____
	P(x,y)
```

Example:

L(x,y): x loves y

$\forall x\forall yL(x,y)$: everyone loves everyone
$\exists x\exists yL(x,y)$: Someone loves someone (could be one person with self-love)


Cases:

$\exists y[\forall xL(x,y)]$
for some person, everyone loves them

$\exists x[\forall yL(x,y)]$
for some specific person, that person loves everyone

$\forall [x\exists yL(x,y)]$

for each person, there exists someone that the first person loves

$\forall y[\exists xL(x,y)]$
for each person, someone loves them

DeMorgan's for multiple Quantifiers

$\neg \exists x\forall y\forall z\exists q\forall n[T(x,y,z,q,n)]$
$\forall x\neg \forall y\forall z\exists q\forall n[T(x,y,z,q,n)]$
...
$\forall x\exists x\exists z\forall q\exists n\neg(T(x,y,z,q,n))$


## Practice

F(x,y): x can fool y
L(x): x is a lumberjack
H(x): x is a harpist

All lumberjacks are harpists
$\forall x[L(x)\implies H(x)]$

Everyone is a harpist except for lumberjacks, who are not.
$\forall x[H(x)\iff \neg L(x)]$
or
$\forall x[H(x)\oplus L(x)]$


Everyone can fool someone
$\forall x\exists yF(x,y)$


Some lumberjacks are not harpists
$\exists x[L(x)\land \neg H(x)]$

Someone can fool everyone

$\exists x\forall yF(x,y)$

Some lumberjack can fool every harpist
$\exists x[L(x)\land \forall y[F(x,y)]]$

There is exactly one (three?) harpist(s) who can fool every lumberjack. Cannot use $\exists!$

this one is really hard
