<h1 align="center">Introduction to Linear Algebra</h1>

## Session Material:
Lay: 1.1-1.5  + 1.7-1.10 (1.8-1.10 self-study)  


[Session Notes]()

[Session Material](https://viaucdk-my.sharepoint.com/:f:/g/personal/rib_viauc_dk/EiMKdymBUehBpz9ft6ta4NABEVbrfJnmhYTNyJLH83PH9w?e=iY0JyU)

---

## Session Description

We'll begin with systems of linear equations, what they are, how to represent them with matrices, and how to solve them using row reduction. You'll learn key row operations, how to reach echelon forms, identify pivots, and determine basic and free variables. We'll cover when systems have unique, infinite, or no solutions, revisiting concepts like Theorem 2.

Next, we introduce vectors: linear combinations, spans, and how vector equations relate to linear systems, with geometric intuition in 2D and 3D. We'll examine linear dependence and independence, identifying redundant vectors and linking this to simple homogeneous systems (Theorems 7–9). Finally, we'll introduce linear transformations, how matrices map vectors between spaces, laying a vital foundation for what's to come.

### Key Concepts

 - Linear Systems
 - Matrices
 - Row Reduction
 - Vectors
 - Span
 - Linear Dependence
 - Linear Transformations

!!! tip "Learning Objectives"

    - Identify and represent linear systems using matrices.
    - Apply row reduction techniques to solve linear systems.
    - Describe and construct vectors, spans, and linear combinations.
    - Distinguish and determine linear dependence and independence in sets of vectors.
    - Analyze and interpret linear transformations and their relationship with matrices.

---

## Quiz

After the session, you should be able to answer this quiz. You can see your score at the bottom of the page. Your answers are not saved or recorded.

---

<?quiz?>
question: A system of linear equations has no solution if its augmented matrix, after row reduction to echelon form, contains a row of the form:
answer: $[0 \; 0 \; \dots \; 0 \; | \; 0]$
answer: A row where every entry is non-zero.
answer: $[1 \; 0 \; \dots \; 0 \; | \; b]$ where $b$ is any real number.
answer-correct: $[0 \; 0 \; \dots \; 0 \; | \; b]$ where $b$ is a non-zero real number.
answer: A column corresponding to a free variable.
content:
<p><strong>Explanation:</strong> A row of the form $[0 \; 0 \; \dots \; 0 \; | \; b]$ where $b \neq 0$ represents the equation $0x_1 + 0x_2 + \dots + 0x_n = b$. If $b$ is non-zero, this equation is $0 = b$, which is a contradiction. Therefore, the system is inconsistent and has no solution. This relates to understanding when systems have unique, infinite, or no solutions based on their echelon form.</p>
<?/quiz?>

---

<?quiz?>
question: Consider the matrix equation $Ax = b$. If the vector $b$ can be written as a linear combination of the columns of matrix $A$, what can be said about the system?
answer-correct: The system $Ax = b$ is consistent (has at least one solution).
answer: The system has no solution.
answer: The columns of $A$ are linearly dependent.
answer: The matrix $A$ must be invertible.
answer: The system has a unique solution only if $A$ is an identity matrix.
content:
<p><strong>Explanation:</strong> The definition of $Ax$ is a linear combination of the columns of $A$ using the entries of $x$ as weights. If $b$ is in the span of the columns of $A$ (meaning $b$ <em>is</em> a linear combination of the columns of $A$), then there exists at least one vector $x$ such that $Ax = b$. This means the system is consistent.</p>
<?/quiz?>

---

<?quiz?>
question: Which of the following sets of vectors in $\mathbb{R}^3$ is linearly dependent. Let $v_1 = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix}$, $v_2 = \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix}$, $v_3 = \begin{bmatrix} 0 \\ 0 \\ 1 \end{bmatrix}$, $v_4 = \begin{bmatrix} 2 \\ 0 \\ 0 \end{bmatrix}.$

