# Shannon–Fano Algorithm
---
The Shannon–Fano algorithm was independently developed by Shannon at Bell Labs and Robert Fano at MIT. 

It is a top down approach where we sort the symbols according to the frequency count of their occurrences. Then, we recursively divide the symbols into two parts, each with approximately the same number of counts, until all parts contain only one symbol.

## Example
---
Let’s suppose the symbols to be coded are the characters in the word HELLO. The frequency count of the symbols is:

| Symbol | H| E|L|O|
| -|-|-|-|-|
| count|1|1|2|1

The encoding steps of the Shannon–Fano algorithm can be presented in the fol- lowing top-down manner:

1. Sort the symbols according to the frequency count of their occurrences.  
2. Recursively divide the symbols into two parts, each with approximately the same number of counts, until all parts contain only one symbol.

![[Pasted image 20231109155536.png]]

| Symbol | Count | $\log_{2}\frac{1}{p_{i}}$ | Code | Number of Bits Used|
|-|-|-|-|-|
| L | 2|1.32|0|2|
|H|1|2.32|10|2|
|E|1|2.32|110|3|
|O|1|2.32|111|3|

