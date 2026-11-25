# Exercise 3. Inconsistent System

## Problem

Solve or show that the system is inconsistent:

$$
\begin{cases}
x+2y=3, \\
2x+4y=7.
\end{cases}
$$

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

> **Why this exercise:** teaches how to recognize that a system has no solution without guessing.

## Method

We write the augmented matrix and eliminate the first variable from the second row.

A row with zero coefficients but a nonzero right-hand side represents an impossible equation. If such a row appears, the system is inconsistent and has no solution.

## Solution

### 1. Form the augmented matrix

Using the variable order $x,y$, we obtain

$$
\left[
\begin{array}{cc|c}
1 & 2 & 3 \\
2 & 4 & 7
\end{array}
\right].
$$

### 2. Eliminate x from the second row

Apply the row operation

$$
R_2\leftarrow R_2-2R_1.
$$

The new second row is

$$
\begin{aligned}
&(2-2\cdot1,\;4-2\cdot2,\;7-2\cdot3) \\
&\qquad=(0,0,1).
\end{aligned}
$$

Therefore, the augmented matrix becomes

$$
\left[
\begin{array}{cc|c}
1 & 2 & 3 \\
0 & 0 & 1
\end{array}
\right].
$$

### 3. Interpret the contradiction

The second row represents the equation

$$
0x+0y=1,
$$

which simplifies to

$$
0=1.
$$

This is impossible for every choice of $x$ and $y$.

Since the row operation preserves the solution set, the original system also has no solution. Therefore, the system is inconsistent.

The contradiction comes from the right-hand sides: the left-hand side of the second original equation is twice that of the first, but $7$ is not twice $3$.

## Verification

Any pair satisfying the first equation must satisfy

$$
x+2y=3.
$$

Multiplying both sides by 2 gives

$$
2x+4y=6.
$$

However, the second original equation requires

$$
2x+4y=7.
$$

The same expression cannot equal both 6 and 7. Thus, no pair $(x,y)$ satisfies both equations, confirming the conclusion from elimination.
