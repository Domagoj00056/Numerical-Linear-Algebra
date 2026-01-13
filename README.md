# Numerical-Linear-Algebra
In this project we will study the performance of finite difference methods to solve the boundary value problem

$$
\frac{d^2 y}{dx^2} -xy = 0
$$
which is Airy's equation and arises in various applied problems including in optics and quantum mechanics. The equation has solutions which are defined in terms of the special functions $Ai(x)$ and $Bi(x)$ the [Airy functions](https://en.wikipedia.org/wiki/Airy_function) of first and second kind. 
The general solution is given by

$$
y(0) = 1 \qquad \& \qquad y(L) = 0
$$

$$
y(x) = C_1 Ai(x) + C_2 Bi(x)
$$

$$
y(0) = 1 \qquad \text{dd} \qquad y(L) = 0
$$

This therefore gives us a nice example to test finite difference approximations, the iterative solution of the set of linear equations which comprise the boundary value problem with a comparison to the `scipy` Airy functions. 

We will work with boundary conditions 



where $L$ is the length of the interval, to be varied during the project.



We saw in lectures that a boundary value problem of this type can be solved using finite difference differentiation matrices to discretise the operator on the left hand side of the equation. Recall from lectures that with second order finite differences the matrix for the first derivative is

$$D=\frac{1}{2h}\left(
{\begin{array}{cccccc}
0&1&0&.&.&0\\
-1&0&1&.&.&0\\
0&-1&0&1&.&0\\
.&.&.&.&.&.\\
.&.&.&.&.&.\\
0&.&.&.&-1&0\\
\end{array}}
\right)$$

and the second derivative

$$ D_2 = \frac{1}{h^2}\left(
{\begin{array}{cccccc}
-2&1&0&.&.&0\\
1&-2&1&.&.&0\\
0&1&-2&1&.&0\\
.&.&.&.&.&.\\
.&.&.&.&.&.\\
0&.&.&.&1&-2\\
\end{array}}
\right).$$
