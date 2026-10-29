# Exercise 3. When Can Matrices Be Multiplied?

## Problem

The matrix sizes are

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}.
$$

For the products

$$
AB,\ BA,\ BC,\ CB,\ AC,\ CA,\ AD,\ DA
$$

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

## Method

For a matrix $X$ of size $m\times n$ and a matrix $Y$ of size $p\times q$, the product $XY$ is defined if and only if $n=p$.

The number of columns of the first matrix must equal the number of rows of the second matrix. When this condition holds, the result has size $m\times q$.

Thus, the general rule is

$$
(m\times n)(n\times q)\longrightarrow m\times q.
$$

This condition follows from the row-by-column multiplication rule: each entry of the product is obtained by multiplying corresponding entries of a row of the first matrix and a column of the second matrix, then adding the products. The row and column must contain the same number of entries.

## Solution

For each product, compare the inner dimensions. If they match, the outer dimensions give the size of the result.

| Product | Matrix sizes | Inner-dimension check | Defined? | Result size |
| --- | --- | --- | --- | --- |
| $AB$ | $(2\times3)(3\times4)$ | $3=3$ | Yes | $2\times4$ |
| $BA$ | $(3\times4)(2\times3)$ | $4\neq2$ | No | Not defined |
| $BC$ | $(3\times4)(4\times2)$ | $4=4$ | Yes | $3\times2$ |
| $CB$ | $(4\times2)(3\times4)$ | $2\neq3$ | No | Not defined |
| $AC$ | $(2\times3)(4\times2)$ | $3\neq4$ | No | Not defined |
| $CA$ | $(4\times2)(2\times3)$ | $2=2$ | Yes | $4\times3$ |
| $AD$ | $(2\times3)(2\times2)$ | $3\neq2$ | No | Not defined |
| $DA$ | $(2\times2)(2\times3)$ | $2=2$ | Yes | $2\times3$ |

### Example of a defined product

For $AB$, each row of $A$ contains 3 entries and each column of $B$ contains 3 entries. Their dot products are therefore defined.

There are 2 rows in $A$ and 4 columns in $B$, producing 2 rows and 4 columns in $AB$.

### Example of an undefined product

For $BA$, each row of $B$ contains 4 entries, but each column of $A$ contains only 2 entries. The entries cannot be paired for the required dot product, so $BA$ is not defined.

This also shows that the existence of $AB$ does not imply the existence of $BA$.

## Verification

The sizes of the defined products can also be checked by considering their columns.

- $AB$: each of the 4 columns of $B$ has 3 entries. Multiplication by $A$ produces a column with 2 entries, so $AB$ has size $2\times4$.
- $BC$: each of the 2 columns of $C$ has 4 entries. Multiplication by $B$ produces a column with 3 entries, so $BC$ has size $3\times2$.
- $CA$: each of the 3 columns of $A$ has 2 entries. Multiplication by $C$ produces a column with 4 entries, so $CA$ has size $4\times3$.
- $DA$: each of the 3 columns of $A$ has 2 entries. Multiplication by $D$ produces a column with 2 entries, so $DA$ has size $2\times3$.

These results agree with the table. Numerical matrix entries are not needed to determine whether the products are defined or to find their sizes.
