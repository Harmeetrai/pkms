# Lossless Compression
---
[[compression]] is the process of coding that will effectively reduce the total number of bits needed to represent certain information.

If the total number of bits required to represent the data before compression is $B_{0}$ and the total number of bits required to represent the data after compression is $B_{1}$, then we define the **compression ratio** as

$$
\text{compression ratio} = \frac{B_{0}}{B_{1}}
$$
## Self-Information
---
According to the famous scientist Claude E. Shannon, the [[entropy]] $\eta$ of an information source with alphabet $S = {s_{1},s_{2},...,s_{n}}$ is defined as
$$
\begin{align}
\eta=H(S)&=\sum_{i=1}^{n}p_{i}\log_{2}\frac{1}{p_{i}} \\
 &= -\sum_{i=1}^np_{i}\log_{2}p_{i}
\end{align}
$$
The term $\log_{2}\frac{1}{p_{i}}$ indicated the amount of information (self-information befined by Shannon)

# Runlength Coding
---
Instead of assuming a memoryless source, [[run-length coding]] (RLC) exploits memory present in the information source. 
- It is one of the simplest forms of data compression. 
- The basic idea is that if the information source we wish to compress has the property that symbols tend to form continuous groups
- Instead of coding each symbol in the group individually, we can code one such symbol and the length of the group.

## Variable-Length Coding
---
Since the entropy indicates the information content in an information source $S$, it leads to a family of coding methods commonly known as entropy coding methods. [[variable-length coding]] (VLC) is one of the best known such methods. 

- [[shannon–fano algorithm]]
- [[huffman coding]]
- [[LZW Coding]]
- [[arithmetic coding]]