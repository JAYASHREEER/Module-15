Ex. No: 15B - Build a Binary Search Tree Using Built-in Function

AIM:
To write a Python program to build a binary search tree using a built-in function.

ALGORITHM:

Input Handling:

Accept the number of nodes from the user.

Accept the node values.

Sort the list.

BST Construction:

Use the function _build_bst_from_sorted_values(sorted_values):

Find the mid-value.

Recursively build left and right subtrees.

Use binarytree module to create nodes.

Right Subtree Printing:

Use right_subtree(root):

Traverse and print only the right children of the root.

Postorder Traversal:

Use helper function postorder(node) to return nodes in postorder.

Validate BST:

Use is_bst(node, min_val, max_val):

Validate that all left nodes < root and right nodes > root recursively.

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
![image](https://github.com/user-attachments/assets/bdde968e-8fb8-482a-890b-080cd83a0516)

RESULT
Thus, the Python program to build a binary search tree using a built-in function was successfully implemented and verified.
