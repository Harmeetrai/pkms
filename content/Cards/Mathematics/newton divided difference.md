# Newton Divided Difference
---
The newton divided difference is using to [[interpolation|interpolate]] a function given points:
$$
N(x)=[y_{0}]+[y_{0},y_{1}](x-x_{0})+\cdots +[y_{0},\ldots ,y_{k}](x-x_{0})(x-x_{1})\cdots (x-x_{{k-1}}).
$$
This is the divided difference table that could be used to calculate the interpolating polynomial
$$
{\begin{matrix}x_{0}&f(x_{0})&&\\&&{f(x_{1})-f(x_{0}) \over x_{1}-x_{0}}&\\x_{1}&f(x_{1})&&{{f(x_{2})-f(x_{1}) \over x_{2}-x_{1}}-{f(x_{1})-f(x_{0}) \over x_{1}-x_{0}} \over x_{2}-x_{0}}\\&&{f(x_{2})-f(x_{1}) \over x_{2}-x_{1}}&\\x_{2}&f(x_{2})&&\vdots \\&&\vdots &\\\vdots &&&\vdots \\&&\vdots &\\x_{n}&f(x_{n})&&\\\end{matrix}}
$$

