# Big O

Big O notation is a way of expressing the efficiency of an algorithm in terms of how the running time or space usage grows as the input size increases.

`O(1)`: Constant time. The running time is independent of the input size.
```python
def OddOrEven(n):
    return "Even" if n % 2 else "Odd"
```

`O(log n)`: Logarithmic time. The running time grows logarithmically with the input size (half each iteration). An example of this is [[binary search]]
```python
def binarySearch(alist, item):
    first = 0
    last = len(alist)-1
    found = False

    while first <= last and not found:
        midpoint = (first + last)//2
        if alist[midpoint] == item:
            found = True
        else:
            if item < alist[midpoint]:
            last = midpoint-1
            else:
                first = midpoint+1

    return found
```

`O(n)`: Linear time. The running time grows linearly with the input size.
```python
shopping_list = ["Bread", "Butter", "The Nacho Libre soundtrack from the 2006 film Nacho Libre", "Reusable Water Bottle"]
for item in shopping_list:
    print(item)
```

`O(n^2)`: Quadratic time. The running time grows as the square of the input size.
```python
a = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
for i in a:
    for x in a:
        print("x")
```

`O(n log n)`: Linear logarithmic time. The running time grows as the product of the input size and the log of the input size.

![](https://hackr.io/blog/media/2-24.png)

- To determine the Big O complexity of an algorithm, you need to consider the worst-case scenario, which is the scenario where the algorithm takes the most time or space to complete.
- If we have an algorithm described as O(2n), we drop the 2 so it becomes O(n).
- $O(n²+n)$ becomes $O(n²)$. Only keep the larger one in Big O.
