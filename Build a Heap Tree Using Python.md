Ex. No: 15D - Build a Heap Tree Using Python

AIM:
To write a Python program to build a heap tree using appropriate Python package and function.

ALGORITHM:
Initialize a list with elements you want to organize into a heap.

Import the heapq module.

Convert the list into a heap using heapq.heapify(list) — this rearranges the list in-place to satisfy the heap property.

You can now:

Use heapq.heappush(heap, item) to insert an element while maintaining the heap.

Use heapq.heappop(heap) to remove and return the smallest element.


PROGRAM:

```
from binarytree import heapq,build,Node
def heaptree(L):
    nodes=L
    root=build(nodes)
    for i in root.values:
        print(i,"-->",end="")
    print("\nHeight : ",root.height)
    print("Is max heap? : ",root.is_max_heap)
    print("Is complete tree? : ",root.is_complete)
```

OUTPUT
![image](https://github.com/user-attachments/assets/baf8ea87-c601-4d4d-b570-2c18d0505acd)


RESULT
Thus, Python program to build a heap tree using appropriate Python package and function was successfully implemeted and verified.
