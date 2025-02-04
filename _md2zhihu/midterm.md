
# First Order ODE

## Approach

To solve $y' = a(t)y + b(t)$:

1.  **Find $A(t)$:** Calculate the integral of $a(t)$:  $A(t) = \int a(t) , dt$. You can ignore the constant of integration for this step.

1.  **Calculate $e^{A(t)}$ and $e^{-A(t)}$:**  Compute the exponential of $A(t)$ and its negative.

1.  **Find the Integral Part:** Calculate the integral of  $b(t) \cdot e^{-A(t)}$:  $\int b(t)e^{-A(t)} , dt$.  Let's call the result of this integral $I(t)$.

1.  **Particular Solution:** A particular solution is given by $y_p(t) = e^{A(t)} \cdot I(t)$.

1.  **General Solution:** The general solution is $y(t) = c \cdot e^{A(t)} + y_p(t)$, where $c$ is an arbitrary constant.

## Sample

**1** For the solution $y(t)$ of the IVP $y' = (y/t) - 1$, $y(1) = \ln 2$, the value $y(2)$ is equal to:

-   [x] 0
-   [ ] 1
-   [ ] 2
-   [ ] $\ln 2$
-   [ ] $2\ln 2$

**2**. For the solution $y(t)$ of the IVP $y' = \frac{ty+1}{t^2+1}$, $y(0) = 2$, the value $y(1)$ is equal to:

-   [ ] $\sqrt{2}$
-   [ ] 2
-   [ ] $1+\sqrt{2}$
-   [ ] 3
-   [x] $1+2\sqrt{2}$

**3**. For the solution $y(t)$ of the IVP $y' = \frac{2y+1}{t}$, $y(1) = 2$, the value $y(2)$ is equal to:

-   [ ] 11/2
-   [ ] 13/2
-   [ ] 15/2
-   [ ] 17/2
-   [x] 19/2

# Separatble ODEs

## Approach

Given a separable ODE of the form:  $\frac{dy}{dt} = f(t)g(y)$

1.  **Separate:** $\frac{dy}{g(y)} = f(t) dt$

1.  **Integrate:**
    $\int \frac{1}{g(y)} dy = \int f(t) dt$

    Let $G(y) = \int \frac{1}{g(y)} dy$  and  $F(t) = \int f(t) dt$

    Then, the equation becomes: $G(y) = F(t) + C$  (where $C$ is the integration constant)

1.  **Apply Initial Condition $y(t_0) = y_0$:** $G(y_0) = F(t_0) + C$

1.  **Solve for $C$:** $C = G(y_0) - F(t_0)$

1.  **Specific Solution (Implicit Form):** $G(y) = F(t) + G(y_0) - F(t_0)$

1.  **Solve for $y$ (Explicit Form - if possible):**
    If possible, solve $G(y) = F(t) + C$ (or $G(y) = F(t) + G(y_0) - F(t_0)$) for $y$ to get $y = h(t, C)$ or $y = h(t, t_0, y_0)$.

1.  **Evaluate $y(t_1)$:**

Substitute $t = t_1$ into the explicit solution $y = h(t, C)$ (or implicit solution and solve for $y$) to find $y(t_1)$.

## Sample

1.  **For the solution** $y(t)$ **of the IVP** $y' = y\ln t$, $y(1) = 1$ **the value** $y(e)$ **is equal to**

    -   [ ] $e^{-2}$
    -   [ ] $e^{-1}$
    -   [ ] 1
    -   [x] $e$
    -   [ ] $e^{2}$

1.  **For the solution** $y(t)$ **of the IVP** $y' = y^2e^{-t}$, $y(0) = -1$ **the value** $y(-1)$ **is equal to**

    -   [ ] $e$
    -   [x] $1/(e-2)$
    -   [ ] $e+2$
    -   [ ] $1/(e+2)$
    -   [ ] $e-2$

1.  **For the solution** $y(t)$ **of the IVP** $y' = e^{t-2y}$, $y(0) = 0$ **the value** $y(1)$ **is contained in**

    -   [ ] $[0, \frac{1}{2}]$
    -   [x] $[\frac{1}{2}, 1]$
    -   [ ] $[1, \frac{3}{2}]$
    -   [ ] $[\frac{3}{2}, 2]$
    -   [ ] $[2, \infty)$

