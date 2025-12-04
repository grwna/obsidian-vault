# Keywords
- Index Family
- Index Set
- Families of Sets
- Power Set

# Advanced Set Notation
Now that we are familiar with *[[Quantificational Logic#Quantifiers|quantifiers]]*, we can discuss more advanced topics in set theory. For example, we previously defined a set this way, lets say $S$ is the set of all perfect squares:
$$S={\{ x^2\vert x\in \mathbb{N}\}}$$
We can now define the same set this way:
$$S=\{ x \; \vert \;\exists n\in\mathbb{N}\,(n^2=x) \}$$
## Indexed Family
Let's say we want to define a set for the first 100 prime numbers. We can define the $i$-th prime number as $p_{i}$ , then the set would be $P=\{ p_{1}, p_{2}, \dots,p_{100} \}$. Another way to say this is to define $P$ as: 
$$P={\{ p_{i} \;\vert\; i\in I\}}$$
Where:
$$I=\{ i\in\mathbb{N}\;\vert\; 1\leq i\leq 100 \}$$
Here, $P$ is called the *indexed family* and $I$ is called the *index set*. The *index* does not have to be numbers. You can think of the index as a "key" like in a hash map.
>[!note]
>In general, any *indexed family*:
>$$A=\{ x_{i} \;\vert\; i\in I \} \;\text{ can also be defined as } \; A=\{ x \;\vert\; \exists i\in I(x=x_{i}) \}$$
>And consequently:
>$$x\in \{ x_{i} \;\vert\; i\in I\} \equiv \exists i\in I(x=x_{i})$$

## Families of Sets and the Power Set
Sets containing sets. Lets say $A=\{ 1,2,3 \}$, and $\mathcal{F}={\{  A\}}$, here $1\in A$ but $1\notin \mathcal{F}$.

**Families of Sets as Indexed Family**
Lets say $S$ is the set of all students. And for each student, $C_s$ is the set of courses that they take. Then we can define the family of sets as: 
$$\mathcal{F}=\{ C_{s} \;\vert\;s\in S \}$$
Note that each $C_{s}\in\mathcal{F}$ but a specific course $c\in C_{S}$ is not in $\mathcal{F}$.

**Power Set**
A power set of a set $A$, denoted $\mathcal{P}(A)$ is the *family of sets* that contains all possible combination of subsets of $A$. 
>[!example]
>Say $A={1,5}$, then $\mathcal{P}(A) = \{ \varnothing, \{ 1 \}, \{ 5 \}, \{ 1,5 \} \}$
>Also, $\mathcal{P}(\varnothing)=\{ \varnothing \}$.
 
## **Equivalent Notations (Example 2.3.1)**
How do we write the logical form of: $\{ x_{i} \;\vert\; i\in I\}\subseteq A$
One way to write it is to decompose each statement. 
1. First we decompose the subset:
	$$\forall x(x\in \{ x_{i} \;\vert\; i\in I\} \to x\in A)$$
2. Then we decompose the set membership of x statement:
$$\forall x(\exists i\in I(x=x_{i})\to x\in A$$

And thus we found the logical form of the statement. However a different way to say it exists. The original statement is equal to saying "*All elements of $x_{i}$ such that $i$ is in the Index Set is also an element of $A$*".
Thus another way to write the original statement is:
$$\forall i\in I(x_{i}\in A)$$
But how do we show that this is **truly** equivalent to the orignal statement? we will learn a way to show this in *Chapter 3: Proofs*.