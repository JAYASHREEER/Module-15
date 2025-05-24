Ex. No: 15B - Build a Binary Search Tree Using Built-in Function

AIM:
To write a Python program to build a binary search tree using a built-in function.

ALGORITHM:
```
1.Define a Node class:

Each node has a key, left, and right.

2.Define a BST class:

With a method to insert() a key.

Optionally a method to inorder() traverse (for checking correctness).

3.Insert Algorithm:

Start from the root.

If the key is less than the current node, go left.

If the key is greater, go right.

When you find an empty position (None), insert a new node there.

```

PROGRAM:

```
from binarytree import Node

def _build_bst_from_sorted_values(sorted_values):
    if (len(sorted_values))==0:
        return None
    mid = len(sorted_values)//2
    root = Node(sorted_values[mid])
    root.left = _build_bst_from_sorted_values(sorted_values[:mid])
    root.right = _build_bst_from_sorted_values(sorted_values[mid+1:])
    return (root)


def right_subtree(l):
    print("Right Subtree :")
    for i in l[2].values:
        print(i,"-->",end="")
    return 


a=[]
n = int(input())
for i in range (n):
    x = int(input())
    a.append(x)
p = sorted(a)
l = _build_bst_from_sorted_values(p)
print("Postorder :",l.postorder)
right_subtree(l)
print("\nIs this a Binary Search Tree? ",l.is_bst)
```

OUTPUT
![image](https://github.com/user-attachments/assets/6f656745-2412-43e9-b0c1-bb547bd41fc5)

RESULT
Thus,the Python program to build a binary search tree using a built-in function was successfully implemented and verified.
