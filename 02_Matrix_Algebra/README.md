<h1 align="center">Matrix Algebra</h1>

## Session Material:

Lay: 2.1-2.7 (2.4 + 2.6-2.7 self-study)

[Recap and Exercises]()

[Session Notes]()

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EgCkADot6NBNgecwld6KLpwBki3OkF32RFBmtB_xbwSBoQ?e=DY1uNJ)

---

## Session Description

Now that we’ve learned to represent and solve systems with matrices, this session focuses on doing algebra with matrices themselves. We’ll start with basic operations like addition, scalar multiplication, and then tackle matrix multiplication — both its definition and the practical row-column rule.

We’ll explore special matrices (zero, identity, diagonal), powers, and transposes, and discuss how matrix operations differ from regular arithmetic. Key theorems (1–3 for operations, 5–7 for inverses) will guide us through the rules. A central idea is the invertible matrix and to find it using row reduction.

We’ll finish with the Invertible Matrix Theorem (Theorem 8), which ties together many core ideas.

### Key Concepts

* Matrix Operations
* Matrix Multiplication
* Special Matrices: Zero, Identity, Diagonal
* Matrix Powers
* Matrix Transpose
* Invertible Matrices
* Invertible Matrix Theorem
* Matrix Algebra
  
!!! tip "Learning Objectives"

    - Perform matrix addition, scalar multiplication, and matrix multiplication using the row-column rule.
    - Identify and use special matrices (zero, identity, diagonal) and their properties.
    - Compute and interpret matrix inverses and transposes.
    - Apply the Invertible Matrix Theorem
    - Analyze and solve problems using matrix algebra concepts.

---

## Exercises

<!-- 
1.7: 11, 15-20, 41​​​  
1.8: 3-6, 10  
1.9: 15      
2.1: 1, 2, 10, 13, 40, 41   
2.2: 9, 30, 31, 32   
​2.3: 11, 12, 15, 17  
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

**Exercise 1** (1.7.11)

Find the value(s) of $h$ for which the vectors are linearly dependent. Justify your answer.

$\left[\begin{array}{r}2 \\ -2 \\ 4\end{array}\right],\left[\begin{array}{r}4 \\ -6 \\ 7\end{array}\right],\left[\begin{array}{r}-2 \\ 2 \\ h\end{array}\right]$

??? answer "&nbsp;"

**Exercise 2** (1.7.15-1.7.20)

Determine by inspection whether the vectors in Exercises a-f are linearly independent. Justify each answer.

1. $\left[\begin{array}{l}5 \\ 1\end{array}\right],\left[\begin{array}{l}2 \\ 8\end{array}\right],\left[\begin{array}{l}1 \\ 3\end{array}\right],\left[\begin{array}{r}-1 \\ 7\end{array}\right]$
2. $\left[\begin{array}{r}2 \\ -4 \\ 8\end{array}\right],\left[\begin{array}{r}-3 \\ 6 \\ -12\end{array}\right]$
3. $\left[\begin{array}{r}5 \\ -3 \\ -1\end{array}\right],\left[\begin{array}{l}0 \\ 0 \\ 0\end{array}\right],\left[\begin{array}{r}-7 \\ 2 \\ 4\end{array}\right]$
4. $\left[\begin{array}{l}3 \\ 4\end{array}\right],\left[\begin{array}{r}-1 \\ 5\end{array}\right],\left[\begin{array}{l}3 \\ 5\end{array}\right],\left[\begin{array}{l}7 \\ 1\end{array}\right]$
5. $\left[\begin{array}{r}-8 \\ 12 \\ -4\end{array}\right],\left[\begin{array}{r}2 \\ -3 \\ -1\end{array}\right]$
6. $\left[\begin{array}{r}1 \\ 4 \\ -7\end{array}\right],\left[\begin{array}{r}-2 \\ 5 \\ 3\end{array}\right],\left[\begin{array}{l}0 \\ 0 \\ 0\end{array}\right]$

??? answer "&nbsp;"

**Exercise 3** (1.7.41)

[M] Use as many columns of $A$ as possible to construct a matrix $B$ with the property that the equation $B \mathbf{x}=\mathbf{0}$ has only the trivial solution. Solve $B \mathbf{x}=\mathbf{0}$ to verify your work.

$A=\left[\begin{array}{rrrrr}3 & -4 & 10 & 7 & -4 \\ -5 & -3 & -7 & -11 & 15 \\ 4 & 3 & 5 & 2 & 1 \\ 8 & -7 & 23 & 4 & 15\end{array}\right]$

