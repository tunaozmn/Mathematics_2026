# Exercise 13. Undoing a Composite Transformation

## Problem

The matrices

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix},\qquad H=
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
$$

describe nonuniform scaling and shear. For $T=HS$, find $T^{-1}$ in two ways:

1. first compute $T$, then its inverse,
2. use $(HS)^{-1}=S^{-1}H^{-1}$.

Compare the results. Additionally compute $H^{-1}S^{-1}$ and verify that the incorrect order gives a different matrix. Explain the rule: “when undoing a composition of operations, we undo them from the end.”

> **Why this exercise:** reinforces the inverse of a product in a less direct configuration.

## Method

For column vectors, the rightmost matrix acts first. Thus, $T=HS$ applies the scaling $S$ first and the shear $H$ second.

To reverse this transformation, we undo the shear first and the scaling second. Therefore,

$$
T^{-1}=(HS)^{-1}=S^{-1}H^{-1}.
$$

We will also calculate $T^{-1}$ directly using the inverse formula for a $2\times2$ matrix, then compare the two results.

## Solution

### 1. Compute T

Multiply $H$ by $S$:

$$
\begin{aligned}
T
&=HS \\
&=
\begin{pmatrix}
1 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 0 \\
0 & 1
\end{pmatrix} \\
&=
\begin{pmatrix}
1\cdot2+1\cdot0 & 1\cdot0+1\cdot1 \\
0\cdot2+1\cdot0 & 0\cdot0+1\cdot1
\end{pmatrix} \\
&=
\begin{pmatrix}
2 & 1 \\
0 & 1
\end{pmatrix}.
\end{aligned}
$$

### 2. Find the inverse of T directly

The determinant is

$$
\det T=2\cdot1-1\cdot0=2.
$$

Since it is nonzero, the inverse exists. Applying the inverse formula gives

$$
\begin{aligned}
T^{-1}
&=\frac12
\begin{pmatrix}
1 & -1 \\
0 & 2
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1
\end{pmatrix}.
\end{aligned}
$$

### 3. Use the inverse-of-a-product property

The inverse of the diagonal matrix $S$ is obtained by taking reciprocals of its diagonal entries:

$$
S^{-1}=
\begin{pmatrix}
\frac12 & 0 \\
0 & 1
\end{pmatrix}.
$$

The shear $H$ adds the second coordinate to the first. Its inverse subtracts the second coordinate from the first:

$$
H^{-1}=
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}.
$$

Multiply these inverses in the required order:

$$
\begin{aligned}
S^{-1}H^{-1}
&=
\begin{pmatrix}
\frac12 & 0 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac12\cdot1+0\cdot0 & \frac12\cdot(-1)+0\cdot1 \\
0\cdot1+1\cdot0 & 0\cdot(-1)+1\cdot1
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1
\end{pmatrix}.
\end{aligned}
$$

This agrees with the inverse found directly. Hence,

$$
T^{-1}=S^{-1}H^{-1}=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1
\end{pmatrix}.
$$

### 4. Calculate the product in the incorrect order

Now compute $H^{-1}S^{-1}$:

$$
\begin{aligned}
H^{-1}S^{-1}
&=
\begin{pmatrix}
1 & -1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
\frac12 & 0 \\
0 & 1
\end{pmatrix} \\
&=
\begin{pmatrix}
\frac12 & -1 \\
0 & 1
\end{pmatrix}.
\end{aligned}
$$

Its upper-right entry is $-1$, whereas the corresponding entry of $T^{-1}$ is $-\frac12$. Therefore,

$$
H^{-1}S^{-1}\ne S^{-1}H^{-1}=T^{-1}.
$$

### 5. Explain why the order must be reversed

For a general vector, the original transformation acts in two stages:

$$
\begin{pmatrix}
x \\
y
\end{pmatrix}
\xrightarrow{S}
\begin{pmatrix}
2x \\
y
\end{pmatrix}
\xrightarrow{H}
\begin{pmatrix}
2x+y \\
y
\end{pmatrix}.
$$

To recover the original vector, first undo the last operation, the shear:

$$
\begin{pmatrix}
2x+y \\
y
\end{pmatrix}
\xrightarrow{H^{-1}}
\begin{pmatrix}
2x \\
y
\end{pmatrix}
\xrightarrow{S^{-1}}
\begin{pmatrix}
x \\
y
\end{pmatrix}.
$$

Thus, $H^{-1}$ acts first and $S^{-1}$ acts second. Since the rightmost matrix acts first, the combined inverse is $S^{-1}H^{-1}$.

This is the meaning of undoing a composition from the end.

## Verification

Let

$$
C=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1
\end{pmatrix}.
$$

Multiplying by $T$ gives

$$
\begin{aligned}
TC
&=
\begin{pmatrix}
2 & 1 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & -1+1 \\
0 & 1
\end{pmatrix} \\
&=I.
\end{aligned}
$$

In the reverse order,

$$
\begin{aligned}
CT
&=
\begin{pmatrix}
\frac12 & -\frac12 \\
0 & 1
\end{pmatrix}
\begin{pmatrix}
2 & 1 \\
0 & 1
\end{pmatrix} \\
&=
\begin{pmatrix}
1 & \frac12-\frac12 \\
0 & 1
\end{pmatrix} \\
&=I.
\end{aligned}
$$

Both products confirm that the two methods give the same inverse of $T$.
