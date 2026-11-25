# Exercise 6. A System with a Parameter — Which Cases Actually Occur?

## Problem

Analyze, depending on the parameter $a$, the system

$$
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
$$

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

> **Why this exercise:** teaches how to analyze a parameter without assuming in advance that all theoretically possible cases must occur in a specific system.

## Method

We use elimination to remove the variables from the second equation.

The resulting row will show when the equations are consistent. We then count the pivots and free variables to distinguish a unique solution from infinitely many solutions.

We avoid dividing by $a$, so the analysis also includes $a=0$.

## Solution

### 1. Form the augmented matrix

Using the variable order $x,y$, the augmented matrix is

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
a & a & 4
\end{array}
\right].
$$

### 2. Eliminate the first entry of the second row

Apply

$$
R_2\leftarrow R_2-aR_1.
$$

This operation is valid for every real value of $a$. The new second row is

$$
\begin{aligned}
&(a-a,\;a-a,\;4-2a) \\
&\qquad=(0,0,4-2a).
\end{aligned}
$$

Thus, we obtain

$$
\left[
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 4-2a
\end{array}
\right].
$$

The second row represents

$$
0=4-2a.
$$

### 3. Analyze the consistent case

The system is consistent exactly when

$$
4-2a=0,
$$

which gives

$$
a=2.
$$

For this value, the second row is entirely zero. Only one independent equation remains:

$$
x+y=2.
$$

There is one pivot and one free variable. Let

$$
y=t,\qquad t\in\mathbb{R}.
$$

Then

$$
x=2-t.
$$

Therefore, when $a=2$, the system has infinitely many solutions:

$$
(x,y)=(2-t,t),
\qquad t\in\mathbb{R}.
$$

### 4. Analyze the inconsistent case

If $a\ne2$, then $4-2a\ne0$. The second row therefore represents an equation with zero on the left and a nonzero number on the right.

This is impossible, so the system has no solution for every $a\ne2$.

In particular, $a=0$ gives the impossible second equation $0=4$ and is included in this case.

### 5. Explain why a unique solution cannot occur

The coefficients in the second equation are always $a$ times those in the first equation. Therefore, the second equation cannot provide a second pivot.

If the right-hand sides are compatible, the second equation adds no new restriction, leaving one free variable. Otherwise, the equations contradict each other.

Consequently, no value of $a$ produces exactly one solution.

The classification is:

| Parameter value | Number of solutions |
| --- | --- |
| $a=2$ | Infinitely many |
| $a\ne2$ | None |
| No value of $a$ | Exactly one |

## Verification

For $a=2$, substitute $(x,y)=(2-t,t)$ into the original equations:

$$
\begin{aligned}
x+y&=(2-t)+t=2, \\
2x+2y&=2(2-t)+2t=4.
\end{aligned}
$$

Both equations hold for every real $t$.

For $a\ne2$, any pair satisfying the first equation must satisfy

$$
ax+ay=a(x+y)=2a.
$$

The second equation requires this expression to equal 4, which would force $a=2$. Thus, no solution is possible when $a\ne2$, confirming the classification.
