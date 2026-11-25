# Exercise 13. Do Four Points Lie in One Plane?

## Problem

Given

$$
A=(0,0,0),\qquad B=(1,2,0),\qquad C=(0,1,1),\qquad D=(2,5,1).
$$

1. Construct $\overrightarrow{AB}$ and $\overrightarrow{AC}$.
2. Find $n=\overrightarrow{AB}\times\overrightarrow{AC}$.
3. Construct $\overrightarrow{AD}$ and check whether $\overrightarrow{AD}\cdot n=0$.
4. Based on this, decide whether $D$ lies in the plane determined by $A,B,C$, and justify the criterion.

> **Why this exercise:** combines the known cross and dot products into a geometric criterion needed for planes, without introducing a separate concept used only once.

## Method

Two nonparallel vectors $\overrightarrow{AB}$ and $\overrightarrow{AC}$ determine the directions of the plane through $A,B,C$.

Their cross product gives a nonzero normal vector $n$. A point $D$ lies in this plane exactly when the displacement from $A$ to $D$ is perpendicular to $n$:

$$
\overrightarrow{AD}\cdot n=0.
$$

We first confirm that the normal is nonzero, then apply this test.

## Solution

### 1. Construct the two vectors in the plane

Subtract the coordinates of $A$ from those of $B$ and $C$:

$$
\begin{aligned}
\overrightarrow{AB}
&=(1-0,\;2-0,\;0-0) \\
&=(1,2,0),
\end{aligned}
$$

$$
\begin{aligned}
\overrightarrow{AC}
&=(0-0,\;1-0,\;1-0) \\
&=(0,1,1).
\end{aligned}
$$

### 2. Find a normal vector

Compute the cross product:

$$
\begin{aligned}
n
&=\overrightarrow{AB}\times\overrightarrow{AC} \\
&=(2\cdot1-0\cdot1,\;
0\cdot0-1\cdot1,\;
1\cdot1-2\cdot0) \\
&=(2,-1,1).
\end{aligned}
$$

Since $n\ne(0,0,0)$, the two side vectors are not parallel. Therefore, $A,B,C$ determine a unique plane.

### 3. Test the displacement to D

Construct

$$
\begin{aligned}
\overrightarrow{AD}
&=(2-0,\;5-0,\;1-0) \\
&=(2,5,1).
\end{aligned}
$$

Now calculate its dot product with the normal:

$$
\begin{aligned}
\overrightarrow{AD}\cdot n
&=(2,5,1)\cdot(2,-1,1) \\
&=2\cdot2+5\cdot(-1)+1\cdot1 \\
&=4-5+1 \\
&=0.
\end{aligned}
$$

Thus, $\overrightarrow{AD}$ is perpendicular to the normal vector, so $D$ lies in the plane through $A,B,C$. All four points are coplanar.

### 4. Justify the criterion geometrically

The vectors perpendicular to the nonzero normal $n$ form a plane of directions through the origin. This plane contains both $\overrightarrow{AB}$ and $\overrightarrow{AC}$.

Because these two vectors are independent, they span that entire plane of directions.

The condition $\overrightarrow{AD}\cdot n=0$ therefore means that the displacement from $A$ to $D$ lies along the plane, with no component in the normal direction. Starting at $A$ and following this displacement stays in the plane through $A,B,C$.

## Verification

First, check that the computed normal is perpendicular to both side vectors:

$$
\begin{aligned}
n\cdot\overrightarrow{AB}
&=2\cdot1-1\cdot2+1\cdot0=0, \\
n\cdot\overrightarrow{AC}
&=2\cdot0-1\cdot1+1\cdot1=0.
\end{aligned}
$$

We can also express the displacement to $D$ directly as a linear combination of the two plane directions:

$$
\begin{aligned}
2\overrightarrow{AB}+\overrightarrow{AC}
&=2(1,2,0)+(0,1,1) \\
&=(2,4,0)+(0,1,1) \\
&=(2,5,1) \\
&=\overrightarrow{AD}.
\end{aligned}
$$

This independently confirms that $D$ lies in the plane determined by $A,B,C$.
