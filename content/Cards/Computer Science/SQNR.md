# Signal-to-Quantization Noise Ratio (SQNR)
---
For a quantization accuracy of N bits per sample, the ==peak SQNR ==can be simply expressed:
$$
\text{SQNR}=20*\log_{10}\frac{V_{\text{signal}}}{V_{noise}} = 20*\log_{10}\frac{2^{N-1}}{\frac{1}{2}} = 20*N*\log_{2}=6.02 \text{ N(dB)}
$$
Dynamic range is the ratio of maximum to minimum absolute values of the signal: $\frac{V_{max}}{V_{min}}$