??? answer "&nbsp;"

**Exercise 4** (1.8.3-1.8.6)

In Exercises a-d, with $T$ defined by $T(\mathbf{x})=A \mathbf{x}$, find a vector $\mathbf{x}$ whose image under $T$ is $\mathbf{b}$, and determine whether $\mathbf{x}$ is unique.

1. $A=\left[\begin{array}{rrr}1 & 0 & -3 \\ -3 & 1 & 6 \\ 2 & -2 & -1\end{array}\right], \mathbf{b}=\left[\begin{array}{r}-2 \\ 3 \\ -1\end{array}\right]$
2. $A=\left[\begin{array}{rrr}1 & -2 & 3 \\ 0 & 1 & -3 \\ 2 & -5 & 6\end{array}\right], \mathbf{b}=\left[\begin{array}{l}-6 \\ -4 \\ -5\end{array}\right]$
3. $A=\left[\begin{array}{rrr}1 & -5 & -7 \\ -3 & 7 & 5\end{array}\right], \mathbf{b}=\left[\begin{array}{l}-2 \\ -2\end{array}\right]$
4. $A=\left[\begin{array}{rrr}1 & -3 & 2 \\ 3 & -8 & 8 \\ 0 & 1 & 2 \\ 1 & 0 & 8\end{array}\right], \mathbf{b}=\left[\begin{array}{r}1 \\ 6 \\ 3 \\ 10\end{array}\right]$

??? answer "&nbsp;"

**Exercise 5** (1.8.10)

Find all $\mathbf{x}$ in $\mathbb{R}^4$ that are mapped into the zero vector by the transformation $\mathbf{x} \mapsto A \mathbf{x}$ for the given matrix $A$.

$A=\left[\begin{array}{rrrr}3 & 2 & 10 & -6 \\ 1 & 0 & 2 & -4 \\ 0 & 1 & 2 & 3 \\ 1 & 4 & 10 & 8\end{array}\right]$

??? answer "&nbsp;"

**Exercise 6** (1.9.15)

Fill in the missing entries of the matrix, assuming that the equation holds for all values of the variables.

$\left[\begin{array}{lll}? & ? & ? \\ ? & ? & ? \\ ? & ? & ?\end{array}\right]\left[\begin{array}{l}x_1 \\ x_2 \\ x_3\end{array}\right]=\left[\begin{array}{c}2 x_1-4 x_2 \\ x_1-x_3 \\ -x_2+3 x_3\end{array}\right]$

??? answer "&nbsp;"

**Exercise 7** (2.1.1-2.1.2)

Compute each matrix sum or product if it is defined. If an expression is undefined, explain why. Let

$$
\begin{aligned}
& A=\left[\begin{array}{rrr}
2 & 0 & -1 \\
4 & -5 & 2
\end{array}\right], \quad B=\left[\begin{array}{rrr}
7 & -5 & 1 \\
1 & -4 & -3
\end{array}\right], \\
& C=\left[\begin{array}{rr}
1 & 2 \\
-2 & 1
\end{array}\right], \quad D=\left[\begin{array}{rr}
3 & 5 \\
-1 & 4
\end{array}\right], \quad E=\left[\begin{array}{r}
-5 \\
3
\end{array}\right]
\end{aligned}
$$

1. $-2 A, B-2 A, A C, C D$
2. $A+3 B, 2 C-3 E, D B, E C$

??? answer "&nbsp;"

**Exercise 8** (2.1.10)

Assume that each matrix expression is defined. That is, the sizes of the matrices (and vectors) involved "match" appropriately.

Let $\quad A=\left[\begin{array}{rr}3 & -6 \\ -1 & 2\end{array}\right], \quad B=\left[\begin{array}{rr}-1 & 1 \\ 3 & 4\end{array}\right], \quad$ and $\quad C=$ $\left[\begin{array}{rr}-3 & -5 \\ 2 & 1\end{array}\right]$. Verify that $A B=A C$ and yet $B \neq C$.

??? answer "&nbsp;"

**Exercise 9** (2.1.13)

Assume that each matrix expression is defined. That is, the sizes of the matrices (and vectors) involved "match" appropriately.

