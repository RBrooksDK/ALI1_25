<h1 align="center">Eigenvalues</h1>

## Session Material:

Lay: ​5.1-5.3

[Recap and Exercises]()

[Session Notes]()

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EgXzFwcFf_tBh8mwVvN0UycBh_gTnjRq8A5x15bFaLKCTg?e=eGwSEq)

---

## Session Description

This session introduces some of the most powerful and fascinating concepts in linear algebra: eigenvalues and eigenvectors! We'll explore what these special vectors (eigenvectors) and scalars (eigenvalues) are – basically, vectors that only get scaled (not changed in direction) when a matrix transformation is applied. We'll learn how to find eigenvalues by solving the "characteristic equation" and then find the corresponding eigenvectors by solving a system of equations.

Understanding the set of all eigenvectors for a specific eigenvalue (the "eigenspace") is also key. Finally, we'll tackle the concept of "diagonalization" – a super useful technique where we can transform certain matrices into simpler diagonal forms using their eigenvectors and eigenvalues. This process, often called similarity transformation, simplifies many calculations and reveals deeper properties of the matrix and the transformation it represents.

### Key Concepts

- Eigenvalues
- Eigenvectors
- Characteristic Equation
- Eigenspaces
- Diagonalization
- Matrix Similarity

!!! tip "Learning Objectives"

    - Define and compute eigenvalues and eigenvectors for matrices.
    - Solve the characteristic equation and construct eigenspaces.
    - Diagonalize matrices and explain the process of similarity transformation.
    - Analyze the significance of eigenvalues and eigenvectors in matrix transformations.
    - Apply diagonalization to simplify matrix computations and interpret results.

## Exercises

<!--
​​5.1: 1, 3, 5, 7, 13, 16, 40
5.2: 1, 3, 6, 10, 11
5.3: 1, 6, 10-14, 35, 36
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 1** (5.1.1)

Is $\lambda=2$ an eigenvalue of $\left[\begin{array}{ll}3 & 2 \\ 3 & 8\end{array}\right]$ ? Why or why not?

??? answer "&nbsp;"

**Exercise 2** (5.1.3)

Is $\left[\begin{array}{l}1 \\ 3\end{array}\right]$ an eigenvector of $\left[\begin{array}{ll}1 & -1 \\ 6 & -4\end{array}\right]$ ? If so, find the eigenvalue.

??? answer "&nbsp;"

**Exercise 3** (5.1.5)

Is $\left[\begin{array}{r}3 \\ -2 \\ 1\end{array}\right]$ an eigenvector of $\left[\begin{array}{rrr}-4 & 3 & 3 \\ 2 & -3 & -2 \\ -1 & 0 & -2\end{array}\right]$ ? If so, find the eigenvalue.

??? answer "&nbsp;"

**Exercise 4** (5.1.7)

Is $\lambda=4$ an eigenvalue of $\left[\begin{array}{rrr}3 & 0 & -1 \\ 2 & 3 & 1 \\ -3 & 4 & 5\end{array}\right]$ ? If so, find one corresponding eigenvector.

??? answer "&nbsp;"

**Exercise 5** (5.1.13, 5.1.16)

Find a basis for the eigenspace corresponding to both listed eigenvalues.

13. $A=\left[\begin{array}{rrr}4 & 0 & 1 \\ -2 & 1 & 0 \\ -2 & 0 & 1\end{array}\right], \lambda=1,2,3$
14. $A=\left[\begin{array}{rrrr}5 & 0 & -1 & 0 \\ 1 & 3 & 0 & 0 \\ 2 & -1 & 3 & 0 \\ 4 & -2 & -2 & 4\end{array}\right], \lambda=4$

??? answer "&nbsp;"

**Exercise 6** (5.1.40)

[M] Use a matrix program to find the eigenvalues of the matrix. Then use the method of Example 4 with a row reduction routine to produce a basis for the eigenspace.

$\left[\begin{array}{rrrrr}-23 & 57 & -9 & -15 & -59 \\ -10 & 12 & -10 & 2 & -22 \\ 11 & 5 & -3 & -19 & -15 \\ -27 & 31 & -27 & 25 & -37 \\ -5 & -15 & -5 & 1 & 31\end{array}\right]$

??? answer "&nbsp;"

**Exercise 7** (5.2.1, 5.2.3, 5.2.6)

