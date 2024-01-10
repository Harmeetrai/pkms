# Lagrange Interpolation
---
In [[numerical analysis]], the Lagrange interpolating polynomial is the unique polynomial of lowest degree that [[interpolation|interpolates]] a given set of data.

Given a set of $k+1$ nodes ${x_{0},x_{1},\ldots ,x_{k}}$, which must all be distinct, $x_{j}\neq x_{m}$ for indices $j\neq m$, the **Lagrange basis** for polynomials of degree $\leq k$ for those nodes is the set of polynomials $\{\ell _{0}(x),\ell _{1}(x),\ldots ,\ell _{k}(x)\}$ each of degree $k$ which take values $\ell _{j}(x_{m})=0$ if $m\neq j$ and $\ell _{j}(x_{j})=1$. Each basis polynomial can be explicitly described by the product:

$${\displaystyle {\begin{aligned}\ell _{j}(x)&={\frac {(x-x_{0})}{(x_{j}-x_{0})}}\cdots {\frac {(x-x_{j-1})}{(x_{j}-x_{j-1})}}{\frac {(x-x_{j+1})}{(x_{j}-x_{j+1})}}\cdots {\frac {(x-x_{k})}{(x_{j}-x_{k})}}\\[10mu]&=\prod _{\begin{smallmatrix}0\leq m\leq k\\m\neq j\end{smallmatrix}}{\frac {x-x_{m}}{x_{j}-x_{m}}}.\end{aligned}}}$$
## Cost
The lagrange form of [[interpolation]] is a big improvement over the [[polynomial interpolation]] (using the [[vandermonde matrix]])
- there are no linear systems involved, reducing the computation cost
- cost is $O(n^2)$


