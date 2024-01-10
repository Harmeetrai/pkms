# Depth-First Search
--- 
A _depth-first search_ is where you search deep into a branch and don’t move to the next one until you’ve reached the end. A [[stack]] can be used to traverse the tree.

![](https://static-assets.codecademy.com/Courses/CS102-Data-Structures-And-Algorithms/Breadth-First-Search-And-Depth-First-Search/Depth-First-Tree-Traversal.gif)

Frontier nodes stored in a stack create the deep dive of a depth-first search. Nodes added to the frontier early on can expect to remain in the stack while their sibling’s children (and their children, and so on) are searched. Depth-first search is not considered a complete algorithm since searching an infinite branch in a tree can go on forever. In this situation, an entire section of the tree would be left un-inspected.

```Python
def dfs(graph, start, visited=None):
    if visited is None:
        visited = set()
    visited.add(start)

    print(start)

    for next in graph[start] - visited:
        dfs(graph, next, visited)
    return visited
```
