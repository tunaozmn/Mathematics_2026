# Exercise 15. Comparing Directions Using the Cosine of the Angle

## Problem

Given

$$
a=(1,2,1),\qquad b=(2,4,2),\qquad c=(2,0,3).
$$

For each pair, compute

$$
\frac{u\cdot v}{\|u\|\,\|v\|}.
$$

Order the pairs by increasing angle between the vectors. Explain why for $a$ and $b$ the value is $1$ even though the vectors have different lengths.

> **Why this exercise:** reinforces the connection between the dot product and angle, and the distinction between direction and length.

## Method

For nonzero vectors, the expression

$$
\frac{u\cdot v}{\|u\|\,\|v\|}
$$

equals the cosine of the angle between them.

On the interval from $0$ to $\pi$, cosine decreases as the angle increases. Therefore, a larger cosine means a smaller angle.

We calculate the three vector lengths and the dot product for each pair, then compare the resulting ratios.

## Solution

### 1. Calculate the vector lengths

For $a$,

$$
\begin{aligned}
\|a\|
&=\sqrt{1^2+2^2+1^2} \\
&=\sqrt6.
\end{aligned}
$$

For $b$,

$$
\begin{aligned}
\|b\|
&=\sqrt{2^2+4^2+2^2} \\
&=\sqrt{24} \\
&=2\sqrt6.
\end{aligned}
$$

For $c$,

$$
\begin{aligned}
\|c\|
&=\sqrt{2^2+0^2+3^2} \\
&=\sqrt{13}.
\end{aligned}
$$

### 2. Calculate the ratio for a and b

The dot product is

$$
a\cdot b=1\cdot2+2\cdot4+1\cdot2=12.
$$

Therefore,

$$
\begin{aligned}
\frac{a\cdot b}{\|a\|\,\|b\|}
&=\frac{12}{\sqrt6\cdot2\sqrt6} \\
&=\frac{12}{12} \\
&=1.
\end{aligned}
$$

Hence,

$$
\theta_{ab}=0.
$$

### 3. Calculate the ratio for a and c

The dot product is

$$
a\cdot c=1\cdot2+2\cdot0+1\cdot3=5.
$$

Thus,

$$
\begin{aligned}
\frac{a\cdot c}{\|a\|\,\|c\|}
&=\frac{5}{\sqrt6\sqrt{13}} \\
&=\frac{5}{\sqrt{78}}.
\end{aligned}
$$

Therefore,

$$
\theta_{ac}=\arccos\left(\frac{5}{\sqrt{78}}\right).
$$

### 4. Calculate the ratio for b and c

The dot product is

$$
b\cdot c=2\cdot2+4\cdot0+2\cdot3=10.
$$

Thus,

$$
\begin{aligned}
\frac{b\cdot c}{\|b\|\,\|c\|}
&=\frac{10}{2\sqrt6\sqrt{13}} \\
&=\frac{5}{\sqrt{78}}.
\end{aligned}
$$

Therefore,

$$
\theta_{bc}=\arccos\left(\frac{5}{\sqrt{78}}\right).
$$

### 5. Order the pairs by increasing angle

The results are:

| Pair | Cosine of the angle | Angle |
| --- | --- | --- |
| $a,b$ | $1$ | $0$ |
| $a,c$ | $\frac{5}{\sqrt{78}}$ | $\arccos\left(\frac{5}{\sqrt{78}}\right)$ |
| $b,c$ | $\frac{5}{\sqrt{78}}$ | $\arccos\left(\frac{5}{\sqrt{78}}\right)$ |

Since

$$
0<\frac{5}{\sqrt{78}}<1,
$$

the last two angles are equal and acute. The ordering is

$$
\theta_{ab}<\theta_{ac}=\theta_{bc}.
$$

Thus, the pair $(a,b)$ comes first, while $(a,c)$ and $(b,c)$ are tied.

### 6. Explain why different lengths can give a cosine of 1

The vectors satisfy

$$
b=2a.
$$

Multiplication by the positive scalar 2 doubles the length but preserves direction and orientation. Therefore, the angle between $a$ and $b$ is zero.

The cosine ratio removes the effect of length:

$$
\begin{aligned}
\frac{a\cdot(2a)}{\|a\|\,\|2a\|}
&=\frac{2\|a\|^2}{\|a\|\cdot2\|a\|} \\
&=1.
\end{aligned}
$$

The value 1 expresses identical direction and orientation, not identical vector lengths.

## Verification

Normalize $a$ and $b$:

$$
\frac{a}{\|a\|}=\frac{1}{\sqrt6}(1,2,1),
$$

$$
\begin{aligned}
\frac{b}{\|b\|}
&=\frac{1}{2\sqrt6}(2,4,2) \\
&=\frac{1}{\sqrt6}(1,2,1).
\end{aligned}
$$

Their unit vectors are identical, confirming that the angle between them is zero.

It also follows that they make the same angle with $c$. Algebraically,

$$
\begin{aligned}
\frac{b\cdot c}{\|b\|\,\|c\|}
&=\frac{(2a)\cdot c}{2\|a\|\,\|c\|} \\
&=\frac{a\cdot c}{\|a\|\,\|c\|}.
\end{aligned}
$$

This confirms both the equal angles and the final ordering.
