# Line Types
1. $\begin{bmatrix}
1&0&c_1&d_1\\
0&1&c_2&d_2
\end{bmatrix}$
aka
$\begin{cases}
x+c_1z+d_1w &=& 0\\
y+c_2z+d_2w &=& 0\end{cases}$

2.  $\begin{bmatrix}
1&b_1&0&d_1\\
0&0&1&d_2
\end{bmatrix}$
aka
$\begin{cases}
x+b_1y+d_1w &=& 0\\
z+d_2w &=& 0\end{cases}$

3.  $\begin{bmatrix}
1&b_1&c_1&0\\
0&0&0&1
\end{bmatrix}$
aka
$\begin{cases}
x+b_1y+c_1z &=& 0\\
w &=& 0\end{cases}$

4.  $\begin{bmatrix}
0&1&0&d_1\\
0&0&1&d_2
\end{bmatrix}$
aka
$\begin{cases}
y+d_1w &=& 0\\
z+d_2w &=& 0\end{cases}$

5.  $\begin{bmatrix}
0&1&c_1&0\\
0&0&0&1
\end{bmatrix}$
aka
$\begin{cases}
y+c_1z &=& 0\\
w &=& 0\end{cases}$

6.  $\begin{bmatrix}
0&0&1&0\\
0&0&0&1
\end{bmatrix}$
aka
$\begin{cases}
z &=& 0\\
w &=& 0\end{cases}$


## Questions
- Let $n\equiv 1\pmod 3$ and $n<27$. Is it possible to have a surface with $n$ lines of type $i$ where $i\in\{1,2,\dots,5\}$.

- What is the maximum number of lines of a given type?
  1. $\geq 24$
  2. ?
  3. ?
  4. ?
  5. 3

      Proof: Consider a generic cubic monic polynomial in variables $x,y,z$:

      $$*x^2y+*x^2z+*xy^2+*xz^2+*xyz+*y^3+*y^2z+*yz^2+*z^3$$

  6. 1
