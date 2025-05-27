<h1 align="center">Orthogonality I</h1>

## Session Material:

Lay: 6.1-6.3

[Recap and Exercises]()

[Session Notes]()

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EsTiRlgRBLpMku31mwnbViIBHTOgpvFeUWhBaN0WGJJMkA?e=KYrKvB)

---

## Session Description

Let's add some geometry back into our vector spaces! This session introduces the idea of the "inner product" (or dot product in $\mathbb{R}^n$) as a way to measure things like the "length" of a vector and the "distance" between vectors. Most importantly, it gives us a precise way to define "orthogonal" (or perpendicular) vectors. We'll explore orthogonal complements – the set of all vectors truly perpendicular to a given subspace, and see how they connect fundamental spaces we've already studied.

Building on this, we'll look at "orthogonal sets" of vectors, where every pair is perpendicular. These sets are really special because they're automatically linearly independent, and if they also span the space, they form an "orthogonal basis" – which makes finding coordinates ridiculously easy! Finally, we'll learn how to "orthogonally project" a vector onto a subspace. Think of this as finding the closest point in that subspace to the original vector, a super useful tool with lots of applications (related to the Best Approximation Theorem).

### Key Concepts

* Inner Product / Dot Product
* Vector Length and Distance
* Orthogonal Vectors, Complements, Sets, Bases, and Projection
* Best Approximation

!!! tip "Learning Objectives"

    - Compute inner products, vector lengths, and distances in vector spaces.
    - Identify and construct orthogonal and orthonormal sets and bases.
    - Determine orthogonal complements and analyze their properties.
    - Apply orthogonal projection to find best approximations in subspaces.
    - Interpret the geometric meaning of orthogonality in linear algebra.

---

## Exercises

<!--
"Do this exercise first.pdf" 
6.1: 1, 11, 13, 15-18  
6.2: 1, 9, 12, 21, 35      
6.3: 1, 3, 7, 13, 17 
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 1** (6.1.1)

Compute the quantities using the vectors

$$
\mathbf{u}=\left[\begin{array}{r}
-1 \\
2
\end{array}\right], \quad \mathbf{v}=\left[\begin{array}{l}
4 \\
6
\end{array}\right], \quad \mathbf{w}=\left[\begin{array}{r}
3 \\
-1 \\
-5
\end{array}\right], \quad \mathbf{x}=\left[\begin{array}{r}
6 \\
-2 \\
3
\end{array}\right]
$$

$\mathbf{u} \cdot \mathbf{u}, \mathbf{v} \cdot \mathbf{u}$, and $\frac{\mathbf{v} \cdot \mathbf{u}}{\mathbf{u} \cdot \mathbf{u}}$

??? answer "&nbsp;"

**Exercise 2** (6.1.11)

Find a unit vector in the direction of the given vector.

$\left[\begin{array}{c}7 / 4 \\ 1 / 2 \\ 1\end{array}\right]$

??? answer "&nbsp;"

**Exercise 3** (6.1.13)

Find the distance between $\mathbf{x}=\left[\begin{array}{r}10 \\ -3\end{array}\right]$ and $\mathbf{y}=\left[\begin{array}{l}-1 \\ -5\end{array}\right]$.

??? answer "&nbsp;"

**Exercise 4** (6.1.15-6.1.18)

Determine which pairs of vectors in the following exercises are orthogonal.

15. $\mathbf{a}=\left[\begin{array}{r}8 \\ -5\end{array}\right], \mathbf{b}=\left[\begin{array}{l}-2 \\ -3\end{array}\right]$
16. $\mathbf{u}=\left[\begin{array}{r}12 \\ 3 \\ -5\end{array}\right], \mathbf{v}=\left[\begin{array}{r}2 \\ -3 \\ 3\end{array}\right]$
17. $\mathbf{u}=\left[\begin{array}{r}3 \\ 2 \\ -5 \\ 0\end{array}\right], \mathbf{v}=\left[\begin{array}{r}-4 \\ 1 \\ -2 \\ 6\end{array}\right]$
18. $\mathbf{y}=\left[\begin{array}{r}-3 \\ 7 \\ 4 \\ 0\end{array}\right], \mathbf{z}=\left[\begin{array}{r}1 \\ -8 \\ 15 \\ -7\end{array}\right]$

??? answer "&nbsp;"

**Exercise 5** (6.2.1)

Determine whether the set of vectors is orthogonal.

$\left[\begin{array}{r}-1 \\ 4 \\ -3\end{array}\right],\left[\begin{array}{l}5 \\ 2 \\ 1\end{array}\right],\left[\begin{array}{r}3 \\ -4 \\ -7\end{array}\right]$

??? answer "&nbsp;"

**Exercise 6** (6.2.9)

Show that $\left\{\mathbf{u}_1, \mathbf{u}_2\right\}$ or $\left\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3\right\}$ is an orthogonal basis for $\mathbf{R}^2$ or $\mathbf{R}^3$, respectively. Then express $\mathbf{x}$ as a linear combination of the u's.

$\mathbf{u}_1=\left[\begin{array}{l}1 \\ 0 \\ 1\end{array}\right], \mathbf{u}_2=\left[\begin{array}{r}-1 \\ 4 \\ 1\end{array}\right], \mathbf{u}_3=\left[\begin{array}{r}2 \\ 1 \\ -2\end{array}\right]$, and $\mathbf{x}=\left[\begin{array}{r}8 \\ -4 \\ -3\end{array}\right]$

