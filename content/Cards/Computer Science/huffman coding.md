# Huffman Coding
---
Huffman Coding is a technique of compressing data to reduce its size without losing any of the details. It was first developed by David Huffman.

Encoding steps of the Huffman algorithm are described in the following bottom-up manner.
- Initialization: Put all symbols on a list sorted according to their frequency counts.
- Repeat until the list has only one symbol left:
	1. From the list pick two symbols with the lowest frequency counts. Form a Huffman subtree that has these two symbols as child nodes and create a parent node.
	2. Assign the sum of the children's frequency counts to the parent and insert it into the list such that the order is maintained.
	3. Delete the children from the list.
- Assign a codeword for each leaf based on the path from the root.

## How Huffman Coding [works](https://www.programiz.com/dsa/huffman-coding)?

Suppose the string below is to be sent over a network.

![string](https://cdn.programiz.com/sites/tutorial2program/files/hf-string.png "initial string")


Each character occupies 8 bits. There are a total of 15 characters in the above string. Thus, a total of `8 * 15 = 120` bits are required to send this string.

Huffman coding is done with the help of the following steps.

1. Calculate the frequency of each character in the string.
    ![frequency of string](https://cdn.programiz.com/sites/tutorial2program/files/hf-character-frequency.png "frequency of string")
2. Sort the characters in increasing order of the frequency. These are stored in a priority queue Q.
    ![huffman coding](https://cdn.programiz.com/sites/tutorial2program/files/hf-character-frequency-sorted.png "characters sorted in according to the frequency")
3. Make each unique character as a leaf node.
4. Create an empty node z. Assign the minimum frequency to the left child of z and assign the second minimum frequency to the right child of z. Set the value of the zas the sum of the above two minimum frequencies.
    
    ![huffman coding](https://cdn.programiz.com/sites/tutorial2program/files/hf-encoding-1.png "getting the sum of the least numbers")
5. Remove these two minimum frequencies from Q and add the sum into the list of frequencies (* denote the internal nodes in the figure above).
6. Insert node z into the tree.
7. Repeat steps 3 to 5 for all the characters.
    
    ![huffman coding](https://cdn.programiz.com/sites/tutorial2program/files/hf-encoding-2.png "getting the sum of the least numbers")
    
     
    
    ![huffman coding](https://cdn.programiz.com/sites/tutorial2program/files/hf-encoding-3.png "getting the sum of the least numbers")
8. For each non-leaf node, assign 0 to the left edge and 1 to the right edge.
    
    ![huffman coding](https://cdn.programiz.com/sites/tutorial2program/files/hf-encoding-4.png "getting the sum of the least numbers")

For sending the above string over a network, we have to send the tree as well as the above compressed-code. The total size is given by the table below.

|Character|Frequency|Code|Size|
|---|---|---|---|
|A|5|11|5*2 = 10|
|B|1|100|1*3 = 3|
|C|6|0|6*1 = 6|
|D|3|101|3*3 = 9|
|4 * 8 = 32 bits|15 bits||28 bits|

Without encoding, the total size of the string was 120 bits. After encoding the size is reduced to `32 + 15 + 28 = 75`.