answer: $\{v_1, v_2, v_3\}$
answer: $\{v_1, v_2\}$
answer: $\{v_2, v_3\}$
answer: $\{v_1, v_3\}$
answer-correct: $\{v_1, v_4\}$
content:
<p><strong>Explanation:</strong> A set of vectors is linearly dependent if at least one vector in the set can be written as a linear combination of the others, or equivalently, if there's a non-trivial solution to $c_1\mathbf{v}_1 + c_2\mathbf{v}_2 + \dots + c_p\mathbf{v}_p = \mathbf{0}$. In this case, $v_4 = 2v_1$. Thus, $2v_1 - v_4 = \mathbf{0}$ is a non-trivial linear combination that equals the zero vector, making the set $\{v_1, v_4\}$ linearly dependent. The set $\{v_1, v_2, v_3\}$ is the standard basis for $\mathbb{R}^3$ and is linearly independent.</p>
<?/quiz?>

---

<?quiz?>
question: A linear transformation $T: \mathbb{R}^n \to \mathbb{R}^m$ is defined by $T(x) = Ax$. If $A$ is an $m \times n$ matrix with $n$ pivot positions (i.e., a pivot in every column), what can be concluded about the columns of $A$?
answer: The matrix $A$ has $m$ rows.
answer-correct: The columns of $A$ are linearly independent.
answer: The columns of $A$ span $\mathbb{R}^m$.
answer: The transformation $T$ is onto $\mathbb{R}^m$.
answer: The equation $Ax = \mathbf{0}$ has infinitely many solutions.
content:
<p><strong>Explanation:</strong> If an $m \times n$ matrix $A$ has $n$ pivot positions, it means there is a pivot in every column. This implies that the equation $Ax = \mathbf{0}$ has only the trivial solution. By definition (Theorem 7, or related concepts), this means the columns of $A$ are linearly independent. It does not guarantee that $T$ is onto unless $m=n$, nor does it guarantee that the columns span $\mathbb{R}^m$ unless $m \le n$ and there are $m$ pivots.</p>
<?/quiz?>

---

