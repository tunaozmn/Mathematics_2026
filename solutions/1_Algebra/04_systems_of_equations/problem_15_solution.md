# Exercise 15. Classifying Three Systems

## Problem

For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**

$$
\begin{cases}
x+y=2, \\
x-y=0,
\end{cases}
$$

**System 2**

$$
\begin{cases}
x+y=2, \\
2x+2y=4,
\end{cases}
$$

**System 3**

$$
\begin{cases}
x+y=2, \\
2x+2y=5.
\end{cases}
$$

For each, justify the classification: one solution, infinitely many solutions, or no solution.

> **Why this exercise:** brings together the three basic cases and requires recognizing them from the structure after elimination.

## Method

We eliminate $x$ from the second equation of each system and inspect the resulting row.

- A nonzero pivot in each variable column gives exactly one solution.
- A zero row with zero right-hand side leaves a free variable in these systems, giving infinitely many solutions.
- A zero coefficient row with nonzero right-hand side gives a contradiction, so there is no solution.

We stop as soon as the classification is determined.

## Solution

### 1. Classify System 1

The augmented matrix is

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
1 & -1 & 0
\end{array}
\right].
$$

Apply

$$
R_2\leftarrow R_2-R_1.
$$

We obtain

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -2 & -2
\end{array}
\right].
$$

There is a nonzero pivot in both variable columns, and no contradictory row appears. The second equation determines $y$, and the first then determines $x$.

Therefore, System 1 has exactly one solution. No further elimination is needed to classify it.

### 2. Classify System 2

The augmented matrix is

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
2 & 2 & 4
\end{array}
\right].
$$

Apply

$$
R_2\leftarrow R_2-2R_1.
$$

We obtain

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 0
\end{array}
\right].
$$

The second row represents $0=0$, so it imposes no additional restriction. The only remaining equation is

$$
x+y=2.
$$

The system is consistent and has one pivot for two variables. Therefore, one variable is free, and System 2 has infinitely many solutions.

### 3. Classify System 3

The augmented matrix is

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
2 & 2 & 5
\end{array}
\right].
$$

Apply

$$
R_2\leftarrow R_2-2R_1.
$$

We obtain

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 1
\end{array}
\right].
$$

The second row represents

$$
0x+0y=1,
$$

or $0=1$. This is impossible, so System 3 has no solution.

### 4. Summarize the classifications

| System | Second row after elimination | Classification |
| --- | --- | --- |
| 1 | $(0,-2\mid -2)$ | Exactly one solution |
| 2 | $(0,0\mid 0)$ | Infinitely many solutions |
| 3 | $(0,0\mid 1)$ | No solution |

Each classification required only one row operation.

## Verification

The same conclusions follow directly from the original equations.

For System 1, subtracting the first equation from the second gives $-2y=-2$, which fixes $y$ uniquely. The first equation then fixes $x$ uniquely.

For System 2, the second equation is exactly twice the first, including its right-hand side. It adds no restriction to the single equation in two unknowns.

For System 3, twice the first equation requires $2x+2y=4$, while the second requires $2x+2y=5$. These conditions contradict each other.

Thus, the three systems illustrate exactly one solution, infinitely many solutions, and no solution, respectively.