Find the characteristic polynomial and the real eigenvalues of the following matricies.

1. $\left[\begin{array}{ll}2 & 7 \\ 7 & 2\end{array}\right]$
2. $\left[\begin{array}{rr}-4 & 2 \\ 6 & 7\end{array}\right]$
3. $\left[\begin{array}{rr}9 & -2 \\ 2 & 5\end{array}\right]$

??? answer "&nbsp;"

**Exercise 8** (5.2.10, 5.2.11)

Following exercises require techniques from Section 3.1. Find the characteristic polynomial of each matrix, using either a cofactor expansion or the special formula for $3 \times 3$ determinants described prior to Exercises 15-18 in Section 3.1. [Note: Finding the characteristic polynomial of a $3 \times 3$ matrix is not easy to do with just row operations, because the variable $\lambda$ is involved.]

10. $\left[\begin{array}{rrr}3 & 1 & 1 \\ 0 & 5 & 0 \\ -2 & 0 & 7\end{array}\right]$
11. $\left[\begin{array}{lll}3 & 0 & 0 \\ 2 & 1 & 4 \\ 1 & 0 & 4\end{array}\right]$

??? answer "&nbsp;"

**Exercise 9** (5.3.1)

Let $A=P D P^{-1}$ and compute $A^4$.

$P=\left[\begin{array}{ll}5 & 7 \\ 2 & 3\end{array}\right], D=\left[\begin{array}{ll}2 & 0 \\ 0 & 1\end{array}\right]$

??? answer "&nbsp;"

**Exercise 10** (5.3.6)

The matrix $A$ is factored in the form $P D P^{-1}$. Use the Diagonalization Theorem to find the eigenvalue of $A$ and a basis for the eigenspace.

$\begin{aligned} A & =\left[\begin{array}{rrr}3 & 0 & 0 \\ -3 & 4 & 9 \\ 0 & 0 & 3\end{array}\right] \\ & =\left[\begin{array}{rrr}3 & 0 & -1 \\ 0 & 1 & -3 \\ 1 & 0 & 0\end{array}\right]\left[\begin{array}{lll}3 & 0 & 0 \\ 0 & 4 & 0 \\ 0 & 0 & 3\end{array}\right]\left[\begin{array}{rrr}0 & 0 & 1 \\ -3 & 1 & 9 \\ -1 & 0 & 3\end{array}\right]\end{aligned}$

??? answer "&nbsp;"

**Exercise 11** (5.3.10-14)

Diagonalize the matrices, if possible. The real eigenvalues for Exercises (b)-(e) are included next to the matrix.

10. $\left[\begin{array}{ll}1 & 3 \\ 4 & 2\end{array}\right]$
11. $\left[\begin{array}{lll}0 & 1 & 1 \\ 2 & 1 & 2 \\ 3 & 3 & 2\end{array}\right]$
    $\lambda=-1,5$
12. $\left[\begin{array}{lll}3 & 1 & 1 \\ 1 & 3 & 1 \\ 1 & 1 & 3\end{array}\right]$
    $\lambda=2,5$
13. $\left[\begin{array}{rrr}2 & 2 & -1 \\ 1 & 3 & -1 \\ -1 & -2 & 2\end{array}\right]$
    $\lambda=1,5$
14. $\left[\begin{array}{rrr}2 & 0 & -2 \\ 1 & 3 & 2 \\ 0 & 0 & 3\end{array}\right]$
    $\lambda=2,3$

??? answer "&nbsp;"

**Exercise 12** (5.3.35, 5.3.36)

[M] Diagonalize the matrices. Use your matrix program's eigenvalue command to find the eigenvalues, and then compute bases for the eigenspaces as in Section 5.1.

35. $\left[\begin{array}{rrrrr}13 & -12 & 9 & -15 & 9 \\ 6 & -5 & 9 & -15 & 9 \\ 6 & -12 & -5 & 6 & 9 \\ 6 & -12 & 9 & -8 & 9 \\ -6 & 12 & 12 & -6 & -2\end{array}\right]$
36. $\left[\begin{array}{rrrrr}24 & -6 & 2 & 6 & 2 \\ 72 & 51 & 9 & -99 & 9 \\ 0 & -63 & 15 & 63 & 63 \\ 72 & 15 & 9 & -63 & 9 \\ 0 & 63 & 21 & -63 & -27\end{array}\right]$