Ex. No: 15C - Expression Tree with Inorder and Postorder Traversal

AIM:
To write a Python program to build the given expression tree and print the inorder and postorder traversals.

ALGORITHM:
🔸 1. Build Expression Tree
Initialize an empty stack.

For each token in the postfix expression:

If the token is an operand (number):

Create a new node with the operand.

Push it to the stack.

If the token is an operator (+, -, *, /):

Pop two nodes from the stack: right, then left.

Create a new node with the operator.

Set its left and right children.

Push this new node back to the stack.

At the end, the top of the stack is the root of the expression tree.

🔸 2. Inorder Traversal (left, root, right)
Recursively:

Traverse the left subtree.

Visit the root (operator or operand).

Traverse the right subtree.

Add parentheses if desired for clarity.

🔸 3. Postorder Traversal (left, right, root)
Recursively:

Traverse the left subtree.

Traverse the right subtree.

Visit the root.



PROGRAM:

```
from binarytree import build
nodes=[10,12,5,3,4,11,2,None,None,6,7,None,None,None,8]
root=build(nodes)
print("Binary tree:")
for i in (root.values):
  print(i,"-->",end="")
print("\nlevel order traversal:",root.levelorder)
print("\nInorder traversal:",root.inorder)
print("\nPreorder traversal:",root.preorder)
print("\nPostorder traversal:",root.postorder)
```

OUTPUT
![image](https://github.com/user-attachments/assets/1c1b14a9-4925-4d27-ac65-06ba2516135b)

RESULT
Thus, Python program to build the given expression tree and print the inorder and postorder traversals was uccessfully implemented and verified.
