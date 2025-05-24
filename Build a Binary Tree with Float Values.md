Ex. No: 15A - Build a Binary Tree with Float Values

AIM:
To write a Python program to build a binary tree with a root, left, and right node using floating-point values.

ALGORITHM:
Step 1: Define the Node structure
Each node will contain:

A floating-point value.

A left child (can be None).

A right child (can be None).

Step 2: Create nodes
Create the root node with a float value.

Create left and right child nodes (also with float values).

Step 3: Link nodes
Assign the left node to root.left.

Assign the right node to root.right.


PYTHON PROGRAM
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
![image](https://github.com/user-attachments/assets/ac25cd61-338b-43f0-ab71-4729d1e68fb7)

RESULT
Thus,Python program to build a binary tree with a root, left, and right node using floating-point values was succsessfully implemented and verified.
