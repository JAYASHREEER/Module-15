![image](https://github.com/user-attachments/assets/52e64a9c-e4b2-4752-9b79-250bc694d187)Ex. No: 15E - Build and Evaluate an Expression Tree

AIM:
To write a Python program to build and evaluate the given Expression tree.

ALGORITHM:
🔹 1. Input
An expression in postfix (Reverse Polish) notation is ideal, e.g., ["3", "4", "5", "*", "+"].

🔹 2. Build Tree Algorithm
Create a stack.

For each token in the postfix expression:

If token is an operand (number):

Create a node and push to stack.

If token is an operator (+, -, *, /):

Pop two nodes from stack: right and left.

Create a node with the operator.

Set popped nodes as its right and left children.

Push this new node to stack.

The final element in the stack is the root of the expression tree.

🔹 3. Evaluate Tree Algorithm
Recursively evaluate the tree:

If the node is a number → return it.

Else:

Evaluate left and right subtrees.

Apply the operator at the current node to the left/right results.


PROGRAM:

```
from binarytree import Node,build
x=['*',4,'-',5,'+',2,7]
x=build(x)
print(x.inorder)
print(x.postorder)
```

OUTPUT:
![image](https://github.com/user-attachments/assets/976f6845-8c19-4743-8989-1f894464591a)

RESULT:
Thus,Python program to build and evaluate the given Expression tree was successfully implemented and verified.

