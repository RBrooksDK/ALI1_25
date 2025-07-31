<h1 align="center">Introduction to Linear Algebra</h1>

## Session Material:
Lay: 1.1-1.5  + 1.7-1.10 (1.8-1.10 self-study)  


[Session Notes](https://drive.google.com/file/d/1ICEnghBXNo3U_R6AS3uUzzUHit7FCVRy/view?usp=sharing)

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

<!-- 
1.2: 1, 7, 9, 11, 33   
1.3: 11, 13, 14, 28     
1.4: 6, 8, 11, 17, 18​   
1.5: 7, 15, 23, 24 
-->
<style type="text/css">
    ol { list-style-type: lower-alpha; }
</style>

## Exercises

**Exercise 1** (1.2.1)

Determine which matrices are in reduced echelon form and which others are only in echelon form.

1. $\left[\begin{array}{llll}1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 1 & 1\end{array}\right]$
2. $\left[\begin{array}{llll}1 & 0 & 1 & 0 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 0 & 1\end{array}\right]$
3. $\left[\begin{array}{llll}1 & 0 & 0 & 0 \\ 0 & 1 & 1 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 1\end{array}\right]$
4. $\left[\begin{array}{lllll}1 & 1 & 0 & 1 & 1 \\ 0 & 2 & 0 & 2 & 2 \\ 0 & 0 & 0 & 3 & 3 \\ 0 & 0 & 0 & 0 & 4\end{array}\right]$

??? answer "&nbsp;"
    1. Reduced echelon form
    2. Reduced echelon form
    3. Not echelon form
    4. Echelon form

**Exercise 2** (1.2.7)

Find the general solution of the given system.

$\left[\begin{array}{llll}1 & 3 & 4 & 7 \\ 3 & 9 & 7 & 6\end{array}\right]$

??? answer "&nbsp;"
    $$
    \left\{
      \begin{array}{l}
        x_1 = -5 - 3 x_2 \\
        x_2 \text{ is free } \\
        x_3 = 3
      \end{array}
    \right.
    $$

**Exercise 3** (1.2.9)

Find the general solution of the given system.

$\left[\begin{array}{rrrr}0 & 1 & -2 & 3 \\ 1 & -3 & 4 & -6\end{array}\right]$

??? answer "&nbsp;"
    $$
    \left\{
        \begin{array}{l}
            x_1=3+2 x_3 \\
            x_2=3+2 x_3 \\
            x_3 \text { is free }
        \end{array}\right.
    $$

**Exercise 4** (1.2.11)

Find the general solution of the given system.

$\left[\begin{array}{rrrr}3 & -2 & 4 & 0 \\ 9 & -6 & 12 & 0 \\ 6 & -4 & 8 & 0\end{array}\right]$

??? answer "&nbsp;"
    $$
    \left\{
        \begin{array}{l}
            x_1=\frac{2}{3} x_2-\frac{4}{3} x_3 \\
            x_2 \text { is free } \\
            x_3 \text { is free }
        \end{array}\right.
    $$

**Exercise 5** (1.2.33)

Find the interpolating polynomial $p(t)=a_0+a_1 t+a_2 t^2$ for the data $(1,6),(2,15),(3,28)$. That is, find $a_0, a_1$, and $a_2$ such that

$$
\begin{aligned}
& a_0+a_1(1)+a_2(1)^2=6 \\
& a_0+a_1(2)+a_2(2)^2=15 \\
& a_0+a_1(3)+a_2(3)^2=28
\end{aligned}
$$

??? answer "&nbsp;"
    The polynomial is $p(t)=1+3 t+2 t^2$.

**Exercise 6** (1.3.11)

Determine if $\mathbf{b}$ is a linear combination of $\mathbf{a}_1, \mathbf{a}_2$, and $\mathbf{a}_3$.

$\mathbf{a}_1=\left[\begin{array}{r}1 \\ -2 \\ 0\end{array}\right], \mathbf{a}_2=\left[\begin{array}{l}0 \\ 1 \\ 2\end{array}\right], \mathbf{a}_3=\left[\begin{array}{r}5 \\ -6 \\ 8\end{array}\right], \mathbf{b}=\left[\begin{array}{r}2 \\ -1 \\ 6\end{array}\right]$

??? answer "&nbsp;"
    $\mathbf{b}$ is a linear combination of $\mathbf{a}_1, \mathbf{a}_2$, and $\mathbf{a}_3$.

**Exercise 7** (1.3.13)

Determine if $\mathbf{b}$ is a linear combination of the vectors formed from the columns of the matrix $A$.

$A=\left[\begin{array}{rrr}1 & -4 & 2 \\ 0 & 3 & 5 \\ -2 & 8 & -4\end{array}\right], \mathbf{b}=\left[\begin{array}{r}3 \\ -7 \\ -3\end{array}\right]$

??? answer "&nbsp;"
    $\mathbf{b}$ is not a linear combination of the columns of $A$.

**Exercise 8** (1.3.14)

Determine if $\mathbf{b}$ is a linear combination of the vectors formed from the columns of the matrix $A$.

$A=\left[\begin{array}{rrr}1 & 0 & 5 \\ -2 & 1 & -6 \\ 0 & 2 & 8\end{array}\right], \mathbf{b}=\left[\begin{array}{r}2 \\ -1 \\ 6\end{array}\right]$

??? answer "&nbsp;"
    $\mathbf{b}$ is a linear combination of the columns of $A$.

**Exercise 9** (1.3.28)

A steam plant burns two types of coal: anthracite (A) and bituminous (B). For each ton of A burned, the plant produces 27.6 million Btu of heat, 3100 grams (g) of sulfur dioxide, and 250 g of particulate matter (solid-particle pollutants). For each ton of B burned, the plant produces 30.2 million Btu, 6400 g of sulfur dioxide, and 360 g of particulate matter.

1. How much heat does the steam plant produce when it burns $x_1$ tons of A and $x_2$ tons of B ?
2. Suppose the output of the steam plant is described by a vector that lists the amounts of heat, sulfur dioxide, and particulate matter. Express this output as a linear combination of two vectors, assuming that the plant burns $x_1$ tons of A and $x_2$ tons of B .
3. $[\mathbf{M}]$ Over a certain time period, the steam plant produced 162 million Btu of heat, $23,610 \mathrm{~g}$ of sulfur dioxide, and 1623 g of particulate matter. Determine how many tons of each type of coal the steam plant must have burned. Include a vector equation as part of your solution.

??? answer "&nbsp;"
    1. The amount of heat produced when the steam plant burns $x_1$ tons of anthracite and $x_2$ tons of bituminous coal is $27.6 x_1+30.2 x_2$ million Btu.
    2. The total output produced by $x_1$ tons of anthracite and $x_2$ tons of bituminous coal is given by the vector $x_1\left[\begin{array}{c}27.6 \\ 3100 \\ 250\end{array}\right]+x_2\left[\begin{array}{c}30.2 \\ 6400 \\ 360\end{array}\right]$.
    3. The steam plant burned $3.9$ tons of anthracite coal and $1.8$ tons of bituminous coal.

**Exercise 10** (1.4.6)

Use the definition of $A \mathbf{x}$ to write the matrix equation as a vector equation, or vice versa.

6. $\left[\begin{array}{rr}2 & -3 \\ 3 & 2 \\ 8 & -5 \\ -2 & 1\end{array}\right]\left[\begin{array}{r}-3 \\ 5\end{array}\right]=\left[\begin{array}{r}-21 \\ 1 \\ -49 \\ 11\end{array}\right]$

??? answer "&nbsp;"
    $-3 \cdot\left[\begin{array}{r}2 \\ 3 \\ 8 \\ -2\end{array}\right]+5 \cdot\left[\begin{array}{r}-3 \\ 2 \\ -5 \\ 1\end{array}\right]=\left[\begin{array}{r}-21 \\ 1 \\ -49 \\ 11\end{array}\right]$

**Exercise 11** (1.4.8)

Use the definition of $A \mathbf{x}$ to write the matrix equation as a vector equation, or vice versa.

8. $z_1\left[\begin{array}{r}2 \\ -4\end{array}\right]+z_2\left[\begin{array}{r}-1 \\ 5\end{array}\right]+z_3\left[\begin{array}{r}-4 \\ 3\end{array}\right]+z_4\left[\begin{array}{l}0 \\ 2\end{array}\right]=\left[\begin{array}{r}5 \\ 12\end{array}\right]$

??? answer "&nbsp;"
    $\left[\begin{array}{rrrr}2 & -1 & -4 & 0 \\ -4 & 5 & 3 & 2\end{array}\right]\left[\begin{array}{l}z_1 \\ z_2 \\ z_3 \\ z_4\end{array}\right]=\left[\begin{array}{r}5 \\ 12\end{array}\right]$

**Exercise 12** (1.4.11)

Given $A$ and $\mathbf{b}$, write the augmented matrix for the linear system that corresponds to the matrix equation $A \mathbf{x}=\mathbf{b}$. Then solve the system and write the solution as a vector.

$A=\left[\begin{array}{rrr}1 & 3 & -4 \\ 1 & 5 & 2 \\ -3 & -7 & 6\end{array}\right], \mathbf{b}=\left[\begin{array}{r}-2 \\ 4 \\ 12\end{array}\right]$

??? answer "&nbsp;"
    $\mathbf{x}=\left[\begin{array}{l}x_1 \\ x_2 \\ x_3\end{array}\right]=\left[\begin{array}{r}-11 \\ 3 \\ 0\end{array}\right]$

**Exercise 13** (1.4.17, 1.4.18)

Refer to the matrices $A$ and $B$ below. Make appropriate calculations that justify your answers and mention an appropriate theorem.

$$
A=\left[\begin{array}{rrrr}
1 & 3 & 0 & 3 \\
-1 & -1 & -1 & 1 \\
0 & -4 & 2 & -8 \\
2 & 0 & 3 & -1
\end{array}\right] \quad B=\left[\begin{array}{rrrr}
1 & 4 & 1 & 2 \\
0 & 1 & 3 & -4 \\
0 & 2 & 6 & 7 \\
2 & 9 & 5 & -7
\end{array}\right]
$$

1. How many rows of $A$ contain a pivot position? Does the equation $A \mathbf{x}=\mathbf{b}$ have a solution for each $\mathbf{b}$ in $\mathbb{R}^4$ ?
2. Can every vector in $\mathbb{R}^4$ be written as a linear combination of the columns of the matrix $B$ above? Do the columns of $B$ span $\mathbb{R}^3$ ?

??? answer "&nbsp;"
    1. $A \mathbf{x}=\mathbf{b}$ does not have a solution for each $\mathbf{b}$ in $\mathbb{R}^4$.
    2.  Not all vectors in $\mathbb{R}^4$ can be written as a linear combination of the columns of $B$. The columns of $B$ certainly do not span $\mathbb{R}^3$.

**Exercise 14** (1.5.7)

Describe all solutions of $A \mathbf{x}=\mathbf{0}$ in parametric vector form, where $A$ is row equivalent to the given matrix.

$\left[\begin{array}{llll}1 & 3 & -3 & 7 \\ 0 & 1 & -4 & 5\end{array}\right]$

??? answer "&nbsp;"
    $\mathbf{x}=\left[\begin{array}{l}x_1 \\ x_2 \\ x_3 \\ x_4\end{array}\right]=\left[\begin{array}{c}-9 x_3+8 x_4 \\ 4 x_3-5 x_4 \\ x_3 \\ x_4\end{array}\right]=\left[\begin{array}{c}-9 x_3 \\ 4 x_3 \\ x_3 \\ 0\end{array}\right]+\left[\begin{array}{c}8 x_4 \\ -5 x_4 \\ 0 \\ x_4\end{array}\right]=x_3\left[\begin{array}{r}-9 \\ 4 \\ 1 \\ 0\end{array}\right]+x_4\left[\begin{array}{r}8 \\ -5 \\ 0 \\ 1\end{array}\right]$

**Exercise 15** (1.5.15)

Describe and compare the solution sets of $x_1+5 x_2-$ $3 x_3=0$ and $x_1+5 x_2-3 x_3=-2$.

??? answer "&nbsp;"
    The solution set of the homogeneous equation is the plane through the origin in $\mathbf{R}^3$ spanned by $\mathbf{u}$ and $\mathbf{v}$. The solution set of the nonhomogeneous equation is parallel to this plane and passes through the point $\mathbf{p}=\left[\begin{array}{r}-2 \\ 0 \\ 0\end{array}\right]$.

**Exercise 16** (1.5.23)

Mark each statement True or False. Justify each answer.

1. A homogeneous equation is always consistent.
2. The equation $A \mathbf{x}=\mathbf{0}$ gives an explicit description of its solution set.
3. The homogeneous equation $A \mathbf{x}=\mathbf{0}$ has the trivial solution if and only if the equation has at least one free variable.
4. The equation $\mathbf{x}=\mathbf{p}+t \mathbf{v}$ describes a line through $\mathbf{v}$ parallel to $\mathbf{p}$.
5. The solution set of $A \mathbf{x}=\mathbf{b}$ is the set of all vectors of the form $\mathbf{w}=\mathbf{p}+\mathbf{v}_h$, where $\mathbf{v}_h$ is any solution of the equation $A \mathbf{x}=\mathbf{0}$.

??? answer "&nbsp;"
    1. True. See the first paragraph of the subsection titled Homogeneous Linear Systems.
    2. False. The equation $A \mathbf{x}=\mathbf{0}$ gives an implicit description of its solution set. See the subsection entitled Parametric Vector Form.
    3. False. The equation Ax =0 always has the trivial solution. The box before Example 1 uses the word nontrivial instead of trivial.
    4. False. The line goes through $\mathbf{p}$ parallel to $\mathbf{v}$. See the paragraph that precedes Fig. 5.
    5. False. The solution set could be empty! The statement (from Theorem 6) is true only when there exists a vector $\mathbf{p}$ such that $A \mathbf{p}=\mathbf{b}$.

**Exercise 17** (1.5.24)

Mark each statement True or False. Justify each answer.

1. A homogeneous system of equations can be inconsistent.
2. If $\mathbf{x}$ is a nontrivial solution of $A \mathbf{x}=\mathbf{0}$, then every entry in $\mathbf{x}$ is nonzero.
3. The effect of adding $\mathbf{p}$ to a vector is to move the vector in a direction parallel to $\mathbf{p}$.
4. The equation $A \mathbf{x}=\mathbf{b}$ is homogeneous if the zero vector is a solution.

??? answer "&nbsp;"
    1. False. The trivial solution is always a solution to a homogeneous system of linear equations.
    2. False. A nontrivial solution of $A \mathbf{x}=\mathbf{0}$ is any nonzero $\mathbf{x}$ that satisfies the equation. See the sentence before Example 2.
    3. True. See the paragraph following Example 3.
    4. True. If the zero vector is a solution, then $\mathbf{b}=A \mathbf{x}=A \mathbf{0}=\mathbf{0}$.
    5. True. See Theorem 6.