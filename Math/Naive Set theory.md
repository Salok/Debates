#Naive Definition of Sets
A set is a collection of elements such that the set itself can be an element of another set.

One cannot be too careful when deciding set formation rules. Paradoxes lurk behind every corner, waiting for the unsuspecting mathematician. Ex: Russell's Paradox, Burali-Forti's Paradox, Cantor's Paradox.

##The axioms
###Axiom of infinity
*There exists a set that contains the 0 and the successor of each of its elements.*

###Axiom of extension
*Two sets are equal iff they contain the same elements.*

This is a very reasonable definition of equality.

###Axiom of comprehension (aka the first Python axiom)
For every set and formula of FOL there exists a set containing those elements of the set such that the formula is true. Ie, {a for a in A if S(a)}

###Axiom of pairing
*For every two sets there exists a set containing them both.*

From here we can define ordered sets and thus cartesian products.

###Axiom of unions
*For every two sets there exists a set that contains the elements of both.*

Turns out that pairing is not enough to define unions, so we need this other tool.

###Axiom of powers
*For every set there exists a set containing all the subsets of the set.*

This axiom lets us increase the cardinality of infinite sets. Supposing the **Continuum Hypothesis**, it is the only way to do so.

###Axiom of substitution (aka the second Python axiom)
*If A is a set, and for every a in A the set F(a) = {x for x in X if S(x,a)} can be formed, then there exists a set containing {F(a) for a in A}.*

###Axiom of choice
* *For every set A there is a choice function f of power set: P(A)\/empty->A such that /forall X /in P(A)\/empty f(X) /in X.*
* *For every collection of non-empty sets there is a choice function.
* *For every relation R there is a function f such that f is a subset of R and their domains are the same.*
* *For every collection of disjoint sets there is a set whose intersection with every member of the collection is a singleton.*
* *For every family of non-empty sets there is an element that belongs to the Cartesian product of the family.*

####Zorn's Lemma
*Given a poset where every chain has an upper bound, there exists a maximal element in the poset.*

Typical chains are ordered by inclusion, so that their union is an upper bound.

Zorn's lemma is equivalent to the axiom of Choice.

Some equivalent formulations:
* Every poset has a maximal chain
* Every chain in a poset is included in a maximal chain.
* If every chain in a poset has a lower upper bound, then there exists a maximal element in the poset.

####Well Ordering Theorem
*Every set can be well ordered.*

Pending Q: Why is Choice so controversial?

Pending: Show division by 3 is possible

##Finiteness
A set is finite if it is equivalent to some natural number. Otherwise, it is infinite.

Dedekind proposed an alternative definition: a set is infinite if it is equivalent to a subset of itself. Otherwise is finite.

#Well order
A set is well ordered if for every non-empty subset of it we can find a smallest element.

##Transfinite induction
If the presence in a given inductive set of every predecessor of any element of a well ordered set implies that the element itself belongs to the set, then the inductive set is equal to the well ordered set.

Complete induction, where you try to prove that a number in /omega pertains to an inductive set given that all their predecessors belong to the set, is a special case of transfinite induction analogous to natural induction.

Three cases may be distinguished when doing transfinite induction:
1. n is a minimal element (analogous to the base step in natural induction)
2. n has a direct predecessor
3. n is a limit element with no direct predecessor

##Transfinite recursion theorem
You can define a function from a well ordered set W to other set whose value at a point depends on the value of all the predecessors of the point in W.

##Comparability of well ordered sets
If X and Y are well ordered sets, then either they are similar (order preserving correspondence) or one is similar to an initial segment of the other.

#Ordinal numbers
Ordinal numbers are sets whose elements are subsets of the set.
They are formed by some limit numbers and their successors.

Ex: 0, 1, 2,... /omega, /omega + 1,... /omega 2,... /omega ²,... /omega ^/omega.

Ordinal numbers are naturally ordered by inclusion, which is equivalent to belonging and continuation in them.

Ordinal arithmetic is not well behaving. Commutativity fails.

###Counting theorem
Every woset is similar to an unique ordinal number.

#Cardinal numbers
The cardinal number of a set is the minimum element of the set consisting of all the ordinal numbers equivalent to said set. Every cardinal number is a limit number.

Cardinal arithmetic is well behaving. For finite cases works as expected. If we allow choice, then in infinite cases satisfies that:
* *#(A) + #(B) = #(A), A infinite, A >= B*
* *#(AxB) = #(A), A infinite, A >= B*
* *#(n)^#(A) = #(P(A)), A infinite, n finite*

Pending: #(AxA)=#(A) implies choice

###Schroder-Bernstein Theorem
If X is dominated by Y and Y is dominated by X, then X is similar to Y.

###Countability
A set is countable if it is finite or equivalent to /omega.

###Cantor's theorem
No set is equivalent to its own power set. Corollary: there are uncountable sets.

##The (generalized) continuum hypothesis
The continuum hypothesis states that there is no cardinal number between the cardinal number of omega and the cardinal number of 2^omega.

The generalized continuum hypothesis goes one step further and ensures that all the infinite cardinals are obtained from the repeated application of exponentiation. Thus, if /aleph is a cardinal, the smallest cardinal number greater than /aleph is 2^/aleph.


#Extending Set Theory
One can construct integers from the natural numbers through ordered pairs with an equivalence relation: (a,b) ~ (c,d) iff a+d = b+c.

Similarly, the rationals can be constructed using the relation: (a,b) ~ (c,d) iff ad = bc.
