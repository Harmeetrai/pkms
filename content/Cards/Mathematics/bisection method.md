# Bisection Method
---
This is a method of solving the [[root-finding problem]]
- there is a root in interveral $[a,b]$ if there is a sign change ($-$ to $+$ or the other way)
- At each step the method divides the interval in two parts/halves by computing the midpoint $p_1 = \frac{(a+b)}{2}$ of the interval and the value of the function f(p) at that point.
- replace $a$ or $b$ with $p_1$ making sure there is still a sign change with $f(p_1)$ and $(f(a) \text{ or } f(b))$

![[Pasted image 20231015151708.png]]

Number of iterations required is given by to get an answer to a certain accuracy $\epsilon$ is given by $k$, where $[a,b]$ are the initial interval:
$$
k = \lceil log_2(b-a) - log(\epsilon)  \rceil
$$
### Algorithm
```pseudocode
input: Function f, 
       endpoint values a, b, 
       tolerance TOL, 
       maximum iterations NMAX
conditions: a < b, 
            either f(a) < 0 and f(b) > 0 or f(a) > 0 and f(b) < 0
output: value which differs from a root of f(x) = 0 by less than TOL
 
N ← 1
while N ≤ NMAX do // limit iterations to prevent infinite loop
    c ← (a + b)/2 // new midpoint
    if f(c) = 0 or (b – a)/2 < TOL then // solution found
        Output(c)
        Stop
    end if
    N ← N + 1 // increment step counter
    if sign(f(c)) = sign(f(a)) then a ← c else b ← c // new interval
end while
Output("Method failed.") // max number of steps exceeded
```