# Exercise 7. Choosing a Method Deliberately

## Problem

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

$$
\begin{cases}
2x-y=3, \\
4y=8;
\end{cases}
$$

2. three systems $Ax=b_i$ with the same invertible matrix $A$, when $A^{-1}$ is already known;
3. one $3\times3$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

> **Why this exercise:** practices choosing a method based on the structure of the problem instead of solving another small system by two methods.

## Method

The choice of method depends on what is already known and what remains to be computed.

A triangular system can be solved directly by back substitution. If an inverse is already available, it can be reused for several right-hand sides. For a single system with no inverse supplied, elimination works directly with the given right-hand side.

## Solution

### 1. Triangular system: use back substitution

The system is

$$
\begin{cases}
2x-y=3, \\
4y=8.
\end{cases}
$$

Its coefficient matrix is upper triangular:

$$
A=
\begin{pmatrix}
2 & -1 \\
0 & 4
\end{pmatrix}.
$$

The second equation contains only $y$, so no elimination is necessary.

From that equation,

$$
y=\frac84=2.
$$

Substitute $y=2$ into the first equation:

$$
\begin{aligned}
2x-2&=3, \\
2x&=5, \\
x&=\frac52.
\end{aligned}
$$

Thus, the unique solution is

$$
(x,y)=\left(\frac52,2\right).
$$

Back substitution uses the triangular structure immediately. Computing an inverse would introduce unnecessary work for this single right-hand side.

### 2. Three right-hand sides with a known inverse: reuse the inverse

For the three systems

$$
Ax=b_i,\qquad i=1,2,3,
$$

use the already known inverse:

$$
x^{(i)}=A^{-1}b_i,\qquad i=1,2,3.
$$

Here, $x^{(i)}$ denotes the solution vector for the right-hand side $b_i$.

The plan is to multiply the same matrix $A^{-1}$ by each of the three right-hand side vectors. These computations can also be grouped into one matrix product:

$$
\begin{aligned}
\begin{pmatrix}
x^{(1)} & x^{(2)} & x^{(3)}
\end{pmatrix}
&=
A^{-1}
\begin{pmatrix}
b_1 & b_2 & b_3
\end{pmatrix}.
\end{aligned}
$$

The inverse is the reusable part. There is no need to calculate it again or to repeat elimination separately for each system.

This choice is appropriate because the inverse is already known and all three systems have the same coefficient matrix.

### 3. One 3×3 system with no inverse supplied: use Gaussian elimination

Form the augmented matrix $[A\mid b]$ and apply elementary row operations to obtain row echelon form.

Then inspect the resulting equations:

- If there is a pivot for every variable, use back substitution to find the unique solution.
- If there is no contradiction but a variable is free, choose values for the free variables to obtain one solution vector.
- If a row represents an impossible equation, report that no solution exists.

The goal involves only one right-hand side, so calculating the entire inverse is unnecessary. Elimination works directly on the system we need to solve and does not require assuming that $A$ is invertible.

If more right-hand sides were later supplied for the same matrix, the recorded row operations could be applied to those right-hand sides as well.

### 4. Compare the choices

| Situation | Chosen method | Reason |
| --- | --- | --- |
| One triangular system | Back substitution | The required zeros are already present. |
| Three systems with a known inverse | Multiply each right-hand side by $A^{-1}$ | The inverse is available and reusable. |
| One 3×3 system with no inverse supplied | Gaussian elimination | It works directly with the single right-hand side and reveals consistency. |

The choice depends on the matrix structure, the available information, and the number of right-hand sides.

## Verification

For case 1, substitute the calculated values into both equations:

$$
\begin{aligned}
2x-y&=2\cdot\frac52-2=3, \\
4y&=4\cdot2=8.
\end{aligned}
$$

Thus, the solution satisfies the triangular system.

For case 2, the proposed procedure satisfies each original equation because

$$
Ax^{(i)}=A(A^{-1}b_i)=(AA^{-1})b_i=b_i.
$$

For case 3, elementary row operations preserve the solution set. Any resulting solution vector should be checked by substituting it into the original equation $Ax=b$.
