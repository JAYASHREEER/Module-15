Ex. No: 15E - Build and Evaluate an Expression Tree

AIM:
To write a Python program to build and evaluate the given Expression tree.

ALGORITHM:
Build Expression Tree
Initialize an empty stack.

Traverse the postfix expression:

If the token is an operand:

Create a node and push it to the stack.

If the token is an operator:

Pop two nodes from the stack.

Create a new node with the operator as root and the two popped nodes as right and left children.

Push the new node back to the stack.

After traversal, the stack will have one element — the root of the expression tree.

Evaluate Expression Tree
Use recursion:

If the node is a leaf (operand), return its value.

Else, recursively evaluate the left and right subtrees.

Apply the operator at the current node to the results of the subtrees.


PROGRAM:
```
from binarytree import Node,build
x=['*',4,'-',5,'+',2,7]
x=build(x)
print(x.inorder)
print(x.postorder)
```
OUTPUT:
![image](https://github.com/user-attachments/assets/2027da80-0618-47d7-bfa2-442501186f68)

RESULT:
Thus, Python program to build and evaluate the given Expression tree was successfully implemented and verified.

