# Breadth-First Search
---
A _breadth-first search_ is when you inspect every node on a level starting at the top of the tree and then move to the next level. A [[queue]] could be used to traverse the tree.

![](https://static-assets.codecademy.com/Courses/CS102-Data-Structures-And-Algorithms/Breadth-First-Search-And-Depth-First-Search/Breadth-First-Tree-Traversal.gif)

```python
def bfs(graph, root):

    visited, queue = set(), collections.deque([root])
    visited.add(root)

    while queue:

        # Dequeue a vertex from queue
        vertex = queue.popleft()
        print(str(vertex) + " ", end="")

        # If not visited, mark it as visited, and
        # enqueue it
        for neighbour in graph[vertex]:
            if neighbour not in visited:
                visited.add(neighbour)
                queue.append(neighbour)
```