1.  **For the solution** $y(t)$ **of the IVP** $y' = (y^2-3)/(ty)$, $y(1) = 2$ **the value** $y(2)$ **is equal to**

    -   [ ] $\sqrt{6}$
    -   [x] $\sqrt{7}$
    -   [ ] $\sqrt{8}$
    -   [ ] $3$
    -   [ ] $\sqrt{10}$

1.  **For the solution** $y(t)$ **of the IVP** $y' = -t(y^2+1)$, $y(0) = 1$ **the value** $y(1)$ **is contained in**

    -   [x] $[0, \frac{1}{2}]$
    -   [ ] $[\frac{1}{2}, 1]$
    -   [ ] $[1, \frac{3}{2}]$
    -   [ ] $[\frac{3}{2}, 2]$
    -   [ ] $[2, \infty)$

# Exact Differential Equations and Integrating Factors

## Approach

**Goal:** Find integrating factor $\mu$ for ODE $M dx + N dy = 0$

**Exactness Check:** Is $M_y = N_x$?  If yes, ODE is exact.

**Integrating Factor Cases:**

<table>
<tr class="header">
<th style="text-align: left;"><span class="math inline"><em>μ</em></span> Type</th>
<th style="text-align: left;">Condition for <span class="math inline"><em>g</em></span></th>
<th style="text-align: left;">Formula for <span class="math inline"><em>g</em></span></th>
<th style="text-align: left;">Case No.</th>
<th style="text-align: left;">$’(s) = $ Relation</th>
</tr>
<tr class="odd">
<td style="text-align: left;"><span class="math inline"><em>μ</em>(<em>x</em>)</span></td>
<td style="text-align: left;"><span class="math inline">$\frac{M_y - N_x}{N} = g(x)$</span></td>
<td style="text-align: left;"><span class="math inline">$\frac{M_y - N_x}{N}$</span></td>
<td style="text-align: left;">①</td>
<td style="text-align: left;"><span class="math inline"><em>μ</em>′(<em>s</em>) = <em>g</em>(<em>s</em>)<em>μ</em>(<em>s</em>)</span></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span class="math inline"><em>μ</em>(<em>y</em>)</span></td>
<td style="text-align: left;"><span class="math inline">$\frac{M_y - N_x}{-M} = g(y)$</span></td>
<td style="text-align: left;"><span class="math inline">$\frac{M_y - N_x}{-M} = \frac{N_x - M_y}{M}$</span></td>
<td style="text-align: left;">②</td>
<td style="text-align: left;"><span class="math inline"><em>μ</em>′(<em>s</em>) =  − <em>g</em>(<em>s</em>)<em>μ</em>(<em>s</em>)</span></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span class="math inline"><em>μ</em>(<em>x</em><em>y</em>)</span></td>
<td style="text-align: left;"><span class="math inline">$\frac{M_y - N_x}{N_y - M_x} = g(xy)$</span></td>
<td style="text-align: left;"><span class="math inline">$\frac{M_y - N_x}{N_y - M_x}$</span></td>
<td style="text-align: left;">③</td>
<td style="text-align: left;"><span class="math inline"><em>μ</em>′(<em>s</em>) = <em>g</em>(<em>s</em>)<em>μ</em>(<em>s</em>)</span></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span class="math inline">$\mu(\frac{y}{x})$</span></td>
<td style="text-align: left;"><span class="math inline">$\frac{x^2(M_y - N_x)}{N_y + M_x} = g(\frac{y}{x})$</span></td>
<td style="text-align: left;"><span class="math inline">$\frac{x^2(M_y - N_x)}{N_y + M_x}$</span></td>
<td style="text-align: left;">④</td>
<td style="text-align: left;"><span class="math inline"><em>μ</em>′(<em>s</em>) =  − <em>g</em>(<em>s</em>)<em>μ</em>(<em>s</em>)</span></td>
</tr>
</table>

**Note:**