Let $\mathbf{r}_1, \ldots, \mathbf{r}_p$ be vectors in $\mathbb{R}^n$, and let $Q$ be an $m \times n$ matrix. Write the matrix $\left[\begin{array}{lll}Q \mathbf{r}_1 & \cdots & Q \mathbf{r}_p\end{array}\right]$ as a product of two matrices (neither of which is an identity matrix).

??? answer "&nbsp;"

**Exercise 10** (2.1.40)

$[\mathbf{M}]$ Let

$$
S=\left[\begin{array}{lllll}
0 & 1 & 0 & 0 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 & 0 \\
0 & 0 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 & 0
\end{array}\right]
$$

Compute $S^k$ for $k=2, \ldots, 6$.

??? answer "&nbsp;"

**Exercise 11** (2.1.41)

Assume that each matrix expression is defined. That is, the sizes of the matrices (and vectors) involved "match" appropriately.

$[\mathbf{M}]$ Describe in words what happens when $A^5, A^{10}, A^{20}$, and $A^{30}$ are computed for

$$
A=\left[\begin{array}{rrr}
1 / 4 & 1 / 2 & 1 / 4 \\
1 / 2 & 1 / 3 & 1 / 6 \\
1 / 4 & 1 / 6 & 7 / 12
\end{array}\right]
$$


??? answer "&nbsp;"

**Exercise 12** (2.2.9)

1. In order for a matrix $B$ to be the inverse of $A$, the equations $A B=I$ and $B A=I$ must both be true.
2. If $A$ and $B$ are $n \times n$ and invertible, then $A^{-1} B^{-1}$ is the inverse of $A B$.
3. If $A=\left[\begin{array}{ll}a & b \\ c & d\end{array}\right]$ and $a b-c d \neq 0$, then $A$ is invertible.
4. If $A$ is an invertible $n \times n$ matrix, then the equation $A \mathbf{x}=\mathbf{b}$ is consistent for each $\mathbf{b}$ in $\mathbb{R}^n$.
5. Each elementary matrix is invertible.

??? answer "&nbsp;"

**Exercise 13** (2.2.30-2.2.32)

Find the inverses of the matrices, if they exist. Use the algorithm introduced in this section.

1. $\left[\begin{array}{ll}3 & 6 \\ 4 & 7\end{array}\right]$
2. $\left[\begin{array}{rrr}1 & 0 & -2 \\ -3 & 1 & 4 \\ 2 & -3 & 4\end{array}\right]$
3. $\left[\begin{array}{rrr}1 & 2 & -1 \\ -4 & -7 & 3 \\ -2 & -6 & 4\end{array}\right]$

??? answer "&nbsp;"

**Exercise 14** (2.3.11)

1. If the equation $A \mathbf{x}=\mathbf{0}$ has only the trivial solution, then $A$ is row equivalent to the $n \times n$ identity matrix.
2. If the columns of $A$ span $\mathbb{R}^n$, then the columns are linearly independent.
3. If $A$ is an $n \times n$ matrix, then the equation $A \mathbf{x}=\mathbf{b}$ has at least one solution for each $\mathbf{b}$ in $\mathbb{R}^n$.
4. If the equation $A \mathbf{x}=\mathbf{0}$ has a nontrivial solution, then $A$ has fewer than $n$ pivot positions.
5. If $A^T$ is not invertible, then $A$ is not invertible.

??? answer "&nbsp;"

**Exercise 15** (2.3.12)

1. If there is an $n \times n$ matrix $D$ such that $A D=I$, then $D A=I$.
2. If the linear transformation $\mathbf{x} \mapsto A \mathbf{x}$ maps $\mathbb{R}^n$ into $\mathbb{R}^n$, then the row reduced echelon form of $A$ is $I$.
3. If the columns of $A$ are linearly independent, then the columns of $A$ span $\mathbb{R}^n$.
4. If the equation $A \mathbf{x}=\mathbf{b}$ has at least one solution for each $\mathbf{b}$ in $\mathbb{R}^n$, then the transformation $\mathbf{x} \mapsto A \mathbf{x}$ is not one-to-one.
5. If there is a $\mathbf{b}$ in $\mathbb{R}^n$ such that the equation $A \mathbf{x}=\mathbf{b}$ is consistent, then the solution is unique.

??? answer "&nbsp;"

**Exercise 16** (2.3.15)

Is it possible for a $4 \times 4$ matrix to be invertible when its columns do not span $\mathbb{R}^4$ ? Why or why not?

??? answer "&nbsp;"

**Exercise 17** (2.3.17)

Can a square matrix with two identical columns be invertible? Why or why not?