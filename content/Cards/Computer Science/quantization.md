# Quantization
---
- Quantization is a function that maps an input interval to one integer
- Can reduce the bits required to represent the source.
- Reconstructed result is generally not the original input

![[Pasted image 20231212153129.png]]

decision boundaries bi (on the left) are the bin boundaries and reconstruction levels yi (on the right) are output value of each bin by the dequantizer.

All bins have the same size except possibly for the two outer intervals:
- bi and yi are spaced evenly  
- The spacing of bi and yi are both ∆ (step size)

![[Pasted image 20231212153303.png]]

- [[uniform quantization]]
- [[nonuniform quantization]]