-   After finding the correct case and $g(s)$, calculate $\mu(s)$ by solving the $\mu'(s) = \pm g(s)\mu(s)$ relationship which leads to  $\mu(s) = e^{\pm \int g(s) ds}$.
-   Multiply the original ODE by $\mu$ to make it exact.

## Sample

1.  **The ODE** $(y^2 + y) dx - x dy$ **has the integrating factor**

    -   [ ] 0
    -   [ ] $x^{-1}$
    -   [ ] $y^{-1}$
    -   [ ] $x^{-2}$
    -   [x] $y^{-2}$

1.  **The ODE** $(x^4y^2 - y) dx + (x^2y^4 - x) dy = 0$ **has the integrating factor**

    -   [ ] $1/(xy)$
    -   [ ] 1
    -   [x] $1/(xy)^2$
    -   [ ] $1/(xy^2)$
    -   [ ] $1/(x^2y)$

1.  **The family of curves** $y = c/x^2, c \in \mathbb{R}$ **satisfies the ODE**

    -   [ ] $dy = x^{-2} dx$
    -   [ ] $dy = 2x^{-3} dx$
    -   [x] $2xy dx + x^2 dy = 0$
    -   [ ] $dx = dy$
    -   [ ] $2yx^{-3} dx - x^{-2} dy = 0$

1.  **The ODE** $3x dx - (y - 3x^2/y) dy$ **has the integrating factor**

    -   [ ] 0
    -   [ ] $x$
    -   [ ] $y$
    -   [ ] $x^2$
    -   [x] $y^2$

# Radius of Convergence

## Approach

To find the radius of convergence $R$ of a power series $\sum_{n=0}^{\infty} c_n z^n$:

1.  **Find the Coefficients:**

    -   Identify the coefficients $c_n$ in your power series. This is the number multiplying $z^n$.  Look for a pattern in these numbers as $n$ changes (0, 1, 2, 3...).
    -   **Important for series with "gaps":** If some powers of $z$ are missing (like $z^3, z^5$ are present but $z^2, z^4$ are not), the coefficient for the missing power is **zero**. You need to define $c_n$ for *all* $n \ge 0$.

1.  **Calculate $|c_n|^{1/n}$ (or Estimate Its Limit):**

    -   Take the absolute value of each coefficient $|c_n|$.
    -   Raise it to the power of $1/n$ (which is the same as taking the $n$-th root: $\sqrt[n]{|c_n|}$).
    -   Think about what happens to $|c_n|^{1/n}$ as $n$ becomes very large.  What is the limit as $n \to \infty$? Let's call this limit $L$.  *In many simple cases, you can just estimate this limit*.

1.  **Find the Limit Superior $L = \limsup_{n \to \infty} (|c_n|^{1/n})$ (More precisely):**

    -   For more complicated series, or if the limit from step 2 is not obvious, you might need to find the *limit superior*.  But often for introductory problems, the simple limit from step 2 works.  Assume for now that $L = \lim_{n \to \infty} (|c_n|^{1/n})$ exists.

1.  **Calculate Radius $R$:**

    -   Once you have $L$, the radius of convergence $R$ is:
        -   If $L > 0$, then $R = \frac{1}{L}$.
        -   If $L = 0$, then $R = \infty$ (series converges for all $z$).
        -   If $L = \infty$, then $R = 0$ (series only converges for $z = 0$).

**Simplified Steps (Formula Focus):**

1.  **Get $c_n$**: Identify the coefficient of $z^n$.
1.  **Calculate $|c_n|^{1/n}$**: Compute the $n$-th root of the absolute value of $c_n$.
1.  **Find $L = \lim_{n\to\infty} |c_n|^{1/n}$** (or $\limsup$).
1.  **Radius $R$**:
    -   $R = 1/L$, if $0 < L < \infty$
    -   $R = \infty$, if $L = 0$
    -   $R = 0$, if $L = \infty$

## Sample

1.  The power series $z + \frac{1}{2}z^2 + \frac{1}{4}z^4 + \frac{1}{8}z^8 + \frac{1}{16}z^{16} + \dots$ has radius of convergence

    -   [ ] 0
    -   [x] 1
    -   [ ] $\sqrt{2}$
    -   [ ] 2
    -   [ ] $\infty$

