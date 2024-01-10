# Array Remove
--- 
We first search for the element to be deleted using linear search. Let's assume that the linear search returns the index of the element in the array, which we store in the variable **position**.

- If **position** is equal to -1, then the element to be deleted is not present in the array. 
- Otherwise, the element is present in the array. We delete the element by shifting all elements one position to the left, starting from the index **position + 1** up to **endIndex**.

```cpp
//Pseudocode
int delete(int A[], int endIndex, int key)
{
    int position = linearSearch(A, endIndex, key)
    if (position == - 1)
    {
        print("Element is not present in the array")
        return -1
    }
    
    for (int i = position; i < endIndex; i = i + 1)
        A[i] = A[i + 1]
    
    return endIndex - 1
}
```

Time complexity = Time complexity of the linear search + Time complexity of shifting elements to the left is $O(n) + O(n) = O(n)$.