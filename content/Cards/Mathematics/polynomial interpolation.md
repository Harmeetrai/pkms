# Polynomial Interpolation
---
In [[numerical analysis]], polynomial interpolation is the [[interpolation]] of a given bivariate data set by the polynomial of lowest possible degree that passes through the points of the dataset

[[linear algebra]] can be used to solve polynomial interpolation:
$$
{\displaystyle {\begin{bmatrix}1&x_{0}&x_{0}^{2}&\dots &x_{0}^{n}\\1&x_{1}&x_{1}^{2}&\dots &x_{1}^{n}\\1&x_{2}&x_{2}^{2}&\dots &x_{2}^{n}\\\vdots &\vdots &\vdots &\ddots &\vdots \\1&x_{n}&x_{n}^{2}&\dots &x_{n}^{n}\end{bmatrix}}{\begin{bmatrix}c_{0}\\c_{1}\\\vdots \\c_{n}\end{bmatrix}}={\begin{bmatrix}y_{0}\\y_{1}\\\vdots \\y_{n}\end{bmatrix}}.}
$$
The matrix on the left is called the [[vandermonde matrix]]

## Disadvantages of Polynomial Interpolation
- [[vandermonde matrix]] is ill-conditioned which can lead to large errors in the coefficients $c_{i}$
- solving dense matrix system requires $O(n^3)$ floating point operations (expensive)