1.  The power series $\sum_{k=1}^{\infty} 2^{k}z^{k^2}$ has radius of convergence

    -   [ ] 0
    -   [ ] $\frac{1}{2}$
    -   [x] 1
    -   [ ] 2
    -   [ ] $\infty$

1.  The power series $z + z^2 + z^4 + z^8 + z^{16} + \dots$ has radius of convergence

    -   [ ] 0
    -   [ ] $\frac{1}{2}$
    -   [x] 1
    -   [ ] 2
    -   [ ] $\infty$

# Picard-Iteration

## Approach

**Problem-Solving Approach for Picard-Lindelöf Iterates**

To find $\phi_2(t)$ (the second Picard-Lindelöf iterate) for an Initial Value Problem (IVP) using the iterative formula:

$\phi_{k+1}(t) = y_0 + \int_{0}^{t} f(s, \phi_k(s)) , ds, \quad k = 0, 1, 2, \dots$

**Steps:**

1.  **Identify $f(t, y)$ and $y_0$ from the IVP:**
    For an IVP in the form $y' = f(t, y)$, $y(0) = y_0$,  determine the function $f(t, y)$ and the initial value $y_0$.

1.  **Determine the Initial Iteration $\phi_0(t)$:**
    The starting point for the iteration is the constant function based on the initial condition:
    $\phi_0(t) = y_0$

1.  **Calculate the First Iteration $\phi_1(t)$ (for k=0 in the formula):**
    Use the formula with $k=0$:
    $\phi_1(t) = y_0 + \int_{0}^{t} f(s, \phi_0(s)) , ds$
    Substitute $\phi_0(s) = y_0$ into $f(s, \phi_0(s))$, then evaluate the definite integral with respect to $s$ from $0$ to $t$.

1.  **Calculate the Second Iteration $\phi_2(t)$ (for k=1 in the formula):**
    Use the formula with $k=1$:
    $\phi_2(t) = y_0 + \int_{0}^{t} f(s, \phi_1(s)) , ds$
    Substitute the expression you found for $\phi_1(s)$ into $f(s, \phi_1(s))$, then evaluate the definite integral with respect to $s$ from $0$ to $t$.

1.  **Select the Correct Option:**
    Compare your calculated expression for $\phi_2(t)$ with the provided multiple-choice options and choose the one that matches.

**Formula-Based Steps Summary:**

1.  **Identify:** $f(t,y), y_0$ from $y' = f(t, y), y(0) = y_0$
1.  **Set:** $\phi_0(t) = y_0$
1.  **Calculate $\phi_1(t)$:**
    $\phi_1(t) = y_0 + \int_{0}^{t} f(s, \phi_0(s)) , ds$
1.  **Calculate $\phi_2(t)$:**
    $\phi_2(t) = y_0 + \int_{0}^{t} f(s, \phi_1(s)) , ds$
1.  **Match:** Compare $\phi_2(t)$ to options.

**Important Note:** The integral is always evaluated from $0$ to $t$, and in each step you're substituting the *previous* iterate into the function $f$. You are iteratively refining an approximation to the solution of the IVP.

## Sample

1.  The sequence $\phi_0, \phi_1, \phi_2, \dots$ of Picard-Lindelöf iterates for the IVP $y' = y+t$, $y(0) = -1$ has $\phi_2(t)$ equal to

    -   [ ] $\frac{1}{6}t^3$
    -   [ ] $-1 - t - \frac{1}{2}t^2$
    -   [x] $-1 - t + \frac{1}{6}t^3$
    -   [ ] $-1 - t - \frac{1}{2}t^2 + \frac{1}{6}t^3$
    -   [ ] $-1 - t$

1.  The sequence $\phi_0, \phi_1, \phi_2, \dots$ of Picard-Lindelöf iterates for the IVP $y' = y+2t$, $y(0) = -2$ has $\phi_2(t)$ equal to

    -   [ ] $-2 + 2t + \frac{1}{3}t^3$
    -   [ ] $-t^2 + \frac{1}{3}t^3$
    -   [x] $-2 - 2t + \frac{1}{3}t^3$
    -   [ ] $t^2 + \frac{1}{3}t^3$
    -   [ ] $1 + t + \frac{3}{2}t^2 + \frac{1}{3}t^3$

