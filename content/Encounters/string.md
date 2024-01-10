# String

A string is a sequence of characters. Many tips that apply to [[array]] also apply to strings.

## Time Complexity
A strings is an array of characters, so the time complexities of basic string operations will closely resemble that of array operations.

| Operation | Big-O |
| ---- | ---- |
| Access | O(1) |
| Search | O(n) |
| Insert | O(n) |
| Remove | O(n) |

## Techniques
These are some of the techniques used in coding interviews

### Counting Characters
The most common way of counting characters is by using a [[hashmap]]. The space complexity for the hashmap is `O(1)` since there are 26 characters.

### String of unique characters
To count the unique characters in a word, the 26-bit bitmask can be used to indicate which lower case latin characters are inside the string:
```python
mask = 0  
for c in word:  
	mask |= (1 << (ord(c) - ord('a')))
```
To determine if two strings have common characters, perform `&` on the two bitmasks. If the result is non-zero, ie. `mask_a & mask_b > 0`, then the two strings have common characters.

### Anagram
An [[anagram]] is word switch or word play. The approaches are
1. sorting both strings should produce the same string, this takes `O(nlogn)` time and `O(logn)` space
2. counting the frequency of characters using a [[hashmap]], this takes `O(n)` time and `O(1)` space

### Palindrome
Here are ways to determine if a string is a [[palindrome]]:

- Reverse the string and it should be equal to itself.
- Have two pointers at the start and end of the string. Move the pointers inward till they meet. At every point in time, the characters at both pointers should match.

The order of characters within the string matters, so hash tables are usually not helpful.