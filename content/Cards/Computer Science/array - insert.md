# Array Insert
---
In an unsorted array, there is no order associated with the data elements. So we can directly insert elements at the end of the array. Suppose the size of the array is **n** and the index of the end element is **endIndex.**

- **if(endIndex >= n)**, then the array is full and it is not possible to insert any element further. 
- **if(endIndex < n)**, then there is some space left in the array and we can insert the element at **endIndex + 1**. As an output, we also return the new index of the end element which is endIndex + 1.

```cpp
int insert(int A[], int endIndex, int key, int n)
{
    if (endIndex >= n)
    {
        print("Array is full. Element could not be inserted")
        return -1
    }    
    A[endIndex + 1] = key
    return endIndex + 1
}
```

The time complexity of the insert operation at the end is $O(1)$.