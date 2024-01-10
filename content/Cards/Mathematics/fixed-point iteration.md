# Fixed-Point Iteration
---
The number $p$ is a fixed point for a given function $g$ if $g(p) = p$. Determine any fixed points of the functin $g(x)=x^2-2$
$$
p =g(p)=p^2-2 \text{ which implies that }   0=p^2-p-2=(p+1)(p-2)
$$
A fixed point intersects the graph of $y=x$ at points $p=-1$ and $p=2$
![[Pasted image 20231003105521.png]]

To approximate the fixed point of a function $g$ we choose an initial approximation $p_0$ and generate the sequence $\{p_n\}^{\infty}_{n=0}$ by letting $p_n=g(p_{n-1})$ for each $n\geq 1$: 
$$
p =\lim_{n\rightarrow \infty}p_n=\lim_{n\rightarrow \infty}g(p_{n-1})=g(\lim_{n\rightarrow \infty}p_{n-1})=g(p)
$$
![[Pasted image 20231003110247.png]]