1.  The sequence $\phi_0, \phi_1, \phi_2, \dots$ of Picard-Lindelöf iterates for the IVP $y' = 2y+2$, $y(0) = 2$ has $\phi_2(t)$ equal to

    -   [ ] $2t + 6t^2$
    -   [ ] $2t + 5t^2$
    -   [x] $2 + 6t + 6t^2$
    -   [ ] $2t + 4t^2$
    -   [ ] $1 + 4t + 4t^2$

# Matrix Norms

## Approach

For a matrix $A$, the norm of $A$ can be defined in different ways. Two common matrix norms are the Operator Norm ($||A||$) and the Frobenius Norm ($||A||_F$).

**1. Operator Norm ($||A||$) - (Subordinate to Euclidean length)**

-   **Definition (using unit vectors parameterized by trigonometric functions):**

    Let $x = \begin{pmatrix} \sin x \\ \cos x \end{pmatrix}$, where $x \in [0, 2\pi]$. This $x$ represents any vector on the unit circle in $\mathbb{R}^2$. The Operator Norm of $A$ is defined as:$||A|| = \max \{||Ax||_2 \}$

    where $||Ax||_2$ is the Euclidean norm (length) of the vector $Ax$.  This means we find the maximum length of the vector $Ax$ when $x$ is a unit vector.

-   **Example Calculation for  $A = \begin{pmatrix} \frac{1}{2} & \pm 1 \\ 0 & \frac{1}{2} \end{pmatrix}$ :**

    Using $x = \begin{pmatrix} \sin x \\ \cos x \end{pmatrix}$, calculate $||Ax||_2$:

    $||A|| = \max_{x} \left\{ \left| \begin{pmatrix} \frac{1}{2} & \pm 1 \\ 0 & \frac{1}{2} \end{pmatrix} \begin{pmatrix} \sin x \\ \cos x \end{pmatrix} \right|_2 \right\}$

    $ = \max_{x} \left\{ \left| \begin{pmatrix} \frac{1}{2} \sin x \pm \cos x \\ \frac{1}{2} \cos x \end{pmatrix} \right|_2 \right\}$

    $ = \max_{x} \left\{ \sqrt{ \left( \frac{1}{2} \sin x \pm \cos x \right)^2 + \left( \frac{1}{2} \cos x \right)^2 } \right\}$

    $ = \sqrt{ \frac{3}{4} + \frac{\sqrt{2}}{2} } = \frac{1 + \sqrt{2}}{2} \approx 1.207 $

**2. Frobenius Norm ($||A||_F$):**

-   **Definition:**

    The Frobenius Norm of a matrix $A$ is defined as the square root of the sum of the squares of all its elements:$||A||_F = \sqrt{ \sum_{i,j} |a_{ij}|^2 }$

    This is essentially calculating the Euclidean norm of the matrix treated as a vector.

-   **Example Calculation for  $A = \begin{pmatrix} \frac{1}{2} & \pm 1 \\ 0 & \frac{1}{2} \end{pmatrix}$ :**

    $||A||_F = \sqrt{ \left(\frac{1}{2}\right)^2 + (\pm 1)^2 + (0)^2 + \left(\frac{1}{2}\right)^2 }$

    $ = \sqrt{ \frac{1}{4} + 1 + 0 + \frac{1}{4} } $

    $ = \sqrt{ \frac{1}{2} + 1 } = \sqrt{ \frac{3}{2} } = \frac{\sqrt{6}}{2} \approx 1.225 $

## Sample

1.  The matrix norm of $\begin{pmatrix} 2 & -3 \\ 3 & 2 \end{pmatrix}$ (subordinate to the Euclidean length on $\mathbb{R}^2$) is contained in the interval

    -   [ ] $[1, 2]$
    -   [ ] $[2, 3]$
    -   [x] $[3, 4]$
    -   [ ] $[4, 5]$
    -   [ ] $[5, 6]$

1.  The matrix norm of $\begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix}$ (subordinate to the Euclidean length on $\mathbb{R}^2$) is equal to

    -   [ ] 0
    -   [ ] 1
    -   [x] $\sqrt{2}$
    -   [ ] 2
    -   [ ] 4