??? answer "&nbsp;"

**Exercise 7** (6.2.12)

Compute the orthogonal projection of $\left[\begin{array}{r}1 \\ -1\end{array}\right]$ onto the line through $\left[\begin{array}{r}-1 \\ 3\end{array}\right]$ and the origin.

??? answer "&nbsp;"

**Exercise 8** (6.2.21)

Determine whether the set of vectors is orthonormal. If the set is only orthogonal, normalize the vectors to produce an orthonormal set.

$\left[\begin{array}{l}1 / \sqrt{10} \\ 3 / \sqrt{20} \\ 3 / \sqrt{20}\end{array}\right],\left[\begin{array}{c}3 / \sqrt{10} \\ -1 / \sqrt{20} \\ -1 / \sqrt{20}\end{array}\right],\left[\begin{array}{c}0 \\ -1 / \sqrt{2} \\ 1 / \sqrt{2}\end{array}\right]$

??? answer "&nbsp;"

**Exercise 9** (6.2.35)

[M] Show that the columns of the matrix $A$ are orthogonal by making an appropriate matrix calculation. State the calculation you use.

$A=\left[\begin{array}{rrrr}-6 & -3 & 6 & 1 \\ -1 & 2 & 1 & -6 \\ 3 & 6 & 3 & -2 \\ 6 & -3 & 6 & -1 \\ 2 & -1 & 2 & 3 \\ -3 & 6 & 3 & 2 \\ -2 & -1 & 2 & -3 \\ 1 & 2 & 1 & 6\end{array}\right]$

??? answer "&nbsp;"

**Exercise 10** (6.3.1)

You may assume that $\left\{\mathbf{u}_1, \ldots, \mathbf{u}_4\right\}$ is an orthogonal basis for $\mathbb{R}^4$.

$\mathbf{u}_1=\left[\begin{array}{r}0 \\ 1 \\ -4 \\ -1\end{array}\right], \mathbf{u}_2=\left[\begin{array}{l}3 \\ 5 \\ 1 \\ 1\end{array}\right], \mathbf{u}_3=\left[\begin{array}{r}1 \\ 0 \\ 1 \\ -4\end{array}\right], \mathbf{u}_4=\left[\begin{array}{r}5 \\ -3 \\ -1 \\ 1\end{array}\right]$, $\mathbf{x}=\left[\begin{array}{r}10 \\ -8 \\ 2 \\ 0\end{array}\right]$. 

Write $\mathbf{x}$ as the sum of two vectors, one in
$\operatorname{Span}\left\{\mathbf{u}_1, \mathbf{u}_2, \mathbf{u}_3\right\}$ and the other in Span $\left\{\mathbf{u}_4\right\}$.

??? answer "&nbsp;"

**Exercise 11** (6.3.3)

Verify that $\left\{\mathbf{u}_1, \mathbf{u}_2\right\}$ is an orthogonal set, and then find the orthogonal projection of $\mathbf{y}$ onto $\operatorname{Span}\left\{\mathbf{u}_1, \mathbf{u}_2\right\}$.

$\mathbf{y}=\left[\begin{array}{r}-1 \\ 4 \\ 3\end{array}\right], \mathbf{u}_1=\left[\begin{array}{l}1 \\ 1 \\ 0\end{array}\right], \mathbf{u}_2=\left[\begin{array}{r}-1 \\ 1 \\ 0\end{array}\right]$

??? answer "&nbsp;"

**Exercise 12** (6.3.7)

Let $W$ be the subspace spanned by the $\mathbf{u}$ 's, and write $y$ as the sum of a vector in $W$ and a vector orthogonal to $W$.

$\mathbf{y}=\left[\begin{array}{l}1 \\ 3 \\ 5\end{array}\right], \mathbf{u}_1=\left[\begin{array}{r}1 \\ 3 \\ -2\end{array}\right], \mathbf{u}_2=\left[\begin{array}{l}5 \\ 1 \\ 4\end{array}\right]$

??? answer "&nbsp;"

**Exercise 13** (6.3.13)

Find the best approximation to $\mathbf{z}$ by vectors of the form $c_1 \mathbf{v}_1+c_2 \mathbf{v}_2$.

$\mathbf{z}=\left[\begin{array}{r}3 \\ -7 \\ 2 \\ 3\end{array}\right], \mathbf{v}_1=\left[\begin{array}{r}2 \\ -1 \\ -3 \\ 1\end{array}\right], \mathbf{v}_2=\left[\begin{array}{r}1 \\ 1 \\ 0 \\ -1\end{array}\right]$

??? answer "&nbsp;"

**Exercise 14** (6.3.17)

Let $\mathbf{y}=\left[\begin{array}{l}4 \\ 8 \\ 1\end{array}\right], \quad \mathbf{u}_1=\left[\begin{array}{l}2 / 3 \\ 1 / 3 \\ 2 / 3\end{array}\right], \quad \mathbf{u}_2=\left[\begin{array}{r}-2 / 3 \\ 2 / 3 \\ 1 / 3\end{array}\right], \quad$ and
$W=\operatorname{Span}\left\{\mathbf{u}_1, \mathbf{u}_2\right\}$.

1. Let $U=\left[\begin{array}{ll}\mathbf{u}_1 & \mathbf{u}_2\end{array}\right]$. Compute $U^T U$ and $U U^T$.
2. Compute $\operatorname{proj}_W \mathbf{y}$ and $\left(U U^T\right) \mathbf{y}$.