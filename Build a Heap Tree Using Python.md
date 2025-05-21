Ex. No: 15D - Build a Heap Tree Using Python

AIM:
To write a Python program to build a heap tree using appropriate Python package and function.

ALGORITHM:
Step 1: Input Collection
Prompt the user to enter the number of elements in the heap.

Accept each element (integer or float) from the user and store it in a list.

Step 2: Heap Construction
Use the built-in heapq module.

Call heapq.heapify(list) to convert the list into a min-heap.

Step 3: Heap Operations (Optional)
You may also perform:

heappush(heap, item) – to insert a new item.

heappop(heap) – to remove and return the smallest item.

Step 4: Display
Print the heap list after heapify.

(Optional) Visualize the heap as a binary tree structure.

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
![image](https://github.com/user-attachments/assets/09e25c1c-edc1-4094-944d-dfaaf5d36591)

RESULT
Thus, the Python program to build a heap tree using appropriate Python package and function was successfully implemented and verified.
