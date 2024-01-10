# Uniform Quantization
--- 
uniform scalar quantizer partitions the domain of input values into equally spaced intervals, except possibly at the two outer intervals. 
- The end points of partition intervals are called the quantizer’s decision boundaries. 
- The output or reconstruction value corresponding to each interval is taken to be the midpoint of the interval. 
- The length of each interval is referred to as the step size, denoted by the symbol $\Delta$

Uniform scalar quantizers are of two types: [[midrise quantizer]] and [[midtread quantizer]]:
![[Pasted image 20231212155543.png]]

The goal for the design of a successful uniform quantizer is to minimize the [[distortion measure|distortion]] for a given source input with a desired number of output values. This can be done by adjusting the step size $\Delta$ to match the input statistics.

Let $B=\{b_{0}, b_{1}, \dots, b_{m}\}$ to be the set of descision boundaries and  $Y=\{y_{1}, y_{2}, \dots, y_{m}\}$ to be the set of reconstruction values. Suppose the input is uniformly distributed in the interval $[-X_{max}, X_{max}]$, then the rate of quantizer is:
$$
R=\lceil \log_{2}M \rceil 
$$
This means that $R$ is the number of bits required to code $M$ things. The step size $\Delta$ is given by:
$$
\Delta = \frac{2X_{max}}{M}
$$
We could write this in terms of $b$:
$$
b_{i}=\left(  i-\frac{M}{2} \right)\Delta
$$