<?quiz?>
question: Given the augmented matrix $\begin{bmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \end{bmatrix}$ which is in echelon form, how many solutions does the corresponding system of linear equations have?
answer: Exactly two solutions.
answer: No solution.
answer-correct: Infinitely many solutions.
answer: Exactly one unique solution.
answer: The number of solutions cannot be determined from this form.
content:
<p><strong>Explanation:</strong> The matrix represents the system $x_1 + 2x_2 = 3$ and $0x_1 + 0x_2 = 0$. The second equation $0=0$ is always true and provides no restriction. The first column (for $x_1$) has a pivot, but the second column (for $x_2$) does not. This means $x_2$ is a free variable. Since there is at least one free variable and the system is consistent (no row like $[0 \; 0 \; | \; b]$ where $b \neq 0$), the system has infinitely many solutions. This relates to identifying pivots and basic/free variables.</p>
<?/quiz?>

---

<?quiz?>

question: Consider the system of linear equations: $x_1 + 2x_2 - x_3 = 1$, $2x_1 + 5x_2 + x_3 = 4$, $x_1 + 3x_2 + 2x_3 = 3$. After performing row operations to bring the augmented matrix to row echelon form, one possible row echelon form is $\begin{bmatrix} 1 & 2 & -1 & | & 1 \\ 0 & 1 & 3 & | & 2 \\ 0 & 0 & 0 & | & 0 \end{bmatrix}$. Which variable is a free variable?
answer: $x_1$
answer: There are no free variables.
answer-correct: $x_3$
answer: $x_2$
answer: Both $x_2$ and $x_3$ are free variables.
content:

<p><strong>Explanation:</strong> In the given row echelon form, the pivot columns are the first and second columns (corresponding to $x_1$ and $x_2$). The third column (corresponding to $x_3$) does not contain a pivot. Therefore, $x_3$ is a free variable. The system has infinitely many solutions.</p>
<?/quiz?>

---

<?quiz?>


question: Let $A = \begin{bmatrix} 1 & -2 & 1 \\ 0 & 2 & -8 \\ -4 & 5 & 9 \end{bmatrix}$ and $b = \begin{bmatrix} 0 \\ 8 \\ -9 \end{bmatrix}$. The augmented matrix $[A|b]$ can be row reduced to $\begin{bmatrix} 1 & 0 & -7 & | & 8 \\ 0 & 1 & -4 & | & 4 \\ 0 & 0 & 0 & | & 0 \end{bmatrix}$. What is the solution $x$ to $Ax = b$ if we let the free variable be $x_3 = t$?
answer: $x = \begin{bmatrix} 8 \\ 4 \\ 0 \end{bmatrix} + t \begin{bmatrix} -7 \\ -4 \\ 0 \end{bmatrix}$
answer: $x = \begin{bmatrix} 8 \\ 4 \\ t \end{bmatrix}$
answer: $x = \begin{bmatrix} -7 \\ -4 \\ 1 \end{bmatrix} + t \begin{bmatrix} 8 \\ 4 \\ 0 \end{bmatrix}$
answer: The system has no solution.
answer-correct: $x = \begin{bmatrix} 8 \\ 4 \\ 0 \end{bmatrix} + t \begin{bmatrix} 7 \\ 4 \\ 1 \end{bmatrix}$
content:

<p><strong>Explanation:</strong> From the reduced row echelon form, we have the equations: $x_1 - 7x_3 = 8$ and $x_2 - 4x_3 = 4$. Since $x_3$ is free, let $x_3 = t$. Then $x_1 = 8 + 7t$ and $x_2 = 4 + 4t$. In vector form, this is $x = \begin{bmatrix} x_1 \\ x_2 \\ x_3 \end{bmatrix} = \begin{bmatrix} 8 + 7t \\ 4 + 4t \\ t \end{bmatrix} = \begin{bmatrix} 8 \\ 4 \\ 0 \end{bmatrix} + t \begin{bmatrix} 7 \\ 4 \\ 1 \end{bmatrix}$.</p>
<?/quiz?>

---

<?quiz?>


question: For what value(s) of $h$ will the vectors $v_1 = \begin{bmatrix} 1 \\ -1 \\ -2 \end{bmatrix}$, $v_2 = \begin{bmatrix} 5 \\ -4 \\ -7 \end{bmatrix}$, $v_3 = \begin{bmatrix} -3 \\ 1 \\ h \end{bmatrix}$ be linearly dependent?
answer-correct: $h = 0$ only
answer: For all values of $h$.
answer: For no values of $h$.
answer: $h = -1$
answer: $h = 3$
content:

<p><strong>Explanation:</strong> The vectors are linearly dependent if the matrix $A = [v_1 \ v_2 \ v_3]$ has fewer than 3 pivots, or if the augmented matrix $[A | \mathbf{0}]$ has a non-trivial solution. Here is the row reduction for the matrix

$$\begin{aligned}
&\begin{bmatrix}
1 & 5 & -3 \\
-1 & -4 & 1 \\
-2 & -7 & h
\end{bmatrix}
\quad
\xrightarrow{\, R_2 \mapsto R_2 + R_1 \,,\, R_3 \mapsto R_3 + 2R_1 \,}
\quad
\begin{bmatrix}
1 & 5 & -3 \\
0 & 1 & -2 \\
0 & 3 & h - 6
\end{bmatrix} \\[1em]
&\xrightarrow{\, R_3 \mapsto R_3 - 3R_2 \,}
\quad
\begin{bmatrix}
1 & 5 & -3 \\
0 & 1 & -2 \\
0 & 0 & h
\end{bmatrix}
\end{aligned}$$

Since the last row has a pivot in the third column if $h \neq 0$, the vectors are linearly independent. If $h = 0$, the last row becomes $[0 \; 0 \; 0]$, indicating that the vectors are linearly dependent. Thus, the only value of $h$ that makes the vectors linearly dependent is $h = 0$.</p>


<?/quiz?>

---

<?quiz?>


question: Let $T: \mathbb{R}^2 \to \mathbb{R}^2$ be a linear transformation such that $T\left(\begin{bmatrix} 1 \\ 0 \end{bmatrix}\right) = \begin{bmatrix} 2 \\ 5 \end{bmatrix}$ and $T\left(\begin{bmatrix} 0 \\ 1 \end{bmatrix}\right) = \begin{bmatrix} -1 \\ 6 \end{bmatrix}$. What is $T\left(\begin{bmatrix} 3 \\ -2 \end{bmatrix}\right)$ (you will need to do some calculations!)?
answer: $\begin{bmatrix} 1 \\ 11 \end{bmatrix}$
answer-correct: $\begin{bmatrix} 8 \\ 3 \end{bmatrix}$
answer: $\begin{bmatrix} 4 \\ 27 \end{bmatrix}$
answer: $\begin{bmatrix} 5 \\ -7 \end{bmatrix}$
answer: $\begin{bmatrix} 6 \\ -10 \end{bmatrix}$
content:

<p><strong>Explanation:</strong> Since $T$ is a linear transformation, $T(x+y) = T(x) + T(y)$ and $T(cx) = cT(x)$. We can write 
$$\begin{bmatrix} 3 \\ -2 \end{bmatrix} = 3\begin{bmatrix} 1 \\ 0 \end{bmatrix} - 2\begin{bmatrix} 0 \\ 1 \end{bmatrix}$$
Therefore,
$$\begin{aligned}
T\left(\begin{bmatrix} 3 \\ -2 \end{bmatrix}\right) &= T\left(3\begin{bmatrix} 1 \\ 0 \end{bmatrix} - 2\begin{bmatrix} 0 \\ 1 \end{bmatrix}\right) \\
&= 3T\left(\begin{bmatrix} 1 \\ 0 \end{bmatrix}\right) - 2T\left(\begin{bmatrix} 0 \\ 1 \end{bmatrix}\right) \\
&= 3\begin{bmatrix} 2 \\ 5 \end{bmatrix} - 2\begin{bmatrix} -1 \\ 6 \end{bmatrix} \\
&= \begin{bmatrix} 6 \\ 15 \end{bmatrix} - \begin{bmatrix} -2 \\ 12 \end{bmatrix} \\
&= \begin{bmatrix} 6 - (-2) \\ 15 - 12 \end{bmatrix} \\
&= \begin{bmatrix} 8 \\ 3 \end{bmatrix}
\end{aligned}$$

Alternatively, the standard matrix for $T$ is 
$$A = \begin{bmatrix} T(e_1) & T(e_2) \end{bmatrix} = \begin{bmatrix} 2 & -1 \\ 5 & 6 \end{bmatrix}$$

Then
$$\begin{aligned}
T(x) = Ax &= \begin{bmatrix} 2 & -1 \\ 5 & 6 \end{bmatrix} \begin{bmatrix} 3 \\ -2 \end{bmatrix} \\
&= \begin{bmatrix} (2)(3) + (-1)(-2) \\ (5)(3) + (6)(-2) \end{bmatrix} \\
&= \begin{bmatrix} 6+2 \\ 15-12 \end{bmatrix} \\
&= \begin{bmatrix} 8 \\ 3 \end{bmatrix}
\end{aligned}$$</p>
<?/quiz?>

---

<?quiz?>


question: If $A$ is an $m \times n$ matrix whose columns span $\mathbb{R}^m$, what must be true about the echelon form of $A$? (Revisiting concepts like Theorem 2 or 4 from Lay's book context)
answer: $A$ has a pivot position in every column.
answer: $A$ has $n$ rows.
answer: The equation $Ax = \mathbf{0}$ has only the trivial solution.
answer: $m < n$.
answer-correct: $A$ has a pivot position in every row.
content:

<p><strong>Explanation:</strong> If the columns of an $m \times n$ matrix $A$ span $\mathbb{R}^m$, it means that for every $b$ in $\mathbb{R}^m$, the equation $Ax = b$ has a solution. This is equivalent to stating that matrix $A$ has a pivot position in every row (according to Theorem 4 in Lay, etc., or similar theorems). This ensures there's no row of zeros in the coefficient part of the augmented matrix $[A|b]$ that could lead to an inconsistency like $0=c$ where $c \neq 0$.</p>
<?/quiz?>

---

## Exercises

**Exercise 1**

??? answer "&nbsp;"

**Exercise 2**

??? answer "&nbsp;"

**Exercise 3**

??? answer "&nbsp;"

**Exercise 4**

??? answer "&nbsp;"

**Exercise 5**

??? answer "&nbsp;"

**Exercise 6**

??? answer "&nbsp;"

**Exercise 7**

??? answer "&nbsp;"

**Exercise 8**

??? answer "&nbsp;"

**Exercise 9**

??? answer "&nbsp;"

**Exercise 10**

??? answer "&nbsp;"