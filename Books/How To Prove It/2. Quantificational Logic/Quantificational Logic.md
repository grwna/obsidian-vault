# Keywords

# Quantifiers
To say that $P(x)$ is true for every value of $x$ in $U$, we write $\forall xP(x)$. It reads "For all $x$, $P(x)$." or "For all $x$, $P(x)$ is true". This is equivalent to saying that the [[Variables and Sets#Truth Set|truth set]] of $P(x)$ is $U$.

We also write $\exists xP(x)$ to say that at least one value of $x$ makes $P(x)$ true. This is equivalent to saying the truth set of $P(x) \neq\varnothing$.

We can then write the example given in [[Conditional and Biconditional Connectives#Conditional Statement|conditional statements]] as:
$$\forall x(x>2\to x^2>4)$$
>[!important]
>Quantifiers *bind* a variable. This means the variables next to a quantifier symbol are always *bound variables*

"Words such as *everyone*, *someone*, *everything*, or *something* are often used to express the meanings of statements containing quantifiers."

The form of *quantifiers applied to a conditional statement* happens often and is very **important** to understand it.

We can use multiple quantifiers in a statement to better represent a statement. For example, the statement "*All parents are married*" can be represented as:
$$\forall x(\exists yP(x,y)\to \exists zM(x,z))$$
Where,
- $P(x,y)$ - $x$ is a parent of $y$
- $M(x,z)$ - $x$ is married to $z$
**Please note** that the usage of quantifiers in the statement is **very important**, so that the variables are bounded.

>[!note]
>How do we comprehend multiple quantifiers in a statement?
>$$\forall x \exists y(x+y=5)$$
>Think about the $\forall$ first, take it out and get the rest of the statement. Then understand the statement without the $\forall$.
>
>In this case, the statement above means "*no matter what value of x you choose, there will always be atleas one y for which x + y = 5 is true*"

**The Orders of Quantifiers Matter**
In the note above, if we swapped the quantifiers:
$$\exists y\forall x (x+y=5)$$
This now means: "*There is a value for y in which no matter what x you choose, x+y=5*"
It should be clear that this statement is false.

>[!note]
>The order of quantifiers *does not matter* if the quantifier is the same.
>Example: 
>$$\exists y\exists x(x+y=2) \text{   is equivalent to   }\exists x \exists y(x+y=2)$$
>We can interpret these as meaning:
>- $\exists x\exists y$ - there are $x$ and $y$ such that
>- $\forall x\forall y$ - for all $x$ and $y$
>In which the order is *interchangeable*, and $x=y$ is a possibility. You must add $\dots \land x\neq y$.

**Translating English to Quantificational Logic**
The rule of thumb is:
- $\forall$ will use $\to$
	**Example:** "*All humans are mortal*"
	Then the most natural interpretation is: "*If it is human, then it is mortal*"
- $\exists$ will use $\land, \lor$
	**Example:** "*Some humans are mortal*"
	Interpretation: "*There exists something that is a human AND it is mortal*"
This generally holds for their negations as well.

**Translating Quantificational Logic to English**
If there are two quantified variables, if they *interact* ($x$ likes $y$, $x$ is related to $y$), then use two quantifiers outside the parentheses.

# Equivalences Involving Quantifiers

Using equivalences, we can reexpress unintuitive statements into ones we can easily comprehend. 

**Quantifier Negation Laws**
$$\neg \exists xP(x)\text{ is equivalent to }\forall x \neg P(x)$$
$$\neg \forall xP(x)\text{ is equivalent to }\exists x \neg P(x)$$
Combining these with De Morgan and other equivalence laws, we can often reexpress *negative statements* as an equivalent but easier to understand *positive statement*

>[!warning]
>Be careful how you apply the negation.

Example of quantifier negation law application:
"*Everyone who Patricia likes, Sue doesn't like*"
$$\forall x(L(p,x)\to \neg L(s,x))$$
$$\forall x(\neg L(p,x)\lor \neg L(s,x)) \tag{conditional law}$$
$$\forall x\neg(L(p,x)\land L(s,x)) \tag{De Morgan's law}$$
$$\neg\exists x(L(p,x)\land L(s,x)) \tag{quantifier negation law}$$
The final statement that we got means "*There's no one that both Patricia and Sue likes*". And this might be easier to understand than the first statement.

**Exactly One**
In [[#Exercises|exercise 1]], we encounter a statement that uses **exactly one** of something. This occurs often in mathematics that there is a special notation for it:
$$\exists!xP(x)$$
This is equivalent to the form: $$\exists xP(x)\land \neg \exists y(P(y)\land y\neq x)$$
**Scope (Universe of Discourse**
To write specific constraints for the *universe of discourse*
# Exercises
1. Analyze the logical forms of the following statements.
	- John likes exactly one person
The answer to that is: $$\exists x(L(j,x)\land \neg \exists y(L(j,y)\land y\neq x))$$Where: 
- $L(x,y)$ - $x$ likes $y$
- $j$ - John
