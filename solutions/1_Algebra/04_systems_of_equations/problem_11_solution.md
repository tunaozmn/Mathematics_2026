# Exercise 11. A Parameter in a System of Three Equations

## Problem

Analyze the number of solutions depending on $t$:

$$
\begin{cases}
x+y+z=1, \\
x+ty+z=2, \\
x+y+tz=3.
\end{cases}
$$

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

> **Why this exercise:** develops parametric analysis while still relying only on elimination.

## Method

We subtract the first equation from the other two to eliminate $x$.

The resulting equations contain factors depending on $t$. Before dividing by these factors, we identify when they are zero and analyze that case separately.

## Solution

### 1. Form the augmented matrix

Using the variable order $x,y,z$, we obtain

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
1 & t & 1 & 2 \\
1 & 1 & t & 3
\end{array}
\right].
$$

### 2. Eliminate x from the second and third rows

Apply

$$
R_2\leftarrow R_2-R_1,
\qquad
R_3\leftarrow R_3-R_1.
$$

These operations are valid for every real value of $t$. They give

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
0 & t-1 & 0 & 1 \\
0 & 0 & t-1 & 2
\end{array}
\right].
$$

The transformed system is

$$
\begin{cases}
x+y+z=1, \\
(t-1)y=1, \\
(t-1)z=2.
\end{cases}
$$

To solve the last two equations by division, we need $t-1\ne0$. Therefore, we consider $t\ne1$ and $t=1$ separately.

### 3. Analyze the case t ≠ 1

When $t\ne1$, division by $t-1$ is valid. The last two equations give

$$
y=\frac{1}{t-1},
\qquad
z=\frac{2}{t-1}.
$$

Substitute into the first equation:

$$
\begin{aligned}
x
&=1-y-z \\
&=1-\frac{1}{t-1}-\frac{2}{t-1} \\
&=1-\frac{3}{t-1} \\
&=\frac{t-4}{t-1}.
\end{aligned}
$$

Thus, for every $t\ne1$, the solution is

$$
(x,y,z)=
\left(
\frac{t-4}{t-1},
\frac{1}{t-1},
\frac{2}{t-1}
\right).
$$

All three pivot entries, $1,t-1,t-1$, are nonzero. Hence, every variable is uniquely determined, and there is exactly one solution.

### 4. Analyze the case t = 1

When $t=1$, the transformed augmented matrix becomes

$$
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
0 & 0 & 0 & 1 \\
0 & 0 & 0 & 2
\end{array}
\right].
$$

The last two rows represent

$$
0=1,
\qquad
0=2.
$$

These are contradictions, so the system has no solution.

This is also visible in the original equations: at $t=1$, they require the same expression $x+y+z$ to equal 1, 2, and 3.

### 5. Summarize the classification

| Parameter value | Number of solutions | Reason |
| --- | --- | --- |
| $t\ne1$ | Exactly one | There is a nonzero pivot for every variable. |
| $t=1$ | None | Elimination produces contradictory rows. |

There is no parameter value giving infinitely many solutions. The only value at which pivots disappear is $t=1$, and that case is inconsistent.

## Verification

For $t\ne1$, substitute the proposed solution into all three original equations.

First equation:

$$
\begin{aligned}
x+y+z
&=\frac{t-4+1+2}{t-1} \\
&=\frac{t-1}{t-1} \\
&=1.
\end{aligned}
$$

Second equation:

$$
\begin{aligned}
x+ty+z
&=\frac{t-4+t+2}{t-1} \\
&=\frac{2t-2}{t-1} \\
&=2.
\end{aligned}
$$

Third equation:

$$
\begin{aligned}
x+y+tz
&=\frac{t-4+1+2t}{t-1} \\
&=\frac{3t-3}{t-1} \\
&=3.
\end{aligned}
$$

All three equations hold for every $t\ne1$. The excluded value $t=1$ was checked separately and gives no solution.
