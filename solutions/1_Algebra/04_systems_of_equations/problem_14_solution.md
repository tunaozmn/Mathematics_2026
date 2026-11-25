# Exercise 14. A Small Change in the Right-Hand Side

## Problem

Compare the systems

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3
\end{cases}
$$

and

$$
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3.1.
\end{cases}
$$

Check the consistency of each system and explain why a small change in one number can change the type of the system.

> **Why this exercise:** shows the difference between a consistent and an inconsistent system without introducing new theory.

## Method

The first two equations are identical in both systems. We solve these equations and then check whether their solution satisfies the third equation.

We also compare the third equation with the sum of the first two. This reveals whether it adds no new restriction or creates a contradiction.

## Solution

### 1. Solve the two shared equations

Both systems contain

$$
\begin{cases}
x+y=2, \\
2x-y=1.
\end{cases}
$$

Adding the equations eliminates $y$:

$$
\begin{aligned}
(x+y)+(2x-y)&=2+1, \\
3x&=3, \\
x&=1.
\end{aligned}
$$

Substitute $x=1$ into the first equation:

$$
1+y=2,\qquad y=1.
$$

Thus, any solution of either full system must be

$$
(x,y)=(1,1).
$$

### 2. Check the first system

The third equation of the first system is

$$
3x=3.
$$

At $x=1$, this becomes $3=3$, so it is satisfied.

In fact, this third equation is exactly the sum of the first two equations. It is redundant and does not change their solution set.

Therefore, the first system is consistent and has the unique solution

$$
(x,y)=(1,1).
$$

### 3. Check the second system

The third equation of the second system is

$$
3x=3.1.
$$

However, the first two equations force $x=1$, which gives

$$
3x=3\ne3.1.
$$

Therefore, the only candidate from the first two equations fails the third equation. The second system is inconsistent and has no solution.

### 4. Show the difference in the augmented matrices

Write the right-hand side of the third equation as $c$. Both systems then have the augmented matrix

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
2 & -1 & 1 \\
3 & 0 & c
\end{array}
\right],
$$

where $c=3$ for the first system and $c=3.1$ for the second.

Apply the operations successively:

$$
R_3\leftarrow R_3-R_1,
\qquad
R_3\leftarrow R_3-R_2.
$$

The third row first becomes $(2,-1,c-2)$ and then $(0,0,c-3)$. Thus, we obtain

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
2 & -1 & 1 \\
0 & 0 & c-3
\end{array}
\right].
$$

For the first system, the last row represents

$$
0=3-3=0,
$$

which imposes no additional restriction.

For the second system, it represents

$$
0=3.1-3=0.1,
$$

which is a contradiction.

### 5. Explain why the small change matters

The first two equations already fix both unknowns. Their sum requires the exact equality $3x=3$.

Changing the third right-hand side to $3.1$ makes that equation incompatible with the first two. Although the numerical change is small, an exact solution must satisfy every equation exactly.

The same issue would occur if the third right-hand side were any number other than 3.

| System | Consistency | Number of solutions |
| --- | --- | --- |
| Third equation $3x=3$ | Consistent | Exactly one: $(1,1)$ |
| Third equation $3x=3.1$ | Inconsistent | None |

## Verification

For $(x,y)=(1,1)$, the first system gives

$$
\begin{aligned}
x+y&=1+1=2, \\
2x-y&=2\cdot1-1=1, \\
3x&=3\cdot1=3.
\end{aligned}
$$

All three equations hold.

For the second system, the first two still hold, but the third would require $3=3.1$. Since the first two equations uniquely determine $(1,1)$, no other point can satisfy the full second system.
