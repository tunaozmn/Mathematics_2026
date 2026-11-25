# Exercise 14. A System of Equations and the Determinant

## Problem

Consider the system $Ax=b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4
\end{pmatrix}.
$$

For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.

> **Why this exercise:** connects the determinant with uniqueness of solutions and requires distinguishing the exceptional cases.

## Method

A square system $Ax=b$ has exactly one solution for every right-hand side $b$ if and only if $A$ is invertible. This is equivalent to

$$
\det A\ne0.
$$

We first calculate the determinant to identify the exceptional value of $k$.

When the determinant is zero, the equations may be dependent or inconsistent, depending on $b$. We compare the two equations to distinguish infinitely many solutions from no solution.

## Solution

### 1. Calculate the determinant

Using the formula for a $2\times2$ matrix,

$$
\begin{aligned}
\det A
&=1\cdot4-2\cdot k\\
&=4-2k.
\end{aligned}
$$

The determinant is zero when

$$
4-2k=0,
$$

which gives

$$
k=2.
$$

Therefore, the system has exactly one solution for every $b$ precisely when

$$
\boxed{k\ne2}.
$$

### 2. Examine the exceptional value

When $k=2$, the matrix is

$$
A=
\begin{pmatrix}
1 & 2 \\
2 & 4
\end{pmatrix}.
$$

Write

$$
x=
\begin{pmatrix}
x_1\\
x_2
\end{pmatrix},
\qquad
b=
\begin{pmatrix}
b_1\\
b_2
\end{pmatrix}.
$$

The system becomes

$$
\begin{aligned}
x_1+2x_2&=b_1,\\
2x_1+4x_2&=b_2.
\end{aligned}
$$

The left-hand side of the second equation is twice the left-hand side of the first. Subtracting twice the first equation from the second gives

$$
0=b_2-2b_1.
$$

Thus, the system is consistent exactly when $b_2=2b_1$.

### 3. Give an example with infinitely many solutions

Choose

$$
b=
\begin{pmatrix}
1\\
2
\end{pmatrix}.
$$

Then the equations are

$$
\begin{aligned}
x_1+2x_2&=1,\\
2x_1+4x_2&=2.
\end{aligned}
$$

The second equation is twice the first, so it imposes no additional restriction.

Let $x_2=s$, where $s$ is any real number. The first equation gives

$$
x_1=1-2s.
$$

Therefore, all solutions have the form

$$
x=
\begin{pmatrix}
1-2s\\
s
\end{pmatrix},
\qquad s\in\mathbb R.
$$

Since $s$ is arbitrary, there are infinitely many solutions.

### 4. Give an example with no solution

Choose

$$
b=
\begin{pmatrix}
1\\
3
\end{pmatrix}.
$$

The equations are now

$$
\begin{aligned}
x_1+2x_2&=1,\\
2x_1+4x_2&=3.
\end{aligned}
$$

Subtracting twice the first equation from the second gives

$$
0=3-2\cdot1=1.
$$

This is impossible, so the system has no solution.

## Verification

For the example with infinitely many solutions, substitute the proposed solution into both left-hand sides:

$$
\begin{aligned}
x_1+2x_2
&=(1-2s)+2s=1,\\
2x_1+4x_2
&=2(1-2s)+4s=2.
\end{aligned}
$$

Thus, every real value of $s$ produces the required right-hand side.

For the example with no solution, the first equation forces $2x_1+4x_2=2$, contradicting the required value $3$.

These examples show why a zero determinant does not by itself distinguish infinitely many solutions from no solution: consistency also depends on the right-hand side $b$.
