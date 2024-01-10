# Taylor Polynomials
---
Let $P_n(x)$ be the nth Taylor polynomial for $f$ about $x_0$ and let $R_n(x)$ be the remainder term (trucation error) associated with $P_n(x)$.

Suppose $f \in C^n[a,b],f^{(n+1)}$ exists on $[a,b]$, and $x_0 \in [a,b]$. For every $x \in [a,b]$ there exists a number $\xi(x)$ between $x_0$ and $x$ with
$$
f(x) = P_n(x) + R_n(x)
$$
where
$$
P_n(x) = f(x_0)+ f^`(x_0)(x-x_0)+\frac{f^ {``}(x_0)}{2!}(x-x_0)^2+...+\frac{f^{(n)}(x_0)}{n!}(x-x_0)^n = \sum_{k=0}^{n}\frac{f^{(k)}(x_0)}{k!}(x-x_0)^k
$$
and
$$
R_n(x) = \frac{f^{n+1}(\xi(x))}{(n+1)!}
(x-x_0)^{n+1}
$$

![[Taylor_Polynomial_.pdf]]

## Example
---
- Let $f(x)=cos(x)$ and $x_0=0$, determine the second Taylor Polynomial
	- Since $f\in C^\infty (\mathbb{R})$ Taylor's polynomial can be applied for $n \ge 0$
	- $$f^`(x)=sin(x), f^{``}(x)=-cos(x), f^{```}(x)=sin(x), f^{4}(x)=cos(x)$$
	- Finding the second Taylor Polynomial, $n=2,x_0=0$
	- $$cos(x)=f(0)+f^`(0)x+\frac{f{``}(0)}{2!}x^2+\frac{f^{```}(\xi(x))}{3!}x^3 = 1 -\frac{1}{2}x^2+\frac{1}{6}x^3sin(\xi(x))$$