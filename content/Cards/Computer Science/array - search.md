# Array Serach
---
Searching in an array is done throug a linear search, there can be other [[algorithms]] that are more optomized 

```cpp
int linearSearch(int A[], int n, int key)
{
    for (int i = 0; i < n; i = i + 1)
    {
        if (A[i] == key)
            return i
    }
    return -1
}
```
