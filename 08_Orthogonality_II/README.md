<h1 align="center">Orthogonality II</h1>

## Session Material:
Lay: ​​​6.4-6.6

[Recap and Exercises]()

[Session Notes]()

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EtRCyXB5jWNAvJv9H0Uo-_8BEsXd36hxB3TOHflc7XSGjw?e=M8MUba)

---

## Session Description

Building on our understanding of orthogonal vectors and bases, this session focuses on powerful techniques and applications related to orthogonality. First, we'll learn the "Gram-Schmidt process" – a step-by-step method to turn *any* basis for a subspace into an orthogonal (or orthonormal) one. This is a fundamental algorithm! Related to Gram-Schmidt is the "QR factorization," a way to break down certain matrices into a product of a matrix with orthonormal columns and an upper triangular matrix.

Then, we'll tackle a super common problem in real-world data: what do you do when a linear system $A\mathbf{x}=\mathbf{b}$ has *no* exact solution? We'll introduce "least-squares" solutions – the 'best possible' approximate solutions that minimize the error. Geometrically, finding the least-squares solution involves projecting the vector $\mathbf{b}$ onto the column space of matrix $A$. We'll see how these least-squares ideas are applied, especially in fitting models to data (like finding the 'best' line through a set of points).

### Key Concepts

* Gram-Schmidt Process
* Orthogonalization
* Least Squares
* Inconsistent Systems
* Projections
* Data Fitting

!!! tip "Learning Objectives"

    - Apply the Gram-Schmidt process to construct orthogonal and orthonormal bases.
    - Solve least-squares problems and interpret best-fit solutions.
    - Analyze projections and their role in data fitting and inconsistent systems.
    - Connect orthogonality concepts to practical applications in modeling and data analysis.

## Exercises

<!--
6.4: 1, 6 12, 24
6.5: 1, 3, 5, 7, 12, 25
6.6: 3, 4, 7, 13 
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 1** (6.4.1, 6.4.6)

In the following exercises, the given set is a basis for a subspace $W$. Use the Gram-Schmidt process to produce an orthogonal basis for $W$.

1. $\left[\begin{array}{r}3 \\ 0 \\ -1\end{array}\right],\left[\begin{array}{r}8 \\ 5 \\ -6\end{array}\right]$
6. $\left[\begin{array}{r}3 \\ -1 \\ 2 \\ -1\end{array}\right],\left[\begin{array}{r}-5 \\ 9 \\ -9 \\ 3\end{array}\right]$

??? answer "&nbsp;"

**Exercise 2** (6.4.12)

Find an orthogonal basis for the column space of the following matrix:

$\left[\begin{array}{rrr}1 & 3 & 5 \\ -1 & -3 & 1 \\ 0 & 2 & 3 \\ 1 & 5 & 2 \\ 1 & 5 & 8\end{array}\right]$

??? answer "&nbsp;"

**Exercise 3** (6.4.24)

[M] Use the Gram-Schmidt process as in Example 2 to produce an orthogonal basis for the column space of

$$
A=\left[\begin{array}{rrrr}
-10 & 13 & 7 & -11 \\
2 & 1 & -5 & 3 \\
-6 & 3 & 13 & -3 \\
16 & -16 & -2 & 5 \\
2 & 1 & -5 & -7
\end{array}\right]
$$

??? answer "&nbsp;"

**Exercise 4** (6.5.1, 6.5.3) <!-- NOTE: Formulation may be a bit confusing because we are using a and b also for labeling the exercises -->

Find a least-squares solution of $A \mathbf{x}=\mathbf{b}$ by (a) constructing the normal equations for $\hat{\mathbf{x}}$ and (b) solving for $\hat{\mathbf{x}}$.

1. $A=\left[\begin{array}{rr}-1 & 2 \\ 2 & -3 \\ -1 & 3\end{array}\right], \mathbf{b}=\left[\begin{array}{l}4 \\ 1 \\ 2\end{array}\right]$
3. $A=\left[\begin{array}{rr}1 & -2 \\ -1 & 2 \\ 0 & 3 \\ 2 & 5\end{array}\right], \mathbf{b}=\left[\begin{array}{r}3 \\ 1 \\ -4 \\ 2\end{array}\right]$

??? answer "&nbsp;"

**Exercise 5** (6.5.5)

Describe all least-squares solutions of the equation $A \mathbf{x}=\mathbf{b}$.

$A=\left[\begin{array}{lll}1 & 1 & 0 \\ 1 & 1 & 0 \\ 1 & 0 & 1 \\ 1 & 0 & 1\end{array}\right], \mathbf{b}=\left[\begin{array}{l}1 \\ 3 \\ 8 \\ 2\end{array}\right]$

??? answer "&nbsp;"

**Exercise 6** (6.5.7)

Compute the least-squares error associated with the leastsquares solution found in Exercise 4b.

??? answer "&nbsp;"

**Exercise 7** (6.5.12)

Find (a) the orthogonal projection of $\mathbf{b}$ onto $\mathrm{Col} A$ and (b) a least-squares solution of $A \mathbf{x}=\mathbf{b}$.

$A=\left[\begin{array}{rrr}1 & 1 & 0 \\ 1 & 0 & -1 \\ 0 & 1 & 1 \\ -1 & 1 & -1\end{array}\right], \mathbf{b}=\left[\begin{array}{l}2 \\ 5 \\ 6 \\ 6\end{array}\right]$

??? answer "&nbsp;"

**Exercise 8** (6.5.25)

Describe all least-squares solutions of the system

$$
\begin{aligned}
& x+y=2 \\
& x+y=4
\end{aligned}
$$

??? answer "&nbsp;"

**Exercise 9** (6.6.3-6.6.4)

Find the equation $y=\beta_0+\beta_1 x$ of the leastsquares line that best fits the given data points.

3. $(-1,0),(0,1),(1,2),(2,4)$
4. $(2,3),(3,2),(5,1),(6,0)$

??? answer "&nbsp;"

**Exercise 10** (6.6.7)

A certain experiment produces the data $(1,1.8),(2,2.7)$, $(3,3.4),(4,3.8),(5,3.9)$. Describe the model that produces a least-squares fit of these points by a function of the form $y=\beta_1 x+\beta_2 x^2$
Such a function might arise, for example, as the revenue from the sale of $x$ units of a product, when the amount offered for sale affects the price to be set for the product.

1. Give the design matrix, the observation vector, and the unknown parameter vector.
2. [M] Find the associated least-squares curve for the data.

??? answer "&nbsp;"

**Exercise 11** (6.6.13)

[M] To measure the takeoff performance of an airplane, the horizontal position of the plane was measured every second, from $t=0$ to $t=12$. The positions (in feet) were: $0,8.8$, $29.9,62.0,104.7,159.1,222.0,294.5,380.4,471.1,571.7$, 686.8 , and 809.2.

1. Find the least-squares cubic curve $y=\beta_0+\beta_1 t+$ $\beta_2 t^2+\beta_3 t^3$ for these data.
2. Use the result of part (a) to estimate the velocity of the plane when $t=4.5$ seconds.