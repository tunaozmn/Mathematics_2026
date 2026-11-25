# Exercise 5. Row Echelon Form and Number of Solutions

## Problem

For the augmented matrix

$$
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0
\end{pmatrix}
$$

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

> **Why this exercise:** teaches how to read information about solutions directly from row echelon form.

## Method

The matrix is already in row echelon form, so no further elimination is needed.

We first check for a contradictory row. Then we identify the pivot columns: variables in those columns are determined by the equations, while variables in columns without pivots are free.

Finally, we use back substitution to express the pivot variables in terms of the free variable.

## Solution

### 1. Interpret the rows as equations

Using the variable order $x,y,z$, the matrix represents

$$
\begin{cases}
x+2y-z=3, \\
y+2z=1, \\
0=0.
\end{cases}
$$

The third row imposes no restriction. There is no row representing an equation such as $0=1$, so the system is consistent.

### 2. Identify the pivots and the free variable

The first row has its pivot in the $x$ column. The second row has its pivot in the $y$ column.

There is no pivot in the $z$ column, so $z$ is free.

There are three unknowns and two pivots. Therefore, the number of free variables is

$$
3-2=1.
$$

Since the system is consistent and has one free variable, it has infinitely many solutions.

### 3. Use back substitution

Let

$$
z=t,\qquad t\in\mathbb{R}.
$$

The second equation gives

$$
\begin{aligned}
y+2t&=1, \\
y&=1-2t.
\end{aligned}
$$

Substitute this expression into the first equation:

$$
\begin{aligned}
x+2(1-2t)-t&=3, \\
x+2-5t&=3, \\
x&=1+5t.
\end{aligned}
$$

Thus, all solutions are

$$
(x,y,z)=(1+5t,1-2t,t),
\qquad t\in\mathbb{R}.
$$

Equivalently, in vector form,

$$
\begin{aligned}
\begin{pmatrix}
x \\
y \\
z
\end{pmatrix}
&=
\begin{pmatrix}
1 \\
1 \\
0
\end{pmatrix}
+t
\begin{pmatrix}
5 \\
-2 \\
1
\end{pmatrix},
\qquad t\in\mathbb{R}.
\end{aligned}
$$

Only one variable can be chosen freely: once $z$ is selected, the second equation fixes $y$, and the first fixes $x$.

## Verification

Substitute the parametric expressions into the two nonzero equations.

For the first equation,

$$
\begin{aligned}
x+2y-z
&=(1+5t)+2(1-2t)-t \\
&=1+5t+2-4t-t \\
&=3.
\end{aligned}
$$

For the second equation,

$$
\begin{aligned}
y+2z
&=(1-2t)+2t \\
&=1.
\end{aligned}
$$

The third equation is always $0=0$. Hence, every real value of $t$ gives a solution, confirming the parametric description.