1.  The matrix norm of $\begin{pmatrix} 2 & 1 \\ 1 & 0 \end{pmatrix}$ (subordinate to the Euclidean length on $\mathbb{R}^2$) is equal to

    -   [ ] 0
    -   [ ] 1
    -   [ ] $\sqrt{2}$
    -   [ ] 2
    -   [x] $1+\sqrt{2}$

# Phase Line

### **1. Basic Concepts**

-   **Autonomous Equation**: A differential equation ( y' = f(y) ) that depends only on the variable ( y ) and does not explicitly contain the independent variable ( t ).
-   **Equilibrium Points**: The values of ( y ) that make ( f(y) = 0 ), which are critical points where the solution remains constant.
-   **Phase Line**: A representation on the ( y )-axis that marks equilibrium points and analyzes the sign of ( y' ) in their vicinity to determine the increasing or decreasing trend of solutions.

---

### **2. Steps of Phase Line Analysis**

#### **(1) Find Equilibrium Points**

Solve the equation ( f(y) = 0 ) to obtain all equilibrium points ( y = c_1, c_2, \dots ).

#### **(2) Divide into Intervals**

Divide the ( y )-axis into several intervals using the equilibrium points as dividers. For example, if equilibrium points are ( y = -2, 0, 2 ), the intervals are:
[ (-\infty, -2),\ (-2, 0),\ (0, 2),\ (2, +\infty) ]

#### **(3) Analyze the Sign of the Derivative**

In each interval, choose any point ( y_0 ) and substitute it into ( f(y) ) to calculate the sign of ( y' ):

-   If ( y' > 0 ), the solution is increasing in this interval (arrow points to the right).
-   If ( y' < 0 ), the solution is decreasing in this interval (arrow points to the left).

#### **(4) Determine Stability of Equilibrium Points**

-   **Stable**: If arrows on both sides point towards the equilibrium point (e.g., ( \rightarrow \leftarrow )).
-   **Unstable**: If arrows on both sides point away from the equilibrium point (e.g., ( \leftarrow \rightarrow )).
-   **Semi-stable**: If on one side the arrow points towards, and on the other side it points away (e.g., ( \rightarrow \rightarrow ) or ( \leftarrow \leftarrow )).

---

### **3. Application Examples**

#### **Example 1**
: 
(
 y' = y^4 - 4y^2 
)
, initial value 
(
 y(4.29) = 1 
)

1.  **Equilibrium Points**: Solve ( y^4 - 4y^2 = 0 ), yielding ( y = -2, 0, 2 ).
1.  **Sign of Derivative in Intervals**:
    -   ( y > 2 ): ( y' = (+) ) (increasing, arrow to the right).
    -   ( 0 < y < 2 ): ( y' = (-) ) (decreasing, arrow to the left).
    -   ( -2 < y < 0 ): ( y' = (+) ) (increasing, arrow to the right).
    -   ( y < -2 ): ( y' = (-) ) (decreasing, arrow to the left).

1.  **Stability**:
    -   ( y = -2 ): Stable (arrows on both sides point towards it).
    -   ( y = 0 ): Semi-stable (right arrow points left, left arrow points right).
    -   ( y = 2 ): Unstable (arrows on both sides point away).

1.  **Solution Trend**: Initial value ( y = 1 ) is in ( (0, 2) ), ( y' < 0 ), solution is decreasing and trends towards ( y = 0 ).
    **Limit**: (\boxed{0})

#### **Example 2**
: 
(
 y' = y^3 - 7y + 6 
)
, initial value 
(
 y(0) = 0 
)

1.  **Equilibrium Points**: Solve ( y^3 - 7y + 6 = 0 ), yielding ( y = -3, 1, 2 ).
1.  **Sign of Derivative in Intervals**:
    -   ( y > 2 ): ( y' = (+) ).
    -   ( 1 < y < 2 ): ( y' = (-) ).
    -   ( -3 < y < 1 ): ( y' = (+) ).
    -   ( y < -3 ): ( y' = (-) ).

1.  **Stability**:
    -   ( y = -3 ): Unstable.
    -   ( y = 1 ): Stable.
    -   ( y = 2 ): Unstable.

1.  **Solution Trend**: Initial value ( y = 0 ) is in ( (-3, 1) ), ( y' > 0 ), solution is increasing and trends towards ( y = 1 ).
    **Limit**: (\boxed{1})

#### **Example 3**
: 
(
 y' = y^4 - 1 
)
, initial value 
(
 y(2021) = 0 
)

1.  **Equilibrium Points**: Solve ( y^4 - 1 = 0 ), yielding ( y = -1, 1 ).
1.  **Sign of Derivative in Intervals**:
    -   ( y > 1 ): ( y' = (+) ).
    -   ( -1 < y < 1 ): ( y' = (-) ).
    -   ( y < -1 ): ( y' = (+) ).

1.  **Stability**:
    -   ( y = -1 ): Stable.
    -   ( y = 1 ): Unstable.

1.  **Solution Trend**: Initial value ( y = 0 ) is in ( (-1, 1) ), ( y' < 0 ), solution is decreasing and trends towards ( y = -1 ).
    **Limit**: (\boxed{-1})

# Second Order ODE (homogenous and inhomogenous)

**$ay'' + by' + cy = r(x)$**

where $a$, $b$, $c$ are constants, and $r(x)$ is a function of $x$.

## Homogenous Second Order ODEs:  $ay'' + by' + cy = 0$

1.  **Write down the Characteristic Equation:  $ar^2 + br + c = 0$**

1.  **Solve the Characteristic Equation:**

    • Find the roots $\alpha_1, \alpha_2$ of this quadratic equation using the formula:
      $\alpha_{1,2} = \dfrac{-r_1 \pm \sqrt{r_1^2 - 4r_0}}{2}$

1.  **Check Root Type:**

    A. **Distinct Roots** ($\alpha_1 \neq \alpha_2$, when $r_1^2 \neq 4r_0$)

    1.  **Real Distinct Roots**

        -   General Solution: $y = C_1 e^{\alpha_1 t} + C_2 e^{\alpha_2 t}$

    1.  **Complex Conjugate Roots** ($\alpha_{1,2} = \zeta \pm i\beta$)

        -   General Solution: $y = e^{\zeta t}(C_1 \cos(\beta t) + C_2 \sin(\beta t))$

    B. **Repeated Roots** ($\alpha_1 = \alpha_2 = \alpha$, when $r_1^2 = 4r_0$)

    -   General Solution: $y = C_1 e^{\alpha t} + C_2 t e^{\alpha t}$

**Note:** In all cases, $C_1$ and $C_2$ are arbitrary constants determined by initial conditions.

## Inhomogeneous Second Order ODEs:  $ay'' + by' + cy = r(x)$

This section details the "Method of Undetermined Coefficients" (待定系数法) to find a particular solution $y_p(x)$ for the inhomogeneous equation.

### 1. Choosing the Form of $y_p(x)$ - Based on r(x)

The choice of the form of the particular solution $y_p(x)$ depends on the form of the function $r(x)$. Use the following table as a guide:

<table>
<tr class="header">
<th style="text-align: left;">Term in r(x)</th>
<th style="text-align: left;">Choice for <span class="math inline"><em>y</em><sub><em>p</em></sub>(<em>x</em>)</span></th>
</tr>
<tr class="odd">
<td style="text-align: left;"><span class="math inline"><em>k</em><em>e</em><sup><em>γ</em><em>x</em></sup></span></td>
<td style="text-align: left;"><span class="math inline"><em>C</em><em>e</em><sup><em>γ</em><em>x</em></sup></span></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span class="math inline"><em>k</em><em>x</em><sup><em>n</em></sup></span> (n = 0, 1, …)</td>
<td style="text-align: left;"><span class="math inline"><em>K</em><sub><em>n</em></sub><em>x</em><sup><em>n</em></sup> + <em>K</em><sub><em>n</em> − 1</sub><em>x</em><sup><em>n</em> − 1</sup> + ... + <em>K</em>₁<em>x</em> + <em>K</em>₀</span></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span class="math inline"><em>k</em>cos <em>ω</em><em>x</em></span></td>
<td style="text-align: left;"><span class="math inline"><em>K</em>cos <em>ω</em><em>x</em> + <em>M</em>sin <em>ω</em><em>x</em></span></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span class="math inline"><em>k</em>sin <em>ω</em><em>x</em></span></td>
<td style="text-align: left;"><span class="math inline"><em>K</em>cos <em>ω</em><em>x</em> + <em>M</em>sin <em>ω</em><em>x</em></span></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span class="math inline"><em>k</em><em>e</em><sup><em>α</em><em>x</em></sup>cos <em>ω</em><em>x</em></span></td>
<td style="text-align: left;"><span class="math inline"><em>e</em><sup><em>α</em><em>x</em></sup>(<em>K</em>cos<em>ω</em><em>x</em>+<em>M</em>sin<em>ω</em><em>x</em>)</span></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span class="math inline"><em>k</em><em>e</em><sup><em>α</em><em>x</em></sup>sin <em>ω</em><em>x</em></span></td>
<td style="text-align: left;"><span class="math inline"><em>e</em><sup><em>α</em><em>x</em></sup>(<em>K</em>cos<em>ω</em><em>x</em>+<em>M</em>sin<em>ω</em><em>x</em>)</span></td>
</tr>
</table>

where $k, γ, n, ω, α$ are known constants, and $C, K_i, M$ are undetermined coefficients that need to be determined by substituting $y_p(x)$ into the ODE.

### 2. Rules for Determining $y_p(x)$

-   **Basic Rule :**
    If $r(x)$ consists of terms listed in the table above, then choose $y_p(x)$ to have the corresponding form from the "Choice for $y_p(x)$" column and solve for the undetermined coefficients.

-   **Modification Rule :**
    If a term in the initially chosen $y_p(x)$ is already a solution to the corresponding homogeneous ODE ($ay'' + by' + cy = 0$), modify the choice for $y_p(x)$ by multiplying it by $x$ (or by $x^s$ if necessary, where $s$ is the smallest positive integer that makes no term in the modified $y_p(x)$ a solution to the homogeneous equation. Usually, multiplication by $x$ or $x^2$ is sufficient).

-   **Sum Rule :**
    If $r(x)$ is a sum of several terms, the particular solution $y_p(x)$ should be taken as the sum of the particular solutions corresponding to each term in $r(x)$, adjusting each component with the Modification Rule if needed.

---

**Basic Rule:** 若 $r(x)$ 包含在上表左列中，那么 $y_p(x)$ 就取右侧对应的形式，之后代入求系数

**Modification Rule:** 若使用Basic Rule选取的 $y_p(x)$ 是（6.1）对应的齐次ODE的解时，取 $y_p(x)$ 与 $x$ 的乘积生成新的 $y_p(x)$ (若齐次ODE有重根复、 且 $y_p(x)$ 就是那个根时， 乘以的是 $x^2$ )

**Sum Rule:** 若 $r(x)$ 是上表左列几种情况的加和， 那么 $y_p(x)$ 也是右侧对应的几种情况的加和， 注意，加和前根据Modification Rule对每项进行调整。

---

### 3. Example: Find the General Solution of $y'' - y = 16e^{-x}$

**STEP1: Solve the corresponding homogeneous equation y'' - y = 0**.  The characteristic equation is $r^2 - 1 = 0 \Rightarrow r = \pm 1$.  Therefore, the complementary function is

$y_c(x) = c_1e^x + c_2e^{-x}$

**STEP2: According to the table, assume  $y_p(x) = Be^{-x}$**. However, because it duplicates a term from the complementary function, according to the Modification Rule, we need to multiply by an $x$, so assume $y_p(x) = Bxe^{-x}$.

**STEP3: Substitute into the original equation, solve for coefficients**.

$16e^{-x} = y_p'' - y_p = B(x - 2)e^{-x} - (Bxe^{-x}) = -2Be^{-x}$
$\Rightarrow B = -8 \Rightarrow y_p(x) = -8xe^{-x}$

**Final general solution for y(x) is** $y(x) = -8xe^{-x} + c_1e^x + c_2e^{-x}$



Reference:

