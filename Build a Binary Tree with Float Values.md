Ex. No: 15A - Build a Binary Tree with Float Values

AIM:
To write a Python program to build a binary tree with a root, left, and right node using floating-point values.

ALGORITHM:
Prompt the user to enter three floating-point values:

One for the root node.

One for the left child.

One for the right child.

Step 2: Node Creation
Create a root node using the entered root value.

Create a left child node using the left value.

Create a right child node using the right value.

Step 3: Tree Construction
Assign:

Left child to root.left.

Right child to root.right.

Step 4: Display
Print the structure of the binary tree:

Display the root node.

Show its left and right child values properly formatted (if needed, use two decimal places).


PYTHON PROGRAM
```
from binarytree import Node
def _build_bst_from_sorted_values(sorted_values):
    if len(sorted_values)==0:
        return None
    mid=len(sorted_values)//2
    root=Node(sorted_values[mid])
    root.left=_build_bst_from_sorted_values(sorted_values[:mid])
    root.right=_build_bst_from_sorted_values(sorted_values[mid+1:])
    return (root)
def insert_BST(val):
    global a
    if val in a:
        return False
    else:
        a.append(val)
        tree=_build_bst_from_sorted_values(sorted(a))
        return tree
def display(T):
    for i in T.values:
        print(i,"-->",end="")
a=[3,1,4,2]  
val=int(input())
print("BST before insertion:")
bst=_build_bst_from_sorted_values(sorted(a))
display(bst)
t1=insert_BST(val)
print("\nBST after insertion:")
display(t1)

```
OUTPUT
![image](https://github.com/user-attachments/assets/7d8b90eb-8e51-43f6-893d-32ce740abdd9)

RESULT
Thus the Python program to build a binary tree with a root, left, and right node using floating-point values was successfully implemented and verified.
